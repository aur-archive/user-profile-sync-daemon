# Maintainer: Guten Ye

pkgname="user-profile-sync-daemon"
pkgver=0.1 
pkgrel=4
pkgdesc="sync browser profiles to tmpfs. README at https://github.com/GutenYe/aur/tree/master/user-profile-sync"
arch=("i686" "x86_64")
url="https://github.com/GutenYe/aur/tree/master/user-profile-sync"
license=("MIT")
depends=("user-daemon-system-git" "rsync")
backup=("home/$USER/etc/conf.d/profile-sync")
source=("rc.profile-sync"
        "conf.profile-sync")

package() {
  cd "$srcdir"

	install -Dm755 rc.profile-sync "$pkgdir/home/$USER/etc/rc.d/profile-sync"
  install -Dm664 conf.profile-sync "$pkgdir/home/$USER/etc/conf.d/profile-sync"

  chown $USER:$USER -R "$pkgdir/home/$USER"
}

# vim:set ts=2 sw=2 et:
md5sums=('183e497c5ed4ffccb71cbe481f4ddbb8'
         'd0927b0cfa96471bb8642f6f433b7ac4')
