
# Frontend interview topics

<details>
  <summary>Closure Examples</summary>

```javascript
const outer = (argOuter) => {
  const res = (argInner) => {
    argOuter = argOuter + argInner;
  };
  const log = () => argOuter;
  return {
    res,
    log,
  };
};
const { res, log } = outer(1);
res(2); // argOuter is now 3
res(3); // argOuter is now 6
res(4); // argOuter is now 10
console.log(log()); // logs 10 because everytime you call res, it updates argOuter variable value also

```
 </details>
