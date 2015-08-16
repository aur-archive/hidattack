# Archtrack maintainer: Evan Teitelman <teitelmanevan at gmail dot com>
# Contributor: Francesco Piccinno <stack.box@gmail.com>

pkgname=hidattack
pkgver=0.1
pkgrel=2
pkgdesc="HID Attack (attacking HID host implementations)"
url="http://mulliner.org/bluetooth/hidattack.php"
updateurl="http://mulliner.org/bluetooth/hidattack.php=>hidattack"
license=('GPL')
arch=(i686 x86_64)
makedepends=('gcc')
depends=(bluez openobex)
source=(http://www.mulliner.org/bluetooth/${pkgname}${pkgver//./}.tar.gz)
md5sums=('0748ddd70ef23122687693b2bbaa6960')

build() {
  cd "$srcdir/${pkgname}${pkgver//./}"
  make CFLAGS="$CFLAGS"

  install -Dm755 hidattack $pkgdir/usr/bin/hidattack
  install -Dm644 README $pkgdir/usr/share/$pkgname/README
  install -Dm644 ha.inp $pkgdir/usr/share/$pkgname/ha.inp
}

