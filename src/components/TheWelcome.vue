<script setup lang="ts">
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'

// SUGGESTION: Create a new icon file at src/components/icons/IconNewFeature.vue
// with an SVG and import it here to avoid reusing DocumentationIcon.
// Example:
//   import NewFeatureIcon from './icons/IconNewFeature.vue'
//
// Minimal icon component template:
// <template>
//   <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" viewBox="0 0 24 24">
//     <!-- paste SVG path(s) here -->
//   </svg>
// </template>

const openReadmeInEditor = () => fetch('/__open-in-editor?file=README.md')
</script>

<template>
  <!-- Documentation item: links to the official Vue.js docs -->
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Documentation</template>

    Vue's
    <a href="https://vuejs.org/" target="_blank" rel="noopener">official documentation</a>
    provides you with all information you need to get started.
  </WelcomeItem>

  <!-- Tooling item: highlights Vite, VSCode, Vitest, Cypress, Playwright -->
  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Tooling</template>

    This project is served and bundled with
    <a href="https://vite.dev/guide/features.html" target="_blank" rel="noopener">Vite</a>. The
    recommended IDE setup is
    <a href="https://code.visualstudio.com/" target="_blank" rel="noopener">VSCode</a>
    +
    <a href="https://github.com/vuejs/language-tools" target="_blank" rel="noopener"
      >Vue - Official</a
    >. If you need to test your components and web pages, check out
    <a href="https://vitest.dev/" target="_blank" rel="noopener">Vitest</a>
    and
    <a href="https://www.cypress.io/" target="_blank" rel="noopener">Cypress</a>
    /
    <a href="https://playwright.dev/" target="_blank" rel="noopener">Playwright</a>.

    <br />

    More instructions are available in
    <a href="javascript:void(0)" @click="openReadmeInEditor"><code>README.md</code></a
    >.
  </WelcomeItem>

  <!-- Ecosystem item: showcases Pinia, Vue Router, Vue Test Utils, Vue Dev Tools -->
  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Ecosystem</template>

    Get official tools and libraries for your project:
    <a href="https://pinia.vuejs.org/" target="_blank" rel="noopener">Pinia</a>,
    <a href="https://router.vuejs.org/" target="_blank" rel="noopener">Vue Router</a>,
    <a href="https://test-utils.vuejs.org/" target="_blank" rel="noopener">Vue Test Utils</a>, and
    <a href="https://github.com/vuejs/devtools" target="_blank" rel="noopener">Vue Dev Tools</a>. If
    you need more resources, we suggest paying
    <a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">Awesome Vue</a>
    a visit.
  </WelcomeItem>

  <!-- Community item: links to Vue Land Discord, StackOverflow, and social accounts -->
  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Community</template>

    Got stuck? Ask your question on
    <a href="https://chat.vuejs.org" target="_blank" rel="noopener">Vue Land</a>
    (our official Discord server), or
    <a href="https://stackoverflow.com/questions/tagged/vue.js" target="_blank" rel="noopener"
      >StackOverflow</a
    >. You should also follow the official
    <a href="https://bsky.app/profile/vuejs.org" target="_blank" rel="noopener">@vuejs.org</a>
    Bluesky account or the
    <a href="https://x.com/vuejs" target="_blank" rel="noopener">@vuejs</a>
    X account for latest news in the Vue world.
  </WelcomeItem>

  <!-- Support item: encourages users to sponsor the Vue.js project -->
  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Support Vue</template>

    As an independent project, Vue relies on community backing for its sustainability. You can help
    us by
    <a href="https://vuejs.org/sponsor/" target="_blank" rel="noopener">becoming a sponsor</a>.
  </WelcomeItem>

  <!--
    ============================================================
    REVIEW: New WelcomeItem — requires changes before merging
    ============================================================

    ISSUE 1 — DUPLICATE ICON (src/components/TheWelcome.vue:118)
    DocumentationIcon is already used by the first WelcomeItem (line 19).
    Each item should have its own distinct icon.

    Fix: Create src/components/icons/IconNewFeature.vue, import it at the top
    of <script setup>, then replace <DocumentationIcon /> below with <NewFeatureIcon />.

    ISSUE 2 — PLACEHOLDER HEADING (line 122)
    The heading "Test" is not meaningful.
    Replace with a descriptive title, e.g. "Getting Started" or "Contributing".

    ISSUE 3 — PLACEHOLDER BODY (line 125)
    The body text "Test" is not meaningful.
    Replace with a real description and, ideally, a relevant link. Example:

      Learn how to contribute to this project by reading the
      <a href="https://github.com/your-org/your-repo/blob/main/CONTRIBUTING.md" target="_blank" rel="noopener">Contributing Guide</a>.

    ISSUE 4 — NO PR DESCRIPTION
    This PR has no description. Add one explaining what this new item represents.

    SUGGESTED FINAL RESULT:
    ──────────────────────────────────────────────────────────────
    <WelcomeItem>
      <template #icon>
        <NewFeatureIcon />
      </template>
      <template #heading>Your Feature Name</template>

      A clear description of what this item is about.
      <a href="https://example.com" target="_blank" rel="noopener">Learn more</a>.
    </WelcomeItem>
    ──────────────────────────────────────────────────────────────
  -->
  <WelcomeItem>
    <template #icon>
      <!-- FIXME (Issue 1): DocumentationIcon is already used in the first WelcomeItem (line 19).
           Create a new icon component at src/components/icons/IconNewFeature.vue,
           import it above, and replace this with <NewFeatureIcon />. -->
      <DocumentationIcon />
    </template>
    <!-- FIXME (Issue 2): Replace "Test" with a meaningful heading, e.g. "Getting Started" -->
    <template #heading>Test</template>

    <!-- FIXME (Issue 3): Replace this placeholder with a real description and relevant links -->
    Test
  </WelcomeItem>
  <div class="item">
    <i>
      <DocumentationIcon />
    </i>
    <div class="details">
      <h3>
        Ola
      </h3>
    </div>
  </div>
</template>
<style scoped>
.item {
  margin-top: 2rem;
  display: flex;
  position: relative;
}

.details {
  flex: 1;
  margin-left: 1rem;
}
</style>
