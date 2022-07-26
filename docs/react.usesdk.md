<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@thirdweb-dev/react](./react.md) &gt; [useSDK](./react.usesdk.md)

## useSDK() function

<b>Signature:</b>

```typescript
export declare function useSDK(): ThirdwebSDK | undefined;
```
<b>Returns:</b>

ThirdwebSDK \| undefined

 Create an instance of the Thirdweb SDK that uses the connected wallet to sign transactions, and the desiredChainId of the ThirdwebProvider context to determine the network to use.

## Example


```javascript
const sdk = useSDK();
```
