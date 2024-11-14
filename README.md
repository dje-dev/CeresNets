# CeresNets
This GitHub repository contains the latest binary weight files for the Ceres neural network chess engine.
The weights are in ONNX format and can be used with the [Ceres](https://github.com/dje-dev/Ceres) chess engine. 

Although these compressed ZIP files can be directly downloaded and uncompressed, it is most conveniet to use
the UCI download command supported by the Ceres engine.

For example, to download the C1-512-15 network, use the command:
```
download C1-256-10
```
See the Ceres installation instructions for more details.


## Available Networks

| ID | Date|Dim/Depth |Params(mm)|TRT Size(mb)|Training Pos(bn)|Speed (nps)[^1]|Elo (1000n)[^2]|First Appearance
| ---- | ------- |
|[C1-256-10](https://github.com/dje-dev/CeresNets/releases/tag/C1-256-10)|Sep 2024|256x10 |15|37|4.0|34,600[^3]|-96
|[C1-384-12](https://github.com/dje-dev/CeresNets/releases/tag/C1-384-12)|Sep 2024| 384x12 |31|70|6.0|19,200|-42
|[C1-512-15](https://github.com/dje-dev/CeresNets/releases/tag/C1-512-15)|Sep 2024|512x15 |70|140|5.2|9,600|9|TCEC Swiss 7
|[C1-768-15](https://github.com/dje-dev/CeresNets/releases/tag/C1-768-15)|Sep 2024|768x15 |126|257|9.0|5,600|54|TCEC Cup 14
|[C1-512-25](https://github.com/dje-dev/CeresNets/releases/tag/C1-512-25)|Oct 2024|512x25|129|263|6.0|8,300|74|TCEC S27 E/2 Leagues
|[C1-640-25](https://github.com/dje-dev/CeresNets/releases/tag/C1-640-25)|Nov 2024|640x25|185|374|7.0|5,500|124|TCEC S27 League 1

[^1]:Using TensorRT 10.5 on NVIDIA A6000 Ada with batch size 128. 
[^2]:Using openings UHO_Lichess_4852_v1.epd
[^3]:Actual speed within Ceres closer to 25,000 due to current implementation inefficiencies.
