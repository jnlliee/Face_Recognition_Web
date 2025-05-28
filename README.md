# 🧠 안면 인식 웹 애플리케이션 (Face Recognition Web App)

이 프로젝트는 FastAPI, React, MediaPipe, OpenCV를 활용한 **웹 기반 안면 인식 시스템**입니다.  
사용자는 웹 브라우저를 통해 얼굴을 등록하고, 실시간으로 인식 결과를 확인할 수 있습니다.

---

## 📦 Requirements (실행 환경 및 의존성)

아래 패키지가 필요합니다:

```bash
fastapi
uvicorn
pyngrok
opencv-python-headless
mediapipe
pillow
numpy
python-multipart
```

## ▶️ How to Run (실행 방법)

1. `app.py`, `index.html`, `run_server.py` 파일을 준비합니다.
2. 다음 디렉토리들을 생성합니다:
   - `www` → 프론트엔드 UI (React, HTML)
   - `uploads` → 업로드된 이미지 저장소 (자동 생성)
   - `registered_faces` → 등록된 얼굴 벡터 저장소

3. 서버 실행:
```
python run_server.py
```


4. 실행 후 출력되는 `ngrok` 공개 주소를 복사하여 웹 브라우저에 입력하면 애플리케이션이 실행됩니다.

---

## 🔧 기능 설명

- 실시간 웹캠 스트리밍
- 얼굴 등록 (이름과 함께 저장)
- 얼굴 인식 (유사도 비교 기반)
- 등록된 얼굴과 비교하여 인식 여부 판단
- 인식된 얼굴 위치 표시 및 신뢰도 시각화
- React 기반 직관적인 사용자 인터페이스

---

## 🧪 기술 스택

- **Frontend**: React (CDN), Babel, HTML, CSS
- **Backend**: FastAPI, Python
- **AI/인식 처리**: MediaPipe (FaceMesh, FaceDetection), OpenCV
- **Storage**: Pickle 파일을 활용한 로컬 벡터 저장
- **배포**: ngrok + uvicorn (로컬 or Colab 환경)

---

## 📁 프로젝트 폴더 구조 예시
```
face-recognition-app/
├── app.py
├── run_server.py
├── www/
│ └── index.html
├── uploads/
└── registered_faces/
```
