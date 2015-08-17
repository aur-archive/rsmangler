# Maintainer: onny <onny@project-insanity.org>
# Contributor: onny <onny@project-insanity.org>

pkgname=rsmangler
pkgver=1.4
pkgrel=1
pkgdesc="rsmangler takes a wordlist and mangle it"
url=('http://www.randomstorm.com/rsmangler-security-tool.php')
arch=('i686' 'x86_64')
license=('custom:Creative-Commons-BY-SA')
depends=('ruby')
source=("http://www.randomstorm.com/tools/${pkgname}_${pkgver}.tar.bz2")
sha512sums=('55148f2a4bdcdcf3f06414a16f84ae32436b12c05a26c993bd7d63f20a16c8aada36b1b2918a8d67fdfcff64e204f08b819d13a82a512be5e26f98ce87a88044')
package() {
	mkdir -p $pkgdir/opt/rsmangler
	mkdir -p $pkgdir/usr/bin
	cp -r $srcdir/${pkgname}/* $pkgdir/opt/rsmangler/
	echo -e "#!/bin/bash\nruby /opt/rsmangler/rsmangler.rb \$@" > $pkgdir/usr/bin/rsmangler
	chmod a+x $pkgdir/usr/bin/rsmangler
}
