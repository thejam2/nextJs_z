This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.


## (폴더명)
라우트에 영향x, layout 가능

## layout vs template
페이지 이동할때 리렌더링 안되게 하고싶을땐 layout, 리렌더링 되게 하고싶을땐 template

서로 공존 x, 선택해야함, 대부분 layout

## css 모듈 선택 이유
- tailwind →호불호 심하고, 가독성 x
- Styled Component → Server Component SSR 문제
- sass
- css module →sass보다 간단
- vanilla extract → Windows와 문제
- 100dvw, 100dvh → 레이아웃 틀어짐 방지

## 패러렐 라우트
- 모달 창 → 패러렐 라우트와 인터셉트 라우트
- 뒤에보일 page와 @modal 폴더를 같은 경로에 생성
- @modal폴더 안에 모달 page 생성
- defaults.tsx -> 패러렐 라우트에 대한 기본 값 (그냥 return null;해주면 됨)

## 인터셉팅 라우트
- 주소가 다른데 같이 뜨게 만들어주는 것
- (..)i → ..은 부모 컴포넌트
- (..)이나 (.)은 브라우저 주소 기준
- 만약 (beforeLogin)안의 @modal 안에 (..)i 폴더를 생성 시 (beforeLogin)보다 더 상위의 app으로 이동 (@가 붙은 폴더의 경우는 주소에 해당되지 않아서 무시)
- i/login/page.tsx를 대체하고 싶다면 @modal/(.)i로 i의 파일 이름을 변경해야함
- 패러렐 라우트가 있고 인터셉팅 라우트가 있다면 메인의 i/flow/page가 처리하는 게 아니라 인터셉팅 라우트의 page가 처리하게 됨 (클라이언트에서 라우팅 할 때만 인터셉트 라우팅이 적용)
- 직접 접근, 새로고침, 주소로 접근 시 메인 i로 실행되어서 i/login/page.tsx도 필요