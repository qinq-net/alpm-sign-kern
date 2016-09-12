# $Id$
pkgname=sign-kern
pkgver=0.1
pkgrel=1
pkgdesc='Sign Kernel with Local Key "/etc/sign-kern/db.key\"'
url=
license=('custom:BSD')
arch=('any')
makedepends=()
depends=('sbsigntools')
optdepends=()
conflicts=("")
provides=("${pkgname}")
groups=()
source=('alpm-hook' 
        'kernel-sign.hook')
sha256sums=('86f1699014feaa83cfc4d22f6e2b44f6b7dfc9a7cf10ddd055ed698834ff081b'
            'e60bea2a93b33131e6d8c9f7212a410ce6ea434ca75f75e304669d96a87c150e')
backup=()

package() {
	cd "${srcdir}"
	install -d "${pkgdir}/etc/sign-kern"
	install -Dm755 alpm-hook "${pkgdir}/usr/lib/sign-kern/alpm-hook"
	install -Dm755 kernel-sign.hook "${pkgdir}/usr/share/libalpm/hooks/kernel-sign.hook"
}
