# Unity C#-study

### Unity 기본 조작 단축키

* Q : 화면이동
* W : 게임오브젝트 위치 이동
* E : 게임오브젝트 회전
* R : 게임오브젝트 확대/축소


### C#기본 Method

Method : 코드 묶음
Start Method : 게임이 시작할 때 한번 실행
Update Method : 매 프레임 마다 호출되어 실행
=>만든 메소드는 Start Method나 Update Method에서 함수를 호출하여 실행


### 변수

클래스 안에 선언한 변수 : 멤버변수 => 어디에서든 이용가능
메소드 안에 선언한 변수 : 지역변수 => 메소드 안에서만 이용가능


### 함수

-Debug.Log("") : Console에 log출력
-transform.position.x(or y or z) : 오브젝트의 좌표를 정해줌 => 글로벌좌표
  로컬좌표 => transform.localPosition.x(or y or z)
-GetComponent<기능>() : 인스펙터의 기능들을 가져와 스크립터에서 바꿈
-GameObject.Find(“오브젝트 이름”) : 카메라가 게임 오브젝트 따라움직임
-GetComponent<Rigidbody>().AddForce(Vector3.up) : 오브젝트의 물리적인힘에 변화를 줄때(위의방향으로 힘을 줌)
-Application.LoadLevel(“씬이름”) : 다시 시작
-물체 충돌
  void OnCollisionEnter : 두물체간에 실제 충돌이일어났을 때 - 매개변수(collision)
  void OnTriggerEnter : 특정영역을 지나갔을 때 - (collider)
  

### 사용자 입력
  
-Input.GetAxis(“Horizontal”or“Vertical”) : 키보드의 화살표를 입력받아 양옆or위아래로 이동
-transform.localEulerAngles.x(or y or z) : 축의 회전량구하기
-Input.GetKeyDown(KeyCode.Space(원하는키)) : 사용자 지정 키 입력 받기(키를 누르는순간)
  키를 떼는 순간 => Input.GetKeyUp
  키가 눌려있는 동안 => Input.GetKey
-Input.touchCount>0 : 어딘가 터치가 되어있음
-Input.GetMouseButten(0) : 0번째 마우스버튼(왼쪽버튼)이 눌려져있음
-Input.mousePosition.x(or y or z) : 좌표를 통해 마우스가 어디를 클릭했는지 알수있음
