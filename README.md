# opensw23

# Team Introduction

|  name  |    ID     | role |
| :----: | :-------: | :--: |
| 김채원 | 201910357 |  -   |
| 윤찬규 | 202211328 |  -   |
| 임제형 | 202011356 |  -   |
| 황서진 | 202211404 |  -   |

# Topic Introduction

### - Topic : Facial expression deepfake 기술에 적절한 타켓 이미지 유형 분석<br/>
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

![face](https://github.com/dldyou2/opensw23-E1I3/assets/60469410/51d424c2-2637-427a-8574-ae64778ac555)

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/fef9b4f3-bd34-4d94-91a8-8eb4d8d4eb4d

- output

https://github.com/dldyou2/opensw23-E1I3/assets/60469410/b1030e12-4a91-484a-9368-e70adb69c002

# Analysis/Visualization

# Installation

### [테스트 환경]

- OS : window
- python 버전: python3.10.9
- code editor : visual studio code

### [설치]
   
1. 깃허브 주소 및 초기 설정
   opensw23-E1I3 repository를 clone한 뒤, 필요한 python 모듈을 다운합니다. 가상 환경 활성화 후 실행을 권장합니다. 이하 clone한 폴더를 최상위 폴더라고 지칭합니다.

<pre>
<code>

  git clone https://github.com/dldyou2/opensw23-E1I3.git

</code>
</pre>


2. (권장) 가상 환경 구성
   안전한 개발 환경 구축을 위해 가상 환경을 구성합니다. 아래 코드를 cmd에서 작성해주세요.
   '''
   
   python -m venv .venv
   call .venv/Scripts/activate -> Scripts 가 아니라 bin으로 되어 있는 경우도 있음 (주의)
   
   해당 가상 환경에 라이브러리를 설치해줍니다.
   pip install -r requirements.txt
   
   '''
   
3. YAML configs 확인

   first-order-model 중에서도 이용하는 주제에 따라 사용해야하는 yaml파일이 달라집니다.  
   ![YamlListImg](https://github.com/dldyou2/opensw23-E1I3/blob/f8717260b81905717e92017534bc65b13ce9780d/yamlListImg.png)

   E1I3에서는 Facial Expression Deepfake을 구동하기에 **vox-256.yaml** 파일을 사용합니다. 모든 yaml파일은 .\config 에서 확인할 수 있습니다.

4. tar 파일 다운로드

   아래 링크에서 pretrained data인 tar파일을 다운로드합니다.
   https://drive.google.com/drive/folders/1PyQJmkdCsAkOYwUyaj_l-l0as-iLDgeH (vox-cpk.pth.tar 다운로드 받기)
   다운로드한 tar 파일은 최상위 폴더에 저장합니다.

4. Data Set 수집

   소스 이미지와 기반이 될 비디오 파일을 수집합니다.
   원활한 파일 관리를 위하여 클론한 최상위 폴더에 dataSet이라는 이름의 폴더를 만들고 그 안에 사용할 png, mp4 선정하여 저장합니다.  
   추가적으로 소스파일이 필요한 경우 아래 링크에서 다운로드 가능합니다.  
   https://drive.google.com/drive/folders/1TIjufuJdPgkzvCQ3G1mICQZVCxWbCOFX

5. 명령어

   terminal에서 아래의 명령어를 전달합니다.
   <pre>
   <code>
   python demo.py --config .\config\vox-256.yaml --driving_video dataSet\04.mp4 --source_image dataSet\01.png --checkpoint .\vox-cpk.pth.tar --relative --adapt_scale --cpu
   </code>
   </pre>

전달한 argument들의 의미는 아래와 같습니다. 사용 목적에 따라 변경하여 사용합니다.

- --config : 적용할 yaml파일 주소
- --source_image : 소스 이미지 파일 주소
- --driving_video : 소스 동영상 파일 주소
- --checkpoint : pretrained data인 tar파일 주소
- --cpu : GPU 미사용시 호출하는 명령어 ( 아래 사진의 오류 발생 시 해결가능 )  
  ![ErrorImg](https://github.com/dldyou2/opensw23-E1I3/blob/f8717260b81905717e92017534bc65b13ce9780d/errorImg.png)

6. result 파일

만들어진 동영상은 argument를 따로 전달하지 않을 시 최상위 폴더에 생성되며, 명령어에 --result_video ./dataSet/result.mp4 를 추가하여 인자를 전달 시 생성될 파일위치 지정 및 이름 설정이 가능합니다.

# Presentation
