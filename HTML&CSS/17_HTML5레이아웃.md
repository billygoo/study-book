
# 17장 HTML5 레이아웃 
## 배울 내용
1. 새로운 HTML5 레이아웃 요소와 사용법
2. `<div>` 요소에 대하여 유용한 대안을 제공하는 방법
3. 구 브라우저에서 HTML5 요소를 인식하게 하는 방법 

## 전통적인 HTML레이아웃 VS 새로운 HTML5 레이아웃 요소 
- 전통 
    - 헤더, 기사, 푸터, 사이드바 요소처럼 페이지에 잇는 관련 요소들을 그룹화하는 데 `<div>`요소를 사용
    - `<div>` 요소의 역할을 나타내는 데에는 class나 id 속성을 사용
- 새로운 
    - 페이지를 여러 부분으로 나눌 수 있는 새로운 요소들이 추가됨
    - `<header>`, `<nav>`, `<article>` 등의 태그

## 헤더와 푸터 `<header>` `<footer>`

- 사용 용도 
    - 사이트의 각 페이지의 상단과 하단에 표시되는 메인 헤더와 푸터에 사용
    - 페이지 내에 있는 각각의 `<article>`과 `<section>`에 대한 헤더와 푸터에 사용
- 예시
    - `<header>` 요소에 사이트의 이름과 메인 내비게시션을 포함
    - `<footer>` 요소에는 개인정보 취급 방침과 조항 그리고 조건에 대한 링크와 저작권 정보를 추가
    - 각각의 콘텐츠는 `<article>`과 `<section>` 요소를 사용


## 내비게이션 `<nav>`

- 사용 용도
    - 페이지 상단에 배치되는 메뉴같이 사이트에서 주요 내비게이션 블록을 포함하는 데 사용

---

    <nav>
		<ul>
			<li><a href="" class="current">홈</a></li>
			<li><a href="">교실</a></li>
			<li><a href="">케이터링</a></li>
			<li><a href="">소개</a></li>
			<li><a href="">연락처</a></li>
		</ul>
	</nav>

---

## 기사 `<article>`

- 사용 용도
    - 문서나 페이지 또는 사이트의 독립적인 부분을 구성하는 섹션을 나타냄 
- 예시
    - 신문의 기사나 블로그 항목, 사용자 의견, 포럼에서 올라온 글, 기타 콘텐츠의 다른 독립적인 부분으로 사용
- 규칙
    - `<article>` 요소는 중첩될 수 있다. 

---

	<article>
		<figure>
			<img src="images/bok-choi.jpg" alt="Bok Choi" />
			<figcaption>Bok Choi</figcaption>
		</figure>
		<hgroup>
			<h2>일본의 채식주의자</h2>
			<h3>런던에서의 5주 코스</h3>
		</hgroup>
		<p>5주간 전통적인 일본의 채식주의자 음식에 대해 소개하고 쌀과 국수 요리를 가르친다.</p>
	</article>    

---


## 사이드바 `<aside>`

- 사용 용도 
    - `<aside>`요소가 `<article>` 요소 내에서 사용 될 때
        - 기사와 관련은 있지만 전체적인 의미에서 필수적이지 않은 정보를 포함할 때 사용
        - 기사나 관련된 인용문이나 용어 설명을 `<aside>` 요소에 작성
    - `<aside>`요소가 `<article>` 요소 밖에서 사용 될 때
        - 전체 페이지와 관련된 콘텐츠에 대한 컨테이너 역할로 사용 
        - 사이트의 다른 섹션에 대한 링크, 최근 글 목록, 검색 박스, 최근 트윗 등에 사용 

---

    <aside>
    	<section class="popular-recipes">
    		<h2>인기 요리법</h2>
    		<a href="">야키토리(Yakitori) - 구운 닭</a>
    		<a href="">츠쿠네(Tsukune) - 닭꼬치</a>
    		<a href="">오코노미야키(Okonomiyaki)- 해물 부침개</a>
    		<a href="">미즈타키(Mizutaki) - 영계백숙</a>
    	</section>
    	<section class="contact-details">
    		<h2>연락처</h2>
    		<p>Yoko's Kitchen<br />
    			27 Redchurch Street<br />
    			Shoreditch<br />
    			London E2 7DP</p>
    	</section>
    </aside>

---


## 섹션 `<section>` 

- 사용 용도
    - 관련된 콘텐츠를 그룹화
- 예시
    - 홈페이지에 최신 뉴스, 인기 상품, 뉴스 레터 구독 등 페이지의 다양한 섹션을 구성 
- 규칙
    - 각 섹션은 자체적인 제목을 포함한다.
    - 섹션 하위에 다른 섹션을 구성할 수 있다.
    - 페이지가 하나의 고유한 콘텐츠를 포함하지 않는한 전체 페이지에 대한 래버로 사용해서는 안된다.
        - 최상위로는 `<div>` 요소를 사용한다.


---

	<section class="courses">
		<article>
			<figure>
				<img src="images/bok-choi.jpg" alt="Bok Choi" />
				<figcaption>Bok Choi</figcaption>
			</figure>
			<hgroup>
				<h2>일본의 채식주의자</h2>
				<h3>런던에서의 5주 코스</h3>
			</hgroup>
			<p>5주간 전통적인 일본의 채식주의자 음식에 대해 소개하고 쌀과 국수 요리를 가르친다.</p>
		</article>    
		<article>
			<figure>
				<img src="images/teriyaki.jpg" alt="Teriyaki sauce" />
				<figcaption>Teriyaki Sauce</figcaption>
			</figure>
			<hgroup>
				<h2>소스 마스터클래스</h2>
				<h3>1일 워크샵</h3>
			</hgroup>
			<p>1일 집중 코스에서는 다양한 일본 요리에서 사용할 수 있는 가장 맛있는 소스를 만드는 방법을 살펴본다.</p>
		</article>    
	</section>

---

## 헤더그룹화 `<hgroup>` 

- 사용 용도
    - `<h1>`부터 `<h6>` 요소까지 하나 이상을 그룹화하여 단일 제목으로 처리
- 예시
    - `<hgroup>` 요소 안에 `<h2>`요소 내 제목과 `<h3>` 요소 내 부제목을 포함하는데 사용

---

	<hgroup>
		<h2>일본의 채식주의자</h2>
		<h3>런던에서의 5주 코스</h3>
	</hgroup>

---

## 참조 `<figure>`, `<figcaption>`

- 사용 용도
    - 참조 설명을 추가하는데 사용 
- 예시
    - 이미지, 비디오, 그래프, 다이어그램, 코드 예제, 메인 기사에 대한 부가 설명을 위해 사용 
- 규칙
    - `<figure>` 요소의 콘텐츠가 다른 부분으로 이동하여도 기사의 내용에 지장이 없는 요소에 사용한다. 


---

	<figure>
		<img src="images/teriyaki.jpg" alt="Teriyaki sauce" />
		<figcaption>Teriyaki Sauce</figcaption>
	</figure>

---

## 요소 그룹화 `<div>`

- 사용 용도
    - 관련된 요소를 그룹화하는 방법

> 기존 추가된  HTML5 요소는 명시적으로 언급한 용도 외에는 다른 목적으로 사용하면 안된다.  


## 블록 레벨 요소 링크
블록 레벨 요소 주위에 `<a>` 요소를 사용해 전체 블록 링크로 만들 수 있다.


## 구 브라우저 지원 방법
구 브라우저는 새로운 **HTML5 요소를 인식하지 못하면 자동적으로 인라인 요소로 처리한다.**

- 지원 방법
    - 새로운 요소가 블록 레벨 요소로 표시되도록 CSS를 추가한다.
    - 공개된 자바 스크립트를 사용해 해당 요소가 동작 하게 한다.
        - HTML5 shiv : https://github.com/aFarkas/html5shiv
        - IE 9보다 낮은 경우 수행되는 조건부 주석 안에 넣는다.

---
    
    <!DOCTYPE html>
    <html>
    	<head>
    		<title>HTML5 레이어</title>

    		<style type="text/css">
    			header, section, footer, aside, nav, article, figure, figcaption {
    				display: block;}
    			
    		<!--[if lt IE 9]>
    		<script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
    		<![endif]-->
    	</head>
    	<body>
             ...
    	</body>
    </html>

---