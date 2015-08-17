# Contributor: John D Jones III <j[nospace]n[nospace]b[nospace]e[nospace]k[nospace]1972 -_AT_- the domain name google offers a mail service at ending in dot com>
# Generator  : CPANPLUS::Dist::Arch 1.25

pkgname='perl-opengl-image'
pkgver='1.03'
pkgrel='42'
pkgdesc="v1.03 copyright 2007 Graphcomp - ALL RIGHTS RESERVED"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl-opengl')
makedepends=()
url='http://search.cpan.org/dist/OpenGL-Image'
source=('http://search.cpan.org/CPAN/authors/id/B/BF/BFREE/OpenGL-Image-1.03.tar.gz')
md5sums=('c68c25103fd19c752e5e9c97f0aecac0')
sha512sums=('01593098e83a1c1a4509c81865e363ab6bb1744418253e28212a3cd701c2bf9ae8898463d3b54f05585c4dc8da9c0fd6d1e6a9101154f051e1284846044fffdc')
_distdir="OpenGL-Image-1.03"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir/$_distdir"
  make install

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
