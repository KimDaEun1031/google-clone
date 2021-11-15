# google-clone
## 결과물 비교 왼쪽 원본 || 오른쪽 클론
![clondef](https://user-images.githubusercontent.com/73865700/141749092-ce35ef8b-36cf-41e3-993b-17a8dde22f62.PNG)

## 1회차 페이지
![clone](https://user-images.githubusercontent.com/73865700/141673930-b95584cb-55c9-4015-9708-491578490153.PNG)

#### > 1회차 - 약 3시간 소요
1. header 제작
2. section 영역 로고 위치 지정
3. footer 고정

#### > 2회차 - 약 4시간 소요
1. section 제작
2. footer 제작

> UI 제작 완료 - 약 7시간 소요

#### Code

## index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Google Clone</title>
    <link rel="shortcut icon" href="./image/icon/favicon.ico">
    <link rel="stylesheet" href="style.css">
    <script src="https://use.fontawesome.com/releases/v5.2.0/js/all.js"></script>
</head>
<!-- HTML과 CSS를 사용해 구글과 비슷한 UI를 구현하는 것이 목표 -->
<body>
    <header>
        <div class="header">
            <ul>
                <li><a href="#"><img src="./image/profile.png" alt="프로필" id="profile"></a></li>
                <li><a href="#"><img src="./image/dial-pad.svg" alt="앱" id="keypad"></a></li>
                <li><a href="#" id="photo">이미지</a></li> 
                <li><a href="#" id="mail">Gmail</a></li>         
            </ul>
        </div>       
    </header>
    <section>
        <div class="logo">
            <img src="./image/google-title.png" alt="구글 로고">
        </div>   
        <div class="search-box">
            <i class="fas fa-search"></i><input type="text" id="search"/>
            <a href="#"><i class="fas fa-microphone"></i></a>
            <a href="#"><i class="fas fa-keyboard"></i></a>       
        </div> 
        <div class="button-list">
            <button class="google-search">Google 검색</button>
            <button class="google-logo-list">I'm Feeling Lucky</button>
        </div> 
        <div class="sentence">
            <p>모든 여성의 경제적인 잠재력과 기회를 지원하는 <a href="#" >비영리 단체를 알아보세요.</a></p>
        </div>
        <div class="lang-service">
            <span>Google 제공 서비스 : <a href="#">English</a></span>
        </div>
    </section>
    <footer>
        <div class="footer-container">
            <div class="country">
                <p>대한민국</p>
            </div> 
            <hr/>
            <div class="info">
                <div class="first-info">
                    <a href="#">Google 정보</a>
                    <a href="#">광고</a>
                    <a href="#">비지니스</a>
                    <a href="#">검색의 원리</a>
                </div>
                <div class="second-info">
                    <a href="#">개인정보처리방침</a>
                    <a href="#">약관</a>
                    <a href="#">설정</a>                
                </div>
            </div>  
        </div>            
    </footer>
</body>
</html>
```

## style.css
```
/*전체 영역*/

* {
    list-style: none;
    font-family: Arial, Helvetica, sans-serif;
}

a:link {
    color: black;
    text-decoration: none;
}

a:visited {
    color: black;
    text-decoration: none;
}

a:hover {
    color: black;
    text-decoration: underline;
}

img {
    /*흐림 방지*/
    image-rendering: -webkit-optimize-contrast;
    transform: translateZ(0);
    backface-visibility: hidden;
}

/*header 영역*/

.header ul {
    display: flex;
    flex-direction: row-reverse;
    justify-content: flex-start;
    align-items: center;  
}

.header ul li a {
    margin-right: 20px;   
    font-size: 13px;
    color: rgb(75, 75, 75);
}

a #profile{
    margin-top: 6px;
    width: 35px;
    height: 35px;
    border-radius: 50%;
}

#mail {
    font-weight: 400;
}

#keypad {
    margin-top: 6px;
    max-width: 20px;
    width: 100%;
    height: auto;  
    /*svg 색상 변경*/
    filter: invert(53%) sepia(14%) saturate(0%) hue-rotate(257deg) brightness(83%) contrast(91%);
}

/*section 영역*/

section {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    margin-top: 13%;
}

/*logo 영역*/

.logo img {
    width: 280px;
    margin-top: 13%;
}

/*search 영역*/

.search-box {
    border: 1px solid;
    height: 45px;
    width: 550px;
    border-radius: 50px;
    border-color: rgb(207, 207, 207);
    margin-top: 30px;
}

.search-box .fa-search {
    margin-left: 15px;
    margin-top: 14px;
    height: 15px;
    width: 15px;
    color: rgb(145, 145, 145);
}

.search-box .fa-keyboard {
    float: right;
    margin-top: 11px;
    margin-right: 13px; 
    height: 20px;
    width: 20px;
    color: rgb(116, 116, 116);
}

.search-box .fa-microphone {
    float: right;
    margin-top: 11px;
    margin-right: 15px;
    margin-left: 5px;
    height: 20px;
    width: 20px;
    color: rgb(116, 116, 116);
}

.search-box #search {
    border: none;
    outline: none;
    width: 78%;
    margin: 6px;
}

.search-box:hover {
    border: none;
    box-shadow: 1px 1px 5px #ddd;
}

/*button 영역*/

.button-list button {
    border: none;
    outline: none;   
    height: 35px;   
    line-height: 30px;
    border-radius: 5px;
    font-size: 14px;
    margin-top: 30px;
    margin-right: 5px;
    background-color: rgb(248, 247, 247);
}

.button-list .google-search {
    width: 130px;
}

.button-list .google-logo-list {
    width: 150px;

}

.button-list button:hover {
    border: 1px solid;
    border-color: rgb(228, 228, 228);
    box-shadow: 1px 1px 5px #ddd;
}

/*sentence 영역*/

.sentence {
    margin-top: 10px;
    font-size: 13px;
}

.sentence a {
    color: rgb(5, 5, 209);
}

.sentence a:visited {
    color: rgb(105, 27, 179);
}

/*lang-service 영역*/

.lang-service {
    margin-top: 15px;
    font-size: 13px;
}

.lang-service a {
    color: rgb(5, 5, 209);
}

/*footer 영역*/

/*footer 고정*/
footer {
    position: fixed;
    left: 0px;
    bottom: 0px;
    height: 100px;
    width: 100%;
    background-color: rgb(243, 243, 243);
    color: white;
}

.footer-container hr {
    border-color: rgb(255, 255, 255);
}

footer .footer-container .country {
    font-size: 15px;
    margin-left: 28px;
    color: rgb(128, 128, 128);
}

footer .footer-container .info {
    display: flex;
    justify-content: space-between;
    font-size: 14px;
}

footer .footer-container .info .first-info{
    display: flex;
}

footer .footer-container .info .first-info a {
    margin-top: 6px;
    margin-left: 30px;
    color: rgb(128, 128, 128);
}

footer .footer-container .info .second-info{
    display: flex;
}

footer .footer-container .info .second-info a {
    margin-top: 6px;
    margin-right: 30px;
    color: rgb(128, 128, 128);
}

```
