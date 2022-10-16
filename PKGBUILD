# Maintainer: Stefano Capitani <stefano@manjaro.org>
# Maintainer: Mark Wagie <mark at manjaro dot org>

# Arch credits:
# Maintainer: Eli Schwartz <eschwartz@archlinux.org>

pkgname=pacman-static
pkgver=6.0.2
_cares_ver=1.18.1
_nghttp2_ver=1.50.0
_curlver=7.85.0
_sslver=1.1.1q
_zlibver=1.2.13
_xzver=5.2.7
_bzipver=1.0.8
_zstdver=1.5.2
_libarchive_ver=3.6.1
_gpgerrorver=1.46
_libassuanver=2.5.5
_gpgmever=1.18.0
pkgrel=1
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
validpgpkeys+=('A5A45B12AD92D964B89EEE2DEC560C81CEC2276E') # Martin Matuska <mm@FreeBSD.org>

sha512sums=('9d76fb58c3a50e89a4b92b1f9e3bfdecca3f69e05022ea88fbd34f9df540c4fc688ad4f8b27e77eedb791aa682c27037abe65c789c6d9ee393bae5b620c3df13'
            'SKIP'
            'c2f7f14972cb268a85966f2bd26ac515fa61d9cf6b6bcaa5cffc04f02a18abf116b15537eb4dfbdfa79e7b1472de7034dfdbce7a082cc5b23627d87e2939e529'
            '1276ec0799916019f8c0af6b55a139701bd15e0ca4a00811d07963893978bc96c107b980f0fd49f81aa70bc8b3b8cd671195ba357c390772d4c2c5643c50c5a5'
            'SKIP'
            'bbad693bcde9c55e5942499950d76011f53ad43d3270eee2c8db486bcf46f5fc92b32dd8752caf4c5976fe493d083e2d34fa299cb96fb8e76d8f5fcc2cc56a36'
            'SKIP'
            'cb9f184ec4974a3423ef59c8ec86b6bf523d5b887da2087ae58c217249da3246896fdd6966ee9c13aea9e6306783365239197e9f742c508a0e35e5744e3e085f'
            'SKIP'
            '3857c298663728a465b5f95a3ef44547efbfb420d755e9dde7f20aa3905171b400e1c126d8db5c2b916c733bbd0724d8753cad16c9baf7b12dcd225a3ee04a97'
            '99f0e843f52290e6950cc328820c0f322a4d934a504f66c7caa76bd0cc17ece4bf0546424fc95135de85a2656fed5115abb835fd8d8a390d60ffaf946c8887ad'
            'SKIP'
            '06329fdbd1d897aa99dc96900c6246457288c586d02bb4869a92dd2f97973f95acb3a2fa9598a20613ea029f816836a8e3b65e36fec2b807b5e7553141429ab9'
            'SKIP'
            '083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3'
            'SKIP'
            'bf8183dcb42ac306c120836fdd03a13f3f41de72f697a928a7795008acc86e2533ce42f6b554bde7f1ca834f1a0282f8371585b9129ea88441f3f8dd49f1e923'
            'SKIP'
            'b06223bb2b0f67d3db5d0d9ab116361a0eda175d4667352b5c0941408d37f2b0ba8e507297e480ccebb88cbba9d0a133820b896914b07d264fb3edaac7b8c99d'
            'SKIP'
            '70117f77aa43bbbe0ed28da5ef23834c026780a74076a92ec775e30f851badb423e9a2cb9e8d142c94e4f6f8a794988c1b788fd4bd2271e562071adf0ab16403'
            'SKIP'
            'c0cb0b337d017793a15dd477a7f5eaef24587fcda3d67676bf746bb342398d04792c51abe3c26ae496e799c769ce667d4196d91d86e8a690d02c6718c8f6b4ac'
            'SKIP'
            '2e5a72edc468080c0e8f29e07d9c33826ffb246fa040ec42399bedeecf698b7555f69ffd15057ad79c0f50cd4926d43174599d99632b1b99ec6cd159c43a70b8'
            'SKIP')
b2sums=('648f62307e413cb352ed92e92df1ace510c1fc5e9ddd254baeef071e89cb7dae1786a95d29c5f69e8b03b1a8cfe3cd65671588dc362c8d3b281c092393aad54c'
        'SKIP'
        'ae5d89a1f7287a3f2f2b9380ff5e9efb7f0646950d15ed281f268dafc65eb34ad7e34610333b4c98db8a657034ea462e7f1eda80ff2e94a918751dbb112c9a2a'
        'c03a572726c6bbb24a3e4773673d0c87f4833bb9582aed57a424eea8c965beb6e232f502b61922b124d37403d91ebfefe0db7373673fc22e0d752c4e5036eb07'
        'SKIP'
        'aa131db640c112cb4a4468ea50f389447fc25a469e70661ec356f4c4bc304629cb4f03cd85809a95e64621e9c754a8c933489b63df9c472ef1298a67fbe9f809'
        'SKIP'
        'fc8fd6a62dc291d0bda328a051e253175fb04442cc4b8f45d67c3a5027748a0fc5fb372d0483bc9024ae0bff119c4fac8f1e982a182612427696d6d09f5935f5'
        'SKIP'
        'e2ff99e8236487f43171c771d0ee89137b73f3d0b2756bcb0d6525c810ffa9f5a3763c3744327fb47cef21eabfc50fff96632f4bbe2cd244206a99daffa0c25a'
        '73cd65f287d662a988287205b74e93d516d6a74e18555d0f1a2777557e73e81249b45341c687fe97e65406a7210f77b8914ed146bac517d3fcc4c9fcb16546d3'
        'SKIP'
        '5363c5d0403e041c6d2e35b5d3321feeb8e63b8556496373c820975850b50e28e0da903446a49ba516fd9f40e0101dd39cfa9a9b8dd143c9849c84a715bb5d7b'
        'SKIP'
        '22ab3acd84f4db8c3d6f59340c252faedfd4447cea00dafbd652e65b6cf8a20adf6835c22e58563004cfafdb15348c924996230b4b23cae42da5e25eeac4bdad'
        'SKIP'
        '513e4526a92bcb59416b3457d186a30e554f9e0cf21d7114eb3e9fbcbd9d662c8d95cf0b06237f6fe3f756862c63de0aa146d6a23cb4111c16e6459608d115f1'
        'SKIP'
        '6748c463256b7d0a05fe89a63c5f3abda1975d861c35821248664f2f09cd2273ef619d12408b6107a99519939ca7214f492e705c29f52f7bbdc422237281c1ca'
        'SKIP'
        '24952e97c757b97c387ab4c2c4bf7b040f2874e9326c129805c7f5326fa14d80e083b0842e336a635531a2c8d4a66d428c816bae6b175f1c4518add1ffa3554d'
        'SKIP'
        'a071b839eb75455378514f003920cd387320e9fae416e71151cf6ac1b4a058b58ed054450b79e3eeaf820ff5324ea14efa003612867477b7379a776942d62be6'
        'SKIP'
        'e7b79e97545dabeac164069e87adbd2081d3bd75c22f80b3797c6e487a477b3f6347b6fc14c76668eb69f2f2e5dcdd5a33a694e0a292ce426b8d0d93435218cf'
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
