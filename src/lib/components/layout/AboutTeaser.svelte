<!--
@component AboutTeaser
Engaging founder story teaser that builds personal connection and company credibility.
-->
<script lang="ts">
	// Types
	type TeamMember = {
		name: string;
		role: string;
		image: string;
	};

	// Components
	import Button from "../ui/Button.svelte";
	import IconArrowRight from "~icons/lucide/arrow-right";

	// State
	let sectionRef: HTMLElement;
	let isHovered = $state(false);

	let props = $props();

	// Data
	const teamMember: TeamMember = {
		name: "Founder",
		role: "CEO, Flint",
		image: "/generated/image-environmental-portrait-one-professional-.webp"
	};

	const founderQuote = "I built Flint after watching campaigns stall for weeks just waiting for landing pages. We needed a way to move fast without asking devs for favors or breaking our brand system.";
</script>

<section bind:this={sectionRef} {...props}>
	<div class="section-px section-py container mx-auto">
		<div class="relative mx-auto max-w-4xl">
			<!-- Quote Section -->
			<div class="grid gap-12">
				<blockquote class="relative">
					<div class="quote-mark text-brand-primary opacity-20" aria-hidden="true">"</div>
					<p class="text-title2 leading-relaxed">
						{founderQuote}
					</p>
				</blockquote>

				<!-- Founder Info & CTA -->
				<div 
					role="group"
					aria-label="Founder information"
					class={[
						"founder-card flex items-center justify-between gap-8 rounded-lg border transition-all duration-300",
						isHovered ? "border-brand-primary/30 bg-surface-secondary/50" : "border-surface-tertiary bg-surface-secondary/20"
					]}
					onmouseenter={() => isHovered = true}
					onmouseleave={() => isHovered = false}
				>
					<div class="flex items-center gap-4">
						<img
							src={teamMember.image}
							alt={teamMember.name}
							class="size-16 rounded-full object-cover ring-2 ring-surface-tertiary"
						/>
						<div>
							<div class="text-headline font-medium">{teamMember.name}</div>
							<div class="text-callout text-emphasis-medium">{teamMember.role}</div>
						</div>
					</div>
					
					<Button 
						href="/about" 
						variant="secondary" 
						size="md"
						class={[
							"learn-more-btn whitespace-nowrap transition-transform duration-300",
							isHovered ? "translate-x-1" : ""
						]}
					>
						<span>Learn our story</span>
						<IconArrowRight class="ml-2 size-4" />
					</Button>
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	.quote-mark {
		position: absolute;
		top: -2rem;
		left: -1rem;
		font-size: 8rem;
		font-weight: 700;
		line-height: 1;
		font-family: Georgia, serif;
		user-select: none;
		pointer-events: none;
	}

	.founder-card {
		padding: 1.5rem 2rem;
	}

	@media (max-width: 768px) {
		.founder-card {
			flex-direction: column;
			align-items: flex-start;
			gap: 1rem;
			padding: 1.5rem;
		}

		.quote-mark {
			font-size: 5rem;
			top: -1.5rem;
			left: -0.5rem;
		}
	}
</style>
