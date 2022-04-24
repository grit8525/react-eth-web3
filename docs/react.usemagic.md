<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@thirdweb-dev/react](./react.md) &gt; [useMagic](./react.usemagic.md)

## useMagic() function

Convienience hook for connecting to magic link (email wallet).

<b>Signature:</b>

```typescript
export declare function useMagic(): (configuration: LoginWithMagicLinkConfiguration) => Promise<{
    data?: import("wagmi-core").ConnectorData<any> | undefined;
    error?: Error | undefined;
}>;
```
<b>Returns:</b>

(configuration: LoginWithMagicLinkConfiguration) =&gt; Promise&lt;{ data?: import("wagmi-core").ConnectorData&lt;any&gt; \| undefined; error?: Error \| undefined; }&gt;

a function that will prompt the user to connect their magic link, given an email.

## Example

In order to use the hook to connect users with magic link, you just need to provide the users email to the connect function.

You can setup the hook with the following configuration:

```javascript
import { useMagic } from "@thirdweb-dev/react"
import { useState } from "react"

const LoginWithMagicLink = () => {
  const connectWithMagic = useMagic()
  const [email, setEmail] = useState()

  return (
    <div>
      <input value={email} onChange={(e) => setEmail(e.target.value)} />
      <button onClick={() => connectWithMagic({ email })}>Login</button>
    </div>
  )
}
```
