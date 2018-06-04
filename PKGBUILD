# Maintainer: Florian Pritz< flo@xinu.at>
# Contributor: Dany Martineau <dany.luc.martineau@gmail.com>

pkgname=qrencode
pkgver=4.0.1
pkgrel=1
pkgdesc="C library for encoding data in a QR Code symbol."
arch=(x86_64)
depends=('libpng')
makedepends=(sdl)
url="https://megaui.net/fukuchi/works/qrencode/"
license=('GPL')
source=(https://megaui.net/fukuchi/works/${pkgname}/${pkgname}-${pkgver}.tar.bz2)
md5sums=('62950c75b1987a701aa5e70977ee960c')

build() {
  cd "${srcdir}/$pkgname-$pkgver"

  ./configure --prefix=/usr

  make
}

package() {
  cd "${srcdir}/$pkgname-$pkgver"

  make prefix="$pkgdir/usr" install
}
