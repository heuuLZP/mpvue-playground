<template>
  <div>
    <div class="mb-10">生命周期</div>
	<div class="content">
		<p>
			beforeCreate、created小程序启动时已经触发
		</p>
		<p>
			beforeMount、mounted页面加载时才触发
		</p>
		<input type='text' class="form-control mb-10" placeholder="请输入..." v-model='name'>
		<div>{{name}}</div>
		<p>
			beforeUpdate、update当页面重新渲染时才触发,比如改变输入框中的值
		</p>
		<p>
			beforeCreate -> created -> onLoad -> onShow -> onReady -> beforeMount -> （如果是再次打开 beforeUpdate ->） mounted  ->  onUnload
		</p>
	</div>
  </div>
</template>

<script>
export default {
  components: {},

  data() {
    return {
      name: '',
    };
  },
  beforeCreate() {
    console.log('beforeCreate 触发...');
  },
  created() {
    console.log('create 触发...');
  },
  beforeMount() {
    console.log('beforeMount 触发...');
  },
  mounted() {
    console.log('mounted 触发...');
  },
  beforeUpdate() {
    console.log('beforeUpdate 触发...');
  },
  updated() {
    console.log('updated 触发...');
  },
  beforeDestroy() {
    console.log('beforeDestroy 触发...');
  },
  destroyed() {
    console.log('destroyed 触发...');
  },
  onLoad() {
    console.log('onLoad 触发...');
  },
  onShow() {
    console.log('onShow 触发...');
  },
  onReady() {
    console.log('onReady 触发...');
  },
  onHide() {
    console.log('onHide 触发...');
  },
  onUnload() {
    console.log('onUnload 触发...');
  },
};
</script>

<style scoped>
p {
	margin-bottom: 10px;
	font-size: 14px;
}
.mb-10 {
	margin-bottom: 10px;
}
.content {
	padding-left: 10px;
}
.form-control {
  display: block;
  padding: 0 12px;
  margin-bottom: 5px;
  border: 1px solid #ccc;
  width: 200px;
}
</style>
