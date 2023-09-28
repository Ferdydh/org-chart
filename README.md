
# Customizable organization chart, based on d3 v7

<span class="badge-npmversion">
     <a href="https://www.npmjs.com/package/@ferdydh/d3-org-chart" title="View this project on NPM">
          <img src="https://img.shields.io/npm/v/@ferdydh/d3-org-chart.svg" alt="NPM version" />
     </a>
</span>

This repo is a fork from [d3-org-chart](https://github.com/bumbeishvili/org-chart/) by David B([twitter](https://twitter.com/dbumbeishvili) and [LinkedIn](https://www.linkedin.com/in/bumbeishvili/)). Our ultimate goal is to integrate typescript and react natively into the library, fix reported issues, improve customization, and provide better documentation.



### Installing

```
npm i @ferdydh/d3-org-chart
```

```jsx
import { OrgChart } from '@ferdydh/d3-org-chart';

type Props = {
     data: DataType[]
}

type DataType = {
     id: string | number // required property
     parentId: string | number // required property
}

export const OrgChartComponent = ({ data }: Props) => {
  const container = useRef(null);

  useEffect(() => {
    if (fields && container.current) {
      const chart = new OrgChart<DataType>()
        .container(container.current)
        .data(fields)
        .render();
    }
  }, [fields, container.current]);

  return (
    <div>
      <div ref={container} />
    </div>
  );
};
```


#### Featured:

Custom components & algorithms used

- [Curved edges - vertical](https://observablehq.com/@bumbeishvili/curved-edges-compacty-vertical)
- [Curved edges - horizontal](https://observablehq.com/@bumbeishvili/curved-edges-compact-horizontal)
- [Flextree Algorithm](https://github.com/Klortho/d3-flextree)


## Author

Ferdy DH
