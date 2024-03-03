# Synthesizing Missing MRI Sequences Towards Reliable Brain Tumors Segmentation Using Deep Learning

## Model architechture
<img src="https://github.com/A-shazli/MRI_SEQ_SYNTH/assets/61319952/fb9466d8-62a5-4c48-a48e-846a445dadcf">

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
 
## Disclaimer
<p>This repo is based on jupyter notebooks. Be sure to run the notebooks in the order they are labeled. <br>Make sure to read the comments and use the paths as shown in the notebooks</p>

## License
This project is licensed under the GNU general public License - see the <a href='https://github.com/A-shazli/MRI_SEQ_SYNTH/blob/main/LICENSE'>LICENSE.txt</a> file for details

## Citation
<p>This work is currently undergoing review in the alexandria engineering journal (AEJ). If you find this code useful, feel free to use it (or part of it) in your project and please cite our <a href=''>paper</a>:</p>

```
@article{
   title={Synthesizing Missing MRI Sequences Towards Reliable Brain Tumors Segmentation Using Deep Learning},
   ISSN={},
   url={},
   DOI={},
   journal={Alexandria Engineering Journal (AEJ)},
   author={Abdulkhalek Al-Fakih, Abdullah Shazly, Abbas Mohammed, Mohammed Elbushnaq, Kanghyun Ryu, Yeong Hyeon Gu, Mohammed A. Al-masni, and Meena M. Makary},
   year={},
   month={}
}
```

## References
<ol>
  <li>
    <a href='https://github.com/NVIDIA/DeepLearningExamples/blob/master/PyTorch/Segmentation/nnUNet/notebooks/BraTS21.ipynb'>Optimized U-Net for Brain Tumor Segmentation<a/>
  </li>
</ol>

<hr/>

