# DoRo_HackaThon

## :heavy_check_mark: 제출자 : 도원결의 (김건희, 김지은, 오형석, 이현진, 임다현, 최진규) 

## :heavy_check_mark: 참가분야 : 도로 시설물 양호/불량 데이터 이상 탐지/분류 프로그램 개발

---

**모두 Colab환경에서 진행**

#### <모델 구조>

Image Input > 30class 구분 (YoLov5) : 시설물 탐지 -> Class 별 불량/양호 분류 (EfficentNet) --> 불량 판정시 불량부분 탐지 (YoLov5) -> 결과 .txt 파일 산출

---

<학습 데이터셋>
도로시설물 데이터 (F1 soft 제공)



<제출 파일>
doro_contest
└ 이미지 전처리.ipynb(학습을 위해 사용했던 전처리 코드)
└ road (이미지 전처리 및 불량_양호 판별(EfficientNet) train dataset )

└ 시설물 인식.ipynb(학습을 위해 사용했던 코드)
└ image_labels (labels)
└ dataset (yolOv5 trained pt - 시설물 탐지 train에 사용)
└ best64_180.pt (yolo trained pt)
└ data.yaml(yolo class)

└ 불량_양호 판별.ipynb(학습을 위해 사용했던 코드)
└ Model (EfficientNet trained pt)

└ 불량부분 판별.ipynb(학습을 위해 사용했던 코드)
└ part_dataset (yolo v5 train dataset - 불량 부분 탐지)
└ yolov5 (yolo v5 +yolo trained pt - 불량부분 탐지 내용)

└ Inference.ipynb(inference code)
└ test_input(test할 데이터가 들어갈 폴더)
└ test_output (inference txt파일이 저장될 폴더)
└ test_summary 

<구동 방법>

1. Inference.ipynb 파일을 열기
2. 필요 라이브러리 설치 (필요하다면)
3. 구동 전 doro_contest 가 있는 파일의 경로를 입력해주세요.
4. 실행

