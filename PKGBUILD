# Contributor: Jesus Jerez <jhuss@archlinux.org.ve>
# Contributor: Alomsimoy <alomsimoy@gmail.com>
# Maintainer: Eduardo Parra Mazuecos <eduparra90 at gmail dot com>
# based in netbeans PKGBUILD

pkgname=netbeans-es
pkgver=8.0.1
pkgrel=1
pkgdesc="Netbeans IDE development platform in Spanish"
url="http://www.netbeans.org"
arch=('any')
license=('CDDL')
conflicts=('netbeans')
provides=('netbeans')
depends=('java-environment')
source=('http://bits.netbeans.org/8.0.1/community/zip/netbeans-8.0.1-201409082112.zip'
		'netbeans.desktop')
md5sums=('898f4f7454f246d5b901b034bdc90e5b'
         '88c631d0d263218e01ea886fde2bc913')
install=netbeans.install
options=('!strip')

build() {
	install -d ${pkgdir}/usr/bin
	install -d ${pkgdir}/usr/share/netbeans
	
	rm ${srcdir}/netbeans/bin/netbeans.exe
	install -D -m644 netbeans.desktop ${pkgdir}/usr/share/applications/netbeans.desktop
	cp -r ${srcdir}/netbeans/* ${pkgdir}/usr/share/netbeans/
	ln -s /usr/share/netbeans/bin/netbeans ${pkgdir}/usr/bin/netbeans
}
