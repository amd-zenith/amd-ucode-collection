# AMD uCode collection

![Microcode file count](https://img.shields.io/github/directory-file-count/amd-zenith/amd-ucode-collection/patches?label=Microcode%20patches)
[![Update collection](https://github.com/amd-zenith/amd-ucode-collection/actions/workflows/update-collection.yml/badge.svg)](https://github.com/amd-zenith/amd-ucode-collection/actions/workflows/update-collection.yml)
[![CodeQL](https://github.com/amd-zenith/amd-ucode-collection/actions/workflows/codeql.yml/badge.svg)](https://github.com/amd-zenith/amd-ucode-collection/actions/workflows/codeql.yml)
[![Scorecard](https://github.com/amd-zenith/amd-ucode-collection/actions/workflows/scorecard.yml/badge.svg)](https://github.com/amd-zenith/amd-ucode-collection/actions/workflows/scorecard.yml)
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/amd-zenith/amd-ucode-collection/badge)](https://scorecard.dev/viewer/?uri=github.com/amd-zenith/amd-ucode-collection)

A collection of AMD uCode files.

This collection is maintained using [ZenScraper](https://github.com/amd-zenith/zenscraper), a tool to obtain AMD uCode files!

## Structure

All uCode patches are stored in the `patches/` directory.

Every patch file follows the same naming convention:

```
family<family>_cpuid<cpuid>_rev<revision>_date<yyyymmdd>_enc<ee>_sha<hash12>.bin
```

| Field      | Description                                                                          |
| ---------- | ------------------------------------------------------------------------------------ |
| `family`   | CPU family, 2 hex digits (currently `0f` to `1a`)                                    |
| `cpuid`    | Processor signature the patch applies to, 8 hex digits                               |
| `revision` | Patch revision, 8 hex digits                                                         |
| `yyyymmdd` | Patch date                                                                           |
| `ee`       | Encryption identifier, 2 hex digits: `00` for plain patches, `01` for encrypted ones |
| `hash12`   | First 12 hex digits of the patch file SHA-256                                        |

For example, `family1a_cpuid00B00F81_rev0b008124_date20260408_enc01_sha9a73959ffb9c.bin`.
