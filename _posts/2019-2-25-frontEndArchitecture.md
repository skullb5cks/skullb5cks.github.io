---
layout: post
title: front-end architecture with nodejs
---

nginx, nodejs(graphql, expressjs, nextjs), tomcat(rest api), db
  
nodejs 사용이유  
1. SSR
2. view를 위한 rest api 조합(graphql)  
  - https://www.prisma.io/blog/how-to-wrap-a-rest-api-with-graphql-8bf3fb17547d  
3. 인증  
  - SPA의 라우터 마다 인증을 다르게 가저갈 경우 노드서버에서 처리가 가능  
  
    
graphql 사용이유
1. 필요하지 않은 정보는 가져오지 않는다.(over fetching 없는 리소스 구현)
2. 다중 api 요청이 필요한 경우 하나의 api로 응답할 수 있다. (under fetching)
  

Todo  
1. graphql 
2. graphql with rest api (rest api를 sync하여 사용할필요가 없다. 기존 api는 그대로 놔두고 graphql를 위한 end-point만 추가 한다)  
  
reference  
- https://www.slideshare.net/Kivol/graphql-in-action-rest  
