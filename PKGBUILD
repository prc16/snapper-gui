# Maintainer: prc16 <prc16 at protonmail dot com>

pkgname=snapper-gui
pkgver=0.1.1
pkgrel=1
pkgdesc="Gui for snapper, a tool of managing snapshots of Btrfs subvolumes and LVM volumes"
arch=(any)
url="https://github.com/prc16/snapper-gui"
license=('GPL2')
depends=('python3' 'gtk3' 'python-dbus' 'python-gobject' 'python-setuptools' 'gtksourceview3' 'snapper')
optdepends=('gksu: Access snapper-gui from application menu under GTK-base DE'
            'kdesu: Access snapper-gui from application menu under KDE')
makedepends=('git')
provides=('snapper-gui')
conflicts=('snapper-gui')
install=snapper-gui.install
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/prc16/snapper-gui/archive/v${pkgver}.tar.gz")
sha256sums=('d85e8dc9431f7bd2f2bd440335778fac29613a4dd1db769c29dd6464254bf6d3')

package() {
  cd "$srcdir/$pkgname-$pkgver"
  python setup.py install --root="${pkgdir}/" --optimize=1
}