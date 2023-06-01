# Maintainer: Stefano Capitani <stefano@manjaro.org>
# Maintainer: Mark Wagie <mark at manjaro dot org>

# Arch credits:
# Maintainer: Eli Schwartz <eschwartz@archlinux.org>

pkgname=pacman-static
pkgver=6.0.2
_cares_ver=1.19.1
_nghttp2_ver=1.53.0
_curlver=8.1.1
_sslver=3.0.8
_zlibver=1.2.13
_xzver=5.4.3
_bzipver=1.0.8
_zstdver=1.5.5
_libarchive_ver=3.6.2
_gpgerrorver=1.47
_libassuanver=2.5.5
_gpgmever=1.20.0
pkgrel=6
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
validpgpkeys=('3690C240CE51B4670D30AD1C38EE757D69184620'  # Lasse Collin <lasse.collin@tukaani.org>
              '22D465F2B4C173803B20C6DE59FCF207FEA7F445') # Jia Tan <jiat0218@gmail.com>
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
            'ae3c7b12fc019fa139e94c16f69070734d9c600c1ebefad46758cd7f9a93d39f1d72fa2a9bce10e757141749436858316752157d9957e6aaa455764e2f667a4e'
            '466a94efda626e815a6ef7a890637056339f883d549ea6055e289fd8cd2391130e5682c905c0fb3bd7e955af7f6deb793562c170eb0ee066a4a62085a82ba470'
            '95aeaca94ec78284102d1f5f8d0e24d7a084f2431356a08e7f6baf79c13c56040f2600571877d74e45b53b9f61ef493d201ed85808233c24b4dcbf45cdb6e762'
            '8ce10be000d7d4092c8efc5b96b1d2f7da04c1c3a624d3a7923899c6b1de06f369016be957e36e8ab6d4c9102eaeec5d1973295d547f7893a7f11f132ae42b0d'
            'b1873dbb7a49460b007255689102062756972de5cc2d38b12cc9f389b6be412da6797579b1acd3717a8cd2ee118fd9801b94e55f063d4328f050f0876a5eb53c'
            '99f0e843f52290e6950cc328820c0f322a4d934a504f66c7caa76bd0cc17ece4bf0546424fc95135de85a2656fed5115abb835fd8d8a390d60ffaf946c8887ad'
            'aff0fe166af6df4491a6f5df2372cab100b081452461a0e8c6fd65b72af3f250f16c64d9fb8fd309141e9b9ae4e41649f48687cc29e63dd82f27f2eab19b4023'
            'SKIP'
            '083f5e675d73f3233c7930ebe20425a533feedeaaa9d8cc86831312a6581cefbe6ed0d08d2fa89be81082f2a5abdabca8b3c080bf97218a1bd59dc118a30b9f3'
            'SKIP'
            'c2d88b2c2050262f85be32877142c94e36a8ee451890f579cd2426c7de565fb22d21c369bad11f306093f0b356e935cef5a8ff5a2b0c007ade0f7e7eb944d2a5'
            'SKIP'
            'bbb4b15dae75856ee5b1253568674b56ad155524ae29a075cb5b0a7e74c4af685131775c3ea2226fff2f84ef80855e77aa661645d002b490a795c7ae57b66a30'
            'SKIP'
            '70117f77aa43bbbe0ed28da5ef23834c026780a74076a92ec775e30f851badb423e9a2cb9e8d142c94e4f6f8a794988c1b788fd4bd2271e562071adf0ab16403'
            'SKIP'
            '82dfd272edd4adab09e8428bf809c13eeb50a4a7d2397c41d29ffa3832c4f46054ad75eb053fbcc876ebbf78bb8bcf71d95bc9dad68f4b326492ea513dd5b606'
            'SKIP'
            'a12bb6839e13a0be1099f42c650fc90fbfe62d32ce38bcbb4794206d29b2c782ae1115124d0e5f6b9716514213af32b05e4a42eb196447674a5f9a2a32bee043'
            'SKIP'
            'b250feccb089e708553584f34bcb3d0cc3030a1332a11fa2a1dcc2b3b0c5017483b02604317673244dfb8a954d7d1400fb5a5391e9f66e3f2c2260771e5d0857')
b2sums=('648f62307e413cb352ed92e92df1ace510c1fc5e9ddd254baeef071e89cb7dae1786a95d29c5f69e8b03b1a8cfe3cd65671588dc362c8d3b281c092393aad54c'
        '580aabc6726827b3905d2807158de55861b07604809fdd78703386ffa0dd40307b14488ef126e9e805634ef6ed267716ec2f28ecaf33823e6b548d68f53fdbbc'
        '4b6c9593edb1a91ab76d54ddacb1cd5d67006d5e628ea1f3289f54e9360be32abeb5d8fc7d23e193feab3e7928e8efde82757eb12fe217dc92ed0d9132bedf5d'
        'bf85691d08dc0c8235ce589b21176903d00b67c6512dd4069ab22368640e318b702d3f71bcefcd304ff4e47cda5fa8a8aba49783b27a928113c81c8c02de08ae'
        'e163cc9b8b458f72405a2f1bde3811c8d0eb22e8b08ff5608ec64799975f1546dcdce31466b8a1d5ed29bc90d19aa6017d711987c81b71f4b20e279828cf753a'
        '928c0cb15cca44bb7f194db9f95985f6c50aacd3e22fe2eb60ece26ed76469289f10d303c645a48407f3d6435ac66f25dd3c4cbc56fdc5dfd9ea2566feda9ff8'
        '73cd65f287d662a988287205b74e93d516d6a74e18555d0f1a2777557e73e81249b45341c687fe97e65406a7210f77b8914ed146bac517d3fcc4c9fcb16546d3'
        'c4192a59ca751567ebab17e08e72aa1bf0f5ca14af0b59fded1c4dff02c1b76ab30119a4138932f78f69bd4b7827071c81d6ca1c56be65491466ea061786ed78'
        'SKIP'
        '22ab3acd84f4db8c3d6f59340c252faedfd4447cea00dafbd652e65b6cf8a20adf6835c22e58563004cfafdb15348c924996230b4b23cae42da5e25eeac4bdad'
        'SKIP'
        '2c2dc95f227e661ada23d8f6141bcd293505ce14e605f946ae00d4d4ac37d10b4eb08279ef7560618c67caf266431f76686fda5ae1921d698a6a93bbaf9a0052'
        'SKIP'
        'bc04efa0686b1b7d7cdce045fc080c090c1abec60349b673c2e1ce27900483aea090eb6ebcb3fb49a4eed36f18156a12413d5446f739475632f4ed2a2481ff27'
        'SKIP'
        '24952e97c757b97c387ab4c2c4bf7b040f2874e9326c129805c7f5326fa14d80e083b0842e336a635531a2c8d4a66d428c816bae6b175f1c4518add1ffa3554d'
        'SKIP'
        '1dce0f32a29ece87f9e0f5c9da394fe3e3b651344889f36e7c403a8336e53f831425384cc43b5aeebc96da50b5ac139a8f5b07dad85e341dcbc4b47b35c8e77a'
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

# to enable func64 interface in musl for 64-bit file system functions
export CFLAGS+=' -D_LARGEFILE64_SOURCE'
export CXXFLAGS+=' -D_LARGEFILE64_SOURCE'

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

    # libassuan needs ARFLAGS specified or a warning from -u kills the build
    cd "${srcdir}"/libassuan-${_libassuanver}
    AR_FLAGS=cr ARFLAGS=cr ./configure --prefix="${srcdir}"/temp/usr \
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
