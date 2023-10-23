<footer>
	<div class="container-footer" id="footer">
		<h2>CONTACT ME</h2>

		<div class="socials">
			<ul>
				<li>
					<a target="_blank" href="https://www.linkedin.com/in/tim-oosterveer-a33522124/">
						<i class="fa-brands fa-linkedin fa-2xl" style="color: #ffffff;" />
					</a>
				</li>
				<li>
					<a target="_blank" href="https://github.com/TimOosterveer">
						<i class="fa-brands fa-github fa-2xl" style="color: #ffffff;" />
					</a>
				</li>
				<li>
					<a href="mailto:timoosterveer99@gmail.com">
						<i class="fa-regular fa-envelope fa-2xl" style="color: #ffffff;" />
					</a>
				</li>
			</ul>
		</div>
	</div>
</footer>

<style>
	footer {
		position: sticky;
		width: 100%;
		height: 20rem;
		background-color: #1a535c;
		padding: var(--padding);
    overflow: hidden;
	}

	.container-footer {
		width: 35vw;
	}

	h2 {
		font-weight: 200;
		font-size: 5rem;
	}

	.socials {
		width: 20vw;
	}

	ul {
		list-style: none;
		display: flex;
		justify-content: space-between;
	}

	@media screen and (max-width: 767px) {

		footer {
			height: 10rem;
		}

		.container-footer{
			width: 100%;
		}

		h2 {
			font-size: 2rem;
		}

		.socials {
			width: 50%;
		}
	}
</style>
