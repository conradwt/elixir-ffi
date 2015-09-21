FFI
===

An easy way to call external functions (e.g. C functions) from [Elixir](https://github.com/elixir-lang/elixir).

Inspired by [Ruby's FFI](https://github.com/ffi/ffi)

** This is alpha software **

## Example Program

```elixir
defmodule MyLib do
  use FFI.Library

  ffi_lib "c"

  attach_function :puts, [:string], :int
end

MyLib.puts(["Hello world"])
```

## Installation

```shell
hub clone joshnuss/elixir-ffi
cd elixir-ffi
make
```

## Running Examples

```shell
mix run examples/basic.exs
```

## License

MIT
