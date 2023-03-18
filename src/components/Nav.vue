<template>
	<div class="container">
		<header class="fixed-top" id="site-header">
			<nav class="navbar navbar-expand-md navbar-dark text-black-50 container">
				<a class="navbar-brand" href="/">
					<img src="./../assets/logo.png" alt="" width="50px" />
					<span style="color: black" class="font-italic">Zuno Libray</span>
				</a>

				<button
					class="navbar-toggler"
					type="button"
					data-toggle="collapse"
					data-target="#navbarSupportedContent"
					aria-controls="navbarSupportedContent"
					aria-expanded="false"
					aria-label="Toggle navigation"
				>
					<span class="navbar-toggler-icon"></span>
				</button>

				<div class="collapse navbar-collapse" id="navbarSupportedContent">
					<ul class="navbar-nav mr-auto">
						<li class="nav-item active">
							<router-link
								to="/"
								class="nav-link nav-link-menu pr-3 pl-3"
								style="
									border-radius: 20px;
									color: black;
									background: whitesmoke;
								"
								>Home <span class="sr-only">(current)</span></router-link
							>
						</li>
						<li class="nav-item">
							<router-link to="/" class="nav-link nav-link-menu"
								>Category</router-link
							>
						</li>
						<li class="nav-item">
							<router-link to="/" class="nav-link nav-link-menu"
								>Popular</router-link
							>
						</li>

						<li class="nav-item">
							<router-link to="/" class="nav-link nav-link-menu"
								>My Picks</router-link
							>
						</li>
					</ul>

					<ul class="navbar-nav">
						<li class="nav-item">
							<router-link to="/" class="nav-link nav-link-menu">
								<img src="img/user_50px.png" alt="" width="25px" srcset="" />
							</router-link>
						</li>
						<li class="nav-item">
							<router-link to="/" class="nav-link nav-link-menu">
								<img
									src="img/shopping_cart_50px.png"
									alt=""
									width="25px"
									srcset=""
								/>
							</router-link>
						</li>
					</ul>
				</div>
			</nav>
		</header>
	</div>
</template>
