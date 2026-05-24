# Implementing an OpenCV-Based Drowsiness Detection Device Using Raspberry Pi

OpenCV로 얼굴과 눈을 실시간 감지하여 눈이 감기면 부저로 경보음을 울리는 졸음방지 IoT 디바이스 프로젝트입니다.

## 🎬 데모 영상

[![Demo Video](https://img.youtube.com/vi/x5WMLfPlDnk/0.jpg)](https://www.youtube.com/shorts/x5WMLfPlDnk)

## 📌 프로젝트 개요

- OpenCV Haar Cascade로 웹캠에서 얼굴·눈 실시간 감지
- 눈 1개 이하 감지 → 졸음 상태 판단 → 부저 경보음 작동
- 눈 2개 이상 감지 → 정상 상태 → 부저 꺼짐

## 🛠️ 사용 기술

| 항목 | 내용 |
|---|---|
| Language | Python 3.x |
| Library | OpenCV (cv2), gpiozero, time |
| Algorithm | Haar Cascade Face/Eye Detection |
| Hardware | Raspberry Pi, 웹캠, 능동부저 |

## 📂 파일 구성

```
project_34/
├── main34.py       # 얼굴·눈 인식 시각화 (부저 없음)
└── main34-1.py     # 눈 감지 시 부저 경보음 최종 코드
```

## 🔌 회로 연결

| 부품 | GPIO 핀 |
|---|---|
| 능동부저 (+) 핀 | GPIO 16 |
| 능동부저 (-) 핀 | GND |

## 🚀 실행 방법

```bash
# Section 13 가상환경 활성화
source {가상환경이름}/bin/activate
cd myProjects/project_34

# gpiozero 설치
pip install gpiozero

# 얼굴·눈 인식 시각화 확인
python main34.py

# 졸음방지 최종 실행
python main34-1.py
```

## 📚 참고문헌

- [OpenCV Documentation](https://docs.opencv.org/)
- [Cascade Classifier - Object Detection](https://docs.opencv.org/4.x/db/d28/tutorial_cascade_classifier.html)
- [GPIO Zero Documentation](https://gpiozero.readthedocs.io/)
- [Active Buzzer Module](https://components101.com/misc/buzzer-pinout-working-datasheet)
