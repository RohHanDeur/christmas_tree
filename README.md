# 🎄 Animated Christmas Tree (Python / curses)

터미널에서 실행되는 **애니메이션 크리스마스 트리**입니다.  
`curses` 기반으로 **나선형 조명(스트링)**, **보케 배경**, **눈 내림 + 바닥 누적**, **반짝이는 큰 별**을 렌더링합니다.

---

## ✨ Features

- Spiral string lights (Yellow / White / Red) with flicker
- Bokeh background layer (soft glow dots)
- Falling snow (back/front layers) + ground accumulation
- Branch snow settling + decay
- Big twinkling star at the top
- Quit with `q`

---

## 📦 Requirements

- Python **3.9+** 권장 (`list[int]` 타입 힌트 사용)
- 터미널이 **유니코드(UTF-8)** 및 색상 출력 지원
- macOS / Linux 권장  
  - Windows는 기본 콘솔에서 `curses`가 제한될 수 있어 **WSL 권장**

---

## ▶️ Run

프로젝트 루트에서 아래 파일을 실행하세요.

### 1) 실행

```bash
python3 Python/animated_tree.py
```
2) 종료  
q 키를 누르면 종료됩니다.

## 🖥️ Terminal Tips (깨짐/흐림/색 이상 대응)
글자 깨짐이 있으면
터미널 인코딩이 UTF-8인지 확인하세요.

폰트는 Nerd Font / Apple SD Gothic Neo / D2Coding 등 유니코드 지원 폰트 권장

창이 작으면 트리가 잘립니다
안내 메시지(최소 사이즈)가 뜨면 터미널 창을 더 키우세요.

색이 “갈색처럼” 보이면
터미널 테마/색상 설정에 따라 DIM이 어둡게 보일 수 있습니다.

현재 코드는 “갈색 느낌”을 줄이기 위해 와이어/전구의 DIM을 최소화하는 방향으로 구성되어 있습니다.

## 📁 File
Python/animated_tree.py

curses 기반 애니메이션 렌더러 (단일 파일)

📝 How It Works (간단 구조)
렌더링 레이어 순서(뒤 → 앞):

Bokeh

Back snow

Star

Wire (spiral guide)

Tree leaves (edge 강조)

Bulbs (flicker + glow)

Fairy dots (subtle)

Branch snow

Trunk

Ground + accumulation

Front snow
