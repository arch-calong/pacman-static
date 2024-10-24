# Maintainer: Mark Wagie <mark at manjaro dot org>
# Contributor: Stefano Capitani <stefano@manjaro.org>
# Contributor: Eli Schwartz <eschwartz@archlinux.org>

pkgname=pacman-static
pkgver=7.0.0.r3.g7736133
_cares_ver=1.33.1
_nghttp2_ver=1.63.0
_curlver=8.9.1
_sslver=3.3.2
_zlibver=1.3.1
_xzver=5.6.2
_bzipver=1.0.8
_zstdver=1.5.6
_libarchive_ver=3.7.4
_gpgerrorver=1.50
_libassuanver=3.0.0
_gpgmever=1.23.2
pkgrel=1
# use annotated tag and patch level commit from release branch (can be empty for no patches)
_git_tag=7.0.0
_git_patch_level_commit=77361331ae3864c6ea880e715c5864d59336f275
pkgdesc="Statically-compiled pacman (to fix or install systems without libc)"
arch=('i486' 'i686' 'pentium4' 'x86_64' 'arm' 'armv6h' 'armv7h' 'aarch64')
url="https://www.archlinux.org/pacman/"
license=('GPL-2.0-or-later')
depends=('pacman')
makedepends=('meson' 'musl' 'kernel-headers-musl' 'git')
options=('!emptydirs' '!lto')

# pacman
source=("git+https://gitlab.archlinux.org/pacman/pacman.git#tag=v${_git_tag}?signed"
        pacman-revertme-makepkg-remove-libdepends-and-libprovides.patch::https://gitlab.archlinux.org/pacman/pacman/-/commit/354a300cd26bb1c7e6551473596be5ecced921de.patch)

validpgpkeys=('6645B0A8C7005E78DB1D7864F99FFE0FEAE999BD'  # Allan McRae <allan@archlinux.org>
              'B8151B117037781095514CA7BBDFFC92306B1121') # Andrew Gregory (pacman) <andrew@archlinux.org>
# nghttp2
source+=("https://github.com/nghttp2/nghttp2/releases/download/v$_nghttp2_ver/nghttp2-$_nghttp2_ver.tar.xz")
# c-ares
source+=("https://github.com/c-ares/c-ares/releases/download/v${_cares_ver}/c-ares-${_cares_ver}.tar.gz"{,.asc})
validpgpkeys+=('27EDEAF22F3ABCEB50DB9A125CC908FDB71E12C2'  # Daniel Stenberg <daniel@haxx.se>
               'DA7D64E4C82C6294CB73A20E22E3D13B5411B7CA') # Brad House <brad@brad-house.com>
# curl
source+=("https://curl.haxx.se/download/curl-${_curlver}.tar.gz"{,.asc})
validpgpkeys+=('27EDEAF22F3ABCEB50DB9A125CC908FDB71E12C2') # Daniel Stenberg
# openssl
source+=("https://github.com/openssl/openssl/releases/download/openssl-${_sslver}/openssl-${_sslver}.tar.gz"{,.asc}
         "ca-dir.patch"
         "openssl-3.0.7-no-atomic.patch")
validpgpkeys+=('8657ABB260F056B1E5190839D9C4D26D0E604491'
              '7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C'
              'A21FAB74B0088AA361152586B8EF1A6BA9DA2D5C'
              'EFC0A467D613CB83C7ED6D30D894E2CE8B3D79F5'
              'BA5473A2B0587B07FB27CF2D216094DFD0CB81EF')

validpgpkeys+=('8657ABB260F056B1E5190839D9C4D26D0E604491'  # Matt Caswell <matt@openssl.org>
              '7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C'   # Matt Caswell <matt@openssl.org>
              'A21FAB74B0088AA361152586B8EF1A6BA9DA2D5C'   # Tom�? Mr�z <tm@t8m.info>
              'EFC0A467D613CB83C7ED6D30D894E2CE8B3D79F5')  # OpenSSL security team key
# zlib
source+=("https://zlib.net/zlib-${_zlibver}.tar.gz"{,.asc})
validpgpkeys+=('5ED46A6721D365587791E2AA783FCD8E58BCAFBA') # Mark Adler <madler@alumni.caltech.edu>
# xz
source+=("git+https://github.com/tukaani-project/xz#tag=v${_xzver}")
validpgpkeys+=('3690C240CE51B4670D30AD1C38EE757D69184620')  # Lasse Collin <lasse.collin@tukaani.org>
# bzip2
source+=("https://sourceware.org/pub/bzip2/bzip2-${_bzipver}.tar.gz"{,.sig})
validpgpkeys+=('EC3CFE88F6CA0788774F5C1D1AA44BE649DE760A') # Mark Wielaard <mark@klomp.org>
# zstd
source+=("https://github.com/facebook/zstd/releases/download/v${_zstdver}/zstd-${_zstdver}.tar.zst"{,.sig})
validpgpkeys+=('4EF4AC63455FC9F4545D9B7DEF8FE99528B52FFD') # Zstandard Release Signing Key <signing@zstd.net>
# libgpg-error
source+=("https://gnupg.org/ftp/gcrypt/libgpg-error/libgpg-error-${_gpgerrorver}.tar.bz2"{,.sig})
validpgpkeys+=('D8692123C4065DEA5E0F3AB5249B39D24F25E3B6'  # Werner Koch
               '031EC2536E580D8EA286A9F22071B08A33BD3F06'  # NIIBE Yutaka (GnuPG Release Key) <gniibe@fsij.org>
               '6DAA6E64A76D2840571B4902528897B826403ADA') # "Werner Koch (dist signing 2020)"
# libassuan
source+=("https://gnupg.org/ftp/gcrypt/libassuan/libassuan-${_libassuanver}.tar.bz2"{,.sig})
# gpgme
source+=("https://www.gnupg.org/ftp/gcrypt/gpgme/gpgme-${_gpgmever}.tar.bz2"{,.sig})
validpgpkeys+=('AC8E115BF73E2D8D47FA9908E98E9B2D19C6C8BD') #  Niibe Yutaka (GnuPG Release Key)
# libarchive
source+=("https://github.com/libarchive/libarchive/releases/download/v${_libarchive_ver}/libarchive-${_libarchive_ver}.tar.xz"{,.asc})
validpgpkeys+=('A5A45B12AD92D964B89EEE2DEC560C81CEC2276E'  # Martin Matuska <mm@FreeBSD.org>
              'DB2C7CF1B4C265FAEF56E3FC5848A18B8F14184B') # Martin Matuska <martin@matuska.org>

sha512sums=('44e00c2bc259fe6a85de71f7fd8a43fcfd1b8fb7d920d2267bd5b347e02f1dab736b3d96e31faf7b535480398e2348f7c0b9914e51ca7e12bab2d5b8003926b4'
            '1a108c4384b6104e627652488659de0b1ac3330640fc3250f0a283af7c5884daab187c1efc024b2545262da1911d2b0b7b0d5e4e5b68bb98db25a760c9f1fb1a'
            'ac5005f33664981e194730223881f4207c9570cb8d9bba51b5592a3e7eb59455ebe25bf190211811513c64497a1b42ec7a82cc7f810059f46c99a83dd2d6cef9'
            'b5ec4f08539be552f01d49f03327e3999754b940d83c63fbd934c2ed34cf7f05c3f90c9eb64a78a3d7862280bf75765296576a70a6029257daaf90e3e35ab3e4'
            'SKIP'
            '27c91a58f23f02dd150556edaa73e1be08a93134d3d05049e546b39f05e0f4383e41bf6a56a643eae03eda0f39a527059510b2e34167ae9e7c75b393964a9f8b'
            'SKIP'
            '5ae47bf1aed2740a33ba5df7dc7345a6738aa6bfa3c9c4de5e51742485e24b25192988d7a2c1b8201ef70056ad8abd0ca78b3d55abe24c0b0373d83b47ed9b74'
            'SKIP'
            'b1873dbb7a49460b007255689102062756972de5cc2d38b12cc9f389b6be412da6797579b1acd3717a8cd2ee118fd9801b94e55f063d4328f050f0876a5eb53c'
            'b5887ea77417fae49b6cb1e9fa782d3021f268d5219701d87a092235964f73fa72a31428b630445517f56f2bb69dcbbb24119ef9dbf8b4e40a753369a9f9a16f'
            '580677aad97093829090d4b605ac81c50327e74a6c2de0b85dd2e8525553f3ddde17556ea46f8f007f89e435493c9a20bc997d1ef1c1c2c23274528e3c46b94f'
            'SKIP'
            'af3fd021a9c8eaacfb1ae2af3f7e2a0b0554068461de5be3e2c631174cf5fe15425b739832e826c0fb158484b8cea53701be8c568d7ce1f6113b4630205f5c26'
            'SKIP'
            '083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3'
            'SKIP'
            '21f9da445afd76acaf3acb22d216c2b584d95e8c68e00f5cb3f6673f2d556dd14a7593344adf8ffd194bba3314387ee0e486d6248f6c935abca2edd8a4cf95ed'
            'SKIP'
            '96e466d892a50843af6d7c08c0da602518bc6a28836bfc35f0a28cde74d368f57c5c70c65f0f41edb4fc1ca5ebd00f2ece531d8b3eb1bd6db566adbb29bc61ff'
            'SKIP'
            '7c5c95c1b85bef2d4890c068a5a8ea8a1fe0d8def6ab09e5f34fc2746d8808bbb0fc168e3bd66d52ee5ed799dcf9f258f4125cda98c8384f6411bcad8d8b3139'
            'SKIP'
            '6cfcd07e81a93de240582de5a46545420cee93d1f27fe20ea2c983780fdd3036b69fdba073cf549d68a20791e189bf4b3cdde14a43f912d2ab9ef3414c83ac75'
            'SKIP'
            '84bc346ba15861ab10aa54a3d687de955178e4efbe12bf3a49a467181e7f819673949f131f4c8338de8ed6e319a8565af376e5a540380bda08e60dffbc7c8686'
            'SKIP')

export LDFLAGS="$LDFLAGS -static"
export CC=musl-gcc
export CXX=musl-gcc

# https://www.openwall.com/lists/musl/2014/11/05/3
# fstack-protector and musl do not get along but only on i686
if [[ $CARCH = i686 || $CARCH = pentium4 || $CARCH = i486 ]]; then
    # silly build systems have configure checks or buildtime programs that don't CFLAGS but do do CC
    export CC="musl-gcc -fno-stack-protector"
    export CXX="musl-gcc -fno-stack-protector"
    export CFLAGS="${CFLAGS/-fstack-protector-strong/}"
    export CXXFLAGS="${CXXFLAGS/-fstack-protector-strong/}"
fi

# to enable func64 interface in musl for 64-bit file system functions
export CFLAGS+=' -D_LARGEFILE64_SOURCE'
export CXXFLAGS+=' -D_LARGEFILE64_SOURCE'

# keep using xz-compressed packages, because one use of the package is to
# recover on systems with broken zstd support in libarchive
[[ $PKGEXT = .pkg.tar.zst ]] && PKGEXT=.pkg.tar.xz

prepare() {
    cd "${srcdir}/pacman"

    # apply patch level commits on top of annotated tag for pacman
    if [[ -n ${_git_patch_level_commit} ]]; then
        if [[ v${_git_tag} != $(git describe --tags --abbrev=0 "${_git_patch_level_commit}") ]] then
            error "patch level commit ${_git_patch_level_commit} is not a descendant of v${_git_tag}"
            exit 1
        fi
        git rebase "${_git_patch_level_commit}"
    fi

    # handle local pacman patches
    local -a patches
    patches=($(printf '%s\n' "${source[@]}" | grep 'pacman-.*.patch'))
    patches=("${patches[@]%%::*}")
    patches=("${patches[@]##*/}")

    if (( ${#patches[@]} != 0 )); then
        for patch in "${patches[@]}"; do
            if [[ $patch =~ revertme-* ]]; then
                msg2 "Reverting patch $patch..."
                patch -RNp1 < "../$patch"
            else
                msg2 "Applying patch $patch..."
                patch -Np1 < "../$patch"
            fi
        done
    fi

    # openssl
    cd "${srcdir}"/openssl-${_sslver}
    patch -Np1 -i "${srcdir}/ca-dir.patch"
    case ${CARCH} in
        arm|armv6h|armv7h)
            # special patch to omit -latomic when installing pkgconfig files
            msg2 "Applying openssl patch openssl-3.0.7-no-atomic.patch..."
            patch -Np1 -i "${srcdir}/openssl-3.0.7-no-atomic.patch"
    esac
}

build() {
    export PKG_CONFIG_PATH="${srcdir}"/temp/usr/lib/pkgconfig
    export PATH="${srcdir}/temp/usr/bin:${PATH}"

    # openssl
    cd "${srcdir}"/openssl-${_sslver}
    case ${CARCH} in
        x86_64)
            openssltarget='linux-x86_64'
            optflags='enable-ec_nistp_64_gcc_128'
            ;;
        pentium4)
            openssltarget='linux-elf'
            optflags=''
            ;;
        i686)
            openssltarget='linux-elf'
            optflags='no-sse2'
            ;;
        i486)
            openssltarget='linux-elf'
            optflags='386 no-threads'
            ;;
        arm|armv6h|armv7h)
            openssltarget='linux-armv4'
            optflags=''
            ;;
        aarch64)
            openssltarget='linux-aarch64'
            optflags='no-afalgeng'
            ;;
    esac
    # mark stack as non-executable: http://bugs.archlinux.org/task/12434
    ./Configure --prefix="${srcdir}"/temp/usr \
                --openssldir=/etc/ssl \
                --libdir=lib \
                -static \
                no-ssl3-method \
                ${optflags} \
                "${openssltarget}" \
                "-Wa,--noexecstack ${CPPFLAGS} ${CFLAGS} ${LDFLAGS}"
    make build_libs
    make install_dev

    # xz
    cd "${srcdir}"/xz
    ./autogen.sh --no-po4a --no-doxygen
    ./configure --prefix="${srcdir}"/temp/usr \
                --disable-shared
    cd src/liblzma
    make
    make install

    # bzip2
    cd "${srcdir}"/bzip2-${_bzipver}
    sed -i "s|-O2|${CFLAGS}|g;s|CC=gcc|CC=${CC}|g" Makefile
    make libbz2.a
    install -Dvm644 bzlib.h "${srcdir}"/temp/usr/include/
    install -Dvm644 libbz2.a "${srcdir}"/temp/usr/lib/

    cd "${srcdir}"/zstd-${_zstdver}/lib
    make libzstd.a
    make PREFIX="${srcdir}"/temp/usr install-pc install-static install-includes

    # zlib
    cd "${srcdir}/"zlib-${_zlibver}
    ./configure --prefix="${srcdir}"/temp/usr \
                --static
    make libz.a
    make install

    # libarchive
    cd "${srcdir}"/libarchive-${_libarchive_ver}
    CPPFLAGS="-I${srcdir}/temp/usr/include" CFLAGS="-L${srcdir}/temp/usr/lib" \
        ./configure --prefix="${srcdir}"/temp/usr \
                    --without-xml2 \
                    --without-nettle \
                    --disable-{bsdtar,bsdcat,bsdcpio,bsdunzip} \
                    --without-expat \
                    --disable-shared
    make
    make install-{includeHEADERS,libLTLIBRARIES,pkgconfigDATA,includeHEADERS}

    # nghttp2
    cd "${srcdir}"/nghttp2-${_nghttp2_ver}
    ./configure --prefix="${srcdir}"/temp/usr \
        --disable-shared \
        --disable-examples \
        --disable-python-bindings
    make -C lib
    make -C lib install

    # c-ares
    # needed for curl, which does not use it in the repos
    # but seems to be needed for static builds
    cd "${srcdir}"/c-ares-${_cares_ver}
    ./configure --prefix="${srcdir}"/temp/usr \
        --disable-shared
    make -C src/lib
    make install-pkgconfigDATA
    make -C src/lib install
    make -C include install

    # curl
    cd "${srcdir}"/curl-${_curlver}
    # c-ares is not detected via pkg-config :(
    ./configure --prefix="${srcdir}"/temp/usr \
                --disable-shared \
                --with-ca-bundle=/etc/ssl/certs/ca-certificates.crt \
                --disable-{dict,gopher,imap,ldap,ldaps,manual,pop3,rtsp,smb,smtp,telnet,tftp} \
                --without-{brotli,libidn2,librtmp,libssh2,libpsl} \
                --disable-libcurl-option \
                --with-openssl \
                --enable-ares="${srcdir}"/temp/usr
    make -C lib
    make install-pkgconfigDATA
    make -C lib install
    make -C include install

    # libgpg-error
    cd "${srcdir}"/libgpg-error-${_gpgerrorver}
    ./configure --prefix="${srcdir}"/temp/usr \
        --disable-shared
    make -C src
    make -C src install-{binSCRIPTS,libLTLIBRARIES,nodist_includeHEADERS,pkgconfigDATA}

    # libassuan
    cd "${srcdir}"/libassuan-${_libassuanver}
    ./configure --prefix="${srcdir}"/temp/usr \
        --disable-shared
    make -C src
    make -C src install-{binSCRIPTS,libLTLIBRARIES,nodist_includeHEADERS,pkgconfigDATA}

    # gpgme
    cd "${srcdir}"/gpgme-${_gpgmever}
    ./configure --prefix="${srcdir}"/temp/usr \
        --disable-fd-passing \
        --disable-shared \
        --disable-languages
    make -C src
    make -C src install-{binSCRIPTS,libLTLIBRARIES,nodist_includeHEADERS,pkgconfigDATA}

    # ew libtool
    rm "${srcdir}"/temp/usr/lib/lib*.la

    # Finally, it's a pacman!
    mkdir -p "${srcdir}"/pacman
    cd "${srcdir}"/pacman
    meson --prefix=/usr \
        --includedir=lib/pacman/include \
        --libdir=lib/pacman/lib \
        --buildtype=plain \
        -Dbuildstatic=true \
        -Ddefault_library=static \
        -Ddoc=disabled \
        -Ddoxygen=disabled \
        -Dldconfig=/usr/bin/ldconfig \
        -Dscriptlet-shell=/usr/bin/bash \
        build
    meson compile -C build
}

package() {
    cd "${srcdir}"/pacman
    DESTDIR="${pkgdir}" meson install -C build

    rm -rf "${pkgdir}"/usr/share "${pkgdir}"/etc
    for exe in "${pkgdir}"/usr/bin/*; do
        if [[ -f ${exe} && $(head -c4 "${exe}") = $'\x7fELF' ]]; then
            mv "${exe}" "${exe}"-static
        else
            rm "${exe}"
        fi
    done

    cp -a "${srcdir}"/temp/usr/{bin,include,lib} "${pkgdir}"/usr/lib/pacman/
    sed -i "s@${srcdir}/temp/usr@/usr/lib/pacman@g" \
        "${pkgdir}"/usr/lib/pacman/lib/pkgconfig/*.pc \
        "${pkgdir}"/usr/lib/pacman/bin/*
}

