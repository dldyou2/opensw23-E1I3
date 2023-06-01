# opensw23

# Team Introduction

|  name  |    ID     | role |
| :----: | :-------: | :--: |
| 김채원 | 201910357 |  -   |
| 윤찬규 | 202211328 |  -   |
| 임제형 | 202011356 |  -   |
| 황서진 | 202211404 |  -   |

# Topic Introduction
- Topic : facial expression 기술에 적절한 타켓 이미지 유형 분석
  Facial Expression 기술이란, 타겟 이미지의 대상을 소스 비디오 대상의 표정을 묘사하도록 만드는 기술이다.
- 분석 기준
1. 대상
    - 대상의 종류
      사람 뿐 아니라 이목구비를 가진 강아지, 고양이, 새 등에도 적용되는가.
    - 대상의 수
      한 화면에 대상의 수가 많아도, 모든 대상의 얼굴에 기술이 적용되는가.
    - 이목구비 가림 정도
      이목구비를 가려도 적용되는가.
      
2. 이미지 조건
    - 채도
      이목구비를 인식하는 데, 채도가 영향을 미치는가.
    - 방향
      대상이 회전되어 있어도, 이목구비를 잘 인식하는가.
      
# Results
input

![face1](https://github.com/dldyou2/opensw23-E1I3/assets/76515856/e67187ef-fb41-48c5-9770-c89ac91fe319)
![movie](https://github.com/dldyou2/opensw23-E1I3/assets/76515856/72d54b9f-8ae6-4bdc-aaa2-2e31eeb4ceab)


output
![result](https://github.com/dldyou2/opensw23-E1I3/assets/76515856/fa7893d7-46bf-436b-adac-46b33d556fe0)

# Analysis/Visualization

# Installation

[테스트 환경]
OS : window
python 버전: python3.10.9
code editor : visual studio code

[설치]
1. 깃허브 주소 및 초기 설정
first-order-model repository를 clone한 뒤, 필요한 python 모듈을 다운합니다. 가상 환경 활성화 후 실행을 권장합니다. 
'''
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
'''
2. YAML configs 확인
first-order-model 중에서도 이용하는 주제에 따라 사용해야하는 yaml파일이 달라집니다.
  > ... 용도의 yaml, ... 용도의 yaml 파일이 있습니다. 
E1I3에서는 Facial Expression을 구동하기에 dataset중에서도 **vox-256.yaml** 파일을 config파일로 지정합니다. (--config .\config\vox-256.yaml)

3. 
https://drive.google.com/drive/folders/1PyQJmkdCsAkOYwUyaj_l-l0as-iLDgeH (vox-cpk.pth.tar 다운로드 받기)
위 링크에서 pretrained data인 tar파일을 다운로드 하여 이용함

4. Data Set 수집
소스 이미지와 기반이 될 비디오 파일을 적용하기 위하여
클론한 최상위 폴더에 dataSet이라는 이름의 폴더를 만들고 그 안에 사용할 png, mp4 선정하여 저장

5. 명령어 
전달 가능한 argument로는 --- 이 있습니다. 


# Presentation
