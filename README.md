# Vue 3 컴포넌트 리팩터링 과제

본 프로젝트는 Vue 3 환경 내에서 Options API 또는 구형 Composition API(`setup()` 함수)로 작성된 `example` 컴포넌트들을 **최신 `<script setup>` 스타일로 통일하는 리팩터링** 과제입니다.

## 동작 확인 스크린샷
![스크린샷 2025-11-04 202953.png](screenshots/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202025-11-04%20202953.png)
![스크린샷 2025-11-04 203003.png](screenshots/%EC%8A%A4%ED%81%AC%EB%A6%B0%EC%83%B7%202025-11-04%20203003.png)
## 변경 요약

`example` 폴더 내의 모든 컴포넌트 파일(`E01` ~ `E12`)을 다음과 같은 원칙으로 리팩터링했습니다.

- **`<script setup>` 도입:** 모든 컴포넌트에 `<script setup>` 구문을 적용하여 코드의 가독성과 간결성을 높였습니다.
- **보일러플레이트 제거:** `export default { ... }`, `setup() { ... }`, `return { ... }` 등의 반복적인 상용구 코드를 모두 제거했습니다.
- **API 함수화:**
    - `data()` → `ref()`, `reactive()`
    - `methods: {}` → `function` 선언
    - `computed: {}` → `computed()`
    - `watch: {}` → `watch()`
    - `mounted()` → `onMounted()`
- **`props` / `emit` / `provide` / `inject` 변환:**
    - `props: []` → `defineProps()` (또는 `setup()` 함수 사용)
    - `emits: []` → `defineEmits()` (또는 `setup()` 함수 사용)
    - `provide: {}` → `provide()`
    - `inject: []` → `inject()`
- **컴포넌트 자동 등록:** `components: {}` 선언 없이 `import`만으로 컴포넌트가 자동 등록되도록 하였습니다.