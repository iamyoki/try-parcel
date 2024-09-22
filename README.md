# Test out parcel v2.12.0 is slower than <= v2.11.0

## Choose one demo to run in dev

`cd parcel-2.12.0-ts`

`pnpm install`

`pnpm dev` or `npx parcel watch`

Go to `index.ts` file and press `cmd+s` to trigger build

## Build time comparison

My env:

| env    | version          |
| ------ | ---------------- |
| os     | macos 14         |
| pnpm   | 9.11             |
| node   | 20.17            |
| parcel | 2.12.0 vs 2.11.0 |

My results:

`parcel watch` (with cache, hmr on), `cmd+s` source file.

| project | parcel version | build time |
| ------- | -------------- | ---------- |
| ts      | 2.12.0         | 200-300ms  |
| ts      | 2.11.0         | 2-8ms      |
| js      | 2.12.0         | 10-20ms    |
| react   | 2.12.0         | 10-15ms    |
| react   | 2.11.0         | 2-8ms      |

## Conclusion

In any scenario, v2.11.0 is faster than v2.12.0 very much.

In ts project, v2.12.0 is about 200-300ms each build, unacceptably slow.
