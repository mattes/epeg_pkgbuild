# Maintainer: Matt <somebody[at]foo[dot]tld>
pkgname=epeg
pkgver=0.9.1.042
pkgrel=1
pkgdesc="Insanely fast JPEG thumbnail scaling with the minimum fuss and CPU overhead. It makes use of libjpeg features of being able to load an image by only decoding the DCT coefficients needed to reconstruct an image of the size desired."
url="http://www.enlightenment.org/"
arch=('any')
license=('MIT')
depends=('libjpeg-turbo')
install='epeg.install'
source=("http://www.server.tld/${pkgname}-${pkgver}.tar.gz")
md5sums=('a0afa52d60cea6c0363a2a8cb39a4095')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
}

