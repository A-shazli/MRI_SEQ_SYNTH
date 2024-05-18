# FLAIR MRI Sequence Synthesis Using Squeeze Attention Generative Model for Reliable Brain Tumor Segmentation

## Model architechtures
<img src="https://github.com/A-shazli/MRI_SEQ_SYNTH/assets/61319952/34064ca4-1420-44d3-aec0-fb47d44a3a80">

## Full framwork
<img src="https://github.com/A-shazli/MRI_SEQ_SYNTH/assets/61319952/0c85cd27-8df0-4774-a26c-7158740e9544">

## Application
### Synthesizing missing MRI sequence
<img src='https://github.com/A-shazli/MRI_SEQ_SYNTH/assets/61319952/d5491ec6-2c7c-4e4c-94cf-f33dc026b277'>

### Brain tumor segmentation
<img src='https://github.com/A-shazli/MRI_SEQ_SYNTH/assets/61319952/79b593fe-f21f-44de-b017-de68c7ce3a48'>


## Prerequisites
<ul>
  <li>Download the dataset <a href='https://www.med.upenn.edu/cbica/brats2021/#Data2'>from this link</a></li>
  <li>Required file structure</li>
  
  ```
  /data 
 │
 ├───BraTS2021_train
 │      ├──BraTS2021_00000 
 │      │      └──BraTS2021_00000_flair.nii.gz
 │      │      └──BraTS2021_00000_t1.nii.gz
 │      │      └──BraTS2021_00000_t1ce.nii.gz
 │      │      └──BraTS2021_00000_t2.nii.gz
 │      │      └──BraTS2021_00000_seg.nii.gz
 │      ├──BraTS2021_00002
 │      │      └──BraTS2021_00002_flair.nii.gz
 │      ...    └──...
 │
 └────BraTS2021_val
        ├──BraTS2021_00001 
        │      └──BraTS2021_00001_flair.nii.gz
        │      └──BraTS2021_00001_t1.nii.gz
        │      └──BraTS2021_00001_t1ce.nii.gz
        │      └──BraTS2021_00001_t2.nii.gz
        ├──BraTS2021_00002
        │      └──BraTS2021_00002_flair.nii.gz
        ...    └──...
  ```

  <li>
    <h3>Creare a new environment and in the terminal run the following command to install the required packages from the requirements.txt</h3>

  ``` 
  pip install -r requirements.txt
  ```
  </li>
  
</ul>

## Documentation
### 1- FIRST NOTEBOOK (PREPROCESSING)
This notebook's purpose is to do the necessary preprocessing to the volumes so they can be used as input to the GANs network. This includes, but is not limited to, converting to 2D images, normalization, and resizing to the GANs' default input size.
### 2- SECOND NOTEBOOK(GANS INFERENCE)
This notebook's purpose is to use our Attention GANs model to synthesize the missing FLAIR sequence and reconstruct the 3D volume from the 2D inferred FLAIR images, then save it at the required destination. If you want to use the pretrained sequence identification model, you can access it at this  <a href='https://github.com/Jpvmello/type-identification-mri-sequences'>Repo<a/>. However, we assume that the FLAIR is the one that is always missing, so we did not include it in our code.
### 3- THIRD NOTEBOOK(SEGMENTAION)
This notebook uses the optimized nnU-Net available at this  <a href='https://github.com/NVIDIA/DeepLearningExamples/blob/master/PyTorch/Segmentation/nnUNet/notebooks/BraTS21.ipynb'>Repo<a/> to segment the tumor using the three original sequences plus the synthesized FLAIR.
### 4- FOURTH NOTEBOOK(SHAPE RESTORATION)
This is an optional notebook you can use if you want to return the segmented prediction to its original dimensions. What we mean by original dimensions are the dimensions before background removal. Of course, you can use the segmentation mask as it is, but if you want to use the masks for online evaluations at the BraTS challenge, you must give them the predictions in their original shapes. In summary, this notebook crops the background volumes but saves the indices of cropping so you can undo it after the segmentation prediction. This background removal step is done by default in the optimized nnU-Net, but it does not save the indices.
### 5- TRAINING.ipynb
This is the notebook that you can use if you want to train your own Attention GANs network.
  
## Disclaimer
<p>This repo is based on jupyter notebooks. Be sure to run the notebooks in the order they are labeled. <br>Make sure to read the comments and use the paths as shown in the notebooks , And if you want to use our checkpoints please contact us at the following email m3zaelray2@gmail.com </p>

## License
This project is licensed under the GNU general public License - see the <a href='https://github.com/A-shazli/MRI_SEQ_SYNTH/blob/main/LICENSE'>LICENSE.txt</a> file for details

## Citation
<p>If you find this code useful, feel free to use it (or part of it) in your project and please cite our <a href=''>paper</a>:</p>

```
@article{
   title={FLAIR MRI Sequence Synthesis Using Squeeze Attention Generative Model for Reliable Brain Tumor Segmentation},
   ISSN={2090-2670},
   url={https://www.sciencedirect.com/science/article/pii/S111001682400468X?via%3Dihub},
   DOI={https://doi.org/10.1016/j.aej.2024.05.008},
   journal={Alexandria Engineering Journal (AEJ)},
   author={Abdulkhalek Al-Fakih, Abdullah Shazly, Abbas Mohammed, Mohammed Elbushnaq, Kanghyun Ryu, Yeong Hyeon Gu, Mohammed A. Al-masni, and Meena M. Makary},
   year={2024},
   month={May}
}
```

## References
<ol>
  <li>
    <a href='https://github.com/NVIDIA/DeepLearningExamples/blob/master/PyTorch/Segmentation/nnUNet/notebooks/BraTS21.ipynb'>Optimized U-Net for Brain Tumor Segmentation<a/>
  </li>
</ol>

<hr/>

