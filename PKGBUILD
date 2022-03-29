#!/bin/bash

# Disable various shellcheck rules that produce false positives in this file.
# Repository rules should be added to the .shellcheckrc file located in the
# repository root directory, see https://github.com/koalaman/shellcheck/wiki
# and https://archiv8.github.io for further information.
# shellcheck disable=SC2034,SC2154
# ToDo: Add files: User documentation
# ToDo: Add files: Tooling
# FixMe: Namcap warnings and errors

# Maintainer: Ross Clark <archiv8@artisteducator.com>
# Contributor: Ross Clark <archiv8@artisteducator.com>

pkgname=google-java-format
pkgver=1.15.0
pkgrel=1
pkgdesc="Reformats Java source code to comply with Google Java Style"
url="https://github.com/google/google-java-format"
arch=("any")
license=("Apache")
depends=(
  "java-runtime"
  "bash"
)
source=(
  "https://github.com/google/$pkgname/releases/download/v$pkgver/$pkgname-$pkgver-all-deps.jar"
  "$pkgname"
  "https://raw.githubusercontent.com/google/$pkgname/master/LICENSE"
)
sha512sums=(
"2bde8271b17725fb0cf552f97d4852dacb040c1d82432bc325ebdf94391bdf83df9e340071cc17e326f9fad3756e2fa09dfd6ba756d67b5e311fda0298e8b2be"
            "3d80ed0455c5d6a6193c790d55bcdc1d79289f6ff7177d4f040857b5bcffead0745b7d592f72e5e9e327ba0b9028c319ad3ffbbfa50f0dbce21d03c4e1081b70"
            "2540a2214e70e97c3f4bba2fe95d3ebfdb5a6b66c056cfe1ae5ce259bfc203b8273eb46adc0adf4aec069ef01de7e2223403267f4398c4171bc7e763140f40b6"
)

package() {
  install -Dm755 "$srcdir/$pkgname-$pkgver-all-deps.jar" "$pkgdir/usr/share/java/$pkgname/$pkgname.jar"
  install -Dm755 "$srcdir/$pkgname" "$pkgdir/usr/bin/$pkgname"
  install -Dm644 LICENSE* -t "$pkgdir/usr/share/licenses/$pkgname"
}
