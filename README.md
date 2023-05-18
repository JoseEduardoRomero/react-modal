# Eduardo_dev Product-Card

Este es un paquete de pruebas de despliegue de NPM

### José Eduardo Romero

## Ejemplo

```
    import { ProductCard, ProductImage, ProductTitle, ProductButtons} from 'do-product-card'
```

```
    <ProductCard
        key={product.id}
        product={product}
        initialValues={{
          count: 6,
        }}
      >
        {({ reset, count, isMaxCountReached, maxCount, increaseBy }) => (
          <>
            <ProductImage />
            <ProductTitle />
            <ProductButtons />

            <button onClick={reset}>Reset</button>
            <button onClick={() => increaseBy(-2)}> -2 </button>
            {!isMaxCountReached && (
              <button onClick={() => increaseBy(+2)}> +2 </button>
            )}

            <span>
              {count} - {maxCount}
            </span>
          </>
        )}
    </ProductCard>
```
