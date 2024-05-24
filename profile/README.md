## 🗓️ 사용자와 자유로운 상호작용이 가능한 Gen AI 기반 스마트 스케줄링 웹 서비스, NESS

<p>todomate나 구글 캘린더가 있어도 너무 바쁠 때면 일정 정리를 깜빡한 적이 있지 않나요?</p>
<p>그 이유는 기존의 일정 관리 서비스들은 아날로그 스케줄러를 그저 디지털로 옮겨놓은 것에 불과할 뿐이고, 모든 관리는 결국 사람이 수동으로 해주어야 하기 때문입니다. 팀 Re:coding은 이러한 문제를 극복하기 위해 간편하면서도 관리 보조의 기능성을 동시에 제공해줄 수 있는 방안을 생각해보게 되었습니다. 그 결과로 나온 LLM을 통해 사용자의 의도에 맞는 프로액티브한 스케쥴링을 제공 가능한 챗봇, NESS를 소개합니다.</p>

![NESS](https://github.com/studio-recoding/.github/assets/89632139/be9c413b-c5fa-43ef-88b2-e271a4192c52)

## ⚙️ Architecture
<p>NESS가 사용하는 기술은 아래와 같습니다.</p>
<img width="1920" alt="미래 아키텍처" src="https://github.com/studio-recoding/.github/assets/89632139/1623a223-992e-4ce1-8529-188162d345c7">

NESS는 `LangChain`과 `Vector DB`라는 기술을 사용합니다. 먼저 `LangChain`은 구조적으로 AI 모델, 에이전트 및 프롬프트를 만들고 연결할 수 있는 기술로, LLM 기반 어플리케이션을 위한 대부분의 작업을 중앙에서 제어해주는 오케스트레이션 프레임워크입니다.

`Vector DB`는 일반적인 관계형 DB와는 달리 정보를 벡터로 저장하는 데이터베이스로, 이렇게 백터 임배딩을 통해 각 데이터간 유사도를 계산하고, 유사도가 높은 데이터를 반환할 수 있습니다.

이 두 가지 기술을 활용해 LLM에 프롬프트를 보내기 전에 먼저 `Vector DB`에서 관련 데이터를 받아오고, LLM에게 프롬프트와 함께 전송하는 패턴을 `RAG`라고 일컫습니다. 이렇게 `RAG based LLM`을 통해 사용자의 기존 데이터를 참고하면 사용자 맞춤형 인공지능 비서를 만들 수 있습니다.

<p>더 자세한 설명은 아래 링크에서 참고해주세요.</p>

<a href="https://velog.io/@re_coding/NESS%EC%9D%98-1%EC%B0%A8-%EC%95%84%ED%82%A4%ED%85%8D%EC%B3%90-%EA%B5%AC%EC%84%B1feat.-RAG-Based-LLM"><img src="https://img.shields.io/badge/Team%20recoding%20Blog-7A64FF?style=for-the-badge&logo=tistory&logoColor=white"/></a>


## 📧 Contact us
[![recoding](https://img.shields.io/badge/recoding-7A64FF?style=for-the-badge&logo=gmail&logoColor=white)](mailto:maxcse01@gmail.com)
