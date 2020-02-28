<template>
  <div class="container">
    <p class="works-img">
      <img src="~/assets/web/programming01.jpg" alt="EASYMEMO" />
    </p>
    <p
      class="works-description"
    >メモ帳のアプリ。JavaScriptとPHPで作成。入力中はLocalStorageで一時的に保存し、入力後はデータベースに保存する。一覧画面では、ページネーション機能をつけ、10個単位でページを切り替えられるようにしている。メモの削除や更新も可能。レスポンシブにも対応済み。</p>
    <p class="view-more-btn-outer">
      <a class="view-more-btn" href="http://to-kweb.com/memos/" target="_blank">サイトを見る</a>
    </p>
  </div>
</template>

<style lang="scss" scoped>
@import "assets/style/btn.scss";
@import "assets/style/works_view_more.scss";
</style>