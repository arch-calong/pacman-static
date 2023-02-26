# Maintainer: Stefano Capitani <stefano@manjaro.org>
# Maintainer: Mark Wagie <mark at manjaro dot org>

# Arch credits:
# Maintainer: Eli Schwartz <eschwartz@archlinux.org>

pkgname=pacman-static
pkgver=6.0.2
_cares_ver=1.19.0
_nghttp2_ver=1.52.0
_curlver=7.88.1
_sslver=3.0.8
_zlibver=1.2.13
_xzver=5.4.1
_bzipver=1.0.8
_zstdver=1.5.4
_libarchive_ver=3.6.2
_gpgerrorver=1.46
_libassuanver=2.5.5
_gpgmever=1.18.0
pkgrel=5
pkgdesc="Statically-compiled pacman (to fix or install systems without libc)"
arch=('x86_64' 'aarch64')
url="https://www.archlinux.org/pacman/"
license=('GPL')
depends=('pacman')
makedepends=('meson' 'musl' 'kernel-headers-musl')
options=('!emptydirs' 'lto')

# pacman
#source=("https://sources.archlinux.org/other/pacman/pacman-${pkgver}.tar.xz"{,.sig})
source=("https://sources.archlinux.org/other/pacman/pacman-${pkgver}.tar.xz")
validpgpkeys=('6645B0A8C7005E78DB1D7864F99FFE0FEAE999BD'  # Allan McRae <allan@archlinux.org>
              'B8151B117037781095514CA7BBDFFC92306B1121') # Andrew Gregory (pacman) <andrew@archlinux.org>
# nghttp2
source+=("https://github.com/nghttp2/nghttp2/releases/download/v$_nghttp2_ver/nghttp2-$_nghttp2_ver.tar.xz")
# c-ares
#source+=("https://c-ares.haxx.se/download/c-ares-${_cares_ver}.tar.gz"{,.asc})
source+=("https://c-ares.haxx.se/download/c-ares-${_cares_ver}.tar.gz")
validpgpkeys=('27EDEAF22F3ABCEB50DB9A125CC908FDB71E12C2') # Daniel Stenberg <daniel@haxx.se>
# curl
#source+=("https://curl.haxx.se/download/curl-${_curlver}.tar.gz"{,.asc})
source+=("https://curl.haxx.se/download/curl-${_curlver}.tar.gz")
validpgpkeys=('27EDEAF22F3ABCEB50DB9A125CC908FDB71E12C2') # Daniel Stenberg <daniel@haxx.se>
# openssl
#source+=("https://www.openssl.org/source/openssl-${_sslver}.tar.gz"{,.asc}
source+=("https://www.openssl.org/source/openssl-${_sslver}.tar.gz"
         "ca-dir.patch")
validpgpkeys+=('8657ABB260F056B1E5190839D9C4D26D0E604491'  # Matt Caswell <matt@openssl.org>
               '7953AC1FBC3DC8B3B292393ED5E9E43F7DF9EE8C' # Richard Levitte <levitte@openssl.org>
               'A21FAB74B0088AA361152586B8EF1A6BA9DA2D5C') # Tomáš Mráz <tm@t8m.info>
# zlib
#source+=("https://zlib.net/zlib-${_zlibver}.tar.gz"{,.asc})
source+=("https://zlib.net/zlib-${_zlibver}.tar.gz")
validpgpkeys+=('5ED46A6721D365587791E2AA783FCD8E58BCAFBA') # Mark Adler <madler@alumni.caltech.edu>
# xz
source+=("https://tukaani.org/xz/xz-${_xzver}.tar.gz"{,.sig})
validpgpkeys=('3690C240CE51B4670D30AD1C38EE757D69184620') # Lasse Collin <lasse.collin@tukaani.org>
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
            '3af1ce13270f7afc8652bd3de71200d9632204617fe04d2be7156d60eeb1a5cc415573677791a399ae03577e8e3256939b1b05d27dbd98dee504d09ec5325d56'
            'a7f5988bef393afec08a225be92f6eee54a3e67170fb26cbe00dcc5c5a457b27037bbcfeccc39fb855ed72f100196958d6cbbe251bf1ccfbdd353be18f098359'
            '67701d458548712bbfaa55f2ebefbf87cdbba01b7b1200f608b1c3af67e8dd8e243fa89f256446d217d658a5a1242331d8b0168ab600351e74ee0e2511e79dae'
            '8ce10be000d7d4092c8efc5b96b1d2f7da04c1c3a624d3a7923899c6b1de06f369016be957e36e8ab6d4c9102eaeec5d1973295d547f7893a7f11f132ae42b0d'
            'b1873dbb7a49460b007255689102062756972de5cc2d38b12cc9f389b6be412da6797579b1acd3717a8cd2ee118fd9801b94e55f063d4328f050f0876a5eb53c'
            '99f0e843f52290e6950cc328820c0f322a4d934a504f66c7caa76bd0cc17ece4bf0546424fc95135de85a2656fed5115abb835fd8d8a390d60ffaf946c8887ad'
            '5cff8383a68fb88ecbb3770ec48af0ad5582e08de9dccd339e0b685aaa53447e59d6425caa3f63b54a674e5d78c20520876db547d156e6658ad4841660cba85b'
            'SKIP'
            '083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3'
            'SKIP'
            'd4ecbfb43c3d8217dd20043ba1945ec2048c6620246b4f91595436f25dbb7eb7d14fe07e6bc538ad6a5a89209bdfe987245a25d20e5fcf615176bcd35eb26a3b'
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
        'a77ff3e1f901768daf7e681cad06bf3b9ea44876dba76e06c2aaec8637196f27ee7213e3ef52da53b995f68a2a617f64947b4392f57140310bdc5a1d994ad1b2'
        'd77be535dfa852bf3d91258ddf06b3c63a40123883adb83a4e5652d4b1b16801ddefefad70d83a7d6d9aa81c9c81956fef42bc778d7380d6b398ccfc9f8b82dc'
        '4f4b6dbcddc404854011ec62939696c8b7cb68feb8dfbb053cd9d7773620cadef23e4518ab9e66bb56ae2b12b15a0c40a3e15993f4452fb0c82321d74ba85a27'
        'e163cc9b8b458f72405a2f1bde3811c8d0eb22e8b08ff5608ec64799975f1546dcdce31466b8a1d5ed29bc90d19aa6017d711987c81b71f4b20e279828cf753a'
        '928c0cb15cca44bb7f194db9f95985f6c50aacd3e22fe2eb60ece26ed76469289f10d303c645a48407f3d6435ac66f25dd3c4cbc56fdc5dfd9ea2566feda9ff8'
        '73cd65f287d662a988287205b74e93d516d6a74e18555d0f1a2777557e73e81249b45341c687fe97e65406a7210f77b8914ed146bac517d3fcc4c9fcb16546d3'
        'f4dc8698fb97002aa0548107b448ab0dd8659cce506a83775930f95fd775601f7de1df44866310ac617853410a1915cd4e90ad4088b2fd56418e67b6f0fc4e98'
        'SKIP'
        '22ab3acd84f4db8c3d6f59340c252faedfd4447cea00dafbd652e65b6cf8a20adf6835c22e58563004cfafdb15348c924996230b4b23cae42da5e25eeac4bdad'
        'SKIP'
        '8caea5dae06928076c2e54b059a501bd757663bae5948cb49ae32a7591c11636b22cb3b45d4f91653da800e1815cf5b28f72c69f4696ada4fdc746a272239da9'
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
