<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@thirdweb-dev/react](./react.md) &gt; [useTransferNFT](./react.usetransfernft.md)

## useTransferNFT() function

> This API is provided as a preview for developers and may change based on feedback that we receive. Do not use this API in a production environment.
> 

Use this to transfer tokens on your [NFTContract](./react.nftcontract.md)

<b>Signature:</b>

```typescript
export declare function useTransferNFT<TContract extends NFTContract>(contract: RequiredParam<TContract>): import("@tanstack/react-query").UseMutationResult<Omit<{
    receipt: import("@ethersproject/abstract-provider").TransactionReceipt;
    data: () => Promise<unknown>;
}, "data">, unknown, TransferNFTParams<TContract>, unknown>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  contract | [RequiredParam](./react.requiredparam.md)<!-- -->&lt;TContract&gt; | an instance of a [NFTContract](./react.nftcontract.md) |

<b>Returns:</b>

import("@tanstack/react-query").UseMutationResult&lt;Omit&lt;{ receipt: import("@ethersproject/abstract-provider").TransactionReceipt; data: () =&gt; Promise&lt;unknown&gt;; }, "data"&gt;, unknown, [TransferNFTParams](./react.transfernftparams.md)<!-- -->&lt;TContract&gt;, unknown&gt;

a mutation object that can be used to transfer NFTs

## Example 1


```jsx
const Component = () => {
  const nftDrop = useNFTDrop(<ContractAddress>);
  const {
    mutate: transferNFT,
    isLoading,
    error,
  } = useTransferNFT(nftDrop);

  if (error) {
    console.error("failed to transfer nft", error);
  }

  return (
    <button
      disabled={isLoading}
      onClick={() => transferNFT({ to: "0x...", tokenId: 2 })}
    >
      Transfer NFT!
    </button>
  );
};
```

## Example 2


```jsx
const Component = () => {
  const { contract } = useContract(<ContractAddress>);
  const {
    mutate: transferNFT,
    isLoading,
    error,
  } = useTransferNFT(contract?.nft);

  if (error) {
    console.error("failed to transfer nft", error);
  }

  return (
    <button
      disabled={isLoading}
      onClick={() => transferNFT({ to: "0x...", tokenId: 2 })}
    >
      Transfer
    </button>
  );
};
```
