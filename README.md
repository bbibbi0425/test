<div style="display: flex; align-items: center; justify-content: center; gap: 16px;">
  <h1 style="margin: 0; font-size: 28px;">피싱 웹 사이트 탐지 시스템 |   <img src="./assets/logo.png" alt="로고" style="height: 30px;" /></h1>
</div>
<br>


## 🌊 소개

<strong>wave to www</strong>는 <strong>누구나 쉽게 사용할 수 있도록 설계된 사용자 중심의 피싱 탐지 서비스</strong>입니다.
단순히 <strong>위험 여부만을 알려주는 기존 방식</strong>에서 한 걸음 더 나아가,
<strong>AI 분석</strong>과 <strong>룰 기반 코드 분석</strong>을 결합하여 <strong>왜 위험한지에 대한 근거</strong>까지 함께 제공합니다.

<strong>HTML, JavaScript, URL 패턴 등 피싱 사이트의 공통적인 특징</strong>을 사전에 분석하고 이를 <strong>모듈화</strong>하여
<strong>탐지의 정밀도</strong>와 <strong>설명력</strong>을 높였습니다. <strong>웹 기반 서비스</strong>와 <strong>크롬 확장 프로그램</strong> 두 가지 형태로 제공되며,
사용자는 <strong>직접 URL을 입력</strong>하거나 <strong>웹서핑 중 마우스오버만으로 실시간 탐지</strong>를 받을 수 있습니다.

<strong>누구나 이해할 수 있는 시각적 결과</strong>와 함께,
<strong>전문가에게는 분석 도구로</strong>, <strong>기관에는 대응 체계로 활용</strong> 가능한
<strong>범용성과 실용성</strong>을 갖춘 서비스입니다.

<p align="center">
  <img src="./assets/main.png" alt="프로젝트 메인"/>
</p>

--- 

## 🍀 목차

- [🌊 소개](#-소개)
- [✅ 주요 기능](#-주요-기능)
- [🦾 AI] (#-AI)
- [🛠 기술 스택](#-기술-스택)
- [📁 프로젝트 구조](#-프로젝트-구조)
- [🚀 실행 방법](#-실행-방법)
  - [🔗 서비스 링크](#-서비스-링크)
  - [🌊 사용 흐름](#-사용-흐름)
- [👩‍💻 프로젝트 참여자](#-프로젝트-참여자)


---

## ✅ 주요 기능

- 기능 1
- 기능 2
- 기능 3

---

## 🦾 AI


사용 데이터셋: https://www.kaggle.com/datasets/shashwatwork/web-page-phishing-detection-dataset?resource=download

<img src="./assets/features.png" alt="특징" style="width: 600px;" />

<img src="./assets/ai.png" alt="AI" style="width: 400px;" />


---

## 🛠 기술 스택
<p align="center">
  <img src="./assets/front.png"width="500"/>
  <img src="./assets/back.png"width="500"/>
</p>

---

## 📁 프로젝트 구조

<pre>
PROJECT/
├── .github/                                  
├── scripts/                                  # 배포 및 실행 스크립트 모음
├── source/                                   
│   └── chrome_extension/                     # Chrome Extension
│       └── gui/                              # Front-End
│           ├── dist/                         # 빌드 결과물
│           │   └── assets/                   # 배포용 이미지 등 리소스
│           └── src/                          # 확장 프로그램 원본 코드
│               └── assets/                   # 확장용 이미지 등 리소스
├── kernel/                                   # Kernel
│   ├── engines/                              # 탐지 엔진 베이스 및 모듈들
│   ├── kernel_db/                            # 탐지에 사용되는 각종 DB
│   │   ├── data_black_list/                  # 블랙리스트 (브랜드, 도메인, 링크)
│   │   ├── data_etc/                         # 기타 TLD, 국가 코드 등
│   │   └── data_white_list/                  # 화이트리스트 도메인
│   ├── plugins/                              # 탐지 모듈 플러그인 모음
│   │   ├── ai_modules/                       # AI 관련 모듈
│   │   │   ├── ai_model/                     # 학습된 모델(pkl 파일 등)
│   │   │   └── ai_source/                    # 특징 추출 등 AI 추론 코드
│   │   ├── html_modules/                     # HTML 기반 탐지 모듈
│   │   ├── js_modules/                       # JS 기반 탐지 모듈
│   │   └── url_modules/                      # URL 기반 탐지 모듈
├── server/                                   # Server - Back-End : FAST API
│   ├── app/                                  # 서버 애플리케이션 모듈
│   │   ├── schemas/                          # 요청/응답 스키마 정의
│   │   └── utils/                            # 공통 유틸리티 함수들
│   ├── server_config/                        # 서버 설정 파일
│   └── sessions/                             # 사용자 세션 관리 모듈
├── tests/                                    # 모듈별 테스트 코드
│   └── module_test/
│       ├── module_test_data/                 # 테스트용 피싱 데이터
│       └── module_test_results/              # 테스트 결과 스크립트
├── web/                                      # 사용자 웹 인터페이스 (React)
│   └── gui/
│       └── React/
│           ├── public/                       # 정적 파일 (index.html 등)
│           └── src/                          # React 앱 소스
│               ├── assets/                   # 이미지 및 폰트 리소스
│               │   ├── fonts/                # Poppins 등 폰트 파일
│               │   └── img/                  # 로고, 아이콘 등 이미지
│               ├── components/               # 공통 UI 컴포넌트
│               ├── pages/                    # 페이지 단위 컴포넌트
│               └── styles/                   # CSS 스타일 파일
</pre>

---

## 🚀 실행 방법

### 🔗 서비스 링크

<p align="center">
  <a href="" target="_blank">
    <img src="https://img.shields.io/badge/Web%20Service-WaveTo-blue?style=for-the-badge&logo=vercel" alt="웹 서비스 링크"/>
  </a>
  &nbsp;
  <a href="" target="_blank">
    <img src="https://img.shields.io/badge/Chrome%20Extension-다운로드-29ABE2?style=for-the-badge&logo=googlechrome" alt="크롬 확장 프로그램 링크"/>
  </a>
</p>

### 🌊 사용 흐름

---

## 👩‍💻 프로젝트 참여자

<div align="center">

<table style="border: none;">
  <tr>
    <td align="center"><strong>여지훈</strong></td>
    <td align="center"><strong>강지민</strong></td>
    <td align="center"><strong>서하진</strong></td>
    <td align="center"><strong>이기석</strong></td>
  </tr>
  <tr>
    <td align="center"><img src="./assets/jihun.JPG" width="107"/></td>
    <td align="center"><img src="./assets/jimin.JPG" width="105"/></td>
    <td align="center"><img src="./assets/hajin.JPG" width="110"/></td>
    <td align="center"><img src="./assets/gisuk.JPG" width="118"/></td>
  </tr>
  <tr>
    <td align="center">🌈 <strong>PM</strong><br/>🛠️ <strong>백엔드</strong></td>
    <td align="center">🌳 <strong>AI</strong><br/>🎨 <strong>디자인</strong></td>
    <td align="center">⚙️ <strong>커널</strong></td>
    <td align="center">📱 <strong>프론트엔드</strong></td>
  </tr>
</table>

</div>