# Maintainer: Edoardo Maria Elidoro <edoardo.elidoro@gmail.com>
# Contributor: Dirk <lowph at lotje com>
# Contributor: Piotr Husiatynski <phusiatynski@gmail.com>

pkgname=xfce4-wmdock-plugin
pkgver=0.3.4
pkgrel=1
pkgdesc="The WMdock plugin is a compatibility layer for running WindowMaker dockapps on the XFCE desktop. It integrates the dockapps into a panel, closely resembling the look and feel of the WindowMaker dock or clip, respectively."
url="http://www.ibh.de/~ellguth/xfce4-wmdock-plugin.html"
arch=('i686' 'x86_64')
license="GPL"
depends=(xfce4-panel)
install=$pkgname.install
source=(http://archive.xfce.org/src/panel-plugins/xfce4-wmdock-plugin/0.3/$pkgname-$pkgver.tar.bz2)
md5sums=('b7e7f90add968dd71efd8d1b026b4373')

build() {
  cd "${srcdir}"/$pkgname-$pkgver
  ./configure --prefix=/usr
  make
}
package() {
  cd "${srcdir}"/$pkgname-$pkgver
  make DESTDIR="${pkgdir}" install
}
