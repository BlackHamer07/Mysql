# 기초문법

  1. select * from ~~


    - 모든 검색구문의 기본적인 문장이다.
    - from -- 테이블에서 전체적인(*) 것을 검색한다.
  2. where 구문


    - select * from ~~ where ~~
    - where 구문에 조건을 쓰게 된다
    - where 구문의 조건에 맞춰서 from에서부터 받아온 테이블에서 조건에 맞춰 검색이된다.
    
    
  3. AND, OR, NOT


    - 대게 where 구문에 쓰인다
    - AND = 여러 조건 모두 만족을 하는가?
    - OR =  여러 조건 중에 적어도 하나는 만족하는가?
    - NOT 부정적인 문구
    
    
  4. IN 


    - AND,OR,NOT과 같이 where구문에 쓰인다
    - 예를 들어 state = 'seoul' or state = 'busan' .... 여러가지를 검색할때
    - state IN ('seoul','busan',...) 간단명료하게 쓰일 수 있다.
    
    
  5. BETWEEN


    - where 구문에 쓰인다
    - 조건중에서도 사이값을 검색할때
    - where weight between 100 and 200 -> 몸무게처럼 사이값을 검색할때
    
    
  6. LIKE


    - where 구문에 쓰인다
    - 문자열을 검색할 때 주로 쓰인다.
    - where name like 'kim%' -> kim으로 시작하는 것을 검색해라
    - where name like '%kim%' -> kim이란 문자가 어디에 있어도 상관이 없으며 kim이란 문자가 있는 것을 검색
    - where name like '%kim' -> kim으로 끝나는 것을 검색해라.
    - where name like '(______)kim' -> (______)는 글자로 취급이 되므로 1글자 뒤에 있는 kim 모든것
    
    
  7. REGEXP


    - where 구문에 쓰인다.
    - Like와 비슷하지만 다른점이 존재함
    - where name REGEXP '^kim' -> kim으로 시작하는 것을 검색해라
    - where name REGEXP 'kim$' -> kim으로 끝나는 것을 검색해라
    - where name REGEXP 'kim|Lee' -> kim,Lee의 사람을 검색해라
    - where name REGEXP '^kim|Lee|Sin' -> kim으로 시작하는 사람을 검색, Lee와Sin이 들어가는 이름 검색
    - where name REGEXP 'kim[skm]' -> kims / kimk / kimm 이렇게 kim뒤에 오는게 skm인 사람을 검색 대괄호가 앞에도 올 수 있다.
    - where name REGEXP 'kim[a-h]' -> 위와 마찬가지로 딸려오는 것을 검색하는데 a~h까지 있는 문자중에서 검색해라
    
  8. is null / is not nulll
    
    
    - null값은 0인값이 아닌 모르는 값을 나타낸다 (중요)
    
    
  9. Order by
    
    
    - where 구문다음에 쓰인다
    - order by는 정렬을 할 때 쓰인다.
    - 내림차순 정렬을 원하면 order by name DESC를 쓴다.
    - 오른차순 정렬을 하게되면 order by name AES를 쓴다.


  10. Limit
    
    
    - 항상 구문 마지막에 쓰이는 것을 명심해야된다.
    - limit 3 -> 3개까지의 검색결과를 도출함
    - 예를 들어서 고객이 10명이고 limit 300을 하게될시 300명은 없지만 고객이 10명이므로 10명의 결과를 낼수 있다.
    - limit 6, 3 -> 오프셋이라고 부른다. 그 이유는 1페이지에 1-3 / 2페이지 4-6 / 3페이지 7-9인데 3페이지의 결과를 내고싶으면 limit 6,3에서 limit 6은 1-6가지의 결과를 넘기고 나머지 3은 6 이후에 3개를 검색하라 이뜻이다.
    
