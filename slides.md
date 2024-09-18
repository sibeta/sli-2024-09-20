---
# You can also start simply with 'default'
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# some information about your slides (markdown enabled)
title: Innovation Journey
info: |
  Personal 1-1 meeting presentation on AI, Cloud, and innovative work.
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
---


<div style="display: flex; align-items: center; justify-content: center;">
  <img src="./images/home.png" alt="Home Avatar" style="width: 50px; height: 50px; border-radius: 50%; margin-right: 10px;">
  1 - 1 with 
  <img src="./images/coca-cola.jpg" alt="Avatar" style="width: 50px; height: 50px; border-radius: 50%; margin-left: 10px;">
</div>

<div class="grid grid-cols-3 gap-4 mt-10">
  <div v-for="(topic, index) in topics" :key="topic.name" 
       class="relative h-64 cursor-pointer group perspective">
    <div class="absolute inset-0 transition-all duration-500 preserve-3d group-hover:[transform:rotateY(180deg)]">
      <div class="absolute inset-0 backface-hidden">
        <img src="./images/coca-cola.jpg" alt="Cover" class="w-full h-full object-cover rounded-lg shadow-lg">
      </div>
      <div class="absolute inset-0 backface-hidden [transform:rotateY(180deg)] bg-gray-100 rounded-lg shadow-lg 
                  flex items-center justify-center text-2xl font-bold text-gray-800">
        <span @click="navigateTo(topic.slideIndex)" class="cursor-pointer">{{ topic.name }}</span>
      </div>
    </div>
  </div>
</div>

<script setup>
const topics = [
  { name: "AI Coding", slideIndex: 2 },
  { name: "Laaa's Evil Idea", slideIndex: 5 },
  { name: "New Way Delivery", slideIndex: 6 }
];

const navigateTo = (slideIndex) => {
  $slidev.nav.go(slideIndex);
};
</script>

<style>
.perspective { perspective: 1000px; }
.backface-hidden { backface-visibility: hidden; }
.preserve-3d { transform-style: preserve-3d; }
</style>


---

# Why AI Coding?

AI Coding refers to the use of artificial intelligence technologies to assist or automate parts of the software development process.
<br>
- ⚡ **Increased Productivity** - Automates repetitive tasks, speeding up the development process.
- 🛡️ **Improved Code Quality** - Detects bugs, vulnerabilities, and suggests cleaner code.
- 🚀 **Faster Learning Curve** - Assists beginners with code suggestions and explanations.
- 🐞 **Enhanced Debugging** - Identifies and fixes bugs more efficiently.
- 🧠 **Customization and Optimization** - Provides personalized code suggestions based on your coding style.
- 🔍 **Better Code Review** - Automates code review, ensuring best practices and standards.
- 🔧 **Automated Refactoring** - Automatically improves existing code to be more efficient and readable.
<br>

<div class="fixed bottom-5 right-5 p-2 bg-white rounded-full shadow-md hover:bg-gray-100 transition-colors cursor-pointer" @click="$slidev.nav.go(1)">
  <img src="./images/home.png" alt="Home" class="w-8 h-8">
</div>


---

# AI Coding Tools

- GitHub Copilot
- Tabnine
- Kite
- Cursor
- DeepCode
- Codeium
- Replit
- OpenAI Codex

<br />

<n-space>
  <span class="color-gray" @mouseover="showDrawer()">Go to AI Coding Tools Navigation</span>

  <n-drawer title="AI Coding Tools" :active="show" @close="closeDrawer()">
    <iframe width="1400" height="100%" :src="url" frameborder="0"></iframe>
  </n-drawer>
</n-space>


<script setup>
  import { ref } from 'vue'
  const show = ref(false)
  const url = ref('')

  function showDrawer() {
    show.value = true
    //url.value = 'https://pnpm.io/zh/motivation'
    url.value = 'http://localhost:8080'
  }

  function closeDrawer() {
    show.value = false
  }

</script>

<div class="fixed bottom-5 right-5 p-2 bg-white rounded-full shadow-md hover:bg-gray-100 transition-colors cursor-pointer" @click="$slidev.nav.go(1)">
  <img src="./images/home.png" alt="Home" class="w-8 h-8">
</div>

---

# My AI Coding Experience

- EEE Formula Development --- Coco
- Draw PlantUML Diagram
- Draw Canvas ICON
- Develop Script for Script Runner
- Develop Web Tool
- Write PPT via slidev

<div class="fixed bottom-5 right-5 p-2 bg-white rounded-full shadow-md hover:bg-gray-100 transition-colors cursor-pointer" @click="$slidev.nav.go(1)">
  <img src="./images/home.png" alt="Home" class="w-8 h-8">
</div>

---

# Laaa's Evil Idea

- Cloud technologies you're working with
- Innovative cloud solutions
- Impact on the business

<div class="fixed bottom-5 right-5 p-2 bg-white rounded-full shadow-md hover:bg-gray-100 transition-colors cursor-pointer" @click="$slidev.nav.go(1)">
  <img src="./images/home.png" alt="Home" class="w-8 h-8">
</div>

---

# Amazing Work

- Highlight your most impressive projects
- Key achievements and innovations
- Future goals and aspirations

<div class="fixed bottom-5 right-5 p-2 bg-white rounded-full shadow-md hover:bg-gray-100 transition-colors cursor-pointer" @click="$slidev.nav.go(1)">
  <img src="./images/home.png" alt="Home" class="w-8 h-8">
</div>
---

# Diagrams

You can create diagrams / graphs from textual descriptions, directly in your Markdown.

<div class="grid grid-cols-4 gap-5 pt-4 -mb-6">

```mermaid {scale: 0.5, alt: 'A simple sequence diagram'}
sequenceDiagram
    Alice->John: Hello John, how are you?
    Note over Alice,John: A typical interaction
```

```mermaid {theme: 'neutral', scale: 0.8}
graph TD
B[Text] --> C{Decision}
C -->|One| D[Result 1]
C -->|Two| E[Result 2]
```

```mermaid
mindmap
  root((mindmap))
    Origins
      Long history
      ::icon(fa fa-book)
      Popularisation
        British popular psychology author Tony Buzan
    Research
      On effectiveness<br/>and features
      On Automatic creation
        Uses
            Creative techniques
            Strategic planning
            Argument mapping
    Tools
      Pen and paper
      Mermaid
```

```plantuml {scale: 0.7}
@startuml

package "Some Group" {
  HTTP - [First Component]
  [Another Component]
}

node "Other Groups" {
  FTP - [Second Component]
  [First Component] --> FTP
}

cloud {
  [Example 1]
}

database "MySql" {
  folder "This is my folder" {
    [Folder 3]
  }
  frame "Foo" {
    [Frame 4]
  }
}

[Another Component] --> [Example 1]
[Example 1] --> [Folder 3]
[Folder 3] --> [Frame 4]

@enduml
```

</div>

Learn more: [Mermaid Diagrams](https://sli.dev/features/mermaid) and [PlantUML Diagrams](https://sli.dev/features/plantuml)

---
layout: iframe

# the web page source
url: http://localhost:8080/
---

---

## 抽屉功能

功能：嵌入 iframe 等内容

<br />

<n-space>
  <span class="color-gray" @mouseover="showDrawer()">鼠标悬浮此处打开抽屉</span>

  <n-drawer title="AI Coding Tools" :active="show" @close="closeDrawer()">
    <iframe width="1400" height="100%" :src="url" frameborder="0"></iframe>
  </n-drawer>
</n-space>


<script setup>
  import { ref } from 'vue'
  const show = ref(false)
  const url = ref('')

  function showDrawer() {
    show.value = true
    //url.value = 'https://pnpm.io/zh/motivation'
    url.value = 'http://localhost:8080'
  }

  function closeDrawer() {
    show.value = false
  }

</script>
