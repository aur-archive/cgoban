# Maintainer: Gaetan Bisson <bisson@archlinux.org>
# Contributor: Jason Chu <jason@archlinux.org>
# Contributor: Tom Newsom <Jeepster@gmx.co.uk>

pkgname=cgoban
pkgver=1.9.14
pkgrel=1
pkgdesc='SGF editor and client for connection to IGS'
url='http://sourceforge.net/projects/cgoban1/'
arch=('i686' 'x86_64')
license=('GPL2')
depends=('libxt')
source=("http://downloads.sourceforge.net/project/cgoban1/cgoban1/$pkgver/$pkgname-$pkgver.tar.gz")
sha1sums=('90bd53499c9f410caddaae601e7f00350d520a32')

build() {
	cd "$srcdir/$pkgname-$pkgver"
	./configure --prefix=/usr --mandir=/usr/share/man
	make
}

package() {
	cd "$srcdir/$pkgname-$pkgver"
	install -d "$pkgdir"/usr/{bin,share/man/man6}
	make DESTDIR="$pkgdir" install
}
