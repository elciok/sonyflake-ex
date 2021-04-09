# sonyflake-ex

[![codecov][codecov-badge]][codecov] [![Build Status][travis-ci-badge]][travis-ci]

Sonyflake is a distributed unique ID generator inspired by [Twitter's
Snowflake](https://blog.twitter.com/2010/announcing-snowflake).

This is an elixir rewrite of the original
[sony/sonyflake](https://github.com/sony/sonyflake) project, written
in Go.

A Sonyflake ID is composed of

    39 bits for time in units of 10 msec
     8 bits for a sequence number
    16 bits for a machine id

## Installation

Add the package `sonyflake` to the list of dependencies in `mix.exs`:

```elixir
{:sonyflake_ex, "~> 0.1.0", hex: :sonyflake}
```

## Quickstart

``` elixir
sf = Sonyflake.new()
{:ok, sf, id} = Sonyflake.next_id(sf)
IO.puts(id)
```

There is a `Sonyflake.Setting` submodule to configure the
generator. API docs can be found autogenerated on [hexdocs].

## License

The MIT License (MIT).


  [codecov]: https://codecov.io/gh/hjpotter92/sonyflake-ex
  [codecov-badge]: https://codecov.io/gh/hjpotter92/sonyflake-ex/branch/main/graph/badge.svg?token=C0gJpcbuXe
  [hexdocs]: https://hexdocs.pm/sonyflake/
  [travis-ci]: https://travis-ci.com/hjpotter92/sonyflake-py
  [travis-ci-badge]: https://travis-ci.com/hjpotter92/sonyflake-py.svg?branch=master
