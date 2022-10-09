# Maintainer: Jan Alexander Steffens (heftig) <jan.steffens@gmail.com>

pkgbase=linux-g14
pkgver=5.19.13.arch1
pkgrel=2
pkgdesc='Linux'
_srctag=v${pkgver%.*}-${pkgver##*.}
url="https://gitlab.com/dragonn/linux-g14.git"
arch=(x86_64)
license=(GPL2)
makedepends=(
  bc kmod libelf pahole cpio tar xz
  xmlto
  git
  "gcc>=11.0"
)
options=('!strip')
_srcname=archlinux-linux

source=(
  "$_srcname::git+https://github.com/archlinux/linux?signed#tag=$_srctag"
  config         # the main kernel config file
  "choose-gcc-optimization.sh"

  "sys-kernel_arch-sources-g14_files-0004-5.15+--more-uarches-for-kernel.patch"::"https://raw.githubusercontent.com/graysky2/kernel_compiler_patch/master/more-uarches-for-kernel-5.15+.patch"
  "sys-kernel_arch-sources-g14_files-0005-lru-multi-generational.patch"

  0001-acpi-proc-idle-skip-dummy-wait.patch
  0001-asus-wmi-tuf-gpu-fan.patch
  0001-asus-wmi-Expand-support-of-GPU-fan-to-read-RPM-and-l.patch
  0001-HID-amd_sfh-Add-keyguard-for-ASUS-ROG-X13-tablet.patch
  0001-platform-x86-asus-wmi-Convert-all-attr-show-to-use-s.patch
  0001-s2idle-use-microsoft-guid.patch
  0002-platform-x86-asus-wmi-Use-kobj_to_dev.patch
  0002-s2idle-use-microsoft-guid.patch
  0003-platform-x86-asus-wmi-Document-the-dgpu_disable-sysf.patch
  0003-s2idle-use-microsoft-guid.patch
  0004-platform-x86-asus-wmi-Document-the-egpu_enable-sysfs.patch
  0004-s2idle-use-microsoft-guid.patch
  0005-platform-x86-asus-wmi-Document-the-panel_od-sysfs-at.patch
  0005-s2idle-use-microsoft-guid.patch
  0006-platform-x86-asus-wmi-Refactor-disable_gpu-attribute.patch
  0006-s2idle-use-microsoft-guid.patch
  0007-platform-x86-asus-wmi-Refactor-egpu_enable-attribute.patch
  0007-s2idle-use-microsoft-guid.patch
  0008-s2idle-use-microsoft-guid.patch
  0008-platform-x86-asus-wmi-Refactor-panel_od-attribute.patch
  0009-platform-x86-asus-wmi-Simplify-some-of-the-_check_pr.patch
  0010-platform-x86-asus-wmi-Support-the-hardware-GPU-MUX-o.patch
  0011-platform-x86-asus-wmi-Adjust-tablet-lidflip-handling.patch
  0012-platform-x86-asus-wmi-Add-support-for-ROG-X13-tablet.patch
  0013-platform-x86-asus-wmi-Simplify-tablet-mode-switch-pr.patch
  0014-platform-x86-asus-wmi-Simplify-tablet-mode-switch-ha.patch
  0017-asus-wmi-Implement-TUF-laptop-keyboard-LED-modes.patch
  0018-asus-wmi-Implement-TUF-laptop-keyboard-power-states.patch
  #0019-HID-amd_sfh-Add-keyguard-for-ASUS-ROG-X13-tablet.patch
  0020-asus-wmi-Modify-behaviour-of-Fn-F5-fan-key.patch
  0021-rog-x16-patch-test1.patch
  0022-gv601r-tablet-mode-test.patch
  0023-mediatek-bt-add-e0e2.patch
  0024-pahole-124-fix.patch

  "sys-kernel_arch-sources-g14_files-0047-asus-nb-wmi-Add-tablet_mode_sw-lid-flip.patch"
  "sys-kernel_arch-sources-g14_files-0048-asus-nb-wmi-fix-tablet_mode_sw_int.patch"
  "sys-kernel_arch-sources-g14_files-0049-ALSA-hda-realtek-Add-quirk-for-ASUS-M16-GU603H.patch"
)

validpgpkeys=(
  'ABAF11C65A2970B130ABE3C479BE3E4300411886'  # Linus Torvalds
  '647F28654894E3BD457199BE38DBBDC86092693E'  # Greg Kroah-Hartman
  'A2FF3A36AAA56654109064AB19802F8B0D70FC30'  # Jan Alexander Steffens (heftig)
  'C7E7849466FE2358343588377258734B41C31549'  # David Runge
)

sha256sums=('SKIP'
            '7dcbed3f72a2a84dd5b40bbe38c8fa2d82d1d68fcaa657f40163a6123a19886f'
            '278118011d7a2eeca9971ac97b31bf0c55ab55e99c662ab9ae4717b55819c9a2'
            '380bcf40cc8396e97bd1d7f2577ab2ace51885858d3f155b1fb2dd5469efd00d'
            'e0f9b3e968568552b7852a5ce41e7fa5b9b8784273c483a9b1372bc420758ff8'
            '40e4c300be6681ab3b30042eb4bb5981081ce029b2bdd4773a38b4a9f65e943e'
            '4246dff9cbaee0de807711824fbc056a836321bb800d3e6ddad18fabc86d3def'
            '9efcef7aab8094ed3596cba872527d6e838c760ba4f4c5b7b1586a963b71d576'
            'f6f7c233d982be80eb6cd13ba8223d1989eca82107201b6bc4673ce840877aa5'
            'a51b11bd64915454981aeb0aa680efb508a24a6df552caa17cd01e31a776a7e5'
            'ab7f8697494e0969db63ff020aae244e2dc4ee52c06559878938bd042ee20a79'
            '02424be0d9a42d8b19a5ed0a3a108b35dc31a9e2938efa9cf81f52a682e39f63'
            'c419173ff28d78bac07f386180065489618ccbcd14bf88298a68d8640ad10c43'
            '113289ef6a4e813bae02487a4cf961f821e000a195e25ff4ffcb56eedd42b12b'
            'fe3a66bac3076918164bcb423851bca9e16ef870be1f6445214c370a4db68dc5'
            'f7b1f4d3c461f010c89507ff378df8232ea5d4bfcda600c5a06e8e09128d5291'
            '751378e4e8e7d97025087e6b98cd25c6ca4d76b1cf18ffad194776f8824a9320'
            '625e5f05b3fbdccedb1bf48b42422cd8de1f9bb3f621b37c569bd1081ba52e43'
            '3d0e38901ae7fe4f242ebb6617b5f8745286f82dd6fa862a3275d78e44e57ebc'
            '4eca79899c890d07f20b79534730d415853e1ec80b38b9b6a30301e5806961f3'
            '9866928fb441eb03dc273e194a78b8d6563d30389b7f1611201c9a1927628dc5'
            '7e575f72423e01b74716e1fc21a3364f4cac29366b48caa0cda3504f75071ad3'
            '349209cf1bb3a6701c4be5348f889ae116d6ae6205a5f3372d1150362ef8d153'
            '7057f33c63880a540f5dcba0945140f9dccb2a6de6715eb5853d65c5447c1736'
            'd6f06dfee9d7910208c3851e730ccb79bf349b5ea5f8ab74f994489c679c40e3'
            '83ff058305e6fc0920584bff9c8ffd2e48590e659652a7c8ae7fc4310b129ad3'
            '2bbb9725cfdd834553ef30f81609bd9b6c4f6a71caf8da1c65eb413b68d3d98a'
            '92e63800f0ec71456345cd7152dac44996ea24e4bc24a3a5a07c6e8e29d4ab6e'
            'c47962c06c85fcaa8c8cc5a9bbd8eff56968caeb4e777ef99f2bbda731398718'
            '87d3df1c0eac4b7d301b2dc375f9e754429ca394c9ff09218a00ab1462627e24'
            'b636fc36762bbd8d83a09bcb448d7c2ad176139068e15f162a3da01769a4c6e1'
            '6fe53b9f7423b441d1de6e229b656376515fe003e0c6a11c982f75fabbecb018'
            '6907a750183e1f06c4b15014f078bcd15cb4ea498fd9d4c5c4c4d1955dac69d3'
            '15e912a66e4bbce1cf0450f1dc6610653df29df8dd6d5426f9c1b039490436c8'
            'e9e4b03b836e1a86a2a5dc70b0d5512348eb19742f83bee794a3ab7d91bd41cf'
            '982a31e47d3d586789e1b3cdda25f75e3b71d810e7494202089b8f2cef7c0ef9'
            'f47a5a5e329e410a0ae7d46b450707d5575a4deda5b3b58281f5eca14938fb21'
            '544464bf0807b324120767d55867f03014a9fda4e1804768ca341be902d7ade4'
            'f7a4bf6293912bfc4a20743e58a5a266be8c4dbe3c1862d196d3a3b45f2f7c90'
            'e7bd53abc9fddc66790a2e63637b4e2b54ed541f41a2f0fb3aca91ea64ff90dc'
            'f61452c84bc8b8e6907e26d1503be583aa0534516ea7d5607be315ab198c060b')

# notable microarch levels:
#
# 14, Zen2
# 15, Zen3
# 38, Skylake (Comet Lake laptops)
# 93, x86-64-v3 (package default)
# 98, Intel Native
# 99, AMD Native
if [ -z ${_microarchitecture+x} ]; then
  _microarchitecture=93
fi

export KBUILD_BUILD_HOST=archlinux
export KBUILD_BUILD_USER=$pkgbase
export KBUILD_BUILD_TIMESTAMP="$(date -Ru${SOURCE_DATE_EPOCH:+d @$SOURCE_DATE_EPOCH})"

prepare() {
  cd $_srcname

  echo "Setting version..."
  scripts/setlocalversion --save-scmversion
  #echo '' >.scmversion                        # HACK:  maybe needed
  echo "-$pkgrel" > localversion.99-pkgrel
  echo "${pkgbase#linux}" > localversion.20-pkgname

  local src
  for src in "${source[@]}"; do
    src="${src%%::*}"
    src="${src##*/}"
    [[ $src = *.patch ]] || continue
    msg2 "Applying patch $src..."
    patch -Np1 < "../$src"
  done

  # if throw is defined we had a hard patch failure, propagate it and stop so we can address
  [[ -z "$_throw" ]]

  echo "Setting config..."
  cp ../config .config

  make olddefconfig

  # let user choose microarchitecture optimization in GCC
  # this needs to run *after* `make olddefconfig` so that our newly added configuration macros exist
  sh ${srcdir}/choose-gcc-optimization.sh $_microarchitecture

  make -s kernelrelease > version
  echo "Prepared $pkgbase version $(<version)"

  scripts/config --enable CONFIG_PINCTRL_AMD
  scripts/config --enable CONFIG_X86_AMD_PSTATE
  scripts/config --module CONFIG_AMD_PMC

  scripts/config --disable CONFIG_MODULE_COMPRESS_NONE \
                 --enable CONFIG_MODULE_COMPRESS_ZSTD

  ## SET default LRU parameters
  scripts/config --enable CONFIG_LRU_GEN
  scripts/config --enable CONFIG_LRU_GEN_ENABLED
  scripts/config --disable CONFIG_LRU_GEN_STATS
  scripts/config --set-val CONFIG_NR_LRU_GENS 7
  scripts/config --set-val CONFIG_TIERS_PER_GEN 4

  # DISABLE not need modules on ROG laptops
  # XXX: I'm going to make an opinionated decision here and save everyone some compilation time
  # XXX: on drivers almost no-one is going to use; if you need any of theese turn them on in myconfig
  scripts/config  --disable CONFIG_INFINIBAND \
                  --disable CONFIG_DRM_NOUVEAU \
                  --disable CONFIG_PCMCIA_WL3501 \
                  --disable CONFIG_PCMCIA_RAYCS \
                  --disable CONFIG_IWL3945 \
                  --disable CONFIG_IWL4965 \
                  --disable CONFIG_IPW2200 \
                  --disable CONFIG_IPW2100 \
                  --disable CONFIG_FB_NVIDIA \
                  --disable CONFIG_SENSORS_ASUS_EC \
                  --disable CONFIG_SENSORS_ASUS_WMI_EC

  # select slightly more sane block device driver options; NVMe really should be built in 
  scripts/config  --disable CONFIG_RAPIDIO \
                  --module CONFIG_CDROM \
                  --disable CONFIG_PARIDE \

  # bake in s0ix debugging parameters so we get useful problem reports re: suspend
  scripts/config  --enable CONFIG_CMDLINE_BOOL \
                  --set-str CONFIG_CMDLINE "makepkgplaceholderyolo" \
                  --disable CMDLINE_OVERRIDE

  # HACK: forcibly fixup CONFIG_CMDLINE here as using scripts/config mangles escaped quotes
  sed -i 's#makepkgplaceholderyolo#ibt=off pm_debug_messages amd_pmc.enable_stb=1 amd_pmc.dyndbg=\\"+p\\" acpi.dyndbg=\\"file drivers/acpi/x86/s2idle.c +p\\"#' .config

  # Note the double escaped quotes above, sed strips one; the final result in .config needs to contain single slash
  # escaped quotes (eg: `CONFIG_CMDLINE="foo.dyndbg=\"+p\""`) to avoid dyndbg parse errors at boot. This is impossible
  # with the current kernel config script.


}

build() {
  cd $_srcname
  make all
}

_package() {
  pkgdesc="The $pkgdesc kernel and modules"
  depends=(coreutils kmod initramfs)
  optdepends=('crda: to set the correct wireless channels of your country'
              'linux-firmware: firmware images needed for some devices')
  provides=(VIRTUALBOX-GUEST-MODULES WIREGUARD-MODULE linux-rog)
  replaces=(virtualbox-guest-modules-arch wireguard-arch)

  cd $_srcname
  local kernver="$(<version)"
  local modulesdir="$pkgdir/usr/lib/modules/$kernver"

  echo "Installing boot image..."
  # systemd expects to find the kernel here to allow hibernation
  # https://github.com/systemd/systemd/commit/edda44605f06a41fb86b7ab8128dcf99161d2344
  install -Dm644 "$(make -s image_name)" "$modulesdir/vmlinuz"

  # Used by mkinitcpio to name the kernel
  echo "$pkgbase" | install -Dm644 /dev/stdin "$modulesdir/pkgbase"

  echo "Installing modules..."
  make INSTALL_MOD_PATH="$pkgdir/usr" INSTALL_MOD_STRIP=1 modules_install

  # remove build and source links
  rm "$modulesdir"/{source,build}
}

_package-headers() {
  pkgdesc="Headers and scripts for building modules for the $pkgdesc kernel"
  provides=(linux-rog linux-rog-headers)
  depends=(pahole)

  cd $_srcname
  local builddir="$pkgdir/usr/lib/modules/$(<version)/build"

  echo "Installing build files..."
  install -Dt "$builddir" -m644 .config Makefile Module.symvers System.map \
    localversion.* version vmlinux
  install -Dt "$builddir/kernel" -m644 kernel/Makefile
  install -Dt "$builddir/arch/x86" -m644 arch/x86/Makefile
  cp -t "$builddir" -a scripts

  # add objtool for external module building and enabled VALIDATION_STACK option
  install -Dt "$builddir/tools/objtool" tools/objtool/objtool

  # required when DEBUG_INFO_BTF_MODULES is enabled
  install -Dt "$builddir/tools/bpf/resolve_btfids" tools/bpf/resolve_btfids/resolve_btfids

  # add xfs and shmem for aufs building
  mkdir -p "$builddir"/{fs/xfs,mm}

  echo "Installing headers..."
  cp -t "$builddir" -a include
  cp -t "$builddir/arch/x86" -a arch/x86/include
  install -Dt "$builddir/arch/x86/kernel" -m644 arch/x86/kernel/asm-offsets.s

  install -Dt "$builddir/drivers/md" -m644 drivers/md/*.h
  install -Dt "$builddir/net/mac80211" -m644 net/mac80211/*.h

  # http://bugs.archlinux.org/task/13146
  install -Dt "$builddir/drivers/media/i2c" -m644 drivers/media/i2c/msp3400-driver.h

  # http://bugs.archlinux.org/task/20402
  install -Dt "$builddir/drivers/media/usb/dvb-usb" -m644 drivers/media/usb/dvb-usb/*.h
  install -Dt "$builddir/drivers/media/dvb-frontends" -m644 drivers/media/dvb-frontends/*.h
  install -Dt "$builddir/drivers/media/tuners" -m644 drivers/media/tuners/*.h

  echo "Installing KConfig files..."
  find . -name 'Kconfig*' -exec install -Dm644 {} "$builddir/{}" \;

  echo "Removing unneeded architectures..."
  local arch
  for arch in "$builddir"/arch/*/; do
    [[ $arch = */x86/ ]] && continue
    echo "Removing $(basename "$arch")"
    rm -r "$arch"
  done

  echo "Removing documentation..."
  rm -r "$builddir/Documentation"

  echo "Removing broken symlinks..."
  find -L "$builddir" -type l -printf 'Removing %P\n' -delete

  echo "Removing loose objects..."
  find "$builddir" -type f -name '*.o' -printf 'Removing %P\n' -delete

  echo "Stripping build tools..."
  local file
  while read -rd '' file; do
    case "$(file -bi "$file")" in
      application/x-sharedlib\;*)      # Libraries (.so)
        strip -v $STRIP_SHARED "$file" ;;
      application/x-archive\;*)        # Libraries (.a)
        strip -v $STRIP_STATIC "$file" ;;
      application/x-executable\;*)     # Binaries
        strip -v $STRIP_BINARIES "$file" ;;
      application/x-pie-executable\;*) # Relocatable binaries
        strip -v $STRIP_SHARED "$file" ;;
    esac
  done < <(find "$builddir" -type f -perm -u+x ! -name vmlinux -print0)

  echo "Stripping vmlinux..."
  strip -v $STRIP_STATIC "$builddir/vmlinux"

  echo "Adding symlink..."
  mkdir -p "$pkgdir/usr/src"
  ln -sr "$builddir" "$pkgdir/usr/src/$pkgbase"
}


pkgname=("$pkgbase" "$pkgbase-headers")
for _p in "${pkgname[@]}"; do
  eval "package_$_p() {
    $(declare -f "_package${_p#$pkgbase}")
    _package${_p#$pkgbase}
  }"
done

# vim:set ts=8 sts=2 sw=2 et:
