---
layout: post
categories: [mocapclean]
permalink: /action/mocapclean/2026-03-04-beforeCapture/
description: > 
  당일 촬영이 문제없이 이루어 질 수 있도록, 이렇게 준비해왔습니다.
image: 
  path: /assets/img/images/fingerRND.jpg
  srcset: 
    1920w: /assets/img/images/fingerRND.jpg
    960w:  /assets/img/images/fingerRND.jpg
    480w:  /assets/img/images/fingerRND.jpg
accent_image: /assets/img/images/ViconMain.jpg
excerpt_separator: <!--more-->
sitemap: false
---

# Before Mocap 
  >손가락 모션캡쳐를 더욱 깔끔히 촬영하기 위해, 마커가 잘 찍히면서도 액터가 주먹쥐는 액션에 위화감을 느끼지 않도록, 직접 여러방법을 통해 테스트해보는 과정입니다.
{:.note.smaller}
## 촬영전에는 이런 준비를 해왔습니다.

![어드밴스드5](../../assets/img/images/lhsRND_advanced5.png)

툴에 들어갈 어셋을 리타겟하기 용이하도록, 스크립트를 제작하여 단숨에 T-pose로 만들어줍니다.
필요에 의해 RIG를 지우고, model과 joint만 남겨둬도 메시가 찢어지지 않도록 주의합니다.

![바이콘](../../assets/img/images/retarget.png)

또한 해당 데이터를 툴에서 미리 리타겟해두고, 촬영 당일에는 만들어둔 리타겟메시의 크기를 조정해   액터의 신장과 비슷하게 맞춰주는 작업만 하여 촬영 딜레이를 최소화합니다.

<!--more-->
---
## 프리뷰는 직관적으로

![UEinvicon](../../assets/img/images/UE_inVicon.jpg)
![mocapProp](../../assets/img/images/mocapProp.png)

언리얼 환경에 프리뷰용 어셋들을 세팅합니다. 이후 레퍼런스 캠이나, 촬영시 오브젝트 or 환경 역할을 해줄 더미, 프랍 등, 촬영에 추가적인 도움이 될 요소들을 사전준비합니다.

---
## 리스트업

![mocaplist](../../assets/img/images/mocapscript.png)

당일 촬영이 예정되어있는 샷을 액셀 등으로 가시화해, 촬영자와 액터가 어떤 액션을 취해야 하는지 명확하게 리스트로 전달합니다.



* toc
{:toc .large-only}

프로그램 내적인 부분은 물론, 의상 및 프랍 등 센스있는 준비가 촬영을 더욱 원활하게 만들고, 좋은 데이터를 받습니다.
{:.note.smaller}
