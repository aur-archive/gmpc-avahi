# Contributor: yugrotavele <yugrotavele at archlinux dot us>
# Contributor: Lukas Miczka <lukascpu@gmail.com>
# Modified from original gmpc pkgbuild created by tobias <tobias@archlinux.org>

pkgname=gmpc-avahi
pkgver=11.8.16
pkgrel=2
pkgdesc="This plugin auto-detects the presence of mpd servers in the network."
arch=('i686' 'x86_64')
url="http://gmpc.wikia.com/wiki/GMPC_PLUGIN_AVAHI"
license=('GPL')
depends=('gmpc>=11.8.16')
makedepends=('intltool')
options=('!libtool')
source=(http://download.sarine.nl/Programs/gmpc/$pkgver/$pkgname-$pkgver.tar.gz)
sha1sums=('a73929cba594dd9f6fbdd71670856e93e4f12335')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir" install
}

# vim:set ts=2 sw=2 et:
