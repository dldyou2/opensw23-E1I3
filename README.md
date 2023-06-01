# opensw23

# Team Introduction

|  name  |    ID     | role |
| :----: | :-------: | :--: |
| 김채원 | 201910357 |  -   |
| 윤찬규 | 202211328 |  -   |
| 임제형 | 202011356 |  -   |
| 황서진 | 202211404 |  -   |

# Topic Introduction

# Results

# Analysis/Visualization

# Installation

[테스트 환경]
OS : window
python 버전: python3.10.9

깃허브 주소 및 초기 설정
git clone https://github.com/AliaksandrSiarohin/first-order-model.git
pip install -r requirements.txt
pip install ffmpeg-python
pip install PyYAML==5.3.1

pip install torch
pip install torchvision

pip3 install -U scikit-learn
pip install ffmpeg
pip install pandas
pip install matplotlib
pip install imageio-ffmpeg

YAML configs 확인

first-order-model 중에서도 이용하는 주제에 따라 사용해야하는 yaml파일이 달라짐

E1I3에서는 Facial Expression을 구동하기에 dataset중에서도 vox-256.yaml 파일을 config파일로 지정함

https://drive.google.com/drive/folders/1PyQJmkdCsAkOYwUyaj_l-l0as-iLDgeH (vox-cpk.pth.tar 다운로드 받기)
위 링크에서 pretrained data인 tar파일을 다운로드 하여 이용함

소스 이미지와 기반이 될 비디오 파일을 적용하기 위하여
클론한 최상위 폴더에 dataSet이라는 이름의 폴더를 만들고 그 안에 사용할 png, mp4 선정하여 저장

https://drive.google.com/drive/folders/1PyQJmkdCsAkOYwUyaj_l-l0as-iLDgeH (vox-cpk.pth.tar 다운로드 받기)

# Presentation
