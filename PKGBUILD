# Maintainer: Musikolo <musikolo {at} hotmail [dot] com>

packager=('Musikolo')
_original_pkgname=eyasdp
pkgname=kdeplasma-addons-applets-${_original_pkgname}
pkgver=0.9.0
pkgdesc="Enhanced yaSDP(yet another ShutDown plasmoid)"
pkgrel=1
arch=(i686 x86_64)
url="http://kde-look.org/content/show.php?content=146530"
license=(GPL3)
groups=('kde' 'plasmoid')
makedepends=(cmake automoc4)
depends=(kdebase-workspace)
options=()
conflicts=('eyasdp')
source=(http://kde-look.org/CONTENT/content-files/146530-${_original_pkgname}-${pkgver}.tar.bz2)
md5sums=('8129aa5989a7edd5b8f48d9657f8e856')
sha1sums=('bbda20bbb25a09bc2b9f1f02ec36d5eb4f78561e')

build() {
  cd "${_original_pkgname}-${pkgver}"
  cmake -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix`
  make
  make DESTDIR=${pkgdir} install

  _licenses_dir="${pkgdir}`kde4-config --prefix`/share/licenses/${pkgname}"
  install -D AUTHORS ${_licenses_dir}/AUTHORS
  install -D ChangeLog ${_licenses_dir}/ChangeLog
  install -D COPYING ${_licenses_dir}/COPYING
  install -D TODO ${_licenses_dir}/TODO
}
