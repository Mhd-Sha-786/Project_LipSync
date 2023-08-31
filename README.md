# Project_LipSync
Lip Sync using Wav2Lip-HQ<br>
Here they had using Wav2Lip-HQ where they use image super resolution and face segmentation.<br>
Since the Wav2Lip having much issues in libraries during installation, here we donot get any any kind of library errors.<br>
Steps:<br>

1. The github repository is cloned.<br>
     git clone "https://github.com/Markfryazino/wav2lip-hq.git" <br>
2. Installing gdown and the required files for the model<br>
The "gdown" library enables us to download larger files from the Google Drive.<br>
   !pip3 install gdown <br>
   !pip3 install -r requirements.txt <br>
3. The face detection checkpoint is also downloaded.<br>
   !wget "https://www.adrianbulat.com/downloads/python-fan/s3fd-619a316812.pth" -O "face_detection/detection/sfd/s3fd.pth" <br>
4. The urls of wav2lip_gan.path, pretarined ESRGAN and face_segmentation paths are given accordingly.<br>
5. The urls of required video and audio is provided.<br>
6. Due to Exception, the librosa==0.8.0 version is installed.<br>
   !pip install librosa==0.8.0 <br>
7. Finally, inference script is executed.<br>
   !python inference.py <br>
    --checkpoint_path "checkpoints/wav2lip_gan.pth" <br>
    --segmentation_path "checkpoints/face_segmentation.pth" <br>
    --sr_path "checkpoints/esrgan_yunying.pth" <br>
    --face /path/ to/ source video <br>
    --audio /path /to /source audio <br>
    --outfile /desired /path /to /output <br>
8. The final output video will be stored in result folder.<br>


Since this is a basic model and much optimization is needed to imporove the quality of lip sync.<br>
Here the video is resized and trimmed for quality of lip sync. 
