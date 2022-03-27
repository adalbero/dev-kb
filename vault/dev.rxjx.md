---
id: 6ndfa92md94p2aicbaxf0z1
title: RxJx
desc: ""
updated: 1648403788400
created: 1648403788400
---

## Higher-Order Mapping Operators

- Automatically subscribe to the inner Observable
- Flatten the resulting Observable returning Observable<T> not Observable<Observable<T>>
- Automatically unsubscribe from the inner Observable

### switchMap

- Stops the current operation and performs the new operation

### concatMap

- Performs each operation one at a time, in order

```typescript
const urls = [
  "https://api.mocki.io/v1/0350b5d5",
  "https://api.mocki.io/v1/ce5f60e2",
];

from(urls)
  .pipe(
    concatMap((url) => {
      return fromFetch(url);
    })
  )
  .subscribe((response) => console.log(response.status));
```

> [concatMap](https://indepth.dev/reference/rxjs/operators/concat-map) - In Depth Dev Reference

### mergeMap

- Performs each operation concurrently

---

## Combination Operators

### combineLatest

- Emits a combined value when any of the observables emit
- Won't emit until all Observables have emitted at least once

### merge

- Emits the one value when any of the Observables emit

### forkJoin

- When all Observables complete, emit the last value from each Observable into an array

---

### Subject

- Special type of Observable that allows values to be multicasted to many Observers
- Like EventEmitters.

### BehaivorSubject

- Variant of [Subject](#subject) that requires an initial value and emits its current value whenever it is subscribed to

---

## References

**RxJsPatterns in Angular**

[![Youtube Video](https://img.youtube.com/vi/uv_sblwIJag/0.jpg)](https://www.youtube.com/watch?v=uv_sblwIJag)

---

### Tags

`#javascript #rsjx`
