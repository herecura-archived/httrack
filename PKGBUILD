# Maintainer: SpepS <dreamspepser at yahoo dot it>
# Contributor: Roman Kyrylych <roman@archlinux.org>
# Contributor: orelien <aurelien.foret@wanadoo.fr>

pkgname=httrack
pkgver=3.48.22
pkgrel=1
pkgdesc="An easy-to-use offline browser utility."
arch=('i686' 'x86_64')
url="http://www.httrack.com/"
license=('GPL')
depends=('bash' 'zlib')
options=('!libtool' '!makeflags')
install="$pkgname.install"
source=("http://download.httrack.com/$pkgname-$pkgver.tar.gz")
sha256sums=('b2831ad7b48e933959f83a9de8a72bcaa0f8eb87e9453ad85debd50d33a9c48f')

build() {
  cd "$pkgname-$pkgver"

  ./configure --prefix=/usr \
              --enable-static=no
  make
}

package() {
  cd "$pkgname-$pkgver"

  make DESTDIR="$pkgdir" install
}
