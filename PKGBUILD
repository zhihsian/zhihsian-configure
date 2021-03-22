# Maintainer: zsien <i@zsien.cn>

pkgbase=zsien-configuration
pkgname=('zsien-libinput'
         'zsien-nvidia-graphics'
         'zsien-sudo'
         'zsien-noto-cjk'
         'zsien-disable-xhc-wake'
         'zsien-plasma-desktop')
pkgver=4.1.0
pkgrel=1
arch=(any)
license=('MIT')
url='https://github.com/zsien/zsien-configuration'

package_zsien-libinput() {
    pkgdesc='My configure files of libinput'
    depends=('xf86-input-libinput')

    install -D ${startdir}/libinput/40-libinput.conf ${pkgdir}/etc/X11/xorg.conf.d/40-libinput.conf
}

package_zsien-nvidia-graphics() {
    pkgdesc='My configure files of nvidia graphics'
    depends=('nvidia-dkms')

    install -D ${startdir}/nvidia-graphics/20-nvidia.conf ${pkgdir}/etc/X11/xorg.conf.d/20-nvidia.conf
}

package_zsien-sudo() {
    pkgdesc='My configure files of sudo'
    depends=('sudo')

    install -D ${startdir}/sudo/keep_env ${pkgdir}/etc/sudoers.d/keep_env
}

package_zsien-noto-cjk() {
    pkgdesc='My configure files of fonts-noto'
    depends=('noto-fonts-cjk')

    install -d ${pkgdir}/etc/fonts/conf.d
    ln -s /etc/fonts/conf.avail/70-noto-cjk.conf ${pkgdir}/etc/fonts/conf.d/70-noto-cjk.conf
}

package_zsien-disable-xhc-wake() {
    pkgdesc='My configure files to disable xhc wake'

    install -D ${startdir}/disable-xhc-wake/disable-xhc-wake.conf ${pkgdir}/etc/tmpfiles.d/disable-xhc-wake.conf
}

package_zsien-plasma-desktop() {
    pkgdesc='My configure files of plasma desktop'
    depends=('plasma-meta'
             'plasma5-applets-redshift-control'
             'breeze-blurred-git'
             'materia-gtk-theme'
             'papirus-icon-theme'
             'latte-dock'
             'fcitx-rime'
             'fcitx-gtk2'
             'fcitx-gtk3'
             'fcitx-qt4'
             'fcitx-qt5'
             'fcitx-skin-material'
             'firefox'
             'firefox-i18n-zh-tw',
             'libappindicator-gtk3')

    install -D ${startdir}/plasma-desktop/ZhihsianBreeze.colors ${pkgdir}/usr/share/color-schemes/ZhihsianBreeze.colors
    install -D ${startdir}/plasma-desktop/ZhihsianBreeze.colorscheme ${pkgdir}/usr/share/konsole/ZhihsianBreeze.colorscheme
}
