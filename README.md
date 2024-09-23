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