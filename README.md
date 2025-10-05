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
