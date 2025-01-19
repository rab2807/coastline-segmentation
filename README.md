# Coastline Detection using Satellite Imagery 

This repository contains the notebooks for our **CSE 472 Machine Learning Sessional project**.

Dataset: [Sentinel-2 Water Edges Dataset (SWED)](https://openmldata.ukho.gov.uk/)

The task is to segment the water bodies with the Sentinel-2 multispectral satellite imagery. We benchmarked total 6 deep learning architectures:

CNN based:
 * Unet
 * Unet with Channel Spatial block attention (CBAM)
 * MultiResUnet
 * MultiResUnet with Channel Spatial block attention (CBAM)
   
Transformer based:
 * SwinViT
 * TransUnet

From our experiment, TransUnet shows the best performance among all.

Benchmark results
---

| Model                    | accuracy  | bal_accuracy | precision | recall   | f1_score | jaccard_index | cohen_kappa | mcc      |
|--------------------------|-----------|--------------|-----------|----------|----------|---------------|-------------|----------|
| U-Net                   | 0.893694  | 0.901379     | **0.961387**  | 0.848395 | 0.901364 | 0.820439      | 0.787065    | 0.794313 |
| U-Net + CBAM             | 0.913052  | 0.914918     | 0.943596  | 0.902053 | 0.922357 | 0.855902      | 0.823685    | 0.824763 |
| MultiResUNet            | 0.91562   | 0.912634     | 0.920495  | 0.933222 | 0.926815 | 0.863611      | 0.827209    | 0.827318 |
| MultiResUNet + CBAM      | 0.902392  | 0.906614     | 0.948143  | 0.877505 | 0.911457 | 0.837319      | 0.803077    | 0.806067 |
| SwinUNet                | 0.896011  | 0.89906      | 0.936364  | 0.87804  | 0.906264 | 0.828596      | 0.789775    | 0.791835 |
| TransUNet               | **0.940173** | **0.939501** | **0.951013**  | **0.944135** | **0.947562** | **0.900349**      | **0.877924**    | **0.877956** |