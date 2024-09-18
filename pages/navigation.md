# 1 - 1 with BBBB

<div class="grid grid-cols-3 gap-4 mt-10">
  <div v-for="(topic, index) in ['AI Coding', 'Laurent\'s Evil Idea', 'New Way Delivery']" :key="topic" 
       class="relative h-64 cursor-pointer group perspective">
    <div class="absolute inset-0 transition-all duration-500 preserve-3d group-hover:[transform:rotateY(180deg)]">
      <div class="absolute inset-0 backface-hidden">
        <img src="./images/coca-cola.jpg" alt="Cover" class="w-full h-full object-cover rounded-lg shadow-lg">
      </div>
      <div class="absolute inset-0 backface-hidden [transform:rotateY(180deg)] bg-gray-100 rounded-lg shadow-lg 
                  flex items-center justify-center text-2xl font-bold text-gray-800">
        <span @click="$slidev.nav.go(index + 2)" class="cursor-pointer">{{ topic }}</span>
      </div>
    </div>
  </div>
</div>

<style>
.perspective { perspective: 1000px; }
.backface-hidden { backface-visibility: hidden; }
.preserve-3d { transform-style: preserve-3d; }
</style>