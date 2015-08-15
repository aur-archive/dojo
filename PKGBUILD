# Maintainer: Leo von Klenze <aur@leo.von-klenze.de>
pkgname=dojo
pkgver=1.10.0
pkgrel=1
pkgdesc="Dojo is an Open Source DHTML toolkit written in JavaScript."
arch=(i686 x86_64)
url="http://www.dojotoolkit.org"
license=('BSD' 'Academic Free License')

source=(http://download.dojotoolkit.org/release-$pkgver/dojo-release-$pkgver.tar.gz)
md5sums=('f5a22d281fd151e1298388031af6cb88')

install_dir='usr/share/javascript/dojotoolkit'

package() {
    mkdir -p $pkgdir/$install_dir
    cd $srcdir/dojo-release-$pkgver || return 1 

    find $pkgname -type f | while read file; do
        install -Dm644 "$file" "$pkgdir/$install_dir/$file" || return 1
    done || return 1
}

