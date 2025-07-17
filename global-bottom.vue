<script setup>
// Slidevのglobal-bottom.vueでは、$slidevオブジェクトが自動的に利用可能です
// インポートは必要ありません
</script>

<template>
  <footer class="absolute bottom-0 left-0 right-0 p-4 text-sm opacity-75 pointer-events-none">
    <div class="flex justify-between items-center">
      <!-- 左下のコピーライト -->
      <div class="text-left text-gray-400">
        &copy; Yuhei FUJITA
      </div>
      
      <!-- 右下のページ番号 -->
      <div class="text-right text-gray-400">
        {{ $slidev.nav.currentPage }} / {{ $slidev.nav.total }}
      </div>
    </div>
  </footer>
</template>

<style scoped>
footer {
  font-family: inherit;
}
</style>
