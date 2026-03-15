# MANsMAN

> SSAFY 10기 특화프로젝트 최우수상 | 남성 화장품 추천 서비스

## My Contribution

| | |
|---|---|
| **Role** | Backend, Infra |
| **Period** | 2024.02 ~ 2024.04 (6주) |
| **Team** | 6명 (BE 4, FE 2) |

### What I Did

#### 1. 커뮤니티 게시판 API (RESTful, Spring Data JPA)
- 전체 약 60개 API 중 17개 담당
- 게시물 CRUD + 사진 다중 이미지 순서 관리 + 좋아요/스크랩
- 댓글 CRUD + 댓글 좋아요 (별도 Controller 분리)
- ERD 설계 및 JPA Entity 구현 (Board, Comment, BoardImage, Scrap, BoardLike, CommentLike 등 7개 테이블)
- 조회수/댓글수/스크랩수 카운팅 기능
- 권한 검증: 본인 게시물/댓글만 수정/삭제 가능하도록 구현

#### 2. Jenkins CI/CD 파이프라인
- GitLab Webhook으로 코드 변경사항 자동 감지
- **폴더 수준 변경 감지**로 변경된 컴포넌트(Spring/FastAPI/Frontend)만 선별 빌드/배포
- Credentials로 secret 파일 및 API 키 관리
- 배포 성공/실패 시 Mattermost 알림 전송

#### 3. Docker 인프라 구축 (AWS EC2)
- Nginx: Reverse Proxy + SSL 인증서 설정
- 컨테이너 구성: Jenkins(9090), Spring(8080), FastAPI(8000), MySQL(3306), Redis(6379)
- Docker Compose로 전체 서비스 오케스트레이션
- FastAPI Docker 이미지 최적화: Python 3.12 업그레이드, tensorflow-intel 제거, 호환성 이슈 트러블슈팅 (7회 반복 수정)

#### 4. 기타
- PPT 제작 및 최종 발표 담당

### Tech Stack
`Spring Boot` `Spring Data JPA` `MySQL` `Redis` `Docker` `Nginx` `Jenkins` `AWS EC2`

---

## 📌 개요
MANsMAN은 사용자의 **피부타입을 분석**하고 분석결과와 화장품 사용패턴에 따라 **맞춤형 추천 서비스**를 제공하는 모바일 앱 서비스입니다.

|||
|-|-|
|기간|2024. 2. 26 ~ 2024. 4. 5 (6주)
|인원|6명|


<br/><br/>

## 📝 개발문서

### [> Notion](https://hungry-attention-0f2.notion.site/939943a144c646f08975a022dbe7ce7e?v=d85b58eaa1ee40908ec0793a58fe5e07&pvs=4)



<br/><br/>

## 🔧 기술스택

### Front-End

<img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=Flutter&logoColor=black"> <img src="https://img.shields.io/badge/firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black">



### Back-End
<img src="https://img.shields.io/badge/springboot-6DB33F?style=for-the-badge&logo=SpringBoot&logoColor=black"> <img src="https://img.shields.io/badge/JPA-6DB33F?style=for-the-badge&logo=JPA&logoColor=black"> <img src="https://img.shields.io/badge/fastapi-009688?style=for-the-badge&logo=fastapi&logoColor=black">

### DB
<img src="https://img.shields.io/badge/redis-DC382D?style=for-the-badge&logo=redis&logoColor=black"> <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=MySQL&logoColor=black"> <img src="https://img.shields.io/badge/S3-569A31?style=for-the-badge&logo=amazons3&logoColor=black">




### Infra
<img src="https://img.shields.io/badge/docker-2496ED?style=for-the-badge&logo=docker&logoColor=black"> <img src="https://img.shields.io/badge/nginx-009639?style=for-the-badge&logo=nginx&logoColor=black"> <img src="https://img.shields.io/badge/jenkins-D24939?style=for-the-badge&logo=Jenkins&logoColor=black">


<br/><br/>

## 📱 주요기능

- 사진 촬영 후 AI분석
- 피부 관리 일지
- 화장품 추천 


<br/><br/>

## 🏗️ 아키텍처

![image](https://github.com/cuzzzu1318/cuzzzu1318/assets/77597885/0192565f-09f5-4adb-b088-339ec0a24416)

<br/><br/>


## ⚙️ ERD

![image](/exec/images/MANsMAN_ERD.png)

<br/><br/>

## 👥 팀원 소개

| [김동영](https://github.com/ssafy10kim) | [황채원](https://github.com/wondreaming) | [송승준](https://github.com/seungjun-song) | [이현민](https://github.com/hyunmin2667) | [박정호](https://github.com/cuzzzu1318) | [조창래](https://github.com/crcho5133) |
| :---: | :---: | :---: | :---: | :---: | :---: |
|![image](https://github.com/cuzzzu1318/cuzzzu1318.github.io/assets/77597885/4340db40-6587-433b-be93-78c578260226)|![image](https://github.com/cuzzzu1318/cuzzzu1318.github.io/assets/77597885/44734b9f-1e4e-4c10-a24e-39906257dde6)|![image](https://github.com/cuzzzu1318/cuzzzu1318.github.io/assets/77597885/70dc7727-3516-47e7-aa24-6802c06c47a0)|![image](https://github.com/cuzzzu1318/cuzzzu1318.github.io/assets/77597885/184e1b1c-349a-465d-b7f3-70d029f31657)|![image](https://github.com/cuzzzu1318/cuzzzu1318.github.io/assets/77597885/274fbc64-40bd-4691-bbe1-1417391f8695)|![image](https://github.com/cuzzzu1318/cuzzzu1318.github.io/assets/77597885/1ac93d83-9107-4e70-9754-036fc8410e4b)|
|FE|FE|Full Stack|**BE(팀장)**|BE(Data)|BE(Data)|
|Flutter <br>FireBase 알림|Flutter|Security / JWT<br>API<br>Flutter|Infra<br>API|API<br>fastAPI<br>|API<br>fastAPI
