# ChatGLM

A Low-cost Deployment of
[THUDM/ChatGLM-6B](https://github.com/THUDM/ChatGLM-6B)
with Practice of
[ljsabc/Fujisaki](https://github.com/ljsabc/Fujisaki)

<a target="_blank" href="https://colab.research.google.com/github/KumaTea/ChatGLM/blob/main/ChatGLM.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

## Benchmark

```python
def get_bench(l):
    times = [i[1]/len(i[0].encode('utf-8')) for i in l]
    times = sorted(times)
    times = times[1:-1]
    print(avg(times))
```

> Time cost for generating 100 characters

| Hardware | FP16 | INT8 | INT4 |
| --- | --- | --- | --- |
| A100 | 2.029 | 2.490 | 2.119 |
| T4 | 2.793 | 6.348 | 5.550 |
| CPU | 44.202 | 87.822 | 169.017 |
