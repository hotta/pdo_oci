pdo_oci
=======

pdo_oci runs on php-5.6

Original version <http://php.net/manual/ja/ref.pdo-oci.php> has been experimental 
state since 2005. Forgotten? So I applied patches as following:
* Fixed config.m4 to fit 64bit version.
* Character string will be truncated in case ORACLE's encoding is SJIS and client side is UTF-8.
* Character string can be truncated in case ORACLE's SJIS data includes HANKAKU-KANA.

元のバージョンは <http://php.net/manual/ja/ref.pdo-oci.php> は 2005 年から 
experimental のままで放置されているので救済するものです。以下のパッチを
当てています。
* config.m4 を 64bit でも通るようにした。
* ORACLE 側のエンコーディングが SJIS でクライアント側が UTF-8 の場合、文字列が途中で切れてしまうことがあるのに対応。
* ORACLE 側の SJIS データに半角カナが含まれている場合、文字列が途中で切れてしまうことがあるのに対応。
