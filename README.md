<h1 align="center">Senior Front‑end Engineer — ship delightful, blazing‑fast web experiences</h1>

<p align="center">
  <a href="https://readme-typing-svg.demolab.com?font=Inter&weight=600&size=22&duration=2500&pause=800&color=00DC82&center=true&vCenter=true&width=900&lines=Senior+Front-end+Engineer;Performance+%26+Core+Web+Vitals+%E2%9A%A1%EF%B8%8F;UX%2FA11y-first+mindset;Design+System+%26+Micro-frontend;TypeScript+everywhere;Testing+%26+CI%2FCD+at+scale">
    <img src="https://readme-typing-svg.demolab.com?font=Inter&weight=600&size=22&duration=2500&pause=800&color=00DC82&center=true&vCenter=true&width=900&lines=Senior+Front-end+Engineer;Performance+%26+Core+Web+Vitals+%E2%9A%A1%EF%B8%8F;UX%2FA11y-first+mindset;Design+System+%26+Micro-frontend;TypeScript+everywhere;Testing+%26+CI%2FCD+at+scale" alt="typing intro">
  </a>
</p>

<p align="center">
  <a href="https://maxpamlevi.github.io">Website/Portfolio</a> •
  <a href="https://github.com/maxpamlevi">GitHub</a>
  <!-- Thêm LinkedIn/Twitter/email của bạn tại đây -->
</p>

---

Xin chào! Mình là một Senior Front‑end tập trung vào:
- Hiệu năng thực chiến: tối ưu Core Web Vitals (LCP/CLS/INP), performance budget, code‑splitting, prefetch/prerender.
- Kiến trúc và scale: monorepo (pnpm + Turbo/Nx), micro‑frontend, module federation, design system bền vững.
- Trải nghiệm người dùng: a11y theo WCAG, motion an toàn (prefers‑reduced‑motion), i18n, dark mode.
- Chất lượng và tự động hóa: TypeScript, ESLint/Prettier, Storybook, Jest/RTL, Cypress/Playwright, GitHub Actions.

Mục tiêu: Ship sản phẩm pixel‑perfect, nhanh, đo đếm được, dễ bảo trì — và mang lại niềm vui cho cả người dùng lẫn dev.

---

Tech radar nhanh
- Frameworks: React, Next.js, Vue/Nuxt, SvelteKit
- Ngôn ngữ: TypeScript, Modern CSS (Tailwind, CSS Modules, CSS‑in‑JS)
- Tooling: Vite, Webpack, Turbopack, SWC/ESBuild, pnpm
- State/Data: Redux/Zustand, TanStack Query, GraphQL (Apollo/urql), REST
- UI/Design System: Storybook, Radix UI, Headless UI
- Testing: Jest, React Testing Library, Vitest, Cypress, Playwright
- Observability: Sentry, LogRocket, Web Vitals, Lighthouse CI

<p align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="react" height="36"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg" alt="nextjs" height="36"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg" alt="vue" height="36"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" alt="ts" height="36"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vitejs/vitejs-original.svg" alt="vite" height="36"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-plain.svg" alt="tailwind" height="36"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/storybook/storybook-original.svg" alt="storybook" height="36"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jest/jest-plain.svg" alt="jest" height="36"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cypressio/cypressio-original.svg" alt="cypress" height="36"/>
</p>

---

Dự án tiêu biểu
- Portfolio/Playground: https://maxpamlevi.github.io
- <!-- Thêm 2–3 dự án nổi bật (sản xuất/mã nguồn) cùng số liệu: +X% LCP, −Y% bundle, +Z% CVR -->

Triết lý sản phẩm
- Đo lường > cảm tính: luôn gắn Web Vitals, RUM và A/B khi tối ưu.
- Tối ưu theo dòng chảy người dùng: ưu tiên TTI/INP và critical path trước “điểm số”.
- DX tốt → sản phẩm tốt: tạo scaffolding, lint rules, CI, preview để dev tập trung vào giá trị.

---

GitHub Insights
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=maxpamlevi&show_icons=true&include_all_commits=true&rank_icon=github&theme=transparent&hide_border=true" alt="stats" />
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com?user=maxpamlevi&theme=transparent&hide_border=true" alt="streak" />
</p>
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=maxpamlevi&layout=compact&langs_count=10&card_width=445&hide_border=true&theme=transparent" alt="top languages" />
</p>
<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=maxpamlevi&no-frame=true&no-bg=true&row=1&column=7" alt="trophies" />
</p>
<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=maxpamlevi&radius=12&theme=github-compact&area=true&hide_border=true" alt="activity graph" />
</p>

---

Snippet ưa thích (TypeScript + React): useSmartImage — ưu tiên UX, hiệu năng và a11y
- Tự động lazy‑load, placeholder mờ, preconnect CDN, tôn trọng prefers‑reduced‑motion.
- Giảm layout shift với intrinsic ratio và decoding async.

```tsx
import React, { useEffect, useMemo } from "react";

type SmartImageProps = {
  src: string;
  alt: string;
  width: number;
  height: number;
  priority?: boolean;
  className?: string;
  sizes?: string;
  fetchPriority?: "high" | "low" | "auto";
};

const cdn = (url: string, w: number) =>
  `${url}${url.includes("?") ? "&" : "?"}w=${w}&auto=format&fit=max`;

export function SmartImage({
  src,
  alt,
  width,
  height,
  priority,
  className,
  sizes = "(min-width: 768px) 50vw, 100vw",
  fetchPriority = priority ? "high" : "auto",
}: SmartImageProps) {
  const ratio = `${(height / width) * 100}%`;
  const srcSet = useMemo(
    () =>
      [320, 640, 960, 1200, 1600]
        .map((w) => `${cdn(src, w)} ${w}w`)
        .join(", "),
    [src]
  );

  useEffect(() => {
    if (!priority) return;
    // Preconnect nhẹ nhàng đến CDN để tối ưu handshake
    try {
      const u = new URL(src);
      const link = document.createElement("link");
      link.rel = "preconnect";
      link.href = `${u.protocol}//${u.host}`;
      document.head.appendChild(link);
      return () => document.head.removeChild(link);
    } catch {}
  }, [src, priority]);

  return (
    <figure style={{ display: "block" }}>
      <div
        style={{
          position: "relative",
          width: "100%",
          paddingTop: ratio, // intrinsic ratio tránh CLS
          overflow: "hidden",
          borderRadius: 12,
          background:
            "linear-gradient(90deg,#f3f3f3 25%,#ecebeb 37%,#f3f3f3 63%)",
          animation:
            window.matchMedia?.("(prefers-reduced-motion: reduce)").matches
              ? "none"
              : "loadingShimmer 1.2s infinite",
        }}
      >
        <img
          loading={priority ? "eager" : "lazy"}
          decoding="async"
          src={cdn(src, 960)}
          srcSet={srcSet}
          sizes={sizes}
          width={width}
          height={height}
          alt={alt}
          fetchPriority={fetchPriority}
          style={{
            position: "absolute",
            inset: 0,
            width: "100%",
            height: "100%",
            objectFit: "cover",
          }}
          className={className}
        />
      </div>
      <figcaption style={{ fontSize: 12, color: "#6b7280", marginTop: 8 }}>
        {alt}
      </figcaption>
    </figure>
  );
}
```

Ghi chú triển khai
- README này sẽ hiển thị khi bạn tạo repo trùng tên tài khoản: github.com/maxpamlevi/maxpamlevi
- Một số widget có thể bị rate‑limit. Nếu cần:
  - Triển khai self‑host (Vercel) cho github‑readme‑stats hoặc thay theme=transparent bằng chủ đề khác.
  - Tắt/bật vài card để nhẹ hơn.
- Thêm liên hệ cá nhân (email/LinkedIn) vào phần trên cùng.
- Thêm số liệu thực chiến cho dự án tiêu biểu (LCP/INP, giảm bundle, tăng CR).

<p align="right">
  <img src="https://komarev.com/ghpvc/?username=maxpamlevi&label=Profile%20views&color=0e75b6&style=flat" alt="views" />
</p>
