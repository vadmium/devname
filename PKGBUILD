pkgname=devname
pkgver=0.0.0
pkgrel=0
arch=any
pkgdesc="Generic persistent device naming"
depends=("udev>=162")
source=(devname 60-path.rules full-path.diff)
md5sums=(
  9e261cc5f9c78807bfc1a324d56287ad
  cdba66422a73131fbc724849536385fb
  2c62bf649cacc476d7d21c27a89a9f54
)

package() {
  mkdir -p "$pkgdir/lib/udev/rules.d" "$pkgdir/sbin"
  install --mode +r "$srcdir/60-path.rules" "$pkgdir/lib/udev/rules.d/"
  install "$srcdir/devname" "$pkgdir/sbin/"
}
