<script lang="ts">
	// Components
	import UseCases from "$lib/components/layout/UseCases.svelte";
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CustomerCardHero from "$lib/components/layout/hero-sections/CustomerCardHero.svelte";
</script>

<CustomerCardHero
  centered={false}
  title="The right tech. Every time."
  subtitle="Probook helps home service teams send the best technician to every job, increase sales, and make dispatch simple."
  customers={[
    {
      name: "Dani Dascher",
      position: "Dispatcher at Auchinachie",
      imageSrc: "/generated/image-a-friendly-woman-dispatcher-smiling-whil.webp",
      quote: "With Probook, I trust every job gets matched to the right tech. Our board is finally calm."  
    },
    {
      name: "Mike Sullivan",
      position: "Lead Dispatcher at Auchinachie",
      imageSrc: "/generated/image-an-experienced-male-technician-wearing-a.webp",
      quote: "Probook made it easy to coach new dispatchers and keep sales up, even on our busiest days."
    },
    {
      name: "Brandy Heesh",
      position: "Operations Manager at Auchinachie",
      imageSrc: "/generated/image-a-professional-woman-in-a-service-compan.webp",
      quote: "We’re seeing higher flips, more installs, and happier customers since switching to Probook."
    },
    {
      name: "Chris Holleran",
      position: "Vice President and General Manager at Auchinachie Services",
      imageSrc: "/generated/image-a-confident-male-operations-manager-stan.webp",
      quote: "Probook helps us scale without the stress—and it’s simple for the whole team."
    },
    {
      name: "Andrea Williams",
      position: "Lead Dispatcher at Blake Brothers",
      imageSrc: "/generated/image-a-friendly-female-lead-dispatcher-at-her.webp",
      quote: "I depend on Probook every day. It’s made dispatching fast and accurate so I can focus on the customer."
    }
  ]}
/>
<LogoScroller
	label="Trusted by industry leaders"
	logoUrls={[
		'https://logo.clearbit.com/onehourheatandair.com',
		'https://logo.clearbit.com/benjaminfranklinplumbing.com',
		'https://logo.clearbit.com/mistersparky.com',
		'https://logo.clearbit.com/rescueairtx.com'
	]}
/>

<Summary
	title="What we do"
	text="Probook delivers AI-powered dispatching for home service companies. Optimize technician assignments, increase sales, and simplify day-to-day dispatch—no guesswork, just results."
/>

<Testimonials
	testimonials={[
		{
			name: "Doug Fenwick",
			position: "Dispatcher",
			company: "Raymond Cooling & Heating",
			quote: "With Probook, I'm no longer chained to the board. Autopilot frees up ten extra hours every week for me to help customers and actually step away at lunch—it’s like hiring a second dispatcher without the extra salary.",
			image: "/generated/image-a-middle-aged-male-dispatcher-in-a-hvac-.webp"
		},
		{
			name: "Mia Farrow",
			position: "Operations manager",
			company: "Cascade Plumbing",
			quote: "Before Probook, late jobs meant lost installs and chaotic days. Now, live alerts help us reschedule jobs before things go off track. We've saved nearly $20k a month by catching revenue that used to slip away.",
			image: "/generated/image-a-female-plumbing-manager-in-a-bustling-.webp"
		},
		{
			name: "Eldon Fisher",
			position: "Owner",
			company: "Fisher Home Services",
			quote: "We cut misassigned jobs by 30% just by using Copilot. That’s over $12,000 a month back in our pocket from better job-tech matches. I wish we’d found it years ago.",
			image: "/generated/image-an-older-male-owner-of-a-home-services-c.webp"
		}
	]}
/>

<Features
	title="What sets Probook apart"
	subtitle="AI dispatching built for top-performing home service teams"
	features={[
	  {
	    title: "AI-powered dispatching",
	    description: "Assigns the right tech to every job by analyzing skills, revenue potential, and windshield time in real time."
	  },
	  {
	    title: "Copilot & Autopilot modes",
	    description: "Choose guided recommendations or full automation, so one dispatcher can manage 20+ technicians."
	  },
	  {
	    title: "Live Revenue Heatmap",
	    description: "View top sellers and hot zip codes at a glance, so the whole team focuses where it counts."
	  },
	  {
	    title: "Real-time ServiceTitan sync",
	    description: "Instantly reflects jobs, updates, and completions—no double entry and no waiting."
	  },
	  {
	    title: "2-day onboarding with our CEO",
	    description: "Onsite launch and weekly check-ins mean your team is confident and moving on day one."
	  },
	  {
	    title: "3-min response. 24/7 support.",
	    description: "Industry-best 3-minute median response, 25-minute median resolution, and 100% satisfaction."
	  }
	]}
/>

<UseCases
	title="Use Cases"
	subtitle="Real-world applications for your business needs"
	useCases={[
		{
			title: "Fill cancelations quicker",
			description: "Empty spot on the board? Probook fills it instantly based on nearby availability and revenue upside.",
			image: "/generated/image-a-bustling-office-environment-with-hvac-.webp",
			link: {
				href: "/use-cases/fill-cancelations",
				label: "Learn more"
			}
		},
		{
			title: "Reschedule with less fallout",
			description: "Get proactive reschedule suggestions triggered by late jobs—reduce angry calls and missed installs.",
			image: "/generated/image-in-a-cozy-office-space-a-plumbing-compan.webp",
			link: {
				href: "/use-cases/reschedule-assist",
				label: "Learn more"
			}
		},
		{
			title: "Send the right tech for same-day flips",
			description: "Prioritize calls with replacement potential and match them with the closer most likely to convert.",
			image: "/generated/image-a-group-of-service-technicians-standing-.webp",
			link: {
				href: "/use-cases/right-tech-flips",
				label: "Learn more"
			}
		}
	]}
/>

<AboutTeaser />
<CallToAction
  title="Smarter dispatching. Stronger. Yes."
  subtitle="Reduce workload, grow sales, and simplify dispatching"
  description="Get immediate results with a 2-day in-person launch and hands-on support. No disruption—just smarter dispatching from day one."
  imageSrc="/generated/image-a-cheerful-female-dispatcher-sitting-at-.webp"
  callsToAction={[
    { href: '/book-demo', label: 'Book a demo', variant: 'primary' },
    { href: '/get-started', label: 'Get started', variant: 'secondary' }
  ]}
/>
