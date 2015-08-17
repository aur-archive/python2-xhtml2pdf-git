# Maintainer: Francesco Marella <francesco.marella@anche.no>
# Contributor: Zhehao Mao <zhehao.mao@gmail.com>

pkgname=python2-xhtml2pdf-git
_gitname=xhtml2pdf
pkgver=0.0.4.r157.gef878d0
pkgrel=1
pkgdesc='PDF generator using HTML and CSS'
arch=('any')
url='http://pypi.python.org/pypi/xhtml2pdf/'
license=('Apache')
depends=('git' 'python2-distribute' 'python2-reportlab' 'python2-html5lib' 'python2-pypdf2-git' 'python2-pillow')
makedepends=('python2-distribute')
source=("git+https://github.com/chrisglass/xhtml2pdf.git")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$_gitname"
  git describe --tags | sed -r 's/([^-]*-g)/r\1/;s/-/./g'
}

package() {
	  cd "$srcdir/$_gitname"
	  python2 ./setup.py install --root="${pkgdir}" --prefix="/usr"
      #install -D -m644 LICENSE.txt "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE.txt"
}
