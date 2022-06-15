# gsap-fade-enter-leave

## Get Started

1. install

```
npm install react react-router-dom @zlxiao97/gsap-fade-enter-leave
```

2. Fade-enter

```
import { useAnimation } from "@zlxiao97/gsap-fade-enter-leave";

export default () => {
  const [ids] = useAnimation([
  { targets: ["l1", "l2"], vars: { x: "-500px" } },
  {
    targets: ["r1", "r2"],
    vars: { x: `${screenWidth + 500}px` }
  },
  {
    targets: ["m1"],
    vars: { y: `-600px` }
  }
  ]);
  const {l1, m1, r1, l2, r2 } = ids
  return (
    <div>
      <div key="l1" id={l1}>l1</div>
      <div key="m1" id={m1}>m1</div>
      <div key="r1" id={r1}>r1</div>
      <div key="l2" id={l2}>l2</div>
      <div key="r2" id={r2}>r2</div>
    </div>
  );
};
```

3. Fade-leave

```
replace:
import { useNavigate } from "react-router-dom";
to:
import { useNavigate } from "@zlxiao97/gsap-fade-enter-leave";
```