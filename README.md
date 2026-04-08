# 🎨 jy-awesome-ui 

( React / TypeScript / styled-components ) | Apple-style React UI Component Library

Apple 디자인 시스템에서 영감을 받은 React UI 컴포넌트 라이브러리입니다.  
다크모드를 기본 지원하며, `styled-components` 기반으로 구현되어 있어 별도의 CSS 빌드 설정 없이 사용할 수 있습니다.

[![npm version](https://img.shields.io/npm/v/jy-awesome-ui)](https://www.npmjs.com/package/jy-awesome-ui)
[![license](https://img.shields.io/npm/l/jy-awesome-ui)](./LICENSE)

---

## 특징

- Apple HIG 스타일 — 둥근 모서리, glassmorphism, 부드러운 트랜지션
- 다크모드 — 모든 컴포넌트에 `isDark` prop으로 개별 제어
- TypeScript — 완전한 타입 지원
- Tree-shakable — 사용한 컴포넌트만 번들에 포함
- `"use client"` 배너 포함 — Next.js App Router 대응

---

## 설치

```bash
npm install jy-awesome-ui
```

### 피어 의존성 설치

```bash
npm install react react-dom styled-components lucide-react
```

---

## 사용법

### CSS 임포트 (전역 스타일, 한 번만)

```tsx
import 'jy-awesome-ui/styles.css';
```

### 컴포넌트 사용

```tsx
import { Button, Card, Badge } from 'jy-awesome-ui';

export default function App() {
  return (
    <Card isDark={false}>
      <Badge variant="primary">New</Badge>
      <Button variant="default" size="md" isDark={false}>
        시작하기
      </Button>
    </Card>
  );
}
```

### styled-components 기반 확장 컴포넌트 (선택)

```tsx
import { BreadcrumbStyled, PaginationStyled, SidebarStyled } from 'jy-awesome-ui/styled';
```

---

## 컴포넌트 목록

### 레이아웃 & 네비게이션
| 컴포넌트 | 설명 |
|----------|------|
| `Navbar` | 상단 내비게이션 바 (sticky, transparent 지원) |
| `Sidebar` / `SidebarStyled` | 사이드바 레이아웃 |
| `BottomNavigation` | 모바일 하단 탭 바 |
| `Layout` | 페이지 레이아웃 래퍼 |
| `Breadcrumb` / `BreadcrumbStyled` | 브레드크럼 |
| `NavigationMenu` | 드롭다운 포함 내비게이션 메뉴 |

### 데이터 표시
| 컴포넌트 | 설명 |
|----------|------|
| `StatCard` | 지표 카드 (수치 + 증감률 표시) |
| `StatusIndicator` | 상태 표시 인디케이터 |
| `Table` | 기본 테이블 |
| `Chart` | 차트 래퍼 |
| `Carousel` | 이미지/콘텐츠 캐러셀 |
| `Timeline` | 타임라인 목록 |

### 입력 & 폼
| 컴포넌트 | 설명 |
|----------|------|
| `Button` | 버튼 (default, outline, ghost, destructive / sm, md, lg) |
| `Input` | 텍스트 입력 |
| `Textarea` | 멀티라인 입력 |
| `Select` | 드롭다운 선택 |
| `Checkbox` | 체크박스 |
| `RadioGroup` | 라디오 그룹 |
| `Switch` | 토글 스위치 |
| `Slider` | 슬라이더 |
| `InputOtp` | OTP 입력 |
| `Form` | React Hook Form 연동 폼 |
| `Calendar` | 날짜 선택 달력 |

### 피드백 & 오버레이
| 컴포넌트 | 설명 |
|----------|------|
| `Banner` | 인라인 알림 배너 (info, success, warning, error) |
| `Alert` | 알림 메시지 |
| `AlertDialog` | 확인 다이얼로그 |
| `Dialog` | 모달 다이얼로그 |
| `Drawer` | 하단 슬라이드 드로어 |
| `Sheet` | 사이드 슬라이드 패널 |
| `Sonner` | 토스트 알림 |
| `Toast` | 토스트 메시지 |
| `Tooltip` | 툴팁 |
| `Progress` | 프로그레스 바 |
| `Loading` | 로딩 인디케이터 |
| `Skeleton` | 스켈레톤 UI |
| `EmptyState` | 빈 상태 안내 |

### 구조 & 기타
| 컴포넌트 | 설명 |
|----------|------|
| `Stepper` | 단계 진행 표시 |
| `Tabs` | 탭 패널 |
| `Accordion` | 아코디언 |
| `Collapsible` | 접기/펼치기 |
| `Card` | 카드 컨테이너 |
| `Badge` | 뱃지 |
| `Chip` | 칩/태그 (삭제 가능) |
| `Avatar` | 사용자 아바타 |
| `Divider` | 구분선 |
| `Popover` | 팝오버 |
| `HoverCard` | 호버 카드 |
| `Command` | 커맨드 팔레트 |
| `DropdownMenu` | 드롭다운 메뉴 |
| `ContextMenu` | 우클릭 컨텍스트 메뉴 |
| `Menubar` | 메뉴바 |
| `ScrollArea` | 커스텀 스크롤 영역 |
| `Resizable` | 리사이즈 가능한 패널 |
| `Pagination` / `PaginationStyled` | 페이지네이션 |
| `Toggle` / `ToggleGroup` | 토글 버튼 |

---

## 다크모드

모든 컴포넌트는 `isDark` prop으로 독립적으로 다크모드를 적용합니다.

```tsx
const isDark = window.matchMedia('(prefers-color-scheme: dark)').matches;

<Button isDark={isDark} variant="default">
  버튼
</Button>
```

---

## 빌드

```bash
# 빌드
npm run build

# 개발 (watch 모드)
npm run dev
```

빌드 결과물은 `dist/` 에 생성됩니다.

---

## 라이선스

MIT
