
# sFID score for tensorflow

This is a port of the unofficial implementation of [Sliding Fréchet Inception Distance](https://proceedings.neurips.cc/paper_files/paper/2016/file/8a3363abe792db2d8761d6403605aeb7-Paper.pdf) to tensorflow.
It better captures spatial relationships than FID.

## Installation

Clone this repository, and then create the tensorflow environment:

```bash
git clone https://github.com/BienLuky/Tensorflow-sfid.git
```

Requirements:
- tensorflow == 2.5.0

## Usage

To compute the sFID score between two datasets, where images of each dataset are contained in an individual folder. Firstly, the two datasets need to be saved in .npz format and then to be calculated:
```
python sfid.py --ref_batch path/dataset1.npz --sample_batch path/dataset2.npz --ref_path path/to/dataset1 --sample_path path/to/dataset2
```
where the <ref_batch> and <sample_batch> replace the path to save datasets in .npz, the <ref_path> and <sample_path> replace the path of datasets to calculate sFID.
To run the evaluation on GPU, add the flag `CUDA_VISIBLE_DEVICES=N`, where `N` is the index of the GPU to use.

