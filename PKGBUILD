# Maintainer: <waruqi@gmail.com>

_realname=xmake
pkgbase=mingw-w64-${_realname}
pkgname="${MINGW_PACKAGE_PREFIX}-${_realname}"
pkgver=2.3.1
pkgrel=1
pkgdesc="A make-like build utility based on Lua"
arch=('any')
url="https://github.com/xmake-io/xmake"
license=('Apache')
depends=("${MINGW_PACKAGE_PREFIX}-ncurses"
         "${MINGW_PACKAGE_PREFIX}-readline")
makedepends=("${MINGW_PACKAGE_PREFIX}-gcc")
source=("${_realname}-${pkgver}.tar.gz"::"https://github.com/xmake-io/${_realname}/releases/download/v${pkgver}/${_realname}-v${pkgver}.tar.gz")
sha256sums=('e6e2d3b6679ae6fa2663125d3b0d927ffe811e9d8da88b97209bc508f35df6d7')

build() {
    cd "$srcdir"
    make build
}

package() {
    cd "$srcdir"
    make install DESTDIR="${pkgdir}" prefix="${MINGW_PREFIX}"
}
