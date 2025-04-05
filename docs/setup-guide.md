# 🛠️ CUDA 및 PyTorch 설치 가이드

NVIDIA GPU에서 PyTorch를 실행하기 위한 CUDA 환경 설정 방법을 안내합니다.

---

## 1️⃣ NVIDIA 드라이버 설치 확인

GPU 드라이버가 올바르게 설치되어 있는지 확인:

nvidia-smi

---

## 2️⃣ CUDA Toolkit 설치

[CUDA Toolkit 다운로드 페이지](https://developer.nvidia.com/cuda-toolkit)에서 적합한 버전을 선택하여 설치하세요.

설치 후 버전 확인:

nvcc --version

---

## 3️⃣ PyTorch 설치

PyTorch 공식 사이트에서 환경에 맞는 설치 명령어를 확인하세요:  
[PyTorch 설치 페이지](https://pytorch.org/get-started/locally/)

예시 (CUDA 11.8 지원):

pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118

설치 확인:

```python
import torch
print(f"PyTorch 버전: {torch.__version__}")
print(f"CUDA 사용 가능 여부: {torch.cuda.is_available()}")
if torch.cuda.is_available():
    print(f"CUDA 버전: {torch.version.cuda}")
    print(f"GPU 이름: {torch.cuda.get_device_name(0)}")


---

## 참고 링크 🔗

1. [NVIDIA 드라이버 다운로드](https://www.nvidia.com/Download/index.aspx)  
2. [CUDA Toolkit 공식 문서](https://docs.nvidia.com/cuda/)  
3. [PyTorch 공식 문서](https://pytorch.org/docs/)
