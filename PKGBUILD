pkgname=libusb-compat
pkgver=0.1.5
pkgrel=1
pkgdesc="Library to enable user space application programs to communicate with USB devices"
arch=('x86_64')
url="http://libusb.sourceforge.net/"
license=('LGPL')
depends=('libusb' 'sh')
source=("http://downloads.sourceforge.net/${pkgname%-*}/${pkgname}-${pkgver%.*}/$pkgname-$pkgver/${pkgname}-${pkgver}.tar.bz2")

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr --disable-static
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
}

md5sums=('2780b6a758a1e2c2943bdbf7faf740e4')
