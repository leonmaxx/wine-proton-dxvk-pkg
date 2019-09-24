pkgname=wine-proton-dxvk
pkgver=1.4
pkgrel=1
pkgdesc='Vulkan-based D3D11, D3D10 and D3D9 implementation for Linux/Wine'
url='https://github.com/doitsujin/dxvk'
arch=('x86_64')
license=('BSD')

depends=('wine-proton')
d9vkver=0.20

source=("https://github.com/doitsujin/dxvk/releases/download/v$pkgver/dxvk-$pkgver.tar.gz"
        "https://github.com/Joshua-Ashton/d9vk/releases/download/0.20/d9vk-$d9vkver.tar.gz"
        "wine-update-prefix")

sha256sums=('bf22785de1ce728bbdcfb4615035924112b4718049ca2cade5861b03735181de'
            'bd53c17eafeffcf2251d3911b7814b92c8f7e4c6b7364217da38645093a1db35'
            '573d21cb287f526c8292aa2326e15316a9725864c4b84869052f6fca4c995775')

package() {
  mkdir -p "$pkgdir/usr/share/wine-proton-dxvk/x32"
  mkdir -p "$pkgdir/usr/share/wine-proton-dxvk/x64"
  mkdir -p "$pkgdir/usr/bin"
  
  cp "$srcdir/d9vk-$d9vkver/x32/d3d9.dll" "$pkgdir/usr/share/wine-proton-dxvk/x32/"
  cp "$srcdir/dxvk-$pkgver/x32/d3d10.dll" "$pkgdir/usr/share/wine-proton-dxvk/x32/"
  cp "$srcdir/dxvk-$pkgver/x32/d3d10_1.dll" "$pkgdir/usr/share/wine-proton-dxvk/x32/"
  cp "$srcdir/dxvk-$pkgver/x32/d3d10core.dll" "$pkgdir/usr/share/wine-proton-dxvk/x32/"
  cp "$srcdir/dxvk-$pkgver/x32/d3d11.dll" "$pkgdir/usr/share/wine-proton-dxvk/x32/"
  cp "$srcdir/dxvk-$pkgver/x32/dxgi.dll" "$pkgdir/usr/share/wine-proton-dxvk/x32/"

  cp "$srcdir/d9vk-$d9vkver/x64/d3d9.dll" "$pkgdir/usr/share/wine-proton-dxvk/x64/"
  cp "$srcdir/dxvk-$pkgver/x64/d3d10.dll" "$pkgdir/usr/share/wine-proton-dxvk/x64/"
  cp "$srcdir/dxvk-$pkgver/x64/d3d10_1.dll" "$pkgdir/usr/share/wine-proton-dxvk/x64/"
  cp "$srcdir/dxvk-$pkgver/x64/d3d10core.dll" "$pkgdir/usr/share/wine-proton-dxvk/x64/"
  cp "$srcdir/dxvk-$pkgver/x64/d3d11.dll" "$pkgdir/usr/share/wine-proton-dxvk/x64/"
  cp "$srcdir/dxvk-$pkgver/x64/dxgi.dll" "$pkgdir/usr/share/wine-proton-dxvk/x64/"
  
  cp -L "$srcdir/wine-update-prefix" "$pkgdir/usr/bin/"
}
