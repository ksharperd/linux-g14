# Maintainer: Jan Alexander Steffens (heftig) <jan.steffens@gmail.com>

pkgbase=linux-g14
pkgver=5.16.8.arch1
pkgrel=1
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
_fedora_kernel_commit_id=e087e6d70c49c685b4d7cc7364496ade3aed3609
source=(
  "$_srcname::git+https://github.com/archlinux/linux?signed#tag=$_srctag"
  config         # the main kernel config file
  "choose-gcc-optimization.sh"

  "sys-kernel_arch-sources-g14_files-0004-5.15+--more-uarches-for-kernel.patch"::"https://raw.githubusercontent.com/graysky2/kernel_compiler_patch/master/more-uarches-for-kernel-5.15+.patch"
  "sys-kernel_arch-sources-g14_files-0005-lru-multi-generational.patch"
  
  "https://gitlab.com/asus-linux/fedora-kernel/-/archive/$_fedora_kernel_commit_id/fedora-kernel-$_fedora_kernel_commit_id.zip"

  # pull newer version from fedora repo
  "sys-kernel_arch-sources-g14_files-0043-ALSA-hda-realtek-Fix-speakers-not-working-on-Asus-Fl.patch"
  "sys-kernel_arch-sources-g14_files-0046-fan-curvers.patch"
  "sys-kernel_arch-sources-g14_files-0047-asus-nb-wmi-Add-tablet_mode_sw-lid-flip.patch"
  "sys-kernel_arch-sources-g14_files-0048-asus-nb-wmi-fix-tablet_mode_sw_int.patch"
  "sys-kernel_arch-sources-g14_files-0049-ALSA-hda-realtek-Add-quirk-for-ASUS-M16-GU603H.patch"
  "sys-kernel_arch-sources-g14_files-0050-asus-flow-x13-support_sw_tablet_mode.patch"

  # mediatek mt7921 bt/wifi patches
  "sys-kernel_arch-sources-g14_files-8017-mt76-mt7921-enable-VO-tx-aggregation.patch"
  "sys-kernel_arch-sources-g14_files-8018-mt76-mt7921e-fix-possible-probe-failure-after-reboot.patch"
  "sys-kernel_arch-sources-g14_files-8026-cfg80211-dont-WARN-if-a-self-managed-device.patch"

  "sys-kernel_arch-sources-g14_files-8050-r8152-fix-spurious-wakeups-from-s0i3.patch"

  # squashed s0ix enablement through
  "sys-kernel_arch-sources-g14_files-9001-v5.16.8-s0ix-patch-2022-02-08.patch"
  "sys-kernel_arch-sources-g14_files-9004-HID-asus-Reduce-object-size-by-consolidating-calls.patch"
  "sys-kernel_arch-sources-g14_files-9005-acpi-battery-Always-read-fresh-battery-state-on-update.patch"
  
  "sys-kernel_arch-sources-g14_files-9006-amd-c3-entry.patch"
  
  "sys-kernel_arch-sources-g14_files-9009-amd-pstate-sqashed-v7.patch"
  "sys-kernel_arch-sources-g14_files-9010-ACPI-PM-s2idle-Don-t-report-missing-devices-as-faili.patch"

  "sys-kernel_arch-sources-g14_files-9052-x86-csum-Rewrite-optimize-csum_partial.patch"
)

validpgpkeys=(
  'ABAF11C65A2970B130ABE3C479BE3E4300411886'  # Linus Torvalds
  '647F28654894E3BD457199BE38DBBDC86092693E'  # Greg Kroah-Hartman
  'A2FF3A36AAA56654109064AB19802F8B0D70FC30'  # Jan Alexander Steffens (heftig)
  'C7E7849466FE2358343588377258734B41C31549'  # David Runge
)

sha256sums=('SKIP'
            '0707fea88a6b1ff6ec807fd42be595363592db78fdc74da645bfadb940372402'
            '278118011d7a2eeca9971ac97b31bf0c55ab55e99c662ab9ae4717b55819c9a2'
            '380bcf40cc8396e97bd1d7f2577ab2ace51885858d3f155b1fb2dd5469efd00d'
            '7ff5a1fb7fdda19cab12d295e14180e43047ce132ac42aaee8346b045e3e9487'
            '6806c034b7480245a0b9eec448bd79042ff5ff3f9f5efbf2af78227bc56004a8'
            '32bbcde83406810f41c9ed61206a7596eb43707a912ec9d870fd94f160d247c1'
            '0c422d8f420c1518aab1b980c6cdb6e029a4fa9cde1fd99a63670bb105a44f36'
            '15e912a66e4bbce1cf0450f1dc6610653df29df8dd6d5426f9c1b039490436c8'
            'e9e4b03b836e1a86a2a5dc70b0d5512348eb19742f83bee794a3ab7d91bd41cf'
            '982a31e47d3d586789e1b3cdda25f75e3b71d810e7494202089b8f2cef7c0ef9'
            '7ece5cf3e4400ad383fa1bb74ca0633d1eaf5ee2b2819f3d341ab3ed021c66e2'
            '1ce9fd988201c4d2e48794c58acda5b768ec0fea1d29555e99d35cd2712281e4'
            '6dccebe5fb07b6c938ca77854582162088eebbd8cf7e80416c257bfd1b0f9f60'
            '3d8961438b5c8110588ff0b881d472fc71a4304d306808d78a4055a4150f351e'
            'f47a5a5e329e410a0ae7d46b450707d5575a4deda5b3b58281f5eca14938fb21'
            '70c3253a70ce50b1241591df14e4749a1040398a1b2a5a5d0f899fe079208319'
            '544464bf0807b324120767d55867f03014a9fda4e1804768ca341be902d7ade4'
            'f7a4bf6293912bfc4a20743e58a5a266be8c4dbe3c1862d196d3a3b45f2f7c90'
            'ee8794a551e33226900654d5c806183bf3b9b2e06f64fdc322987215d233d399'
            'a3ad5931f6d90a0bdd7258a2b44c21cd2409eb805891d45e8332ae2affd9da3f'
            'e7bd53abc9fddc66790a2e63637b4e2b54ed541f41a2f0fb3aca91ea64ff90dc'
            '261807a9bc838709bd04e65a83eba2fefd8554699e5dfc8da9a1ee8499807813')

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

_fedora_kernel_patch_skip_list=(
  # fedora kernel patches to skip
  # use plain file names or bash glob syntax, ** don't quote globs **

  # multi-select and ranges examples
  # 00{03,05,08}-drm-amdgpu*.patch
  # 00{01..12}-drm-amdgpu*.patch
  
  "linux-kernel-test.patch"           # test patch, please ignore
  patch-*-redhat.patch                # wildcard match any redhat patch version
  
  0001-asus-wmi-Add-support-for-platform_profile.patch
  0001-asus-wmi-Add-panel-overdrive-functionality.patch
  0002-asus-wmi-Add-dgpu-disable-method.patch
  0004-HID-asus-Remove-check-for-same-LED-brightness-on-set.patch
  0001-HID-asus-Prevent-Claymore-sending-suspend-event.patch
  0015-PCI-quirks-Quirk-PCI-d3hot-delay-for-AMD-xhci.patch
)

export KBUILD_BUILD_HOST=archlinux
export KBUILD_BUILD_USER=$pkgbase
export KBUILD_BUILD_TIMESTAMP="$(date -Ru${SOURCE_DATE_EPOCH:+d @$SOURCE_DATE_EPOCH})"

_fedora_patch_in_skip_list() {
  for p in "${_fedora_kernel_patch_skip_list[@]}"; do [[ "$1" == $p ]] && return 0; done
  return 1
}

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

  msg2 "Applying asus-linux patches..."
  local p_err=()
  local p_meh=()

  # this will apply only enabled patches from the fedora-linux kernel.spec
  # this stops us from applying broken or in-progress patches that are in git but aren't actually in use

  local _fkernel_path="../fedora-kernel-${_fedora_kernel_commit_id}"
  for src in $(awk -F ' ' '/^ApplyOptionalPatch.*(patch|diff)$/{print $2}' "${_fkernel_path}/kernel.spec"); do
    src="${src##*/}"
    _fedora_patch_in_skip_list "$src" && continue
    echo "Applying patch $src..."
    if OUT="$(patch --forward -Np1 < "${_fkernel_path}/$src")"; then
      : #plain "Applied patch $src..."
    else
      # if you want to ignore a specific patch failure for some reason do it right here, then 'continue'
      if { echo "$OUT" | grep -qiE 'hunk(|s) FAILED'; }; then
        error "Patch failed $src" && echo "$OUT" && p_err+=("$src") && _throw=y
      else
        warning "Duplicate patch $src" && p_meh+=("$src")
      fi
    fi
  done
  (( ${#p_err[@]} > 0 )) && error "Failed patches:" && for p in ${p_err[@]}; do plain "$p"; done
  (( ${#p_meh[@]} > 0 )) && warning "Duplicate patches:" && for p in ${p_meh[@]}; do plain "$p"; done
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
                  --disable CONFIG_IPW2100

  # select slightly more sane block device driver options; NVMe really should be built in 
  scripts/config  --disable CONFIG_RAPIDIO \
                  --module CONFIG_CDROM \
                  --disable CONFIG_PARIDE \

  # bake in s0ix debugging parameters so we get useful problem reports re: suspend
  scripts/config  --enable CONFIG_CMDLINE_BOOL \
                  --set-str CONFIG_CMDLINE "makepkgplaceholderyolo" \
                  --disable CMDLINE_OVERRIDE

  # HACK: forcibly fixup CONFIG_CMDLINE here as using scripts/config mangles escaped quotes
  sed -i 's#makepkgplaceholderyolo#pm_debug_messages amd_pmc.enable_stb=1 amd_pmc.dyndbg=\\"+p\\" acpi.dyndbg=\\"file drivers/acpi/x86/s2idle.c +p\\"#' .config

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
