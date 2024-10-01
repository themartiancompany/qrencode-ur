# SPDX-License-Identifier: AGPL-3.0
#
# Maintainer: Truocolo <truocolo@aol.com>
# Maintainer: Pellegrino Prevete (tallero) <pellegrinoprevete@gmail.com>
# Maintainer: Florian Pritz< flo@xinu.at>
# Contributor: Dany Martineau <dany.luc.martineau@gmail.com>

_pkg=qrencode
pkgname="${_pkg}"
pkgver=4.1.1
pkgrel=3
pkgdesc="C library for encoding data in a QR Code symbol."
arch=(
  x86_64
  i686
  aarch64
  arm
  armv7l
  mips
  powerpc
  pentium4
)
depends=(
  'libpng'
)
makedepends=(
  'sdl2'
)
provides=(
  "lib${_pkg}=${pkgver}"
)
conflicts=(
  "lib${_pkg}"
)
_http="https://fukuchi.org"
_ns="works"
url="${_http}/${_ns}/${_pkg}"
license=(
  'GPL'
)
source=(
  "${url}/${_pkg}-${pkgver}.tar.bz2"
)
sha256sums=(
  'e455d9732f8041cf5b9c388e345a641fd15707860f928e94507b1961256a6923'
)

build() {
  cd \
    "${srcdir}/${_pkg}-${pkgver}"
  ./configure \
    --prefix=/usr
  make
}

check() {
  cd \
    "${srcdir}/${_pkg}-${pkgver}"
  make \
    check
}

package() {
  cd \
    "${srcdir}/${_pkg}-${pkgver}"
  make \
    prefix="${pkgdir}/usr" \
    install
}
