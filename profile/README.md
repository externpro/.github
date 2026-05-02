# externpro 🧰🔧

**A CMake build platform and dependency provider with reusable CI pipelines.**
Reproducible builds. Reusable dependencies. Consistent CI. Fewer “works on my machine” surprises.

[![CMake](https://img.shields.io/badge/CMake-CMakePresets-blue)](https://github.com/externpro/externpro)
[![CI](https://img.shields.io/badge/CI-Reusable%20Workflows-black)](https://github.com/externpro/externpro/tree/main/.github/workflows)
[![Supply%20Chain](https://img.shields.io/badge/Supply%20Chain-SBOM%2FAttestation-6f42c1)](https://github.com/externpro/externpro/blob/main/.github/docs/supply-chain.md)
[![Containers](https://img.shields.io/badge/Containers-Docker-2496ED)](https://github.com/orgs/externpro/packages?repo_name=buildpro)
[![xpbuild](https://github.com/externpro/buildpro/actions/workflows/xpbuild.yml/badge.svg)](https://github.com/externpro/buildpro/actions/workflows/xpbuild.yml)
[![Release](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.github.com%2Frepos%2Fexternpro%2Fexternpro%2Freleases%2Flatest&query=%24.tag_name&label=release)](https://github.com/externpro/externpro/releases)
[![License](https://img.shields.io/github/license/externpro/externpro)](https://github.com/externpro/externpro/blob/main/LICENSE)

## Why externpro? 🎯

externpro standardizes **toolchains**, **dependencies**, and **CI workflows** across developers, machines, and repositories—so teams ship faster with less drift and duplication.

## Main repos 📌

1. **[externpro](https://github.com/externpro/externpro) (core)** 🧰
   CMake build platform + dependency provider model + reusable workflows (`xpinit`, `xpupdate`, `xpbuild`, `xptag`, `xprelease`).

2. **[buildpro](https://github.com/externpro/buildpro) (Linux toolchain images)** 🐳
   Linux Docker build images used by externpro-enabled repos to keep compilers/tools/system deps consistent.

3. **[tutorial](https://github.com/externpro/tutorial) (adoption walkthrough)** 🎓
   Vendor externpro as a `.devcontainer` submodule, run `xpInit`, follow `xpTag → xpBuild → xpRelease`, and consume externpro-produced deps via `find_package()`.

## Start here 🚀

1. Add externpro as a submodule to your project — the [tutorial](https://github.com/externpro/tutorial#readme) walks through the exact steps
1. Run a CI workflow to initialize things
1. Make small modifications to existing CMake (or introduce CMake)
1. Use other org repos as reference implementations (see the externpro projects table: https://github.com/externpro/externpro/blob/main/cmake/README.md)
1. Start building and delivering your projects on multiple OSes, architectures, and compilers - creating packages that can be consumed by other projects quickly and consistently!
1. Read the core overview in [externpro](https://github.com/externpro/externpro#readme)
1. Review the foundational patterns in [buildpro](https://github.com/externpro/buildpro#readme)

## What you get ✅

| Capability | What it means |
|---|---|
| 🏗️ **Build platform** | A consistent build + toolchain baseline across Linux/macOS/Windows, x86_64/arm64, and multiple compiler toolchains (Linux buildpro containers; macOS/Windows GitHub-hosted runners) |
| 📦 **Dependency provider** | Dependencies are provided to your build as ready-to-use packages/targets, so consuming projects can just `find_package()` and link (rather than each repo reinventing fetch/build/patch) |
| 🔁 **Reusable CI** | Standardized init/update/build/test/tag/release pipelines with supply chain outputs (SBOM/attestation) |

## Repos in this org 🧪

Most repositories in the organization act as **reference implementations**—examples of integrating externpro and using the workflow as intended.
See the externpro projects table:
https://github.com/externpro/externpro/blob/main/cmake/README.md
