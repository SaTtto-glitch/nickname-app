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
html, body, #app{
			width: 100%; height: 100%;
			margin: 0px; padding: 0px;
		}
		.d-title {
			width: 100%; height: auto;
			margin: 0px; padding: 30px 0px;
			background-color: silver;
			font-size: 2em;
			text-align: center;
		}
		.d-line-1 {
			width: 100%; height: auto;
			margin: 0px; padding: 120px 0px 10px 0px;
			background-color: lightgray;
			text-align: center;
			font-size: 2em;
		}
		.d-line-2 {
			width: 100%; height: auto;
			margin: 0px; padding: 0px;
			background-color: lightgray;
			text-align: center;
			font-size: 6em;
			font-weight: bold;
			color: darkred;
		}
		.d-line-3 {
			width: 100%; height: auto;
			margin: 0px; padding: 10px 0px 120px 0px;
			background-color: lightgray;
			text-align: center;
			font-size: 2em;
		}
</style>
