pkgname=devname
pkgver=0.0.1
pkgrel=0
arch=any
pkgdesc="Generic persistent device naming"
depends=("udev>=162")
source=(devname)
md5sums=(bed11cce4d9455ae8b70a493c24932e0)

source+=(http://ftp.kernel.org/pub/linux/utils/kernel/hotplug/udev-182.tar.xz)
md5sums+=(023877e6cc0d907994b8c648beab542b)
license=(GPL)
conflicts=("udev<183")

package() {
  mkdir -p "$pkgdir/lib/udev/rules.d" "$pkgdir/sbin"
  install --mode +r "$srcdir/60-path.rules" "$pkgdir/lib/udev/rules.d/"
  install "$srcdir/devname" "$pkgdir/sbin/"
  install "$srcdir/udev-182/src/rule_generator/rule_generator.functions" "$pkgdir/lib/udev/"
}
