# Maintainer miikaoskari
# Previous maintainer: apropos <jj@toki.la>
pkgname=binaryninja-free
_pkgname=binaryninja
pkgver=4.0.5336
pkgrel=1
pkgdesc="An interactive decompiler, disassembler, debugger, and binary analysis platform."
arch=('x86_64')
url="https://binary.ninja"
license=('custom:Binary Ninja Free Edition License Agreement')
depends=('python' 'glibc' 'qt5-base')
makedepends=()
optdepends=()
source=(
	"https://cdn.binary.ninja/installers/binaryninja_free_linux.zip"
	"${pkgname}.png"
	"${pkgname}.desktop"
)
sha256sums=(
	'43d091dd454fcc5cc21c5accc48746ad0d11a8bd0be7ae8c0599c61bfde7381e'
	'4f318001e7d39279ce063ef42077bae03e95c112aa203a4be3ea3d913c34327e'
	'075158d0131dd89565e021a6854a6ae0237442e0b4e03a61638a7f8a69ec9f85'
)

package() {
	install -d "${pkgdir}/opt/${pkgname}"
	install -d "${pkgdir}"/usr/share/{icons,applications}

	cp -r "${srcdir}/${_pkgname}"/* "${pkgdir}/opt/${pkgname}/"
	install "${srcdir}/${pkgname}.png" "${pkgdir}/usr/share/icons/"
	install "${srcdir}/${pkgname}.desktop" "${pkgdir}/usr/share/applications/"
}
