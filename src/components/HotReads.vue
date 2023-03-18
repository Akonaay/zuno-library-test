<template>
	<div class="container" style="margin-top: -200px">
		<h5 class="mb-2">
			<img src="./../assets/fire_50px.png" width="25px" alt="" srcset="" />
			Hot Reads
		</h5>
		<div class="row">
			<div class="">
				<Carousel :autoplay="true" :items="7">
					<img
						class="img-fluid"
						src="./../assets/base.png"
						v-for="book in books"
						:key="book.BibNum"
					/>
				</Carousel>
			</div>
		</div>
	</div>
</template>

<script>
import Carousel from "vue-owl-carousel";
export default {
	name: "HotReads",
	components: { Carousel },
	data() {
		return {
			books: [],
		};
	},
	methods: {
		async fetchHotBooks() {
			await fetch("http://localhost:3000/books?_limit=5")
				.then((res) => res.json())
				.then((data) => (this.books = data))
				.catch((err) => console.log(err.message));
		},
	},
	mounted() {
		this.fetchHotBooks();
	},
};
</script>
