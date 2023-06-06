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

- input

<img src="https://github.com/dldyou2/opensw23-E1I3/assets/60469410/51d424c2-2637-427a-8574-ae64778ac555" width="250px" height="250px">

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/fef9b4f3-bd34-4d94-91a8-8eb4d8d4eb4d

- output

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/b1030e12-4a91-484a-9368-e70adb69c002

# Analysis/Visualization

## Result Video의 완성도 판단 기준

1. 눈 : 눈 경계선 인식 및 눈동자의 방향
2. 입 : 입 경계선 인식 및 치아의 생성 여부
3. 전체 윤곽 : 전체적인 움직임과 원본 영상의 일치 정도 및 고개의 회전

### 1. 대상체의 크기에 따라 적용을 했을 때
---
- 이목구비만 보이게 확대한 이미지
   - `1-1.mp4`
      - 눈의 일부만 인식한 것처럼 보이며, 입의 경우 입 전체가 아닌 일부를 인식하여 입술 전체가 아닌 일부만 움직이는 모습을 보였다. 이목구비만 확대한 사진이었기에 머리의 움직임이 아닌 얼굴 내부 윤곽의 움직임을 보여주었다.
 - 원본보다 큰 이미지
   - `1-2.mp4` 
      - 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
 - 원본과 크기가 같은 이미지
   - `1-3.mp4`
      - 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
 - 원본보다 작은 이미지
   - `1-4.mp4`
      - 눈의 경계선은 인식하였으나, 눈동자가 자연스럽게 움직이지 않고 입의 경우 경계선 인식이 확실하게 이뤄지지 않았다. 치아 생성은 이뤄지지만 입이 확실하게 인식되지 못한 탓에 흐리게 생성된다. 전체 윤곽의 경우 돌려지는 느낌이 아닌 비율이 찌그러지는 느낌으로 영상이 생성됨.
      
 - 원본보다 매우 작은 이미지
   - `1-5.mp4`
      - 눈을 배경의 일부로 인식한 것으로 보이고, 눈동자의 움직임이 없다. 입의 경우 경계선 인식 자체를 하지 못하였으며 턱을 입술의 일부로 인식한듯한 결과를 도출하였다. 전체 윤곽 또한 1-3보다 더 부자연스러운 모습을 보였다.
      
---
### 2. 대상체의 위치에 따라 적용을 했을 때
---
- 중앙에 위치한 이미지
   - `2-1.mp4`
      - 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
- 좌측에 위치한 이미지
   - `2-2.mp4`
      - 눈과 입의 경계선을 확실하게 인식하나, 공간의 부족으로 왼쪽으로 고개가 이동 시 가장자리의 이미지가 찌그러지는 모습을 보임, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
- 우측에 위치한 이미지
   - `2-3.mp4`
      - 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
- 상단에 위치한 이미지
   - `2-4.mp4`
      - 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
- 눈 위쪽이 잘리도록 상단에 위치한 이미지
   - `2-5.mp4`
      -  `2-4.mp4` 까지 진행한 결과가 자연스러웠기에 극단적으로 상부로 이미지를 옮겨 다시 실행하였다. 눈동자의 움직임이 없는 것으로 보아 눈의 인식이 자연스레 이뤄지지 않았음을 알 수 있다. 입의 인식은 확실하게 이뤄졌으며 전체 윤곽의 움직임도 자연스럽다. 하지만 얼굴의 상부가 가장자리를 넘었을 때 이미지가 찌그러지는 모습을 보인다.

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
      - 좌측 상단에서 새 터미널을 열어줍니다..
      - 해당 터미널을 열어주었다면 해당 가상환경으로 진행이 가능합니다..
     
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
