<script lang="ts">
	import { Button } from "$lib/components/ui/button";
	import UserAuthForm from "./(components)/user-auth-form.svelte";
</script>

<div
	class="container relative hidden h-[800px] flex-col items-center justify-center md:grid lg:max-w-none lg:px-0"
>
	<Button
		href="/examples/authentication"
		variant="ghost"
		class="absolute right-4 top-4 md:right-8 md:top-8"
	>
		Login
	</Button>
	
	<div class="lg:p-8">
		<div
			class="mx-auto flex w-full flex-col justify-center space-y-6 sm:w-[350px] content-center"
		>
			<div class="flex flex-col space-y-2 text-center">
				<h1 class="text-2xl font-semibold tracking-tight">
					Log in
				</h1>
				<p class="text-sm text-muted-foreground">
                    
				</p>
			</div>
			<UserAuthForm />
			
			<p class="px-8 text-center text-sm text-muted-foreground">
				By clicking continue, you agree to our{" "}
				<a
					href="/terms"
					class="underline underline-offset-4 hover:text-primary"
				>
					Terms of Service
				</a>{" "}
				and{" "}
				<a
					href="/privacy"
					class="underline underline-offset-4 hover:text-primary"
				>
					Privacy Policy
				</a>
				.
			</p>
		</div>
	</div>
</div>