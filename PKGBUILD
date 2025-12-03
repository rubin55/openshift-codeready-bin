# Maintainer:  Rubin Simons <me@rubin55.org>

pkgname=openshift-codeready-bin
pkgver=2.57.0
pkgrel=1
pkgdesc="CodeReady tools for OpenShift (crc), binary release"
provides=('crc')
conflicts=('crc-bin')
arch=('x86_64')
url="https://www.okd.io/crc"
license=("Apache")

source=("crc-v${pkgver}-linux-amd64.tar.xz::https://developers.redhat.com/content-gateway/file/pub/openshift-v4/clients/crc/${pkgver}/crc-linux-amd64.tar.xz")

sha256sums=('20c13525dfbee1795ceaf79006b8947f1aedd24a84dac40f5764a7a24454dc7a')

options=("!strip")

package() {
    install -o root -g root -m 755 -d "${pkgdir}/usr/bin"
    install -o root -g root -m 755 "${srcdir}/crc-linux-${pkgver}-amd64/crc" "${pkgdir}/usr/bin/crc"
}
