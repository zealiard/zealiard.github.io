---
layout: post
title:  Karabiner로 MacOS 한/영키 변경하기
author: David
categories: [MacOS, Karabiner]
image: media/15776797726131/keyboard.jpg
featured: true
hidden: true
---
MacBook을 새로 바꿨더니 `Caps Lock`키가 한/영 전환키로 바뀌었다. MacOS Sierra 버전에서 `Caps Lock`을 한/영전환키로 사용할 수 있는 옵션이 추가되었는데, 요즘 나오는 MacBook은 키보드도 `한/A`으로 인쇄되어 나온다.

처음 `Caps Lock`키를 사용했을 때는 조금 헷갈리기는 하지만 익숙해지면 괜찮을 것이라 생각했었는데, 코딩을 하다보니 `Tab`과 `Caps Lock`를 누를 때마다 멈칫멈칫하게 되었다. 그리고 오른쪽 새끼손가락은 점점 힘들어지는데 오른쪽 엄지손가락은 하는 일이 없다 -_-;

결국 예전처럼 오른쪽 `Command`키를 한/영 전환키로 사용하기로 했다.

---

## 1. Karabiner 설치하기

우선 MacOS용 Key Mapping 앱을 설치하자.

[https://pqrs.org/osx/karabiner](https://pqrs.org/osx/karabiner){: target="_blank" }

예전에는 KeyRemap4MacBook이라는 이름을 사용했었는데, 2014년즈음 Karabiner로 개명되었다.  
오픈소스이며, [github](https://github.com/pqrs-org/Karabiner-Elements){: target="_blank" }에서 소스를 확인 할 수 있다.

필자의 경우 2012년부터 쭉~ 사용해 왔는데, 한 번 MacOS 업그레이드에 빠르게 대응하지 못했던적이 있었지만, 그 이후에는 한 번도 문제가 되었던 적은 없었다.

![](/media/15776797726131/karabiner.jpg){: class="img-viewer" }

자신의 OS 버전에 맞게 선택해 다운로드하고 설치하면 된다.

![](/media/15776797726131/installation.jpg){: class="img-viewer" }

Karabiner는 Key Remap 기능뿐만 아니라, Profile 기능을 통해 설정한 매핑 정보를 쉽게 변경할 수 있으며, 내/외장 키보드를 구분해 적용할 수 있는 기능도 제공한다. 그 외에도 트랙패드를 확장하는 기능과 보안기능, CLI 등의 기능도 제공하는데 좀더 자세한 설명은 [매뉴얼](https://pqrs.org/osx/karabiner/document.html){: target="_blank" }을 참고하길 바란다.

---

## 2. 오른쪽 `Command`키를 한/영키로 설정하기

Karabiner를 설치하면, `Karabiner-Elements`와 `Karabiner-EventViewer`가 설치되는데, `Karabiner-Elements`는 Key Mapping을 설정하는 기능을 하며, `Karabiner-EventViewer`는 키보드 및 마우스의 입력 이벤트를 확인 할 수 있는 기능을 제공한다.

![](/media/15776797726131/karabiner-elements.png){: class="img-viewer" }

우선 `Karabiner-Elements`에서 `Add item`을 눌러 `right_command`를 `F18`로 할당해 준다.

![](/media/15776797726131/keyboard-settings.png){: class="img-viewer" }

키보드 설정에서 입력소스를 `F18`키로 설정해 준다. (더블클릭하고 오른쪽 `Command`를 누르면 된다)  
자~ 이제 오른쪽 `Command`키가 한/영키로 작동 할 것이다.  

![](/media/15776797726131/keyboard-settings2.png){: class="img-viewer" }

이제 `한/A`키로 전환하는걸 꺼주면, `Caps Lock`(길게 누르지 않아도 됨)으로 사용할 수 있다.

---

## 3. Parallels의 윈도우 한/영키를 오른쪽 `Command`로 변경하기

Mac을 사용하기는 하지만, 간혹 윈도우를 사용할 일이 꼭 생기기 때문에 Parallels를 이용해 윈도우를 사용하고 있는 사람들이 많을 것이다. 이제 MacOS와 같은 키를 사용해 윈도우에서도 한/영 전환을 해보자.

![](/media/15776797726131/parallels-settings.png){: class="img-viewer" }

Paralles의 `설정 > 단축키 > 가상 컴퓨터`를 선택한 다음 `+` 버튼을 누른다.

![](/media/15776797726131/parallels-settings2.png){: class="img-viewer" }

이제 `F18`키를 `AltGr`로 매핑시켜준다.  
`F18`은 `⌥` + 오른쪽 `Command`키를 누르면 Cmd가 선택되면서 `F18`이 입력되는데, 마우스로 Cmd선택을 해제해주면 된다.

이제 윈도우를 구동해서 오른쪽 `Command`키로 한/영 전환을 할 수 있다.

---

## `Function`키 문제

Karabiner를 사용할 때 `F키 + Key` 조합이 정상적으로 작동하지 않는 경우가 발생했다. 특히 Intellij Idea 같은 IDE를 사용할 때 단축키를 사용하는데 문제가 되었다.  
예를들어, `Shift + F6`을 누르면 `F6`만 인식되었다. Karabiner를 끄면 정상작동한다.  
뭔가 Karabiner에서 옵션을 변경하면 해결 될 것 같아 이것저것 살펴보다 해결을 하긴 했다.

![](/media/15776797726131/karabiner-settings.png){: class="img-viewer" }

Device 부분을 둘다 체크.

![](/media/15776797726131/karabiner-settings2.png){: class="img-viewer" }

Function keys를 위와 같이 설정.

이렇게 하니 정상적으로 동작했다. 키보드와 터치바를 다른 Device로 인식하는 걸까?  
무슨 이유인지는 모르겠지만, 일단 해결~