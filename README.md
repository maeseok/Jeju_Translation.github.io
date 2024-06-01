# 🌊 제주의 언어 다리: 사투리에서 표준어로의 양방향 번역 모델 생성 프로젝트

## 🎯 1. 프로젝트 소개
이 프로젝트는 제주 사투리와 한국어 표준어 사이를 연결하는 양방향 번역 모델을 개발하여, 제주 방언의 이해를 돕고, 제주 문화의 보존에 기여하고자 합니다.

## 📊 2. 데이터
번역 모델 개발을 위해 사용된 데이터:
- 한국어 방언 발화 데이터 (AI-Hub 제공)
  - 방언(제주도)을 사용하는 일상 대화를 인식, 음성을 문자로 바꾸어주는 방언 발화 음성 데이터
  - json 파일을 전처리해 얻은 라벨 데이터만 사용
  - https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=115&topMenu=100&aihubDataSe=data&dataSetSn=121
- 중·노년층 한국어 방언 데이터 (AI-Hub 제공)
  - 충청, 전라, 제주 도민 방언 발화 음성 데이터 중 제주 발화 데이터만 사용
  - json 파일을 전처리해 얻은 라벨 데이터만 사용
  - https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=115&topMenu=100&aihubDataSe=data&dataSetSn=71558
- 카카오 JIT 제주 방언 데이터 (카카오브레인 Github 참조)
  - 깃허브 페이지 참고해서 데이터 수집
  - https://github.com/kakaobrain/jejueo
- 생활제주어 데이터 (제주어사전 참조)
  - 제주특별자치도 자체에서 관리하는 제주어사전 웹페이지에서 수집
  - https://www.jeju.go.kr/culture/dialect/lifeDialect.htm

## 💻 3. 모델 학습
사전 학습된 모델을 불러 Fine-tuning을 진행해주었습니다.

번역 모델 개발을 위해 활용한 모델:
- gogamza/kobart-base-v2
  - SKT-AI 에서 제공
  - https://huggingface.co/gogamza/kobart-base-v2 (Hugging Face)
  - https://github.com/SKT-AI/KoBART (Github)

고려해봤지만 선택하지 않은 모델:
- T5 (시간이 오래 걸리는 문제가 있음)
- Jebert (성능이 별로 좋지 않았음)

## 📈 4. 주요 성과
- BLEU 점수
    - 제주어 -> 표준어 : 0.89
    - 표준어 -> 제주어 : 0.77
- 이 모델은 제주 사투리와 표준어 간의 양방향 번역에서 뛰어난 성능을 보였습니다.

## 🔍 5. 향후 계획
모델 성능을 더욱 향상시키기 위해 추가 데이터 수집과 모델 파인 튜닝을 계획하고 있습니다.
인터페이스는 가볍게나마 만들었고 추후에 링크 첨부하겠습니다.
음성 BY 음성 기능도 구현 중입니다.
