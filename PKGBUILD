# Maintainer: Zijung Chueh <i@zijung.me>

pkgbase=zijung-configure
pkgname=('zijung-libinput'
         'zijung-nvidia-graphics'
         'zijung-sudo'
         'zijung-disable-xhc-wake')
pkgver=3.3.0
pkgrel=1
arch=('any')
license=('MIT')
url='https://github.com/zijung/zijung-configure'

package_zijung-libinput() {
    pkgdesc='My configure files of libinput'
    depends=('xf86-input-libinput')

    install -D -m755 ${startdir}/libinput/40-libinput.conf ${pkgdir}/etc/X11/xorg.conf.d/40-libinput.conf
}

package_zijung-nvidia-graphics() {
    pkgdesc='My configure files of nvidia graphics'
    depends=('nvidia-dkms')

    install -D -m755 ${startdir}/nvidia-graphics/20-nvidia.conf ${pkgdir}/etc/X11/xorg.conf.d/20-nvidia.conf
}

package_zijung-sudo() {
    pkgdesc='My configure files of sudo'
    depends=('sudo')

    install -D -m755 ${startdir}/sudo/keep_env ${pkgdir}/etc/sudoers.d/keep_env
}

package_zijung-disable-xhc-wake() {
    pkgdesc='My configure files to disable xhc wake'

    install -D -m755 ${startdir}/disable-xhc-wake/disable-xhc-wake.conf ${pkgdir}/etc/tmpfiles.d/disable-xhc-wake.conf
}
