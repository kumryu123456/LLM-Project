# ⚙️ CUDA 및 PyTorch 설치 가이드

NVIDIA GPU에서 PyTorch를 실행하기 위한 CUDA 환경 설정 방법을 안내합니다.

---

## 📌 1. NVIDIA 드라이버 설치 확인
GPU 드라이버가 올바르게 설치되어 있는지 확인하려면 아래 명령어를 실행하세요:


```python
nvidia-smi
```

**실행 결과 예시**:
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 470.57.02 Driver Version: 470.57.02 CUDA Version: 11.8 |
|-------------------------------+----------------------+----------------------+
| GPU Name Persistence-M| Bus-Id Disp.A | Volatile Uncorr. ECC|
| Fan Temp Perf Pwr:Usage/Cap| Memory-Usage | GPU-Util Compute M.|
+-------------------------------+----------------------+----------------------+
| 0 NVIDIA RTX 4070 Ti On | 00000000:01:00.0 Off | |
+-----------------------------------------------------------------------------+

---

## 📌 2. CUDA Toolkit 설치
[CUDA Toolkit 다운로드 페이지](https://developer.nvidia.com/cuda-toolkit)에서 적합한 버전을 선택하여 설치하세요.

설치 후, 아래 명령어로 CUDA 버전을 확인합니다:

```python
nvcc --version
```

**실행 결과 예시**:
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2025 NVIDIA Corporation
Built on Sun_Sep_10_19:22:12_PDT_2025
Cuda compilation tools, release 11.8, V11.8.89

---

## 📌 3. PyTorch 설치
PyTorch 공식 사이트에서 환경에 맞는 설치 명령어를 확인하세요:  
[PyTorch 설치 페이지](https://pytorch.org/get-started/locally/)

### **예시 (CUDA 11.8 지원)**:

```python
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

### **설치 확인**
아래 Python 코드를 실행하여 PyTorch와 CUDA가 제대로 작동하는지 확인하세요:



```python
import torch
print(f"PyTorch 버전: {torch.__version__}")
print(f"CUDA 사용 가능 여부: {torch.cuda.is_available()}")
if torch.cuda.is_available():
    print(f"CUDA 버전: {torch.version.cuda}")
    print(f"GPU 이름: {torch.cuda.get_device_name(0)}")
```

**실행 결과 예시**:
PyTorch 버전: 2.6.0+cu118
CUDA 사용 가능 여부: True
CUDA 버전: 11.8
GPU 이름: NVIDIA GeForce RTX 4070 Ti SUPER
---

## 🔗 참고 링크

1. [NVIDIA 드라이버 다운로드](https://www.nvidia.com/Download/index.aspx)
2. [CUDA Toolkit 공식 문서](https://docs.nvidia.com/cuda/)
3. [PyTorch 공식 문서](https://pytorch.org/docs/)

