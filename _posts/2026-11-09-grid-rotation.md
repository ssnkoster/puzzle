---
layout: post
title: "4화. 머릿속에서 돌려 보기 — 회전과 대칭의 퍼즐"
date: 2026-11-09
thumbnail: /assets/episodes/017-grid/thumb.png
---

격자무늬 네 개 중 하나만 나머지와 달라요. 어느 것이 다른 하나일까요?

---

## 지금 바로 풀어 보세요

힌트 버튼을 누르면 한 번에 하나씩 힌트가 열려요. 마지막 힌트 뒤에는 정답이 풀이 과정과 함께 천천히 나타나요.

<iframe class="puzzle-frame" src="/puzzle/demos/017-grid/" title="퍼즐 017" loading="lazy"></iframe>
<p class="puzzle-open"><a href="/puzzle/demos/017-grid/">새 창에서 크게 열기 ↗</a></p>

그림을 머릿속에서 돌려 보세요. **돌렸을 때 겹치면 같은 그림**이에요. 뒤집어야만 겹치는 그림은 어떨까요?

## 한 걸음 더: 돌리기와 뒤집기는 달라요

정사각형 그림은 90°씩 네 번 돌려서 같은 모양을 만들 수 있어요. 하지만 **뒤집기(거울상)**는 아무리 돌려도 만들 수 없어요. 왼손과 오른손을 떠올려 보세요. 닮았지만 아무리 돌려도 겹치지 않죠. 수학에서는 이런 돌리기·뒤집기의 모음을 **대칭**으로 다뤄요.

## 코딩으로 해석하기

```python
import numpy as np
A = np.array([[1,0,1,0,0],[0,0,0,0,1],[0,0,1,0,0],[0,1,0,0,0],[0,0,0,0,1]])
B = np.array([[0,0,1,0,1],[1,0,0,0,0],[0,0,1,0,0],[0,0,0,1,0],[1,0,0,0,0]])

def same_by_rotation(x, y):
    return any(np.array_equal(np.rot90(x, k), y) for k in range(4))

print(same_by_rotation(A, B), same_by_rotation(A, np.fliplr(B)))
```

회전만으로 같은지, 뒤집기까지 필요한지를 코드로 확인할 수 있어요.

---

*출처: 《멘사 창의력 퍼즐 Mensa Mind Maze Quest》 존 브렘너 지음 · 권태은 옮김 · 보누스 (퍼즐 017)*
