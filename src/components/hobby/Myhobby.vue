<script>
export default {
	setup() {
		return {
			bios: [
				{
					id: 1,
					bio:
						'Hobby:',
				},
				{
					id: 2,
					bio:
						'My Hobbies when I do not have a class is: Reading and sleeping. ',
                       
				},
			],
		};
	},
};
</script>

<template>
    <body class="bg-blue-400">
	<div class="block sm:flex sm:gap-10 mt-10 sm:mt-20 bg-blue-400">
		<!-- About profile image -->
		<div class="w-full sm:w-1/4 mb-7 sm:mb-0">
			<img
				src="@/assets/images/anna.jpg"
				class="rounded-xl w-96"
				alt="anna"
			/>
		</div>

		<!-- About details -->
		<div class="w-full sm:w-3/4 text-left">
			<p
				v-for="bio in bios"
				:key="bio.id"
				class="font-general-regular mb-4 text-ternary-light dark:text-ternary-light text-lg"
			>
				{{ bio.bio }}
			</p>
		</div>
	</div>
</body>
</template>
