# @code-workers.io/ts-memoize

Library providing memoization functionality via:
* a `memoize`-function
* a `Memoize`-decorator


## Installation

```bash
npm i @code-workers.io/ts-memoize
```

## Usage

### Decorator Usage
Annotate the function you want to memoize using the `Memoize`-decorator:

```typescript
class Test {
  @Memoize()
  calculate(a: number, b: number): number {
    return a + b;
  }
}
```

### Function usage
Use the `memoize`-function:

```typescript
class Test {
  calc(a: number, b: number): number {
    return memoize((a, b) => a + b).memoized(a, b);
  }
}
```
