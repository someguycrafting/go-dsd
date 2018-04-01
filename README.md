# go-dsd

Digital Speech Decoder (and Encoder), with some basic DSP processing functions.

## Documentation

Read the [package documentation](https://godoc.org/github.com/pd0mz/go-dsd).


## Changes

* Removed Advanced Multi-Band Excitation (AMBE) codec support, not needed
* Removed AMBE debug options
* Removed DMR data types
* Changed Codec2 Encode method to accept samples in uint16 data type (Codec2 default)
* Changed Codec2 Decode method to return decoded speech in uint16 data type (Codec2 default)
* Added type conversion methods

## Supported codecs

### Codec2

Codec2 is a low-bitrate speech audio codec (speech coding) that is patent free
and open source. Both decoding and encoding of Codec2 frames are supported.


## Install instructions


### Install dependencies
sudo apt install libcodec2-dev

### Install go package

> See the build instructions for setting the compiler flags, you'll need
> to do it also before installing the package.

Install the package by running

```
go get github.com/someguycrafting/go-dsd
```

## Build instructions
Since Go release 1.8.7, some compiler/linker options are disabled and need to be whitelisted (see reason [here](https://github.com/golang/go/wiki/InvalidFlag)).

Before
```
go build
```
run
```
export CGO_CFLAGS_ALLOW="-L/usr/local/lib"
```
