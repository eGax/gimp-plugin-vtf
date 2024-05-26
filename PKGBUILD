pkgname=gimp-plugin-vtf
pkgver=1.1
pkgrel=1
pkgdesc="VTF GIMP plugin"
url="https://github.com/linux-source-tools/gimp-plugin-vtf"
arch=(x86_64)
license=(unknown)
depends=(gimp)
makedepends=(cmake)
_commit=e351d8eafb7e7af3193d750ef61783e02ad61a8b
source=("git+https://github.com/linux-source-tools/gimp-plugin-vtf.git#commit=$_commit")
sha256sums=('SKIP')

pkgver() {
  cd "$pkgname"
  git describe --tags | sed 's/-/+/g'
}

build() {
  cd "$pkgname"
  make
}

package() {
  cd "$pkgname"
  mkdir -p "${pkgdir}/usr/lib/gimp/2.0/plug-ins/"
  cp file-vtf "${pkgdir}/usr/lib/gimp/2.0/plug-ins/file-vtf"
}
