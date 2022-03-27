
## Pattern - Unsubscribe on destroy

Pattern to automatically unsubscribe to an Observable when the componet is destroyed.

```typescript
export class MyComponent implements OnInit, OnDestroy {
  protected onDestroy$ = new Subject<void>();

  constructor(private service: MyService) {}

  ngOnInit() {
    this.service
      .requestData()
      .pipe(takeUntil(this.onDestroy$))
      .subscribe((param) => console.log);
  }

  ngOnDestroy() {
    this.onDestroy$.next();
    this.onDestroy$.complete();
  }
}
```

## Pattern - Trigger an observable by an action

```html
<ul *ngFor="let product of product$ | async">
  <li>{{ product.name }}</li>
</ul>

<div>Selected product: {{ (productSelected$ | async).name }}</div>

<ul *ngFor="let supplier of productSuppliers$ | async">
  <li>{{ supplier.name }}</li>
</ul>
```

```typescript

// Products

private productFilterSubject = new Subject<string>();
public productFilterAction$ = this.productFilterSubject.asObservable();

product$ = this.productFilterAction$.pipe(
  switchMap( (action: string) => this.requestProduct(action));
);

public onChange(action: string) {
  this.productFilterAction$.next(action)
}

// Selected Products

private productSelectedSubject = new Subject<string>();
public prodctSelectedAction$ = this.productSelectedSubject.asObservable();

prodctSelected$ = combineLatest([
  this.products$,
  this.productSelectedAction$
]).pipe(
  map(([products, selectedProductId]) =>
    products.find(product => product.id === selectedProductId)
  )
);

public onSelected(id: string) {
  this.prodctSelectedAction$.next(id);
}

// Selected Products Children

productSuppliers$ = this.productSelected$.pipe(
  switchMap( (product) =>
      forkJoin(product.supplierIds.map(supplierId => this.requestSupplier(supplierId)))
  )
);

```

See:

- [switchMap](./rxjs.md#switchmap)
- [forkJoin](./rxjs.md#forkjoin)

## Pattern - Combine multipe streams
