# Neuro-Accessible Learning Platformer

> Hand-gesture game controller for students with disabilities

<p align="center">
  <img src="https://img.shields.io/static/v1?style=for-the-badge&label=type&message=accessibility%20%7C%20CV&color=ef4444" alt="Accessibility CV" />
  <img src="https://img.shields.io/static/v1?style=for-the-badge&label=stack&message=python%20%7C%20opencv%20%7C%20mediapipe&color=6366f1" alt="Python OpenCV MediaPipe" />
  <img src="https://img.shields.io/static/v1?style=for-the-badge&label=compliance&message=WCAG&color=10b981" alt="WCAG Compliant" />
</p>

---

<table>
  <tr>
    <td align="center"><b>0</b><br /><sub>physical input required</sub></td>
    <td align="center"><b>3+</b><br /><sub>schools tested</sub></td>
    <td align="center"><b>WCAG</b><br /><sub>compliant</sub></td>
    <td align="center"><b>Real-time</b><br /><sub>gesture mapping</sub></td>
  </tr>
</table>

---

## Problem

Traditional game controllers exclude students with motor disabilities from educational games their peers use daily. Adaptive controllers exist but are expensive ($100+), require custom hardware, and still demand physical manipulation that many students can't perform. The result: students with disabilities are locked out of game-based learning environments.

## Solution

Engineered a hand-gesture controller using computer vision that maps hand landmarks to game inputs in real time — **zero physical hardware required**. A standard webcam becomes the controller.

**What I built:**

- **Gesture recognition engine** using Python, OpenCV, and MediaPipe's hand landmark detection
- **Real-time input mapping** — hand positions and gestures translate directly to game controls (movement, jump, interact)
- **Tunable sensitivity profiles** — gesture thresholds adjust per student's motor ability, not one-size-fits-all
- **School evaluation sessions** — tested with 3+ schools for students with disabilities, iterated on feedback

## Technical Architecture

```
Webcam Feed → OpenCV Frame Capture → MediaPipe Hand Landmarks (21 points)
     ↓
Gesture Classification (custom thresholds per profile)
     ↓
Game Input Mapping → Educational Platformer Engine
```

## Key Design Decisions

| Decision | Rationale |
|---|---|
| **MediaPipe over custom CV** | 21-point hand landmark model is robust across lighting conditions and skin tones, runs on commodity hardware |
| **Per-student sensitivity** | Motor ability varies widely — a student with cerebral palsy needs different thresholds than one with muscular dystrophy |
| **No physical controller** | The entire point is eliminating hardware barriers, not replacing one physical device with another |
| **Educational game genre** | Platformers map naturally to directional + action inputs, the minimum viable gesture set |

## Accessibility

- WCAG compliant UI and visual feedback
- High-contrast mode for visual impairments
- Audio feedback for gesture recognition confirmation
- Teacher dashboard for adjusting student profiles

---

<sub>Built by <a href="https://github.com/tanhemdev">Tanya Hemdev</a> · UC Berkeley · Cognitive Science + Data Science</sub>
