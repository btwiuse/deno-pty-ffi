# Deno Pty FFI

deno wrapper over https://docs.rs/portable-pty/latest/portable_pty/ that exposes
a simple interface

## Usage

```ts
import { Pty } from "https://deno.land/x/deno_pty_ffi/mod.ts";

const pty = await Pty.create({
  cmd: "bash",
  args: [],
  env: [],
});

await pty.write("ls -la\n");
console.log(await pty.read());
```
