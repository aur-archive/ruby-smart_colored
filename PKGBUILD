# Maintainer: foalsrock <foalsrock at gmail dot com>

_gemname=smart_colored
pkgname=ruby-${_gemname}
pkgver=1.1.1
pkgrel=1
pkgdesc="Ruby gem for color and formatting in terminal."
arch=(any)
url="https://github.com/toy/smart_colored"
license=('custom')
depends=('ruby')
makedepends=('ruby')
source=(http://rubygems.org/downloads/${_gemname}-${pkgver}.gem)
noextract=(${_gemname}-${pkgver}.gem)
md5sums=('de49f0588da655f4d430d3104d381f76')

package() {
  cd "${srcdir}"
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"

  gem install --ignore-dependencies --no-user-install -i "${pkgdir}${_gemdir}" \
    ${_gemname}-${pkgver}.gem
}
