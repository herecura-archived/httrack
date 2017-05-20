# Maintainer: SpepS <dreamspepser at yahoo dot it>
# Contributor: Roman Kyrylych <roman@archlinux.org>
# Contributor: orelien <aurelien.foret@wanadoo.fr>

pkgname=httrack
pkgver=3.49.2
pkgrel=1
pkgdesc="An easy-to-use offline browser utility."
arch=('i686' 'x86_64')
url="http://www.httrack.com/"
license=('GPL')
depends=('bash' 'zlib' 'desktop-file-utils' 'hicolor-icon-theme')
options=('!libtool' '!makeflags')
source=("http://download.httrack.com/$pkgname-$pkgver.tar.gz")
sha256sums=('3477a0e5568e241c63c9899accbfcdb6aadef2812fcce0173688567b4c7d4025')

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
