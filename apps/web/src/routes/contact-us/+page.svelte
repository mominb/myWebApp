<script>
	let name;
	let email;
	let subject;
	let message;

	function sendMessage(event) {
		event.preventDefault();
		console.log('Name:', name);
		console.log('Email:', email);
		console.log('Subject:', subject);
		console.log('Message:', message);
	}
</script>

<section class="bg-white">
	<div class="py-8 lg:py-16 px-4 mx-auto max-w-screen-md">
		<h2 class="mb-4 text-4xl tracking-tight font-extrabold text-center text-gray-900 ">
			Contact Us
		</h2>

		<!-- svelte-ignore a11y-click-events-have-key-events -->
		<form on:submit|preventDefault={sendMessage} class="space-y-8">
			<div>
				<label for="name" class="block mb-2 text-sm font-medium text-gray-900 ">Your name</label>
				<input
					bind:value={name}
					type="name"
					id="name"
					class="shadow-sm bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full p-2.5 "
					placeholder="Your name"
					required
				/>
			</div>
			<div>
				<label for="email" class="block mb-2 text-sm font-medium text-gray-900 ">Your email</label>
				<input
					bind:value={email}
					type="email"
					id="email"
					class="shadow-sm bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full p-2.5 "
					placeholder="example@email.com"
					required
				/>
			</div>

			<div>
				<label for="subject" class="block mb-2 text-sm font-medium text-gray-900 ">Subject</label>
				<input
					bind:value={subject}
					type="text"
					id="subject"
					class="block p-3 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 shadow-sm focus:ring-primary-500 focus:border-primary-500 "
					placeholder="Let us know how we can help you"
					required
				/>
			</div>
			<div class="sm:col-span-2">
				<label for="message" class="block mb-2 text-sm font-medium text-gray-900 "
					>Your message</label
				>
				<textarea
					bind:value={message}
					id="message"
					rows="6"
					class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg shadow-sm border border-gray-300 focus:ring-primary-500 focus:border-primary-500 "
					placeholder="Leave a comment..."
				/>
			</div>
			<button on:click={sendMessage} type="submit" class="btn btn-primary">Send message</button>
		</form>
	</div>
</section>
