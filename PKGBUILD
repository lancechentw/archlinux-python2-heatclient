# Maintainer: Lance Chen <cyen0312+aur@gmail.com>

pkgname=python2-heatclient
_pypiname=python-heatclient
pkgver=0.2.10
pkgrel=1
pkgdesc="OpenStack Orchestration API Client Library"
arch=(any)
url="https://pypi.python.org/pypi/python-heatclient/"
license=('Apache')
depends=('python2'
         'python2-iso8601>=0.1.9'
         'python2-keystoneclient>=0.9.0'
         'python2-pbr>=0.6'
         'python2-prettytable>=0.7'
         'python2-requests>=1.1'
         'python2-six>=1.7.0'
         'python2-yaml>=3.1.0')
makedepends=('python2-setuptools')
options=(!emptydirs)
source=("https://pypi.python.org/packages/source/p/${_pypiname}/${_pypiname}-${pkgver}.tar.gz")
md5sums=('f451ca000e4e2e739aeb351cccd2789d')

build() {
  cd "$_pypiname-$pkgver"
  /usr/bin/python2 setup.py build
}

package() {
  cd "$srcdir/$_pypiname-$pkgver"
  /usr/bin/python2 setup.py install --root="$pkgdir/" --optimize=1
}

# vim: sw=2 sts=2 et
