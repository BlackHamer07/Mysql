# 심화과정

## Join부터는 심화라고 생각함

1. Join
  
  - join은 두 테이블을 결합을 할 때 쓰인다
  - (중요) 두 테이블을 결합할 때 두 테이블의 공통적인 부분을 결합하여 결합을 한다.
  - 예를 들어) select * from orders join products on orders.order_id = products.oreder_id 같은 부분을 결합
  - 또한 다른 곳에 위치한 테이블도 결합이 가능하다
  - select * from orders o join sql_inventory.products p on o.order_id = p.order_id 와 같이 다른 위치의 테이블을 결합가능


2. self join
  
  - self join은 자기 자신을 혼자서 결합할 때 쓰인다.
  - 자기 자신을 결합할 때는 공통적인 부분보다 필요한 조건에 맞게 검색되게 하는 것이 중요하다
  - 이해하기 쉽게 설명을 해보자면 CEO,매니저,CEO사번,매니저 사번 등등 입력이 되어있는데 각각의 CEO들의 매니저를 검색하고 싶을 때 사용한다고 하면 된다.
  - (예정) 추후 더 알게된다면 추가 예정

3. multi join (2개 이상의 테이블을 결합할 때)
  
  - 첫번째로 다중 조인을 하면 join을 몇 번을 쓰는 것과 상관없이 join을 쓰면 된다.
  - -> select *
  
       from orders o 
       
        join customers c on o.customer_id = c.customer_id
        
        join order_statuses os on o.status = os.order_status_id
