# Maintainer: Antonio Rojas <nqn76sw@gmail.com>
# Contributor: Rémy Oudompheng <oudomphe@clipper.ens.fr>

pkgname=m4rie
pkgver=20140914
pkgrel=1
pkgdesc="Algorithms for linear algebra over F_2^e"
arch=('i686' 'x86_64')
url="http://m4ri.sagemath.org/"
license=('GPL')
depends=('m4ri')
source=(http://m4ri.sagemath.org/downloads/m4rie/$pkgname-$pkgver.tar.gz)
md5sums=('10e9fd98efb72568ee64c6510f4cc0de')

build() {
  cd $pkgname-$pkgver
  ./configure --prefix=/usr --with-openmp
  make
}

check() {
  cd $pkgname-$pkgver
  make check
}

package() {
  cd $pkgname-$pkgver
  make install DESTDIR="$pkgdir"
}

