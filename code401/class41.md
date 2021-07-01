# Read : 41

## React 4

### Next.js Dynamic Routes

- Defining routes by using predefined paths is not always enough for complex applications. 

- In **Next.js** you can add brackets to a page (`[param]`) to create a dynamic route *(a.k.a. url slugs, pretty urls, and others)*.

- Page: `pages/post/[pid].js`:
```
import { useRouter } from 'next/router'
const Post = () => {
  const router = useRouter()
  const { pid } = router.query
  return <p>Post: {pid}</p>
}
export default Post
```
- Any route like `/post/1`, `/post/abc`, etc. will be matched by `pages/post/[pid].js`. 

- The matched path parameter will be sent as a query parameter to the page, and it will be merged with the other query parameters.

- Route: `/post/abc` will have the following query object:
```
{ "pid": "abc" }
```

- Route `/post/abc?foo=bar` will have the following query object:
```
{ "foo": "bar", "pid": "abc" }
```

- However, route parameters will override query parameters with the same name. 

- For example, the route `/post/abc?pid=123` will have the following query object:
```
{ "pid": "abc" }
```

- Multiple dynamic route segments work the same way. 

- The page `pages/post/[pid]/[comment].js` will match the route `/post/abc/a-comment` and its query object will be:
```
{ "pid": "abc", "comment": "a-comment" }
```

- Client-side navigations to dynamic routes are handled with `next/link`. 

- If we wanted to have links to the routes used above it will look like this:
```
import Link from 'next/link'
function Home() {
  return (
    <ul>
      <li>
        <Link href="/post/abc">
          <a>Go to pages/post/[pid].js</a>
        </Link>
      </li>
      <li>
        <Link href="/post/abc?foo=bar">
          <a>Also goes to pages/post/[pid].js</a>
        </Link>
      </li>
      <li>
        <Link href="/post/abc/a-comment">
          <a>Go to pages/post/[pid]/[comment].js</a>
        </Link>
      </li>
    </ul>
  )
}
export default Home
```

##### [Go Back](code_401_reading_notes.md)