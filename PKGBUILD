# Maintainer: Stefano Capitani <stefano@manjaro.org>
# Maintainer: Mark Wagie <mark at manjaro dot org>

# Arch credits:
# Maintainer: Eli Schwartz <eschwartz@archlinux.org>

pkgname=pacman-static
pkgver=6.0.1
_cares_ver=1.18.1
_nghttp2_ver=1.46.0
_curlver=7.81.0
_sslver=1.1.1m
_zlibver=1.2.11
_xzver=5.2.5
_bzipver=1.0.8
_zstdver=1.5.2
_libarchive_ver=3.5.2
_gpgerrorver=1.44
_libassuanver=2.5.5
_gpgmever=1.16.0
pkgrel=2
pkgdesc="Statically-compiled pacman (to fix or install systems without libc)"
arch=('x86_64' 'aarch64')
url="https://www.archlinux.org/pacman/"
license=('GPL')
depends=('pacman')
makedepends=('meson' 'musl' 'kernel-headers-musl')
options=('!emptydirs')

# pacman
source=("https://sources.archlinux.org/other/pacman/pacman-${pkgver}.tar.xz"{,.sig})
validpgpkeys=('6645B0A8C7005E78DB1D7864F99FFE0FEAE999BD'  # Allan McRae <allan@archlinux.org>
              'B8151B117037781095514CA7BBDFFC92306B1121') # Andrew Gregory (pacman) <andrew@archlinux.org>
# nghttp2
source+=("https://github.com/nghttp2/nghttp2/releases/download/v$_nghttp2_ver/nghttp2-$_nghttp2_ver.tar.xz")
# c-ares
source+=("https://c-ares.haxx.se/download/c-ares-${_cares_ver}.tar.gz"{,.asc})
validpgpkeys+=('27EDEAF22F3ABCEB50DB9A125CC908FDB71E12C2') # Daniel Stenberg <daniel@haxx.se>
# curl
source+=("https://curl.haxx.se/download/curl-${_curlver}.tar.gz"{,.asc})
# openssl
source+=("https://www.openssl.org/source/openssl-${_sslver}.tar.gz"{,.asc}
         "ca-dir.patch")
validpgpkeys+=('8657ABB260F056B1E5190839D9C4D26D0E604491'  # Matt Caswell <matt@openssl.org>
               '7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C') # Richard Levitte <levitte@openssl.org>
# zlib
source+=("https://zlib.net/zlib-${_zlibver}.tar.gz"{,.asc})
validpgpkeys+=('5ED46A6721D365587791E2AA783FCD8E58BCAFBA') # Mark Adler <madler@alumni.caltech.edu>
# xz
source+=("https://tukaani.org/xz/xz-${_xzver}.tar.gz"{,.sig})
validpgpkeys+=('3690C240CE51B4670D30AD1C38EE757D69184620') # Lasse Collin <lasse.collin@tukaani.org>
# bzip2
source+=("https://sourceware.org/pub/bzip2/bzip2-${_bzipver}.tar.gz"{,.sig})
validpgpkeys+=('EC3CFE88F6CA0788774F5C1D1AA44BE649DE760A') # Mark Wielaard <mark@klomp.org>
# zstd
source+=("https://github.com/facebook/zstd/releases/download/v${_zstdver}/zstd-${_zstdver}.tar.zst"{,.sig})
validpgpkeys+=('4EF4AC63455FC9F4545D9B7DEF8FE99528B52FFD') # Zstandard Release Signing Key <signing@zstd.net>
# libgpg-error
source+=("https://gnupg.org/ftp/gcrypt/libgpg-error/libgpg-error-${_gpgerrorver}.tar.bz2"{,.sig})
validpgpkeys+=('6DAA6E64A76D2840571B4902528897B826403ADA'  # "Werner Koch (dist signing 2020)"
               '031EC2536E580D8EA286A9F22071B08A33BD3F06') # NIIBE Yutaka (GnuPG Release Key) <gniibe@fsij.org>
# libassuan
source+=("https://gnupg.org/ftp/gcrypt/libassuan/libassuan-${_libassuanver}.tar.bz2"{,.sig})
# gpgme
source+=("https://www.gnupg.org/ftp/gcrypt/gpgme/gpgme-${_gpgmever}.tar.bz2"{,.sig})
# libarchive
source+=("https://github.com/libarchive/libarchive/releases/download/v${_libarchive_ver}/libarchive-${_libarchive_ver}.tar.xz"{,.asc})
validpgpkeys+=('A5A45B12AD92D964B89EEE2DEC560C81CEC2276E') # Martin Matuska <mm@FreeBSD.org>

sha512sums=('d17b9aea9f8d51a5a02fc9faa8e36227c0edea73957cc8a8174a23a81ca42737ecfce630aa86008ab26daec584004b772cd2eb3527aeef9e098b445edaa21f6f'
            'SKIP'
            'fcf3573bcc421705190c7cf0e3230f6f3028b669cb2976d29cfeb73e706deaae91ce60d0a615472e3f296454049ea5798f1e8defdd260a98895e94fea6a7a16b'
            '1276ec0799916019f8c0af6b55a139701bd15e0ca4a00811d07963893978bc96c107b980f0fd49f81aa70bc8b3b8cd671195ba357c390772d4c2c5643c50c5a5'
            'SKIP'
            'e3084f0fa083f7f93eac923edbfdddb5fd0a372b94673ba9d4427a2b95508898c15ecdf63b99a1c1f6cf3215e27b06cbaa2b7073df038d43b362e586f92495d3'
            'SKIP'
            'ba0ef99b321546c13385966e4a607734df38b96f6ed45c4c67063a5f8d1482986855279797a6920d9f86c2ec31ce3e104dcc62c37328caacdd78aec59aa66156'
            'SKIP'
            '3857c298663728a465b5f95a3ef44547efbfb420d755e9dde7f20aa3905171b400e1c126d8db5c2b916c733bbd0724d8753cad16c9baf7b12dcd225a3ee04a97'
            '73fd3fff4adeccd4894084c15ddac89890cd10ef105dd5e1835e1e9bbb6a49ff229713bd197d203edfa17c2727700fce65a2a235f07568212d820dca88b528ae'
            'SKIP'
            '7443674247deda2935220fbc4dfc7665e5bb5a260be8ad858c8bd7d7b9f0f868f04ea45e62eb17c0a5e6a2de7c7500ad2d201e2d668c48ca29bd9eea5a73a3ce'
            'SKIP'
            '083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3'
            'SKIP'
            'bf8183dcb42ac306c120836fdd03a13f3f41de72f697a928a7795008acc86e2533ce42f6b554bde7f1ca834f1a0282f8371585b9129ea88441f3f8dd49f1e923'
            'SKIP'
            'a0eef310b9d44532d1ae6e7266226ea3e82d908aa31f775a026e56a7f8303b78adfdceb3ae5a40f7d242987635e764c539a024ce8dc0d66590e1a3fa50f6b784'
            'SKIP'
            '70117f77aa43bbbe0ed28da5ef23834c026780a74076a92ec775e30f851badb423e9a2cb9e8d142c94e4f6f8a794988c1b788fd4bd2271e562071adf0ab16403'
            'SKIP'
            '69487be69612e9bf0221ff56ae687248bd13635db1b7087130e93c1670e38f3c810bbca17723555c04fe207976c35871bbc3da005179ce099504321cf33636e4'
            'SKIP'
            'ac7c47f9ddfe5d4d5db6ca9c1bcba788af95662bf0e54ca5426fe66cd8262896e12acc426eecdf0e0d6681c180bcd37f4c4469619273607e95399c7f49b61c7c'
            'SKIP')
b2sums=('907c39bb368beea037dcb4b32c56b04a86580123d23ddfe5a1d30ed53143a9b6204044d74040e5bcfe80061673d59597ad2e033525561d6b195a95a104203fa9'
        'SKIP'
        '85fe1259b791ff7cda163265f553e0aac8a10ef6674cf6152d5bc7747c7f4f3bc6e9d9c0472534dd7185f093936efed1b4632da64d426b6a7ac432657e8579a1'
        'c03a572726c6bbb24a3e4773673d0c87f4833bb9582aed57a424eea8c965beb6e232f502b61922b124d37403d91ebfefe0db7373673fc22e0d752c4e5036eb07'
        'SKIP'
        '662eb940d5b3da8e040c6ff09d5ac5175c7d37fc839a547d30a092ab356dd4fbb0cd7a5e808798268f0dd6a7f769496066b71dea2d153e0689cacc8b7e7ede5a'
        'SKIP'
        '163262933df11afdb7b0c58fbbf0454b05e02951d28ed24e2c530affa18dee884d86555f7314506852ebfcc092bb509b6f9cd33893e30dab67bfb6f5713946eb'
        'SKIP'
        'e2ff99e8236487f43171c771d0ee89137b73f3d0b2756bcb0d6525c810ffa9f5a3763c3744327fb47cef21eabfc50fff96632f4bbe2cd244206a99daffa0c25a'
        '6bfc4bca5dcadba8a0d4121a2b3ed0bfe440c261003521862c8e6381f1a6f0a72d3fc037351d30afd7ef321e8e8d2ec817c046ac749f2ca0c97fbdc2f7e840b7'
        'SKIP'
        'aded57324e129572c41646b3cc3b0b59a459452d9338d9245663b63dac2a463fb1f1b2b1d2d4ad3c09cb71fb8439df52cd94f24db99e782fc899b94a288a3043'
        'SKIP'
        '22ab3acd84f4db8c3d6f59340c252faedfd4447cea00dafbd652e65b6cf8a20adf6835c22e58563004cfafdb15348c924996230b4b23cae42da5e25eeac4bdad'
        'SKIP'
        '513e4526a92bcb59416b3457d186a30e554f9e0cf21d7114eb3e9fbcbd9d662c8d95cf0b06237f6fe3f756862c63de0aa146d6a23cb4111c16e6459608d115f1'
        'SKIP'
        'dc101769510bc9edff38048216a961df8b08373a0b6d04b13c882bbcb43c4d0e05ecfdfd7788c89b5799082f4d15386efac5eb1762a48ae1ab70b554d0bfbb36'
        'SKIP'
        '24952e97c757b97c387ab4c2c4bf7b040f2874e9326c129805c7f5326fa14d80e083b0842e336a635531a2c8d4a66d428c816bae6b175f1c4518add1ffa3554d'
        'SKIP'
        'da55e695b148e949a1c0770d0298d7a8c9f87d7a1f9e45d380f8c13c472bd44cb4266adb9a113e2b1dcc2596291744f48fdf998ff2de876059d89d184dc87f3a'
        'SKIP'
        '161ac11115a80c21233e4dbe52f92201fa3372e5750cff38b3f49d60f2440b560c4c9a55dfca8f6313750eb2b65a6b0a8427619c382085bcc24cdfe45f6d6233'
        'SKIP')

export LDFLAGS="$LDFLAGS -static"
export CC=musl-gcc
export CXX=musl-gcc

# keep using xz-compressed packages, because one use of the package is to
# recover on systems with broken zstd support in libarchive
[[ $PKGEXT = .pkg.tar.zst ]] && PKGEXT=.pkg.tar.xz

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
    cd "${srcdir}"/xz-${_xzver}
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
                    --disable-{bsdtar,bsdcat,bsdcpio} \
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
                --disable-{dict,gopher,imap,imaps,ldap,ldaps,manual,pop3,pop3s,rtsp,scp,sftp,smb,smbs,smtp,smtps,telnet,tftp} \
                --without-{brotli,libidn2,librtmp,libssh2} \
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
    mkdir -p "${srcdir}"/pacman-${pkgver}/builddir
    cd "${srcdir}"/pacman-${pkgver}/builddir
    meson setup \
        --prefix=/usr \
        --includedir=lib/pacman/include \
        --libdir=lib/pacman/lib \
        --buildtype=plain \
        -Dbuildstatic=true \
        -Ddefault_library=static \
        -Ddoc=disabled \
        -Dldconfig=/usr/bin/ldconfig \
        -Dscriptlet-shell=/usr/bin/bash \
        ..
    ninja
}

package() {
    cd "${srcdir}"/pacman-${pkgver}/builddir
    DESTDIR="${pkgdir}" ninja install

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
