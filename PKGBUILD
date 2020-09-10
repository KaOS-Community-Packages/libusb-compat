pkgname=libusb-compat
pkgver=0.1.7
pkgrel=1
pkgdesc="Library to enable user space application programs to communicate with USB devices"
arch=('x86_64')
url="http://libusb.sourceforge.net/"
license=('LGPL')
depends=('libusb' 'sh')
source=("https://github.com/libusb/libusb-compat-0.1/releases/download/v$pkgver/$pkgname-$pkgver.tar.gz")
sha256sums=('0679ce38aa02498c1eea9c13398a0d2356883d574632a59c1e25274ed4925cf8')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr --disable-static
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
}

a
