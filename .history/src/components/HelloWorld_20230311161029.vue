<template>
  <div class="hello">
    <p class="d-title">
      {{ appName }}
    </p>
    <p class="d-line-1">あなたのニックネームは</p>
    <p class="d-line-2">
      {{ nickname }}
    </p>
    <p class="d-line-3">です!!</p>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      appName: "ニックネームメーカー", // アプリ名
      nickname: "ニックネーム", // ニックネーム
      names: ["スライム", "スライムベス", "メタルスライム", "はぐれメタル", "メタルキング"],
    };
  },

  methods: {
    myMethodA() {},
    myMethodB() {},
    myMethodC() {},

    roulette() {
      // ニックネームを確定する関数
      console.log("roulette!!");
      // ランダムを使って1つだけ選択する
      let rdm = Math.random() * this.names.length; // 乱数と配列の要素数を掛け算
      let index = Math.floor(rdm); // 整数に変換(配列の添字)
      this.nickname = this.names[index]; // ニックネームの決定
    },
  },

  created() {
    console.log("created!!");
    this.roulette(); // roulette関数を実行する
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
