# Maintainer: SoulHarsh007 <harsh.peshwani@outlook.com>

pkgname="rebornos-grub2-theme"
_pkgname="grub2-themes"
pkgver=1.0.0
pkgrel=1
pkgdesc="Grub2 Theme for RebornOS"
arch=('any')
url="https://rebornos.org/"
license=('GPL3')
source=("${_pkgname}::git+https://github.com/vinceliuice/grub2-themes.git" 'rebornos.png')
b2sums=('SKIP'
  '7051ab5e8412867565af3d42f36ae967a71edfc49d7f0d14841fb8e17bc56d18df477e9723076b4858b76a32c502a6ae7c8048594ee6b2bbf153b144fe9756c5')

package() {
  install -dm755 "${pkgdir}/boot"
  install -dm755 "${pkgdir}/boot/grub"
  install -dm755 "${pkgdir}/boot/grub/themes"
  install -dm755 "${pkgdir}/boot/grub/themes/stylish"
  install -dm755 "${pkgdir}/boot/grub/themes/stylish/icons"
  cd "${srcdir}/${_pkgname}"
  ./install.sh -b -t stylish -g "${pkgdir}/boot/grub/themes"
  install -m644 "${srcdir}/rebornos.png" "${pkgdir}/boot/grub/themes/stylish/icons/rebornos.png"
}
