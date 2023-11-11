# lip-sync-with-Wav2Lip

### This project utilizes a pre-trained model from Wav2lip to synchronize lip movements with audio files. The model employs sophisticated algorithms to dynamically adjust video content based on the accompanying audio, independent of language and speaker identity.

## Description
 The code and model used in this project are fully attributed to Wav2lip. While their repository may have unresolved errors and issues, this project documents common errors that may arise and provides potential solutions.The link to the Wav2Lip - https://github.com/Rudrabha/Wav2Lip.git

## Disclaimer
 This project is for educational and study purposes. I do not claim ownership or authority over the underlying code, data, or models. Please refer to the original sources and licenses for more information. I am not affiliated with the original authors or creators of the code, data, or models, and any questions or issues should be directed to them.

### Prerequisites

- `Python 3.6`.
  Please note that the files in requirements.txt will only be downloaded in Python3.6 version, it does not work with later versions of python.
- ffmpeg: `sudo apt-get install ffmpeg`.
  This code can be used only for Linux systems. However for Windows, ffmpeg must manually be downloaded from website and the environment variable must be set in the system. for more details refer this - https://www.gyan.dev/ffmpeg/builds/
- git clone using the command `git clone https://github.com/Rudrabha/Wav2Lip.git`
- Install necessary packages using `pip install -r requirements.txt`.
  Update the requirements mentioned earlier to [this](https://github.com/saiayush/lip-sync-with-Wav2Lip/blob/main/requirements.txt)
- Face detection [pre-trained model](https://www.adrianbulat.com/downloads/python-fan/s3fd-619a316812.pth) should be downloaded to `face_detection/detection/sfd/s3fd.pth`.
- Download the weights -
- [Wav2Lip](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/radrabha_m_research_iiit_ac_in/Eb3LEzbfuKlJiR600lQWRxgBIY27JZg80f7V9jtMfbNDaQ?e=TBFBVW)  
- [Wav2Lip + GAN](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/radrabha_m_research_iiit_ac_in/EdjI7bZlgApMqsVoEUUXpLsBxqXbn5z8VTmoxp55YNDcIA?e=n9ljGW)
- [Expert Discriminator](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/radrabha_m_research_iiit_ac_in/EQRvmiZg-HRAjvI6zqN9eTEBP74KefynCwPWVmF57l-AYA?e=ZRPHKP)
- [Visual Quality Discriminator](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/radrabha_m_research_iiit_ac_in/EQVqH88dTm1HjlK11eNba5gBbn15WMS0B0EZbDBttqrqkg?e=ic0ljo)

### Inference

You can lip-sync any video to any audio:
```bash
python inference.py --checkpoint_path <ckpt> --face <video.mp4> --audio <an-audio-source> 
```
Replace <ckpt> witht the path to the checkpoint downloaded.
Replace <video.mp4> with the path to the video file to be edited.
Replace <an-audio-source> with the path to the audio file.

The result is saved (by default) in `results/result_voice.mp4`. You can specify it as an argument,  similar to several other available options. The audio source can be any file supported by `FFMPEG` containing audio data: `*.wav`, `*.mp3` or even a video file, from which the code will automatically extract the audio.

Add `--pads` , `--nosmooth` , `--resize_factor` for better results.

A suggestion to run this command in terminal as the progess can be seen, which is not possible in jupyter notebook.

## Result
The Test dataset is [video](https://drive.google.com/file/d/14MITSafuVLFDyjfM153rXCITPuJNEFYA/view?usp=sharing) and [audio](https://drive.google.com/file/d/13Ck1RPsiWA5Bz8QQTjTLHWSeEm-qFAkv/view?usp=sharing)
The model was tested with Wav2Lip with no additional Arguements such as `--pads` , `--nosmooth` , `--resize_factor`

The first test is done with Wav2Lip model with no additional arguements such as `--pads` , `--nosmooth` , `--resize_factor`
The result is [here](https://drive.google.com/file/d/1jKvuEeMvhvOfSgAoJ2ljBLdagAW6Jpzw/view?usp=sharing)

The second test is done with Wave2Lip with arguements `--nosmooth` and `--pads 0 20 0 0`
The result is [here](https://drive.google.com/file/d/1y8L120L--X5Q9FOF5J-I8zduNZO93Vif/view?usp=sharing)

### References
 https://github.com/Rudrabha/Wav2Lip.git
 https://www.gyan.dev/ffmpeg/builds/
