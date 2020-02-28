<template>
  <div class="container">
    <p class="works-img">
      <img src="~/assets/web/taskmanagement.jpg" alt="TaskManagementApp" />
    </p>
    <p class="works-description">
      Nuxt.jsとFirebaseを使用したタスク管理アプリ。チャンネルの作成・削除、タスクの追加・削除・進捗の状況変更が可能。上記の機能をリアルタイムに実現。
      <span>
        <a href="https://github.com/To-Ko5/task_management_app" target="_blank">ソースコードはこちら</a>
      </span>
    </p>
    <p class="view-more-btn-outer">
      <a class="view-more-btn" href="https://chats-app-tk.firebaseapp.com/" target="_blank">サイトを見る</a>
    </p>
  </div>
</template>

<style lang="scss" scoped>
@import "assets/style/btn.scss";
@import "assets/style/works_view_more.scss";

span {
  display: block;
  a {
    text-decoration: underline;
  }
}
</style>