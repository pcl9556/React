<h3>컴포넌트(Component)</h3>

화면을 구성하는 가장 작은 단위.
function Hello() {
  return <h1 태그>안녕하세요!</h1>;
}

<h3>JSX</h3>

자바스크립트 안에서 HTML처럼 작성하는 문법.
리액트에서 쓰는 JavaScript + XML 문법
const element = <h1 태그>Hello, React!</h1>;

<h3>상태(State) & 속성(Props) </h3>

State: 컴포넌트 내부에서 변하는 값 (예: 입력창 값, 체크 여부)
       컴포넌트 안에서 관리하는 값.
       값이 바뀌면 화면이 자동으로 다시 렌더링됨.
       useState Hook을 사용.
      

Props: 부모 → 자식으로 전달하는 값 (수정 불가)
       부모 컴포넌트 → 자식 컴포넌트로 데이터 전달할 때 사용 (읽기 전용!).

<h3>렌더링(Rendering)</h3>

ReactDOM.createRoot(...).render(<App />)

화면에 컴포넌트를 붙여주는 역할.

<h3>이벤트 처리</h3>

HTML의 onclick, onchange 같은 이벤트를 CamelCase로 사용.

함수(핸들러)를 연결.

<button onClick={() => alert("버튼 클릭!")}>클릭</button>

<h3>useEffect</h3>

컴포넌트가 렌더링된 후에 실행할 코드 작성.

API 호출, 타이머 설정 등에 사용.

<h3>React ↔ Spring Boot 연동(CORS) </h3>
1) 서버(Spring Boot) 설정
- @Configuration으로 한 번만 설정하면 모든 컨트롤러에 적용
정확한 오리진을 지정

2) 프론트(React)에서 요청 보내기 - (fetch/axios) 프론트는 이 값을 읽어서 모든 변경 요청에 X-XSRF-TOKEN 헤더로 보냄
3) 컨트롤러 (세션 로그인 흐름)
4) JWT(토큰)
서버: 로그인 시 Authorization: Bearer <token>을 프론트로 반환
프론트: 토큰을 localStorage/memory에 보관 후 모든 요청 헤더에 포함
서버 CORS: exposedHeaders("Authorization")로 브라우저에서 읽을 수 있게

<h3> iteration </h3>
map() - JSX 요소 반복 렌더링
key - 각 요소 식별을 위한 고유값 (반드시 필요)
filter(), sort() - 반복 전에 조건이나 정렬 가능

<h3> async </h3>
“비동기 함수”를 선언할 때 사용하는 키워드
- 항상 Promise를 반환
- 값을 받으려면 then() 또는 await으로 처리
- 
