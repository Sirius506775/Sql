# [ 프로그래머스 SQL 고득점 kit ] - 모든 레코드 조회하기

### **문제 설명**

`ANIMAL_INS` 테이블은 동물 보호소에 들어온 동물의 정보를 담은 테이블입니다. `ANIMAL_INS` 테이블 구조는 다음과 같으며, `ANIMAL_ID`, `ANIMAL_TYPE`, `DATETIME`, `INTAKE_CONDITION`, `NAME`, `SEX_UPON_INTAKE`는 각각 동물의 아이디, 생물 종, 보호 시작일, 보호 시작 시 상태, 이름, 성별 및 중성화 여부를 나타냅니다.

| NAME | TYPE | NULLABLE |
| --- | --- | --- |
| ANIMAL_ID | VARCHAR(N) | FALSE |
| ANIMAL_TYPE | VARCHAR(N) | FALSE |
| DATETIME | DATETIME | FALSE |
| INTAKE_CONDITION | VARCHAR(N) | FALSE |
| NAME | VARCHAR(N) | TRUE |
| SEX_UPON_INTAKE | VARCHAR(N) | FALSE |


동물 보호소에 들어온 모든 동물의 정보를 ANIMAL_ID순으로 조회하는 SQL문을 작성해주세요. SQL을 실행하면 다음과 같이 출력되어야 합니다.

| ANIMAL_ID | ANIMAL_TYPE | DATETIME | INTAKE_CONDITION | NAME | SEX_UPON_INTAKE |
| --- | --- | --- | --- | --- | --- |
| A349996 | Cat | ‣ | Normal | Sugar | Neutered Male |
| A350276 | Cat | ‣ | Normal | Jewel | Spayed Female |
| A350375 | Cat | ‣ | Normal | Meo | Neutered Male |
| A352555 | Dog | ‣ | Normal | Harley | Spayed Female |

### ***1. SQL Kata***
Programmers SQL 고득점 kit Level 1

Select 문제 中 **모든 레코드 조회하기**

---

### ***2. Problem-Solving***

**모든 동물의 정보**를 **ANIMAL_ID 순으로 조회**해야한다.

동물의 정보를 **조회**하기 위해서 **Select**문을 활용하고, **모든 column을 포함**해야하기 때문에 ***** **(Asterisk)**를 사용하여, 모든 값들을 검색한다.

**정렬 기준이 될 column을 지정**하기 위해 **order by**를 사용한다. **desc**를 붙이면 **내림차순**으로 정렬할 수 있으며, 기본은 **오름차순(Asc)**이다.

---

### ***3. Solution***

```
SELECT * FROM ANIMAL_INS ORDER BY ANIMAL_ID;
```
