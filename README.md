# lip-sync-with-Wav2Lip

### This project utilizes a pre-trained model from Wav2lip to synchronize lip movements with audio files. The model employs sophisticated algorithms to dynamically adjust video content based on the accompanying audio, independent of language and speaker identity.

## Description
 The code and model used in this project are fully attributed to Wav2lip. While their repository may have unresolved errors and issues, this project documents common errors that may arise and provides potential solutions.The link to the Wav2Lip - https://github.com/Rudrabha/Wav2Lip.git

## Disclaimer
 This project is for educational and study purposes. I do not claim ownership or authority over the underlying code, data, or models. Please refer to the original sources and licenses for more information. I am not affiliated with the original authors or creators of the code, data, or models, and any questions or issues should be directed to them.

### Prerequisites

- `Python 3.6`
  Please note that the files in requirements.txt will only be downloaded in Python3.6 version, it does not work with later versions of python.
- ffmpeg: `sudo apt-get install ffmpeg`
  This code can be used only for Linux systems. However for Windows, ffmpeg must manually be downloaded from website and the environment variable must be set in the system. for more details refer this - https://www.gyan.dev/ffmpeg/builds/ 
- Install necessary packages using `pip install -r requirements.txt`.
  Update the requirements mentioned earlier to this
- Face detection [pre-trained model](https://www.adrianbulat.com/downloads/python-fan/s3fd-619a316812.pth) should be downloaded to `face_detection/detection/sfd/s3fd.pth`. Alternative [link](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/prajwal_k_research_iiit_ac_in/EZsy6qWuivtDnANIG73iHjIBjMSoojcIV0NULXV-yiuiIg?e=qTasa8) if the above does not work.
