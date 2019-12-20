---
layout: post
title:  RSocket과 gRPC
author: David
categories: [Reactive, RSocket, gRPC]
image: media/title/rsocket-vs-grpc.jpg
---
RSocket이 소개될 때마다 자주 등장하는 질문 중 하나는 "gRPC와 RSocket은 어떻게 다른가?" 이다.  
오늘은 RSocket과 gRPC에 대해 간단히.. 아주 간단하게 알아보도록 하겠다.

gRPC는 구글에서 개발한 HTTP/2 기반의 ***RPC 프레임워크*** 이다.  
폴리글랏 RPC의 문제를 해결하기 위한 목적으로 디자인 되었으며, protobuf IDL과 HTTP/2 프로토콜로 구성되어 있다. 구글에서 마이크로서비스 간 통신을 위해 사용되고 검증되었으며, 2015년 오픈소스로 공개되었다.

RSocket은 애플리케이션 간 통신을 위해 디자인 되었으며, 역압(Back-Pressure)과 Reactive Stream 개념을 end-to-end에 적용하는 네트워크 ***프로토콜*** 이다.

OSI 7계층의 개념으로 봤을 때 gRPC는 7계층에 속하며, RSocket은 5/6계층에 속한다.  
일반적으로 High-Level 기술은 Low-Level 기술보다 사용하기 쉽지만, 성능은 떨어지는 경향이 있다. OSI 계층도 마찬가지로 Low-Level을 다루는 것이 성능상의 이점이 있지만, 모두에게 익숙한 HTTP를 사용할 수 없다는 단점이 생긴다.

#### **그렇다면, 익숙하지 않은 RSocket을 사용해야 할 만한 이유가 있을까?**

1. Spring에서 잘 지원해 준다.(난 Java를 주로 다룬다 -_-)
2. 성능이 좋다. (벤치마크는?)
3. 생각보다 어렵지 않다. (정말?)
4. 남들이 잘 모른다. (우쭐~)

프로그래밍 패러다임이 빠르게 변화되고 있고, 향후 Java 진형에서는 Reactive를 다룰수 있는 개발자와 없는 개발자로 나눠지질 수도 있다. 이 Reactive를 다루는 기술에는 Reactor와 Rsocket이 주요 기술로 부각될 것으로 예상하고 있다. 그리고 이미 많은 개발자들이 RxJava를 이용해 Reactive한 개발을 하고 있다. 미래를 대비하는 마음으로 미리 공부해 보는 것도 개발자로서 좋은 자세 아니겠는가?

물론 성능적으로도 우위에 있는 것은 사실이다. 아래 링크를 따라가면 벤치마크 결과를 볼 수 있는데, 참고용으로 보면 좋을 것 같다.

[https://dzone.com/articles/rsocket-vs-grpc-benchmark](https://dzone.com/articles/rsocket-vs-grpc-benchmark){: target="_blank" }

최근 R2DBC를 지원하는 spring-data-r2dbc GA버전이 릴리즈 되었다. 이제는 RDB를 다루는 기술도 Reactive하게 변화하고 있으니, JVM기반 언어로 생계를 유지하는 분들은 관심을 가져보는 것도 좋을 듯 싶다.

참고로 RSocket과 gRPC의 차이점에 대해 더 알고싶다면 [Differences between gRPC and RSocket](https://medium.com/netifi/differences-between-grpc-and-rsocket-e736c954e60){: target="_blank" }를 참고해 보면 좋을 것 같다.