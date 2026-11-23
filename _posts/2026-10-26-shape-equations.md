---
layout: post
title: "2화. 도형이 숫자라고? — 연립방정식을 눈으로 푸는 법"
date: 2026-10-26
thumbnail: /assets/episodes/053-shapes/thumb.png
---

●, ▲, ★ 도형들이 줄마다 더해져 있고 합이 적혀 있어요. 마지막 줄의 합은 얼마일까요?

---

## 지금 바로 풀어 보세요

힌트 버튼을 누르면 한 번에 하나씩 힌트가 열려요. 마지막 힌트 뒤에는 정답이 풀이 과정과 함께 천천히 나타나요.

<iframe class="puzzle-frame" src="/puzzle/demos/053-shapes/" title="퍼즐 053" loading="lazy"></iframe>
<p class="puzzle-open"><a href="/puzzle/demos/053-shapes/">새 창에서 크게 열기 ↗</a></p>

각 줄을 식으로 보고, **두 줄을 빼면** 무엇이 사라지는지 살펴보세요. 도형 하나의 값이 보이기 시작해요.

## 한 걸음 더: 이게 바로 연립방정식이에요

도형을 문자로 바꾸면 ●=a, ▲=b, ★=c인 세 개의 식이 돼요. 이렇게 식이 여러 개 있을 때, 한 식에서 다른 식을 빼서 문자를 하나씩 없애 나가는 방법을 **소거법**이라고 해요. 퍼즐에서는 두 줄을 빼면 도형이 일부만 남아서 ● − ★ = 2 같은 간단한 관계가 나와요.

## 코딩으로 해석하기

```python
import numpy as np
# 각 줄의 (●, ▲, ★) 개수와 합
A = np.array([[2, 2, 1], [1, 2, 2], [1, 1, 3]])
s = np.array([33, 31, 34])
a, b, c = np.linalg.solve(A, s)
print(a, b, c, 2*a + b + c)
```

컴퓨터는 이 계산을 한 줄로 해요. 하지만 손으로 소거법을 해 보면 **왜 그 값이 나오는지** 이해할 수 있어요.

---

*출처: 《멘사 창의력 퍼즐 Mensa Mind Maze Quest》 존 브렘너 지음 · 권태은 옮김 · 보누스 (퍼즐 053)*
