# Maintainer: DwE <dwe@localhost>
pkgname=equicord-hook
pkgver=1.0.0
pkgrel=1
pkgdesc="Pacman hook to automatically patch Discord (~/.config/discord) with Equicord"
arch=('any')
url="https://github.com/Equicord/Equicord"
license=('GPL-3.0-only')
depends=('pacman')
optdepends=(
    'discord: Official Discord package'
    'equicord-installer-bin: Equicord CLI installer'
)
source=(
    'equicord.hook'
    'equicord-hook-script'
)
sha256sums=(
    'SKIP'
    'SKIP'
)

package() {
    # Install pacman hook into standard ALPM hooks directory
    install -Dm644 "$srcdir/equicord.hook" "$pkgdir/usr/share/libalpm/hooks/equicord.hook"
    
    # Install executable script into system binaries
    install -Dm755 "$srcdir/equicord-hook-script" "$pkgdir/usr/bin/equicord-hook-script"
}
