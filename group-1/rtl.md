---
description: TESTING TOOL
---

# RTL

Reacting Testing Library





BDT- Behaviour Driven Test





<pre><code><strong>//CRA create react app
</strong><strong>npm i -D jest 
</strong><strong>
</strong>//vite 
npm i -D jest ts-jest @testing-library/react @testing-library/jest-dom @testing-library/user-event @babel/preset-react @babel/preset-typescript @babel/preset-env identity-obj-proxy
</code></pre>

jest:  테스트 프레임 워크&#x20;

ts-jest:  Jest에서 타입스크립트를 사용

@testing-library/react:  React DOM 유틸리티 도구&#x20;

@testing-library/jest-dom: DOM 상태 검사할때 반복되는 작업을 피하기위해서 사용된다.&#x20;

@testing-library/user-event: 사용자와 같이 이벤트 발생

identity-obj-proxy:&#x20;

## Package.json

```
"scripts": {
  "prebuild": "npm run test",
  "test": "jest"
},
```

## jest.config.json

```
{
    "roots": ["<rootDir>/test/"],
    "testEnvironment": "jsdom",
    "moduleNameMapper": {
        "\\.(css|less|svg)$": "identity-obj-proxy"
    },
    "setupFilesAfterEnv": ["<rootDir>/test/setup.ts"],
    "transform": {
        "^.+\\.tsx?$": "ts-jest"
    }
}
```







