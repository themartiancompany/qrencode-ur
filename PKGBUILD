# Maintainer: Florian Pritz< flo@xinu.at>
# Contributor: Dany Martineau <dany.luc.martineau@gmail.com>

pkgname=qrencode
pkgver=3.1.1
pkgrel=2
pkgdesc="C library for encoding data in a QR Code symbol."
arch=(i686 x86_64)
depends=('libpng>=1.4.0')
makedepends=(sdl)
url="http://megaui.net/fukuchi/works/qrencode/index.en.html"
license=('GPL')
options=(!libtool)
source=(http://megaui.net/fukuchi/works/${pkgname}/${pkgname}-${pkgver}.tar.bz2 libpng14.diff)
md5sums=('e7feb2c2c65d0f2f4010a14da3ecdb89' '93e87b2751b0d422a08e96ccaae4d082')

build() {
  cd "${srcdir}/$pkgname-$pkgver"
  patch -p1 < "$srcdir/libpng14.diff"
  autoreconf
  ./autogen.sh
  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}/$pkgname-$pkgver"

  make prefix="$pkgdir/usr" install
}
