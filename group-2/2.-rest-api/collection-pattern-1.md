# Collection Pattern 적용



> ## 학습 키워드
>
> * CQS



## CRUD

1. Create
2. Read
3. Update
4. Delete

## CQS

* **Command와 Query를 분리**하자는 개념
  1. command-> 상태가 변함, 안전하지 않음 (Create, Update, Delete)
  2. Query -> 상태 변환X, 안전함,  분산 캐시등이 수월함 (Read)

###
