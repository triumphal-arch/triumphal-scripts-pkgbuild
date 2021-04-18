# Maintainer: Peter Eisenmann <p3732 at getgoogleoff dot me>
pkgname=triumphal-scripts
pkgver=0.1.0
pkgrel=1
pkgdesc="Scripts for a nicer GNOME experience with Arch"
arch=('any')
url="https://github.com/triumphal-arch/triumphal-scripts"
license=('GPL3')
depends=()
makedepends=('git' 'ninja' 'meson')
source=("$pkgname::git+$url.git?unsigned#tag=$pkgver")
sha256sums=('SKIP')

build() {
	arch-meson $pkgname build
	meson compile -C build
}

package() {
	DESTDIR="$pkgdir" meson install -C build
}
