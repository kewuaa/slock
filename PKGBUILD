pkgname=slock
pkgver="0.1.0"
pkgrel=1
arch=("x86_64")
depends=(
    "libx11"
    "libxcrypt"
    "libxext"
    "libxrandr"
    "imlib2"
)
makedepends=("gcc" "make")


build() {
    cd ${srcdir}/..
    make clean
    make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}


package() {
    cd ${srcdir}/..
    make DESTDIR="${pkgdir}" PREFIX="/usr" MANPREFIX="/usr/local/man" install
}
