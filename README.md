# AMD uCode collection

![Microcode file count](https://img.shields.io/github/directory-file-count/amd-zenith/amd-ucode-collection/patches?label=Microcode%20patches)


A collection of AMD uCode files.

This collection is maintained using [ZenScraper](https://github.com/amd-zenith/zenscraper), a tool to obtain AMD uCode files!

## Structure

All uCode patches are stored in the `patches/` directory.

For the patch files, the following naming convention applies:
* Older patches (no encryption, family <= 15h): `family<family>_cpuid<cpuid>_rev<revision>_date<yyyymmdd>_sha<hash12>.bin`
* Newer patches (family >= 16h): `family<family>_cpuid<cpuid>_rev<revision>_date<yyyymmdd>_enc<ee>_sha<hash12>.bin`
