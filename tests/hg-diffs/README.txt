Diffs should be exported in the same way that the ShipItRepo does - for example:

$ hhvm -m debug
Welcome to HipHop Debugger!
Type "help" or "?" for a complete list of commands.

hphpd> require_once('./autoload.php')
hphpd> $repo = Facebook\ShipIt\ShipItRepo::open('/tmp/hg-test', 'master')
hphpd> $patch = $repo->getNativePatchFromID('f77188bb2a4f0ef67edbcb6ffc2443b680592f30')
hphpd> file_put_contents('tests/hg-diffs/submodule-hhvm-third-party.diff', $patch)
