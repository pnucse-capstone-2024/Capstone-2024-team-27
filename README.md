### 1. 연구동기
> 방대한 양의 데이터가 쏟아지는 빅데이터 시대에 중요한 키워드(단어)를 추출하는 것은 중요한 문제이다.
> 
> 이를 위해 텍스트 클라우드(Text Cloud)가 사용되지만, 기존의 텍스트 클라우드는 사용자 개인의 선호도나 특징을 반영하지 못한다.
> 
> 이를 위해, 우리는 사용자 개인의 선호도와 특징을 반영하여 텍스트 클라우드를 시각화하고자 한다.


### 2. 구현
> 사용자의 특징을 추출하기 위해 생성형 AI인 Llama3 모델을 이용한다.
> 
> 사용자와 많은 대화를 하기 위해 멀티턴(Multi Turn) 대화를 학습하여 Fine-tuning한다.
> 
> 사용자가 입력한 문장의 감정과 특징을 분석하고 이를 통해 뉴스를 추천한다.
> 
> 동시에, 사용자의 감정과 문장의 특징을 통해 추천한 뉴스를 코사인 유사도를 기반으로 텍스트 클라우드를 생성한다.

### 3. Fine Tuning
> Hugging Face에서 Meta사의 Llama 3를 다운로드 한다.
>
> `unsloth` 모듈을 이용하여 빠르게 학습시킨다.
>
> ### `unsloth` 모듈 호환성 가이드
> 
> ### 1. **PyTorch 버전 호환성**
>    - 권장 PyTorch 버전: `2.x` (일반적으로 2.0 이상)
> 
> ### 2. **관련 종속성**
> 
>    - **transformers**: `>= 4.x`
>    - **torchvision**: PyTorch 버전에 맞는 버전 사용 (예: PyTorch 2.0을 사용하면 torchvision 2.x 사용)
>    - **numpy**: `>= 1.19`
>    - **scipy**: `>= 1.5`
>    - **tokenizers**: 주로 transformers와 함께 사용되며, `>= 0.10.0` 버전 사용
>    - **sentencepiece**: 특정 토크나이징 작업에 필요하다면, `>= 0.1.91` 버전 사용
>    
> ### 3. **다른 도구 (선택 사항)**
>    - **huggingface-hub**: `>= 0.10.x` (Hugging Face 모델과 상호작용 시)
>    - **datasets**: `>= 1.5` (Hugging Face의 데이터셋을 사용할 경우)
> 
> ### 4. **환경 권장 사항**
>    - **Python**: `>= 3.8` (Python 3.8 이상 사용 권장)
>    - **CUDA (GPU 사용 시)**: PyTorch 버전에 맞는 CUDA 버전 사용 (예: CUDA 11.3+)

### 4. 시연 영상
> 시연영상 유튜브 링크
> > https://www.youtube.com/watch?v=YoGGfor5GlI/0.jpg
> > https://www.youtube.com/watch?v=YoGGfor5GlI

### 5. 팀 소개
> 금비(팀장)
> > 모델 튜닝 및 데이터 전처리
> > 
> > email : rmaql0106@pusan.ac.kr
>
> 원윤서
> > 프론트, 백엔드 담당
> > 
> > email : yoonsu0325@pusan.ac.kr
