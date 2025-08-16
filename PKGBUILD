# Maintainer: Samuel Mesa <samuelmesa@linuxmail.org>

pkgname=rknputop
pkgver=cdf2774
pkgrel=1
pkgdesc="Simple top-like script for Rockhip NPUs on Linux"
arch=('x86_64' 'aarch64')
url="https://github.com/ramonbroox/rknputop"
license=('GPL-3.0-or-later')
depends=('python' 'python-psutil' 'python-plotext')
makedepends=('git')
source=("git+$url.git")
sha256sums=('SKIP')

pkgver() {
  cd "$srcdir/$pkgname"
  printf "%s" "$(git describe --long --tags --always | sed 's/\([^-]*-g\)/r\1/;s/-/./g')"
}

package() {
    cd "$srcdir/$pkgname"

    # Install the main script
    install -Dm755 rknputop "$pkgdir/usr/bin/rknputop"
}
