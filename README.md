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

![result](https://github.com/dldyou2/opensw23-E1I3/assets/76515856/fa7893d7-46bf-436b-adac-46b33d556fe0)
![]

# Analysis/Visualization

# Installation

[테스트 환경]
OS : window
python 버전: python3.10.9

[깃허브 주소 및 초기 모듈 설정]
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

[YAML configs 확인]
first-order-model 중에서도 이용하는 주제에 따라 사용해야하는 yaml파일이 달라짐
![YamlListImg][./image/yamlListImg.png]
E1I3에서는 Facial Expression을 구동하기에 dataset중에서도 vox-256.yaml 파일을 config파일로 지정함

[pretrained data(tar파일) 다운로드]
https://drive.google.com/drive/folders/1PyQJmkdCsAkOYwUyaj_l-l0as-iLDgeH (vox-cpk.pth.tar 다운로드 받기)
위 링크에서 pretrained data인 tar파일을 다운로드 하여 이용함

[dataSet 설정]
소스 이미지와 기반이 될 비디오 파일을 적용하기 위하여
클론한 최상위 폴더에 dataSet이라는 이름의 폴더를 만들고 그 안에 사용할 png, mp4 선정하여 저장

[명령어 수정]
repository 권장 기본 입력코드 ->
python demo.py --config config/dataset_name.yaml --driving_video path/to/driving --source_image path/to/source --checkpoint path/to/checkpoint --relative --adapt_scale

Day2 초기 result를 얻기 위한 입력코드 ->
python demo.py --config .\config\bair-256.yaml --driving_video dataSet\04.mp4 --source_image dataSet\01.png --checkpoint .\bair-cpk.pth.tar --relative --adapt_scale --cpu

기존 명령어 뒤에 —cpu를 추가해야함. >> 아래의 오류를 —cpu로 해결함
![errorImg][./image/errorImg.png]
—cpu : GPU가 NVIDIA가 아닌 경우 필요.

# Presentation
