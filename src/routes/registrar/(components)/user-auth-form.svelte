<script lang="ts">
	import { Icons } from "$lib/components/docs/icons";
	import { Button } from "$lib/components/ui/button";
	import { Input } from "$lib/components/ui/input";
	import { Label } from "$lib/components/ui/label";
	import { cn } from "$lib/utils";

	let className: string | undefined | null = undefined;
	export { className as class };

	let isLoading = false;
	async function onSubmit() {
		isLoading = true;

		setTimeout(() => {
			isLoading = false;
		}, 3000);
	}

	function handleClick() {
    if (!isLoading) {
		let isLoading = false;
		onSubmit();
		
      // Call your function here when the button is clicked and not in a loading state
      console.log('Button clicked!');
    }
  }
</script>

<div class={cn("grid gap-6", className)} {...$$restProps}>
	<form on:submit|preventDefault={onSubmit}>
		<div class="grid gap-2">
			<div class="grid gap-1">
				<Label class="sr-only" for="email">Email</Label>
				<Input
					id="email"
					placeholder="name@example.com"
					type="email"
					autocapitalize="none"
					autocomplete="email"
					autocorrect="off"
					disabled={isLoading}
				/>
			</div>
			<div class="grid gap-1">
				<Label class="sr-only" for="email">Email</Label>
				<Input
					id="contra"
					placeholder="Contraseña"
					type="password"
					autocapitalize="none"
					disabled={isLoading}
				/>
			</div>
			<Button on:click={handleClick} disabled={isLoading}>
				{#if isLoading}
					<Icons.spinner class="mr-2 h-4 w-4 animate-spin" />
				{/if}
				Crear cuenta
			</Button>
		</div>
	</form>
	<div class="relative">
		<div class="absolute inset-0 flex items-center">
			<span class="w-full border-t" />
		</div>
		<div class="relative flex justify-center text-xs">
			<span class="bg-background px-2 text-muted-foreground">
				<a
					href="/login"
					class="underline underline-offset-4 hover:text-primary"
				>
					¿Ya tienes cuenta? Da click aqui!
			</span>
		</div>
	</div>

</div>