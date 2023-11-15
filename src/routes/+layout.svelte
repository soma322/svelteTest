<script lang="ts">
import "../app.postcss";
import { ModeWatcher } from "mode-watcher";
import { cn } from "$lib/utils";

	let className: string | undefined | null = undefined;
	export { className as class };
</script>


<ModeWatcher />


<nav class={cn("flex items-center space-x-4 lg:space-x-6", className)}>
	<a
		href="/examples/dashboard"
		class="text-sm font-medium transition-colors hover:text-primary"
	>
		Overview
	</a>

	<a
		href="/examples/dashboard"
		class="text-sm font-medium text-muted-foreground transition-colors hover:text-primary"
	>
		Customers
	</a>
	<a
		href="/examples/dashboard"
		class="text-sm font-medium text-muted-foreground transition-colors hover:text-primary"
	>
		Products
	</a>
	<a
		href="/examples/dashboard"
		class="text-sm font-medium text-muted-foreground transition-colors hover:text-primary"
	>
		Settings
	</a>
</nav>

<slot></slot>

