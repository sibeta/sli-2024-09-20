---
# You can also start simply with 'default'
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Welcome to Slidev
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
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

# Page 1


<div class="flex justify-center space-x-4">
  <span @click="$slidev.nav.go(3)" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Click here1 to slide 3 <carbon:arrow-right class="inline"/>
  </span>
  <span @click="$slidev.nav.go(4)" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Click here2 to slide 4 <carbon:arrow-right class="inline"/>
  </span>
  <span @click="$slidev.nav.go(5)" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Click here3 to slide 5 <carbon:arrow-right class="inline"/>
  </span>
</div>



This is center layout, click here to slide 3

---
layout: center
---

# Page 2
This is center layout

---
layout: center
---

# Page 3
This is center layout

<div class="flex justify-center mt-4">
  <span @click="$slidev.nav.go(1)" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Back to navigation slide <carbon:arrow-left class="inline"/>
  </span>
</div>



---
layout: center
---

# Page 4
This is center layout

<div class="flex justify-center mt-4">
  <span @click="$slidev.nav.go(1)" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Back to navigation slide <carbon:arrow-left class="inline"/>
  </span>
</div>

---
layout: center
---

# Page 5
This is center layout

<div class="flex justify-center mt-4">
  <span @click="$slidev.nav.go(1)" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Back to navigation slide <carbon:arrow-left class="inline"/>
  </span>
</div>