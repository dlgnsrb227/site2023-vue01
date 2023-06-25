<template>
  <div className="intro__program container">
    <h2 className="react">React.js</h2>
    <p>
      React.js는 페이스북에서 개발한 오픈 소스 JavaScript 라이브러리로, 사용자
      인터페이스(UI)를 구축하기 위해 사용됩니다.
      <br />
      React는 재사용 가능한 UI 컴포넌트를 작성하고 이를 조합하여 복잡한 UI를
      만들 수 있도록 돕는다는 점에서 매우 강력하고 인기 있는 도구입니다.
    </p>
    <p>
      React는 가상 DOM(Virtual DOM) 기술을 기반으로 작동합니다.
      <br />
      이는 React가 UI 변경 사항을 실제 DOM에 직접 적용하는 대신 가상 DOM에 변경
      사항을 적용한 다음 최소한의 DOM 조작으로 업데이트를 수행하는 것을
      의미합니다. <br />
      이 방식은 성능을 향상시키고 웹 애플리케이션의 반응성을 개선하는 데 도움이
      됩니다.
    </p>
    <div className="intro__program__desc">
      <span>React.js 주요특징</span>
      <ul>
        <li>
          컴포넌트 기반: React는 재사용 가능한 UI 컴포넌트를 작성하는 데 초점을
          맞추고 있습니다.
          <br />
          각 컴포넌트는 자체적으로 동작하며, 다른 컴포넌트와 조합하여 복잡한
          UI를 구성할 수 있습니다.
        </li>
        <li>
          가상 DOM: React는 가상 DOM을 사용하여 최소한의 DOM 조작으로 업데이트를
          수행합니다.
          <br />
          이는 변경 사항을 효율적으로 적용하고 성능을 향상시킵니다.
        </li>
        <li>
          단방향 데이터 흐름: React는 단방향 데이터 흐름을 채택하고 있습니다.
          <br />
          데이터는 상위 컴포넌트에서 하위 컴포넌트로 흘러가며, 하위 컴포넌트는
          상위 컴포넌트의 데이터를 수정할 수 없습니다. <br />
          이는 애플리케이션의 상태 변화를 추적하기 쉽게 만들어줍니다.
        </li>
        <li>
          JSX: JSX는 JavaScript를 확장한 문법으로, JavaScript 코드 안에서 XML과
          유사한 구문을 사용하여 컴포넌트의 구조와 모양을 정의할 수 있게 합니다.
          <br />
          이는 가독성을 높이고 컴포넌트의 렌더링 로직과 UI 구성 요소를 한 곳에서
          관리할 수 있게 도와줍니다.
        </li>
      </ul>
    </div>
  </div>
  <div className="intro__program container">
    <h2 className="vue">Vue.js</h2>
    <p>
      Vue.js는 사용자 인터페이스를 구축하기 위한 프로그레시브 프레임워크입니다.
      <br />즉, 작은 규모의 프로젝트부터 복잡한 단일 페이지 애플리케이션까지
      다양한 규모와 요구사항에 맞게 점진적으로 확장할 수 있습니다.
      <br />
      Vue.js는 MVVM(Model-View-ViewModel) 패턴을 기반으로 하며, 가상 DOM(Virtual
      DOM)을 사용하여 성능을 향상시킵니다.
    </p>
    <p>
      Vue.js는 HTML, CSS 및 JavaScript와 통합하여 사용할 수 있도록 설계되어
      있습니다.<br />
      애플리케이션의 사용자 인터페이스를 작성하기 위해 Vue.js의 템플릿 문법을
      사용할 수 있으며,<br />
      이를 통해 데이터와 DOM을 바인딩하고, 반응형으로 업데이트할 수 있습니다.
      <br />
      또한, Vue.js는 컴포넌트 기반 아키텍처를 제공하여 재사용 가능한 UI 요소를
      만들고 조합할 수 있습니다.
    </p>
    <div className="intro__program__desc">
      <span>Vue.js의 주요특징</span>
      <ul>
        <li>
          반응형 데이터 바인딩: Vue.js는 데이터와 DOM 요소를 양방향으로
          바인딩하여 데이터 변경 시 자동으로 화면을 업데이트할 수 있습니다.<br />
          이를 통해 개발자는 직접 DOM 조작을 할 필요 없이 데이터 상태만 관리하면
          됩니다.
        </li>
        <li>
          컴포넌트 기반 아키텍처: Vue.js는 재사용 가능한 컴포넌트를 생성하고
          조합할 수 있는 컴포넌트 기반 아키텍처를 제공합니다. <br />각
          컴포넌트는 자체의 데이터, 템플릿, 스타일을 갖고 있으며, 상위
          컴포넌트에서 하위 컴포넌트로 데이터를 전달할 수 있습니다.
        </li>
        <li>
          가상 DOM: Vue.js는 가상 DOM을 사용하여 변경된 부분만 실제 DOM에
          적용함으로써 성능을 최적화합니다.<br />
          가상 DOM은 실제 DOM과 동기화되며, 변경된 부분만 실제 DOM에 반영하여
          불필요한 렌더링을 줄여줍니다.
        </li>
        <li>
          디렉티브: Vue.js는 HTML 태그에 v- 접두사가 있는 디렉티브를 사용하여
          템플릿에서 동적인 동작을 수행할 수 있습니다.<br />
          예를 들어, v-bind 디렉티브를 사용하여 요소의 속성을 데이터에
          연결하거나, v-for 디렉티브를 사용하여 배열을 반복적으로 렌더링할 수
          있습니다.
        </li>
        <li>
          라우팅: Vue.js는 vue-router를 통해 클라이언트 측 라우팅을
          지원합니다.<br />
          이를 사용하여 다른 URL에 대한 라우팅 규칙을 정의하고, 컴포넌트 간의
          전환과 상태 관리를 쉽게 처리할 수 있습니다.
        </li>
        <li>
          상태 관리: Vue.js는 Vuex라는 상태 관리 패턴 및 라이브러리를
          제공합니다.<br />
          Vuex를 사용하여 애플리케이션의 상태를 중앙 집중식으로 관리하고, 다른
          컴포넌트 간의 데이터 공유와 효율적인 상태 업데이트를 수행할 수
          있습니다.
        </li>
      </ul>
    </div>
  </div>
  <div className="intro__program container">
    <h2 className="vite">Vite.js</h2>
    <p>
      Vite.js는 현대적인 웹 개발을 위한 빠르고 경량화된 웹 개발 빌드
      도구입니다.<br />
      Vue.js 팀에서 개발한 Vite.js는 Vue.js 애플리케이션 개발을 위해 특히
      최적화되었지만, 다른 프레임워크나 라이브러리에도 사용할 수 있습니다.<br />
      Vite.js는 개발 환경에서의 빠른 개발 속도와 최적화된 빌드를 제공하여
      개발자들에게 탁월한 개발 경험을 제공합니다.
    </p>
    <div className="intro__program__desc">
      <span>Vite.js 주요특징</span>
      <ul>
        <li>
          빠른 개발 서버: Vite.js는 개발 서버를 통해 빠른 개발 속도를
          제공합니다.<br />
          개발 서버는 기본적인 자산 변환 및 모듈 해석을 실시간으로 처리하며,
          브라우저로부터의 요청에 필요한 자산을 빠르게 제공합니다.<br />
          이는 변경된 파일만 다시 빌드하여 핫 리로딩(Hot Reloading)을 지원하고,
          개발 중인 애플리케이션의 변경 사항을 실시간으로 반영할 수 있도록
          도와줍니다.
        </li>
        <li>
          빠른 빌드: Vite.js는 빌드 과정에서 미리 컴파일된 모듈을 캐싱하여
          향상된 성능을 제공합니다.<br />
          이는 개발 중에도 미리 컴파일된 모듈을 활용하므로, 빌드 시간을 크게
          단축시켜 줍니다.<br />
          또한, 동적 임포트(Dynamic Import)를 통해 필요한 모듈만 요청하여 번들
          크기를 최소화합니다.
        </li>
        <li>
          ES 모듈 지원: Vite.js는 네이티브 ES 모듈 지원을 통해 모듈 시스템을
          기반으로 개발할 수 있도록 합니다.<br />
          이는 각 파일이 별도의 모듈로 처리되므로, 효율적인 종속성 관리와 번들
          크기 최적화를 가능하게 합니다.
        </li>
        <li>
          다중 프레임워크 지원: Vite.js는 Vue.js를 위해 특별히
          최적화되었지만,<br />
          React, Preact, Lit, Svelte 등과 같은 다른 프레임워크 및 라이브러리와도
          함께 사용할 수 있습니다.<br />
          따라서 개발자들은 선호하는 프레임워크를 사용하여 Vite.js의 이점을
          활용할 수 있습니다.
        </li>
        <li>
          플러그인 시스템: Vite.js는 다양한 플러그인을 통해 기능을 확장할 수
          있는 유연한 플러그인 시스템을 제공합니다.<br />
          개발자들은 필요에 따라 플러그인을 추가하거나 직접 커스텀 플러그인을
          작성하여 개발 환경을 더욱 효율적으로 구성할 수 있습니다.
        </li>
      </ul>
    </div>
  </div>
  <div className="intro__program container">
    <h2 className="next">Next.js</h2>
    <p>
      Next.js는 React 기반의 서버 사이드 렌더링(SSR) 및 정적 사이트 생성(Static
      Site Generation, SSG)을 지원하는 웹 프레임워크입니다.<br />
      Next.js는 React의 기능을 확장하고 보강하여 웹 애플리케이션의 개발을
      간소화하고 성능을 최적화하는 데 도움을 줍니다.
    </p>
    <div className="intro__program__desc">
      <span>React.js 주요특징</span>
      <ul>
        <li>
          서버 사이드 렌더링 (SSR): Next.js는 서버 사이드 렌더링을 기본적으로
          지원합니다.<br />
          이는 서버에서 초기 HTML을 생성하고 클라이언트로 전송하여 초기 로딩
          속도를 향상시킵니다.<br />
          SSR은 검색 엔진 최적화(SEO)에 유리하며, 동적인 콘텐츠를 렌더링하거나
          사용자에게 개인화된 콘텐츠를 제공하는 데 유용합니다.
        </li>
        <li>
          정적 사이트 생성 (SSG): Next.js는 정적 사이트 생성을 지원하여 사전에
          페이지를 미리 렌더링하여 정적인 HTML 파일을 생성할 수 있습니다. 이를
          통해 웹 페이지의 로딩 속도를 크게 개선할 수 있습니다.<br />
          정적 사이트 생성은 블로그, 제품 목록, 문서 페이지 등과 같이 콘텐츠가
          자주 변경되지 않는 경우에 적합합니다.
        </li>
        <li>
          자동 코드 분할 (Automatic Code Splitting): Next.js는 자동으로 페이지
          간에 필요한 JavaScript와 CSS를 분할하여 로딩 속도를 최적화합니다.<br />
          각 페이지는 필요한 코드만을 로드하므로 초기 로딩 시간이 단축되고,
          사용자 경험을 향상시킵니다.
        </li>
        <li>
          클라이언트 사이드 라우팅 (Client-Side Routing): Next.js는 클라이언트
          사이드 라우팅을 제공하여 사용자의 인터랙션에 따라 필요한 컴포넌트만
          로드하고 업데이트할 수 있습니다.<br />
          이를 통해 애플리케이션의 성능을 향상시키고, 부드러운 페이지 전환을
          제공할 수 있습니다.
        </li>
        <li>
          API 라우트: Next.js는 API 라우트를 제공하여 서버리스 함수 형태로
          백엔드 엔드포인트를 구성할 수 있습니다.<br />
          이를 활용하여 데이터 요청 및 처리를 위한 API 엔드포인트를 구축할 수
          있습니다.
        </li>
        <li>
          환경 설정 간편화: Next.js는 기본적으로 구성이 간단하며, 쉬운 설정
          옵션을 제공합니다.<br />
          Babel, Webpack, Hot Module Replacement(HMR) 등의 도구와 기능을 미리
          구성되어 있어 개발자는 별도의 설정 없이 바로 개발을 시작할 수
          있습니다.
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss">
.intro__program {
  margin-top: 100px;
  h2 {
    display: inline-flex;
    justify-content: center;
    align-items: flex-end;
    width: 100%;
    height: 35px;
    font-size: 35px;
    font-weight: 900;
    background-color: #1eff0057;
    border-radius: 30px;
    margin-bottom: 20px;
    position: relative;
    &::before {
      content: "";
      position: absolute;
      z-index: -1;
      left: 50%;
      transform: translateX(-50%);
      background-image: url("data:image/svg+xml,%0A%3Csvg width='40' height='40' xmlns='http://www.w3.org/2000/svg' viewBox='-11.5 -10.23174 23 20.46348'%3E%3Ctitle%3EReact Logo%3C/title%3E%3Ccircle cx='0' cy='0' r='2.05' fill='%2361dafb'/%3E%3Cg stroke='%2361dafb' stroke-width='1' fill='none'%3E%3Cellipse rx='11' ry='4.2'/%3E%3Cellipse rx='11' ry='4.2' transform='rotate(60)'/%3E%3Cellipse rx='11' ry='4.2' transform='rotate(120)'/%3E%3C/g%3E%3C/svg%3E");
      background-size: contain;
      background-position: center center;
      background-repeat: no-repeat;
      width: 100px;
      height: 100px;
    }
    &.vue::before {
      background-image: url("data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg version='1.1' viewBox='0 0 261.76 226.69' width='40' height='40' xmlns='http://www.w3.org/2000/svg'%3E%3Cg transform='matrix(1.3333 0 0 -1.3333 -76.311 313.34)'%3E%3Cg transform='translate(178.06 235.01)'%3E%3Cpath d='m0 0-22.669-39.264-22.669 39.264h-75.491l98.16-170.02 98.16 170.02z' fill='%2341b883'/%3E%3C/g%3E%3Cg transform='translate(178.06 235.01)'%3E%3Cpath d='m0 0-22.669-39.264-22.669 39.264h-36.227l58.896-102.01 58.896 102.01z' fill='%2334495e'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
    }
    &.vite::before {
      background-image: url("data:image/svg+xml,%3Csvg width='40' height='40' viewBox='0 0 410 404' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M399.641 59.5246L215.643 388.545C211.844 395.338 202.084 395.378 198.228 388.618L10.5817 59.5563C6.38087 52.1896 12.6802 43.2665 21.0281 44.7586L205.223 77.6824C206.398 77.8924 207.601 77.8904 208.776 77.6763L389.119 44.8058C397.439 43.2894 403.768 52.1434 399.641 59.5246Z' fill='url(%23paint0_linear)'/%3E%3Cpath d='M292.965 1.5744L156.801 28.2552C154.563 28.6937 152.906 30.5903 152.771 32.8664L144.395 174.33C144.198 177.662 147.258 180.248 150.51 179.498L188.42 170.749C191.967 169.931 195.172 173.055 194.443 176.622L183.18 231.775C182.422 235.487 185.907 238.661 189.532 237.56L212.947 230.446C216.577 229.344 220.065 232.527 219.297 236.242L201.398 322.875C200.278 328.294 207.486 331.249 210.492 326.603L212.5 323.5L323.454 102.072C325.312 98.3645 322.108 94.137 318.036 94.9228L279.014 102.454C275.347 103.161 272.227 99.746 273.262 96.1583L298.731 7.86689C299.767 4.27314 296.636 0.855181 292.965 1.5744Z' fill='url(%23paint1_linear)'/%3E%3Cdefs%3E%3ClinearGradient id='paint0_linear' x1='6.00017' y1='32.9999' x2='235' y2='344' gradientUnits='userSpaceOnUse'%3E%3Cstop stop-color='%2341D1FF'/%3E%3Cstop offset='1' stop-color='%23BD34FE'/%3E%3C/linearGradient%3E%3ClinearGradient id='paint1_linear' x1='194.651' y1='8.81818' x2='236.076' y2='292.989' gradientUnits='userSpaceOnUse'%3E%3Cstop stop-color='%23FFEA83'/%3E%3Cstop offset='0.0833333' stop-color='%23FFDD35'/%3E%3Cstop offset='1' stop-color='%23FFA800'/%3E%3C/linearGradient%3E%3C/defs%3E%3C/svg%3E%0A");
    }
    &.next::before {
      background-image: url("data:image/svg+xml,%3Csvg width='50' height='30' viewBox='0 0 100 61' fill='none' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Crect width='100' height='60.3333' fill='url(%23pattern0)'/%3E%3Cdefs%3E%3Cpattern id='pattern0' patternContentUnits='objectBoundingBox' width='1' height='1'%3E%3Cuse xlink:href='%23image0_11_1156' transform='scale(0.00333333 0.00552486)'/%3E%3C/pattern%3E%3Cimage id='image0_11_1156' width='300' height='181' xlink:href='data:image/png;base64,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'/%3E%3C/defs%3E%3C/svg%3E");
      top: -60px;
    }
  }
  p {
    margin-top: 50px;
    padding: 10px 30px;
    font-size: 18px;
  }

  .intro__program__desc {
    margin-top: 40px;
    padding: 0 30px;
    span {
      font-size: 24px;
      font-weight: 700;
    }
    ul {
      li {
        display: inline-block;
        margin-top: 15px;
        padding-left: 15px;
        position: relative;
        line-height: 1.2;

        &::before {
          content: "";
          width: 8px;
          height: 8px;
          background-color: #39493c;
          border-radius: 50%;
          position: absolute;
          left: 0;
          top: 5px;
        }
      }
    }
  }
}
</style>
