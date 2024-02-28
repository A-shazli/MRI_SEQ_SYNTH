# MRI_SEQ_SYNTH

## LINK TO PAPER WILL BE HERE

## Abstract
Manual segmentation of brain tumors in structural MRI images is an arduous and time-consuming task. Therefore, an automatic and robust segmentation will significantly impact neuro-oncological clinical trials by reducing excessive manual annotation time . In this study, we propose a self-configuring deep learning model that aims to automatically segment different brain tumor tissues (Edema, Enhancing Tumor, and Necrosis) even in cases of missing MRI sequences, which are common in practical clinical settings. To tackle this issue, we enhance a Generative Adversarial Network (GAN) by incorporating a squeeze-and-excitation attention module into its generator and a PatchGAN into its discriminator. This enhancement allows our model to synthesize the missing MRI sequence by leveraging information from other available sequences (T1-weighted, T2-weighted, Contrast-Enhanced T1-weighted (T1ce), or Fluid Attenuated Inversion Recovery (FLAIR)), with a particular emphasis on the FLAIR sequence. For the segmentation task, we employ an optimized nnU-Net model, which is trained using existing sequences and evaluated using both available and synthesized sequences (including missing ones), mimicking real-world scenarios where often only limited MRI sequences are available or usable. Our findings demonstrate a notable enhancement in brain tumor segmentation, reflected in a significant increase in overall Dice scores from 0.688% (when FLAIR is missing) to 0.873% (when utilizing synthesized FLAIR derived from T2). This improvement brings the segmentation performance closer to what was achieved when real FLAIR is available, where the Dice score reaches 0.901%. Additionally, the resulting tumor segmentations are subsequently used to assess the response to treatment, in both cases where all sequences were available and when synthesis was employed,  according to Response Assessment in Neuro-oncology (RANO) criteria.

<img src="https://github.com/A-shazli/MRI_SEQ_SYNTH/assets/61319952/fb9466d8-62a5-4c48-a48e-846a445dadcf">

<h1>THIS REPO IS BASED ON COLAB NOTEBOOKS <br/>FOLLOW THE INSTRUCTIONS IN THE NOTEBOOKS TO RUN <br/>ALSO RUN THE NOTEBOOKS IN THE SEQUENCE THEY ARE NUMBERED</h1>
<hr/>

<h2>Make sure to read the comments and use the paths as shown in the notebooks</h2>

<a href="https://drive.google.com/drive/u/0/folders/1x3xXbj5YS-8fWlt_ntTq0PHgIwDH_dbx">LINK TO PRETRAINED MODELS</a>
