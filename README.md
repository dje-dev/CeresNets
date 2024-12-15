# CeresNets
This GitHub repository contains the latest binary weight files for the Ceres neural network chess engine.
The weights are in ONNX format and can be used with the [Ceres](https://github.com/dje-dev/Ceres) chess engine. 

Although these compressed ZIP files can be directly downloaded and uncompressed, it is most convenient to use
the UCI download command supported by the Ceres engine.

For example, to download the C1-256-10 network, use the command:
```
download C1-256-10
```
See the Ceres installation instructions for more details.


## Available Networks
| ID | Date | Size | Params | TRT Size | Train[^2] | Speed[^3] | Elo[^4]|
| --- | --- | --- | --- | --- | --- | --- | --- |
| [C1-256-10](https://github.com/dje-dev/CeresNets/releases/tag/C1-256-10) | Sep 24 | 256x10 | 15mm | 37mb | 4.0bn | 34,600[^5] | -96|
| [C1-384-12](https://github.com/dje-dev/CeresNets/releases/tag/C1-384-12) | Sep 24 | 384x12 | 31mm | 70mb | 6.0bn | 19,200 | -42|
| [C1-512-15](https://github.com/dje-dev/CeresNets/releases/tag/C1-512-15) | Sep 24 | 512x15 | 70mm | 140mb | 5.2bn | 9,600 | 9|
| [C1-768-15](https://github.com/dje-dev/CeresNets/releases/tag/C1-768-15) | Sep 24 | 768x15 | 126mm | 257mb | 9.0bn | 5,600 | 54|
| [C1-512-25](https://github.com/dje-dev/CeresNets/releases/tag/C1-512-25) | Oct 24 | 512x25 | 129mm | 263mb | 6.0bn | 8,300 | 74|
| [C1-640-25](https://github.com/dje-dev/CeresNets/releases/tag/C1-640-25) | Nov 24 | 640x25 | 185mm | 374mb | 7.0bn | 5,500 | 124|
| [C1-640-34](https://github.com/dje-dev/CeresNets/releases/tag/C1-640-34) | Dec 24 | 640x34 | 250mm | 504mb | 10.0bn | 3,900 | 160|

[^1]:Size of transformer embedding dimension by number of encoder layers
[^2]:Number of training positions on which the network was trained
[^3]:Nodes per second using TensorRT 10.5 on NVIDIA A6000 Ada with batch size 128. 
[^4]:Using openings UHO_Lichess_4852_v1.epd and fixed nodes test (1000 nodes per search)
[^5]:Actual speed within Ceres closer to 25,000 due to current implementation inefficiencies
