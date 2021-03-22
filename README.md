<p align="center">
  <img src="https://github.com/shie-ld/huffman-coding/blob/master/images/logo.png">
</p>

<h1 align="center">Huffman Coding</h1>

<p align="center">
  <a href="https://github.com/shie-ld/huffman-coding/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/shie-ld/huffman-coding"
      alt="MIT License" />
  </a>
  <a href="https://www.linkedin.com/in/rudresh-dixit-11a15618a">
    <img src="https://img.shields.io/badge/-LinkedIn-black.svg?style=plastic-square&logo=linkedin&colorB=555"
      alt="linkedin" />
  </a>
  <a href="https://github.com/shie-ld/huffman-coding/issues">
    <img src="https://img.shields.io/github/issues-raw/shie-ld/huffman-coding"
      alt="open issues" />
  </a>
  <a href="https://github.com/shie-ld/huffman-coding/issues?q=is%3Aissue+is%3Aclosed">
    <img src="https://img.shields.io/github/issues-closed-raw/shie-ld/huffman-coding"
      alt="closed issues" />
  </a>
</p>

Self-made C++ **file archiver** and **archive extractor** programs based on Huffman's lossless compression algorithm
## Table of Contents

* [How does it work](#how-does-it-work)
  * [Compressor](#compressor)
  * [Decompressor](#decompressor)
* [How to use it?](#how-to-use-it)

## How does it work?
_You can check out documentation inside [Compressor.cpp](https://github.com/shie-ld/huffman-coding/blob/master/Compressor.cpp) and [Decompressor.cpp](https://github.com/shie-ld/huffman-coding/blob/master/Decompressor.cpp) files to help you understand Huffman's algorithm's inner workings._
### Compressor:
The `Compressor` is a 2-pass program. What I mean by this is that the `Compressor` reads input files twice.

In the first pass, the program counts usage frequency of every unique byte and creates a weighted translation tree for every used unique byte inversely proportional to its usage frequency and then writes this transformation info to the compressed file for decompression purposes

In the second pass, the program translates input files according to the translation tree and writes it to the newly created compressed file

### Decompressor:
The `Decompressor` is a 1-pass program:
The `Decompressor` first reads translation info and creates a binary tree from it. After this process is done, it uses this binary translation tree to decode the rest of the file

## How to use it?
1. Compile with `make` using your favourate shell:
```
make all
```
2. After running make, you can use `archive` command below to compress the file you want:
* To compress one file use:
```
./archive {{filename}}
```
* To compress multiple files use:

```
./archive {{filename1}} {{filename2}} ...
```
3.  And to decompress a compressed file, use the `extract` command below:
```
./extract {{filename}}
```



<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/shie-ld/huffman-coding/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Rudresh Dixit - 00rudreshdixit@gmail.com

Project Link: [https://github.com/shie-ld/huffman-coding](https://github.com/shie-ld/huffman-coding)

