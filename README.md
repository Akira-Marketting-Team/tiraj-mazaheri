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


## Font
face: `PlayFair Display`
added the font in each page and component it is required 

`if you have a better way of adding the fonts dynamically rather than my method please do`

```bash
import { Playfair_Display } from "next/font/google";

const playfair = Playfair_Display({
    weight: ['400'],
    style: ['normal'],
    subsets: ['latin'],
    display: 'swap',
  });
```
How to use:
```bash
<h1 className={`tailwind-styles ${playfair.className}`}>
```


## Icons
- [Lucide Dev](https://lucide.dev/)
- [React Icons](https://react-icons.github.io/react-icons/)


## Color Scheme
Added the cream color scheme in the `tailwind.config.js` file:

```bash
colors: {
    cream: "#EFE9D8",
//  newColor: "palleteName",
},
```

How to use:
```bash
<div className="bg-cream">Text</div>
```
## Shadcn UI

I added a custom button component. you can modify it in `components/ui/button.tsx`:

```bash
cream: "border border-black rounded-full text-md p-0 bg-cream hover:bg-black hover:text-cream h-8",
creamLight: "border border-black rounded-full text-md p-0 hover:bg-white hover:text-black text-cream h-8",
creamDark: "border border-black rounded-full text-md p-0 hover:bg-cream hover:text-black text-cream h-8",
creamBig: "inline-flex items-center justify-center w-full h-12 gap-3 px-5 py-3 font-medium duration-200 bg-gray-100 md:w-auto rounded-xl hover:bg-gray-200",
```

With custom sizes in the `size` object:

```bash
light: 'h-10 rounded-full px-8 bg-black',
darkSm: 'h-8 rounded-full px-4 bg-black'
```
How to use:

```bash
<Button variant="creamDark" size="light">Text</Button>
```


You can start editing the page by modifying `app/page.js`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.
