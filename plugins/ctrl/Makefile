include ../../common.mk

PLUGIN_TARGET = ../../bin/plugins/ctrl/ctrl.so
PLUGIN_SRC=$(shell find . -name "*.go")
PLUGIN_MAIN = ctrl.go

all: prepare $(PLUGIN_TARGET)

prepare:
	@mkdir -p ../../bin/plugins/ctrl

$(PLUGIN_TARGET): $(PLUGIN_MAIN) $(PLUGIN_SRC)
	$(GC_ENV) $(GOCC) $(GC_PLUGIN_FLAGS) -o $@ $<

clean:
	$(GOCC) clean -mod=vendor && rm -rf ../../bin/plugins/ctrl
