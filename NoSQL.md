출처 : [Understanding the Different Types of NoSQL Databases](https://www.mongodb.com/scale/types-of-nosql-databases)

## Contents
###  What NoSQL databases have in common
NoSQL databases는 대용량 데이터 및 트래픽에 대한 SQL database의 한계로 개발되었습니다.
다양한 사례에서 relational, 관계형 데이터베이스에 비해 비용 절감이 가능하며, 유연한 schema model과 다수의 서버에 걸쳐 수평적으로 확장 가능하도록 설계된 구조는 단일 서버에서 감당하지 못하는 대량의 데이터와 application 부하를 해결 가능합니다.

아래의 이유들로 NoSQL의 인기가 상승하고 있습니다.
<ol>
  <li>개발 속도가 빠릅니다</li>
  <li>다양한 형태의 데이터 구조를 더 쉽게 처리하고 envolved, 발전 시킬 수 있습니다</li>
  <li>SQL로는 많은 양의 데이터를 경제적으로 처리하기 어렵습니다</li>
  <li>SQL로는 대량의 트래픽과 zero downtime에 대한 need를 충족시키기 어렵습니다</li>
  <li>새로운 application paradiam에 대한 지원이 용이합니다</li>
</ol>

#### zero downtime & details
<details>
  <summary>데이터를 경제적으로 처리한다란?</summary>
1. 확장성
  NoSQL database는 수평적으로 확장이 가능하기에, 여러 서버에 데이터를 분산하여 처리할 수 있습니다. 덕분에 대량의 데이터나 높은 트래픽을 처리하는데 적합합니다.
  SQL database는 단일 서버의 성능 한계에 도달할 경우, 추가적인 하드웨어나 인프라 구성이 필요할 수 있습니다.

2. 유연한 schema
   데이터 모델의 구조를 유연하게 변경하거나 새로운 필드를 추가할 수 있습니다. 덕분에 application의 요구사항이 변경되는 경우에도 데이터 모델을 쉽게 수정할 수 있습니다. SQL은 엄격한 schema 규칙을 따르기에 데이터 모델의 변경이 어려울 수 있습니다.

3. 운영 비용
   NoSQL database는 대부분 opensource로 제공되며, 상대적으로 저렴한 비용으로 사용할 수 있습니다.
</details>

<details><summary>
  Zero downtime이란?
  </summary>
  시스템 또는 application의 연속적인 가용성을 의미합니다. 다시 말해 서비스 중단 없이 시스템을 계속해서 운영할 수 있음을 나타냅니다.

SQL database의 경우, 보통 주기적인 유지보수나 업그레이드 작업을 위해 시스템을 일시적으로 중지시켜야 할 수 있습니다.

NoSQL 데이터베이스는 일반적으로 데이터의 분산 처리와 복제를 통해 zero downtime을 달성할 수 있습니다. 데이터가 여러 서버에 분산되어 저장되고, database의 복제 메커니즘을 통해 데이터의 일관성과 가용성을 보장합니다. 덕분에 개별 서버에서 장애가 발생하거나 유지 보수를 위해 서버를 중지해도 다른 복제된 서버에서 서비스를 계속할 수 있습니다.
  </details>

  <details><summary>
  새로운 어플리케이션 패러다임이란?
  </summary>
  기존의 전통적인 개발 및 아키텍쳐 접근방식에서 벗어나 새로운 방식으로 어플리케이션을 개발하고 구축하는 것을 의미합니다. 다양한 기술과 개념을 포함하며, 그중 일부는 다음과 같습니다.

1. 마이크로 서비스 아키텍쳐
2. 컨테이너화
3. 서버리스 컴퓨팅
4. 데이터 스트리밍 및 실시간 처리


  </details>

## Understanding differences in the 4 types of NoSQL databases

### Document databases
Document databases는 data를 JSON, BSON, 또는 XML document로 저장합니다. document database에서 document는 중첩 가능합니다. 특정 element는 인덱싱되어 빠르게 querying할 수 있습니다.

Document는 application의 data 객체에 더 가까운 형태로 저장되고 검색됩니다. 덕분에 application에서 data를 사용할 때 translation에 소요되는 비용이 감소합니다. 이에 반해 SQL data는 application과 storage간 data를 옮길 때 자주 조립되고, 분해되어야만 합니다

Document database는 application의 요구사항에 맞게 필요에 따라 document structures를 유연하게 변경할 수 있습니다.시간이 지나면서 application 요구사항이 변경되어도 data structure를 조정하여 개발자가 데이터를 통제할 수 있습니다. 반면 SQL database에서는 struct of a database를 change하기 위해 datase administrator, 관리자의 도움이 필요할 수 있습니다.

NoSQL중 가장 널리 사용되는 document database는 일반적으로 scale-out(확장) 아키텍쳐로 구현되며 data volume과 traffic의 scalability(확장 가능성)에 대한 명확한 방법을 제공합니다.

추천 글 : [Comparing MongoDB vs. PostgreSQL](https://www.mongodb.com/compare/mongodb-postgresql)
<details><summary>
  개발자와 관리자
  </summary>
  1. 개발자( developer )
  S/W를 설계, 개발, 구현하는 역할을 수행합니다. 
  주로 프로그래밍 언어를 사용하여 코드를 작성하고, application의 기능과 로직을 구현합니다.

2. 관리자
   system, network, database 등의 intrastructure를 관리하고 유지보수하는 역할을 수행합니다.

주로 시스템의 안정성, 보안, 성능 , 가용성 등을 유지하기 위한 작업을 담당합니다.

시스템 및 네트워크 설정, 사용자 계정 및 권한 관리, 백업 및 복구, 모니터링 등을 수행합니다.

데이터베이스 관리자는 데이터베이스 설치, 구성, 백업, 복구, 성능 최적화 등을 담당합니다.

주로 운영 환경에서 작업하며, 시스템의 안정성과 성능을 유지하고 문제를 해결하기 위해 노력합니다.

3. 요약
   개발자는 주로 S/W의 개발에 집중하고, 관리자는 system과 infrastructure 관리 및 운영에 전념합니다. 그러나 일부 조직에서는 역할이 겹칠 수 있으며, 혼합된 역할을 수행하는 사람도 있을 수 있습니다.
  </details>

### Key-value stores
가장 심플한 NoSQL은 key-value store입니다. database의 모든 data element는 attribute name, 속성 이름(또는 "key")과 value을 포함한 key-value 쌍으로 저장됩니다.
일종의 관계형 데이터베이스와 비슷하기도 한데, 오직 두 개의 열로 구성되어, 하나는 key 또는 attribute name이며 다른 하나는 value 입니다.

쇼핑 카트, 사용자 프로필 등에서 사용됩니다.
쇼핑 카트에서는 각 항목들을 key-value 쌍으로 저장할 수 있고,
사용자 프로필에서는 각 사용자의 attribute와 value를 key-value 쌍으로 저장하여 빠른 검색과 수정을 보장할 수 있습니다.


### Column-oriented databases
#### 특장점
관계형 데이터베이스에서 데이터를 행 단위로 저장하고 읽는 반면, column store는 열 단위로 구성됩니다.
특정 열의 데이터에 대해 분석할 때 불필요한 데이터의 메모리를 소모하지 않고 즉시 원하는 열의 데이터들을 읽을 수 있습니다.

column은 일반적으로 동일한 유형으로 구성되며, 더 효율적인 압축이 가능하여 읽기 속도가 더욱 빨라질 수 있습니다.
특정 column의 값을 빠르게 집계할 수 있기 때문에 (매출 총 합산 등) 분석용으로 사용되는 경우가 많습니다

#### 단점
데이터를 쓰는 방식이 strong consistency을 유지하기 매우 어렵게 합니다.
반면 관계형 database는 행 데이터가 연속적으로 디스크에 쓰이기 때문에, 이러한 문제가 발생하지 않습니다.


<details><summary>
 	What is 'strong consistency'?
  </summary>
 	strong consistency는 분산 시스템에서 데이터 일관성을 보장하는 개념입니다. <br>동시에 여러 작업이 발생하는 환경에서 데이터의 일관성과 정확성을 유지하기 위해 사용됩니다.<br><br>

일관성은 분산 시스템에서 매우 중요한 특성이며, 다수의 node로 구성된 분산 시스템에서 동일한 데이터에 대하여 병렬로 접근하고 업데이트 할 때 data의 상태를 일관되게 유지하는 것을 말합니다.<br>

  </details>


[strong consistency와 eventual consistency간 균형 유지_google](https://cloud.google.com/datastore/docs/articles/balancing-strong-and-eventual-consistency-with-google-cloud-datastore?hl=ko)

### Graph databases

Graph databases는 data elements간의 관계에 집중합니다.
각 element는 node로 저장됩니다 (소셜 미디어 그래프의 사람 처럼).
element들의 connection들은 link 또는 relationship라고 불리웁니다.

graph database에서 connections들은 database의 first-class elements, 일등급 요소로 취급되며 직접 저장됩니다.

relational database에서는 relation, 관계를 표현하기 위해 데이터를 사용하며 linkes are implied, 묵시적으로 연결됩니다.

Graph database는 data elements간의 connection, 연결을 capture & search하는데 최적화되어있습니다. 덕분에 SQL에서 여러 테이블을 JOIN하는 작업의 overhead를 overcoming, 극복합니다.

Graph queries 만으로 실무를 운영하기는 어렵습니다. 때문에 대부분 traditional database와 함께 운영됩니다.

사용 사례로는 social network, knowledge graph, fraud detection 등이 있습니다.

<details><summary>
	capture connection?  
  </summary>
  Graph database에서 connection capture는 data element간의 relation을 명시적으로 저장하고 관리하는 과정을 의미합니다. 
</details>
  


