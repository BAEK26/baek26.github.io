<!-- 1f2bf7b1-f6a3-447e-b29e-db97d9bdc195 -->
---
layout: post
comments: true
title: WebSQL 지원 브라우저
categories: [sql]
---

MySQL 실습은 https://www.w3schools.com/sql/ 브라우저에서 진행한다.여기에는 이미 Customers, Orders와 같은 테이블이 있어 연습하고자 하는 sql 쿼리를 한 번에 확인해볼 수 있다는 장점이 있다.

하지만, 요즘 접속해보면 An unspecified error occurred. 와 같은 에로 메시지만 나오고 실행이 잘 안된다. Select * From Orders; 쿼리는 동작하는데 join같은 거는 안 되는것으로 보인다. 

안되는 쿼리 : 

```javascript
SELECT Customers.CustomerID, Orders.OrderID FROM Customers LEFT JOIN Orders USING(CustomerID);

```



그 이유를 찾아보니 내가 사용하고 있는 크롬 브라우저에서 WebSQL을 지원하지 않기 때문이다. 정확히 말하면 더이상 안한다. 2023년 여름 즈음 업데이트된 124 버전부터는 websql을 중단했다. 



w3school 에서 안내하기로 oracle의 Opera나 safari, chrome에서 사용하라고 했는데, 세 브라우저 모두 설치해서 사용했는데도 다 동작이 안된다!

![image](https://www.notion.so/WebSQL-1f2bf7b1f6a3447eb29edb97d9bdc195?pvs=4#fcb3912bcca14ee2b42d5c6d39f2e683)

그래서 해결책은 다음과 같다.



1. https://sqlfiddle.com/mysql/online-compiler 을 이용한다.
1. websql을 지원하는 브라우저를 설치한다. 
위를 참고하면, w3school에서 지원하는 문법이 제한적인 것 같다. 참고하자. 



- Using을 쓰면 안됨
