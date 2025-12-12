# SNUVC 벤처 컨설팅 랜딩 페이지

서울대학교 벤처 컨설팅 팀 SNUVC의 랜딩 페이지입니다. HTML, CSS, JavaScript를 사용하여 구현한 단일 페이지 애플리케이션입니다.

## 기술 스택

- HTML5: 시맨틱 마크업 구조
- CSS3: 인라인 스타일을 활용한 스타일링
- Vanilla JavaScript: 폼 제출 및 인터랙션 처리
- Google Apps Script: 폼 데이터 수집 및 저장

## 주요 기능

반응형 네비게이션
- 고정 헤더 네비게이션 바
- 앵커 링크를 통한 섹션 간 부드러운 스크롤
- 모바일 환경에서 네비게이션 링크 숨김 처리

섹션 구성
- Hero 섹션: 메인 타이틀 및 CTA 버튼
- 소개 섹션: SNUVC의 핵심 가치 제안
- 투자자 네트워크: 한국 및 실리콘밸리 VC 정보
- 팀 소개: 팀원 프로필 카드
- 서비스: 벤처 컨설팅 및 액셀러레이팅 서비스
- 문의 폼: Google Apps Script 연동

문의 폼 제출
- Google Apps Script Web App을 통한 폼 데이터 전송
- 제출 중 버튼 비활성화 및 상태 메시지 표시
- 성공/실패 피드백 제공
- 타임스탬프 자동 추가

스크롤 애니메이션
- Intersection Observer API를 활용한 스크롤 기반 페이드인 효과
- 섹션이 뷰포트에 진입할 때 자동 애니메이션 트리거

## 구현 세부사항

단일 HTML 파일에 모든 스타일을 인라인으로 포함하여 외부 의존성 없이 독립적으로 동작하도록 구현했습니다. CSS Grid의 auto-fit과 minmax를 조합하여 화면 크기에 따라 자동으로 컬럼 수가 조정되는 반응형 레이아웃을 구현했습니다.

부드러운 스크롤링은 querySelectorAll을 사용하여 모든 앵커 링크를 선택하고, scrollIntoView 메서드의 behavior: 'smooth' 옵션을 활용하여 구현했습니다.

폼 제출 처리는 fetch API를 사용하여 Google Apps Script Web App에 POST 요청을 보냅니다. no-cors 모드를 사용하여 CORS 제한을 우회하고, 제출 중에는 버튼을 비활성화하여 중복 제출을 방지합니다.

스크롤 애니메이션은 Intersection Observer API를 사용하여 구현했습니다. 각 섹션을 관찰하고 뷰포트에 진입할 때 fade-in 클래스를 추가하여 CSS 애니메이션을 트리거합니다.

반응형 디자인은 미디어 쿼리를 통해 모바일 환경에서 그리드 레이아웃을 단일 컬럼으로 변경하고, 폰트 크기와 패딩을 조정합니다.

카드 호버 효과는 CSS transition을 활용하여 border-color와 box-shadow가 부드럽게 변화하도록 구현했습니다.

## 프로젝트 구조

```
SNUVC_venture_consulting/
├── index.html
└── images/
    ├── 1.jpg
    ├── 2.jpg
    ├── 3.jpg
    ├── 4.jpg
    ├── 5.jpg
    └── 6.jpg
```

