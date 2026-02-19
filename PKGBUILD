# Maintainer: Primalmotion <primalmation at pm dot me>

pkgname=initramfs-asuskbdlight
pkgdesc="initramfs hook that turns Asus laptop keyboard backlight on"
pkgver=1.0
pkgrel=3
license=(MIT)
arch=(any)
depends=(mkinitcpio)
source=(asuskbdlight-hook
		asuskbdlight-install
		README.md)

build() {
	return 0
}

package() {
	mkdir -p "${pkgdir}/usr/lib/initcpio/hooks"
	mkdir -p "${pkgdir}/usr/lib/initcpio/install"

	cp "${srcdir}/asuskbdlight-hook" "${pkgdir}/usr/lib/initcpio/hooks/asuskbdlight"
	cp "${srcdir}/asuskbdlight-install" "${pkgdir}/usr/lib/initcpio/install/asuskbdlight"

	mkdir -p "${pkgdir}/usr/share/doc/${pkgname}"
	cp "${srcdir}/README.md" "${pkgdir}/usr/share/doc/${pkgname}/"
}

sha256sums=('fbfcc052cb3d0877cb8644d5dd202cad974484b401209f8722d9b92c0fb61b25'
            '362aa638a104b125f0d5bc5411958f4c00ddf104b6de8ce7f7eb18e1cbe3c17b'
            '9f84df0f294329413cb5c6f33f28b9336338d42c3aa8763dc96dcd8e4570d579')
