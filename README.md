# Crunch

**crunch/crnlib v1.04U** — Advanced DXTn texture compression library (Dæmon branch, Unity format variant)

- Upstream for the Dæmon branch: https://github.com/DaemonEngine/crunch
- Bug tracker for the Dæmon branch: https://github.com/DaemonEngine/crunch/issues

Target & compiler|Build status|Target & compiler|Build status
-|-|-|-
<sub>Linux amd64 GCC</sub>|[![Build Status](https://dev.azure.com/UnvanquishedDevelopment/crunch/_apis/build/status%2FDaemonEngine.crunch?branchName=master&jobName=Job&configuration=Job%20Linux%20amd64%20Clang)](https://dev.azure.com/UnvanquishedDevelopment/crunch/_build/latest?definitionId=3&branchName=master)|<sub>Windows amd64 MSVC</sub>|[![Build status](https://ci.appveyor.com/api/projects/status/github/DaemonEngine/crunch?banch=master&svg=true)](https://ci.appveyor.com/project/DolceTriade/crunch/history)
<sub>Linux amd64 Clang</sub>|[![Build Status](https://dev.azure.com/UnvanquishedDevelopment/crunch/_apis/build/status%2FDaemonEngine.crunch?branchName=master&jobName=Job&configuration=Job%20Linux%20amd64%20Clang)](https://dev.azure.com/UnvanquishedDevelopment/crunch/_build/latest?definitionId=3&branchName=master)|<sub>Windows i686 MSVC</sub>|[![Build status](https://ci.appveyor.com/api/projects/status/github/DaemonEngine/crunch?banch=master&svg=true)](https://ci.appveyor.com/project/DolceTriade/crunch/history)
<sub>Linux i686 GCC|[![Build Status](https://dev.azure.com/UnvanquishedDevelopment/crunch/_apis/build/status%2FDaemonEngine.crunch?branchName=master&jobName=Job&configuration=Job%20Linux%20i686%20GCC)](https://dev.azure.com/UnvanquishedDevelopment/crunch/_build/latest?definitionId=3&branchName=master)|<sub>Windows amd64 MinGW</sub>|[![Build Status](https://dev.azure.com/UnvanquishedDevelopment/crunch/_apis/build/status%2FDaemonEngine.crunch?branchName=master&jobName=Job&configuration=Job%20Windows%20amd64%20MinGW)](https://dev.azure.com/UnvanquishedDevelopment/crunch/_build/latest?definitionId=3&branchName=master)
<sub>Linux arm64 GCC</sub>|[![Build Status](https://dev.azure.com/UnvanquishedDevelopment/crunch/_apis/build/status%2FDaemonEngine.crunch?branchName=master&jobName=Job&configuration=Job%20Linux%20arm64%20GCC)](https://dev.azure.com/UnvanquishedDevelopment/crunch/_build/latest?definitionId=3&branchName=master)|<sub>Windows i686 MinGW</sub>|[![Build Status](https://dev.azure.com/UnvanquishedDevelopment/crunch/_apis/build/status%2FDaemonEngine.crunch?branchName=master&jobName=Job&configuration=Job%20Windows%20i686%20MinGW)](https://dev.azure.com/UnvanquishedDevelopment/crunch/_build/latest?definitionId=3&branchName=master)
<sub>Linux armhf GCC</sub>|[![Build Status](https://dev.azure.com/UnvanquishedDevelopment/crunch/_apis/build/status%2FDaemonEngine.crunch?branchName=master&jobName=Job&configuration=Job%20Linux%20armhf%20GCC)](https://dev.azure.com/UnvanquishedDevelopment/crunch/_build/latest?definitionId=3&branchName=master)|<sub>macOS amd64 AppleClang</sub>|[![Build Status](https://dev.azure.com/UnvanquishedDevelopment/crunch/_apis/build/status%2FDaemonEngine.crunch?branchName=master&jobName=Job&configuration=Job%20macOS%20amd64%20AppleClang)](https://dev.azure.com/UnvanquishedDevelopment/crunch/_build/latest?definitionId=3&branchName=master)
<sub>Web Asm.js Emscripten</sub>|[![Build Status](https://dev.azure.com/UnvanquishedDevelopment/crunch/_apis/build/status%2FDaemonEngine.crunch?branchName=master&jobName=Job&configuration=Job%20Web%20Asm.js%20Emscripten)](https://dev.azure.com/UnvanquishedDevelopment/crunch/_build/latest?definitionId=3&branchName=master)|<sub>macOS arm64 AppleClang</sub>|[![Build Status](https://dev.azure.com/UnvanquishedDevelopment/crunch/_apis/build/status%2FDaemonEngine.crunch?branchName=master&jobName=Job&configuration=Job%20macOS%20arm64%20AppleClang)](https://dev.azure.com/UnvanquishedDevelopment/crunch/_build/latest?definitionId=3&branchName=master)

## Dæmon crunch tool

ℹ️ The [Dæmon engine](https://github.com/DaemonEngine/Daemon) uses the [`master`](https://github.com/DaemonEngine/crunch/tree/master) branch, which tracks the [Unity fork](https://github.com/Unity-Technologies/crunch/tree/unity), with additional fixes and features. The Dæmon engine is the open source game engine powering the [Unvanquished game](https://unvanquished.net). The produced `.crn` files are compatible with both the Daemon game engine and the Unity game engine.

Dæmon crunch is brought to you by:

- **2014-2024**: Dæmon Developers and contributors  
  https://github.com/DaemonEngine/crunch
- **2017-2018**: Alexander Suvorov and Unity Software Inc.  
  https://github.com/Unity-Technologies/crunch/tree/unity
- **2010-2017**: Richard Geldreich, Jr. and Binomial LLC and contributors  
  https://github.com/BinomialLLC/crunch

The Dæmon crunch is known to be used by:

- The [Dæmon game engine](https://github.com/DaemonEngine/Daemon),
- The [Urcheon game data build automation tool](https://github.com/DaemonEngine/Urcheon),
- The [NetRadiant game level editor](https://netradiant.gitlab.io/) and the `q3map2` map compiler and light mapper,
- The [Unvanquished game](https://unvanquished.net),
- The [Xonotic game](https://xonotic.org),
- Some games using the Unity game engine.

This branch provides many improvements over the original crunch:

- ✅️ Unity crunch format (runs many time faster and produces smaller files),
- ✅️ Unity crunch metadata (the header is compatible with Unity),
- ✅️ Improved image compatibility (1-bit PNG images are now supported),
- ✅️ Added features and command line options (top mip renormalization and more),
- ✅️ Network file system compatibility,
- ✅️ Optional header-only checksumming,
- ✅️ Multisystem and multiplatform (runs almost everywhere),
- ✅️ CMake toolchain (with many useful build options).

## Unity crunch format

This repository merged improvements done by Unity Technologies, it produces
smaller files and produces them faster than original code by Binomial.
Unity also modified the format which makes it incompatible with earlier versions of the tool.

Quote from [unvanquished.net](https://unvanquished.net/unvanquished-area-51):

> [Unity guys said](https://blog.unity.com/technology/crunch-compression-of-etc-textures) that their modified crunch tool “can compress up to 2.5
> times faster, while providing about 10% better compression ratio”. So we
> did a test on our own asset repository, re-crunching all the ressources
> and textures packages. At the time we did the test the given corpus
> produced 1797 .crn files.  
> The Unity’s crunch tool reduced compression time by 4.31 and reduced size
> by 11.15%. They said “up to 2.5 time faster” but we’ve seen some random
> textures being compressed 6 time faster and the average of the whole is
> 4.3 time faster, and yes the tool compresses more than 10% more.

## Unity crunch metadata

Unlike the Unity `crunch` tool built from their public repository, this tool produces files loadable by the Unity engine.

Since [February 11th 2023](faf5127b8c69dfd1ae554f4f3bf8168048b48d9f), this branch sets the CRN `m_userdata0` field to `1` to make CRN files loadable by the Unity engine which now prevents to load files with this value set to `0`.

Files with this value set to `1` are expected to use the new format. Files with this value set to `0` may or may not use the new format. When Unity updated the tool and modified the format in an incompatible way, no bit was modified to detect if a CRN file was using the old or the new format. Unity has not updated that field in their public repository of Crunch so there may be files in the wild using new format with this value set to `0`.

## Improved image compatibility

The `stb_image` library was updated from version 1.18 to version 2.30, increasing the amount of image format variants that can be converted, like 1-bit PNG formats.

## Added features and command line options

In addition to the original `crunch` features and command line options this branch brings:

- `-rtopmip`: option to use with `-renormalize` to also renormalize on the top mip-level.
- `-noNormalDetection`: do not attempt to detect normal map to avoid selecting formats thought for normal maps when it's known an image is not a normal map. It may prevent the tool to use heavier and less-supported `DXT5_AGBR` format when `DXT1` is good enough.
- `-h` or `--help`: print the command line built-in help.

## Network file system compatibility

The original `crunch` tool used I/O functions not working on some network file systems like NFS or SSHFS. The limitations is now gone and `crunch` can now process image files stored over the network.

## Optional header-only checksumming

For applications distributing their files in containers already providing a checksum mechanism for the whole contained file, it's now possible to only validate the CRN header checksum instead of the whole file checksum to not checksum the whole file twice.

## Multisystem and multiplatform portability

Unlike upstream branches from Binomial LLC and Unity Software Inc. this branch focuses on keeping the code buildable outside of Windows and Visual Studio, and adds a CMake build option alongside the legacy Makefile.

This `crunch` tool and the related `crnlib` library are known to build with and and run on:

- Compilers: GCC, MinGW, MSVC, Clang, Apple Clang, and more.
- Systems: Linux, Windows, macOS, FreeBSD.
- Architectures: amd64, arm64, i686, armhf.

## CMake toolchain

CMake is now preferred to the old Makefile. The supplied CMake configuration provides many useful build options. Toolchain files for MinGW cross-compilation are also supplied.

## How to build

```sh
git clone https://github.com/DaemonEngine/crunch.git
cd crunch
cmake -S. -Bbuild
cmake --build build --parallel $(nproc)
```

Where `$(nproc)` is the amount of cores of your computer.

You'll then find a `crunch` binary in the `build/` folder.

Some CMake build options are availables (explore more with `ccmake`).

## Licensing

This software uses the ZLIB license, which is located in license.txt.
http://opensource.org/licenses/Zlib

Richard Geldreich removed copyright on all his work on Crunch in order to put it in public domain on 2020-09-15 with commit [`crunch@57353fa`](https://github.com/BinomialLLC/crunch/commit/57353fa9ac0908893215bc30ba106adfb80c4c95) but this repository also contains commits by Alexander Suvorov from Unity Technologies and from Dæmon Developers and contributors.

Portions of this software make use of public domain code originally
written by Igor Pavlov (LZMA), RYG (`crn_ryg_dxt*`), and Sean Barrett (`stb_image*.h`).

If you use this software in a product, an acknowledgment in the product 
documentation would be highly appreciated but is not required.

Note: crunch originally used to live on Google Code: https://code.google.com/p/crunch/

## Overview

crnlib is a lossy texture compression library for developers that ship
content using the DXT1/5/N or 3DC compressed color/normal map/cubemap
mipmapped texture formats. It was written by the same author as the open
source [LZHAM compression library](http://code.google.com/p/lzham/).

It can compress mipmapped 2D textures, normal maps, and cubemaps to
approx. 1-1.25 bits/texel, and normal maps to 1.75-2 bits/texel. The
actual bitrate depends on the complexity of the texture itself, the
specified quality factor/target bitrate, and ultimately on the desired
quality needed for a particular texture. 

crnlib's differs significantly from other approaches because its
compressed texture data format was carefully designed to be quickly
transcodable directly to DXTn with no intermediate recompression step.
The typical (single threaded) transcode to DXTn rate is generally
between 100-250 megatexels/sec. The current library supports PC
(Win32/x64) and Xbox 360. Fast random access to individual mipmap levels
is supported.

crnlib can also generates standard DDS files at specified quality
setting, which results in files that are much more compressible by
LZMA/Deflate/etc. compared to files generated by standard DXTn texture
tools (see below). This feature allows easy integration into any engine
or graphics library that already supports DDS files.

The CRN file format supports the following core DXTn texture formats:
DXT1 (but not DXT1A), DXT5, DXT5A, and DXN/3DC

It also supports several popular swizzled variants (several are
also supported by AMD's Compressonator): 
DXT5_XGBR, DXT5_xGxR, DXT5_AGBR, and DXT5_CCxY (experimental luma-chroma YCoCg).

## Recommended software

AMD's [Compressonator tool](https://github.com/GPUOpen-Tools/Compressonator)
is recommended to view the DDS files created by the crunch tool and the included example projects.

Note: Some of the swizzled DXTn DDS output formats (such as DXT5_xGBR)
read/written by the crunch tool or examples deviate from the DX9 DDS
standard, so DXSDK tools such as `DXTEX.EXE` won't load them at all or
they won't be properly displayed.

## Compression algorithm details

The compression process employed in creating both CRN and
clustered DDS files utilizes a very high quality, scalable DXTn
endpoint optimizer capable of processing any number of pixels (instead
of the typical hard coded 16), optional adaptive switching between
several macroblock sizes/configurations (currently any combination of
4x4, 8x4, 4x8, and 8x8 pixel blocks), endpoint clusterization using
top-down cluster analysis, vector quantization (VQ) of the selector
indices, and several custom algorithms for compressing the resulting
endpoint/selector codebooks and macroblock indices. Multiple feedback
passes are performed between the clusterization and VQ steps to optimize
quality, and several steps use a brute force refinement approach to improve 
quality. The majority of compression steps are multithreaded.

The CRN format currently utilizes canonical Huffman coding for speed
(similar to Deflate but with much larger tables), but the next major
version will also utilize adaptive binary arithmetic coding and higher
order context modeling using already developed tech from the my LZHAM
compression library.

## Supported file formats

crnlib supports three compressed texture file formats. The first
format (clustered DDS) is simple to integrate into an existing project
(typically, no code changes are required), but it doesn't offer the
highest quality/compression ratio that crnlib is capable of. Integrating
the second, higher quality custom format (CRN) requires a few
typically straightforward engine modifications to integrate the
CRN→DXTn transcoder header file library into your tools/engine.

### DDS

crnlib can compress textures to standard DX9-style `.dds` files using
clustered DXTn compression, which is a subset of the approach used to
create CRN files.(For completeness, crnlib also supports vanilla, block
by block DXTn compression too, but that's not very interesting.)
Clustered DXTn compressed DDS files are much more compressible than
files created by other libraries/tools. Apart from increased
compressibility, the DDS files generated by this process are completely
standard so they should be fairly easy to add to a project with little
to no code changes.

To actually benefit from clustered DXTn DDS files, your engine needs to
further losslessly compress the DDS data generated by crnlib using a
lossless codec such as zlib, lzo, LZMA, LZHAM, etc. Most likely, your
engine does this already. (If not, you definitely should because DXTn
compressed textures generally contain a large amount of highly redundant
data.)

Clustered DDS files are intended to be the simplest/fastest way to
integrate crnlib's tech into a project.

### CRN

The second, better, option is to compress your textures to `.crn` files
using crnlib. To read the resulting CRN data, you must add the CRN
transcoder library (located in the included single file, stand-alone
header file library inc/crn_decomp.h) into your application. CRN files
provide noticeably higher quality at the same effective bitrate compared
to clustered DXTn compressed DDS files. Also, CRN files don't require
further lossless compression because they're already highly compressed.

CRN files are a bit more difficult/risky to integrate into a project, but
the resulting compression ratio and quality is superior vs. clustered DDS files.

### KTX

crnlib and crunch can read/write the `.ktx` file format in various pixel formats.
Rate distortion optimization (clustered DXTc compression) is not yet supported
when writing KTX files. 

The KTX file format is just like DDS, except it's a fairly well specified
standard created by the Khronos Group. Unfortunately, almost all of the tools
the original Crunch author found that supported KTX were fairly (to very) buggy,
or were limited to only a handful of pixel formats, so there's no guarantee that
the KTX files written by crnlib can be reliably read by other tools.

## Building the examples

This release contains the source code and projects for three simple
example projects:

### example1

Demonstrates how to use crnlib's high-level C-helper
compression/decompression/transcoding functions in `inc/crnlib.h`. It's a
fairly complete example of crnlib's functionality.

### example2

Shows how to transcodec CRN files to DDS using **only**
the functionality in `inc/crn_decomp.h`. It does not link against against
`crnlib.lib` or depend on it in any way. (Note: The complete source code,
approx. 4800 lines, to the CRN transcoder is included in `inc/crn_decomp.h`.)

`example2` is intended to show how simple it is to integrate CRN textures
into your application.

### example3

Shows how to use the regular, low-level DXTn block compressor
functions in `inc/crnlib.h`. This functionality is included for
completeness. (Your engine or toolchain most likely already has its own
DXTn compressor. crnlib's compressor is typically very competitive or
superior to most available closed and open source CPU-based
compressors.)

## Creating compressed textures with crunch

The simplest way to create compressed textures using crnlib is to
integrate the `crunch` (or `crunch.exe`) command line tool
into your texture build toolchain or export process. It can write DXTn
compressed 2D/cubemap textures to regular DXTn compressed DDS,
clustered (or reduced entropy) DXTn compressed DDS, or CRN files. It
can also transcode or decompress files to several standard image
formats, such as TGA or BMP. Run `crunch --help` for help.

The `.crn` files created by `crunch` can be efficiently transcoded to
DXTn using the included CRN transcoding library, located in full source
form under `inc/crn_decomp.h`.

Here are a few example crunch.exe command lines:

1. Compress blah.tga to blah.dds using normal DXT1 compression:
  * `crunch -file blah.tga -fileformat dds -dxt1`

2. Compress blah.tga to blah.dds using clustered DXT1 at an effective bitrate of 1.5 bits/texel, display image statistic:
  * `crunch -file blah.tga -fileformat dds -dxt1 -bitrate 1.5 -imagestats`

3. Compress blah.tga to blah.dds using clustered DXT1 at quality level 100 (from [0,255]), with no mipmaps, display LZMA statistics:
  * `crunch -file blah.tga -fileformat dds -dxt1 -quality 100 -mipmode none -lzmastats`

3. Compress blah.tga to blah.crn using clustered DXT1 at a bitrate of 1.2 bits/texel, no mipmaps:
  * `crunch -file blah.tga -dxt1 -bitrate 1.2 -mipmode none`

4. Decompress blah.dds to a .tga file:
  * `crunch -file blah.dds -fileformat tga`

5. Transcode blah.crn to a .dds file:
  * `crunch -file blah.crn`

6. Decompress blah.crn, writing each mipmap level to a separate .tga file:
  * `crunch -split -file blah.crn -fileformat tga`

crunch.exe can do a lot more, like rescale/crop images before
compression, convert images from one file format to another, compare
images, process multiple images, etc.

Note: I would have included the full source to crunch.exe, but it still
has some low-level dependencies to crnlib internals which I didn't have
time to address. This version of crunch.exe has some reduced
functionality compared to an earlier eval release. For example, XML file
support is not included in this version.

## Using crnlib

The most flexible and powerful way of using crnlib is to integrate the
library into your editor/toolchain/etc. and directly supply it your
raw/source texture bits. See the C-style API's and comments in
inc/crnlib.h.

To compress, you basically fill in a few structs in and call one function:

```c
void *crn_compress( const crn_comp_params &comp_params,
                    crn_uint32 &compressed_size,
                    crn_uint32 *pActual_quality_level = NULL,
                    float *pActual_bitrate = NULL);
```

Or, if you want crnlib to also generate mipmaps, you call this function:

```c
void *crn_compress( const crn_comp_params &comp_params,
                    const crn_mipmap_params &mip_params,
                    crn_uint32 &compressed_size,
                    crn_uint32 *pActual_quality_level = NULL,
                    float *pActual_bitrate = NULL);
```

You can also transcode/uncompress DDS/CRN files to raw 32bpp images
using `crn_decompress_crn_to_dds()` and `crn_decompress_dds_to_images()`.

Internally, crnlib just uses inc/crn_decomp.h to transcode textures to
DXTn. If you only need to transcode CRN format files to raw DXTn bits
at runtime (and not compress), you don't actually need to compile or
link against crnlib at all. Just include inc/crn_decomp.h, which
contains a completely self-contained CRN transcoder in the "crnd"
namespace. The `crnd_get_texture_info()`, `crnd_unpack_begin()`,
`crnd_unpack_level()`, etc. functions are all you need to efficiently get
at the raw DXTn bits, which can be directly supplied to whatever API or
GPU you're using. (See example2.)

Important note: When compiling under native client, be sure to define
the `PLATFORM_NACL` macro before including the `inc/crn_decomp.h` header file library.

## Known issues/Bugs

* crnlib currently assumes you'll be further losslessly compressing its
output DDS files using LZMA. However, some engines use weaker codecs
such as LZO, zlib, or custom codecs, so crnlib's bitrate measurements
will be inaccurate. It should be easy to allow the caller to plug-in
custom lossless compressors for bitrate measurement.

* Compressing to a desired bitrate can be time consuming, especially when
processing large (2k or 4k) images to the CRN format. There are several
high-level optimizations employed when compressing to clustered DXTn DDS
files using multiple trials, but not so for CRN.

* The CRN compressor does not currently use 3 color (transparent) DXT1
blocks at all, only 4 color blocks. So it doesn't support DXT1A
transparency, and its output quality suffers a little due to this
limitation. (Note that the clustered DXTn compressor used when
writing clustered DDS files does _not_ have this limitation.)

* Clustered DXT5/DXT5A compressor is able to group DXT5A blocks into
clusters only if they use absolute (black/white) selector indices. This
hurts performance at very low bitrates, because too many bits are
effectively given to alpha.

* DXT3 is not supported when writing CRN or clustered DXTn DDS files.
(DXT3 is supported by crnlib's when compressing to regular DXTn DDS
files.) You'll get DXT5 files if you request DXT3. However, DXT3 is
supported by the regular DXTn block compressor. (DXT3's 4bpp fixed alpha
sucks verses DXT5 alpha blocks, so I don't see this as a bug deal.)

* The DXT5_CCXY format uses a simple YCoCg encoding that is workable but
hasn't been tuned for max. quality yet.

* Clustered (or rate distortion optimized) DXTc compression is only
supported when writing to DDS, not KTX. Also, only plain block by block
compression is supported when writing to ETC1, and CRN does not support ETC1.

## Compile to Javascript and WebAssembly with Emscripten

Download and install Emscripten:

- https://emscripten.org/docs/getting_started/downloads.html

From the repository directory, run:

```sh
cmake -Semscripten -Bbuild-emscripten
cmake --build build-emscripten
```

You’ll then find a `crunch.js` script and a `crunch.wasm` binary in the `build-emscripten/` folder.
