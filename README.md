# 숫자 야구 게임 (TDD 따라하기)
## 진행 방법
* 숫자 야구 게임 요구사항을 파악한다.
* 요구사항에 대한 구현을 완료한 후 자신의 github 아이디에 해당하는 브랜치에 Pull Request(이하 PR)를 통해 과제를 제출한다.

## 과제 제출 과정
* [과제 제출 방법](https://github.com/next-step/nextstep-docs/tree/master/precourse)




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

* **숫자야구의 숫자**  
  1. 주어진 숫자에 대한 유효성 체크 기능
        - 숫자는 3자리 이어야 하며, 서로 다른 수 이며, 1 ~ 9를 가지고 있어야 한다. 
  2. 숫자야구의 숫자를 랜덤값으로 생성하는 기능
        - 유효성에 위배 되면 재생성
  

* **컴퓨터**
  1. 컴퓨터가 랜덤한 숫자를 선택 하는 기능.
         
  2. 플레이어의 숫자를 판별하여 힌트를 반환 기능
      - 볼 인지 판단 하는 반환
      - 스트라이크 판단 하는 반환
      - 모두 틀리면 판단 하는 낫딩 반환
  
    
* **플레이어**
  1. 플레이어는 숫자 3개를 입력 기능 
     - 숫자의 유효성이 안맞으면 에러 메시지를 노출하고 재입력한다. 
  2. 플레이어의 게임 재 시작과 게임종료를 입력을 받아 전달하는 기능 
     - 1 이면 시작 2이면 게임 종료
  

* **GAME**

  1. 게임 재시작 기능
  2. 게임 종료 기능
     - 재시작을 입력 하면 게임이 재시작이 된다.
     - 1 이면 시작 2이면 게임 종료 
     
  3. 화면 출력 기능 
      - 힌트 출력
      - 에러 메시지 출력
      - 게임 진행상황 출력

  
    






