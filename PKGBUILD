# Maintainer: Matt <matt005[at]gmail[dot]com>
pkgname=epeg
pkgver=0.9.1.042
pkgrel=1
pkgdesc="Insanely fast JPEG thumbnail scaling with the minimum fuss and CPU overhead. It makes use of libjpeg features of being able to load an image by only decoding the DCT coefficients needed to reconstruct an image of the size desired."
url="http://www.enlightenment.org/"
arch=('any')
license=('MIT')
depends=('libjpeg-turbo')
install='epeg.install'
source=("https://github.com/mattes/epeg/tarball/v${pkgver}")
md5sums=('07ae7bd430e7688403e44797a22723bf')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
}

