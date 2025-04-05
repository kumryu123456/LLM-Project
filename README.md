# 📝 텍스트 기반 QA 시스템 및 PDF 처리 확장

## 프로젝트 개요
이 프로젝트는 PyTorch를 기반으로 텍스트 기반 질문 응답(QA) 시스템을 구현하고, PDF 텍스트 추출 및 멀티모달 데이터 처리를 확장하는 것을 목표로 합니다.

---

## 주요 기능 ✨
- **질문 응답 시스템**: GPT-2 또는 BERT 모델을 활용한 QA 기능.
- **PDF 텍스트 추출**: PyPDF2와 PyMuPDF를 사용하여 PDF에서 텍스트 추출.
- **멀티모달 데이터 확장**: 이미지와 텍스트를 결합한 데이터 처리(후기 단계).

---

## 📖 목차
1. [프로젝트 개요](#프로젝트-개요)
2. [주요 기능](#주요-기능)
3. [실행 방법](#실행-방법)
4. [학습 자료](#학습-자료)
5. [설치 가이드](#설치-가이드)

---

## 실행 방법 🚀

### 1️⃣ 환경 설정
Python 환경을 설정하고 필요한 패키지를 설치합니다:

```python
pip install -r requirements.txt
```
### 2️⃣ 모델 실행
다음 명령어로 메인 스크립트를 실행합니다:

```python
python src/main.py
```

---

## 학습 자료 📚

👉 [공부용 자료 보기](docs/study-guide.md)  
👉 [자주 묻는 질문(FAQ)](docs/faq.md)

---

## 설치 가이드 🛠️

👉 [CUDA 및 PyTorch 설치 가이드 보기](docs/setup-guide.md)

---

## 기술 스택 🧰
- **프로그래밍 언어**: Python 3.9+
- **딥러닝 프레임워크**: PyTorch 2.6.0+cu118
- **PDF 처리 라이브러리**: PyPDF2, PyMuPDF, Tesseract OCR

---

## 기여 방법 🤝

1. 이 저장소를 포크합니다.
2. 새로운 브랜치를 생성합니다:
    ```
    git checkout -b feature-name
    ```
3. 변경 사항을 커밋합니다:
    ```
    git commit -m "Add new feature"
    ```
4. 변경 사항을 푸시합니다:
    ```
    git push origin feature-name
    ```
5. Pull Request를 생성합니다.

---

## 문의하기 💬

궁금한 점이나 제안 사항이 있다면 [Issues](https://github.com/username/project-name/issues)를 통해 문의해주세요.
