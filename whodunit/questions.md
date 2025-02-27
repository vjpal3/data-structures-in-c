# Questions

## What's `stdint.h`?

stdint.h is a header file in C standard library that allows programmers to write portable code by providing a set of typdefs that define exact-width integer types along with max and min allowed values for each type using the macros.

## What's the point of using `uint8_t`, `uint32_t`, `int32_t`, and `uint16_t` in a program?

These are fixed width integer types, whose width remains same across all hardware environments. So writing a portable program using these data types is much more onvinient.

## How many bytes is a `BYTE`, a `DWORD`, a `LONG`, and a `WORD`, respectively?

Byte: 1 byte
DWORD: 4 bytes
LONG: 4 bytes
WORD: 2 bytes

## What (in ASCII, decimal, or hexadecimal) must the first two bytes of any BMP file be? Leading bytes used to identify file formats (with high probability) are generally called "magic numbers."

File type

## What's the difference between `bfSize` and `biSize`?

bfsize : The size, in bytes, of the bitmap file.
biSize : size of the BITMAPINFOHEADER header file. biSize is constant and it equals 40 bytes

## What does it mean if `biHeight` is negative?
A device-independent bitmap (DIB):
A bottom-up DIB, in which the origin lies at the lower-left corner.
A top-down DIB, in which the origin lies at the upper-left corner.
If biHeight is negative, it is a top-down DIB. Top-down DIBs cannot be compressed.

## What field in `BITMAPINFOHEADER` specifies the BMP's color depth (i.e., bits per pixel)?

biBitCount

## Why might `fopen` return `NULL` in `copy.c`?
If fopen fails because the file doesn't exists or it exists but the you don't have permissions to open it, then it returns NULL.


## Why is the third argument to `fread` always `1` in our code?
The third argument represents the quantity units of size to read.
Here we are reading the whole information about that struct(Bitmapfilegeader/bitmapinfoheader) in one call.

## What value does `copy.c` assign to `padding` if `bi.biWidth` is `3`?

padding: 3 bytes

## What does `fseek` do?

It moves the file pointer to a specific position. In this case, With respect to file pointer's current position, it is moving the infile pointer 'padding' number of bytes ahead.

## What is `SEEK_CUR`?
Current position of file pointer.
