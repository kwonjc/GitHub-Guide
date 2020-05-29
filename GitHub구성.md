# 참고 GitHub-Guide

 1. 웹 GitHub 저장소를 생성하기
 2. 생성한 웹 GitHub 저장소 로컬 복제하기
 3. 업로드 파일을 로컬 GitHub 저장소에 저장


## 1.핸즈온 머신러닝 GitHub 저장소

 - GitHub([주소](https://github.com/rickiepark/handson-ml)
 - Read me (책소개, 설치, 파이썬 필수 라이브러리, 아나콘다 사용하기, PIP 사용하기, 주피터 시작하기, 기여자) 옮긴이가 어느정도 재구성
 - Requirement.txt 옮긴이가 어느 정도 재구성

 - 원저자 GitHub([주소]https://github.com/ageron/handson-ml2)


## 2.파이썬 라이브러리를 활용한 데이터 분석 GitHub 저장소

 - GitHub([주소](https://github.com/rickiepark/handson-ml)
 - Read me (2판 책소개, 책 판매 사이트 링크 , 에러타, 설치 , 영어 언어 다운로드) 옮긴이가 어느정도 재구성 
 - Requirement.txt 원저자 GitHub에는 존재 하는데 한글 GitHub에는 없음

 - 원저자 GitHub([주소](https://github.com/wesm/pydata-book))

## 3.피처 엔지니어링 GitHub 저장소

 - GitHub([주소](https://github.com/alicezheng/feature-engineering-book) 원저자 깃허브
 - Read me 짧게 있음

 - 원저자 GitHub([주소](https://github.com/wesm/pydata-book))

# 깃 허브 구성 의견

 - 데이터 다운로드 해야하는 부문에 대한 설명 read me 로 작성
 - 핸즈온 머신러닝에서 처럼 환경 구축 및 install 관련 2장에 내용을 요약해서 추가 하면 좋을 것 같고 패키지 버전, LFS 주석 같은 주의 사항 같은 같이 요약하면 좋을 것 같음
 - 에러타 페이지 ??
 - 책에서 오타 수정내용을 여기서도 연락 처를 남겨서 출판사로 전달하는 내용??
 - 참고로 원문 깃허브 링크 같은거 걸어 놓는거 ??






## 1.웹 GitHub 저장소 생성하기

 - 회원가입([github.com](http://github.com/))
 - New Repositories 생성
 [레포지토리 생성 참고 사이트](https://mrw0119.tistory.com/120)

## 2.생성한 웹 GitHub 저장소 로컬 복제하기

 - 데스크탑 github 설치 ([https://desktop.github.com/](https://desktop.github.com/))
 - 데스크탑 GitHub 실행
 - **"Clone a Repository from internet..."** 클릭 후 복제할 웹 GitHub 저장소 선택
 - 로컬 GitHub 저장소 폴더에서 웹 GitHub 저장소에서 복제된 파일 확인

## 3. 로컬 GitHub 저장소에 업로드 파일을 저장

 - 로컬 GitHub 저장소 폴더에 업로드 할 파일을 저장
 - 업로드 파일을 저장할때 용량이 작은 경우 문제가 되지 않지만 업로드할 파일 용량이 클 경우(100MB)는 에러 발생
 - 예를 들어 업로드할 파일들 중 50MB 미만으로 파일들을 선택해서 저장하고 PUSH 하고  또 50MB 미만으로 저장하고 PUSH 하는 작업을 반복해야함
 - 참고로 윈도우 CMD 창에서 50MB 넘는 파일 모두 추출 하는 명령문 : forfiles /S /M * /C "cmd /c if @fsize GEQ 54857600 echo @path")
 
## 4.웹 GitHub 저장소로 PUSH

 - 로컬 GitHub 저장소 폴더에 업로드 할 파일이 추가되고 데스크탑 GitHub 를 실행하면 **Changes** 목록에 추가된 파일 목록이 나타남
 - Changes 목록을 선택 후 Summary 설명을 작성하고 **Commit to master** 버튼을 클릭하고 PUSH 버튼 클릭
 -  Changes 목록에서 선택한 여러개의 파일 용량이 100MB를 넘거나 하나의 파일를 100MB 넘으면 Commit 할수 없음 
 - 100MB 이상 되는 파일 PUSH (로컬 ==> Web 저장소) 방법
-- git lfs 로 대용량 파일 올리기
-- CMD 창에서 로컬 Github 저장소 경로로 이동 후 아래 명령문 실행 
```
git lfs install
git lfs track "*.csv"
git add .
git commit -m "message input"
git push origin master
```
[참고사이트1](https://velog.io/%4029been/Github-100MB%EB%B3%B4%EB%8B%A4-%ED%81%B0-%ED%8C%8C%EC%9D%BC-%EC%98%AC%EB%A6%AC%EA%B8%B0)
[참고사이트2](https://arclab.tistory.com/216)
[참고사이트3](https://blog.naver.com/lizziechung/221921218133)
- .gitattributes 확장자 파일은 git lfs track "*.csv" 명령문을 수행하면 자동으로 생성됨(내용은 잘 모르겠음)
- 대용량 파일 Commit 하다가 실패하면 히스토리 로그를 지워야 하는데 아래 참고 사이트를 참고 해서 수행했지만 해결 되지 않아 그냥 웹저장소를 다시 만들었음
[참고사이트](https://jootc.com/p/201909143109)

## 5. 협업을 위한 권한 부여

 - 동료에서 커밋 권한 부여 ==> "**Collaborator**" 추가
 - 웹 깃허브에서 **Setting > Manage access ==> collaborators yet**
 [참고사이트](https://git-scm.com/book/ko/v2/GitHub-GitHub-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-%EA%B4%80%EB%A6%AC%ED%95%98%EA%B8%B0)

## 6. 코드 수정 후 PUSH 테스트 

 - 로컬 파일 수정 하기 웹 저장소에 반영하기
 - 웹 저장소에서 파일 수정 후 로컬 저장소에 반영 하기
 - 협업자가 되어서 위의 2가지 실행 해보기

## 7. 기타 

 - 마크다운 사용법 및 확인 웹 참고 사이트 추가
[참고사이트1](https://stackedit.io/app#)
[참고사이트2](https://gist.github.com/ihoneymon/652be052a0727ad59601)
[참고사이트3](https://velog.io/@yuuuye/velog-%EB%A7%88%ED%81%AC%EB%8B%A4%EC%9A%B4MarkDown-%EC%9E%91%EC%84%B1%EB%B2%95)
[참고사이트4](https://4urdev.tistory.com/62)
 - clone vs git fork 차이
[참고사이트1](https://velog.io/%40imacoolgirlyo/Git-fork%EC%99%80-clone-%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90-5sjuhwfzgp)
[참고사이트2](https://playinlion.tistory.com/29)
  - Fork 기능은 상대방의 리포지토리를 내 웹 리포지토리로 그대로 가져 온다. 로컬 컴퓨터에서 Fork한 리포지토리를 복제 해서 사용합니다.여러 사람이 프로젝트 할때 원본이 훼손될 위험을 대비해서
  - 로컬 리포지토리에서 폴더 생성한거는 변화한 파일로 탐지 하지 않음 readme 파일이라도 있어야함

- 이슈 : 수정 사항 및 건의 사항 등 소유자에게 요청 할 수 있는데 다른 연계 기능이 많은 거 같음
- 와치 : 등록하면 소유자의 변화 관리를 확인할 수 있음
- 스타 : 즐겨찾기 기능
- Action 기능 예시 : 많은 기능이 있는데 잘 모르겠음
[참고사이트](https://medium.com/%40elastic7327/%EA%B9%83%ED%97%88%EB%B8%8C%EC%9D%98-%EC%95%A1%EC%85%98-%EA%B8%B0%EB%8A%A5-git-action-%EB%A5%BC-%EC%82%AC%EC%9A%A9%ED%95%B4%EB%B3%B4%EC%9E%90-ed634d622280)

- GitHub 프로젝트 생성 : 관련 내용이 조금 있는데 이슈 및 다 연동해서 프로젝트에서 사용하는 거 같은데 ?? 추가 확인이 필요
[참고사이트](https://www.huskyhoochu.com/issue-based-version-control-201/)
- 이슈 pull request 등 사용법
[참고사이트](https://cheese10yun.github.io/github-proejct/)
-   기초 사용법 : issue, labels, milestone 사용법
[참고사이트1](https://uang.tistory.com/11?category=799977)
[참고사이트2](https://github.com/cau-cmclab/sku-cmclab.github.io/wiki/%EA%B9%83%ED%97%88%EB%B8%8C-%EB%8D%B0%EC%8A%A4%ED%81%AC%ED%83%91%28GitHub-Desktop%29-%EC%82%AC%EC%9A%A9)