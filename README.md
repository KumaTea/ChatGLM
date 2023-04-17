# ChatGLM
An Low-cost Deployment of THUDM/ChatGLM-6B with Practice of ljsabc/Fujisaki

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
