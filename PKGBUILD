# Maintainer: Wei Qiu <qiuwei1987@gmail.com>
pkgname=libbow
pkgver=1.9
pkgrel=1
epoch=
pkgdesc="Bow is a library of C code useful for writing statistical text analysis, language modeling and information retrieval programs."
arch=('any')
url="http://www.cs.cmu.edu/~mccallum/bow/"
license=('GPL')
groups=()
depends=('perl')
makedepends=('gcc')
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=('http://archive.ubuntu.com/ubuntu/pool/universe/b/bow/bow_20020213.orig.tar.gz' 'http://archive.ubuntu.com/ubuntu/pool/universe/b/bow/bow_20020213-10.diff.gz' 'getline.patch')
noextract=()
md5sums=('1d47f13bba3b6caf2dee1986463c4f3f'
         'c710a2ce3721e89070d534121721bd6a'
         '4745109584dac142550185c44fa28b23')

build() {
  cd "$srcdir/bow-20020213"
  patch -p1 -i $srcdir/bow_20020213-10.diff 
  patch -p1 -i $srcdir/getline.patch
  ./configure --prefix=/opt/$pkgname
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make prefix="$pkgdir/opt/$pkgname" install
}
