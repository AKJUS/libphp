# Lambda Node.js 20 Shared Libraries

This document lists all shared libraries (`*.so*`) available in the Lambda Node.js 20 runtime environment.

## Overview

- **Runtime**: Node.js 20
- **Endpoint**: https://php-node20.vercel.app/
- **Last Updated**: 2026-01-13
- **Total Libraries**: ~380+ (varies by path)

## Library Paths

Lambda `LD_LIBRARY_PATH` includes:
- `/var/task/lib` - Application-provided libraries
- `/var/lang/lib` - Lambda runtime libraries
- `/lib64` - System libraries
- `/usr/lib64` - System libraries
- `/var/runtime/lib` - Runtime libraries
- `/opt/lib` - Optional libraries

## Libraries by Path

### /var/lang/lib

- libcrypto.so
- libcrypto.so.3
- libssl.so
- libssl.so.3

### /lib64

- ld-linux-x86-64.so.2
- libacl.so.1
- libacl.so.1.1.2301
- libanl.so.1
- libarchive.so.13
- libarchive.so.13.7.4
- libassuan.so.0
- libassuan.so.0.8.5
- libattr.so.1
- libattr.so.1.1.2501
- libaudit.so.1
- libaudit.so.1.0.0
- libauparse.so.0
- libauparse.so.0.0.0
- libblkid.so.1
- libblkid.so.1.1.0
- libBrokenLocale.so.1
- libbz2.so.1
- libbz2.so.1.0.8
- libc_malloc_debug.so.0
- libc.so.6
- libcap-ng.so.0
- libcap-ng.so.0.0.0
- libcap.so.2
- libcap.so.2.73
- libcom_err.so.2
- libcom_err.so.2.1
- libcrypto.so.3
- libcrypto.so.3.2.2
- libcurl.so.4
- libcurl.so.4.8.0
- libdl.so.2
- libdnf.so.2
- libdrop_ambient.so.0
- libdrop_ambient.so.0.0.0
- libffi.so.8
- libffi.so.8.1.2
- libform.so.6
- libform.so.6.2
- libformw.so.6
- libformw.so.6.2
- libgcc_s-14-20250110.so.1
- libgcc_s.so.1
- libgcrypt.so.20
- libgcrypt.so.20.4.2
- libgio-2.0.so.0
- libgio-2.0.so.0.8200.2
- libgirepository-1.0.so.1
- libgirepository-1.0.so.1.0.0
- libgirepository-2.0.so.0
- libgirepository-2.0.so.0.8200.2
- libglib-2.0.so.0
- libglib-2.0.so.0.8200.2
- libgmodule-2.0.so.0
- libgmodule-2.0.so.0.8200.2
- libgmp.so.10
- libgmp.so.10.4.1
- libgobject-2.0.so.0
- libgobject-2.0.so.0.8200.2
- libgpg-error.so.0
- libgpg-error.so.0.32.0
- libgpgme.so.11
- libgpgme.so.11.32.1
- libgssapi_krb5.so.2
- libgssapi_krb5.so.2.2
- libgssrpc.so.4
- libgssrpc.so.4.2
- libgthread-2.0.so.0
- libgthread-2.0.so.0.8200.2
- libhistory.so.8
- libhistory.so.8.1
- libidn2.so.0
- libidn2.so.0.3.7
- libjson-c.so.5
- libjson-c.so.5.0.0
- libk5crypto.so.3
- libk5crypto.so.3.1
- libkdb5.so.10
- libkdb5.so.10.0
- libkeyutils.so.1
- libkeyutils.so.1.10
- libkrad.so.0
- libkrad.so.0.0
- libkrb5.so.3
- libkrb5.so.3.3
- libkrb5support.so.0
- libkrb5support.so.0.1
- liblua-5.3.so
- liblua-5.4.so
- liblz4.so.1
- liblz4.so.1.9.4
- liblzma.so.5
- liblzma.so.5.2.5
- libm.so.6
- libmagic.so.1
- libmagic.so.1.0.0
- libmemusage.so
- libmenu.so.6
- libmenu.so.6.2
- libmenuw.so.6
- libmenuw.so.6.2
- libmodulemd.so.2
- libmodulemd.so.2.13.0
- libmount.so.1
- libmount.so.1.1.0
- libmpfr.so.6
- libmpfr.so.6.1.0
- libmvec.so.1
- libncurses.so.6
- libncurses.so.6.2
- libncursesw.so.6
- libncursesw.so.6.2
- libnghttp2.so.14
- libnghttp2.so.14.26.0
- libnpth.so.0
- libnpth.so.0.1.2
- libnss_compat.so.2
- libnss_dns.so.2
- libnss_files.so.2
- libnssckbi.so
- libp11-kit.so.0
- libp11-kit.so.0.3.0
- libpanel.so.6
- libpanel.so.6.2
- libpanelw.so.6
- libpanelw.so.6.2
- libpcprofile.so
- libpcre2-8.so.0
- libpcre2-8.so.0.11.0
- libpcre2-posix.so.3
- libpcre2-posix.so.3.0.2
- libpeas-1.0.so.0
- libpeas-1.0.so.0.3200.0
- libpopt.so.0
- libpopt.so.0.0.1
- libpsl.so.5
- libpsl.so.5.3.5
- libpsx.so.2
- libpsx.so.2.73
- libpthread.so.0
- libreadline.so.8
- libreadline.so.8.1
- librepo.so.0
- libresolv.so.2
- librpm.so.9
- librpm.so.9.1.3
- librpmio.so.9
- librpmio.so.9.1.3
- librt.so.1
- libSegFault.so
- libselinux.so.1
- libsepol.so.2
- libsigsegv.so.2
- libsigsegv.so.2.0.6
- libsmartcols.so.1
- libsmartcols.so.1.1.0
- libsolv.so.1
- libsolvext.so.1
- libsqlite3.so.0
- libsqlite3.so.0.8.6
- libssl.so.3
- libssl.so.3.2.2
- libstdc++.so.6
- libstdc++.so.6.0.33
- libtasn1.so.6
- libtasn1.so.6.6.3
- libthread_db.so.1
- libtic.so.6
- libtic.so.6.2
- libtinfo.so.6
- libtinfo.so.6.2
- libunistring.so.2
- libunistring.so.2.1.0
- libutil.so.1
- libuuid.so.1
- libuuid.so.1.3.0
- libverto.so.1
- libverto.so.1.0.0
- libxml2.so.2
- libxml2.so.2.10.4
- libyaml-0.so.2
- libyaml-0.so.2.0.9
- libz.so.1
- libz.so.1.2.11
- libzstd.so.1
- libzstd.so.1.5.5
- p11-kit-proxy.so

### /usr/lib64

*(Same libraries as /lib64 - symlinks to the same files)*

### /var/runtime/lib

*(No libraries found in this path)*

### /opt/lib

*(No libraries found in this path)*

## How to Update This Document

1. Execute the shell script via Node.js 20 endpoint:
   ```bash
   curl -s "https://php-node20.vercel.app/exec?cmd=bash%20-c%20'for%20p%20in%20/var/lang/lib%20/lib64%20/usr/lib64%20/var/runtime/lib%20/opt/lib;%20do%20if%20[%20-d%20\"\$p\"%20];%20then%20echo%20\"===%20\$p%20===\";%20find%20\"\$p\"%20-name%20\"*.so*\"%20-type%20f%202>/dev/null%20|%20sort%20|%20while%20read%20f;%20do%20echo%20\"\$(basename%20\$f)%20(\$(du%20-h%20\$f%20|%20cut%20-f1))\";%20done;%20fi;%20done'"
   ```

2. Or use the simple find command:
   ```bash
   curl -s "https://php-node20.vercel.app/exec?cmd=for%20p%20in%20/var/lang/lib%20/lib64%20/usr/lib64%20/var/runtime/lib%20/opt/lib;%20do%20echo%20\"===%20\$p%20===\";%20find%20\$p%20-name%20\"*.so*\"%20-type%20f%202>/dev/null%20|%20sort;%20done"
   ```

3. Copy the output and format it into this markdown file

4. Update the "Last Updated" date in this document after running the commands

## Notes

- Libraries in `/var/task/lib` are application-specific and may vary
- Libraries in other paths are provided by the Lambda runtime
- This list helps identify which libraries can be removed from packages
