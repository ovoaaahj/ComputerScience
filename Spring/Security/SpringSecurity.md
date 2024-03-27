<h1>Spring Security</h1><br><br>

<h2>SpringSecurity 란?</h2>
인증(Authentication)과 권한(Authorize) 부여 및 보호기능을 제공하는 프레임워크<br><br>

<h2>인증? 인가?</h2>
인증(Authentication) :: 사용자 본인이 맞는지 확인 <br>
인가(Authorize) :: 그 사용자의 자원 접근 권한이 있는지 <br>

보통 인증 -> 인가 순서대로 진행된다<br><br>

<h2>SpringSecurity 구조</h2>

![image](https://github.com/ovoaaahj/ComputerScience/assets/49386460/3c294da0-1ea6-4031-9cb9-f80412663485)

<h4>1. HttpRequest 수신</h4>
 -   사용자가 로그인 정보와 인증 요청
<h4>2. Authentication Filter 에서 받은 요청을 가지고 UsernamePasswordAuthenticationToken의 인증용 객체 생성</h4>
<h4>3. Filter를 통해 Authentication Token을 Authentication Manager로 전달</h4>
- provider Manager에게 UsernamePasswordToken객체 전달<br>
<h4>4. AuthenticationProvider의 목록으로 인증 시도</h4>
- AuthenticationProvider에 등록된 AuthenticationProvider들을 조회해서 인증 요구
<h4>5. UserDetailService의 요구</h4>
- 실제 데이터 베이스에서 사용자인정정보를 가져오는 UserDetailService에 사용자 정보를 줌
<h4>6. UserDetails를 이용해  User에 대한 정보 탐색</h4>
- 넘겨받은 사용자 정보를 이용해 데이터 베이스에서 찾은 정보인 UserDetail 객체를 만듬
<h4>7. User정보들을 UserDatils 가 UserService로 전달</h4>
- AuthenticationProvider들은 UserDetail 정보를 받고 비교함
<h4>8. 인증이 완료되면 사용자 정보를 담은 Authentication 객체 반환</h4>
