# stego-semantic-segmentation-kaggle
CS4240 Deep Learning group assignment, train and evaluate unsupervised semantic segmentation STEGO (ICLR 2022 Paper) on PASCAL VOC 2012 dataset on Kaggle
## Steps
1. Upload this notebook to Kaggle
2. In Session Options -> Accelerator, select GPU T4 x 2
3. Download the PASCAL VOC 2012 Dataset
4. Rename the folders in VOC2012
`cd /your/path/to/VOC2012`
`mv Annotations 'Annotations old'`
`mv SegmentationClass Annotations`
4. In Input -> Upload, select New Dataset, upload the compressed PASCAL VOC 2012 dataset to Kaggle
5. Execute the `git clone` section in the notebook
5. Now the VOC2012 file is under `/kaggle/input` folder, which is read-only. After running the git clone section in the notebook, execute
`cp -r /kaggle/input/your_compressed_file_name/VOC2012 /kaggle/working/STEGO/datadrive/pytorch-data/`
6. Run the rest of the notebook
- run `precompute_knns.py`
- run `train_segmentation.py`
