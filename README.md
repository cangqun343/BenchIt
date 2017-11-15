# [Programming Language Benchmarks](https://benchit.vercel.app/)

[![bench](https://github.com/cangqun343/Another-Benchmarks-Game/actions/workflows/bench.yml/badge.svg)](https://github.com/cangqun343/Another-Benchmarks-Game/actions/workflows/bench.yml)
[![MIT License](https://img.shields.io/github/license/cangqun343/Another-Benchmarks-Game.svg)](https://github.com/cangqun343/Another-Benchmarks-Game/blob/master/LICENSE)

<!-- [![Build status](https://img.shields.io/appveyor/ci/cangqun343/Another-Benchmarks-Game/main.svg)](https://ci.appveyor.com/project/cangqun343/Another-Benchmarks-Game) -->

# Why Build This
The idea is to build an automatic process for benchmark generation and pulishing

### Comparable numbers
*It currently use CI to generate benchmark results to garantee all the numbers are generated from the same environment at nearly the same time. All benchmark tests are executed in a single CI job*

### Automatic publish

*Once a change is merged into main branch, the CI job will re-generate and publish the static website*


# [Website](https://benchit.vercel.app/)
### Build
To achieve better SEO, the published site is static and prerenderd, powered by [nuxt.js](https://nuxtjs.org/).

### Host
The website is hosted on [Vercel](https://vercel.com/)

### Development
```
git clone https://github.com/cangqun343/Another-Benchmarks-Game.git

cd website
yarn
yarn generate
yarn dev
```

# Benchmarks
*All benchmarks are defined in [bench.yaml](https://github.com/cangqun343/Another-Benchmarks-Game/blob/main/bench/bench.yaml)*

*Current benchmarks problems and their implementations are from [The Computer Language Benchmarks Game](https://benchmarksgame-team.pages.debian.net/benchmarksgame/)  ([ Repo](https://salsa.debian.org/benchmarksgame-team/benchmarksgame/))*


# Local development
## Prerequisites

[docker](https://www.docker.com/)

[net5](https://dotnet.microsoft.com/)

[node LTS](https://nodejs.org/)

[yarn](https://yarnpkg.com/)

## Build

*The 1st step is to build source code from various of lanuages*
```bash
cd bench
dotnet run -p tool --task build
```

## Test

*The 2nd step is to test built binaries to ensure the correctness of their implementation*
```bash
cd bench
dotnet run -p tool --task test
```

## Bench

*The 3rd step is to generate benchmarks*
```bash
cd bench
dotnet run -p tool --task bench
```

*For usage*
```bash
cd bench
dotnet run -p tool --help
```

## Referesh website

*Lastly you can re-generate website with latest benchmark numbers*

```
cd website
yarn
yarn content
yarn generate
serve dist
```

# TODOs
Intergrate test environment info into website

Intergrate build / test / benchmark infomation into website

...

# How to contribute
TODO

# Thanks
*This is inspired by [The Computer Language Benchmarks Game](https://benchmarksgame-team.pages.debian.net/benchmarksgame/), thanks to the creator.*

# LICENSES
Code of problem implementation from [The Computer Language Benchmarks Game](https://salsa.debian.org/benchmarksgame-team/benchmarksgame/) is under their [Revised BSD](https://benchmarksgame-team.pages.debian.net/benchmarksgame/license.html)

Other code in this repo is under MIT.
