.PHONY: all clean

all:
	# Compiled versions of these binary modules are available at the url below.
	# This avoids a dependency on go and keeps the binaries out of our git repository.
	# https://ci-files.testing.ansible.com/test/integration/roles/test_binary_modules/
	cd library; \
	GOOS=linux   GOARCH=amd64   go build -o helloworld_linux_x86_64       helloworld.go; \
	GOOS=linux   GOARCH=arm64   go build -o helloworld_linux_aarch64      helloworld.go; \
	GOOS=linux   GOARCH=ppc64le go build -o helloworld_linux_ppc64le      helloworld.go; \
	GOOS=windows GOARCH=amd64   go build -o helloworld_win32nt_64-bit.exe helloworld.go; \
	GOOS=darwin  GOARCH=amd64   go build -o helloworld_darwin_x86_64      helloworld.go; \
	GOOS=freebsd GOARCH=amd64   go build -o helloworld_freebsd_amd64      helloworld.go; \
	GOOS=freebsd GOARCH=arm64   go build -o helloworld_freebsd_arm64      helloworld.go; \
    echo done

clean:
	rm -f library/helloworld_*
