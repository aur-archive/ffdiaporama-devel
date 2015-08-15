# Maintainer: boenki <boenki at gmx dot de>

pkgname=ffdiaporama-devel
pkgver=2.2.devel.2014.0701
pkgrel=1
pkgdesc="Movie creator from photos and video clips (development version)"
arch=('i686' 'x86_64')
url="http://ffdiaporama.tuxfamily.org"
license=('GPL2')
conflicts=('ffdiaporama')
depends=('qt5-svg' 'qt5-tools' 'qt5-imageformats' 'qt5-multimedia' 'ffmpeg' 'pulseaudio' 'exiv2' 'shared-mime-info' 'ffdiaporama-rsc-devel')
optdepends=('ffdiaporama-texturemate: Additional background-images'
            'ffdiaporama-openclipart: use the openclipart-library')
install=${pkgname}.install
source=(http://download.tuxfamily.org/ffdiaporama/Packages/Devel/ffdiaporama_bin_$pkgver.tar.gz)
md5sums=('0ca946d8db68467aefec39917e2dbb4d')

build() {
  cd ffDiaporama
  qmake-qt5 ffDiaporama.pro
  make
}

package() {
  cd ffDiaporama
  make install INSTALL_ROOT=$pkgdir
  find $pkgdir/usr/share -type f -exec chmod 644 {} +
}
