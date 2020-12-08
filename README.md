# 🏎️ 자동차 경주 게임

> 자동차 경주 게임 프로젝트는 우아한 테크코스 프리코스 2주차 미션 입니다.

자동차 경주 게임은 유저가 자동차의 이름과 개수, 그리고 시도할 횟수를 입력하면 자동차들이 유저가 입력한 횟수만큼 경주하게 되고, 경주한 결과와 최종 우승자가 출력되는 게임입니다.

## 🏆 경주 방법

1. 유저가 원하는 자동차의 이름들을 입력합니다.
   - 각 자동차들의 이름은 쉼표(,)로 구분되며 5자 이하로 입력해야 합니다.
2. 유저가 자동차들이 전진을 시도할 횟수를 입력합니다.
   - 시도할 횟수만큼 자동차들은 랜덤 넘버를 생성해 전진(-)을 시도하게 됩니다.
3. 가장 많이 전진한 자동차가 게임에서 우승합니다.
   - 우승자는 2명 이상일 수 있습니다.

## ✔️ 주어진 요구사항

- [기능요구사항](#기능-요구사항)
- [프로그래밍 요구사항](#프로그래밍-요구사항)
- [추가된 요구사항](#추가된-요구사항)
- [미션 저장소 및 진행 요구사항](#미션-저장소-및-진행-요구사항)

## ✔️ 주어진 참고사항

- [프로그램 실행 결과](#프로그램-실행-결과)

## ✔️ 피드백 정리

- [1주차 피드백 정리](#1주차-피드백-정리)

## ✔️ 구현할 기능 목록

1. 사용자가 입력한 자동차 이름을 받기

   - 각 이름은 5자 이하
   - 쉼표(,)로 구분되어 있음
   - **🚦예외 상황**
     - 사용자가 자동차 이름을 아무것도 입력하지 않았을 때 ex) ""
     - 사용자가 자동차 이름을 6자 이상으로 입력했을 때 ex) "eastwest"
     - 사용자가 자동차 이름을 입력하지 않았을 때 ex) "east,,north,south"
     - 사용자가 자동차 이름을 중복으로 입력했을 때 ex) "east,east,west"

2. 사용자가 입력한 이동 횟수를 받기

   - 자동차 이름을 받은 후, 이동 횟수를 받는 입력 창을 보여줌
   - 이동 횟수는 1회 이상
   - **🚦예외 상황**
     - 사용자가 이동 횟수를 0회 또는 음수로 입력했을 때

3. 각 자동차의 전진/멈춤을 위한 랜덤 값 생성

   - 0 에서 9 사이의 값
   - 랜덤 값이 4 이상이면 전진
   - 랜덤 값이 3 이하이면 멈춤

4. 자동차 게임의 진행 결과 출력

   - 각 자동차 이름 옆에 진행 결과 출력
   - 전진하면 `-` 출력
   - 멈춤이면 출력하지 않음

5. 자동차 게임의 최종 우승자 출력
   - 우승자가 여러명일 경우, 쉼표(,)를 이용해 구분

---

## 기능 요구사항

- 주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.
- 자동차에 이름을 부여할 수 있다. 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
- 자동차 이름은 쉼표(,)를 기준으로 구분하며 이름은 5자 이하만 가능하다.
- 사용자는 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.
- 전진하는 조건은 0에서 9 사이에서 random 값을 구한 후 random 값이 4 이상일 경우 전진하고, 3 이하의 값이면 멈춘다.
- 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.
- 우승자가 여러명일 경우 ,를 이용하여 구분한다.

## 프로그램 실행 결과

![실행이미지](images/result.gif)
![실행이미지](images/result.jpg)

## 프로그래밍 요구사항

- 사용자가 잘못된 입력 값을 작성한 경우 `alert`을 이용해 메시지를 보여주고, 재입력할 수 있게 한다.
- 외부 라이브러리(jQuery, Lodash 등)를 사용하지 않고, 순수 Vanilla JS로만 구현한다.
- **자바스크립트 코드 컨벤션을 지키면서 프로그래밍** 한다
  - [https://google.github.io/styleguide/jsguide.html](https://google.github.io/styleguide/jsguide.html)
  - [https://ui.toast.com/fe-guide/ko_CODING-CONVENSION/](https://ui.toast.com/fe-guide/ko_CODING-CONVENTION)
- **indent(인덴트, 들여쓰기) depth를 3이 넘지 않도록 구현한다. 2까지만 허용**한다.
  - 예를 들어 while문 안에 if문이 있으면 들여쓰기는 2이다.
  - 힌트: indent(인덴트, 들여쓰기) depth를 줄이는 좋은 방법은 함수(또는 메소드)를 분리하면 된다.
- **함수(또는 메소드)가 한 가지 일만 하도록 최대한 작게** 만들어라.

### 추가된 요구사항

- **함수(또는 메소드)의 길이가 15라인을 넘어가지 않도록 구현한다.**
- 함수(또는 메소드)가 한 가지 일만 잘 하도록 구현한다.
- 자동차의 이름을 입력하는 input 태그는 `#car-names-input` id값을 가진다.
- 자동차의 이름을 제출하는 button 태그는 `#car-names-submit` id값을 가진다.
- 레이싱 횟수를 입력하는 input 태그는 `#racing-count-input` id값을 가진다.
- 레이싱 횟수을 제출하는 button 태그는 `#racing-count-submit` id값을 가진다.
- 다음 Car 객체를 만들고, new 를 이용해 인스턴스를 만든다.

```javascript
function Car(name) {
  this.name = name;
}

class Car {
  constructor(name) {
    this.name = name;
  }
}
```

- 변수 선언시 `var` 를 사용하지 않는다. `const` 와 `let` 을 사용한다.
  - [const](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/const)
  - [let](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/let)
- `import` 문을 이용해 스크립트를 모듈화하고 불러올 수 있게 만든다.
  - [https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/import](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/import)
- `template literal`을 이용해 데이터와 html string을 가독성 좋게 표현한다.
  - [https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Template_literals](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Template_literals)

## 미션 저장소 및 진행 요구사항

- 미션은 [https://github.com/woowacourse/javascript-racingcar-precours](https://github.com/woowacourse/javascript-racingcar-precourse) 저장소를 fork/clone해 시작한다.
- **기능을 구현하기 전에 javascript-racingcar-precourse/docs/README.md 파일에 구현할 기능 목록**을 정리해 추가한다.
- **git의 commit 단위는 앞 단계에서 README.md 파일에 정리한 기능 목록 단위로 추가**한다.
- [프리코스 과제 제출](https://github.com/woowacourse/woowacourse-docs/tree/master/precourse) 문서 절차를 따라 미션을 제출한다.

## 1주차 피드백 정리

### 📌Readme

- Readme.md를 계속 업데이트 한다.

  - 살아있는 문서를 만들기 위해 노력하자.

- Readme.md를 상세히 작성한다.

  - 해당 프로젝트가 어떤 프로젝트인지 마크다운으로 작성해 소개하는 문서이다. 어떤 프로젝트이고, 어떤 기능을 담는지 기술한다.

- 기능 목록 구현을 재검토한다.

  - 기능 목록을 너무 상세히 작성하지 않는다. (언제든 변경될 수 있기 때문)
  - 구현해야 할 기능 목록을 정리하는 데 집중한다.
  - **예외적인 상황도 기능 목록에 정리한다.**

    - 기능을 구현하며 계속해서 추가해 나간다.

### 📌Naming

- `이름`을 통해 의도를 드러내라.

  - 적절한 이름
    - 변수, 함수, 클래스의 역할에 대한 의도가 명확히 드러나는 이름
  - 적절하지 않은 이름
    - 연속적인 숫자를 덧붙인 이름
    - 불용어(Info, Data, a, an, the)가 추가된 이름

- 의도를 드러낼 수 있다면 이름이 길어져도 괜찮다.

### 📌Convention

- `space`도 convention이다.

  - for, while, if문 사이의 space도 convention이다.

- `space`와 `tab`을 혼용하지 않고 하나만 사용한다.

  - pull request를 보낸 후 들여쓰기를 확인하는 습관을 들이자.

- 불필요한 공백 라인을 만들지 않는다.

- `구현 순서`를 통일하며 프로그래밍 한다.

### 📌Git

- git `commit message`를 의미있게 작성한다.

### 📌Coding

- 중복을 최대한 없애고, `컴포넌트화` 하여 재사용한다.

- var를 사용하지 않는다.

- 의미없는 주석을 달지 않는다.

  - 가능하면 변수 이름, 함수(메소드) 이름을 통해 의도를 드러내고, 의도를 드러내기 힘든 경우 주석을 단다.

- `linter`와 `code formater`의 기능을 활용해라.(오류 사전 예방)

  - lint - `eslint`
    - 정적 분석 도구
    - runtime error를 사전에 잡아줄 수 있다.
  - code formatter - `prettier`
    - 개발자가 작성한 코드가 정해진 코딩 스타일을 따르도록 변환해주는 도구
