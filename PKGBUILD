# Maintainer: G.S.V. Prharsha <gsvprharsha@github>

pkgname=raven-grub-darkmatter
pkgver=1
pkgrel=1
pkgdesc='Darkmatter GRUB Theme for Raven OS'
arch=('any')
url='https://github.com/Raven-OS-Official/raven-grub-darkmatter'
license ('GPL-3.0')
optdepends=('grub-customizer: GUI tool to configure GRUB')
makedepends=('git')
source=("git+https://github.com/Raven-OS-Official/raven-grub-darkmatter")
sha256sums=('SKIP')

pkgver() {
	cd raven-grub-darkmatter
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}
package(){
	install -dm755 "${pkgdir}"/usr/share/grub/themes/
	install -Dm644 raven-grub-darkmatter/LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
	cp -r --no-preserve-ownership raven-grub-darkmatter "${pkgdir}"/usr/share/grub/themes/
	rm -rf "${pkgdir}"/usr/share/grub/themes/raven-grub-darkmatter/.git
	rm "${pkgdir}"/usr/share/grub/themes/raven-grub-darkmatter/install.sh
}
