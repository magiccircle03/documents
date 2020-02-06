# grommet [(공식 링크)](https://v2.grommet.io/)

![그림](https://trello-attachments.s3.amazonaws.com/5e1bc202db7fa64ef4e965c4/5e39387f87dc0c300f09f54c/6168443744a143c9fd7b1b9d2c725df0/image.png)

## 튜토리얼

1. 설치
   ```
   yarn add grommet styled-components
   ```
2. 이런 식으로 임포트해서
   ```
   import { Grommet } from 'grommet';
   ```
3. 이런 식으로 사용할 수 있다!

   ```html
   <Grommet plain>
     <header className="App-header">
       <p>Edit <code>src/App.js</code> and save to reload.</p>
       <a
         className="App-link"
         href="https://reactjs.org"
         target="_blank"
         rel="noopener noreferrer"
       >
         Learn React
       </a>
     </header>
   </Grommet>
   ```

## 튜토리얼 more

[더 자세한 그로멧 튜토리얼 링크](https://github.com/grommet/grommet-starter-new-app) 에서
그로멧 사용법을 더 익힐 수 있습니다.

## 컴포넌트들

[제공 컴포넌트 보기 링크](https://v2.grommet.io/components) 에서

- 그로멧이 제공하는 컴포넌트들
- 컴포넌트의 props들 (커스텀)

를 확인할 수 있습니다.

## 스토리북

[그로멧 스토리북 링크](https://storybook.grommet.io/?path=/story/all--all) 에서

- 더 구체적인 예시와 그 코드

를 확인할 수 있습니다.

- 예시

![button](https://trello-attachments.s3.amazonaws.com/5e39387f87dc0c300f09f54c/726x658/3fee98513749fc5bdc39e6a5b8f471eb/image.png)

```js
import React from "react";
import { storiesOf } from "@storybook/react";

import { grommet, Box, Button, Grommet } from "grommet";

const BasicButtons = props => (
  <Grommet theme={grommet}>
    <Box align="center" pad="medium">
      <Button label="Default" onClick={() => {}} {...props} />
    </Box>
    <Box align="center" pad="medium">
      <Button label="Anchor" href="#" />
    </Box>
    <Box align="center" pad="medium">
      <Button disabled label="Disabled" onClick={() => {}} {...props} />
    </Box>
    <Box align="center" pad="medium">
      <Button primary label="Primary" onClick={() => {}} {...props} />
    </Box>
  </Grommet>
);

storiesOf("Button", module).add("Basic", () => <BasicButtons />);
```

## 특징

- 테마를 사용하여 커스터마이징 가능

예시 1

```
  // color를 brand라는 이름으로 정의하고
  const theme = {
    global: {
      colors: {
        brand: "#aa33aa"
      },
      font: {
        family: "Roboto",
        size: "18px",
        height: "20px"
      }
    }
  };

  // 이렇게 적용가능
  const AppBar = props => (
    <Box
      tag="header"
      direction="row"
      align="center"
      justify="between"
      background="brand"
      pad={{ left: "medium", right: "small", vertical: "small" }}
      elevation="medium"
      style={{ zIndex: "1" }}
      {...props}
    />
  );


```

예시 2
![그림](https://trello-attachments.s3.amazonaws.com/5e1bc202db7fa64ef4e965c4/5e39387f87dc0c300f09f54c/f581a89c2dbaef63534d4449af51dffa/image.png)

문서에 이렇게 써있다면, 코드로는 이런 모양

```js
const theme = {
  global: {
    colors: {
      brand: "#aa33aa"
    },
    font: {
      family: "Roboto",
      size: "18px",
      height: "20px"
    }
  },
  accordion: {
    icons: {
      color: "hotpink"
    },
    border: undefined
  }
};
```
