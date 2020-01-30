pkgname=wine-proton-dxvk
pkgver=1.5.3
pkgrel=1
pkgdesc='Vulkan-based D3D11, D3D10 and D3D9 implementation for Linux/Wine'
url='https://github.com/doitsujin/dxvk'
arch=('x86_64')
license=('BSD')

depends=('wine-proton')
#d9vkver=0.30

source=("https://github.com/doitsujin/dxvk/releases/download/v$pkgver/dxvk-$pkgver.tar.gz"
        "dxvk_config.tar.gz"
        "wine-update-prefix")

sha256sums=('b845c9c492e32648dee44d058c189eff8534e5490a80a3b2a921248bc72e33bd'
            'a3c0f15730f349871511379e8111d279dcda9b1d2bc6f3ba538f889c323d381f'
            '4b05e27bb70ea796f4988c5f74b7787c437b388079e62a025c0fd79a7859cf8d')

package() {
  mkdir -p "$pkgdir/usr/share/wine-proton-dxvk/x32"
  mkdir -p "$pkgdir/usr/share/wine-proton-dxvk/x64"
  mkdir -p "$pkgdir/usr/bin"
  
  cp "$srcdir/dxvk-$pkgver/x32/d3d9.dll" "$pkgdir/usr/share/wine-proton-dxvk/x32/"
  cp "$srcdir/dxvk-$pkgver/x32/d3d10.dll" "$pkgdir/usr/share/wine-proton-dxvk/x32/"
  cp "$srcdir/dxvk-$pkgver/x32/d3d10_1.dll" "$pkgdir/usr/share/wine-proton-dxvk/x32/"
  cp "$srcdir/dxvk-$pkgver/x32/d3d10core.dll" "$pkgdir/usr/share/wine-proton-dxvk/x32/"
  cp "$srcdir/dxvk-$pkgver/x32/d3d11.dll" "$pkgdir/usr/share/wine-proton-dxvk/x32/"
  cp "$srcdir/dxvk-$pkgver/x32/dxgi.dll" "$pkgdir/usr/share/wine-proton-dxvk/x32/"
  cp "$srcdir/dxvk_config/x32/dxvk_config.dll" "$pkgdir/usr/share/wine-proton-dxvk/x32/"

  cp "$srcdir/dxvk-$pkgver/x64/d3d9.dll" "$pkgdir/usr/share/wine-proton-dxvk/x64/"
  cp "$srcdir/dxvk-$pkgver/x64/d3d10.dll" "$pkgdir/usr/share/wine-proton-dxvk/x64/"
  cp "$srcdir/dxvk-$pkgver/x64/d3d10_1.dll" "$pkgdir/usr/share/wine-proton-dxvk/x64/"
  cp "$srcdir/dxvk-$pkgver/x64/d3d10core.dll" "$pkgdir/usr/share/wine-proton-dxvk/x64/"
  cp "$srcdir/dxvk-$pkgver/x64/d3d11.dll" "$pkgdir/usr/share/wine-proton-dxvk/x64/"
  cp "$srcdir/dxvk-$pkgver/x64/dxgi.dll" "$pkgdir/usr/share/wine-proton-dxvk/x64/"
  cp "$srcdir/dxvk_config/x64/dxvk_config.dll" "$pkgdir/usr/share/wine-proton-dxvk/x64/"
  
  cp -L "$srcdir/wine-update-prefix" "$pkgdir/usr/bin/"
}
