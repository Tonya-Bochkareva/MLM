func_lib = ../../ton/crypto/smartcont/stdlib.fc
fift_lib = ../../ton/crypto/fift/lib

.PHONY: build/main.fif
build/main.fif:
	mkdir -p $(@D) 
	func -AP $(func_lib) main.fc -o $@

.PHONY: test
test: test/int

.PHONY: test/int
test/int:
	find test/int -iname "*.fif" -exec \
		bin/test \
			-l $(func_lib) \
			--fift-lib $(fift_lib) \
			main.fc {} +
