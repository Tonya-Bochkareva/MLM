func_lib = ../../ton/crypto/smartcont
fift_lib = ../../ton/crypto/fift/lib

.PHONY: test
test: test/int

.PHONY: test/int
test/int:
	find test/int -iname "*.fif" -exec \
		bin/test \
			-l $(func_lib) \
			--fift-lib $(fift_lib) \
			main.fc {} +
