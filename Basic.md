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
    - where name REGEXP 'kim[skm]' -> kims / kimk / kimm 이렇게 뒤에 오는게 skm인 사람을 검색 대괄호가 앞에도 올 수 있다.
