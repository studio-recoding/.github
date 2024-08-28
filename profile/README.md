## 🗓️ 채팅 하나로 일정을 관리해요! Gen AI 기반 스마트 스케줄링 웹 서비스, NESS

<p>todomate나 구글 캘린더가 있어도 바쁠 때면 일정 정리를 깜빡하고는 하죠.</p>
<p>그 이유는 기존의 일정 관리 서비스들은 아날로그 다이어리를 디지털에 옮겨놓은 것에 불과할 뿐이고, 모든 관리는 결국 사람이 수동으로 해주어야 하기 때문이라고 할 수 있어요. 팀 Re:coding은 이러한 문제를 극복하기 위해 간편하면서도 높은 수준의 관리 보조를 제공해줄 수 있는 방안을 생각해보게 되었습니다. 그 결과로 나온 능동적 스케쥴링 관리를 제공하는 똑똑한 맞춤형 챗봇, NESS를 소개합니다.</p>

<img width="1920" alt="NESS 소개" src="https://github.com/user-attachments/assets/13523a27-1be0-43bb-98fb-eea549ff0431">


## ⚙️ Architecture
<p>NESS의 아키텍쳐를 한눈에 살펴봐요!</p>
<p>NESS는 팀원들의 전문 분야에 맞게 FE/AI/BE 업무를 분할했어요. 전체 아키텍쳐 또한 사용자와 인터렉션하는 NEXT.js 프론트엔드, 인증 및 RDB 데이터를 처리하는 Springboot 웹 백엔드, AI API 호출과 RAG를 담당하는 FastAPI AI 백엔드로 구성되어 있어요. 이런 기술들은 다양한 AWS 서비스와 통합되어 엔드 유저에서 전달 가능해요. 또한, GitHub Action과 통합되어 CI/CD를 구성했어요.</p>

<img width="1920" alt="NESS 아키텍처" src="https://github.com/user-attachments/assets/1ea3eab8-4b36-4b1b-8e1c-8eda624e35be">

NESS는 `LangChain`과 `Vector DB`라는 기술을 사용합니다. 먼저 `LangChain`은 구조적으로 AI 모델, 에이전트 및 프롬프트를 만들고 연결할 수 있는 기술로, LLM 기반 어플리케이션을 위한 대부분의 작업을 중앙에서 제어해주는 오케스트레이션 프레임워크입니다.

`Vector DB`는 일반적인 관계형 DB와는 달리 정보를 벡터로 저장하는 데이터베이스로, 이렇게 백터 임배딩을 통해 각 데이터간 유사도를 계산하고, 유사도가 높은 데이터를 반환할 수 있습니다.

이 두 가지 기술을 활용해 LLM에 프롬프트를 보내기 전에 먼저 `Vector DB`에서 관련 데이터를 받아오고, LLM에게 프롬프트와 함께 전송하는 패턴을 `RAG`라고 일컫습니다. 이렇게 `RAG based LLM`을 통해 사용자의 기존 데이터를 참고하면 사용자 맞춤형 인공지능 비서를 만들 수 있습니다.

## 👩‍💻 Team Studio Re:coding

|                                    Frontend                                    |                                   AI                                    |                                    Backend                                     |
| :--------------------------------------------------------------------------: | :---------------------------------------------------------------------------: | :--------------------------------------------------------------------------: |
| <img src="https://avatars.githubusercontent.com/u/113418916?v=4" width=150px> | <img src="https://avatars.githubusercontent.com/u/90598552?v=4" width=150px> | <img src="https://avatars.githubusercontent.com/u/89632139?v=4" width=150px> | <img src="https://avatars.githubusercontent.com/u/89632139?v=4" width=150px> |
|                     [최민주/Minju Choi](https://github.com/hmuri)                     |                     [황채원/Chaiwon Hwang](https://github.com/uommou)                      |                   [전혜승/Haeseung Jeon](https://github.com/JeonHaeseung)                   |

<p>Studio Re:coding의 팀원들이 개발하고, 스터디하고, (종종) 놀러간 이야기가 궁금하신가요? 아래 벨로그에서 확인해주세요!</p>

<a href="https://velog.io/@re_coding/posts"><img src="https://img.shields.io/badge/Team%20recoding%20Blog-7A64FF?style=for-the-badge&logo=tistory&logoColor=white"/></a>

## 📧 Contact us
[![recoding](https://img.shields.io/badge/recoding-7A64FF?style=for-the-badge&logo=gmail&logoColor=white)](mailto:maxcse01@gmail.com)
