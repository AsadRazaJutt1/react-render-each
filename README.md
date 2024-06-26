﻿# react-render-each

## Installation

```bash
npm i react-render-each
```

### Without React Render Each

```javascript
const products = [
    {
        name: "product 1",
        price: 23
    },
    {
        price: 25
        name: "product 2",
    },
    {
        price: 28
        name: "product 3",
    }
];

const Product = ({data}) => {
    return (
        <>
            <div>{data.name}</div>
            <div>{data.price}</div>
        </>
    )
}

const List = () => {
    return (
        <section>
            {products.map((data, index) => {
                return <Product data={data} key={idx} />;
            })}
        </section>
    );
}
```

## Usage

### Using React Render Each

You don't need to add key in every .map funcation.
Most important with react-render-each your component much clean.
````javascript

import { Each } from "react-render-each";

const products = [
    {
        name: "product 1",
        price: 23
    },
    {
        price: 25
        name: "product 2",
    },
    {
        price: 28
        name: "product 3",
    }
];


const Product = (data, props) => {
    console.log(props);
    return (
        <>
            <div>{data.name}</div>
            <div>{data.price}</div>
        </>
    )
}

const List = (props) => {
  return (
    <section>
      <Each of={producrs} render={Product} {...{props}}/>
    </section>
  );
}

````

