# CDTV Bookmark and Cardmark Identifier Registry

Welcome to the "official" (and currently only) registry of CDTV Bookmark and Cardmark Identifiers. This repository catalogs all known identifiers used on the Commodore CDTV platform, from official Manufacturer IDs issued in the early 1990s to unofficial IDs used by modern developers creating new CDTV content.

If you're developing for CDTV and plan to use bookmarks or cardmarks, you're encouraged to reserve a unique Manufacturer ID by getting in touch. Details on how to apply are in the FAQ below as well as info on what bookmarks and cardmarks are, and how this registry works.

![](pics/CDTV%20Land%20Bookmark%20Cardmark%20Identifier%20Registry%20logo%20A.jpg)

## Manufacturer IDs

This table lists all currently known CDTV Manufacturer IDs.

|  Dec  |  Hex  | ASCII | Manufacturer                        | Remark(s)                |
|------:|:-----:|:-----:|:------------------------------------|:-------------------------|
|     1 | `0001`|       | Commodore                           |                          |
|    13 | `000D`|       | Merit Software                      |                          |
|    15 | `000F`|       | Phibrizzo                           |                          |
|    16 | `0010`|       | CDTV Publishing                     |                          |
|    22 | `0016`|       | ReadySoft                           |                          |
|    25 | `0019`|       | Oxford Digital Enterprises/Empire   |                          |
|    27 | `001B`|       | Discis Knowledge Research           |                          |
|  4660 | `1234`|       | Commodore                           |                          |
| 17228 | `434C`|   CL  | CDTV Land                           |                          |
| 22616 | `5858`|   XX  | Reserved for testing / development  |                          |
| 22617 | `5859`|   XY  | Reserved for testing / development  |                          |
| 22618 | `585A`|   XZ  | Reserved for testing / development  |                          |



## Manufacturer IDs and Product IDs

This table lists all currently known CDTV Product IDs, sorted by Manufacturer ID.

|  Dec  |  Hex  | ASCII | Product                                   | Remark(s)                |
|------:|:-----:|:-----:|:------------------------------------------|:-------------------------|
|     1 | `0001`|       | / **Commodore** /                         | << Manufacturer ID       |
|     1 | `0001`|       | CDTV System Preferences                   |                          |
| 65534 | `FFFE`|       | Debug bookmark                            |                          |
| ----- | ----- | ----- | ----------------------------------------- | ------------------------ |
|    13 | `000D`|       | / **Merit Software** /                    | << Manufacturer ID       |
|     1 | `0001`|       | Classic Board Games                       | Language selection       |
| ----- | ----- | ----- | ----------------------------------------- | ------------------------ |
|    15 | `000F`|       | / **Phibrizzo** /                         | << Manufacturer ID       |
|    12 | `000C`|       | Choctris                                  | Used to store hi-scores  |
| ----- | ----- | ----- | ----------------------------------------- | ------------------------ |
|    16 | `0010`|       | / **CDTV Publishing** /                   | << Manufacturer ID       |
|     1 | `0001`|       | Dr. Wellman's Guide                       | Used to store PIN code   |
| ----- | ----- | ----- | ----------------------------------------- | ------------------------ |
|    22 | `0016`|       | / **ReadySoft** /                         | << Manufacturer ID       |
|     1 | `0001`|       | Wrath of the Demon                        | Load/Save game           |
|     2 | `0002`|       | Guy Spy and the Crystals of Armageddon    | Load/Save game           |
| ----- | ----- | ----- | ----------------------------------------- | ------------------------ |
|    25 | `0019`|       | / **Oxford Digital Enterprises/Empire** / | << Manufacturer ID       |
|     1 | `0001`|       | Team Yankee                               | Load/Save game           |
| ----- | ----- | ----- | ----------------------------------------- | ------------------------ |
|    27 | `001B`|       | / **Discis Knowledge Research** /         | << Manufacturer ID       |
| 53817 | `D239`|       | The Paperbag Princess                     | Bookmark and language    |
| 53819 | `D23B`|       | Thomas's Snowsuit                         | Bookmark and language    |
| 53821 | `D23D`|       | Scary Poems for Rotten Kids               | Bookmark and language    |
| 53823 | `D23F`|       | Mud Puddle                                | Bookmark and language    |
| 53825 | `D241`|       | Cinderella                                | Bookmark and language    |
| 53827 | `D243`|       | The Tale of Benjamin Bunny                | Bookmark and language    |
| 53829 | `D245`|       | A Long Hard Day at the Ranch              | Bookmark and language    |
| 53830 | `D246`|       | Heather Hits Her First Home Run           | Bookmark and language    |
| 53832 | `D248`|       | Moving Gives Me a Stomach Ache            | Bookmark and language    |
| 53844 | `D254`|       | The Night Before Christmas                | Bookmark and language    |
| 53862 | `D266`|       | The Tale of Peter Rabbit                  | Bookmark and language    |
| ----- | ----- | ----- | ----------------------------------------- | ------------------------ |
|  4660 | `1234`|       | / **Commodore** /                         | << Manufacturer ID       |
| 17185 | `4321`|       | CD500 (CDTV-CR) IDE Bookmark              | To speed up drive check  |
| ----- | ----- | ----- | ----------------------------------------- | ------------------------ |
| 17228 | `434C`|    CL | / **CDTV Land** /                         | << Manufacturer ID       |
|     1 | `0001`|       | Extended CDTV System Preferences          | Introduced in OS 2.35    |
|  3001 | `0BB9`|       | Secret of Monkey Island Preferences       | Planned for rev 3        |
| ----- | ----- | ----- | ----------------------------------------- | ------------------------ |


## FAQ

### What are Bookmarks?

Bookmarks are small chunks of data stored in a special non-volatile memory area inside CDTV-compatible systems. CDTV titles use them to save user preferences, settings, and game progress. Think of them as CDTV’s version of saved game files or configuration memory.

### What are Cardmarks?

Cardmarks serve the same purpose as bookmarks but are stored on optional external memory cards, either 64K or 256K CDTV cards (models CD1401 and CD1405). These memory cards plug into the CDTV player via the front panel.

### What are Bookmark IDs?

Each bookmark or cardmark has a 32-bit ID, divided into two parts:
- a 16-bit **Manufacturer ID** 
- a 16-bit **Product ID**

Because the internal bookmark memory must be shared among many different CDTV titles, Commodore assigned unique Manufacturer IDs to developers to avoid conflicts. This system works much like the Autoconfig ID system for hardware on the Amiga.

Each developer is responsible for ensuring their titles only use their assigned Manufacturer ID. Within that ID space, the developer can freely assign unique Product IDs to distinguish between titles or data types.

Both bookmarks and cardmarks use the same ID format.

### What is this registry for?

The main goal of this repository is to avoid bookmark collisions by tracking all known Manufacturer IDs, past and present. This helps developers of new CDTV titles reserve a unique ID, so they don’t accidentally overwrite data from existing titles.

A secondary purpose is to allow developers and enthusiasts to look up which ID corresponds to which piece of CDTV software.

### Where does the registry data come from?

This registry was compiled by CDTV Land through a combination of memory analysis, reverse engineering, and disassembly of CDTV software. Commodore never published an official list of Manufacturer IDs, and any such record appears to have been lost when the company folded.

### Who maintains this registry?

The registry is maintained by CDTV Land. We don't claim to be an authority. This is a community-driven effort born out of necessity. In the absence of an official list, this is the best we've got.

### Do I have to register a Manufacturer ID?

No, registration is optional. But it’s highly encouraged! Registering ensures your bookmarks won’t conflict with others, which is especially important if you're planning to release your CDTV title to the public.

### How do I apply for a Manufacturer ID?

Easy! Either:

* Open a GitHub issue in this repo
* Email us at **[cdtvbookmarkid@gmail.com](mailto:cdtvbookmarkid@gmail.com)**

Let us know the name you'd like to be listed under, and we’ll add your Manufacturer ID to the registry. That's all there's to it!

### Can I choose my own Manufacturer ID?

Yes! As long as the ID hasn’t already been claimed, you’re free to pick one that suits you.

### Can I have multiple Manufacturer IDs?

While a single Manufacturer ID gives you 65,536 possible Product IDs (more than enough for most developers) if you have a valid reason to request more than one, that’s absolutely fine.

### Can I use a Manufacturer ID for testing without registering?

Yes. We’ve set aside three IDs specifically for testing and development:

* **22616** (ASCII: "XX")
* **22617** (ASCII: "XY")
* **22618** (ASCII: "XZ")

These IDs were chosen because their ASCII representation makes them easy to spot in memory dumps. You're welcome to use these freely for internal testing, but **don’t use them in released titles**! Register your own unique Manufacturer ID instead.

### Do I have to register Product IDs too?

No, but it’s appreciated! Registering your Product IDs helps other developers and tools recognize what data belongs to which title, making debugging and analysis easier for everyone.

### Where can I learn more about bookmarks?

A good place to start is the official [CDTV Developer Reference Manual](https://archive.org/details/CDTV_Developer_Reference_Manual). See section **3.2.6 – Bookmark and Cardmark Device Drivers** for a detailed technical explanation.

