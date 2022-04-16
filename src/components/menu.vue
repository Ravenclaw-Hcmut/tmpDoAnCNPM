<template>
  <div class="hello">
    <input type="text" v-model="name">
    <h1>{{ name }}</h1>
		<button @click="isShow = !isShow">toggle</button>

		<div v-show="isShow">
			<h2 v-bind:id="ids">fffffffffffs</h2>
		</div>
    <h1>{{ msg }}</h1>


    <input type="text" v-model="addTask">
	<button @click="tasks.push ({content: addTask, done: false})">Add</button>

	<div v-for = "(task, index) in tasks" :key="index">
		<input type="checkbox" v-model="task.done">
		<span :class="{done: task.done}">{{task.content}} </span>
	</div>
  </div>
</template>

<script>
export default {
	data() {
		return {
			name: 123,
			isShow: true,
			ids:'htl',
			tasks: [
				{ content: 'Evermore', done:false },
				{ content: 'Fearless', done:false },
				{ content: 'Red', done:false },
				{ content: 'Reputation', done:false },
			],
			addTask:'',
		}
	},
	methods: {
		fAdd: function() {
			this.tasks.push({
				content: this.addTask, done: false
			})
		}
	},
  props: {
    msg: String,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.done {
	text-decoration: line-through;
}
</style>
