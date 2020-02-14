# Maintainer: Stefano Capitani <stefano@manjaro.org>

pkgname=pacman-static
pkgdesc="Statically-compiled pacman ( to fix or install systems: extracted version )"
pkgver=5.2.1
pkgrel=3.1
arch=('x86_64')
license=('GPL')
depends=('pacman')
url=https://pkgbuild.com/~eschwartz/repo/x86_64-extracted
source=("$url/pacman-static")
md5sums=('0dea8e7967aaeb1fd2fb64aeca877ebc')
         
package() {
	
	 install -Dm755 "$srcdir/$pkgname" "$pkgdir/usr/bin/$pkgname"
}

