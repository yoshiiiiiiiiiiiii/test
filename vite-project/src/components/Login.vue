<template>
  <div class="login-container">
    <div class="login-card">
      <h2>ログイン</h2>
      <form @submit.prevent="login" class="login-form">
        <div class="form-group">
          <label for="username">ユーザー名:</label>
          <input type="text" id="username" v-model="username" required>
        </div>
        <div class="form-group">
          <label for="password">パスワード:</label>
          <input type="password" id="password" v-model="password" required>
        </div>
        <button type="submit" class="login-button">ログイン</button>
      </form>
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      username: '',
      password: ''
    };
  },
  methods: {
    login(event) {
      event.preventDefault();
      // ログインのロジックをここに実装
      if (this.username === 'your_username' && this.password === 'your_password') {
        // ログイン成功時の処理
        this.$router.push('/home'); // ホームページにリダイレクト
      } else {
        // ログイン失敗時の処理
        alert('ログインに失敗しました');
        this.$router.push('/plc');
      }
    }
  }
};
</script>

