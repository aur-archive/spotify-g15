# Maintainer: Mathieu OTHACEHE <m.othacehe@gmail.com>

pkgname=spotify-g15
pkgver=0.1
pkgrel=1
pkgdesc='Display spotify tracks on G15 keyboard screen'
arch=('i686' 'x86_64')
url='https://github.com/mathieu64200/spotify-g15'
license=('GPL2')
makedepends=('git')
depends=('dbus-glib' 'g15daemon' 'libg15' 'libg15render')
provides=("$pkgname")
source=(https://github.com/mathieu64200/spotify-g15/releases/download/0.1/$pkgname-$pkgver.tar.gz)
sha256sums=('SKIP')

build() {
    cd ${srcdir}/"$pkgname-$pkgver"

    ./configure --prefix=/usr
    make
}

package() {
    cd ${srcdir}/"$pkgname-$pkgver"

    make DESTDIR=${pkgdir} install    
}
