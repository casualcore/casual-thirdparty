
default:	build

clean:
	rm -rf Makefile /Users/albs/dev/casual/1.8/casual/middleware/http/inbound/bin

.PHONY:	default clean

build:
	$(MAKE) -f /Users/albs/dev/casual/1.8/casual/middleware/http/inbound/bin/Makefile

install:
	$(MAKE) -f /Users/albs/dev/casual/1.8/casual/middleware/http/inbound/bin/Makefile install

modules:
	$(MAKE) -f /Users/albs/dev/casual/1.8/casual/middleware/http/inbound/bin/Makefile modules

upgrade:
	/Users/albs/dev/casual/installation/nginx/sbin/nginx -t

	kill -USR2 `cat /Users/albs/dev/casual/installation/nginx/logs/nginx.pid`
	sleep 1
	test -f /Users/albs/dev/casual/installation/nginx/logs/nginx.pid.oldbin

	kill -QUIT `cat /Users/albs/dev/casual/installation/nginx/logs/nginx.pid.oldbin`

.PHONY:	build install modules upgrade
