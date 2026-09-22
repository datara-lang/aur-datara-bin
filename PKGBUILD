# Maintainer: waters1ze <https://github.com/waters1ze>
# Contributor: Datara Language Project <https://github.com/datara-lang>

pkgname=datara-bin
pkgver=1.4.5
pkgrel=1
pkgdesc="High-performance Post-OOP systems and application programming language with Forgen compiler"
arch=('x86_64')
url="https://github.com/datara-lang/datara"
license=('Apache-2.0' 'MIT')
provides=('datara' 'forgen')
conflicts=('datara' 'forgen')
source_x86_64=("https://github.com/datara-lang/datara/releases/download/v${pkgver}/forgen-linux-x64.tar.gz")
sha256sums_x86_64=('77785f7ee68e0ab419d1bffa0eed04f4c60391f2016a6a85c7d5f317cdd97354')

package() {
    cd "${srcdir}"
    install -Dm755 forgen "${pkgdir}/usr/bin/forgen"
    ln -s /usr/bin/forgen "${pkgdir}/usr/bin/datara"
    if [ -d stdlib ]; then
        install -dm755 "${pkgdir}/usr/share/datara/stdlib"
        cp -r stdlib/* "${pkgdir}/usr/share/datara/stdlib/"
    fi
}
