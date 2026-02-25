<script lang="ts">
	import { Button } from "$lib/components/ui/button";
	import {
		ArrowRight,
		Box,
		Code,
		Hexagon,
		Globe,
		Layers,
	} from "lucide-svelte";
	import RewindLogo from "$lib/components/ui/RewindLogo.svelte";
	import MilkyWay from "$lib/components/ui/MilkyWay.svelte";

	// Clean Professional Version
</script>

<!-- Navigation -->
<nav
	class="fixed top-0 w-full z-50 transition-all duration-300 bg-gradient-to-b from-black/80 to-transparent backdrop-blur-[2px]"
>
	<div class="container mx-auto px-6 h-24 flex items-center justify-between">
		<a href="/" class="flex items-center gap-3 group">
			<div
				class="w-10 h-10 rounded-xl bg-white/5 border border-white/10 flex items-center justify-center group-hover:bg-white/10 group-hover:scale-105 transition-all duration-300 shadow-lg shadow-black/20"
			>
				<RewindLogo class="w-5 h-5 text-white" />
			</div>
			<span
				class="font-heading font-bold text-lg tracking-tight text-white group-hover:text-white/90 transition-colors"
				>REWIND <span class="text-white/30 font-light">STUDIOS</span
				></span
			>
		</a>

		<div
			class="hidden md:flex items-center gap-10 bg-black/20 backdrop-blur-md px-8 py-3 rounded-full border border-white/5"
		>
			<a
				href="#work"
				class="nav-link text-sm font-medium text-white/50 hover:text-white transition-colors"
				>Work</a
			>
			<div class="w-1 h-1 rounded-full bg-white/10"></div>
			<a
				href="#studio"
				class="nav-link text-sm font-medium text-white/50 hover:text-white transition-colors"
				>Studio</a
			>
		</div>

		<Button
			variant="ghost"
			class="hidden sm:flex hover:bg-white text-white hover:text-black transition-all rounded-full px-6 font-medium text-sm h-11 border border-white/10 hover:border-white"
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
		<h1
			class="text-6xl md:text-8xl lg:text-9xl font-heading font-bold tracking-tighter text-white max-w-6xl mx-auto leading-[0.85] animate-in fade-in zoom-in-95 duration-1000 delay-200 drop-shadow-2xl"
		>
			RELIVE THE <br class="hidden md:block" />
			<span class="text-gold-shine">GOLDEN AGE</span>
		</h1>

		<p
			class="text-lg md:text-xl text-white/40 max-w-2xl mx-auto leading-relaxed font-light animate-in fade-in slide-in-from-bottom-8 duration-1000 delay-300"
		>
			Blending the magic of the arcade era with the power of modern game
			engines.
		</p>

		<div
			class="flex flex-col sm:flex-row items-center justify-center gap-6 pt-8 animate-in fade-in slide-in-from-bottom-8 duration-1000 delay-500"
		>
			<Button
				size="lg"
				class="h-14 px-10 rounded-full bg-white text-black hover:bg-gray-200 font-bold text-sm tracking-wide transition-all hover:scale-105"
			>
				START GAME
			</Button>
			<Button
				variant="ghost"
				size="lg"
				class="h-14 px-10 rounded-full text-white/60 hover:text-white hover:bg-white/5 border border-white/5 hover:border-white/20 transition-all"
			>
				WATCH TRAILER
			</Button>
		</div>
	</div>
</section>

<!-- Selected Work (Bento Grid) -->
<section id="work" class="py-32 relative">
	<div class="container mx-auto px-6">
		<div
			class="flex flex-col md:flex-row justify-between items-end mb-16 gap-6"
		>
			<div class="space-y-2">
				<h2
					class="text-4xl md:text-5xl font-heading font-bold text-white"
				>
					SELECTED WORK
				</h2>
				<p class="text-white/40">
					Pushing the boundaries of real-time performance.
				</p>
			</div>
			<a
				href="/archive"
				class="text-white text-sm border-b border-white/20 pb-1 hover:border-white transition-all"
				>View Archive</a
			>
		</div>

		<div class="grid grid-cols-1 md:grid-cols-3 gap-6 auto-rows-[500px]">
			<!-- Project 1 (Large) -->
			<div
				class="md:col-span-2 glass-modern rounded-3xl overflow-hidden relative group cursor-pointer glow-hover"
			>
				<div
					class="absolute inset-0 bg-gradient-to-t from-black/80 via-transparent to-transparent z-10"
				></div>
				<div
					class="absolute inset-0 bg-cover bg-center group-hover:scale-105 transition-transform duration-700"
					style="background-image: url('/pocket-physics.jpg');"
				></div>

				<div class="absolute bottom-0 left-0 p-10 z-20 w-full">
					<div class="flex justify-between items-end">
						<div class="space-y-2">
							<span
								class="text-blue-400 text-xs font-bold tracking-widest uppercase mb-2 block"
								>Available Now</span
							>
							<h3
								class="text-4xl font-heading font-bold text-white"
							>
								Pocket Physics
							</h3>
							<p class="text-white/60 max-w-md">
								A real-time fluid simulation engine running
								entirely in Unity. Featured on Awwwards.
							</p>
						</div>
						<div
							class="w-12 h-12 rounded-full bg-white text-black flex items-center justify-center opacity-0 group-hover:opacity-100 transition-all translate-y-4 group-hover:translate-y-0"
						>
							<ArrowRight class="w-5 h-5" />
						</div>
					</div>
				</div>
			</div>

			<!-- Project 2 (Vertical) -->
			<div
				class="glass-modern rounded-3xl overflow-hidden relative group cursor-pointer glow-hover"
			>
				<div
					class="absolute inset-0 bg-gradient-to-t from-black/80 to-transparent z-10"
				></div>
				<div
					class="absolute inset-0 bg-neutral-800 group-hover:scale-105 transition-transform duration-700"
				></div>

				<div class="absolute bottom-0 left-0 p-8 z-20">
					<h3 class="text-2xl font-bold text-white mb-1">
						Neon Drift
					</h3>
					<p class="text-white/50 text-sm">Procedural Racing Sim</p>
				</div>
			</div>

			<!-- Project 3 -->
			<div
				class="glass-modern rounded-3xl overflow-hidden relative group cursor-pointer glow-hover"
			>
				<div
					class="absolute inset-0 bg-gradient-to-t from-black/80 to-transparent z-10"
				></div>
				<div
					class="absolute inset-0 bg-neutral-800 group-hover:scale-105 transition-transform duration-700"
				></div>

				<div class="absolute bottom-0 left-0 p-8 z-20">
					<h3 class="text-2xl font-bold text-white mb-1">
						Dungeon Flip
					</h3>
					<p class="text-white/50 text-sm">Rogue-lite Strategy</p>
				</div>
			</div>

			<!-- Project 4 (Wide) -->
			<div
				class="md:col-span-2 glass-modern rounded-3xl overflow-hidden relative group cursor-pointer glow-hover flex items-center justify-center"
			>
				<div class="text-center space-y-4 relative z-10">
					<div
						class="w-16 h-16 rounded-2xl bg-white/5 border border-white/10 mx-auto flex items-center justify-center"
					>
						<Layers class="w-8 h-8 text-white/40" />
					</div>
					<h3 class="text-xl font-medium text-white/40">
						More Projects Coming Soon
					</h3>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Studio Stats / Info -->
<section id="studio" class="py-32 border-t border-white/5 bg-black/40">
	<div class="container mx-auto px-6">
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-20 items-center">
			<div class="space-y-8">
				<h2
					class="text-4xl md:text-5xl font-heading font-bold text-white leading-tight"
				>
					ENGINEERING <br /> THE IMPOSSIBLE
				</h2>
				<p class="text-lg text-white/60 leading-relaxed font-light">
					Rewind Studios is a collective of engineers, artists, and
					designers obsessed with fidelity. We don't just use engines;
					we master them. Our mission is to blur the line between
					cinema and gameplay.
				</p>
				<div class="grid grid-cols-2 gap-8 pt-8">
					<div>
						<div class="text-4xl font-bold text-white mb-2">
							60<span class="text-blue-500">+</span>
						</div>
						<div
							class="text-sm text-white/40 uppercase tracking-wide"
						>
							Projects Shipped
						</div>
					</div>
					<div>
						<div class="text-4xl font-bold text-white mb-2">
							12M<span class="text-blue-500">+</span>
						</div>
						<div
							class="text-sm text-white/40 uppercase tracking-wide"
						>
							Unique Players
						</div>
					</div>
				</div>
			</div>

			<div class="grid grid-cols-1 gap-4">
				<div
					class="glass-modern p-8 rounded-2xl flex items-center gap-6"
				>
					<Box class="w-8 h-8 text-blue-500" />
					<div>
						<h4 class="text-white font-bold mb-1">Unity Experts</h4>
						<p class="text-white/40 text-sm">
							Custom shaders and pipelines for maximum fidelity.
						</p>
					</div>
				</div>
				<div
					class="glass-modern p-8 rounded-2xl flex items-center gap-6"
				>
					<Globe class="w-8 h-8 text-purple-500" />
					<div>
						<h4 class="text-white font-bold mb-1">
							Cross Platform
						</h4>
						<p class="text-white/40 text-sm">
							Seamless experiences across PC, Console, and Mobile.
						</p>
					</div>
				</div>
				<div
					class="glass-modern p-8 rounded-2xl flex items-center gap-6"
				>
					<Code class="w-8 h-8 text-green-500" />
					<div>
						<h4 class="text-white font-bold mb-1">Open Source</h4>
						<p class="text-white/40 text-sm">
							Contributing back to the ecosystem we love.
						</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Minimal Footer -->
<footer class="py-20 border-t border-white/5">
	<div class="container mx-auto px-6">
		<div class="flex flex-col md:flex-row justify-between gap-12">
			<div class="space-y-4 max-w-sm">
				<div class="flex items-center gap-3 mb-2">
					<RewindLogo class="w-8 h-8 text-white" />
					<h3 class="font-heading font-bold text-2xl text-white">
						REWIND STUDIOS
					</h3>
				</div>
				<p class="text-white/40 font-light">
					Building the future of interactive entertainment for every
					screen.
				</p>
			</div>

			<div class="flex gap-12 md:gap-24">
				<div class="space-y-4">
					<h4
						class="text-xs font-bold text-white uppercase tracking-widest"
					>
						Sitemap
					</h4>
					<ul class="space-y-2 text-sm text-white/60">
						<li>
							<a
								href="#"
								class="hover:text-white transition-colors"
								>Work</a
							>
						</li>
						<li>
							<a
								href="#"
								class="hover:text-white transition-colors"
								>Studio</a
							>
						</li>
					</ul>
				</div>
				<div class="space-y-4">
					<h4
						class="text-xs font-bold text-white uppercase tracking-widest"
					>
						Connect
					</h4>
					<ul class="space-y-2 text-sm text-white/60">
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
			class="mt-20 pt-8 border-t border-white/5 flex flex-col md:flex-row justify-between items-center gap-6 text-xs text-white/20"
		>
			<p>&copy; 2026 Rewind Studios. All rights reserved.</p>
			<div class="flex gap-8">
				<a href="#">Privacy Policy</a>
				<a href="#">Terms of Service</a>
			</div>
		</div>
	</div>
</footer>
