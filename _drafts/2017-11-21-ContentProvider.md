---
layout:post
title: 컨텐츠 프로바이더 
---


## 왜 컨턴츠 프로바이더인가.
일반적으로 어플리케이션에서 자료를 저장할 때 DB를 이합니다. 그런다ㅏ, 한 어플 내부에 저장된 데이터베이스에는 다른 어플리케이션이 접근하는 것이 불가능 합니다. 그렇다면 , 다른 어플리케이션의 데이터에 접근하는 것은 아예없는 것인가요 .? 그렇지 않다. 
만약 그렇게 된다면 엄청난 재앙(?)이 발생합니다. 

주소록 어플리케이션은 주소록 데이터를 DB에 저장하는데 이 주소록을 주소록 앱만 접근가능하면 말도 안되는 일이지요 .

컨텐츠 프로바이더는 어플 내부에 데이터베이스를 다른 어플과 공유 활 수있는 '통로를 제공 해줍니다.


## Content Provider와 Contents resolver
컨텐트 프로바이더를 이용하요 안드로이이드 시스템의 각종 설정 값이나 SD카드 내의 미디어 등에 접근하는 것이 가능합니다.컨텐트 프로바이더에 접근하기 위해선 해당 컨턴츠 프로바이더의 주소가 필요합니다.

컨텐트 프로바이더를 접근할 때는 컨텐트 프로바이더의 주소와 컨텐트 리졸버가 필요합니다. 컨텐트 리졸버는 컨텐트 프로바이더의 주소를 통해 해당 컨텐트 프로바이더에 접근하여 컨텐트 프로바이더의 데이터에 접근 할 수 있도록 해주는 역할을 합니다. 

컨텐트 리졸버는 액티비티 클래스 내의 getContentResolver 메소드를 통해 인스턴스를 받아올 수 있습니다.

## Content Provider 주소 구성 
컨텐트 프로바이더의 주소는 컨텐트 프로바이더를 생성할 때 지정한다. URI 형식으로 구성된다. URI는 URL보다 상위의 개념이다. 어떤 자원의 위치를 표기하기 위한 형식이다.

안드로이드에서 파일을 관리하게 되면 Schema를 두가지 형식을 볼 수 있는다. file과 content이다. 다른 앱과 공유를 하려면 무조건 content 스키마를 이용해야된다. 참고 

Nougat이상 부턴 FileProvider를 이용해 다른 앱과 파일을 공유할 수 있다. [FileProvider](http://stickyny.tistory.com/110)


reference
[커니의 안드로이드 이야기](http://androidhuman.com/279)