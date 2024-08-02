---
title: "github blog에 대해 알아보자"
layout: single
categories: [Github Blog]
use_math: true
---
<style>
.crossline {
    border-bottom: 1.5px solid #6f777d;
}

.highlight1 {
    background-color: #ededed;
    color: #797c7e;
}

.center {
        text-align: center;
      }

.center img{
	width: 300px;
}

.left {
    text-align: left;
}

.left img{
    max-width: 70%
}

a {
  text-decoration-line: none;
/*   text-decoration-line: underline; */
/*   text-decoration-line: overline; */
/*   text-decoration-line: line-through; */
/*   text-decoration-line: underline line-through overline; */
}

.git {
    padding-top: 50px;
    padding-bottom: 10px;
}

</style>

## 1. 시작하기 전에

<!--
<div class="crossline"></div>
-->

<p>
필자는 웹페이지 개발을 하지 않을 뻔더라도 <span class="highlight1">git</span>을 사용하지도 않았던 터라, 처음 github page 구축까지 일주일이 넘게 걸렸다. 이때 github page를 이용해 블로그를 운영하는 방법에 대해 정리한 사이트는 많이 있지만, 대부분 <span class="highlight1">Jekyll</span>이나 <span class="highlight1">git</span>에 익숙하다는 전제하에 설명하는 경우가 많았고, 각자의 개발 환경을 위주로 설명하고 있는 경우가 많아서 그대로 따라하기에도 어려웠던 기억이 있다.
</p>

<span style="font-weight: bold;">Warning</span>: 본인은 이 분야의 전문가가 아니므로 잘못 기재된 내용이 있을 수 있습니다.
{: .notice--warning}
<!--
<div class="center">
<img src="https://1drv.ms/i/c/ce3c26eef978e16d/IQMrEZmOSeo7S51JFkWQgtpdAVZ13CU1lfFD4m8mBYNQDJg?width=1024" alt="Example Image" />
</div>
-->
<img src="https://1drv.ms/i/c/ce3c26eef978e16d/IQMabGtGDBq5TJhBLrB7mzNJAcedJD9faDIGJsKPrLu6doU?width=1024" alt="Example Image" />

### 1.1 github page는 어떻게 관리되는가?

<p>
<span class="highlight1">github.io</span>도메인을 갖는 블로그는 <a href="https://github.com/" target="_blank">githubs</a> 사이트 내의 저장 공간을 이용해서 관리한다. 만약 <a href="https://github.com/" target="_blank">githubs</a> 사이트에 대해 모른다면, 일단은 각종 프로그램 소스를 관리하거나 공유하는 사이트 정도로 이해하고 넘어가도록 하자. github 블로그를 운영하기 위해서는 당연히 자신의 github 계정<b>(구체적으로는 github.io 도메인으로 연동시킬 온라인 저장 공간)</b>과 블로그를 수정하고 관리하는데 사용할 프로그램이 필요하다. 따라서, 본격적으로 블로그를 운영하기에 앞서 <a href="https://github.com/" target="_blank">githubs</a> 사이트에서 본인 계정을 만들고, 아래의 링크를 통해 블로그 운영에 필요한 프로그램을 설치하자.
</p>

<div>
<a href="https://code.visualstudio.com/" target="_blank">visual studio code</a> 
</div>

<div class="left">
<img src="https://1drv.ms/i/c/ce3c26eef978e16d/IQOMERT_RF4WQbhrCQttapOCAWsdtX_QO6IOaNUAW4W3uDQ?width=1024" alt="Example Image" />
</div>



<div class="git">
<a href="https://git-scm.com/" target="_blank">Git</a> 
</div>

<div class="left">
<img src="https://1drv.ms/i/c/ce3c26eef978e16d/IQPfS7o5HPQXSIBDf0UwpT51AbgffSIbCWBUdvf5kEJuqVU?width=1024" alt="Example Image" />
</div>

<br />
<br />
<b>Visual Studio Code (VS Code)</b>는 블로그에 올릴 포스트나 설정 파일들을 관리하는데 사용할 프로그램이고, Git을 설치하면서 함께 설치되는 <b>Git Bash</b>는 자신의 컴퓨터에서 작성한 포스트나 수정한 정보를 온라인 공간에 업데이트 하기 위해 사용한다.
<br />
> 블로그를 관리하고 업데이트하는 과정은 아래 그림과 같이 <b style="color: #045FB4;">VS Code</b> 상에서 관련 파일을 작성한 뒤, 
> <b>Git Bash</b>에 아래 코드를 입력하여 해당 정보를 반영하는 두 단계로 진행된다.

```shell
# Update page (repository) info
git add *
git commit -m "blog-testing"
git push
```

<div class="crossline"></div>

### 1.2 Git 개념 이해하기 (권장)

<p>
본인이 컴퓨터 공학과 관련된 일을 하거나 공부를하고 있다면 <b>git을 공부하고 반드시 사용하도록 하자.</b> 필자의 경우 전자공학을 전공했고, 임베디드 시스템 프로그래밍을 주로 했었기 때문에 <span class="highlight1">git</span>의 필요성을 느끼지 못했었는데, 이번에 블로그 구축을 시작하면서 <span class="highlight1">git</span>이 얼마나 유용한 시스템인지 새삼 깨닫게 되었다. <br /><br />본인이 <span class="highlight1">git</span>에 대해 아예 모른다면 다음의 YouTube 영상 시청을 권장한다.<br />
</p>

<div>
<a href="https://www.youtube.com/watch?v=YQat_D1C-ps" target="_blank">Git & GitHub Page 블로그 만들기</a> 
</div>

<p>
전체 영상이 네 개밖에 되지 않고, 개인적으로는 상당히 유익한 강의라고 생각한다. 보면서 한 번에 이해해도 좋겠지만, <span class="highlight1">git</span>이란게 이런거구나 하는 정도로만 이해할 수 있어도 충분할 것 같다.
</p>
<span style="font-weight: bold;">Notice</span>: 본인이 프로그래머가 아니거나, 블로그 운영에만 관심이 있다면 굳이 시청하지 않으셔도 됩니다.
{: .notice}

<div class="crossline"></div>

### 1.3 튜토리얼 따라하기

<p>
github page를 블로그 플랫폼으로 선택하는 이유 중 하나는 자유롭게 테마를 선택하고, 본인 취향에 맞게 커스터마이징이 가능하다는 이점 때문이다.
<br /><br />
</p>

> 그러나, 본인이 처음 github page를 접해본다면, 그런 기대는 잠시 접어두고 잘 정리된 예제를 따라하는 것으로 시작하기를 권장한다.
<br />

<div style="font-size: 1.3em;">
<b>추천 사이트:</b> <a href="https://devinlife.com/howto/" target="_blank">취미로 코딩하는 개발자</a>
</div>
<br />
<p>Github 블로그 디자인과 관련해서 이것저것 알아봤는데, 개인적으로는 위 블로그가 가장 유익했다. Github 블로그가 처음이라면 해당 블로그의 <b>GitHub Pages 블로그 따라하기</b> 과정을 따라서 진행하는 것을 권장한다.
</p>
<div class="crossline"></div>

### 1.4 Jekyll, Rubby ?

<p>
구글에 “github 블로그 시작하기” 혹은 “github 페이지 만드는 법” 등을 검색해보면 <span class="highlight1">github</span> 라는 단어 이외에도 보이는 문구가 있다. 바로 <span class="highlight1">Jekyll</span> 또는 <span class="highlight1">Rubby</span> 라는 단어이다.
<br /><br />
솔직하게 말해서 필자는 <span class="highlight1">Jekyll</span> 이나 <span class="highlight1">Rubby</span> 에 대해 모른다. 아마도 github 블로그를 구축하는데 사용되는 소스 프로그램인 것 같은데, 대부분 관련 프로그램을 사용하는 내용이 <b>Mac OS</b> 나 <b>Linux</b> 기반의 PC를 기준으로 정리되어 있길래 따로 알아보지 않았다.
<br /><br />
위에서 언급한 추천 사이트의 튜토리얼 과정에도 <span class="highlight1">Jekyll</span> 을 사용해서 테스트하는 항목이 있는데, <b>Windows OS</b> 기반의 PC에서는 해당 기능을 이용하려면 별도의 방법이 필요한 것 같았다. 직접 블로그를 관리해보면서 느낀 점은 <span class="highlight1">Jekyll</span> 에 대해 몰라도 블로그 구축에는 문제가 없다는 것이다.
</p>

>앞서 언급한 <a href="https://devinlife.com/howto/" target="_blank">취미로 코딩하는 개발자</a> 블로그의 튜토리얼 중에도 <span class="highlight1">Bundle</span> 명령어를 이용해 웹페이지에 https//127.0.0.1:4000 주소를 입력해서 로컬 컴퓨터에 블로그 페이지를 띄우는 방법을 소개하고 있지만, 기본적으로 <b>Windows</b> 에서 <b>git bash</b>를 이용하는 경우에는 <span class="highlight1">Bundle</span> 명령어 자체가 없다고 나온다. 그래서 필자는 해당 항목들을 스킵해가며 진행했다.

<div class="crossline"></div>

### 1.5 테마 선택하기
블로그를 개설하는 가장 쉬운 방법은 <a href="http://jekyllthemes.org/" target="_blank">지킬 테마 사이트</a> 에서 원하는 테마를 고른 뒤, 본인의 github repository로 <span class="highlight1">Fork</span> 한 뒤, 해당 repository 이름을 <span class="highlight1">username.github.io </span>로 설정해주는 방법이다.

<div class="left">
<img src="https://1drv.ms/i/c/ce3c26eef978e16d/IQMY7LBSShIBTbtSrrurKaAsAZ8dtdMaDFysmoJ1xYA9OCU?width=1024" alt="Example Image" />
</div>
<br />
<p>
<b>지킬 테마 사이트</b>에 들어가보면 위 그림처럼 여러가지 테마가 보일텐데, 결론부터 이야기하자면 <a href="https://github.com/mmistakes/minimal-mistakes" target="_blank">minimal-mistakes</a>  테마로 시작하는 것을 권장한다. 위에서 소개한 github 블로그를 비롯해 많은 사람들이 <b>minimal-mistakes</b> 테마를 사용하고 있는데, 이 점이 중요한 이유는 블로그 디자인을 수정하고 싶을 때, 어떤 부분을 어떻게 수정해야하는지에 대해 검색하기가 쉽기 때문이다.
</p>

>예를 들어, 본인이 포스팅 하고자 하는 글에 카테고리 또는 태그 항목을 추가하길 원하는데, <b>minimal-mistakes</b> 테마를 이용하는 경우는 /pages/category-archive.md 파일을 수정하고, _config.yml 파일의 categories_archive: 항목을 수정하는 정도로 쉽게 카테고리를 추가할 수 있지만, 이와 다른 형식의 테마를 사용하는 경우 /pages/category-archive.md라는 파일이 존재하지 않을 가능성이 높으며, category 를 추가하기 위해 본인이 추가하고자 하는 category 항목을 일일이 .md 파일로 정의해야하는 경우도 있다.

<p>
아마도 github 페이지가 <span class="highlight1">Jekyll</span> 을 기반으로 디자인이 가능하기 때문에 특정 형식에 얽매이지 않고, 다양한 방식으로 구축이 가능하기 때문이라고 생각되는데… 처음 접하는 사람 입장에서는 시작부터 어떻게 해야할 지 모르는 상황에 놓이게 된다.
<br/><br />
따라서 개인적인 생각으로는 일단 가장 보편적인 <b>minimal-mistakes</b> 테마를 이용해서 기본 기능<b>(메뉴/카테고리/댓글 기능 등)</b> 위주로 블로그를 운영하고, 어느정도 익숙해진 뒤 본격적으로 커스터마이징 하는 것을 추천한다.
</p>
