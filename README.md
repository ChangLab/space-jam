# space-saver
#### Utilities for efficiently managing storage
---

While data storage needs are ever increasing, there are certain steps that can be taken to efficiently store and transfer existing data.

The most important action is to compress data that is not immediately needed. Escpecially, compressing file types that contain text data e.g., any file containing sequences, can reduce a file's footprint by **40–90%**.
This also plays an important role when data is uploaded to AWS (or any other cloud file storage), as it drastically reduces transfer times and monthly storage costs, **which needs to be accounted for years and decades**!

The compression script includes many of the common file formats which gives space savings, while excluding binary formats like `.bam`.
The script utilizes [pigz](https://zlib.net/pigz/) which is a parallel implementation of gzip and provides a _N_ fold increase in compression speed, where _N_ is the number of physical CPU cores.

The script was tested on Linux and macOS, and pigz has been installed on Changrila2 and Sherlock.

To install pigz on Intel or Apple Silicon (M1 and newer) Macs, first install [Homebrew](https://brew.sh) and then do `brew install pigz`.

