## Reproduce the issue

```sh
rm -rf $(pnpm store path)
pnpm install
# postinstall of "canvas" (dependency of workspace project "package-a") gets executed and thus, native code is compiled ✅
pnpm run clean
pnpm install
# postinstall of "canvas" is not executed ❌
```
