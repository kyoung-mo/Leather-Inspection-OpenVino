[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://inspection-app-kooyoungmo.streamlit.app)

# 🔍 가죽 이상 탐지 앱 (Leather Inspection App)

VGG16 전이학습 모델(.keras)을 활용한 가죽 표면 불량 탐지 웹 앱입니다.  
Streamlit으로 UI를 구성하고, Streamlit Cloud에 배포합니다.

<img width="1180" height="655" alt="image" src="https://github.com/user-attachments/assets/54b4539b-7c64-438d-885e-a2d55b80dac2" />

---

## ✨ 주요 기능

- 🖼️ 이미지 파일 업로드 또는 📷 카메라 촬영으로 가죽 표면 검사
- ✅ 정상 / ❌ 불량 판정 및 확률 출력
- VGG16 기반 전이학습 모델 (.keras 포맷) 사용

---

## 📁 프로젝트 구조

```
inspection-app/
├── app_keras.py          # Streamlit 메인 앱
├── requirements.txt      # Python 패키지 목록
├── packages.txt          # 시스템 패키지 목록
├── .python-version       # Python 버전 고정 (3.11)
├── .gitignore
├── .gitattributes        # Git LFS 설정 (*.keras)
└── weights/
    └── leather_model.keras   # 학습된 모델 파일 (Git LFS)
```

---

## 🚀 실행 방법 (로컬)

```bash
# 가상환경 활성화
.venv\Scripts\activate  # Windows

# 패키지 설치
pip install -r requirements.txt

# 앱 실행
streamlit run app_keras.py
```

---

## ☁️ 배포

Streamlit Cloud (share.streamlit.io) 에 배포됩니다.  
GitHub repo 변경 시 자동으로 재빌드됩니다.

- Python: 3.11
- 모델 파일: Git LFS로 관리

---

## 🧠 모델 정보

| 항목 | 내용 |
|------|------|
| 베이스 모델 | VGG16 (ImageNet 전이학습) |
| 입력 크기 | 224 × 224 |
| 출력 | 불량 확률 (sigmoid) |
| 판정 임계값 | 0.5 |
| 포맷 | TensorFlow `.keras` |
