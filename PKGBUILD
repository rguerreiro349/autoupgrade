#
# Contribuidor: {{ nome_do_autor(); }}
#

pkgname=autoupgrade
pkgver=1.0.0
pkgrel=1
pkgdesc='Instantâneo automático e, em seguida, atualize o sistema. (Quando o sistema falhar, faça o procedimento de `sudo timeshift --restore` e remova este plug até que a falha seja resolvida.).'
arch=('any')
url='http://localhost/autoupgrade'
license=('cIO')
install="$pkgname.install"
source=("$pkgname.service" "$pkgname.timer")
md5sums=('SKIP'
    'SKIP')
depends=('timeshift-autosnap')

package()
{
    install -Dm644 "$pkgname.service" "$pkgdir/usr/lib/systemd/system/autoupgrade.service"
    install -Dm644 "$pkgname.timer" "$pkgdir/usr/lib/systemd/system/autoupgrade.timer"
}
