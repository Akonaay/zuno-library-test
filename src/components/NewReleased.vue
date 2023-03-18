<template>
	<div style="" class="container">
		<!-- Search Book  -->
		<div class="d-flex justify-content-center mb-4 mt-4">
			<input
				type="text"
				v-model="search"
				class="form-control"
				placeholder="Find the book you like..."
				@change="searchBook(search)"
			/>
		</div>

		<!-- New Released  -->
		<div>
			<h5 class="mb-4">
				<img
					src="./../assets/open_book_50px.png"
					width="25px"
					alt=""
					srcset=""
				/>
				New Released
			</h5>
			<div class="row">
				<div v-for="book in books" :key="book.BibNum" class="col-md-3 mb-3">
					<div class="book-wrapper">
						<img src="./../assets/base.png" alt="" srcset="" />
						<h6 class="font-weight-bold mt-2" style="font-size: 18px">
							{{ book.title.substring(0, 22) }} ...
						</h6>
						<p>{{ book.author }}</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "NewReleased",
	data() {
		return {
			books: [],
			search: "",
		};
	},
	methods: {
		async fetchBooks() {
			await fetch("http://localhost:3000/books?_limit=12")
				.then((res) => res.json())
				.then((data) => (this.books = data))
				.catch((err) => console.log(err.message));
		},

		async searchBook(title) {
			title = this.search;
			await fetch(`http://localhost:3000/books?q=${title}`)
				.then((res) => res.json())
				.then((data) => (this.books = data))
				.catch((err) => console.log(err.message));
		},
	},
	mounted() {
		this.fetchBooks();
	},
};
</script>
