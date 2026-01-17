# Maintainer: Maxime Lewandowski <maxime@lywel.link>

pkgname=plymouth-theme-pyannote
pkgver=1
pkgrel=1
pkgdesc='Plymouth theme with Pyannote logo and animation'
arch=('any')
url='https://github.com/yourusername/plymouth-theme-pyannote'
license=('custom')
depends=('plymouth')
install="${pkgname}.install"
source=('theme')
sha512sums=('SKIP')

package() {
	cd "${srcdir}/theme"
	install -dm755 "${pkgdir}/usr/share/plymouth/themes/pyannote"
	install -Dm644 *.png "${pkgdir}/usr/share/plymouth/themes/pyannote/"
	install -Dm644 pyannote.plymouth "${pkgdir}/usr/share/plymouth/themes/pyannote/"
}
