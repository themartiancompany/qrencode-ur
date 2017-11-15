# Maintainer: Florian Pritz< flo@xinu.at>
# Contributor: Dany Martineau <dany.luc.martineau@gmail.com>

pkgname=qrencode
pkgver=4.0.0
pkgrel=1
pkgdesc="C library for encoding data in a QR Code symbol."
arch=(x86_64)
depends=('libpng')
makedepends=(sdl)
url="http://megaui.net/fukuchi/works/qrencode/"
license=('GPL')
source=(http://megaui.net/fukuchi/works/${pkgname}/${pkgname}-${pkgver}.tar.bz2)
md5sums=('f92ae29beb877f91df18957b4785b7f0')

build() {
  cd "${srcdir}/$pkgname-$pkgver"

  ./configure --prefix=/usr

  make
}

package() {
  cd "${srcdir}/$pkgname-$pkgver"

  make prefix="$pkgdir/usr" install
}
