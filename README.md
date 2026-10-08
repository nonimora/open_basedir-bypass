# open_basedir-bypass
PHP 5.2.6 - open_basedir / safe_mode bypass via putenv()
## Description
Historical vulnerability in PHP 5.2.6 (Bug #46741). The interaction between putenv() and mail() allowed environment variable injection leading to open_basedir bypass.

## Root Cause
mail() was using sendmail without clearing LD_PRELOAD.

## Impact
Bypass of open_basedir and disabled functions in old PHP versions.

## Status
Fixed since PHP 5.3.3. For educational purposes only.

## Reference
- bugs.php.net/bug.php?id=46741
- CVE: None (marked as Not a bug at the time)

## My Learning
I studied this bug to understand how LD_PRELOAD injection works and why sanitizing environment variables is important.
