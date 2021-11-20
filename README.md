# 서비스 이름 & 서비스 소개

<br />
<br />

# 개발 담당 부분

<table>
    <tr align="center">
        <td style="min-width: 150px;">
            <a href="https://github.com/jynam17">
              <img src="https://github.com/jynam17.png" width="100">
              <br />
              <b>남주영</b>
            </a>
        </td>
        <td style="min-width: 150px;">
            <a href="https://github.com/Tekiter">
              <img src="https://github.com/Tekiter.png" width="100">
              <br />
              <b>박건영</b>
            </a> 
        </td>
        <td style="min-width: 150px;">
            <a href="https://github.com/joohaem">
              <img src="https://github.com/joohaem.png" width="100">
              <br />
              <b>이주함</b>
            </a> 
        </td>
    </tr>
    <tr align="center">
        <td>
            쭈일<br/>
            Web FE
        </td>
        <td>
            커삐<br />
            Web FE
        </td>
        <td>
            쭈삼<br />
            Web FE
        </td>
    </tr>
</table>

<br />
<br />

# 코드 컨벤션

### 네이밍 컨벤션

- 폴더와 파일은 카멜 케이스를 사용한다.
- 예외적으로 리액트 컴포넌트를 정의한 파일과 폴더는 파스칼 케이스를 사용한다.
- 변수와 함수 이름은 카멜 케이스를 사용한다.
- 클래스와 인터페이스는 카멜 케이스를 사용한다.

<br />

### 함수 구문

특별한 이유가 없는 한 함수 선언식을 사용한다.

```javascript
function Component() {
  function handleClick() {
    // etc...
  }

  return <button onClick={handleClick}></button>;
}
```

바로 대입해야 하는 람다 함수는 () => {} 구문을 사용한다.

```javascript
function Component() {
  const [value, setValue] = useState("");

  return <input type="text" value={value} onChange={(e) => setValue(e.target.value)} />;
}
```

#### 컴포넌트 프롭 ?

- 프롭들은 단일 props 변수로 받는다.
- 프롭들 각각을 사용할 땐 구조분해 할당을 사용한다.
- 받을 프롭이 없을 땐 변수를 받지 않는다.

```javascript
function Component(props) {
  const { to, from, value, onClick } = props;

  /// etc...
}

function ComponentWithNoProps() {
  /// etc...
}
```

<br />

### 반응형

반응형 코드들이 온갖 컴포넌트에 산재해 있으면 안 된다. 반응형 코드들은 Layout 컴포넌트에만 있어야 한다.

<br />

### CSS

px 단위는 사용하지 않는다. (em, rem 단위 권장)
미디어 쿼리는 직접 작성하지 않고, styles/responsive 모듈의 displaySize() 함수를 사용한다.
색상은 styles/colors 모듈의 colors 안의 상수를 활용한다.

<br />

### Branch Strategy

기능별로 각자 브랜치를 생성해 작업 후, 풀 리퀘스트를 생성해 메인에 머지한다.

<br />
<br />

# 브랜치 전략
