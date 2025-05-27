<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
  {
    title: "Built by dispatchers, for dispatchers",
    description: "We solve real-world dispatch problems because we’ve lived them—building with and for teams on the ground."
  },
  {
    title: "Show up, don’t just sell",
    description: "We’re hands-on: in-person launches, fast responses, and always a direct line to a real person—not just chatbots."
  },
  {
    title: "Move fast, improve faster",
    description: "Rapid rollouts and continuous improvements shaped by real dispatcher feedback."
  },
  {
    title: "Every feature earns trust",
    description: "We don’t ship AI ‘just because’—we measure results in dispatcher trust, team buy-in, and daily wins."
  },
  {
    title: "Support, always",
    description: "Questions at midnight? We’re there. Every user matters, from day one through every season."
  }
];
</script>

<SecondaryHero
	title="Built by dispatchers for home service teams"
	subtitle="Expert help, fast support, and AI-powered dispatching that actually works on the ground"
	imageSrc="/generated/image-a-diverse-professional-team-collaboratin.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"Before Probook, our team worked the phones as dispatchers—bouncing between spreadsheets and gut decisions, trying to match the right tech with the right call. At 10+ trucks, everything got harder: constant reshuffling, missed revenue, and growing pressure on dispatch. We built Probook because there had to be a better way.",
		"Probook is an AI-powered dispatching tool built by dispatchers, for dispatchers. It uses real data to recommend the best tech for every call—not just who’s closest, but who’s most likely to close the job, finish fast, or turn a tune-up into a sale. It’s field-proven software that boosts revenue, reduces workload, and replaces guesswork with clarity.",
		"We don’t just launch Probook—we show up. Our CEO joins your team for hands-on setup, and we stick with you long after. With 3-minute response times, dedicated check-ins, 24/7 support, and features shaped by dispatch feedback, Probook grows alongside your business and team. Real help, every step of the way."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
	stakeholderType="team"
	title="Meet our founder."
	subtitle="Real experience. Real support."
	stakeholders={[
		{
			name: "George Eliadis",
			position: "CEO & Founder",
			bio: "George Eliadis built Probook from the dispatch board up. With years in the trenches himself, he guides every launch in person and builds real-world AI tools that teams actually trust.",
			image: "/generated/image-a-professional-headshot-of-george-eliadi.webp"
		}
	]}
/>

<StakeholderGrid
	stakeholderType="investor"
	title="Backed by the best."
	subtitle="Point Nine, TSIC and others"
	stakeholders={[
		{
			name: "Point Nine Capital",
			image: "https://cdn.brandfetch.io/pointnine.com/w/400/h/400/logo?c=1id_elLz2Bd5Ej-dWo7"
		},
		{
			name: "TSIC Ventures",
			image: "https://cdn.brandfetch.io/tiny.vc/w/400/h/400/logo?c=1a2b3c4d5e"
		},
		{
			name: "Sequoia Capital",
			image: "https://cdn.brandfetch.io/sequoiacap.com/w/400/h/400/logo"
		}
	]}
/>

<!-- CTA Section -->
<CallToAction
  title="See how Probook works for your team"
  subtitle="Talk to a real dispatcher, not just a sales rep"
  description="Book a demo or ask your toughest dispatching question—our CEO or an experienced dispatcher will personally walk you through the answers. Fast support, real advice, and hands-on help from people who’ve done the job."
  imageSrc="/generated/image-a-friendly-home-service-dispatcher-sitti.webp"
  callsToAction={[
    { href: '/contact', label: 'Talk to a dispatcher', variant: 'primary' },
    { href: '/demo', label: 'Book a demo', variant: 'secondary' }
  ]}
/>
