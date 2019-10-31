pkgname=wine-proton-dxvk
pkgver=1.4.4
pkgrel=1
pkgdesc='Vulkan-based D3D11, D3D10 and D3D9 implementation for Linux/Wine'
url='https://github.com/doitsujin/dxvk'
arch=('x86_64')
license=('BSD')

depends=('wine-proton')
d9vkver=0.30

source=("https://github.com/doitsujin/dxvk/releases/download/v$pkgver/dxvk-$pkgver.tar.gz"
        "https://github.com/Joshua-Ashton/d9vk/releases/download/$d9vkver/d9vk-$d9vkver.tar.gz"
        "wine-update-prefix")

sha256sums=('a845285c8dfc63c7d00c14520b58fc6048796fef69fea49617edb46662a0ba31'
            '9654b888665184bf795aa33a0c7287d04666ebe21e56e53df0f6c331fde24927'
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
