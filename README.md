# 커먼플러스🛒 : 쇼핑몰 통합 관리 서비스
<div align="center">
  <img width="500" alt="main_image_5" src="https://github.com/harin1212/spring/assets/99604087/167173cf-b706-446e-a5ca-eaf6d64f5eae">
    <img width="500" alt="main_image_3" src="https://github.com/harin1212/spring/assets/99604087/5175999e-154f-44ac-99e3-7f62c11e43e1">
</div>

- 배포 URL : https://commonplus.store/
- Test ID : test@test.com
- Test PW : qqqqqqqq!

<br>

## 프로젝트 소개

- 커먼플러스는 ‘다중 플랫폼 쇼핑몰’ 통합 관리 서비스 입니다.
- 쿠팡, 11번가, g마켓, 옥션 셀러들은 자신의 쇼핑몰 계정을 등록하고, 보관상품 등록 + 쇼핑몰 그룹 등록을 통해 외부로 상품을 등록할 수 있습니다.

***※ 보안상의 이유로 코드는 공개되지 않습니다.***
<br>

## 팀원 구성 및 역할

| **이름** |                                                                   **GitHub**                                                                   |                                                                           **구현 기능**                                                                            |
|:------:|:----------------------------------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------------:|
|  김은지   | [<img src="https://avatars.githubusercontent.com/u/78680486?v=4" height="100" width="100"> <br/> @thisiseunji](https://github.com/thissieunji) |     <ul><li>프로젝트 매니저</li><li>프로젝트 초기셋팅</li><li>외부상품 등록, 수정, 조회 기능</li><li>카테고리 조회, 고시정보 조회 기능</li><li>외부몰 계정 등록, 수정, 삭제, 조회 기능</li><li>택배사 조회 기능</li></ul>     |
|  김서영   |  [<img src="https://avatars.githubusercontent.com/u/111834724?v=4" height="100" width="100"> <br/> @seoyeong12](https://github.com/seoyeong12)   |                                                              <ul><li>비밀번호 재설정 기능</li><li>외부상품 등록, 수정, 조회 기능</li><li>주소록 등록, 수정, 조회 기능</li><li>출고지 등록, 수정, 조회,기타 기능</li><li>쇼핑몰 그룹 생성, 조회, 수정, 삭제 기능</li><li>상품 가격/재고/판매상태 수정, 조회 기능</li><li>커스텀 에러</li><li>쿠팡 반품 기능</li></ul>                                                                 |
|  김하린   |   [<img src="https://avatars.githubusercontent.com/u/99604087?v=4" height="100" width="100"> <br/> @harin1212](https://github.com/harin1212)   | <ul><li>로그인, 이메일 중복확인, 회원가입, 로그아웃 기능</li><li>이미지 및 상품 등록, 상품 수정, 조회, 삭제</li><li>외부몰 주문 조회, 취소</li><li>송장 입력, 수정</li><li>상품 준비중으로 변경</li><li>CI/CD 구축 및 배포</li> |
| 박지호  | [<img src="https://github.com/user-attachments/assets/5b67ef40-5da0-4622-b7ad-2b2104564372" alt="KakaoTalk" height="100"> <br/> @pjho4746](https://github.com/pjho4746)   | <ul><li>Swagger 문서 (로컬/배포 서버)</li><li>11번가 반품 기능</li> <li>11번가 고시 정보 DB 덮어쓰기 옵션 설정</li> |
| 김세은  | [<img src="https://github.com/user-attachments/assets/e227e84c-0f69-4d19-a34f-cffe2024afa4" height="100"> <br/> @seeun01](https://github.com/seeun01)   | <ul><li>쇼핑몰 배송지 관리 기능 구현</li><li>쇼핑몰 등록 상품 관리 기능 구현</li> |

<br>

## 시작가이드

### 환경
* java 17
* Gradle 8.x
* Spring Boot 3.2.x
* MySQL 8.x

<br>

### 프론트엔드 기술 스택

* Next.js 
* TypeScript
* module CSS
* fetch API
* Storybook 

<br>

### 실행과정
<pre><code>git clone https://github.com/commonplus/commonplus-back.git
cd commonplus-back
build gradle
gradlew run
</code></pre>

<pre><code>npm run dev
npm run build
npm run storybook
</code></pre>
<br>



### 환경변수
> [노션페이지](https://www.notion.so/env-8308e3ffd01843b8a49d9a173452c2a5?pvs=4) 참고

<br>

### 폴더 구조 설명
```
 src
 ┣ app     /* 앱 라우터 페이지 디렉토리입니다. */
 ┃ ┣ find     // 비밀번호 재설정 페이지
 ┃ ┃ ┣ page.module.css
 ┃ ┃ ┗ page.tsx
 ┃ ┣ group     // 쇼핑몰 그룹 관리 페이지
 ┃ ┃ ┣ _components
 ┃ ┃ ┃ ┗ modal
 ┃ ┃ ┃ ┃ ┣ CategoryGroup.tsx
 ┃ ┃ ┃ ┃ ┣ CategoryGroup.type.ts
 ┃ ┃ ┃ ┃ ┣ NoticeDetailGroup.tsx
 ┃ ┃ ┃ ┃ ┣ NoticeDetailGroup.type.ts
 ┃ ┃ ┃ ┃ ┣ NoticeGroup.tsx
 ┃ ┃ ┃ ┃ ┗ NoticeGroup.type.ts
 ┃ ┃ ┣ page.module.css
 ┃ ┃ ┗ page.tsx
 ┃ ┣ login     // 로그인 페이지
 ┃ ┃ ┣ _components
 ┃ ┃ ┃ ┣ LoginForm.tsx
 ┃ ┃ ┃ ┗ LoginForm.type.ts
 ┃ ┃ ┣ page.module.css
 ┃ ┃ ┗ page.tsx
 ┃ ┣ mall     // 쇼핑몰 계정 관리 페이지
 ┃ ┃ ┣ _components
 ┃ ┃ ┃ ┣ modal
 ┃ ┃ ┃ ┃ ┣ CheckMall.tsx
 ┃ ┃ ┃ ┃ ┣ CheckMall.type.ts
 ┃ ┃ ┃ ┃ ┣ DeleteMall.tsx
 ┃ ┃ ┃ ┃ ┣ RegisMall.tsx
 ┃ ┃ ┃ ┃ ┣ RegisMall.type.ts
 ┃ ┃ ┃ ┃ ┣ SelectMall.tsx
 ┃ ┃ ┃ ┃ ┣ SelectMall.type.ts
 ┃ ┃ ┃ ┃ ┗ SuccessMall.tsx
 ┃ ┃ ┃ ┗ step
 ┃ ┃ ┃ ┃ ┣ AuctionStep.ts
 ┃ ┃ ┃ ┃ ┣ CoupangStep.ts
 ┃ ┃ ┃ ┃ ┣ ElevenStep.ts
 ┃ ┃ ┃ ┃ ┗ GmarketStep.ts
 ┃ ┃ ┣ page.module.css
 ┃ ┃ ┣ page.tsx
 ┃ ┃ ┗ page.type.ts
 ┃ ┣ product     // 보관 상품 페이지
 ┃ ┃ ┣ edit
 ┃ ┃ ┃ ┣ _utils
 ┃ ┃ ┃ ┃ ┗ utils.ts
 ┃ ┃ ┃ ┗ page.tsx
 ┃ ┃ ┣ management     // 상품 관리 페이지
 ┃ ┃ ┃ ┣ mall
 ┃ ┃ ┃ ┃ ┣ page.module.css
 ┃ ┃ ┃ ┃ ┗ page.tsx
 ┃ ┃ ┃ ┗ storage     // 보관 상품 관리
 ┃ ┃ ┃ ┃ ┣ @modal
 ┃ ┃ ┃ ┃ ┃ ┣ (.)uploadShoppingmall
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ _ui
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ Empty
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ Empty.module.css
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ index.tsx
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ MallList
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ MallList.module.css
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ index.tsx
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ Section
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ Section.module.css
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┣ Section.type.ts
 ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ index.tsx
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ page.tsx
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ uploadShoppingmall.module.css
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ uploadShoppingmall.type.ts
 ┃ ┃ ┃ ┃ ┃ ┗ default.ts
 ┃ ┃ ┃ ┃ ┣ uploadShoppingmall     // intercept routing segment
 ┃ ┃ ┃ ┃ ┃ ┗ page.tsx
 ┃ ┃ ┃ ┃ ┣ layout.tsx
 ┃ ┃ ┃ ┃ ┗ page.tsx
 ┃ ┃ ┣ new     // 보관 상품 등록 페이지
 ┃ ┃ ┃ ┣ layout.tsx
 ┃ ┃ ┃ ┗ page.tsx
 ┃ ┃ ┣ page.tsx
 ┃ ┃ ┣ template.module.css
 ┃ ┃ ┣ template.tsx
 ┃ ┃ ┗ utils.ts
 ┃ ┣ signup     // 회원가입 페이지
 ┃ ┃ ┣ _components
 ┃ ┃ ┃ ┣ SignupForm.tsx
 ┃ ┃ ┃ ┗ SignupForm.type.ts
 ┃ ┃ ┣ page.module.css
 ┃ ┃ ┗ page.tsx
 ┃ ┣ error.tsx
 ┃ ┣ global-error.tsx
 ┃ ┣ globals.css
 ┃ ┣ layout.tsx
 ┃ ┣ page.module.css
 ┃ ┗ page.tsx     // 메인 페이지
 ┣ assets     /* 이미지 디렉토리입니다. */
 ┃ ┣ images
 ┃ ┗ ┗ icons     // icon asset
 ┣ components     /* 컴포넌트 디렉토리입니다. */
 ┃ ┣ atoms
 ┃ ┃ ┣ Button     // 버튼 컴포넌트
 ┃ ┃ ┣ Dropdown     // Dropdown Select 컴포넌트
 ┃ ┃ ┣ Icon     // 아이콘
 ┃ ┃ ┣ Input     // 인풋
 ┃ ┃ ┃ ┣ Checkbox     // 체크박스 인풋
 ┃ ┃ ┃ ┣ DateInput     // react day picker 활용 날짜 입력 인풋
 ┃ ┃ ┃ ┣ Radio     // 라디오 인풋
 ┃ ┃ ┃ ┣ TextEditor     // react-quill 라이브러리 활용 텍스트 필드
 ┃ ┃ ┃ ┗ TextField     // input type text, number ..
 ┃ ┃ ┣ Logo     // 메인 로고
 ┃ ┃ ┣ Modal     // 모달
 ┃ ┃ ┣ RequireStar     // 필수 필드 빨간 별
 ┃ ┃ ┣ Table     // 표
 ┃ ┃ ┣ ToastPopup     // 토스트 팝업
 ┃ ┃ ┗ Typography     // 텍스트 표현하는 컴포넌트
 ┃ ┣ organisms
 ┃ ┃ ┣ EmptyBox
 ┃ ┃ ┣ Gnb     // 글로벌 네비게이션 바입니다.
 ┃ ┃ ┣ MallLnb 
 ┃ ┃ ┣ PageInformation
 ┃ ┃ ┣ ProductLnb     // 상품 페이지 컨텍스트에서 사용되는 local navigation bar
 ┃ ┃ ┣ SelectionButton     // 리젝된 컴포넌트입니다.
 ┃ ┃ ┗ productManagementTable     // 상품 관리 table
 ┃ ┃ ┃ ┣ Storage     // 보관 상품
 ┃ ┗ templates
 ┃ ┃ ┣ group
 ┃ ┃ ┃ ┣ address
 ┃ ┃ ┃ ┃ ┗ index.tsx
 ┃ ┃ ┃ ┣ category
 ┃ ┃ ┃ ┃ ┗ index.tsx
 ┃ ┃ ┃ ┣ form
 ┃ ┃ ┃ ┃ ┣ constants.tsx
 ┃ ┃ ┃ ┃ ┗ index.tsx
 ┃ ┃ ┃ ┗ table
 ┃ ┃ ┃ ┃ ┣ GroupTable.module.css
 ┃ ┃ ┃ ┃ ┣ GroupTable.tsx
 ┃ ┃ ┃ ┃ ┗ GroupTable.type.ts
 ┃ ┃ ┣ mall
 ┃ ┃ ┃ ┣ form
 ┃ ┃ ┃ ┃ ┗ constants.tsx
 ┃ ┃ ┃ ┗ table
 ┃ ┃ ┃ ┃ ┣ MallTable.module.css
 ┃ ┃ ┃ ┃ ┣ MallTable.tsx
 ┃ ┃ ┃ ┃ ┗ MallTable.type.ts
 ┃ ┃ ┣ product     // 상품 관련
 ┃ ┃ ┃ ┣ form     // 상품 등록 form template
 ┃ ┃ ┃ ┃ ┣ components
 ┃ ┃ ┃ ┃ ┃ ┣ ui     // 상품 등록 form에서 사용되는 UI 컴포넌트들
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ Fieldset
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ Header
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ ImageInput
 ┃ ┃ ┃ ┃ ┃ ┣ Form1.tsx
 ┃ ┃ ┃ ┃ ┃ ┣ Form2.tsx
 ┃ ┃ ┃ ┃ ┃ ┣ form.module.css
 ┃ ┃ ┃ ┃ ┃ ┗ index.tsx
 ┃ ┃ ┃ ┃ ┣ constants.tsx
 ┃ ┃ ┃ ┃ ┣ form.type.ts
 ┃ ┃ ┃ ┃ ┣ index.tsx
 ┃ ┃ ┃ ┃ ┣ provider.tsx
 ┃ ┃ ┃ ┃ ┗ types.ts
 ┃ ┃ ┃ ┗ management
 ┃ ┃ ┃ ┃ ┣ Storage
 ┃ ┃ ┃ ┃ ┃ ┗ index.tsx
 ┃ ┃ ┃ ┃ ┗ ProductManagement.module.css
 ┃ ┃ ┗ shopProduct
 ┃ ┃ ┃ ┗ table
 ┃ ┃ ┃ ┃ ┣ ShopProductTable.module.css
 ┃ ┃ ┃ ┃ ┣ ShopProductTable.tsx
 ┃ ┃ ┃ ┃ ┗ ShopProductTable.type.ts
 ┣ fonts
 ┃ ┗ index.ts
 ┣ hooks     /* 커스텀 혹이 위치하는 폴더입니다. */
 ┃ ┣ useDidMountAfterOnceEffect.ts
 ┃ ┣ useDidMountEffect.ts
 ┃ ┣ useKeyDown.ts
 ┃ ┣ useModal.ts
 ┃ ┣ useOutsideClick.ts
 ┃ ┣ usePreviewImage.ts
 ┃ ┣ useToast.ts
 ┃ ┣ useToggle.ts
 ┃ ┗ withRequireStar.tsx
 ┣ services     /* API 관련 로직의 디렉토리 입니다. */
 ┃ ┣ creates
 ┃ ┃ ┣ product
 ┃ ┃ ┃ ┣ createProduct.ts
 ┃ ┃ ┃ ┣ createProductImage.ts
 ┃ ┃ ┃ ┗ createProductProcess.ts
 ┃ ┃ ┣ postGroupRegis.ts
 ┃ ┃ ┣ postMallCheck.ts
 ┃ ┃ ┣ postMallRegis.ts
 ┃ ┃ ┣ postUserJoin.ts
 ┃ ┃ ┣ postUserLogin.ts
 ┃ ┃ ┣ postUserLogout.ts
 ┃ ┃ ┣ postUserResetPwd.ts
 ┃ ┃ ┗ postUserResetPwdEmail.ts
 ┃ ┣ deletes
 ┃ ┃ ┣ deleteMall.ts
 ┃ ┃ ┗ deleteProduct.ts
 ┃ ┣ reads
 ┃ ┃ ┣ mallGroup
 ┃ ┃ ┃ ┗ getMallGroup.ts
 ┃ ┃ ┣ product
 ┃ ┃ ┃ ┣ getProduct.ts
 ┃ ┃ ┃ ┗ getProductList.ts
 ┃ ┃ ┣ user
 ┃ ┃ ┣ getAddressList.ts
 ┃ ┃ ┣ getCategory.ts
 ┃ ┃ ┣ getCategoryList.ts
 ┃ ┃ ┣ getCategoryMeta.ts
 ┃ ┃ ┣ getDeliveryCompany.ts
 ┃ ┃ ┣ getGroupList.ts
 ┃ ┃ ┣ getMall.ts
 ┃ ┃ ┣ getMallList.ts
 ┃ ┃ ┣ getOfficeNotice.ts
 ┃ ┃ ┣ getOfficeNoticeList.ts
 ┃ ┃ ┣ getShippingList.ts
 ┃ ┃ ┣ getShippingPolicies.ts
 ┃ ┃ ┗ getUserCheckEmail.ts
 ┃ ┗ updates
 ┃ ┃ ┗ product
 ┃ ┃ ┃ ┣ patchProduct.ts
 ┃ ┃ ┃ ┣ patchProductImage.ts
 ┃ ┃ ┃ ┗ patchProductProcess.ts
 ┣ stories     /* 스토리북 디렉토리 입니다. */
 ┃ ┣ atoms
 ┃ ┗ organisms
 ┣ types     /* 범용 타입 디렉토리 입니다. */
 ┃ ┣ mall.ts
 ┃ ┣ status.ts
 ┃ ┣ styleTypes.ts
 ┃ ┗ utilityTypes.ts
 ┣ utils     /* utils 디렉토리 입니다. */
 ┃ ┣ constants
 ┃ ┃ ┣ config.ts
 ┃ ┃ ┣ mall.ts
 ┃ ┃ ┣ path.ts
 ┃ ┃ ┣ route.ts
 ┃ ┃ ┗ style.ts
 ┃ ┣ error
 ┃ ┃ ┣ errorCode.ts
 ┃ ┃ ┗ errorMessage.ts
 ┃ ┣ date.ts
 ┃ ┣ object.ts
 ┃ ┣ string.ts
 ┗ ┗ token.ts
```

<br>

### 데이터베이스 설정
<pre><code>create database commonplus character set utf8mb4 collate utf8mb4_general_ci;</code></pre>

<br>

### 커밋 메시지 컨벤션
- feat	새로운 기능 추가
- fix	버그 수정
- docs	문서 관련
- style	스타일 변경
- refactor	코드 리팩토링
- test	테스트 관련 코드
- build	빌드 관련 파일 수정
- perf	성능 개선
- ci	CI 설정 파일 수정
- storybook 	스토리북 관련 파일 작성 및 수정
- conf 	설정 관련 수정
- type 	타입과 관련된 작업
- asset	애셋 파일 추가
