pkgname=portsigar
_pkgbase=couchbase-server
pkgver=1.6.4
_pkgbasever=1.8.0
pkgrel=1
pkgdesc="Minimal sigar client used by couchbase"
url='http://www.support.hyperic.com/SIGAR/Home'
arch=('i686' 'x86_64')
license=('Apache')
depends=('libsigar')
source=("http://packages.couchbase.com/releases/1.8.0/${_pkgbase}_src-${_pkgbasever}.tar.gz")
md5sums=('b0d7504fa4600d198f5c55b3944e244a')

build() {
	cd "${srcdir}/${_pkgbase}_src/portsigar"
	./configure --prefix=/usr
	make
}

package() {
	cd "${srcdir}/${_pkgbase}_src/portsigar"
	make DESTDIR="${pkgdir}" install
}
