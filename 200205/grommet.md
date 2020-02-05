# grommet [(공식 링크)](https://v2.grommet.io/)

## 튜토리얼

1. 설치
   ```
   npm install grommet grommet-icons styled-components --save
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
