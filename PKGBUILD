# Maintainer: HumbleSeer <jp01220414@icloud.com>
pkgname=silver-searcher-ng
pkgver=3.0.0
pkgrel=1
epoch=
pkgdesc="The Silver Searcher: A code-searching tool similar to ack, but faster. A fork of ggreer's the_silver_searcher."
arch=(x86_64)
url="https://github.com/silver-searcher/silver-searcher-ng"
license=(Apache)
groups=()
depends=(
    'pcre2'
    'xz'
    'zlib'
    'pkg-config'
)
makedepends=()
checkdepends=()
optdepends=()
provides=('the_silver_searcher')
conflicts=('the_silver_searcher')
install=
changelog=
source=("$pkgname-$pkgver::https://github.com/silver-searcher/silver-searcher-ng/archive/refs/tags/3.0.0.tar.gz")
sha256sums=('20aea0143241cb71b70a1717df00236f2d34a964b1f1eaa2f653cf1986615542')
validpgpkeys=()

prepare() {
	cd "$pkgname-$pkgver"
}

build() {
	cd "$pkgname-$pkgver"
    ./build --prefix=/usr
}

check() {
	cd "$pkgname-$pkgver"
	make -k check
}

package() {
	cd "$pkgname-$pkgver"
	make DESTDIR="$pkgdir/" install
}
