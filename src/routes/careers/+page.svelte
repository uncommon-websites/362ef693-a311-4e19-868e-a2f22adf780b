<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
	{
		title: "Direct impact, every day",
		description: "See your work in action—features go live weekly and shape outcomes for real dispatchers and operators.",
		icon: IconBriefcase
	},
	{
		title: "Mentorship from operators",
		description: "Learn from experienced dispatchers, leaders, and our CEO—fast feedback, real responsibility, steady growth.",
		icon: IconUsers
	},
	{
		title: "Growth and support",
		description: "High-autonomy environment with a 24/7 support culture, competitive compensation, and ample room to advance.",
		icon: IconHeart
	}
];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Gabriela Torres",
    position: "Customer Support Specialist",
    company: "Support Team",
    quote:
      "The culture here is genuinely welcoming and inclusive. From my first day, everyone encouraged me to ask questions and share ideas. I really feel like I belong and can grow here.",
    image: "/generated/image-a-young-hispanic-woman-in-a-professional.webp"
  },
  {
    name: "Derrick Williams",
    position: "Software Engineer",
    company: "Engineering Team",
    quote:
      "There’s always someone willing to offer mentorship or feedback. I’ve been able to take on bigger projects and keep learning every day. My growth here has been tremendous.",
    image: "/generated/image-a-professional-headshot-of-a-black-male-.webp"
  },
  {
    name: "Thomas White",
    position: "Senior Product Manager",
    company: "Product Team",
    quote:
      "Our work environment is built on trust and support. The team is passionate but laid-back, and there's real appreciation for our effort. I’ve never felt more valued.",
    image: "/generated/image-a-senior-white-male-product-manager-is-c.webp"
  }
];

	const processSteps = [
	{
		step: 1,
		title: "Submit your application",
		description: "Send your resume and a quick note about why you're interested—no lengthy cover letter required."
	},
	{
		step: 2,
		title: "Intro call",
		description: "A short call with a team member to discuss your background and what you’re looking for."
	},
	{
		step: 3,
		title: "Skills assessment",
		description: "A relevant challenge or practical scenario to show how you think and work. (Paid if substantial.)"
	},
	{
		step: 4,
		title: "Final interview",
		description: "Meet with our CEO and key team members to discuss your approach and what working together could look like."
	},
	{
		step: 5,
		title: "Decision & feedback",
		description: "Hear from us quickly—yes or no. We value your time and keep candidates in the loop at every step."
	}
];

	const values = [
	{
		title: "Live what you build",
		description: "Most of us started as dispatchers or operators. We work on the ground, stay close to customers, and build what matters most."
	},
	{
		title: "Fast, open, direct",
		description: "We value honest feedback, fast changes, and solving real pain points—together."
	},
	{
		title: "No ego, just results",
		description: "Trust, autonomy, and accountability drive us. When something isn’t working for real users, it doesn’t stay."
	}
];
</script>

<!-- Hero Section -->

<SecondaryHero
  title="Build the future of dispatching together"
  subtitle="Join a mission-driven team focused on growth, support, and real impact"
  image="/generated/image-a-group-of-office-employees-standing-tog.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Build your career while making an impact" />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
