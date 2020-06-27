




# 핸즈온 비지도학습 참고 URL

## CHAPTER 0 서문


## CHAPTER 1 머신러닝 생태계와 비지도학습
## CHAPTER 2 머신러닝 프로젝트 A to Z
## CHAPTER 3 차원 축소
## CHAPTER 4 이상치 탐지
## CHAPTER 5 클러스터링 
## CHAPTER 6 그룹 세분화 
## CHAPTER 7 오토인코더
## CHAPTER 8 핸즈온 오토인코더 
## CHAPTER 9 준지도학습 
## CHAPTER 10 RBM을 사용한 추천 시스템 
## CHAPTER 11 DBN을 사용한 피처 추출
## CHAPTER 12 GAN
## CHAPTER 13 시계열 클러스터링
## CHAPTER 14 결론




## URL List

page|주석 혹은 본문 내용[URL]
-----|-----
||옮긴이_ 하이프 사이클(hype cycle)은 기술의 성숙도를 표현하기 위한 시각적 도구입니다. 과대광고 주기라고도 합니다. 미국의 정보 기술 연구 및 자문 회사인 가트너에서 개발했습니다.[https://ko.wikipedia.org/wiki/%ED%95%98%EC%9D%B4%ED%94%84_%EC%82%AC%EC%9D%B4%ED%81%B4]|
||옮긴이_ 표현학습[representation learning)은 피처학습(feature representation learning)이라고도 하며 원본 데이터의 형상을 학습하여 분석 목적에 적합한 유용한 정보를 추출하거나 파생하는 머신러닝 기법입니다.[https://en.wikipedia.org/wiki/Feature_learning]|
||Figure Eight [https://www.figure-eight.com/] 처럼, 데이터에 레이블을 지정하는 수작업을 머신러닝 기법으로 기계가 대신 해주는 서비스를 제공하는 스타트업도 있습니다.|
||옮긴이_ 가치 함수(value function)는 일반적으로 강화학습에서 많이 사용되는 용어이며, 어떤 상태에 따라 앞으로 얼마의 보상을 받을수 있을지에 대한 기댓값으로 정의될 수 있습니다. 여기에서 가치 함수는 앞에서 언급한 것처럼 스팸 메일 필터 문제에서 정확하게 분류된 이메일의 비율을 예로 들 수 있습니다.[https://minhobby.tistory.com/37]|
||옮긴이_ 배깅은 원자료(raw data)로부터 여러 샘플 데이터(bootstrap sample)를 생성, 각 샘플 데이터를 모델링(modeling)한 후 결과를 집계(aggregating)하여 최종 예측 모델을 산출하는 방법입니다. 원자료로부터 여러 번 복원 샘플링(random sampling)하여 생성한, 크기가 동일한 여러 샘플을 사용하여 모델링함으로써 과대 적합을 피하고 예측 모델의 분산을 줄여 예측력을 향상시키는 일종의 앙상블 학습법의 메타 알고리즘이라고 할 수 있습니다.[https://ko.wikipedia.org/wiki/%EB%B0%B0%EA%B9%85]|
||머신러닝 경진 대회에 그래디언트 부스팅 머신을 사용하는 것을 더 알고 싶다면 Ben Gorman의 블로그 게시물을 참조하십시오.[https://medium.com/kaggle-blog]|
||신경망을 더 알고 싶으면 Ian Goodfellow, Yoshua Bengio, Aaron Courville의 Deep Learning을 확인하십시오(MIT Press).[http://www.deeplearningbook.org]|
||옮긴이_ 선형대수에서 행렬의 차원을 Rank로 표현하며, 행렬의 열들로 생성될 수 있는 벡터 공간의 차원을 의미합니다.[https://en.wikipedia.org/wiki/Rank_(linear_algebra)]|
||옮긴이_ 아타리(atari)는 1972년에 설립한 비디오 게임 회사 이름이자 이 회사에서 개발한 비디오 게임(스페이스 인베이더, 팩맨 등)을 말합니다. 딥마인드가 심층 강화학습을 처음 적용한 아타리 게임은 ‘스페이스 인베이더’로 알려졌습니다.[https://ko.wikipedia.org/wiki/%EC%95%84%ED%83%80%EB%A6%AC]|


## CHAPTER 1 머신러닝 생태계와 비지도학습
page|주석 혹은 본문 내용[URL]
-----|-----
||아직 Git [https://git-scm.com]을 설치하지 않았다면 Git을 설치해야 합니다. Git은 코드를 위한 버전 관리 시스템이며, 이 책의 모든 코딩 예제는 깃허브 리포지토리[https://github.com/aapatel09/handson-unsupervised-learning]에서 가져와 주피터 노트북으로 이용할 수 있습니다.|
||로저 더들러의 깃 가이드[http://rogerdudler.github.io/git-guide]를 살펴보고 리포지토리를 복제하고 변경 사항을 추가, 커밋 및 푸시하고 브랜치를 사용하여 버전 관리를 유지하는 방법을 알아보십시오. 또는 깃허브의 리포지토리[https://github.com/aapatel09/handson-unsupervisedlearning]를 방문하여 리포지토리를 수동 다운로드하여 사용할 수 있습니다.|
||옮긴이_ LFS란 Large File Storage를 뜻하고 대용량 파일을 관리하는 Git 저장소입니다. 대용량 파일을 복제하기 위해서는 LFS를 로컬 컴퓨터에 설치한 후 리포지토리를 복제해야 파일이 잘 복제됩니다. LFS를 설치하지 않고 리포지토리를 복제할 경우 일부 파일이 복제되지 않습니다. git LFS 설치 파일 다운로드 경로는 다음과 같습니다.[https://git-lfs.github.com]|
||파이썬과 머신러닝에 필요한 데이터 과학 라이브러리를 설치하려면 파이썬의 아나콘다 배포판[https://www.anaconda.com/distribution]을 다운로드 하십시오|
||시스템의 32비트 또는 64비트 버전에 따라 자신의 시스템에 맞는 버전의 XGBoost [https://www.lfd.uci.edu/~gohlke/pythonlibs/#xgboost]를 다운로드해야합니다.|
||fastcluster에 대한 자세한 정보는 [https://pypi.org/project/fastcluster/] 를 참조하십시오.|
||옮긴이_ fastcluster 설치 중 다음과 같은 에러 메시지가 나타날 경우 Visual C++ 빌드 도구를 설치해야 합니다. error: Microsoft Visual C++ 14.0 is required. Get it with "Microsoft Visual C++ Build Tools": https://visualstudio.microsoft.com/downloads/ Visual C++ 빌드 도구 설치를 위해서 에러 메시지에 있는 사이트에 접속 후 Visual Studio Community 버전을 다운로드 후 실행하여 Visual C++ 빌드 도구만 설치합니다.|
||이 데이터 셋은 캐글[https://www.kaggle.com/mlg-ulb/creditcardfraud]을 통해 구할 수 있으며, Worldline과 University of Libre de Bruxelles의 머신러닝 그룹이 공동 연구를 진행하면서 수집한 겁니다. 자세한 정보는 Andrea Dal Pozzolo, Olivier Caelen, Reid A. Johnson and Gianluca Bontempi, “Calibrating Probability with Undersampling for Unbalanced Classification” in Symposium on Computational Intelligence and Data Mining(CIDM], IEEE, 2015을 참조하십시오.|
||옮긴이_ 이진 분류에서 두 클래스는 포지티브 및 네거티브 레이블로 구분합니다. 모델을 생성하는 목적은 포지티브 레이블 결과를 찾는 겁니다. 사기 탐지 모델에서 포지티브 레이블은 '사기'를 의미합니다.[https://developers.google.com/machine-learning/glossary?hl=ko#p]|
||옮긴이_ 희소 행렬은 행렬 값이 대부분 0인 경우를 가리키는 표현으로 범주형 변수를 더미 변수(1과 0의 값을 가지는 변수]로 변환한 행렬을 이야기합니다. 원-핫 인코딩과 동일한 의미를 가집니다.[https://ko.wikipedia.org/wiki/%ED%9D%AC%EC%86%8C%ED%96%89%EB%A0%AC]|
||옮긴이_ 층화매개변수는 층화 추출 방식으로 데이터 샘플링하기 위해 지정하는 기준 변수를 말합니다. 모집단의 해당 기준 변수 비율에 맞추어 데이터를 표본 추출하여, 샘플 데이터의 특성 분포를 모집단과 유사하게 맞추기 위해 사용합니다.[https://en.wikipedia.org/wiki/Stratified_sampling]|
||옮긴이_ 랜덤 시드를 의미합니다. 난수 생성 함수는 시드를 기반으로 난수를 발생시키고 시드가 동일하면 동일한 난수를 발생시키게 됩니다. 파이썬 코드상 용어(random state)를 살려서 랜덤 상태로 번역했습니다. [https://en.wikipedia.org/wiki/Random_seed]|
||층화매개변수가 포지티브 레이블의 비율을 유지하는 방법을 자세히 알고 싶으면 공식 웹 사이트를 방문하십시오[https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html]. 실험에서 동일한 분할을 재현하려면 랜덤 상태를 2018로 설정합니다. 이것을 다른 숫자로 설정하거나 아무것도 설정하지 않으면 결과가 달라집니다.|
||L1과 L2에 대한 자세한 정보는“Differences Between L1 and L2 as Loss Function and Regularization.” 블로그 포스트를 참조하십시오. [http://www.chioka.in/differences-between-l1-and-l2-as-loss-function-and-regularization/]|
||옮긴이_ solver 매개변수는 최적화에 사용되는 해 찾기 알고리즘을 지정합니다. Solver를 자세히 알고 싶으면 다음 웹 사이트를 방문하십시오. [https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html]|
||옮긴이_ ROC(수신자 조작 특성 또는 반응자 작용 특성) 곡선은 일반적으로 이진 분류기에 대한 성능을 평가하는 기법입니다. 참 양성 비율(true positive rate, Y축, 민감성) 대 거짓 양성 비율(false positive rate, X축, 1-특이성)을 그래프로 나타냅니다. 신호 탐지 이론에서 가져온 개념으로 세계전쟁 당시 통신에서 사용한 용어(예: 리시버)를 사용합니다. [https://en.wikipedia.org/wiki/Receiver_operating_characteristic]|
||XGBoost 그래디언트 부스팅에 대한 더 자세한 내용은 GitHub 리포지토리를 참조하십시오.[https://github.com/dmlc/xgboost]|
||옮긴이_ 학습률은 최적화 알고리즘의 매개변수이며. 작은 값을 가지면 더 견고한 모델이 만들어 질 수 있지만 수행시간이 오래 걸립니다. 큰 값을 가지면 수행시간은 짧지만 최적 해를 찾지 못할 수도 있습니다. [https://en.wikipedia.org/wiki/Learning_rate]|
||마이크로소프트사의 LightGBM 그래디언트 부스팅을 더 알고 싶으면 다음 링크를 참조하십시오.[https://github.com/Microsoft/LightGBM]|
||머신러닝 솔루션의 결과를 개선하고 과소 적합/과대 적합을 해결하기 위해 하이퍼파라미터(하이퍼파라미터 파인튜닝fine-tuning22이라고 알려진 프로세스)를 조정하는 방법을 살펴보지 않았지만 깃허브 코드[https://github.com/aapatel09/handson-unsupervised-learning]를 통해 이러한 실험을 매우 쉽게 수행할 수 있습니다.|
||앙상블 학습에 대한 더 자세한 내용은 다음 세 링크를 참고하십시오. Kaggle Ensembling Guide[https://mlwave.com/kaggle-ensembling-guide] Introduction to Ensembling/Stacking in Python[https://www.kaggle.com/arthurtok/introduction-to-ensembling-stacking-in-python] A Kaggler’s Guide to Model Stacking in Practice[http://blog.kaggle.com/2016/12/27/a-kagglers-guide-to-model-stacking-in-practice]|



# 참고 GitHub-Guide

 1. 핸즈온 머신러닝 GitHub 저장소
 2. 파이썬 라이브러리를 활용한 데이터 분석 GitHub 저장소
 3. 피처 엔지니어링 GitHub 저장소


## 1.핸즈온 머신러닝 GitHub 저장소

 - GitHub([주소](https://github.com/rickiepark/handson-ml)
 - Read me (책소개, 설치, 파이썬 필수 라이브러리, 아나콘다 사용하기, PIP 사용하기, 주피터 시작하기, 기여자) 옮긴이가 어느정도 재구성
 - Requirement.txt 옮긴이가 어느 정도 재구성

 - 원저자 GitHub([주소]https://github.com/ageron/handson-ml2)


## 2.파이썬 라이브러리를 활용한 데이터 분석 GitHub 저장소

 - GitHub([주소](https://github.com/rickiepark/introduction_to_ml_with_python)
 - Read me (2판 책소개, 책 판매 사이트 링크 , 에러타, 설치 , 영어 언어 다운로드) 옮긴이가 어느정도 재구성 
 - Requirement.txt 원저자 GitHub에는 존재 하는데 한글 GitHub에는 없음

 - 원저자 GitHub([주소](https://github.com/amueller/introduction_to_ml_with_python))

## 3.피처 엔지니어링 GitHub 저장소

 - GitHub([주소](https://github.com/alicezheng/feature-engineering-book) 원저자 깃허브
 - Read me 짧게 있음

# 깃 허브 구성 의견

 - 데이터 다운로드 해야하는 부문에 대한 설명 read me 로 작성
 - 핸즈온 머신러닝에서 처럼 환경 구축 및 install 관련 2장에 내용을 요약해서 추가 하면 좋을 것 같고 패키지 버전, LFS 주석 같은 주의 사항 같은 같이 요약하면 좋을 것 같음
 - 에러타 페이지 ??
 - 책에서 오타 수정내용을 여기서도 연락 처를 남겨서 출판사로 전달하는 내용??
 - 참고로 원문 깃허브 링크 같은거 걸어 놓는거 ??
