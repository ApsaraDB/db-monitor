include ../../common.mk

PLUGIN_TARGET = ../../bin/plugins/polardb_pg_opensource/polardb_pg.so
PLUGIN_SRC=$(shell find . -name "*.go")
PLUGIN_MAIN=polardb_pg.go

all: prepare $(PLUGIN_TARGET)

prepare:
	@mkdir -p ../../bin/plugins/polardb_pg_opensource

$(PLUGIN_TARGET): $(PLUGIN_MAIN) $(PLUGIN_SRC)
	$(GC_ENV) $(GOCC) $(GC_PLUGIN_FLAGS) -o $@ $<

clean:
	$(GOCC) clean -mod=vendor && rm -rf ../../bin/plugins/polardb_pg_opensource
