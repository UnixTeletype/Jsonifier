# Maintainer: Your Name <youremail@domain.com>
pkgname=jsonifier
pkgver=0.9.97
pkgrel=1
pkgdesc="A few classes for extremely fast json parsing/serializing in modern C++."
arch=('x86_64')
url="https://github.com/RealTimeChris/Jsonifier.git"
license=('MIT')
depends=('vcpkg')
makedepends=('cmake' 'gcc' 'make')
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("$pkgname-$pkgver.tar.gz"
        "$pkgname-$pkgver.patch")
noextract=()
sha256sums=()
validpgpkeys=()

prepare() {
	cd "$pkgname-$pkgver"
	patch -p1 -i "$srcdir/$pkgname-$pkgver.patch"
}

build() {
	cd "$pkgname-$pkgver"
	./configure --prefix=/usr
	make
}

check() {
	cd "$pkgname-$pkgver"
	make -k check
}

package() {
	cd "$pkgname-$pkgver"
	make DESTDIR="$pkgdir/" install
}
