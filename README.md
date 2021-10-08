# 숫자 야구 게임 (TDD 따라하기)
## 
* 요구사항분석 문서는 항상 변할 수 있다. 이를 인지하고 업데이트 해나간다.
* 테스트 가능한 부분부터 TDD로 도전 (쉬운거 )


## 기능 요구사항

* 기본적으로 1부터 9까지 서로 다른 수로 이루어진 3자리의 수를 맞추는 게임이다.

* 같은 수가 같은 자리에 있으면 스트라이크, 다른 자리에 있으면 볼 같은 수가 전혀 없으면 포볼 또는 낫싱이란 힌트를 얻고,
  그 힌트를 이용해서 먼저 상대방(컴퓨터)의 수를 맞추면 승리한다.

    * [예시]

      |상대방(컴퓨터)의 수|힌트|
      |--------------|---|
      |426|1스트라이크|
      |456|1스트라이크 1볼|
      |789|1낫싱|

* 위 숫자 야구게임에서 상대방의 역할을 컴퓨터가 한다.   
  컴퓨터는 1에서 9까지 서로 다른 임의의 수 3개를 선택한다.   
  게임 플레이어는 컴퓨터가 생각하고 있는 3개의 숫자를 입력하고, 컴퓨터는 입력한 숫자에 대한 결과를 출력한다.


* 이 같은 과정을 반복해 컴퓨터가 선택한 3개의 숫자를 모두 맞히면 게임이 종료된다.
  게임을 종료한 후 게임을 다시 시작하거나 완전히 종료할 수 있다.  


* 사용자가 잘못된 값을 입력할 경우 [ERROR]로 시작하는 에러 메시지를 출력하고 게임을 계속 진행할 수 있어야 한다.

## 기능 목록  

* 1 ~ 9의 숫자 중 랜덤으로 3개의 숫자 구현한다
* 사용자로 부터 입력 받은 3개 숫자 예외처리
  * 1 ~ 9의 숫자인가
  * 중복값이 있는가
  * 3자리인가
* 위치는 다른데 숫자 값이 같은경우 - 볼
* 숫자 값이 다른경우 - 낫싱
* 사용자가 입력한 값에 대한 실행결과를 구한다.


---
com / user  
123, 456 --> noting  
123, 245 -> 1ball  
123, 145 -> 1strike

기능을 먼저 쪼개 보자
--- 
com / user
1 4 , 1 4 -> strike
1 4 , 2 4 -> ball
1 4 , 2 5 -> notting



  
    







