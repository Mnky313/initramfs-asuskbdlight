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

sha256sums=('043b871f3843d4916d350281e8bf81c0bf42530f36f8d9635604ada7113a8475'
            '523b94f301860eec3defa9a945e06355e733c605fbae8c89067a18a46a09ab2d'
            '9f84df0f294329413cb5c6f33f28b9336338d42c3aa8763dc96dcd8e4570d579')
