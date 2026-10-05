<!-- tyhp-readme:start -->
# tyhpdef/psr-log

Tyhp type definitions for `psr/log` `2.0.0`.

```bash
composer require --dev tyhpdef/psr-log:2.0.0
```

This is a metapackage. Composer also installs `tyhpdef/psr-log-impl` (type files).
Require **this** name, not `tyhpdef/psr-log-impl`.

See https://tyhplang.com.

## Maintain `psr/log`? Ship the types yourself

If you are a Packagist maintainer of `psr/log`, you can take over these
types.

Copy `_tyhpdef/` from **`tyhpdef/psr-log-impl`** (Apache-2.0; keep the `NOTICE`).
Then either:

1. **Bundle** the files in `psr/log` and set `extra.tyhp.package` on
   that `composer.json`, plus
   `"replace": { "tyhpdef/psr-log": "self.version" }`, or
2. **Publish a sibling** types package under your vendor, versioned with
   `psr/log` (same `X.Y.Z`). Set `extra.tyhp.package` there,
   `require` `psr/log` with a real constraint,
   `"replace": { "tyhpdef/psr-log": "self.version" }`, and set
   `extra.tyhp.tyhpdef` on `psr/log` to your sibling’s Composer name.

Ship that to Packagist first, then open an issue:

https://github.com/tyhpproject/tyhp-runtime-src/issues/new?template=tyhpdef-ownership.yml

We verify Packagist ownership and that the types parse and cover the PHP
API, then stop publishing community tags for those versions. We do not
transfer the `tyhpdef/psr-log` Packagist name.

Full process: `TYHPDEF_OWNERSHIP.md` in
https://github.com/tyhpproject/tyhp-runtime-src
<!-- tyhp-readme:end -->
