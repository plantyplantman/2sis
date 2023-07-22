<script>
	const urls = [
		'https://static.wixstatic.com/media/9882f2_1842cae98f4744549b367dfd3712185b~mv2.jpg/v1/fill/w_620,h_1328,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/1_1.jpg',
		'https://static.wixstatic.com/media/9882f2_c8f26c6d265948bb8beee44cf96661d5~mv2.jpg/v1/fill/w_618,h_1314,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/9882f2_c8f26c6d265948bb8beee44cf96661d5~mv2.jpg',
		'https://static.wixstatic.com/media/9882f2_ce70e56470ee43fd8ef3175c04cd67b2~mv2.jpg/v1/fill/w_612,h_1310,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/9882f2_ce70e56470ee43fd8ef3175c04cd67b2~mv2.jpg',
		'https://static.wixstatic.com/media/9882f2_6577834a9a6f40b5a4429245e96292cf~mv2.jpg/v1/fill/w_614,h_1328,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/9882f2_6577834a9a6f40b5a4429245e96292cf~mv2.jpg',
		'https://static.wixstatic.com/media/9882f2_8a1a6087c2be469786352f74244d7b36~mv2.jpg/v1/fill/w_614,h_1298,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/9882f2_8a1a6087c2be469786352f74244d7b36~mv2.jpg'
	];
</script>

<div class="container h-full mx-auto flex-col justify-center items-center lg:mt-20 mt-10">
	<h1 class="h1 text-center mb-4">Menu</h1>
	{#each urls as url}
		<img src={url} alt="menu" class="ml-auto mr-auto" />
	{/each}
</div>
