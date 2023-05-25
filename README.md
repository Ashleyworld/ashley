# 프로그래머스
# 강원도에 위치한 생산공장 목록 출력하기


문제 설명
다음은 식품공장의 정보를 담은 FOOD_FACTORY 테이블입니다. FOOD_FACTORY 테이블은 다음과 같으며 FACTORY_ID, FACTORY_NAME, ADDRESS, TLNO는 각각 공장 ID, 공장 이름, 주소, 전화번호를 의미합니다.

Column name	Type	Nullable
FACTORY_ID	VARCHAR(10)	FALSE
FACTORY_NAME	VARCHAR(50)	FALSE
ADDRESS	VARCHAR(100)	FALSE
TLNO	VARCHAR(20)	TRUE
문제
FOOD_FACTORY 테이블에서 강원도에 위치한 식품공장의 공장 ID, 공장 이름, 주소를 조회하는 SQL문을 작성해주세요. 이때 결과는 공장 ID를 기준으로 오름차순 정렬해주세요.

예시
FOOD_FACTORY 테이블이 다음과 같을 때

![image](https://github.com/Ashleyworld/ashley/assets/132446112/fa303da5-3518-4e8e-bf23-94a6c6cfcd33)


 

처음에 FACTORY_ID 기준으로 오름차순 정렬해서 나와서 생각보다 쉬운 문제인 줄 알았는데
문제가 강원도만 주소로 나오는걸 틀리고 깨달았다. 구글링해서 다시 넣었다:)


SELECT FACTORY_ID, FACTORY_NAME, ADDRESS
from FOOD_FACTORY
where address like '강원도%'
order by FACTORY_ID asc


