pkgname=lighttable
pkgver=0.8.1
pkgrel=1
pkgdesc="An open source code editor IDE very customizable"
arch=('x86_64')
url="http://lighttable.com/"
license=('MIT')  
source=("https://github.com/LightTable/LightTable/releases/download/${pkgver}/lighttable-${pkgver}-linux.tar.gz" "lighttable.png" "lighttable.desktop")
depends=("gtk2" "gconf" "nss" "libnotify" "alsa-lib")
md5sums=('7e4efcce58f2f4a44edb5bde6f5a91db'
         'e24cdac0b3423793c13b83d01f3b2346'
         'b9325a21a98b84cacdb75acdd6476960')

package() {
   install -dm755 $pkgdir/usr/share/lighttable 
   cp -r $srcdir/lighttable-$pkgver-linux/* $pkgdir/usr/share/lighttable
   
   install -Dm644 $srcdir/lighttable.desktop $pkgdir/usr/share/applications/lighttable.desktop
   
   install -Dm644 $srcdir/lighttable.png $pkgdir/usr/share/pixmaps/lighttable.png
   
   install -dm755 $pkgdir/usr/bin
   ln -s  /usr/share/lighttable/LightTable $pkgdir/usr/bin/lighttable 
      
    }   





