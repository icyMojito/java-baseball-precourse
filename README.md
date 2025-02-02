# [숫자 야구 게임]의 기능 목록 #

#### ▦1단계: 1부터 9까지 서로 다른 수로 이루어진 3자리의 수를 뽑아 컴퓨터의 숫자로 지정한다. ####

- 1부터 9 중에서 하나의 숫자를 랜덤으로 뽑는다.
- 앞서 뽑았었던 숫자들과 중복인지 아닌지 검사하고, 중복이면 *1단계의 처음*부터 재실행한다.
- 중복이 아니면 컴퓨터의 숫자에 차례대로 추가하고, *1단계의 처음*부터 재실행한다.  
- 컴퓨터의 숫자가 3자리가 되면 컴퓨터의 숫자 지정 작업을 종료한다.  

#### ▦2단계: 사용자에게 1부터 9까지 서로 다른 수로 이루어진 3자리의 수를 입력받는다. ####

- 사용자에게서 데이터를 입력받는다.  
- 입력된 값이 필요한 조건들에 맞는지 검사하고, 조건 중 한 개라도 맞지 않는다면 *2단계의 처음*부터 재실행한다.  
  - 입력된 값은 3자리의 숫자이다.  
  - 입력된 값에는 0이 포함되지 않는다.  
  - 입력된 값에는 중복된 숫자가 없다. 

#### ▦3단계: 컴퓨터의 숫자와 사용자의 숫자를 한 자리씩 비교하여 판정된 결과를 반환한다.
- 컴퓨터의 숫자와 사용자의 숫자가 전부 다른 숫자이면 낫싱을 반환한다.  
- 컴퓨터의 숫자와 사용자의 숫자 중 위치와 모양이 모두 같은 숫자의 개수를 스트라이크 개수로 구한다.  
- 컴퓨터의 숫자와 사용자의 숫자 중 위치는 다르지만 모양이 같은 숫자의 개수를 볼 개수로 구한다.  
- 스트라이크와 볼 개수를 반환하되, 개수가 0인 판정은 반환하지 않는다.  

#### ▦4단계: 게임종료조건을 만족할 때까지 사용자의 입력과 판정 결과 반환을 지속한다.
- *3단계*에서 게임종료조건인 3스트라이크를 반환받지 못하면 *2단계의 처음*부터 재실행한다.  
- *3단계*에서 게임종료조건인 3스트라이크를 반환받으면 게임 종료 안내 메세지를 출력한다.  

#### ▦5단계: 게임종료 후 사용자에게 게임의 재시작 혹은 종료 요청을 입력받는다.
- *4단계*에서 게임종료조건을 만족하면 사용자에게 게임을 새로 시작할 지 종료할 지 묻는 안내 메세지를 출력한다.  
- 사용자에게 안내 메세지에 따른 요청 데이터를 입력받는다.  
- 입력된 값이 필요한 조건들에 맞는지 검사하고, 조건 중 한 개라도 맞지 않는다면 *5단계 처음*부터 재실행한다.  
  - 입력된 값은 숫자이다.  
  - 입력된 값은 안내 메세지에 기재된 숫자 중 하나이다.  
- 입력된 값이 새로운 게임 시작 요청이면 1단계부터 재실행하고, 종료 요청이면 아무런 작업도 실행하지 않는다.