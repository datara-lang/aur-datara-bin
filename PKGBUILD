# Maintainer: waters1ze <https://github.com/waters1ze>
# Contributor: Datara Language Project <https://github.com/datara-lang>

pkgname=datara-bin
pkgver=1.4.1
pkgrel=1
pkgdesc="High-performance Post-OOP systems and application programming language with Forgen compiler"
arch=('x86_64')
url="https://github.com/datara-lang/datara"
license=('Apache-2.0' 'MIT')
provides=('datara' 'forgen')
conflicts=('datara' 'forgen')
source_x86_64=("https://github.com/datara-lang/datara/releases/download/v${pkgver}/forgen-linux-x64.tar.gz")
sha256sums_x86_64=('9694fba29b4aff7f7deda381f0344af8621383e89fbf1011d6dcd3ac2afd614b')

package() {
    cd "${srcdir}"
    install -Dm755 forgen "${pkgdir}/usr/bin/forgen"
    ln -s /usr/bin/forgen "${pkgdir}/usr/bin/datara"
    if [ -d stdlib ]; then
        install -dm755 "${pkgdir}/usr/share/datara/stdlib"
        cp -r stdlib/* "${pkgdir}/usr/share/datara/stdlib/"
    fi
}
