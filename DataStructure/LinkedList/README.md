# 연결 리스트

![image](https://user-images.githubusercontent.com/95271528/147350666-561ced3f-4033-4741-a3f0-70c320d221a6.png)

각 노드가 데이터 필드와 포인터 필드로 이루어져, 포인터 필드가 다음 노드의 주소를 가리키는 구조
+ 헤드(head) 노드는 첫 번째 노드의 주소를 저장하는 용도로, 데이터 필드를 사용하지 않는다.

## 연결 리스트의 종류

### 단순 연결 리스트(Singly Linked List)

![image](https://user-images.githubusercontent.com/95271528/147350666-561ced3f-4033-4741-a3f0-70c320d221a6.png)

각 노드가 데이터 필드와 하나의 포인터 필드로 이루어져, 포인터 필드가 다음 노드의 주소를 가리키고 마지막 노드의 포인터 필드는 NULL이 저장된다.


### 원형 연결 리스트 (Circular Linked List)

![image](https://user-images.githubusercontent.com/95271528/147351617-a759e7e5-0bbd-4e54-a664-354a7baec8f0.png)

단순 연결 리스트에서 마지막 노드의 포인터 필드가 NULL값이 아닌 첫 번째 노드의 주소 값을 저장한다.

### 이중 연결 리스트 (Doubly Linked List)

![image](https://user-images.githubusercontent.com/95271528/147352615-09ffcfce-55ca-46ac-a606-de066b593f8d.png)

각 노드가 데이터 필드와 두 개의 포인터 필드로 이루어져, 각각의 포인터 필드가 previous 노드의 주소와 next 노드의 주소를 저장한다.

## 배열과 연결 리스트의 비교
+ 배열은 데이터가 메모리의 연속된 공간에 저장되지만, 연결 리스트는 연속적으로 저장하지 않는다.
+ 배열은 임의 접근(Random Access) 방식을 사용하고, 연결 리스트는 순차 접근(Sequential Access) 방식을 사용한다.
  + 원소에 접근하는 시간 복잡도는, 인덱스를 알고 있다면 배열은 O(1), 연결 리스트는 O(n)이다.
+ 데이터 삽입
  + 배열
    + 배열의 맨 뒤에 삽입 시엔 O(1), 그 외 위치에 삽입 시엔 원소를 이동시켜야 하므로 O(n)
  + 연결 리스트
    + 연결 리스트의 맨 앞에 삽인 시엔 O(1), 그 외 위치에 삽입 시엔 탐색으로 인해 O(n)
+ 데이터 삭제
  + 배열
    + 배열의 맨 뒤 원소 삭제 시엔 O(1), 그 외 위치 원소의 삭제 시엔 원소를 이동시켜야 하므로 O(n)
  + 연결 리스트
    + 연결 리스트의 맨 앞 원소 삭제 시엔 O(1), 그 외 위치의 원소 삭제 시엔 탐색으로 인해 O(n)

### 연결 리스트의 장점
+ 배열은 선언 시에 크기가 정해져 크기의 변경에 드는 비용이 큰 반면, 연결 리스트는 크기를 조정하는 것이 간단하다.
+ 배열은 중간에 데이터 삽입(삭제)을 하기 위해서 해당 위치 뒤에 있는 데이터를 모두 이동시키는 작업이 필요하지만, 연결 리스트는 포인터 필드의 값만 수정해 주면 되므로 간단하다.

### 연결 리스트의 단점
+ 데이터의 접근, 탐색에 드는 비용이 크다.

## 삽입 (단순 연결 리스트에서)

![image](https://user-images.githubusercontent.com/95271528/147357565-3930b918-d373-4446-bd53-107644a50254.png)

A와 C 사이에 B를 삽입하는 경우
+ C의 주소를 저장하고 있던 A의 포인터를 B의 주소를 저장하도록 수정
+ B의 포인터가 C의 주소를 가리키도록 함.

## 삭제

![image](https://user-images.githubusercontent.com/95271528/147357774-40d89e34-00a2-4db5-9bc2-9a791be3e46d.png)

A B C 순서로 저장된 연결리스트에서 B를 삭제하는 경우
+ B의 주소를 저장하고 있던 A의 포인터를 B의 다음 노드인 C의 주소를 저장하도록 수정
