<script lang="ts">
    import { onMount } from "svelte";

    let canvas: HTMLCanvasElement;

    onMount(() => {
        const ctx = canvas.getContext("2d");
        if (!ctx) return;

        let width = (canvas.width = canvas.offsetWidth);
        let height = (canvas.height = canvas.offsetHeight);

        let stars: {
            x: number;
            y: number;
            size: number;
            opacity: number;
            speed: number;
        }[] = [];
        const STAR_COUNT = 200;

        function initStars() {
            stars = [];
            for (let i = 0; i < STAR_COUNT; i++) {
                stars.push({
                    x: Math.random() * width,
                    y: Math.random() * height,
                    size: Math.random() * 1.5,
                    opacity: Math.random(),
                    speed: Math.random() * 0.05 + 0.01,
                });
            }
        }

        function animate() {
            if (!ctx) return;
            ctx.clearRect(0, 0, width, height);

            // Draw Nebula (Subtle Gradients)
            const gradient = ctx.createRadialGradient(
                width / 2,
                height / 2,
                0,
                width / 2,
                height / 2,
                width,
            );
            gradient.addColorStop(0, "rgba(59, 130, 246, 0.05)"); // Blue core
            gradient.addColorStop(0.5, "rgba(147, 51, 234, 0.02)"); // Purple mid
            gradient.addColorStop(1, "transparent");
            ctx.fillStyle = gradient;
            ctx.fillRect(0, 0, width, height);

            // Draw Stars
            ctx.fillStyle = "white";
            stars.forEach((star) => {
                ctx.globalAlpha = star.opacity;
                ctx.beginPath();
                ctx.arc(star.x, star.y, star.size, 0, Math.PI * 2);
                ctx.fill();

                // Move stars slowly
                star.y -= star.speed;
                // Reset if moved off screen
                if (star.y < 0) {
                    star.y = height;
                    star.x = Math.random() * width;
                }
            });
            ctx.globalAlpha = 1;

            requestAnimationFrame(animate);
        }

        const handleResize = () => {
            width = canvas.width = canvas.offsetWidth;
            height = canvas.height = canvas.offsetHeight;
            initStars();
        };

        window.addEventListener("resize", handleResize);
        initStars();
        animate();

        return () => window.removeEventListener("resize", handleResize);
    });
</script>

<canvas
    bind:this={canvas}
    class="absolute inset-0 w-full h-full pointer-events-none z-0 mix-blend-screen"
></canvas>
