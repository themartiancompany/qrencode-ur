# Maintainer: Florian Pritz< flo@xinu.at>
# Contributor: Dany Martineau <dany.luc.martineau@gmail.com>

pkgname=qrencode
pkgver=3.3.1
pkgrel=1
pkgdesc="C library for encoding data in a QR Code symbol."
arch=(i686 x86_64)
depends=('libpng>=1.5.0')
makedepends=(sdl)
url="http://megaui.net/fukuchi/works/qrencode/index.en.html"
license=('GPL')
options=(!libtool)
source=(http://megaui.net/fukuchi/works/${pkgname}/${pkgname}-${pkgver}.tar.bz2)
md5sums=('14920ba9d0515bddcaebfbd728229c5d')

build() {
  cd "${srcdir}/$pkgname-$pkgver"
#  autoreconf
  ./autogen.sh
  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}/$pkgname-$pkgver"

  make prefix="$pkgdir/usr" install
}
