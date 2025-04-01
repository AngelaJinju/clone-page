// 🍏 Apple 제품 클론 프로젝트: Figma 프레임 세팅 템플릿
// ⚙️ 목적: iPhone 15 Pro, Vision Pro, MacBook 클론 디자인을 위한 프레임 구성 및 공통 컴포넌트 세팅

// ✅ 1. Figma 프레임 구성 기준 (Desktop 기준)
const FRAME_WIDTH = 1440;
const GRID_COLUMNS = 12;
const GRID_MARGIN = 80;
const GRID_GUTTER = 24;

export const FigmaFrameTemplate = {
  name: "Apple Clone Project",
  size: {
    width: FRAME_WIDTH,
    height: 4000, // 섹션별 유동적으로 조정
  },
  grid: {
    type: "grid",
    columns: GRID_COLUMNS,
    gutter: GRID_GUTTER,
    margin: GRID_MARGIN,
  },
  spacing: {
    sectionPadding: 160,
    sectionGap: 80,
  },
  typography: {
    h1: {
      font: "SF Pro Display / Inter",
      weight: 600,
      size: 64,
      lineHeight: 1.2,
    },
    h2: {
      size: 48,
      weight: 500,
    },
    body: {
      size: 18,
      lineHeight: 1.6,
    },
  },
};

// ✅ 2. 공통 컴포넌트 정의
export const Components = {
  Button: {
    type: "primary",
    padding: "16px 32px",
    borderRadius: 100,
    font: "16px bold",
    variants: ["default", "hover", "disabled"],
  },
  TitleBlock: {
    layout: "vertical",
    align: "center",
    spacing: 16,
    elements: ["Eyebrow (optional)", "H1", "Paragraph"],
  },
  ProductCard: {
    size: "Responsive",
    imageRatio: "16:9",
    hoverEffect: true,
    content: ["Image", "Title", "Text"],
  },
};

// ✅ 3. Webflow 기본 구조 설계 예시 (HTML/CSS 구조 참고용)
export const WebflowStructure = [
  {
    tag: "section",
    class: "hero-section",
    children: [
      {
        tag: "div",
        class: "container",
        children: [
          { tag: "h1", class: "hero-title" },
          { tag: "p", class: "hero-subtitle" },
          { tag: "button", class: "cta-button" },
        ],
      },
    ],
  },
  {
    tag: "section",
    class: "feature-section",
    children: [
      {
        tag: "div",
        class: "container grid-2-cols",
        children: [
          { tag: "img", class: "feature-image" },
          { tag: "div", class: "feature-text" },
        ],
      },
    ],
  },
  {
    tag: "footer",
    class: "site-footer",
    children: [
      { tag: "div", class: "footer-logo" },
      { tag: "ul", class: "footer-links" },
    ],
  },
];
