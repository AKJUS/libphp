# Lambda Shared Libraries Documentation

This directory contains documentation of shared libraries available in different Lambda runtime environments.

## Files

- `node-20.md` - Shared libraries in Node.js 20 Lambda runtime
- `node-22.md` - Shared libraries in Node.js 22 Lambda runtime
- `node-24.md` - Shared libraries in Node.js 24 Lambda runtime

## How to Generate Library Lists

### Method 1: Using Shell Script via Lambda Endpoint (Easiest)

Execute the shell script directly via the appropriate Node.js runtime endpoint:

**For Node.js 20:**
```bash
curl -s "https://php-node20.vercel.app/exec?cmd=bash%20-c%20'for%20p%20in%20/var/lang/lib%20/lib64%20/usr/lib64%20/var/runtime/lib%20/opt/lib;%20do%20if%20[%20-d%20\"\$p\"%20];%20then%20echo%20\"===%20\$p%20===\";%20find%20\"\$p\"%20-name%20\"*.so*\"%20-type%20f%202>/dev/null%20|%20sort%20|%20while%20read%20f;%20do%20echo%20\"\$(basename%20\$f)%20(\$(du%20-h%20\$f%20|%20cut%20-f1))\";%20done;%20fi;%20done'"
```

**For Node.js 22:**
```bash
curl -s "https://php-node22.vercel.app/exec?cmd=bash%20-c%20'for%20p%20in%20/var/lang/lib%20/lib64%20/usr/lib64%20/var/runtime/lib%20/opt/lib;%20do%20if%20[%20-d%20\"\$p\"%20];%20then%20echo%20\"===%20\$p%20===\";%20find%20\"\$p\"%20-name%20\"*.so*\"%20-type%20f%202>/dev/null%20|%20sort%20|%20while%20read%20f;%20do%20echo%20\"\$(basename%20\$f)%20(\$(du%20-h%20\$f%20|%20cut%20-f1))\";%20done;%20fi;%20done'"
```

**For Node.js 24:**
```bash
curl -s "https://php-node24.vercel.app/exec?cmd=bash%20-c%20'for%20p%20in%20/var/lang/lib%20/lib64%20/usr/lib64%20/var/runtime/lib%20/opt/lib;%20do%20if%20[%20-d%20\"\$p\"%20];%20then%20echo%20\"===%20\$p%20===\";%20find%20\"\$p\"%20-name%20\"*.so*\"%20-type%20f%202>/dev/null%20|%20sort%20|%20while%20read%20f;%20do%20echo%20\"\$(basename%20\$f)%20(\$(du%20-h%20\$f%20|%20cut%20-f1))\";%20done;%20fi;%20done'"
```

### Method 2: Using PHP Script (JSON Output)

If you need JSON output, you can create a simple PHP script and execute it via the endpoint. However, the shell commands (Method 1 and 3) are recommended as they're simpler.

### Method 3: Simple find command

For a quick list of library files, use the appropriate endpoint:

**Node.js 20:**
```bash
curl -s "https://php-node20.vercel.app/exec?cmd=for%20p%20in%20/var/lang/lib%20/lib64%20/usr/lib64%20/var/runtime/lib%20/opt/lib;%20do%20echo%20\"===%20\$p%20===\";%20find%20\$p%20-name%20\"*.so*\"%20-type%20f%202>/dev/null%20|%20sort;%20done"
```

**Node.js 22:**
```bash
curl -s "https://php-node22.vercel.app/exec?cmd=for%20p%20in%20/var/lang/lib%20/lib64%20/usr/lib64%20/var/runtime/lib%20/opt/lib;%20do%20echo%20\"===%20\$p%20===\";%20find%20\$p%20-name%20\"*.so*\"%20-type%20f%202>/dev/null%20|%20sort;%20done"
```

**Node.js 24:**
```bash
curl -s "https://php-node24.vercel.app/exec?cmd=for%20p%20in%20/var/lang/lib%20/lib64%20/usr/lib64%20/var/runtime/lib%20/opt/lib;%20do%20echo%20\"===%20\$p%20===\";%20find%20\$p%20-name%20\"*.so*\"%20-type%20f%202>/dev/null%20|%20sort;%20done"
```

## Formatting the Results

When you get the JSON output, format it into the markdown file like this:

```markdown
### /var/lang/lib

- libcrypto.so.3 (20.8 MB)
- libssl.so.3 (5.6 MB)
- ...

### /lib64

- libc.so.6
- libm.so.6
- ...
```

## Usage

When analyzing which libraries to include in a package:

1. Check the appropriate runtime documentation (node-20.md, node-22.md, or node-24.md)
2. Compare libraries in your package's `native/lib` with the list
3. Remove libraries that already exist in Lambda
4. Keep libraries that are not in the list or have version conflicts

## Runtime Endpoints

- **Node.js 20**: https://php-node20.vercel.app/
- **Node.js 22**: https://php-node22.vercel.app/
- **Node.js 24**: https://php-node24.vercel.app/

## Notes

- Libraries in `/var/task/lib` are application-specific and should not be documented here
- Only document libraries provided by the Lambda runtime itself
- Update these files when Lambda runtime versions change
