---
title: "[소프트웨어 공학] CH01. 소프트웨어 공학과 소프트웨어"
excerpt: "소프트웨어 공학의 배경 및 개념과 소프트웨어 기초에 대한 설명"

header:
  overlay_image: https://cdn.pixabay.com/photo/2015/12/04/14/05/code-1076536_1280.jpg

categories:
  - CS기초
  - 소프트웨어 공학

# toc: true
# toc_label: 소프트웨어 공학
# toc_sticky: true

comments: true

date: 2021-04-16
---

## 00. 들어가기 전
저처럼 비전공자이지만 학문적 기초를 닦고자 하시는 분들, 또는 전공자이나 기초적인 컴퓨터 과학 지식(일명 CS 기초)을 더 채우고자 하는 분들을 위해 부족하게나마 도움이 되고자 글을 씁니다.

앞으로 CS 기초와 관련된 글들을 게시할 예정이고, 이번 포스팅은 **소프트웨어 공학**에 대한 정리입니다. 글들은 책을 읽고 요약·정리한 내용으로 채울 예정이고, 추후 강의나 보충 자료를 통해 내용을 수정할 수 있습니다.

블로그에 들려주셔서 감사하고, 이 포스팅이 여러분들께 조금이나마 도움이 되길 바랍니다.
감사합니다.

## 01. 소프트웨어 공학이란?
개발 또는 정보 관련 자격증을 준비하면서 소프트웨어와 소프트웨어 공학이라는 말을 듣게 된다. 소프트웨어가 무엇인지는 막연히 알겠는데, 소프트웨어 공학은 무엇일까?   
소프트웨어 공학은 소프트웨어를 어떻게 만들 것인지, 만드는 동안 소요되는 시간과 또 만들어진 결과물의 모습은 어떻게 되는지에 대해 정리한 것이라고 한다.   
간단히 정리하자면 <u>소프트웨어를 어떻게하면 잘 만들 수 있는지 가르쳐주는 것</u>이 **소프트웨어 공학**이라고 한다.

## 02. 소프트웨어 공학 탄생과 정의
소프트웨어 공학이라는 개념은 <a href="https://ko.wikipedia.org/wiki/%EC%86%8C%ED%94%84%ED%8A%B8%EC%9B%A8%EC%96%B4_%EC%9C%84%EA%B8%B0" target="_blank" class="link-no-underline">소프트웨어 위기(Software Crisis)</a> 속에서 탄생했다. 1960년대 프로그램 개발에 대한 수요가 폭발적으로 증가하면서 많은 개발 프로젝트가 진행됐지만, 당시 이를 지원해줄 공급은 턱없이 부족했고 이에 결과물은 당연히 좋지 못했다.   
많은 소프트웨어 개발 프로젝트가 실패하면서 이를 극복하기 위해, 처음부터 모든 것을 만들어내는 것이 아닌 공학적 패러다임을 적용해 개발을 진행하자는 의견이 제기되었고, 1968년 10월 독일의 가미쉬(Garmisch) 도시에서 개최된 NATO의 한 커퍼런스에서 **"소프트웨어 공학(Software Engineering)"**이라는 용어가 처음 제안되었다.   
컨퍼런스가 진행될 때 의장이었던 <a href="https://en.wikipedia.org/wiki/Friedrich_L._Bauer" target="_blank" class="link-no-underline">프리드리히 바우어(Bauer)</a>는 소프트웨어 공학을 다음과 같이 정의했다.

> 기계에서 효율적으로 작동되는 신뢰성 있는 소프트웨어를 경계적으로 획득하기 위해 적절한 공학적 원리를 수립하여 활용하는 것이다<br>
> "Establishment and use of sound engineering principles to economically obtain software that is reliable and works on real machines efficiently."

소프트웨어 공학 IEEE(Institute of Electrical and Electronics Engineers)는 다르게 정의했다.

> 소프트웨어의 개발과 운용, 유지보수에 대한 체계적(systematic)이며, 훈련된(disciplined) 계량화할 수 있는(quantifiable) 접근방식의 적용이다<br>
> "the application of a systematic, disciplined, quantifiable approach to the development operation, and maintenance of software"

간단히 정리하면,
* 소프트웨어 공학은 소프트웨어 위기 때 많은 프로젝트 실패 속에서 해결 방안으로 탄생
* 소프트웨어 공학이란,
  * 효율적이고 신뢰성 있는 소프트웨어를
  * 경제적(비용과 시간을 고려)이게 개발하기 위하여
  * 체계적이며 계량화할 수 있는 공학적 원리를 이용해 개발하는 방법

정도로 이해하면 될 것 같다.

## 03. 소프트웨어 정의와 구성요소
위에서 소프트웨어 공학이 어떻게 탄생했고, 그것이 무엇인지 정의를 통해 알아봤다. 그렇다면 소프트웨어는 무엇일까? 무엇을 소프트웨어라 말할 수 있는걸까? 이는 단순히 프로그램을 일컫는 말일까?   
답은 아니다. 이를 이해하기 위해 두 개의 정의를 살펴볼 필요가 있다.

> 소프트웨어는 단순한 프로그램 뿐만 아니라 프로그램이 올바르게 작동하도록 하는데 필요한 관련된 문서 및 설치 데이터를 의미한다.
> by. 솜머빌(Sommerville)

솜머빌은 소프트웨어를 프로그램 뿐 아니라 관련된 문서와 데이터까지 포함하여 정의했다.

> 소프트웨어는 1) 실행되면서 원하는 기능이나 함수, 성능을 제공해 주는 명령어(컴퓨터 프로그램); 2) 프로그램이 데이터를 적절하게 처리할 수 있게 해 주는 자료구조; 3) 프로그램의 사용이나 운영을 나타내는 하드카피나 가상 형태인 문서이다. by. 프레스만(Presman)

프레스만은 소프트웨어를 프로그램, 문서, 그리고 자료구조까지 포함해 정의했다.


## 04. 소프트웨어 공학 특징 4가지
## 05. 라이프 사이클(Life Cycle)
## 06. 소프트웨어 도입 프로젝트 방식

## 정리

## 추가 보완 사항
* 소프트웨어 위기의 자세한 내용과 1960년대 컴퓨터 수요 증가 원인을 보충하고 싶음
* 공학적 패러다임 / 공학 개념 도입의 의미를 더 파악하길 바람

## 참고문헌
* <a href="http://www.kyobobook.co.kr/product/detailViewKor.laf?ejkGb=KOR&mallGb=KOR&barcode=9788984687448" target="_blank">김희영, "실무에 바로 활용하는 소프트웨어 공학", 21세기사, 2018</a>
* <a href="http://www.kocw.net/home/search/kemView.do?kemId=1045594" target="_blank">"소프트웨어 공학" KOCW 강의 영상, 조영석, 2014, http://www.kocw.net/home/search/kemView.do?kemId=1045594</a>