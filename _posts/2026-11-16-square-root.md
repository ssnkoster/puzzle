---
layout: post
title: "5화. 어떤 수를 여덟 번 곱하면? — 끝자리와 제곱의 비밀"
date: 2026-11-16
thumbnail: /assets/episodes/034-square/thumb.png
---

여덟 개의 숫자를 순서만 바꾸면 어떤 수를 여덟 번 곱한 값이 돼요. 어떤 수일까요?

---

## 지금 바로 풀어 보세요

힌트 버튼을 누르면 한 번에 하나씩 힌트가 열려요. 마지막 힌트 뒤에는 정답이 풀이 과정과 함께 천천히 나타나요.

<iframe class="puzzle-frame" src="/puzzle/demos/034-square/" title="퍼즐 034" loading="lazy"></iframe>
<p class="puzzle-open"><a href="/puzzle/demos/034-square/">새 창에서 크게 열기 ↗</a></p>

제곱수의 **끝자리**에는 올 수 없는 숫자가 있어요. 그걸 알면 후보가 확 줄어들어요.

## 한 걸음 더: 제곱수의 끝자리

어떤 수를 제곱한 값의 끝자리는 0, 1, 4, 5, 6, 9 중 하나뿐이에요. 2, 3, 7, 8로 끝나는 제곱수는 없어요. 끝자리가 정해지면 **큰 수를 다 계산하지 않고도 후보를 걸러낼** 수 있어요.

## 코딩으로 해석하기

```python
print(sorted({(n * n) % 10 for n in range(100)}))
print(8 ** 8)
```

위 코드로 끝자리를 확인해 보세요. 어떤 수를 여덟 번 곱하는 것은 제곱근을 세 번 구하는 것과 같아요.

---

*출처: 《멘사 창의력 퍼즐 Mensa Mind Maze Quest》 존 브렘너 지음 · 권태은 옮김 · 보누스 (퍼즐 034)*
