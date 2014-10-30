pdo_oci
=======

The original version of PDO_OCI <http://php.net/manual/ja/ref.pdo-oci.php> 
is still experimental state since 2005. Forgotten? 
This repository provides patched version of PDO_OCI which runs on php-5.6.
(This Repository is under construction):

* Fixed config.m4 for 64bit version.
* Character string will be truncated 
  in case ORACLE's encoding is SJIS and client side is UTF-8.
* Character string can be truncated 
  in case ORACLE's SJIS data includes HANKAKU-KANA.
* Fixed config.m4 for OIC(Oracle Instant Client) 12.1.
* Fixed pdo_oci.c for changing "function_entry" type name.

PDO_OCI の元のバージョン <http://php.net/manual/ja/ref.pdo-oci.php> 
は 2005 年から experimental のままで放置されているので救済するものです。
以下のパッチを当てています（注：まだリポジトリ作成途中です）。

* config.m4 を 64bit でも通るようにした。
* ORACLE 側のエンコーディングが SJIS でクライアント側が UTF-8 の場合、
  文字列が途中で切れてしまうことがあるのに対応。
* ORACLE 側の SJIS データに半角カナが含まれている場合、
  文字列が途中で切れてしまうことがあるのに対応。
* config.m4 を OIC 12.1 でも通るようにした。
* function_entry が zend_function_entry に変わったのに対応。
