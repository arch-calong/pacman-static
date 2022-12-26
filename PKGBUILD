# Maintainer: Stefano Capitani <stefano@manjaro.org>
# Maintainer: Mark Wagie <mark at manjaro dot org>

# Arch credits:
# Maintainer: Eli Schwartz <eschwartz@archlinux.org>

pkgname=pacman-static
pkgver=6.0.2
_cares_ver=1.18.1
_nghttp2_ver=1.51.0
_curlver=7.87.0
_sslver=3.0.7
_zlibver=1.2.13
_xzver=5.4.0
_bzipver=1.0.8
_zstdver=1.5.2
_libarchive_ver=3.6.2
_gpgerrorver=1.46
_libassuanver=2.5.5
_gpgmever=1.18.0
pkgrel=4
pkgdesc="Statically-compiled pacman (to fix or install systems without libc)"
arch=('x86_64' 'aarch64')
url="https://www.archlinux.org/pacman/"
license=('GPL')
depends=('pacman')
makedepends=('meson' 'musl' 'kernel-headers-musl')
options=('!emptydirs' 'lto')

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
               '7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C' # Richard Levitte <levitte@openssl.org>
               'A21FAB74B0088AA361152586B8EF1A6BA9DA2D5C') # Tomáš Mráz <tm@t8m.info>
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
validpgpkeys+=('A5A45B12AD92D964B89EEE2DEC560C81CEC2276E'  # Martin Matuska <mm@FreeBSD.org>
              'DB2C7CF1B4C265FAEF56E3FC5848A18B8F14184B') # Martin Matuska <martin@matuska.org>
# patches
source+=('pacman-sync-first-option.patch')

sha512sums=('9d76fb58c3a50e89a4b92b1f9e3bfdecca3f69e05022ea88fbd34f9df540c4fc688ad4f8b27e77eedb791aa682c27037abe65c789c6d9ee393bae5b620c3df13'
            'SKIP'
            '0212680e57a15f9afca3b5226429edebd2fe8a52117480007d4472cd0c1bd3aa4d9f21269c637a11efd0f2146a3ee16c3c07ab35d9fb3d4566235d3a14268eeb'
            '1276ec0799916019f8c0af6b55a139701bd15e0ca4a00811d07963893978bc96c107b980f0fd49f81aa70bc8b3b8cd671195ba357c390772d4c2c5643c50c5a5'
            'SKIP'
            '939be5a7d82f7ed4e96173639aa50f5e6748b387d3f458f3845c584ad24d15d77b8cd64f4f2dc11bcc207b097d125d1dc713a9769964e3d4766182a217e9898d'
            'SKIP'
            '6c2bcd1cd4b499e074e006150dda906980df505679d8e9d988ae93aa61ee6f8c23c0fa369e2edc1e1a743d7bec133044af11d5ed57633b631ae479feb59e3424'
            'SKIP'
            'b1873dbb7a49460b007255689102062756972de5cc2d38b12cc9f389b6be412da6797579b1acd3717a8cd2ee118fd9801b94e55f063d4328f050f0876a5eb53c'
            '99f0e843f52290e6950cc328820c0f322a4d934a504f66c7caa76bd0cc17ece4bf0546424fc95135de85a2656fed5115abb835fd8d8a390d60ffaf946c8887ad'
            'SKIP'
            '29b2cd25bb5b234b329ffe9547692d2c29be393db9d8d4ce70a66dfdaebd54433e79a89d80c57e58cd4559c3c68b9845507d5fedf3eec1c528a81e3d9ddbd811'
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
            'a12bb6839e13a0be1099f42c650fc90fbfe62d32ce38bcbb4794206d29b2c782ae1115124d0e5f6b9716514213af32b05e4a42eb196447674a5f9a2a32bee043'
            'SKIP'
            'b250feccb089e708553584f34bcb3d0cc3030a1332a11fa2a1dcc2b3b0c5017483b02604317673244dfb8a954d7d1400fb5a5391e9f66e3f2c2260771e5d0857')
b2sums=('648f62307e413cb352ed92e92df1ace510c1fc5e9ddd254baeef071e89cb7dae1786a95d29c5f69e8b03b1a8cfe3cd65671588dc362c8d3b281c092393aad54c'
        'SKIP'
        'ca3c5fb439b60f67ce5447c957397c16c7659432d3a3b25076b88142318675eb2af9f039a86ce88df8af3bd0167d98f14cdeb8dad2d01eda1378015acefa354e'
        'c03a572726c6bbb24a3e4773673d0c87f4833bb9582aed57a424eea8c965beb6e232f502b61922b124d37403d91ebfefe0db7373673fc22e0d752c4e5036eb07'
        'SKIP'
        '8ac9477e0923f31dfe523255663d8965ef07ee8823f787f90fcfbe19de3b6e7904d9b30e36a18913f6948cce0467de9df4a0170b1a11d820ea26fb4f267479af'
        'SKIP'
        '141881071fa62f056c514e7c653a61c59cc45fe951ec094041e23fb5e619133b7ebbfe31cd8203969c9d8842b8cbc10ec58da67cc181761a11c1cfdd0869df9a'
        'SKIP'
        '928c0cb15cca44bb7f194db9f95985f6c50aacd3e22fe2eb60ece26ed76469289f10d303c645a48407f3d6435ac66f25dd3c4cbc56fdc5dfd9ea2566feda9ff8'
        '73cd65f287d662a988287205b74e93d516d6a74e18555d0f1a2777557e73e81249b45341c687fe97e65406a7210f77b8914ed146bac517d3fcc4c9fcb16546d3'
        'SKIP'
        '7bcf2e48470b885ae48b1fd0d46ab504961e7c5b1358d8c57a6fe1ba32311f5ca837740cff7ba77767f0a25ef80ec68c3d43029f87af035131526cb71f961d0f'
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
        '355b5d402e352dee802513485ce7e047af58d6de5b9bf6a49f3fd8d7b94117007598820ac979585c0da79747e8b63b70ab151131182368a11f97a047cf9029d4'
        'SKIP'
        '2e8af5fc87561e3a5349124d32fa52237fe6c1febe4887305ea9202d62e65f03105e6a93175a2e95ec6e229482be80396162c1e19f83d7268b8b76bc862fa6cc')

prepare() {
  cd "${srcdir}/pacman-${pkgver}"
  patch -Np1 -i ../pacman-sync-first-option.patch
}

export LDFLAGS="$LDFLAGS -static"
export CC=musl-gcc
export CXX=musl-gcc

# prevent static lib mangling
export CFLAGS+=" -ffat-lto-objects" 

# keep using xz-compressed packages, because one use of the package is to
# recover on systems with broken zstd support in libarchive
[[ $PKGEXT = .pkg.tar.zst ]] && PKGEXT=.pkg.tar.xz

build() {
    export PKG_CONFIG_PATH="${srcdir}"/temp/usr/lib/pkgconfig
    export PATH="${srcdir}/temp/usr/bin:${PATH}"

    # openssl
    cd "${srcdir}"/openssl-${_sslver}
    patch -Np1 -i "${srcdir}/ca-dir.patch"
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
    sed -i "s/iconv //" "${srcdir}"/temp/usr/lib/pkgconfig/libarchive.pc

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
        -Ddoxygen=disabled \
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
