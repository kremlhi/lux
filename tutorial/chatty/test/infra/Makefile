.PHONY: all build test history clean info

TIMESTAMP=$(shell date +"%F_%T")
GITHASH=$(shell git rev-parse --verify --short HEAD)
TOPDIR=$(shell pwd | sed -e 's/tutorial.*/tutorial/')
LUXOPTS=\
	--config_dir=$(TOPDIR)/luxcfg \
	--revision=$(TIMESTAMP)_$(GITHASH)

all: build test

build:

test:
	lux $(LUX_OPTS) .

history:
	lux --history . .

clean:
	rm -rf lux_logs lux_history* chatty_*.log erl_crash.dump *~

info:
	@echo "TOPDIR=$(TOPDIR)"
	@echo "TIMESTAMP=$(TIMESTAMP)"
	@echo "GITHASH=$(GITHASH)"
	@echo "LUXOPTS=$(LUXOPTS)"
