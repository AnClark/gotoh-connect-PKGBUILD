# Maintainer: AnClark Liu <anclarkliu@outlook.com>

pkgname=gotoh-connect
pkgver=1.0.0
pkgrel=1
pkgdesc='Simple relaying command for SSH/HTTP proxy'
arch=('x86_64')
url='https://bitbucket.org/gotoh/connect/'
license=('custom')
options=('!emptydirs')
source=('git+https://github.com/anclark/connect.git')    # Original author has removed his repo. This is a fork
sha256sums=('SKIP')

build() {
  cd "$srcdir"/connect
  make
}

package() {
  # This Makefile doesn't provide any install commands.
  # Manually copy files instead.
  mkdir -p "$pkgdir"/usr/bin
  install -D -m755 "$srcdir"/connect/connect "$pkgdir"/usr/bin
}

# vim: ts=2 sw=2 et:
