pkgbase=bootsplash-themes
pkgname=('bootsplash-theme-xiaomi')
pkgver=0.7
pkgrel=3
url="https://github.com/openmindead/manjaro-bootsplash-mi"
arch=('x86_64')
license=('GPL')

depends=('systemd')
builddepends=('imagemagick')
options=('!libtool' '!emptydirs')

source=('bootsplash-packer'
	'bootsplash-xiaomi.sh'
	'bootsplash-xiaomi.initcpio_install'
	'spinner.gif'
	'mi.png')

sha256sums=('SKIP'
            'SKIP'
            'SKIP'
            'SKIP'
            'SKIP')

build() {
  cd "$srcdir"
  sh ./bootsplash-xiaomi.sh
}

package_bootsplash-theme-xiaomi() {
  pkgdesc="'XIAOMI' branded Bootsplash Theme for Manjaro Linux"
  cd "$srcdir"

  install -Dm644 "$srcdir/bootsplash-xiaomi" "$pkgdir/usr/lib/firmware/bootsplash-themes/xiaomi/bootsplash"
  install -Dm644 "$srcdir/bootsplash-xiaomi.initcpio_install" "$pkgdir/usr/lib/initcpio/install/bootsplash-xiaomi"
} 
