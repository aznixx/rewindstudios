<script lang="ts">
    import { cn } from "$lib/utils";
    let { class: className, ...props } = $props();
</script>

<svg
    xmlns="http://www.w3.org/2000/svg"
    viewBox="0 0 24 24"
    fill="none"
    stroke="currentColor"
    stroke-width="1.5"
    stroke-linecap="round"
    stroke-linejoin="round"
    class={cn("w-10 h-10", className)}
    {...props}
>
    <!-- Perfect Hexagon -->
    <path
        d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"
    />

    <!-- Rewind Triangles (Centered & Sharp) -->
    <!-- First triangle -->
    <polygon
        points="11 12 15 9 15 15 11 12"
        fill="currentColor"
        stroke="none"
    />
    <!-- Second triangle -->
    <polygon points="7 12 11 9 11 15 7 12" fill="currentColor" stroke="none" />
</svg>
