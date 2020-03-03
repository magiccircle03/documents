# GraphQL

## 링크

- [공식 링크(배우기)](https://graphql-kr.github.io/learn/)

## GraphQL이란?

- 페이스북이 발표한, `API를 위한 쿼리 언어`
- SQL과 GQL 비교

| 비교           | sql                                                          | gql                                                         |
| -------------- | ------------------------------------------------------------ | ----------------------------------------------------------- |
| 목적           | 데이터베이스 시스템에 저장된 데이터를 효율적으로 가져오는 것 | 웹 클라이언트가 데이터를 서버로 부터 효율적으로 가져오는 것 |
| 문장 호출 위치 | 주로 백앤드 시스템                                           | 주로 클라이언트 시스템                                      |

## 쿼리 예시

- SQL

```
SELECT name, friends FROM hero;
```

- GQL

```
{
 hero {
   name
   friends {
     name
   }
 }
}
```

## 쿼리와 뮤테이션

- 쿼리 : Read
- 뮤테이션 : Create, Update

쿼리로도 데이터를 변경할 수 있지만
명시적으로
데이터를 가져오는 것은 쿼리, 변경하는 것은 뮤테이션을 사용한다.

## REST API와 비교

| 비교                                                     | REST API                                       | GQL                                   |
| -------------------------------------------------------- | ---------------------------------------------- | ------------------------------------- |
| [Endpoint](https://graphql.org/learn/serving-over-http/) | 여러 개                                        | 주로 하나 (/graphql)                  |
| 응답 구조                                                | 대개 Endpoint에 따라 응답의 구조가 정해져 있음 | 요청할 때 사용한 Query 문에 따라 다름 |

### Rest와 비교한 장점

- HTTP 요청의 횟수를 줄일 수 있음

  - `REST API` 는 각 Resource 종류 별로 요청을 해야 -> 요청 횟수가 필요한 Resource 의 종류에 비례
  - `GraphQL` 은 원하는 정보를 하나의 Query 에 모두 담아 요청하는 것이 가능(GraphQL 쿼리는 연관된 객체와 필드를 탐색 할 수 있으므로)

* HTTP 응답 Size 를 줄일 수 있다.

  - `REST API` 는 응답의 형태가 정해져있어 필요한 정보만 부분적으로 요청하는 것이 힘들다.
  - `GraphQL` 은 원하는 대로 정보를 요청하는 것이 가능하다.

### 예시1

`GraphQL` 쿼리는 연관된 객체와 필드를 탐색 할 수 있으므로,  
기존 `REST` 구조처럼 여러번 요청을 수행하는 대신 한번의 요청으로 많은 데이터를 가져올 수 있다.

```
{
  hero {
      name
      friends {
         name
      }
  }
}
```

```json
{
  "data": {
    "hero": {
      "name": "R2-D2",
      "friends": [
        {
          "name": "Luke Skywalker"
        },
        {
          "name": "Han Solo"
        },
        {
          "name": "Leia Organa"
        }
      ]
    }
  }
}
```

### 예시2

- `REST`와 같은 시스템에서는 -> 요청에 쿼리 파라미터와 URL 세그먼트같은 단일 인자들만 전달할 수 있다.
- `GraphQL`에서는 -> 모든 필드와 중첩된 객체가 인자를 가질 수 있으므로 여러번의 API fetch를 완벽하게 대체할 수 있음.  
  필드에 `인자`를 전달하면, 모든 클라이언트에서 개별적으로 처리하는 대신 서버에서 데이터 변환을 한 번만 구현할 수도 있다.

```
{
  human(id: "1000") {
    name
    height(unit: FOOT)
  }
}
```

```json
{
  "data": {
    "human": {
      "name": "Luke Skywalker",
      "height": 5.6430448
    }
  }
}
```

## 기타 사용법

### 프래그먼트를 이용한 재사용 (함수처럼)

```
{
  leftComparison: hero(episode: EMPIRE) {
    ...comparisonFields
  }
  rightComparison: hero(episode: JEDI) {
    ...comparisonFields
  }
}

fragment comparisonFields on Character {
  name
  appearsIn
  friends {
    name
  }
}
```

```json
{
  "data": {
    "leftComparison": {
      "name": "Luke Skywalker",
      "appearsIn": ["NEWHOPE", "EMPIRE", "JEDI"],
      "friends": [
        {
          "name": "Han Solo"
        },
        {
          "name": "Leia Organa"
        },
        {
          "name": "C-3PO"
        },
        {
          "name": "R2-D2"
        }
      ]
    },
    "rightComparison": {
      "name": "R2-D2",
      "appearsIn": ["NEWHOPE", "EMPIRE", "JEDI"],
      "friends": [
        {
          "name": "Luke Skywalker"
        },
        {
          "name": "Han Solo"
        },
        {
          "name": "Leia Organa"
        }
      ]
    }
  }
}
```

### 변수 사용

```
query HeroNameAndFriends($episode: Episode) {
  hero(episode: $episode) {
    name
    friends {
      name
    }
  }
}
```

```
{
  "episode": "JEDI"
}
```

```json
{
  "data": {
    "hero": {
      "name": "R2-D2",
      "friends": [
        {
          "name": "Luke Skywalker"
        },
        {
          "name": "Han Solo"
        },
        {
          "name": "Leia Organa"
        }
      ]
    }
  }
}
```

- 변수 정의는 위 쿼리에서 `(\$episode: Episode)` 부분
- 선언된 모든 변수는 스칼라, 열거형, input object type이어야 함 ([타입에 대한 상세 정보 LINK](https://graphql-kr.github.io/learn/schema/))

## 참고링크

- **[GraphQL 소개](https://graphql-kr.github.io/learn/) : 공식문서. 상세한 사용 방법과 예제 有**
- [GraphQL 개념잡기](https://tech.kakao.com/2019/08/01/graphql-basic/)
- [GraphQL과 RESTful API](https://www.holaxprogramming.com/2018/01/20/graphql-vs-restful-api/)
