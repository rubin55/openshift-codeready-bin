# Maintainer:  Rubin Simons <me@rubin55.org>

pkgname=openshift-codeready-bin
pkgver=2.43.0
pkgrel=1
pkgdesc="CodeReady tools for OpenShift (crc), binary release"
provides=('crc')
conflicts=('crc-bin')
arch=('x86_64')
url="https://www.okd.io/crc"
license=("Apache")

source=("crc-v${pkgver}-linux-amd64.tar.xz::https://developers.redhat.com/content-gateway/file/pub/openshift-v4/clients/crc/${pkgver}/crc-linux-amd64.tar.xz")

sha256sums=('975834f58c541cf2336b086071ab75dc26553084b212cd541f6b86fe1076e905')

options=("!strip")

package() {
    install -o root -g root -m 755 -d "${pkgdir}/usr/bin"
    install -o root -g root -m 755 "${srcdir}/crc-linux-${pkgver}-amd64/crc" "${pkgdir}/usr/bin/crc"
}
