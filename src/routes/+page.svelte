<script lang="ts">
	import { Button } from "$lib/components/ui/button";
	import {
		ArrowRight,
		Box,
		Code,
		Globe,
		Gamepad2,
	} from "lucide-svelte";
	import RewindLogo from "$lib/components/ui/RewindLogo.svelte";
	import MilkyWay from "$lib/components/ui/MilkyWay.svelte";

	const team = [
		{ name: "Daniel", role: "Lead Developer", image: "/team-1.jpg" },
		{ name: "Jim", role: "Game Designer", image: "/team-2.jpg" },
		{ name: "Floris", role: "2D Artist", image: "/team-3.jpg" },
		{ name: "Kerem", role: "Sound Engineer", image: "/team-4.jpg" },
	];
</script>

<!-- Navigation -->
<nav
	class="fixed top-0 w-full z-50 transition-all duration-300 bg-gradient-to-b from-black/90 via-black/40 to-transparent backdrop-blur-[2px]"
>
	<div class="container mx-auto px-6 h-20 flex items-center justify-between">
		<a href="/" class="flex items-center gap-3 group">
			<div
				class="w-9 h-9 rounded-lg bg-white/5 border border-white/10 flex items-center justify-center group-hover:bg-white/10 group-hover:scale-105 transition-all duration-300"
			>
				<RewindLogo class="w-4.5 h-4.5 text-white" />
			</div>
			<span
				class="font-heading font-bold text-base tracking-tight text-white group-hover:text-white/90 transition-colors"
				>REWIND <span class="text-white/25 font-light">STUDIOS</span
				></span
			>
		</a>

		<div
			class="hidden md:flex items-center gap-8 bg-white/[0.03] backdrop-blur-md px-7 py-2.5 rounded-full border border-white/[0.06]"
		>
			<a
				href="#work"
				class="nav-link text-[13px] font-medium text-white/40 hover:text-white transition-colors"
				>Work</a
			>
			<a
				href="#team"
				class="nav-link text-[13px] font-medium text-white/40 hover:text-white transition-colors"
				>Team</a
			>
			<a
				href="#studio"
				class="nav-link text-[13px] font-medium text-white/40 hover:text-white transition-colors"
				>Studio</a
			>
		</div>

		<Button
			variant="ghost"
			class="hidden sm:flex hover:bg-white text-white hover:text-black transition-all rounded-full px-6 font-medium text-sm h-10 border border-white/10 hover:border-white"
		>
			Let's Talk
		</Button>
	</div>
</nav>

<!-- Hero Section -->
<section
	class="min-h-screen flex items-center justify-center pt-20 relative overflow-hidden bg-[#020202]"
>
	<MilkyWay />

	<div class="container mx-auto px-6 text-center z-10 space-y-10">
		<div class="animate-in fade-in duration-1000 delay-100">
			<div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full border border-white/[0.06] bg-white/[0.03] mb-8">
				<Gamepad2 class="w-3.5 h-3.5 text-amber-400" />
				<span class="text-xs text-white/50 font-medium tracking-wide">INDIE GAME STUDIO</span>
			</div>
		</div>

		<h1
			class="text-6xl md:text-8xl lg:text-9xl font-heading font-bold tracking-tighter text-white max-w-6xl mx-auto leading-[0.85] animate-in fade-in zoom-in-95 duration-1000 delay-200 drop-shadow-2xl"
		>
			RELIVE THE <br class="hidden md:block" />
			<span class="text-gold-shine">GOLDEN AGE</span>
		</h1>

		<p
			class="text-lg md:text-xl text-white/35 max-w-2xl mx-auto leading-relaxed font-light animate-in fade-in slide-in-from-bottom-8 duration-1000 delay-300"
		>
			Blending the magic of the arcade era with the power of modern game
			engines.
		</p>

		<div
			class="flex flex-col sm:flex-row items-center justify-center gap-5 pt-8 animate-in fade-in slide-in-from-bottom-8 duration-1000 delay-500"
		>
			<Button
				size="lg"
				class="h-13 px-10 rounded-full bg-white text-black hover:bg-gray-100 font-bold text-sm tracking-wide transition-all hover:scale-[1.03] shadow-lg shadow-white/10"
			>
				START GAME
			</Button>
			<Button
				variant="ghost"
				size="lg"
				class="h-13 px-10 rounded-full text-white/50 hover:text-white hover:bg-white/5 border border-white/[0.06] hover:border-white/20 transition-all"
			>
				WATCH TRAILER
			</Button>
		</div>
	</div>

	<!-- Scroll indicator -->
	<div class="absolute bottom-10 left-1/2 -translate-x-1/2 animate-bounce">
		<div class="w-5 h-8 rounded-full border border-white/20 flex items-start justify-center pt-1.5">
			<div class="w-1 h-2 rounded-full bg-white/40"></div>
		</div>
	</div>
</section>

<!-- Selected Work (Bento Grid) -->
<section id="work" class="py-32 relative">
	<div class="container mx-auto px-6">
		<div class="mb-16 space-y-3">
			<span class="text-xs font-bold text-blue-400/80 tracking-widest uppercase">Portfolio</span>
			<h2
				class="text-4xl md:text-5xl font-heading font-bold text-white"
			>
				OUR GAME
			</h2>
			<p class="text-white/35">
				Pushing the boundaries of real-time performance.
			</p>
		</div>

		<div
			class="glass-modern rounded-2xl overflow-hidden relative group cursor-pointer glow-hover h-[500px] md:h-[560px]"
		>
			<div
				class="absolute inset-0 bg-gradient-to-t from-black/90 via-black/20 to-transparent z-10"
			></div>
			<div
				class="absolute inset-0 bg-cover bg-center group-hover:scale-105 transition-transform duration-700 ease-out"
				style="background-image: url('/isle-of-infection.png');"
			></div>

			<div class="absolute bottom-0 left-0 p-10 z-20 w-full">
				<div class="flex justify-between items-end">
					<div class="space-y-2">
						<span
							class="text-green-400 text-[11px] font-bold tracking-widest uppercase mb-2 block"
							>Our Latest Game</span
						>
						<h3
							class="text-3xl md:text-5xl font-heading font-bold text-white"
						>
							Isle of Infection
						</h3>
						<p class="text-white/50 max-w-lg text-sm md:text-base">
							A survival horror experience where every step could be your last. Built in Unity.
						</p>
					</div>
					<div
						class="w-12 h-12 rounded-full bg-white text-black flex items-center justify-center opacity-0 group-hover:opacity-100 transition-all translate-y-4 group-hover:translate-y-0 shrink-0"
					>
						<ArrowRight class="w-5 h-5" />
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Team Section -->
<section id="team" class="py-32 border-t border-white/[0.04] relative overflow-hidden">
	<div class="absolute inset-0 bg-gradient-to-b from-transparent via-blue-500/[0.02] to-transparent pointer-events-none"></div>
	<div class="container mx-auto px-6 relative z-10">
		<div class="text-center mb-20 space-y-3">
			<span class="text-xs font-bold text-blue-400/80 tracking-widest uppercase">The People</span>
			<h2 class="text-4xl md:text-5xl font-heading font-bold text-white">
				MEET THE TEAM
			</h2>
			<p class="text-white/35 max-w-lg mx-auto">
				The creative minds behind every pixel and every line of code.
			</p>
		</div>

		<div class="grid grid-cols-2 md:grid-cols-4 gap-5 md:gap-6 max-w-5xl mx-auto">
			{#each team as member, i}
				<div class="group cursor-pointer">
					<div class="relative overflow-hidden rounded-2xl aspect-[3/4] mb-4">
						<img
							src={member.image}
							alt={member.name}
							class="w-full h-full object-cover object-top group-hover:scale-105 transition-transform duration-700 ease-out"
						/>
						<div class="absolute inset-0 bg-gradient-to-t from-black/70 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
					</div>
					<div class="space-y-0.5 px-1">
						<h4 class="text-white font-bold text-sm group-hover:text-white/90 transition-colors">{member.name}</h4>
						<p class="text-white/30 text-xs">{member.role}</p>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- Studio Stats / Info -->
<section id="studio" class="py-32 border-t border-white/[0.04] bg-black/40">
	<div class="container mx-auto px-6">
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-20 items-center">
			<div class="space-y-8">
				<div class="space-y-3">
					<span class="text-xs font-bold text-blue-400/80 tracking-widest uppercase">About Us</span>
					<h2
						class="text-4xl md:text-5xl font-heading font-bold text-white leading-tight"
					>
						ENGINEERING <br /> THE IMPOSSIBLE
					</h2>
				</div>
				<p class="text-lg text-white/50 leading-relaxed font-light">
					Rewind Studios is a collective of engineers, artists, and
					designers obsessed with fidelity. We don't just use engines;
					we master them. Our mission is to blur the line between
					cinema and gameplay.
				</p>
				<div class="grid grid-cols-2 gap-8 pt-4">
					<div class="space-y-1">
						<div class="text-4xl font-bold text-white">
							1<span class="text-blue-400"></span>
						</div>
						<div
							class="text-xs text-white/30 uppercase tracking-wider"
						>
							Projects Shipped
						</div>
					</div>
					<div class="space-y-1">
						<div class="text-4xl font-bold text-white">
								1<span class="text-blue-400"></span>
						</div>
						<div
							class="text-xs text-white/30 uppercase tracking-wider"
						>
							Unique Players
						</div>
					</div>
				</div>
			</div>

			<div class="grid grid-cols-1 gap-3">
				<div
					class="glass-modern p-7 rounded-xl flex items-center gap-5 group hover:bg-white/[0.04] transition-all duration-300"
				>
					<div class="w-10 h-10 rounded-lg bg-blue-500/10 flex items-center justify-center shrink-0">
						<Box class="w-5 h-5 text-blue-400" />
					</div>
					<div>
						<h4 class="text-white font-bold text-sm mb-0.5">Unity Experts</h4>
						<p class="text-white/35 text-xs">
							Custom shaders and pipelines for maximum fidelity.
						</p>
					</div>
				</div>
				<div
					class="glass-modern p-7 rounded-xl flex items-center gap-5 group hover:bg-white/[0.04] transition-all duration-300"
				>
					<div class="w-10 h-10 rounded-lg bg-purple-500/10 flex items-center justify-center shrink-0">
						<Globe class="w-5 h-5 text-purple-400" />
					</div>
					<div>
						<h4 class="text-white font-bold text-sm mb-0.5">
							Cross Platform
						</h4>
						<p class="text-white/35 text-xs">
							Seamless experiences across PC, Console, and Mobile.
						</p>
					</div>
				</div>
				<div
					class="glass-modern p-7 rounded-xl flex items-center gap-5 group hover:bg-white/[0.04] transition-all duration-300"
				>
					<div class="w-10 h-10 rounded-lg bg-green-500/10 flex items-center justify-center shrink-0">
						<Code class="w-5 h-5 text-green-400" />
					</div>
					<div>
						<h4 class="text-white font-bold text-sm mb-0.5">Open Source</h4>
						<p class="text-white/35 text-xs">
							Contributing back to the ecosystem we love.
						</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Minimal Footer -->
<footer class="py-16 border-t border-white/[0.04]">
	<div class="container mx-auto px-6">
		<div class="flex flex-col md:flex-row justify-between gap-12">
			<div class="space-y-4 max-w-sm">
				<div class="flex items-center gap-3 mb-2">
					<RewindLogo class="w-7 h-7 text-white" />
					<h3 class="font-heading font-bold text-xl text-white">
						REWIND STUDIOS
					</h3>
				</div>
				<p class="text-white/30 font-light text-sm">
					Building the future of interactive entertainment for every
					screen.
				</p>
			</div>

			<div class="flex gap-12 md:gap-20">
				<div class="space-y-3">
					<h4
						class="text-[11px] font-bold text-white/50 uppercase tracking-widest"
					>
						Sitemap
					</h4>
					<ul class="space-y-2 text-sm text-white/30">
						<li>
							<a
								href="#work"
								class="hover:text-white transition-colors"
								>Work</a
							>
						</li>
						<li>
							<a
								href="#team"
								class="hover:text-white transition-colors"
								>Team</a
							>
						</li>
						<li>
							<a
								href="#studio"
								class="hover:text-white transition-colors"
								>Studio</a
							>
						</li>
					</ul>
				</div>
				<div class="space-y-3">
					<h4
						class="text-[11px] font-bold text-white/50 uppercase tracking-widest"
					>
						Connect
					</h4>
					<ul class="space-y-2 text-sm text-white/30">
						<li>
							<a
								href="#"
								class="hover:text-white transition-colors"
								>Twitter / X</a
							>
						</li>
						<li>
							<a
								href="#"
								class="hover:text-white transition-colors"
								>GitHub</a
							>
						</li>
						<li>
							<a
								href="#"
								class="hover:text-white transition-colors"
								>LinkedIn</a
							>
						</li>
					</ul>
				</div>
			</div>
		</div>

		<div
			class="mt-16 pt-6 border-t border-white/[0.04] flex flex-col md:flex-row justify-between items-center gap-6 text-xs text-white/15"
		>
			<p>&copy; 2026 Rewind Studios. All rights reserved.</p>
			<div class="flex gap-8">
				<a href="#" class="hover:text-white/40 transition-colors">Privacy Policy</a>
				<a href="#" class="hover:text-white/40 transition-colors">Terms of Service</a>
			</div>
		</div>
	</div>
</footer>
