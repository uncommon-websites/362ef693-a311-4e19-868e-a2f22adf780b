<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
  testimonials={[
    {
      name: "Santiago Alvarez",
      position: "Lead Dispatcher",
      company: "Atlas Comfort Services",
      quote:
        "We saw an immediate jump in revenue and my team can finally handle a full board without late nights. Investing in Probook paid off—fast.",
      image: "/generated/image-professional-headshot-of-a-hispanic-male.webp"
    },
    {
      name: "Imani Grant",
      position: "Operations Manager",
      company: "SureTemp HVAC",
      quote:
        "We worried about switching systems, but Probook made it easy. The ROI is clear. We save hours every week and can give customers better service.",
      image: "/generated/image-professional-headshot-of-a-black-female-.webp"
    },
    {
      name: "Ravi Anand",
      position: "Owner",
      company: "FlowMaster Plumbing",
      quote:
        "I hesitated at first, but Probook let us grow without hiring more staff. My dispatchers say it’s the simplest tech upgrade we’ve made.",
      image: "/generated/image-professional-headshot-of-a-southeast-asi.webp"
    }
  ]}
/>

<CallToAction
  title="Put the right tech on the right job. Every time."
  subtitle="Make every call count—Probook does the heavy lifting."
  description="Maximize revenue, minimize drive time, and let dispatchers work confidently. Join companies already saving hours and seeing more sales—without more stress or complex setup."
  imageSrc="/generated/image-a-home-services-dispatcher-smiling-warml.webp"
  callsToAction={[
    {
      href: '/demo',
      label: 'Book a demo',
      variant: 'primary'
    },
    {
      href: '/contact',
      label: 'Talk to George →',
      variant: 'secondary'
    }
  ]}
/>
