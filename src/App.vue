<template>
	<div id="app">
    <!-- Navbar  -->
		<Navbar />

		<!-- Banner  -->
		<div class="banner">
			<div id="demo-1">
				<div class="demo-inner-content container">
					<div class="container">
						<div class="row">
							<!-- order-lg-first -->
							<div class="col-md-7 mt-lg-0 mt-5">
								<h1 class="mb-4">
									Get your <strong>favourite <br />Book</strong> all in
									<strong>one place</strong>
								</h1>

								<a
									href="#!"
									class="btn btn-md bg-dark text-white rounded pr-3 pl-3"
									style="border-radius: 20px !important"
									>View Categories</a
								>
							</div>
							<!-- order-first text-lg-left -->
							<div class="col-md-5 text-center mt-lg-5">
								<div class="banner-right">
									<img
										src="/assets/img/pexels-karolina-grabowska-4207905.jpg"
										alt=""
										class="img-fluid"
									/>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>

		<!-- Hot Reads  -->
		<HotReads />

		<!-- Search Book & New Released -->
		<NewReleased />

		<!-- Footer  -->
		<Footer />
	</div>
</template>

<script>
import Navbar from "./components/Nav.vue";
import HotReads  from "./components/HotReads.vue";
import NewReleased from "./components/NewReleased.vue";
import Footer from "./components/Footer.vue";

export default {
	name: "App",
	components: {
		Navbar,NewReleased, HotReads, Footer
	},
};
</script>

<style>
