# opensw23-E1I3

# Team Introduction

|  name  |    ID     | role |
| :----: | :-------: | :--: |
| 김채원 | 201910357 | 실험 계획 총괄 |
| 윤찬규 | 202211328 | (팀장) 모델 구동 총괄 |
| 임제형 | 202011356 | 보고서 총괄 |
| 황서진 | 202211404 | PPT 및 발표 총괄 |

# Topic Introduction

- repo source link
   https://github.com/AliaksandrSiarohin/first-order-model
  
### - Topic : Facial expression deepfake 기술에 적절한 타겟 이미지 유형 분석

   Facial Expression deepfake 기술이란, 타겟 이미지의 대상이 소스 비디오 대상의 얼굴 표정을 묘사하도록 만드는 기술입니다.
   
   ![image](https://github.com/dldyou2/opensw23-E1I3/assets/60469410/a9da5d50-bf8e-4d10-b9b2-511b16c35543)
   
### - 분석 기준

1. 대상
   - 대상의 크기 : 한 화면에 대상이 확대된 정도에 따라 어떻게 적용되는가.
   - 대상의 위치 : 한 화면에 대상의 위치에 따라 어떻게 적용되는가.
   - 대상의 종류 : 사람 뿐 아니라 이목구비를 가진 원숭이, 강아지, ... 등에도 적용되는가.
   
2. 이미지 조건
   - 눈 / 입 / 전체 윤곽이 적용이 잘 되었는가.

# Results

**20개**의 데이터를 돌려보았습니다.

> 데이터셋 구성 

1. 대상체의 크기에 따라
2. 대상체의 위치에 따라
3. 대상체의 종류에 따라 


아래의 결과는 해당 데이터 중 원본 크기 / 원본 위치 / 사람 -> 사람 에 해당하는 데이터로 가장 자연스러운 출력을 보여준 것입니다.

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/2346e3b9-64f8-4626-af35-3e9a55f6f4d3

# Analysis/Visualization

## Result Video의 완성도 판단 기준

1. 눈 : 눈 경계선 인식 및 눈동자의 방향
2. 입 : 입 경계선 인식 및 치아의 생성 여부
3. 전체 윤곽 : 전체적인 움직임과 원본 영상의 일치 정도 및 고개의 회전

### 1. 대상체의 크기에 따라 적용을 했을 때
---
https://github.com/dldyou2/opensw23-E1I3/assets/60469410/8b3f35b4-ebf8-4515-907b-54ab72aff88a

> 이목구비만 보이게 확대한 이미지

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/8424497a-dced-4509-af76-cf66fc29a88c

- 눈의 일부만 인식한 것처럼 보이며, 입의 경우 입 전체가 아닌 일부를 인식하여 입술 전체가 아닌 일부만 움직이는 모습을 보였다. 이목구비만 확대한 사진이었기에 머리의 움직임이 아닌 얼굴 내부 윤곽의 움직임을 보여주었다.



> 원본보다 큰 이미지

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/5a4b7a01-55bc-4d3b-b89c-5c3193c80c04

- 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
> 원본과 크기가 같은 이미지

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/5dfe8800-2b8f-4603-a65e-318081aade32

- 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
> 원본보다 작은 이미지

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/f83a715f-f0af-4446-ae61-57939f767931

- 눈의 경계선은 인식하였으나, 눈동자가 자연스럽게 움직이지 않고 입의 경우 경계선 인식이 확실하게 이뤄지지 않았다. 치아 생성은 이뤄지지만 입이 확실하게 인식되지 못한 탓에 흐리게 생성된다. 전체 윤곽의 경우 돌려지는 느낌이 아닌 비율이 찌그러지는 느낌으로 영상이 생성됨.
      
> 원본보다 매우 작은 이미지

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/d4105f5d-d201-43bf-b03e-d63b6187208b

- 눈을 배경의 일부로 인식한 것으로 보이고, 눈동자의 움직임이 없다. 입의 경우 경계선 인식 자체를 하지 못하였으며 턱을 입술의 일부로 인식한듯한 결과를 도출하였다. 전체 윤곽 또한 1-3보다 더 부자연스러운 모습을 보였다.

![1](https://github.com/dldyou2/opensw23-E1I3/assets/60469410/08a2cf32-43b5-4392-9eae-bd44704c491d)
`부위별 점수계를 합산한 총점을 10점으로 환산하였습니다.`

---
### 2. 대상체의 위치에 따라 적용을 했을 때
---
https://github.com/dldyou2/opensw23-E1I3/assets/60469410/f5d76561-810a-44df-9c8c-e392e96520a9

> 중앙에 위치한 이미지

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/741bbc54-7897-402a-b125-1dedcfad6407

- 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
> 좌측에 위치한 이미지

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/a457e0e9-1dfa-40a3-aec1-d6616944f92c

- 눈과 입의 경계선을 확실하게 인식하나, 공간의 부족으로 왼쪽으로 고개가 이동 시 가장자리의 이미지가 찌그러지는 모습을 보임, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
> 우측에 위치한 이미지

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/f6867d32-e93f-41cd-924e-fc6a5c0ea30d

- 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
> 상단에 위치한 이미지

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/9671556b-f348-4773-8a5c-0fd381620cd0

- 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
> 눈 위쪽이 잘리도록 상단에 위치한 이미지

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/7bf62aaf-eb9a-4174-a470-e060a204fc73

-  `2-4.mp4` 까지 진행한 결과가 자연스러웠기에 극단적으로 상부로 이미지를 옮겨 다시 실행하였다. 눈동자의 움직임이 없는 것으로 보아 눈의 인식이 자연스레 이뤄지지 않았음을 알 수 있다. 입의 인식은 확실하게 이뤄졌으며 전체 윤곽의 움직임도 자연스럽다. 하지만 얼굴의 상부가 가장자리를 넘었을 때 이미지가 찌그러지는 모습을 보인다.

![2](https://github.com/dldyou2/opensw23-E1I3/assets/60469410/e2dabe14-fe33-4a4e-a627-14b676ef8c32)
`부위별 점수계를 합산한 총점을 10점으로 환산하였습니다.`

---
### 3. 대상체의 종류에 따라
---
https://github.com/dldyou2/opensw23-E1I3/assets/60469410/6c121304-5418-4cc3-8dd8-8e85b49aa56e

> 사람 얼굴

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/c4478c65-57d5-4a4b-ae4b-5ebdf66e8753

- 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.
      
> 그림

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/d17319f6-ac11-4863-9b62-3d219d57491f

- 눈과 입의 경계선을 확실하게 인식, 치아 생성은 사람 얼굴로 하였을 때 보다 부자연스럽지만 생성이 확인되었으며 전체 윤곽의 움직임도 자연스럽다.
      
> 원숭이

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/504e1497-e177-417a-ac87-19f63f94ce90

- 눈과 입의 경계선을 확실하게 인식, 치아 생성도 자연스러우며 전체 윤곽의 움직임도 자연스럽다.

> 라마

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/f705c01f-400e-41b9-a586-8e182d252bcf

- 눈과 입의 경계선을 확실하게 인식, 치아 생성도 확인되었으며 전체 윤곽의 움직임도 자연스럽다.

> 강아지

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/c489916d-c145-4e0d-8a2c-9e71b22a4f70

- 눈과 입의 경계선을 인식한 것처럼 보이나, 입의 경우 코의 밑 부분까지 조금 넓게 인식한 모습을 보임, 전체 윤곽의 움직임은 자연스럽다.

> 가오리

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/660fa826-b9dd-497e-b552-815ffae2ccb4

- 형태적 특성 탓에 눈의 인식을 판별하기는 어려우며, 입은 확실히 인식한 모습을 보인다.

![3](https://github.com/dldyou2/opensw23-E1I3/assets/60469410/e2021b3a-d798-4059-ae02-f8ba55348378)
`부위별 점수계를 합산한 총점을 10점으로 환산하였습니다.`

`동물 특성상 흰자가 보이지 않아 눈동자의 움직임을 확인할 수 없습니다. 따라서 눈은 눈꺼풀의 움직임을 4점(0,2,4)으로 환산하여, 눈 점수의 가중치를 유지시켰습니다.`

---
### 4. 결론
---
> 적용이 잘 되는 이미지 특성
- 이목구비와 전체 윤곽의 경계선을 기준으로 안팎의 명도가 크게 차이 나는 경우
   - 눈 : 눈을 인식 할 때, 눈의 흰자와 눈동자의 경계선을 통해 인식이 될 것이라 예상. 그러나 흰자가 없어도 눈동자의 명확도가 눈 인식에 더 큰 영향을 미친다.

> 적용이 잘 안되는 이미지 특성
- 이목구비가 인식되지 않는 경우
   - 입과 비슷한 위치에 유사한 음영을 가진 영역이 있을 경우, 해당 영역을 입으로 인식할 가능성이 있다.
   - 이미지 내에서 대상의 크기가 원본보다 확연히 작을 경우 원본 영상에서 입이 있었던 공간에 음영이 다른 부분이 존재한다면 그것을 입이라고 인식하는 모습을 보인다.

> 결과물이 자연스럽지 않은 경우
   - 입 안 그림자 생성이 부자연스럽게 되는 경우
      - source image에 이빨이 있는 경우, 본 기술에서는 이빨을 분리하여 인식하지 못하는 것으로 보인다. 따라서 입 안 그림자가 부자연스럽게 표현됨.
      - `살짝 열린 입, 검은 그림자` > `닫힌 입` > `살짝 열린 입, 검은 그림자, 이빨` > `열린 입, 이빨`
         
   - 가장자리로 이미지가 편향된 경우 생성된 이미지가 자연스럽게 가장자리 경계를 빠져나가는 것이 아닌 내부에서 찌그러진 형태로 이미지를 생성하는 모습을 보인다.

---
# Installation

![image](https://github.com/dldyou2/opensw23-E1I3/assets/60469410/85c8ae8d-3fa2-482f-93c2-9de959cbf010)

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
   python demo.py --config ./config/vox-256.yaml --driving_video dataSet/src.mp4 --source_image dataSet/1-3.png --checkpoint ./vox-cpk.pth.tar --relative --adapt_scale --cpu
   ```

   전달한 argument들의 의미는 아래와 같습니다. 사용 목적에 따라 변경하여 사용합니다.

   - --config : 적용할 yaml파일 주소
   - --source_image : 소스 이미지 파일 주소
   - --driving_video : 소스 동영상 파일 주소
   - --checkpoint : pretrained data인 tar파일 주소
   - --cpu : GPU 미사용시 호출하는 명령어 ( 아래 사진의 오류 발생 시 해결가능 )
   ![ErrorImg](https://github.com/dldyou2/opensw23-E1I3/blob/f8717260b81905717e92017534bc65b13ce9780d/errorImg.png)
   
   **GPU 사용 원할 시 (NVIDIA) `GPU.pdf` 파일 참고**
   
6. result 파일

   만들어진 동영상은 argument를 따로 전달하지 않을 시 최상위 폴더에 `result.mp4` 파일이 생성되며, 명령어에 --result_video dataSet/result.mp4 와 같이 추가 인자를 전달 시 생성될 파일위치 지정 및 이름 설정이 가능합니다.

# Presentation
