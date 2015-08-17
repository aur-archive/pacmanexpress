#Autor: Alexandre Minoshi(Almin-Soft Group)
#Maintainer: Alexandre Minoshi

pkgname=pacmanexpress
pkgver=3.6
pkgrel=1
pkgdesc="X11 GUI for pacman and yaourt with multi install."
options=('!strip')
arch=('i686' 'x86_64')
url="http://almin-soft.ru/index.php?programmy/pacmanexpress/tags/pacmanexpress"
license=('GPL2')
if [ "${CARCH}" = 'x86_64' ]; then
depends=('pacman' 'xorg-server' 'libxrender' 'lib32-libx11')
elif [ "${CARCH}" = 'i686' ]; then
depends=('pacman' 'xorg-server' 'libxrender')
fi
optdepends=('yaourt: AUR support' 'lib32-libxft: antialiased problem fix' 'curl: for download content' 'scrot: for making screenshots')
source=("http://almin-soft.ru/data/files/pacmanxg/download.php?get=pacmanexpress.tar.bz2")

package() {
  install -d $pkgdir/opt/pacmanexpress
  install -Dm755 pacmanexpress $pkgdir/opt/pacmanexpress/pacmanexpress
  install -Dm644 icon.png $pkgdir/usr/share/pixmaps/pacmanexpress.png
  install -Dm644 pacmanexpress.desktop $pkgdir/usr/share/applications/pacmanexpress.desktop
  install -d $pkgdir/usr/bin/
}
md5sums=('f215e99c5f41c4a539045a55cdbb33ca')
