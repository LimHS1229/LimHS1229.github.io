---
layout: post
categories: [mocapclean]
description: > 
  모션캡쳐 데이터는 키 애니메이션과 달리, 과장된 액션 없이 촬영 당시 액터의 상황을 최대한 보존/전달할 수 있도록 초점을 맞춰서 데이터를 클린업합니다. 
image: 
  path: /assets/img/images/hs005.png
  srcset: 
    1920w: /assets/img/images/hs005.png
    960w:  /assets/img/images/hs005.png
    480w:  /assets/img/images/hs005.png
accent_image: /assets/img/images/ViconMain.jpg
excerpt_separator: <!--more-->
sitemap: false
---

# CleanUp Pipeline
## Vicon에서의 클린업

Vicon Shogun Post에서 그래프를 깔끔하게 정리해줍니다.
이 과정에 있어서 가장 신경쓰는건,   
너무 키 애니메이션적인 과장을 주지 않고, 사람이 직접 연기했다는 느낌을 보존하는 것 입니다.

마커의 스왑으로 인해 손발이 뒤집히는 (Flip) 현상을 없애고,
걸음에서 발이 지면에 확실히 닿도록 해줍니다.

<!--more-->
---
## FBX 데이터의 리타겟

![MCP](/assets/img/images/MCPtool.png)

Vicon 에서의 클린업이 완료되면, FBX의 데이터를 maya로 가져옵니다.
(Xsens의 경우에는 MotionBuilder를 사용합니다.)

![MCP](/assets/img/images/MCP_LIGHT.gif)

위 툴은, 클린업 작업자들이 클린업에만 집중하고, maya 에서부터는 모션캡쳐 파이프라인을 자연스럽게 따라갈 수 있도록 순차적으로 버튼을 누르면

0. FrameRate 설정
1. 현재 클린업 버전을 저장
2. Vicon 데이터를 내부 규약에 맞는 Joint와 리타겟
3. 이후 FBX와 Anim을 각각 폴더에 저장
4. 프리뷰용 어셋을 불러옴
5. 프리뷰 어셋에 Anim데이터를 임포트, 프리뷰를 저장

의 다섯개의 과정을 매우 간단하게 끝마칠 수 있습니다.
이후 클린업데이터를 애니메이션 작업자에게 전달하고, 모션캡쳐 라이브러리에 저장합니다.

---



* toc
{:toc .large-only}

클린업 과정 이후의 파이프라인도 직접 만들어, 초심자도 간단히 적응가능하도록 자동화시켰습니다.
{:.note.smaller}
