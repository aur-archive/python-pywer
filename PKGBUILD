# Maintainer: William Giokas <1007380@gmail.com>

pkgname=python-pywer
_pkgname=pywer
pkgver=0.13
pkgrel=1
pkgdesc='A simple python-based AUR helper'
url='http://git.kaictl.net/wgiokas/pywer.git'
license=('MIT')
arch=('any')
provides=('python-pywer')
conflicts=('python-pywer')
makedepends=('python-setuptools' 'git')
depends=('python-requests' 'python-xdg' 'pyalpm')
source=("git+git://git.kaictl.net/wgiokas/pywer.git#tag=$pkgver")
md5sums=('SKIP')

check() {
  cd "$srcdir/$_pkgname"
  ./setup.py -q test -v
}

package() {
  cd "$srcdir/$_pkgname"
  ./setup.py -q install -O1 --prefix=/usr --root="$pkgdir"
  install -Dvm 644 _pywer "$pkgdir/usr/share/zsh/site-functions/_pywer"
}
