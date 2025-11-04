<script lang="ts">
	// Components
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import Hero from "$lib/components/layout/hero-sections/Hero.svelte";

	// Icons
	import IconBrain from "~icons/lucide/brain";
	import IconZap from "~icons/lucide/zap";
	import IconUnlock from "~icons/lucide/unlock";
	import IconTrendingUp from "~icons/lucide/trending-up";
	import IconEye from "~icons/lucide/eye";
	import IconShield from "~icons/lucide/shield";
</script>

<Hero
	title="Ship landing pages in hours, not weeks"
	subtitle="AI agents that generate on-brand landing pages at scale, so your growth team never waits on dev again."
	imageSrc="/generated/image-environmental-portrait-a-professional-ma.webp"
	centered={false}
	callsToAction={[
		{
			href: "/contact",
			label: "Get started"
		},
		{
			href: "/about",
			label: "See how it works"
		}
	]}
/>
<LogoScroller
	label="Trusted by industry leaders"
	logoUrls={[
		'https://cdn.brandfetch.io/notion.so/w/400/h/400/logo',
		'https://cdn.brandfetch.io/vercel.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/linear.app/w/400/h/400/logo',
		'https://cdn.brandfetch.io/stripe.com/w/400/h/400/logo'
	]}
/>

<Summary
	title="The problem we solve"
	text="Growth teams at scaling SaaS companies move fast, but dev bottlenecks turn landing page launches from hours into weeks. Flint's autonomous AI agents internalize your brand system and generate pixel-perfect, on-brand landing pages at scale—so your campaigns go live the same day, not the same month."
/>

<Testimonials
	testimonials={[
		{
			name: "Maya Chen",
			position: "Director of Growth Marketing",
			company: "CloudScale",
			quote:
				"We launched 12 campaign pages in three weeks instead of waiting months for dev resources. Flint paid for itself in the first sprint.",
			image: "/generated/image-environmental-portrait-professional-asia.webp"
		},
		{
			name: "Marcus Williams",
			position: "Head of Demand Generation",
			company: "DataPulse",
			quote:
				"No more brand inconsistency nightmares. Every page matches our design system perfectly, and our CEO actually stopped sending revision requests.",
			image: "/generated/image-collaborative-cluster-professional-black.webp"
		},
		{
			name: "Sofia Rodriguez",
			position: "VP of Marketing",
			company: "Velocity",
			quote:
				"Cut our landing page costs by 60% while tripling output. Our agency was billing $8K per page. Now we ship same-day for pennies.",
			image: "/generated/image-environmental-portrait-professional-hisp.webp"
		}
	]}
/>

<Features
	title="Built for growth teams who move fast"
	subtitle="Autonomous AI agents that understand your brand system and generate pixel-perfect landing pages at scale."
	features={[
		{
			title: "Brand system intelligence",
			description:
				"AI agents that internalize your design tokens, components, and brand guidelines to generate pages that look like your design team built them. No more off-brand pages or manual QA.",
			icon: IconBrain
		},
		{
			title: "Ship in hours, not weeks",
			description:
				"From concept to live page in the same day. Launch campaigns when your audience is ready, not when dev capacity opens up.",
			icon: IconZap
		},
		{
			title: "Zero dev dependency",
			description:
				"Growth teams get full autonomy to create, iterate, and publish landing pages without entering the dev queue. Your engineers stay focused on product.",
			icon: IconUnlock
		},
		{
			title: "Scale without compromise",
			description:
				"Run unlimited campaigns while maintaining perfect brand consistency across every page. The more you ship, the smarter the system becomes.",
			icon: IconTrendingUp
		},
		{
			title: "Same-day live demos",
			description:
				"See your actual brand come to life in a working landing page before you commit. No mockups, no guessing.",
			icon: IconEye
		},
		{
			title: "Enterprise-grade infrastructure",
			description:
				"Built on secure, scalable architecture that growing SaaS companies trust with their most important campaigns.",
			icon: IconShield
		}
	]}
/>
<AboutTeaser />
<CallToAction
	title="See your brand live in hours"
	subtitle="Not weeks"
	description="Stop waiting on dev queues. Get a same-day demo with your actual brand system—no mockups, no guessing, no risk. See exactly how Flint generates pixel-perfect landing pages before you commit."
	imageSrc="/generated/image-environmental-portrait-a-happy-confident.webp"
	callsToAction={[
		{
			href: "/contact",
			label: "Get your demo today",
			variant: "primary"
		},
		{
			href: "/about",
			label: "See how it works",
			variant: "secondary"
		}
	]}
/>
