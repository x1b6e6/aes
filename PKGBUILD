# Maintainer: x1b6e6 <ftdabcde@gmail.com>

pkgname=aes
pkgver=0.2.0
pkgrel=1
pkgdesc="encryption utility with very simple interface"
arch=('any')
url="https://github.com/x1b6e6/aes.git"
license=("MIT")
depends=("libgcrypt" "docopt")
makedepends=("gcc" "make" "cmake")

source=(
	"CMakeLists.txt"
	"aes.cc"
)

sha1sums=(
	"a14bc448b2c43536dffc1e6d63ea257dd6fa33ea"
	"8f54d022a70daf98aabd46f0fd810eca91d7495d"
)

build(){
	cd $srcdir
	cmake -Bbuild -G "Unix Makefiles"
	cmake --build build --target all
}

package() {
	cd "$srcdir"
	install -Dm755 "$srcdir/build/aes" "$pkgdir/usr/bin/aes"
}

# vim: set ts=4 sw=4 :
