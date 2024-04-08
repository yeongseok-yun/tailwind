<template>
  <body class="bg-[#ddd]">
    <div class="bg-[#ACD1DC] p-10">
      <div class="flex flex-col bg-white p-5 flex-wrap gap-10">
        <div class="flex gap-10 flex-col md:flex-row m-auto md:m-0">
          <img
            src="@/assets/backgimg.jpg"
            alt="프로필"
            class="w-48 aspect-square"
          />
          <div>
            <h1 class="text-4xl text-[GRAY] md:mt-10">윤영석</h1>
            <p class="text-gray-500 mt-2">개발자</p>
          </div>
        </div>

        <div class="flex flex-row">
          <div class="flex flex-col gap-10 md:flex-row md:gap-10">
            <div class="md:w-[200px] shrink-0 px-2">
              <h2
                class="text-xl text-[#2390B3] font-bold border-l-4 border-[#2390B3] pl-2 mb-2"
              >
                연락처
              </h2>
              <ul class="space-y-2 mb-10">
                <li>
                  <i class="fas fa-envelope text-gray-400 mr-1"></i>
                  antiravesol@gmail.com
                </li>
                <!-- <li>
                  <i class="fas fa-phone text-gray-400 mr-1"></i>010-0000-0000
                </li> -->
                <li
                  @click="openNewTab('https://github.com/yeongseok-yun')"
                  style="cursor: pointer"
                >
                  <i class="fab fa-github text-gray-400 mr-1"></i> github
                </li>
              </ul>
              <div>
                <h2
                  class="text-xl text-[#2390B3] font-bold border-l-4 border-[#2390B3] pl-2 mb-2"
                >
                  이력서 티엠아이
                </h2>
                <ul class="space-y-2 mb-10">
                  <li>
                    <i class="fas fa-envelope text-gray-400 mr-1"></i>군생활을
                    7년3개월했다
                  </li>
                  <li>
                    <i class="fas fa-envelope text-gray-400 mr-1"></i>일본에서
                    5년살았다.
                  </li>
                  <li>
                    <i class="fas fa-envelope text-gray-400 mr-1"></i>MBTI가
                    ENTJ이다.
                  </li>
                </ul>
              </div>
              <div>
                <h2
                  class="text-xl text-[#2390B3] font-bold border-l-4 border-[#2390B3] pl-2 mb-2"
                >
                  관심사 티엠아이
                </h2>
                <ul class="space-y-2 mb-10">
                  <li>
                    <i class="fas fa-envelope text-gray-400 mr-1"></i>한적함과
                    여유로움을 좋아한다.
                  </li>
                  <li>
                    <i class="fas fa-envelope text-gray-400 mr-1"></i>프로야구
                    기아타이거즈를 응원한다.
                  </li>
                  <li>
                    <i class="fas fa-envelope text-gray-400 mr-1"></i
                    >부동산이라기에는 거창하고 주거에 관심이많다.
                  </li>
                  <li>
                    <i class="fas fa-envelope text-gray-400 mr-1"></i
                    >밤에 먹는 술보다 낮에 먹는 술을 좋아한다.
                  </li>
                </ul>
              </div>
            </div>

            <div class="flex flex-col gap-0">
              <div>
                <h2
                  class="text-xl text-[#2390B3] font-bold border-l-4 border-[#2390B3] pl-2 mb-2"
                >
                  소개
                </h2>
                <GChart
                  type="Timeline"
                  :settings="{ packages: ['timeline'] }"
                  :data="timelineData"
                  class="responsive-chart"
                />
              </div>
              <div class="space-y-2">
                <h2
                  class="text-xl text-[#2390B3] font-bold border-l-4 border-[#2390B3] pl-2 mb-2"
                >
                  IT 경력(총 : {{ yy }}년 {{ mm }}개월)
                </h2>
                <div class="pl-4">
                  <div class="text-xl inline-block">솔트룩스</div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2023.07 ~ 재직중</span
                  >
                  <p>
                    서울 강남구 위치한 인공지능, 빅데이터 전문 회사로 자사
                    LLM을 활용한 LLM 도입 프로젝트에 대한 고객사 수행 업무를 담당
                  </p>
                </div>
                <div class="pl-4">
                  <div class="text-xl inline-block">솔루션링크</div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2022.07 ~ 2023.07</span
                  >
                  <p>
                    서울 서초구 위치한 PMS(Project Management System) 솔루션을
                    개발&구축 하는 회사로 연구개발 & 고객사 수행을 담당
                  </p>
                </div>
                <div class="pl-4">
                  <div class="text-xl inline-block">그레이스케일</div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2022.05 ~ 2022.06</span
                  >
                  <p>
                    경기도 부천에 위치한 시니어 쇼핑 플랫폼을 운영 하는
                    스타트업으로 EC사이트 개발 및 유지보수를 담당
                  </p>
                </div>
                <div class="pl-4">
                  <div class="text-xl inline-block">Witsystems</div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2020.09 ~ 2022.04</span
                  >
                  <p>
                    일본 후쿠오카에 위치한 Iot전문 기업으로 진동에 의한
                    모터,펌프 고장예지 솔루션과 정수장 및 공장의 스마트솔루션,
                    리눅스기반 엣지컴퓨터의 Ai플랫폼을 개발
                  </p>
                </div>

                <div class="pl-4">
                  <div class="text-xl inline-block">Swingbytechnology</div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2018.07 ~ 2020.08</span
                  >
                  <p>
                    일본 도쿄에 위치한 SI프로젝트 수행 및 협력을 담당한 회사로
                    웹개발의 설계,구현을 주로 담당.
                  </p>
                </div>
              </div>
              <div class="my-6"></div>
              <div class="space-y-2">
                <h2
                  class="text-xl text-[#2390B3] font-bold border-l-4 border-[#2390B3] pl-2 mb-2"
                >
                  기타 경력(총 : 07년 04개월)
                </h2>

                <div class="pl-4">
                  <div class="text-xl inline-block">대한민국 육군</div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2008.11 ~ 2016.02</span
                  >
                  <p>
                    포병대대에서 K-9자주포 운용 업무와 군수지원업무를 담당하였고
                    중사로 전역
                  </p>
                </div>
              </div>
              <div class="my-6"></div>
              <div class="space-y-2">
                <h2
                  class="text-xl text-[#2390B3] font-bold border-l-4 border-[#2390B3] pl-2 mb-2"
                >
                  프로젝트 경력
                </h2>
                <div class="pl-4">
                  <div class="text-xl inline-block">
                    한국수력원자력 형상관리 도입 PoC
                  </div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2023.11 ~ 2024.04 / 서울 / PL</span
                  >
                  <p>
                    &nbsp;&nbsp;&nbsp;스킬 : JAVA, SPRINGBOOT, PYTHON, LLAMA2, VUE 
                  </p>
                  <p>
                    &nbsp;&nbsp;&nbsp;내용 : 한국수력원자력 문서에 대한 맞춤형 형상관리 4개 과제에 대한 수행
                  </p>
                </div>
                <div class="pl-4">
                  <div class="text-xl inline-block">
                    행정안전부 LLM도입 PoC
                  </div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2023.08 ~ 2023.10 / 서울 / 멤버</span
                  >
                  <p>
                    &nbsp;&nbsp;&nbsp;스킬 : PYTHON, VUE, LINUX
                  </p>
                  <p>
                    &nbsp;&nbsp;&nbsp;내용 : 자사 LLM 모델을 활용하여 문서업로드, 문서 Q&A 기능 구현
                  </p>
                </div>
                <div class="pl-4">
                  <div class="text-xl inline-block">
                    신세계아이앤씨 PMS 구축
                  </div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2023.03 ~ 2023.07 / 서울 / PL</span
                  >
                  <p>
                    &nbsp;&nbsp;&nbsp;스킬 : JAVA, JAVASCRIPT, ORACLE, JQUERY,
                    SPRING, LINUX
                  </p>
                  <p>
                    &nbsp;&nbsp;&nbsp;내용 : PMS 커스터마이징 및 도입 지원 및
                    컨설팅
                  </p>
                </div>
                <div class="pl-4">
                  <div class="text-xl inline-block">
                    ITSCOPE 애자일 방법론 추가
                  </div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2022.12 ~ 2023.02 / 서울 / PM</span
                  >
                  <p>
                    &nbsp;&nbsp;&nbsp;스킬 : JAVA, JAVASCRIPT, ORACLE, JQUERY,
                    SPRING, LINUX
                  </p>
                  <p>
                    &nbsp;&nbsp;&nbsp;내용 : 자사 솔루션의 프로젝트 방법론 추가
                  </p>
                </div>
                <div class="pl-4">
                  <div class="text-xl inline-block">NH PMS 안정화 지원</div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2022.07 ~ 2022.11 / 경기도 의왕 / 멤버</span
                  >
                  <p>
                    &nbsp;&nbsp;&nbsp;스킬 : JAVA, JAVASCRIPT, ORACLE, JQUERY,
                    SPRING, LINUX
                  </p>
                  <p>&nbsp;&nbsp;&nbsp;내용 : PMS 도입 후 안정화 지원</p>
                </div>
                <div class="pl-4">
                  <div class="text-xl inline-block">EC사이트 유지보수</div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2022.05 ~ 2022.06 / 서울 / 멤버</span
                  >
                  <p>
                    &nbsp;&nbsp;&nbsp;스킬 : JAVA, MARIADB, JQUERY, SPRINGBOOT,
                    LINUX, VUE
                  </p>
                  <p>
                    &nbsp;&nbsp;&nbsp;내용 : 음료 관련 대기업의 경리, 물류
                    시스템을 구축
                  </p>
                </div>
                <div class="pl-4">
                  <div class="text-xl inline-block">
                    EDGE PLATFORM의 시스템 UI 개발
                  </div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2020.10 ~ 2022.04 / 후쿠오카 / PL</span
                  >
                  <p>
                    &nbsp;&nbsp;&nbsp;스킬 : python, Flask, mariaDB, jquery,
                    shell script, linux(yockto), apache
                  </p>
                  <p>
                    &nbsp;&nbsp;&nbsp;내용 : EDGE PC(BLACKBEAR)의 리눅스 간편
                    세팅 과 iot플랫폼 설정 웹 시스템을 개발
                  </p>
                </div>
                <div class="pl-4">
                  <div class="text-xl inline-block">
                    데이터레이크 , 스마트팩토리
                  </div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2020.10 ~ 2022.04 / 후쿠오카 / PL</span
                  >
                  <p>
                    &nbsp;&nbsp;&nbsp;스킬 : python, Flask, mariaDB, aws, vuejs,
                    Ble, numpy, 단순 선형회귀 모델, svm모델
                  </p>
                  <p>
                    &nbsp;&nbsp;&nbsp;내용 : Iot플랫폼 클라우딩 서비스(Ai
                    이상감지 판단 서비스), 스마트팩토리
                  </p>
                </div>
                <div class="pl-4">
                  <div class="text-xl inline-block">&mall 프로젝트</div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2020.01 ~ 2020.08 / 도쿄 / 팀서브리더</span
                  >
                  <p>
                    &nbsp;&nbsp;&nbsp;스킬 : JAVA, JAVASCRIPT, MYSQL, JQUERY,
                    SPRING, LINUX, SVN
                  </p>
                  <p>
                    &nbsp;&nbsp;&nbsp;내용 : EC사이트 SM 프로젝트로 기능 추가 및
                    유지보수를 담당
                  </p>
                </div>
                <div class="pl-4">
                  <div class="text-xl inline-block">기린 MDM 프로젝트</div>
                  <span class="text-sm text-gray-500 ml-2"
                    >2018.07 ~ 2019.12 / 도쿄 / 멤버</span
                  >
                  <p>
                    &nbsp;&nbsp;&nbsp;스킬 : JAVA, JAVASCRIPT, ORACLE, JQUERY,
                    SPRING, LINUX, SVN
                  </p>
                  <p>
                    &nbsp;&nbsp;&nbsp;내용 : 음료 관련 대기업의 경리, 물류
                    시스템을 구축
                  </p>
                </div>
              </div>
              <div>
                <h2
                  class="text-xl text-[#2390B3] font-bold border-l-4 border-[#2390B3] pl-2 mb-2"
                >
                  Skill
                </h2>
                <ul class="grid grid-cols-3 pl-4 list-disc">
                  <li>JAVA</li>
                  <li>PYTHON</li>
                  <li>JAVASCRIPT</li>
                  <li>VUE</li>
                  <li>LINUX</li>
                  <li>AWS S3</li>
                  <li>BLE</li>
                  <li>AWS EC2</li>
                  <li>SQL</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </body>
</template>

<script>
import { GChart } from "vue-google-charts";
export default {
  components: {
    GChart,
  },
  setup() {
  let yy = 0;
  let mm = 0;

  // 현재 날짜를 가져오는 함수
  const currentDate = new Date();

  // 시작일을 2018년 8월 1일로 변경
  const fromDate = new Date(2018, 7, 1); // 8월은 7로 표시

  // 현재 날짜를 기준으로 년, 월 수 계산
  let years = currentDate.getFullYear() - fromDate.getFullYear();
  let months = currentDate.getMonth() - fromDate.getMonth();
  
  // 월이 음수일 경우 연도를 조정
  if (months < 0) {
    years--;
    months += 12;
  }
  
  // 계산된 년, 월 수를 변수에 할당
  yy = years;
  mm = months;

  const openNewTab = function (url) {
    window.open(url, "_blank");
  };

  return {
    yy,
    mm,
    openNewTab,
    GChart,
    timelineData: [
      ["name", "start", "end"],
      ["군복무", new Date(2008, 11, 10), new Date(2016, 2, 26)],
      ["재취직준비", new Date(2016, 3, 1), new Date(2017, 11, 30)],
      [
        "일본에서 개발자로 생활",
        new Date(2017, 12, 1),
        new Date(2022, 4, 15),
      ],
      [
        "한국에서 개발자로 생활",
        new Date(2022, 5, 1),
        currentDate, // 현재 날짜로 변경
      ],
    ],
    timelineOptions: {
      timeline: {
        rowLabelStyle: "none",
        barLabelStyle: "none",
        start: new Date(2005, 0, 1),
        end: new Date(2030, 11, 31),
      },
      colors: ["#E74C3C", "#2C3E50", "#2980B9"],
      tooltip: { textStyle: { fontName: "Ariel", fontSize: 14 } },
    },
  };
}
};
</script>
<style>
/* 스타일 기본값 (브라우저 화면) */
.responsive-chart {
  height: 28vh;
}

/* 모바일 화면에 대한 미디어 쿼리 */
@media (max-width: 768px) {
  .responsive-chart {
    height: 51vh;
  }
}
</style>
