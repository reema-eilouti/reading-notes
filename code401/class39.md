# Read : 39

## React 3

### Next.js

- **Next.js** is an open-source React front-end development web framework created by Vercel.

- It enables functionalities such as server-side rendering and generating static websites for React based web applications. 

- It is a production-ready framework that allows developers to quickly create static and dynamic JAMstack websites and is used widely by many large companies.

- Next.js is one of several recommended "toolchains" available when starting a new React app, all of which provide a layer of abstraction to aid in common tasks. 

- Traditional React apps render all their content in the client-side browser, Next.js is used to extend this functionality to include applications rendered on the server side. 

- On July 27, 2020 Next.js version 9.5 was announced, adding new capabilities including incremental static regeneration, rewrites, and redirect support. 

#### Assets

- Next.js can serve static assets, like images, under the top-level `public` directory. 
- Files inside `public` can be referenced from the root of the application similar to `pages`.
- Unoptimized image in HTML: 
```
<img src="/images/profile.jpg" alt="Your Name" />
```
- Using the Image Component:
```
import Image from 'next/image'
const YourComponent = () => (
  <Image
    src="/images/profile.jpg" // Route of the image file
    height={144} // Desired size with correct aspect ratio
    width={144} // Desired size with correct aspect ratio
    alt="Your Name"
  />
)
```

#### Metadata

- What if we wanted to modify the metadata of the page, such as the `<title>` HTML tag?

```
<Head>
  <title>Create Next App</title>
  <link rel="icon" href="/favicon.ico" />
</Head>
```
```
import Head from 'next/head'
export default function FirstPost() {
  return (
    <>
      <Head>
        <title>First Post</title>
      </Head>
      <h1>First Post</h1>
      <h2>
        <Link href="/">
          <a>Back to home</a>
        </Link>
      </h2>
    </>
  )
}
```

#### CSS

- Next.js has built-in support for CSS and Sass which allows you to import **.css** and **.scss** files.

- Using popular CSS libraries like **Tailwind** CSS is also supported.

```
import styles from './layout.module.css'

export default function Layout({ children }) {
  return <div className={styles.container}>{children}</div>
}
```

##### [Go Back](code_401_reading_notes.md)