# opensw23-E1I3

# Team Introduction

|  name  |    ID     | role |
| :----: | :-------: | :--: |
| 김채원 | 201910357 |  -   |
| 윤찬규 | 202211328 |  -   |
| 임제형 | 202011356 |  -   |
| 황서진 | 202211404 |  -   |

# Topic Introduction

- repo source link
   https://github.com/AliaksandrSiarohin/first-order-model
  
### - Topic : Facial expression deepfake 기술에 적절한 타켓 이미지 유형 분석

   Facial Expression deepfake 기술이란, 타겟 이미지의 대상을 소스 비디오 대상의 표정을 묘사하도록 만드는 기술입니다.
   
### - 분석 기준

1. 대상
   - 대상의 종류 : 사람 뿐 아니라 이목구비를 가진 강아지, 고양이, 새 등에도 적용되는가.
   - 대상의 수 : 한 화면에 대상의 수가 많아도, 모든 대상의 얼굴에 기술이 적용되는가.
   - 이목구비 가림 정도 : 눈, 코, 입과 같은 부분을 가려도 기술이 적용되는가.
   
2. 이미지 조건
   - 채도 : 이목구비를 인식하는 데, 채도가 영향을 미치는가.
   - 방향 : 대상이 회전되어 있어도, 이목구비를 잘 인식하는가.

# Results

원본이미지의 초기이미지와 가장 비슷한 구성의 사람 얼굴 이미지로 도출한 결과이다.
가장 자연스러운 출력을 보여주었기에 아래의 Analysis 및 Visualization에서 기준으로 삼았다.

- input

<img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/6db3f7fd-a596-4a32-9b65-49623754519b" width="250px" height="250px">

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/6620078d-d2ba-48dc-a1e9-d411bfcdbe1e

- output

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/7c8a9026-1d59-43a5-88b8-876d1a4f93a6

# Analysis/Visualization

## Result Video의 완성도 판단 기준

1. 눈 : 눈 경계선 인식 및 눈동자의 방향
2. 입 : 입 경계선 인식 및 치아의 생성 여부
3. 전체 윤곽 : 전체적인 움직임과 원본 영상의 일치 정도 및 고개의 회전

### 1. 대상체의 크기에 따라 적용을 했을 때
---
- 이목구비만 보이게 확대한 이미지
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/cf84f91f-cef0-4b89-b6ea-c3a7a1c0727a" width="250px" height="250px">

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/459457f3-7fea-4c5a-aafd-6b8aa5558599
   
      - 눈의 일부만 인식한 것처럼 보이며, 입의 경우 입 전체가 아닌 일부를 인식하여 입술 전체가 아닌 일부만 움직이는 모습을 보였다. 이목구비만 확대한 사진이었기에 머리의 움직임이 아닌 얼굴 내부 윤곽의 움직임을 보여주었다.
 - 원본보다 큰 이미지
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/37e9fe15-f9cd-45a3-a3ad-b53aa66f12d0" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/6002394c-a992-4454-acb6-07118e02ee33

      - 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
 - 원본과 크기가 같은 이미지
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/5f600dac-8d4b-4ccd-bcfd-9400a398f95a" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/4b939934-cd9c-4c66-a4f6-e6c591ec5a26

      - 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
 - 원본보다 작은 이미지
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/c52b88f1-5eae-43d0-a4f7-94f721721db0" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/e59cd6dc-81a0-4c0f-9cc6-63ce5ea34bc6

      - 눈의 경계선은 인식하였으나, 눈동자가 자연스럽게 움직이지 않고 입의 경우 경계선 인식이 확실하게 이뤄지지 않았다. 치아 생성은 이뤄지지만 입이 확실하게 인식되지 못한 탓에 흐리게 생성된다. 전체 윤곽의 경우 돌려지는 느낌이 아닌 비율이 찌그러지는 느낌으로 영상이 생성됨.
      
 - 원본보다 매우 작은 이미지
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/581a47e4-0e76-443a-aea0-22c8da1de717" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/0aa899a5-6700-44d1-ba0c-1956e2f4e186

      - 눈을 배경의 일부로 인식한 것으로 보이고, 눈동자의 움직임이 없다. 입의 경우 경계선 인식 자체를 하지 못하였으며 턱을 입술의 일부로 인식한듯한 결과를 도출하였다. 전체 윤곽 또한 1-3보다 더 부자연스러운 모습을 보였다.
      
---
### 2. 대상체의 위치에 따라 적용을 했을 때
---
- 중앙에 위치한 이미지
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/ae7b3e33-6a50-46d4-83d7-2a8123b225bf" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/c04ab952-f1cd-4f89-9236-5a7674c59155
   
      - 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
- 좌측에 위치한 이미지
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/daa0eb42-0ca3-43b9-9cb6-31e7f01304c1" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/9e87eccd-6b88-4e6e-baf2-cfb763309c4d

      - 눈과 입의 경계선을 확실하게 인식하나, 공간의 부족으로 왼쪽으로 고개가 이동 시 가장자리의 이미지가 찌그러지는 모습을 보임, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
- 우측에 위치한 이미지
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/b299c67d-6268-4ba8-8cfb-8b55f473e31a" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/b13efbeb-39f6-43c5-af66-1ab7f0b54aec

      - 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
- 상단에 위치한 이미지
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/7460502a-8dba-4c66-8452-f7d50821cae9" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/3da85f93-5f10-4a3d-92c7-4b6f33a195af

      - 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
- 눈 위쪽이 잘리도록 상단에 위치한 이미지
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/871b26ef-1930-4713-acca-8503f39e2ac0" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/ffe95a28-7e8c-4aa8-b9fc-11dc4f18d425

      -  `2-4.mp4` 까지 진행한 결과가 자연스러웠기에 극단적으로 상부로 이미지를 옮겨 다시 실행하였다. 눈동자의 움직임이 없는 것으로 보아 눈의 인식이 자연스레 이뤄지지 않았음을 알 수 있다. 입의 인식은 확실하게 이뤄졌으며 전체 윤곽의 움직임도 자연스럽다. 하지만 얼굴의 상부가 가장자리를 넘었을 때 이미지가 찌그러지는 모습을 보인다.

---
### 3. 대상체의 종류에 따라
---
- 사람 얼굴
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/33577ea7-d8f1-4e18-bbc6-8cf10c185be8" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/363ec8e8-39c3-4df1-94fa-3f5384c4765f

      - 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
- 그림
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/2b7bf78f-3a34-4945-a8e5-12c49a7d9689" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/1e2fa076-2c2b-4994-80dc-c1e002c47675

      - 눈과 입의 경계선을 확실하게 인식, 치아 생성은 사람 얼굴로 하였을 때 보다 부자연스럽지만 생성이 확인되었으며 전체 윤곽의 움직임도 자연스럽다.
      
- 원숭이
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/fbd745c2-7824-4db5-af59-cd89d74ac334" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/74113210-744a-4b55-8df3-0f13c0ed1ea7

      - 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.

- 라마
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/cab0006f-afc5-4038-a635-7bfec7e2274a" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/5de744bc-be51-46a8-9652-d7271e213209

      - 눈과 입의 경계선을 확실하게 인식, 치아 생성도 확인되었으며 전체 윤곽의 움직임도 자연스럽다.

- 강아지
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/90fe0587-7b2e-41cc-8595-36941204a197" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/3c31cf89-d3dc-4913-9600-87180be93bf6

      - 눈과 입의 경계선을 인식한 것처럼 보이나, 입의 경우 코의 밑 부분까지 조금 넓게 인식한 모습을 보임, 전체 윤곽의 움직임은 자연스럽다.

- 가오리
   - <img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/cd26576c-884d-4052-ab0c-8c1ba030b146" width="250px" height="250px"> 

   - https://github.com/dldyou2/opensw23-E1I3/assets/60469410/fa530adf-d161-4397-9d50-e3334cd77904

      - 형태적 특성 탓에 눈의 인식을 판별하기는 어려우며, 입은 확실히 인식한 모습을 보인다.
---
### 4. 결론
---
- 적용이 잘 되는 이미지 특성
   - 이목구비와 전체 윤곽의 경계선을 기준으로 안팎의 명도가 크게 차이 나는 경우
      - 눈 : 눈을 인식 할 때, 눈의 흰자와 눈동자의 경계선을 통해 인식이 될 것이라 예상. 그러나 흰자가 없어도 눈동자의 명확도가 눈 인식에 더 큰 영향을 미친다.

- 적용이 잘 안되는 이미지 특성
   - 이목구비가 인식되지 않는 경우
      - 입과 비슷한 위치에 유사한 음영을 가진 영역이 있을 경우, 해당 영역을 입으로 인식할 가능성이 있다.
      - 이미지 내에서 대상의 크기가 원본보다 확연히 작을 경우 원본 영상에서 입이 있었던 공간에 음영이 다른 부분이 존재한다면 그것을 입이라고 인식하는 모습을 보인다.

   - 결과물이 자연스럽지 않은 경우
      - 입 안 그림자 생성이 부자연스럽게 되는 경우
         - source image에 이빨이 있는 경우, 본 기술에서는 이빨을 분리하여 인식하지 못하는 것으로 보인다. 따라서 입 안 그림자가 부자연스럽게 표현됨.
         - `살짝 열린 입, 검은 그림자` > `닫힌 입` > `살짝 열린 입, 검은 그림자, 이빨` > `열린 입, 이빨`
         
      - 가장자리로 이미지가 편향된 경우 생성된 이미지가 자연스럽게 가장자리 경계를 빠져나가는 것이 아닌 내부에서 찌그러진 형태로 이미지를 생성하는 모습을 보인다.

---
# Installation

### [테스트 환경]
- OS : window
- python 버전: python 3.9.16 / 3.10.9
- code editor : visual studio code
- virtual environment : anaconda

### [설치]
1. 깃허브 주소 및 초기 설정
   opensw23-E1I3 repository를 clone한 뒤, 필요한 python 모듈을 다운합니다. 가상 환경 활성화 후 실행을 권장합니다. 이하 clone한 폴더를 `root` 폴더라고 지칭합니다.
   ```
   git clone https://github.com/dldyou2/opensw23-E1I3.git
   ```
2. (권장) 가상 환경 구성
   안전한 개발 환경 구축을 위해 가상 환경을 구성합니다. 
   - venv로 진행 시
   아래 코드를 cmd에서 작성합니다.
   ```
   python -m venv .venv
   call .venv/Scripts/activate -> Scripts 가 아니라 bin으로 되어 있는 경우도 있음 (주의)
   ```
   - anaconda로 진행 시
      - anaconda prompt를 실행합니다. base에서 실행을 할 예정이기에 `conda clean -a` 명령어로 기존에 다운 받았던 패키지들을 초기화 시켜주는 작업부터 진행합니다. 
      - visual studio code에 들어가서 demo.py 파일을 열어줍니다.
      - 우측 하단의 파이썬 인터프리터를 anaconda base로 설정해줍니다. 파이썬 버전이 다르다면 anaconda navigation에서 environment 에서 base를 클릭 후 우측에서 파이썬 버전을 바꾸어줍니다.
      - 좌측 상단에서 새 터미널을 열어줍니다.
      - 해당 터미널을 열어주었다면 해당 가상환경으로 진행이 가능합니다.
     
   `pip install -r requirements.txt` 명령어를 통해 해당 가상 환경에 라이브러리를 설치해줍니다.
3. YAML configs 확인

   E1I3에서 초기에 clone한 first-order-model 에서는 여러가지의 기능 구현을 위해 다양한 yaml파일이 존재합니다. 하지만, 그중에서도 Facial Expression deepfake을 구현하고자 하기에 **vox-256.yaml** 파일을 사용합니다. 모든 yaml파일은 ./config 에서 확인할 수 있습니다.
   
   ![YamlListImg](https://github.com/dldyou2/opensw23-E1I3/blob/f8717260b81905717e92017534bc65b13ce9780d/yamlListImg.png)
   
4. tar 파일 다운로드

   아래 링크에서 pretrained data인 tar파일을 `root` 폴더 아래에 다운로드합니다.
   https://drive.google.com/drive/folders/1PyQJmkdCsAkOYwUyaj_l-l0as-iLDgeH (`vox-cpk.pth.tar` 다운로드 받기)
   
4. Data Set 수집

   소스 이미지와 기반이 될 비디오 파일을 수집합니다.
   원활한 파일 관리를 위하여 `root` 폴더에 dataSet이라는 이름의 폴더를 생성하고 해당 폴더에 사용할 png, mp4 파일을 저장합니다. 
   추가적으로 소스파일이 필요한 경우 아래 링크에서 다운로드 가능합니다.  
   https://drive.google.com/drive/folders/1TIjufuJdPgkzvCQ3G1mICQZVCxWbCOFX
   
5. 명령어

   terminal에서 아래의 명령어를 전달합니다.
   ```
   python demo.py --config ./config/vox-256.yaml --driving_video dataSet/04.mp4 --source_image dataSet/01.png --checkpoint ./vox-cpk.pth.tar --relative --adapt_scale --cpu
   ```

   전달한 argument들의 의미는 아래와 같습니다. 사용 목적에 따라 변경하여 사용합니다.

   - --config : 적용할 yaml파일 주소
   - --source_image : 소스 이미지 파일 주소
   - --driving_video : 소스 동영상 파일 주소
   - --checkpoint : pretrained data인 tar파일 주소
   - --cpu : GPU 미사용시 호출하는 명령어 ( 아래 사진의 오류 발생 시 해결가능 )  
   ![ErrorImg](https://github.com/dldyou2/opensw23-E1I3/blob/f8717260b81905717e92017534bc65b13ce9780d/errorImg.png)
   
6. result 파일

   만들어진 동영상은 argument를 따로 전달하지 않을 시 최상위 폴더에 `result.mp4` 파일이 생성되며, 명령어에 --result_video ./dataSet/result.mp4 와 같이 추가 인자를 전달 시 생성될 파일위치 지정 및 이름 설정이 가능합니다.

# Presentation
