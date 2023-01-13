# Based on the file created for Arch Linux by:
# Pierre Schmitz <pierre@archlinux.de>

pkgname=hocari-keyring
pkgver=20230113
pkgrel=1
pkgdesc='HocariOS PGP keyring'
arch=('any')
url='https://github.com/Hocari/hocari-keyring'
license=('GPL')
install="${pkgname}.install"
source=('Makefile'
        'hocari.gpg'
        'hocari-revoked'
        'hocari-trusted')
sha256sums=('a2f6708d77ec29c03d3db1be199c04bf1bd0378176edc0312c8bba1095745645'
            'b9a04751229063b3a97aab501d088abc92d9a80596c16101050167653d8e281f'
            'e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855'
            'd95dab4a9616494b92de2ea6a5bde673a82199978c565fea0c3758272780a606')
pkgver() {
    date +%Y%m%d
}

package() {
	cd "${srcdir}"
	make PREFIX=/usr DESTDIR=${pkgdir} install
}
