---
layout: post
title: "3화. 육각형 속 숫자의 비밀 — 규칙을 찾는 두 가지 방법"
date: 2026-11-02
thumbnail: /assets/episodes/018-hexagon/thumb.png
---

완성된 육각형의 숫자들은 어떤 규칙으로 이어져 있어요. 같은 규칙으로 두 번째 육각형의 물음표를 채워 보세요.

---

## 지금 바로 풀어 보세요

힌트 버튼을 누르면 한 번에 하나씩 힌트가 열려요. 마지막 힌트 뒤에는 정답이 풀이 과정과 함께 천천히 나타나요.

<iframe class="puzzle-frame" src="/puzzle/demos/018-hexagon/" title="퍼즐 018" loading="lazy"></iframe>
<p class="puzzle-open"><a href="/puzzle/demos/018-hexagon/">새 창에서 크게 열기 ↗</a></p>

이웃한 숫자끼리 어떤 계산을 하면 다음 숫자가 나올까요? 계산이 **번갈아** 바뀌는지도 살펴보세요.

## 한 걸음 더: 두 연산을 합치면?

규칙은 "(+6)을 하고 ×2", 그다음엔 "(−6)을 하고 ÷2"가 번갈아 나와요. 두 번째 계산은 첫 번째 계산을 **되돌리는 연산**이라 2단계를 거치면 처음 값이 +3 만큼만 달라져요. 이렇게 **여러 연산을 이어 붙인 것을 함수의 합성**이라고 해요.

## 코딩으로 해석하기

```python
def f(x): return (x + 6) * 2
def g(x): return (x - 6) / 2

x = 20
for i in range(5):
    x = f(x) if i % 2 == 0 else g(x)
    print(x)
```

`f`와 `g`를 바꿔 가며 실행해 보세요. 다른 규칙으로도 같은 퍼즐을 만들 수 있어요.

---

*출처: 《멘사 창의력 퍼즐 Mensa Mind Maze Quest》 존 브렘너 지음 · 권태은 옮김 · 보누스 (퍼즐 018)*
