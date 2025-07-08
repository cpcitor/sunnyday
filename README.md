---
author: Stéphane Gourichon (cpcitor)
title: Sunny Day, a short demo for Amstrad CPC
---

Sunny Day, a short demo for Amstrad CPC
=======================================

A demo for Amstrad CPC showcasing full screen 50fps animation.

On which machine will the demo run?
-----------------------------------

-   The demo should run on all Amstrad CPC: even the CPC464 with a tape
    drive will do.
-   All CRTCs are supported.

Why this is significant
-----------------------

It is a well-known fact that the Amstrad CPC has a big framebuffer for
its class (CPU and memory speed).

It takes several frames for the BASIC to simply draw a diagonal line
from one corner to the other (about 5 in mode 0, about 7 in mode 1 and
2). Extremely optimized games like Starion manage several frames per
second drawing a few lines.

This demo appears to shatter this limitation.

How it works
------------

This README is a little short to explain in detail. I'm planning to
spend some time explaining. It doesn't hurt if you ask!

How it looks like
-----------------

Well, after thinking about it I'd say you'd better not know how it looks
like, it would spoil the experience.

So, I'll show you only the preloader and part of the first instant.

See illustration of "preloader" in file "illustrations/sunnyday_preloader.png".

See illustration of "circle" in file "illustrations/sunnyday_00_circle.png".


Files to run the prod
---------------------

### Disk image: `sunnyday.dsk`

This is a disk image file.

#### From a disk image file to a real or emulated CPC accessing it.

Many options. You can:

-   get a CPC emulator for a modern machine (outdated lists on
    [cpcwiki](https://www.cpcwiki.eu/index.php/Category:Emulator) or
    [Wikipedia](https://en.wikipedia.org/wiki/List_of_computer_system_emulators#Amstrad_CPC)),
    insert the image as virtual disc,
-   *easiest on hardware* through the audio cable described in the audio
    section to instruct a real CPC to create a real disc from the image
    with [dsk2cdt2disc](https://github.com/pelrun/dsk2cdt2disc) --
    tested with a CPC-6128, might also work with a
    CPC464+DDI1+pseudo-tape.
-   **or** easy but needs a modern device, transfer to a storage like a
    SD-Card then use HxC, M4 or
    [other](https://www.cpcwiki.eu/index.php/Category:DATA_Storage) to
    let the CPC access the card,
-   **or** transfer to a PC-style 3.5-inch real disk ([Have Linux make a
    USB floppy drive write to a disk that a CPC can then
    read.](https://www.cpcwiki.eu/forum/technical-support/have-linux-make-a-usb-floppy-write-a-disk-that-a-cpc-can-read/))
    then read that disk on a CPC (needs a flat ribbon cable, see [Guide
    on how to connect a 3.5\" drive to a CPC6128/664 -
    CPCWiki](https://www.cpcwiki.eu/index.php/Guide_on_how_to_connect_a_3.5%22_drive_to_a_CPC6128/664)),
-   **or** plug a CPC drive to a PC (needs a flat ribbon cable, [see
    Connect a 3 inch drive to a PC -
    CPCWiki](https://www.cpcwiki.eu/index.php/Connect_a_3_inch_drive_to_a_PC))
    and with this drive transfer the image to a real CPC-style 3-inch
    disk (via Linux commands like `dd`), then you can read the disk with
    a real CPC

#### Run

To run the demo:

    run"sunnyday

You can also transfer the image to a real floppy disk, but that's beyond
this text.

### Tape images: `sunnyday_1000baud.cdt` and `sunnyday_2000baud.cdt`

Tape images are primarily meant to be used with a CPC emulator.

Once you have a CPC running in an emulator, type:

    run"

If the emulated CPC has a disk (disc) drive you will need this
variation:

    |tape
    run"

If the emulated CPC has a French keyboard and a disk (disc) drive, use
this variation:

    ùtape
    run"

You can also convert those images to audio files. See below, I prepared
audio files so that you don't have to!

### For transfer to a real cassette used in a CPC464: `sunnyday_1000baud.wav`

This is an audio file of duration 5 minutes 35 seconds.

-   Use the jack output of a modern machine (PC, smartphone, etc) and
    any decent consumer-grade audio cassette recorder to transfer the
    audio from the WAV file to an audio cassette.
-   Put the audio cassette in a CPC464.

Type:

    run"

If the CPC has a disk (disc) drive you will need this variation:

    |tape
    run"

If the CPC has a French keyboard and a disk (disc) drive, use this
variation:

    ùtape
    run"

-   You can use `sunnyday_2000baud.wav` which is twice faster, but less
    reliable. CPCs are old and some will work only with 1000baud
    version.

### For cable transfer to a real CPC: `sunnyday_2000baud.wav`

This is an audio file of duration 3 minutes 24 seconds.

-   Real CPC6128: if you have a special jack-to-CPC-DIN cable, then plug
    the jack side on the sound output of a modern machine (PC,
    smartphone, etc) and the DIN side to a real CPC 6128, and play the
    audio file at fairly loud volume.
-   Real CPC464: if you have a pseudo-cassette with a cable ending with
    a 3.5mm jack, put it in a CPC464.

If the CPC has a disk (disc) drive, type:

    |tape
    run"

If the CPC has a French keyboard and a disk (disc) drive, use this
variation:

    ùtape
    run"

In the case of a plain CPC464 without a disc drive, use this:

    run"
