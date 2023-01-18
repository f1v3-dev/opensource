# opensource
Opensource SW Project (https://dacon.io/competitions/official/235902/overview/description)

## 개발환경
- Visual Studio Code
- Anaconda3
- Google Colab

## 언어
- Python

## 주제
심리학 테스트 데이터를 분석하여 "심리 성향을 예측"하는 알고리즘을 개발합니다.

## 데이터 설명
[Data Description](https://github.com/f1v3-dev/opensource/blob/main/data_desc.ipynb)

## 데이터 전처리 
  
### Q1 ~ Q20
마키아벨리즘에 관한 질문에 대해 점수를 합산  
질문 중 마키아벨리즘에 반대되는 질문에 점수를 높게 부여한 경우 점수를 낮춤  
합산 결과가 60점이 넘을 경우 high_makia라는 파생 변수에 1을 부여, 넘지 않으면 0  



### TIPI 질문 
- 성실성 : {3번 점수 + (8 - '8번 점수')} ÷ 2
- 우호성 : {7번 점수 + (8 - '2번 점수')} ÷ 2
- 정서적 안정성(점수가 낮으면 신경성과 관련): {9번 점수 + (8 - '4번 점수')} ÷ 2
- 개방성 : {5번 점수 + (8 - '10번 점수')} ÷ 2
- 외향성 : {1번 점수 + (8 - '6번 점수')} ÷ 2


(출처 : https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=bhtalk&logNo=220747143871)  


### vCL1 ~ vCL20
해당 단어를 보고 자신이 아는 단어인지 아닌지 0(don't know), 1(know)로 판단  

### age
50세 이상의 참가자들이 nerdiness 값이 높다는 것을 반영  
children, adult, middle age, old age로 분류하여 파생변수 생성  

### religion
특정 종교와 관련하여 nerdiness 값의 변화가 뚜렷함.

### 시간 관련 컬럼 ['introelapse', 'testelapse', 'surveyelapse']
해당 컬럼은 nerdiness의 값과 상관관계가 적다고 판단하여 drop  



