<html lang="en"><head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=0.85">
    <title>01030401017</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: "#1e40af",
                        secondary: "#f59e0b",
                        accent: "#ef4444",
                        light: "#f9fafb",
                        dark: "#1f2937"
                    }
                }
            }
        }
    </script>
    <style>
        @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap");
        body { font-family: "Poppins", sans-serif; scroll-behavior: smooth; }
        .hero-bg {
            background: linear-gradient(rgba(0,0,0,0.7),rgba(0,0,0,0.7)),
                        url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='100' height='100' viewBox='0 0 100 100'><rect width='100' height='100' fill='%231e40af'/><path d='M0 0L100 100M100 0L0 100' stroke='%233b82f6' stroke-width='0.85'/></svg>");
            background-size: cover; background-position: center;
        }
        .fade-in { animation: fadeIn 1s ease-in; }
        @keyframes fadeIn { from{opacity:0;transform:translateY(20px)} to{opacity:1;transform:translateY(0)} }
        .feature-card:hover { transform: translateY(-10px); box-shadow: 0 20px 25px -5px rgba(0,0,0,.1),0 10px 10px -5px rgba(0,0,0,.04); }
        .nav-link:hover { color:#f59e0b; transition:all .3s ease; }
        .btn-primary { background: linear-gradient(to right,#1e40af,#3b82f6); transition:all .3s ease; }
        .btn-primary:hover { transform:translateY(-3px); box-shadow:0 10px 15px -3px rgba(30,64,175,.3); }

        /* ── Dashboard overlay ── */
        #dashboard-overlay {
            display: none;
            position: fixed; inset: 0; z-index: 100;
            background: #f0f0f0;
            flex-direction: column;
        }
        #dashboard-overlay.active { display: flex; }
        #dashboard-topbar {
            display: flex; align-items: center; gap: 10px;
            background: #1e40af; color: yellow;
            padding: 8px 16px; flex-shrink: 0;
        }
        #dashboard-topbar button {
            background: rgba(255,255,255,.15); border: none; color: white;
            padding: 5px 14px; border-radius: 20px; cursor: pointer;
            font-size: 10px; display:flex; align-items:center; gap:5px;
        }
        #dashboard-topbar button:hover { background: rgba(255,255,255,.3); }
        #dashboard-body {
            flex: 1; overflow-y: auto; padding: 8px;
        }
        /* dashboard tab styles (scoped) */
        #dashboard-body .tabs { display:flex; gap:4px; margin-bottom:4px; flex-wrap:nowrap; }
        #dashboard-body .tab-btn {
            padding:4px 10px; cursor:pointer; border:1px solid #666; border-radius:10px;
            background:#fff; user-select:none; font-size:13px;
        }
        #dashboard-body .tab-btn.active { background:#3b82f6; color:white; border-color:#2563eb; }
        #dashboard-body iframe {
            width:99%; height:calc(100vh - 100px);
            border:.5px solid #ccc; border-radius:10px; background:white;
        }
    </style>
<style>
  *, ::before, ::after{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }::backdrop{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }/* ! tailwindcss v3.4.17 | MIT License | https://tailwindcss.com */*,::after,::before{box-sizing:border-box;border-width:0;border-style:solid;border-color:#e5e7eb}::after,::before{--tw-content:''}:host,html{line-height:1.5;-webkit-text-size-adjust:100%;-moz-tab-size:4;tab-size:4;font-family:ui-sans-serif, system-ui, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";font-feature-settings:normal;font-variation-settings:normal;-webkit-tap-highlight-color:transparent}body{margin:0;line-height:inherit}hr{height:0;color:inherit;border-top-width:1px}abbr:where([title]){-webkit-text-decoration:underline dotted;text-decoration:underline dotted}h1,h2,h3,h4,h5,h6{font-size:inherit;font-weight:inherit}a{color:inherit;text-decoration:inherit}b,strong{font-weight:bolder}code,kbd,pre,samp{font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;font-feature-settings:normal;font-variation-settings:normal;font-size:1em}small{font-size:80%}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}sub{bottom:-.25em}sup{top:-.5em}table{text-indent:0;border-color:inherit;border-collapse:collapse}button,input,optgroup,select,textarea{font-family:inherit;font-feature-settings:inherit;font-variation-settings:inherit;font-size:100%;font-weight:inherit;line-height:inherit;letter-spacing:inherit;color:inherit;margin:0;padding:0}button,select{text-transform:none}button,input:where([type=button]),input:where([type=reset]),input:where([type=submit]){-webkit-appearance:button;background-color:transparent;background-image:none}:-moz-focusring{outline:auto}:-moz-ui-invalid{box-shadow:none}progress{vertical-align:baseline}::-webkit-inner-spin-button,::-webkit-outer-spin-button{height:auto}[type=search]{-webkit-appearance:textfield;outline-offset:-2px}::-webkit-search-decoration{-webkit-appearance:none}::-webkit-file-upload-button{-webkit-appearance:button;font:inherit}summary{display:list-item}blockquote,dd,dl,figure,h1,h2,h3,h4,h5,h6,hr,p,pre{margin:0}fieldset{margin:0;padding:0}legend{padding:0}menu,ol,ul{list-style:none;margin:0;padding:0}dialog{padding:0}textarea{resize:vertical}input::placeholder,textarea::placeholder{opacity:1;color:#9ca3af}[role=button],button{cursor:pointer}:disabled{cursor:default}audio,canvas,embed,iframe,img,object,svg,video{display:block;vertical-align:middle}img,video{max-width:100%;height:auto}[hidden]:where(:not([hidden=until-found])){display:none}.fixed{position:fixed}.z-50{z-index:50}.mx-auto{margin-left:auto;margin-right:auto}.mb-16{margin-bottom:4rem}.mb-2{margin-bottom:0.5rem}.mb-3{margin-bottom:0.75rem}.mb-4{margin-bottom:1rem}.mb-6{margin-bottom:1.5rem}.mb-8{margin-bottom:2rem}.ml-2{margin-left:0.5rem}.ml-4{margin-left:1rem}.mr-2{margin-right:0.5rem}.mt-12{margin-top:3rem}.mt-2{margin-top:0.5rem}.mt-4{margin-top:1rem}.mt-8{margin-top:2rem}.block{display:block}.flex{display:flex}.grid{display:grid}.hidden{display:none}.h-1{height:0.25rem}.h-12{height:3rem}.h-16{height:4rem}.h-screen{height:100vh}.w-12{width:3rem}.w-20{width:5rem}.w-full{width:100%}.max-w-2xl{max-width:42rem}.max-w-7xl{max-width:80rem}.flex-shrink-0{flex-shrink:0}.grid-cols-1{grid-template-columns:repeat(1, minmax(0, 1fr))}.grid-cols-2{grid-template-columns:repeat(2, minmax(0, 1fr))}.flex-col{flex-direction:column}.items-center{align-items:center}.justify-center{justify-content:center}.justify-between{justify-content:space-between}.gap-12{gap:3rem}.gap-2{gap:0.5rem}.gap-4{gap:1rem}.gap-8{gap:2rem}.space-x-4 > :not([hidden]) ~ :not([hidden]){--tw-space-x-reverse:0;margin-right:calc(1rem * var(--tw-space-x-reverse));margin-left:calc(1rem * calc(1 - var(--tw-space-x-reverse)))}.space-x-6 > :not([hidden]) ~ :not([hidden]){--tw-space-x-reverse:0;margin-right:calc(1.5rem * var(--tw-space-x-reverse));margin-left:calc(1.5rem * calc(1 - var(--tw-space-x-reverse)))}.space-y-1 > :not([hidden]) ~ :not([hidden]){--tw-space-y-reverse:0;margin-top:calc(0.25rem * calc(1 - var(--tw-space-y-reverse)));margin-bottom:calc(0.25rem * var(--tw-space-y-reverse))}.space-y-2 > :not([hidden]) ~ :not([hidden]){--tw-space-y-reverse:0;margin-top:calc(0.5rem * calc(1 - var(--tw-space-y-reverse)));margin-bottom:calc(0.5rem * var(--tw-space-y-reverse))}.space-y-4 > :not([hidden]) ~ :not([hidden]){--tw-space-y-reverse:0;margin-top:calc(1rem * calc(1 - var(--tw-space-y-reverse)));margin-bottom:calc(1rem * var(--tw-space-y-reverse))}.space-y-6 > :not([hidden]) ~ :not([hidden]){--tw-space-y-reverse:0;margin-top:calc(1.5rem * calc(1 - var(--tw-space-y-reverse)));margin-bottom:calc(1.5rem * var(--tw-space-y-reverse))}.rounded-full{border-radius:9999px}.rounded-lg{border-radius:0.5rem}.rounded-md{border-radius:0.375rem}.rounded-xl{border-radius:0.75rem}.rounded-l-lg{border-top-left-radius:0.5rem;border-bottom-left-radius:0.5rem}.rounded-r-lg{border-top-right-radius:0.5rem;border-bottom-right-radius:0.5rem}.border{border-width:1px}.border-2{border-width:2px}.border-b{border-bottom-width:1px}.border-t{border-top-width:1px}.border-gray-100{--tw-border-opacity:1;border-color:rgb(243 244 246 / var(--tw-border-opacity, 1))}.border-gray-300{--tw-border-opacity:1;border-color:rgb(209 213 219 / var(--tw-border-opacity, 1))}.border-gray-800{--tw-border-opacity:1;border-color:rgb(31 41 55 / var(--tw-border-opacity, 1))}.border-white{--tw-border-opacity:1;border-color:rgb(255 255 255 / var(--tw-border-opacity, 1))}.bg-gray-50{--tw-bg-opacity:1;background-color:rgb(249 250 251 / var(--tw-bg-opacity, 1))}.bg-amber-500{--tw-bg-opacity:1;background-color:rgb(245 158 11 / var(--tw-bg-opacity, 1))}.bg-blue-50{--tw-bg-opacity:1;background-color:rgb(239 246 255 / var(--tw-bg-opacity, 1))}.bg-dark{--tw-bg-opacity:1;background-color:rgb(31 41 55 / var(--tw-bg-opacity, 1))}.bg-light{--tw-bg-opacity:1;background-color:rgb(249 250 251 / var(--tw-bg-opacity, 1))}.bg-primary{--tw-bg-opacity:1;background-color:rgb(30 64 175 / var(--tw-bg-opacity, 1))}.bg-secondary{--tw-bg-opacity:1;background-color:rgb(245 158 11 / var(--tw-bg-opacity, 1))}.bg-white{--tw-bg-opacity:1;background-color:rgb(255 255 255 / var(--tw-bg-opacity, 1))}.p-3{padding:0.75rem}.p-6{padding:1.5rem}.p-8{padding:2rem}.px-2{padding-left:0.5rem;padding-right:0.5rem}.px-3{padding-left:0.75rem;padding-right:0.75rem}.px-4{padding-left:1rem;padding-right:1rem}.px-8{padding-left:2rem;padding-right:2rem}.py-12{padding-top:3rem;padding-bottom:3rem}.py-2{padding-top:0.5rem;padding-bottom:0.5rem}.py-20{padding-top:5rem;padding-bottom:5rem}.py-3{padding-top:0.75rem;padding-bottom:0.75rem}.pb-3{padding-bottom:0.75rem}.pt-2{padding-top:0.5rem}.pt-8{padding-top:2rem}.text-left{text-align:left}.text-center{text-align:center}.text-xl{font-size:1.25rem;line-height:1.75rem}.text-2xl{font-size:1.5rem;line-height:2rem}.text-3xl{font-size:1.875rem;line-height:2.25rem}.text-4xl{font-size:2.25rem;line-height:2.5rem}.text-base{font-size:1rem;line-height:1.5rem}.text-lg{font-size:1.125rem;line-height:1.75rem}.text-sm{font-size:0.875rem;line-height:1.25rem}.text-xs{font-size:0.75rem;line-height:1rem}.font-bold{font-weight:700}.font-medium{font-weight:500}.font-semibold{font-weight:600}.leading-relaxed{line-height:1.625}.text-amber-400{--tw-text-opacity:1;color:rgb(251 191 36 / var(--tw-text-opacity, 1))}.text-amber-600{--tw-text-opacity:1;color:rgb(217 119 6 / var(--tw-text-opacity, 1))}.text-dark{--tw-text-opacity:1;color:rgb(31 41 55 / var(--tw-text-opacity, 1))}.text-gray-200{--tw-text-opacity:1;color:rgb(229 231 235 / var(--tw-text-opacity, 1))}.text-gray-400{--tw-text-opacity:1;color:rgb(156 163 175 / var(--tw-text-opacity, 1))}.text-gray-600{--tw-text-opacity:1;color:rgb(75 85 99 / var(--tw-text-opacity, 1))}.text-gray-700{--tw-text-opacity:1;color:rgb(55 65 81 / var(--tw-text-opacity, 1))}.text-primary{--tw-text-opacity:1;color:rgb(30 64 175 / var(--tw-text-opacity, 1))}.text-secondary{--tw-text-opacity:1;color:rgb(245 158 11 / var(--tw-text-opacity, 1))}.text-white{--tw-text-opacity:1;color:rgb(255 255 255 / var(--tw-text-opacity, 1))}.shadow-lg{--tw-shadow:0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 10px 15px -3px var(--tw-shadow-color), 0 4px 6px -4px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.shadow-xl{--tw-shadow:0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 20px 25px -5px var(--tw-shadow-color), 0 8px 10px -6px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.transition{transition-property:color, background-color, border-color, fill, stroke, opacity, box-shadow, transform, filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-timing-function:cubic-bezier(0.4, 0, 0.2, 1);transition-duration:150ms}.transition-all{transition-property:all;transition-timing-function:cubic-bezier(0.4, 0, 0.2, 1);transition-duration:150ms}.duration-300{transition-duration:300ms}.hover\:bg-amber-600:hover{--tw-bg-opacity:1;background-color:rgb(217 119 6 / var(--tw-bg-opacity, 1))}.hover\:bg-gray-100:hover{--tw-bg-opacity:1;background-color:rgb(243 244 246 / var(--tw-bg-opacity, 1))}.hover\:bg-secondary:hover{--tw-bg-opacity:1;background-color:rgb(245 158 11 / var(--tw-bg-opacity, 1))}.hover\:bg-white:hover{--tw-bg-opacity:1;background-color:rgb(255 255 255 / var(--tw-bg-opacity, 1))}.hover\:bg-yellow-500:hover{--tw-bg-opacity:1;background-color:rgb(234 179 8 / var(--tw-bg-opacity, 1))}.hover\:text-dark:hover{--tw-text-opacity:1;color:rgb(31 41 55 / var(--tw-text-opacity, 1))}.hover\:text-secondary:hover{--tw-text-opacity:1;color:rgb(245 158 11 / var(--tw-text-opacity, 1))}.focus\:border-transparent:focus{border-color:transparent}.focus\:outline-none:focus{outline:2px solid transparent;outline-offset:2px}.focus\:ring-2:focus{--tw-ring-offset-shadow:var(--tw-ring-inset) 0 0 0 var(--tw-ring-offset-width) var(--tw-ring-offset-color);--tw-ring-shadow:var(--tw-ring-inset) 0 0 0 calc(2px + var(--tw-ring-offset-width)) var(--tw-ring-color);box-shadow:var(--tw-ring-offset-shadow), var(--tw-ring-shadow), var(--tw-shadow, 0 0 #0000)}.focus\:ring-primary:focus{--tw-ring-opacity:1;--tw-ring-color:rgb(30 64 175 / var(--tw-ring-opacity, 1))}@media (min-width: 640px){.sm\:flex-row{flex-direction:row}.sm\:px-6{padding-left:1.5rem;padding-right:1.5rem}}@media (min-width: 768px){.md\:flex{display:flex}.md\:hidden{display:none}.md\:w-1\/2{width:50%}.md\:grid-cols-3{grid-template-columns:repeat(3, minmax(0, 1fr))}.md\:grid-cols-4{grid-template-columns:repeat(4, minmax(0, 1fr))}.md\:flex-row{flex-direction:row}.md\:text-2xl{font-size:1.5rem;line-height:2rem}.md\:text-4xl{font-size:2.25rem;line-height:2.5rem}.md\:text-6xl{font-size:3.75rem;line-height:1}}@media (min-width: 1024px){.lg\:grid-cols-2{grid-template-columns:repeat(2, minmax(0, 1fr))}.lg\:px-8{padding-left:2rem;padding-right:2rem}}</style><style>*, ::before, ::after{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }::backdrop{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }/* ! tailwindcss v3.4.17 | MIT License | https://tailwindcss.com */*,::after,::before{box-sizing:border-box;border-width:0;border-style:solid;border-color:#e5e7eb}::after,::before{--tw-content:''}:host,html{line-height:1.5;-webkit-text-size-adjust:100%;-moz-tab-size:4;tab-size:4;font-family:ui-sans-serif, system-ui, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";font-feature-settings:normal;font-variation-settings:normal;-webkit-tap-highlight-color:transparent}body{margin:0;line-height:inherit}hr{height:0;color:inherit;border-top-width:1px}abbr:where([title]){-webkit-text-decoration:underline dotted;text-decoration:underline dotted}h1,h2,h3,h4,h5,h6{font-size:inherit;font-weight:inherit}a{color:inherit;text-decoration:inherit}b,strong{font-weight:bolder}code,kbd,pre,samp{font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;font-feature-settings:normal;font-variation-settings:normal;font-size:1em}small{font-size:80%}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}sub{bottom:-.25em}sup{top:-.5em}table{text-indent:0;border-color:inherit;border-collapse:collapse}button,input,optgroup,select,textarea{font-family:inherit;font-feature-settings:inherit;font-variation-settings:inherit;font-size:100%;font-weight:inherit;line-height:inherit;letter-spacing:inherit;color:inherit;margin:0;padding:0}button,select{text-transform:none}button,input:where([type=button]),input:where([type=reset]),input:where([type=submit]){-webkit-appearance:button;background-color:transparent;background-image:none}:-moz-focusring{outline:auto}:-moz-ui-invalid{box-shadow:none}progress{vertical-align:baseline}::-webkit-inner-spin-button,::-webkit-outer-spin-button{height:auto}[type=search]{-webkit-appearance:textfield;outline-offset:-2px}::-webkit-search-decoration{-webkit-appearance:none}::-webkit-file-upload-button{-webkit-appearance:button;font:inherit}summary{display:list-item}blockquote,dd,dl,figure,h1,h2,h3,h4,h5,h6,hr,p,pre{margin:0}fieldset{margin:0;padding:0}legend{padding:0}menu,ol,ul{list-style:none;margin:0;padding:0}dialog{padding:0}textarea{resize:vertical}input::placeholder,textarea::placeholder{opacity:1;color:#9ca3af}[role=button],button{cursor:pointer}:disabled{cursor:default}audio,canvas,embed,iframe,img,object,svg,video{display:block;vertical-align:middle}img,video{max-width:100%;height:auto}[hidden]:where(:not([hidden=until-found])){display:none}.fixed{position:fixed}.z-50{z-index:50}.mx-auto{margin-left:auto;margin-right:auto}.mb-16{margin-bottom:4rem}.mb-2{margin-bottom:0.5rem}.mb-3{margin-bottom:0.75rem}.mb-4{margin-bottom:1rem}.mb-6{margin-bottom:1.5rem}.mb-8{margin-bottom:2rem}.ml-2{margin-left:0.5rem}.ml-4{margin-left:1rem}.mr-2{margin-right:0.5rem}.mt-12{margin-top:3rem}.mt-2{margin-top:0.5rem}.mt-4{margin-top:1rem}.mt-8{margin-top:2rem}.block{display:block}.flex{display:flex}.grid{display:grid}.hidden{display:none}.h-1{height:0.25rem}.h-12{height:3rem}.h-16{height:4rem}.h-screen{height:100vh}.w-12{width:3rem}.w-20{width:5rem}.w-full{width:100%}.max-w-2xl{max-width:42rem}.max-w-7xl{max-width:80rem}.flex-shrink-0{flex-shrink:0}.grid-cols-1{grid-template-columns:repeat(1, minmax(0, 1fr))}.grid-cols-2{grid-template-columns:repeat(2, minmax(0, 1fr))}.flex-col{flex-direction:column}.items-center{align-items:center}.justify-center{justify-content:center}.justify-between{justify-content:space-between}.gap-12{gap:3rem}.gap-2{gap:0.5rem}.gap-4{gap:1rem}.gap-8{gap:2rem}.space-x-4 > :not([hidden]) ~ :not([hidden]){--tw-space-x-reverse:0;margin-right:calc(1rem * var(--tw-space-x-reverse));margin-left:calc(1rem * calc(1 - var(--tw-space-x-reverse)))}.space-x-6 > :not([hidden]) ~ :not([hidden]){--tw-space-x-reverse:0;margin-right:calc(1.5rem * var(--tw-space-x-reverse));margin-left:calc(1.5rem * calc(1 - var(--tw-space-x-reverse)))}.space-y-1 > :not([hidden]) ~ :not([hidden]){--tw-space-y-reverse:0;margin-top:calc(0.25rem * calc(1 - var(--tw-space-y-reverse)));margin-bottom:calc(0.25rem * var(--tw-space-y-reverse))}.space-y-2 > :not([hidden]) ~ :not([hidden]){--tw-space-y-reverse:0;margin-top:calc(0.5rem * calc(1 - var(--tw-space-y-reverse)));margin-bottom:calc(0.5rem * var(--tw-space-y-reverse))}.space-y-4 > :not([hidden]) ~ :not([hidden]){--tw-space-y-reverse:0;margin-top:calc(1rem * calc(1 - var(--tw-space-y-reverse)));margin-bottom:calc(1rem * var(--tw-space-y-reverse))}.space-y-6 > :not([hidden]) ~ :not([hidden]){--tw-space-y-reverse:0;margin-top:calc(1.5rem * calc(1 - var(--tw-space-y-reverse)));margin-bottom:calc(1.5rem * var(--tw-space-y-reverse))}.rounded-full{border-radius:9999px}.rounded-lg{border-radius:0.5rem}.rounded-md{border-radius:0.375rem}.rounded-xl{border-radius:0.75rem}.rounded-l-lg{border-top-left-radius:0.5rem;border-bottom-left-radius:0.5rem}.rounded-r-lg{border-top-right-radius:0.5rem;border-bottom-right-radius:0.5rem}.border{border-width:1px}.border-2{border-width:2px}.border-b{border-bottom-width:1px}.border-t{border-top-width:1px}.border-gray-100{--tw-border-opacity:1;border-color:rgb(243 244 246 / var(--tw-border-opacity, 1))}.border-gray-300{--tw-border-opacity:1;border-color:rgb(209 213 219 / var(--tw-border-opacity, 1))}.border-gray-800{--tw-border-opacity:1;border-color:rgb(31 41 55 / var(--tw-border-opacity, 1))}.border-white{--tw-border-opacity:1;border-color:rgb(255 255 255 / var(--tw-border-opacity, 1))}.bg-gray-50{--tw-bg-opacity:1;background-color:rgb(249 250 251 / var(--tw-bg-opacity, 1))}.bg-amber-500{--tw-bg-opacity:1;background-color:rgb(245 158 11 / var(--tw-bg-opacity, 1))}.bg-blue-50{--tw-bg-opacity:1;background-color:rgb(239 246 255 / var(--tw-bg-opacity, 1))}.bg-dark{--tw-bg-opacity:1;background-color:rgb(31 41 55 / var(--tw-bg-opacity, 1))}.bg-light{--tw-bg-opacity:1;background-color:rgb(249 250 251 / var(--tw-bg-opacity, 1))}.bg-primary{--tw-bg-opacity:1;background-color:rgb(30 64 175 / var(--tw-bg-opacity, 1))}.bg-secondary{--tw-bg-opacity:1;background-color:rgb(245 158 11 / var(--tw-bg-opacity, 1))}.bg-white{--tw-bg-opacity:1;background-color:rgb(255 255 255 / var(--tw-bg-opacity, 1))}.p-3{padding:0.75rem}.p-6{padding:1.5rem}.p-8{padding:2rem}.px-2{padding-left:0.5rem;padding-right:0.5rem}.px-3{padding-left:0.75rem;padding-right:0.75rem}.px-4{padding-left:1rem;padding-right:1rem}.px-8{padding-left:2rem;padding-right:2rem}.py-12{padding-top:3rem;padding-bottom:3rem}.py-2{padding-top:0.5rem;padding-bottom:0.5rem}.py-20{padding-top:5rem;padding-bottom:5rem}.py-3{padding-top:0.75rem;padding-bottom:0.75rem}.pb-3{padding-bottom:0.75rem}.pt-2{padding-top:0.5rem}.pt-8{padding-top:2rem}.text-left{text-align:left}.text-center{text-align:center}.text-xl{font-size:1.25rem;line-height:1.75rem}.text-2xl{font-size:1.5rem;line-height:2rem}.text-3xl{font-size:1.875rem;line-height:2.25rem}.text-4xl{font-size:2.25rem;line-height:2.5rem}.text-base{font-size:1rem;line-height:1.5rem}.text-lg{font-size:1.125rem;line-height:1.75rem}.text-sm{font-size:0.875rem;line-height:1.25rem}.text-xs{font-size:0.75rem;line-height:1rem}.font-bold{font-weight:700}.font-medium{font-weight:500}.font-semibold{font-weight:600}.leading-relaxed{line-height:1.625}.text-amber-400{--tw-text-opacity:1;color:rgb(251 191 36 / var(--tw-text-opacity, 1))}.text-amber-600{--tw-text-opacity:1;color:rgb(217 119 6 / var(--tw-text-opacity, 1))}.text-dark{--tw-text-opacity:1;color:rgb(31 41 55 / var(--tw-text-opacity, 1))}.text-gray-200{--tw-text-opacity:1;color:rgb(229 231 235 / var(--tw-text-opacity, 1))}.text-gray-400{--tw-text-opacity:1;color:rgb(156 163 175 / var(--tw-text-opacity, 1))}.text-gray-600{--tw-text-opacity:1;color:rgb(75 85 99 / var(--tw-text-opacity, 1))}.text-gray-700{--tw-text-opacity:1;color:rgb(55 65 81 / var(--tw-text-opacity, 1))}.text-primary{--tw-text-opacity:1;color:rgb(30 64 175 / var(--tw-text-opacity, 1))}.text-secondary{--tw-text-opacity:1;color:rgb(245 158 11 / var(--tw-text-opacity, 1))}.text-white{--tw-text-opacity:1;color:rgb(255 255 255 / var(--tw-text-opacity, 1))}.shadow-lg{--tw-shadow:0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 10px 15px -3px var(--tw-shadow-color), 0 4px 6px -4px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.shadow-xl{--tw-shadow:0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 20px 25px -5px var(--tw-shadow-color), 0 8px 10px -6px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.transition{transition-property:color, background-color, border-color, fill, stroke, opacity, box-shadow, transform, filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-timing-function:cubic-bezier(0.4, 0, 0.2, 1);transition-duration:150ms}.transition-all{transition-property:all;transition-timing-function:cubic-bezier(0.4, 0, 0.2, 1);transition-duration:150ms}.duration-300{transition-duration:300ms}.hover\:bg-amber-600:hover{--tw-bg-opacity:1;background-color:rgb(217 119 6 / var(--tw-bg-opacity, 1))}.hover\:bg-gray-100:hover{--tw-bg-opacity:1;background-color:rgb(243 244 246 / var(--tw-bg-opacity, 1))}.hover\:bg-secondary:hover{--tw-bg-opacity:1;background-color:rgb(245 158 11 / var(--tw-bg-opacity, 1))}.hover\:bg-white:hover{--tw-bg-opacity:1;background-color:rgb(255 255 255 / var(--tw-bg-opacity, 1))}.hover\:bg-yellow-500:hover{--tw-bg-opacity:1;background-color:rgb(234 179 8 / var(--tw-bg-opacity, 1))}.hover\:text-dark:hover{--tw-text-opacity:1;color:rgb(31 41 55 / var(--tw-text-opacity, 1))}.hover\:text-secondary:hover{--tw-text-opacity:1;color:rgb(245 158 11 / var(--tw-text-opacity, 1))}.focus\:border-transparent:focus{border-color:transparent}.focus\:outline-none:focus{outline:2px solid transparent;outline-offset:2px}.focus\:ring-2:focus{--tw-ring-offset-shadow:var(--tw-ring-inset) 0 0 0 var(--tw-ring-offset-width) var(--tw-ring-offset-color);--tw-ring-shadow:var(--tw-ring-inset) 0 0 0 calc(2px + var(--tw-ring-offset-width)) var(--tw-ring-color);box-shadow:var(--tw-ring-offset-shadow), var(--tw-ring-shadow), var(--tw-shadow, 0 0 #0000)}.focus\:ring-primary:focus{--tw-ring-opacity:1;--tw-ring-color:rgb(30 64 175 / var(--tw-ring-opacity, 1))}@media (min-width: 640px){.sm\:flex-row{flex-direction:row}.sm\:px-6{padding-left:1.5rem;padding-right:1.5rem}}@media (min-width: 768px){.md\:flex{display:flex}.md\:hidden{display:none}.md\:w-1\/2{width:50%}.md\:grid-cols-3{grid-template-columns:repeat(3, minmax(0, 1fr))}.md\:grid-cols-4{grid-template-columns:repeat(4, minmax(0, 1fr))}.md\:flex-row{flex-direction:row}.md\:text-2xl{font-size:1.5rem;line-height:2rem}.md\:text-4xl{font-size:2.25rem;line-height:2.5rem}.md\:text-6xl{font-size:3.75rem;line-height:1}}@media (min-width: 1024px){.lg\:grid-cols-2{grid-template-columns:repeat(2, minmax(0, 1fr))}.lg\:px-8{padding-left:2rem;padding-right:2rem}}</style></head>

<body class="bg-gray-50">

    <!-- ══════════════ DASHBOARD OVERLAY ══════════════ -->
    <div id="dashboard-overlay">
        <div id="dashboard-topbar">
            <i class="fas fa-graduation-cap text-xl"></i>
            <span style="font-weight:700;font-size:15px;">Rauk Primary School · Dashboard</span>
            <span style="flex:1"></span>
            <button onclick="closeDashboard()">
                <i class="fas fa-arrow-left"></i> Back to Website
            </button>
        </div>
        <div id="dashboard-body">
<div class="tabs">
  <div class="tab-btn active" data-key="teacher" onclick="switchTpl(event)">👨‍🏫 ទិន្នន័យគ្រូ</div>
  <div class="tab-btn" data-key="attendance" onclick="switchTpl(event)">🔥 វត្តមាន</div>
  <div class="tab-btn" data-key="library" onclick="switchTpl(event)">🏠 បណ្ណាល័យ</div>
   <div class="tab-btn" data-key="datascores" onclick="switchTpl(event)">📊 គ្រប់គ្រងពិន្ទុ</div>
  <div class="tab-btn" data-key="dataclass" onclick="switchTpl(event)">🏫 ថ្នាក់រៀន</div>
</div>

<iframe id="iframe-teacher" style="display:block;"></iframe>
<iframe id="iframe-attendance" style="display:none;"></iframe>
<iframe id="iframe-library" style="display:none;"></iframe>
<iframe id="iframe-datascores" style="display:none;"></iframe>
<iframe id="iframe-dataclass" style="display:none;"></iframe>

<script>
  const CFG = {
    teacher:    { tplId: 'tpl-teacher' },
    attendance: { tplId: 'tpl-attendance' },
    library: { tplId: 'tpl-library' },
    datascores: { tplId: 'tpl-datascores' },
    dataclass:  { tplId: 'tpl-dataclass' }
  };

  function loadTpl(key) {
    const cfg = CFG[key];
    if (!cfg) return;
    const tpl = document.getElementById(cfg.tplId);
    if (!tpl) { alert('Template ' + cfg.tplId + ' not found'); return; }
    const blob = new Blob([tpl.innerHTML], { type: 'text/html;charset=utf-8' });
    const url  = URL.createObjectURL(blob);
    const iframe = document.getElementById('iframe-' + key);
    iframe.src = url;
    iframe.onload = () => URL.revokeObjectURL(url);
  }

  function switchTpl(e) {
    const key = e.currentTarget.dataset.key;
    document.querySelectorAll('.tab-btn').forEach(b =>
      b.classList.toggle('active', b.dataset.key === key)
    );
    Object.keys(CFG).forEach(k => {
      document.getElementById('iframe-' + k).style.display = (k === key) ? 'block' : 'none';
    });
    loadTpl(key);
  }

  loadTpl('teacher');
</script>

<template id="tpl-teacher">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=0.85">
    <title>សាលាបឋមសិក្សា រោគ - ប្រព័ន្ធគ្រប់គ្រង</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Khmer:wght@400;500;600;700&amp;display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body {
            font-family: 'Noto Sans Khmer', sans-serif;
        }
        .khmer-text {
            font-family: 'Noto Sans Khmer', sans-serif;
        }
        .gradient-bg {
            background: linear-gradient(135deg, #0b1628 0%, #111f35 100%);
        }
        .card {
            background-color: #111f35;
            border: 1px solid #1c3356;
            border-radius: 12px;
        }
        .tab-active {
            border-bottom: 2px solid #f59e0b !important;
            color: #f59e0b !important;
        }
        .kpi-card {
            background-color: #111f35;
            border: 1px solid #1c3356;
            border-radius: 12px;
            padding: 16px;
            display: flex;
            align-items: center;
            gap: 14px;
        }
        .chart-container {
            position: relative;
            height: 210px;
        }
        .progress-bar {
            height: 6px;
            border-radius: 4px;
        }
        .tag {
            background-color: rgba(37, 99, 235, 0.13);
            color: #2563eb;
            border: 1px solid rgba(37, 99, 235, 0.27);
            border-radius: 4px;
            padding: 1px 7px;
            font-size: 10px;
            font-weight: 700;
        }
        .tag-green {
            background-color: rgba(16, 185, 129, 0.13);
            color: #10b981;
            border: 1px solid rgba(16, 185, 129, 0.27);
        }
        .tag-red {
            background-color: rgba(239, 68, 68, 0.13);
            color: #ef4444;
            border: 1px solid rgba(239, 68, 68, 0.27);
        }
        .tag-orange {
            background-color: rgba(245, 158, 11, 0.13);
            color: #f59e0b;
            border: 1px solid rgba(245, 158, 11, 0.27);
        }
        .status-badge {
            border-radius: 4px;
            padding: 1px 6px;
            font-weight: 700;
            font-size: 10px;
        }
        .status-green {
            background-color: rgba(16, 185, 129, 0.13);
            color: #10b981;
        }
        .status-red {
            background-color: rgba(239, 68, 68, 0.13);
            color: #ef4444;
        }
        .status-orange {
            background-color: rgba(245, 158, 11, 0.13);
            color: #f59e0b;
        }
        .table-row:nth-child(even) {
            background-color: rgba(13, 31, 51, 0.05);
        }
        .table-row:hover {
            background-color: rgba(13, 31, 51, 0.1);
        }
    </style>
<style>
  *, ::before, ::after{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }::backdrop{--tw-border-spacing-x:0;--tw-border-spacing-y:0;--tw-translate-x:0;--tw-translate-y:0;--tw-rotate:0;--tw-skew-x:0;--tw-skew-y:0;--tw-scale-x:1;--tw-scale-y:1;--tw-pan-x: ;--tw-pan-y: ;--tw-pinch-zoom: ;--tw-scroll-snap-strictness:proximity;--tw-gradient-from-position: ;--tw-gradient-via-position: ;--tw-gradient-to-position: ;--tw-ordinal: ;--tw-slashed-zero: ;--tw-numeric-figure: ;--tw-numeric-spacing: ;--tw-numeric-fraction: ;--tw-ring-inset: ;--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgb(59 130 246 / 0.5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000;--tw-shadow-colored:0 0 #0000;--tw-blur: ;--tw-brightness: ;--tw-contrast: ;--tw-grayscale: ;--tw-hue-rotate: ;--tw-invert: ;--tw-saturate: ;--tw-sepia: ;--tw-drop-shadow: ;--tw-backdrop-blur: ;--tw-backdrop-brightness: ;--tw-backdrop-contrast: ;--tw-backdrop-grayscale: ;--tw-backdrop-hue-rotate: ;--tw-backdrop-invert: ;--tw-backdrop-opacity: ;--tw-backdrop-saturate: ;--tw-backdrop-sepia: ;--tw-contain-size: ;--tw-contain-layout: ;--tw-contain-paint: ;--tw-contain-style: }/* ! tailwindcss v3.4.17 | MIT License | https://tailwindcss.com */*,::after,::before{box-sizing:border-box;border-width:0;border-style:solid;border-color:#e5e7eb}::after,::before{--tw-content:''}:host,html{line-height:1.5;-webkit-text-size-adjust:100%;-moz-tab-size:4;tab-size:4;font-family:ui-sans-serif, system-ui, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";font-feature-settings:normal;font-variation-settings:normal;-webkit-tap-highlight-color:transparent}body{margin:0;line-height:inherit}hr{height:0;color:inherit;border-top-width:1px}abbr:where([title]){-webkit-text-decoration:underline dotted;text-decoration:underline dotted}h1,h2,h3,h4,h5,h6{font-size:inherit;font-weight:inherit}a{color:inherit;text-decoration:inherit}b,strong{font-weight:bolder}code,kbd,pre,samp{font-family:ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;font-feature-settings:normal;font-variation-settings:normal;font-size:1em}small{font-size:80%}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}sub{bottom:-.25em}sup{top:-.5em}table{text-indent:0;border-color:inherit;border-collapse:collapse}button,input,optgroup,select,textarea{font-family:inherit;font-feature-settings:inherit;font-variation-settings:inherit;font-size:100%;font-weight:inherit;line-height:inherit;letter-spacing:inherit;color:inherit;margin:0;padding:0}button,select{text-transform:none}button,input:where([type=button]),input:where([type=reset]),input:where([type=submit]){-webkit-appearance:button;background-color:transparent;background-image:none}:-moz-focusring{outline:auto}:-moz-ui-invalid{box-shadow:none}progress{vertical-align:baseline}::-webkit-inner-spin-button,::-webkit-outer-spin-button{height:auto}[type=search]{-webkit-appearance:textfield;outline-offset:-2px}::-webkit-search-decoration{-webkit-appearance:none}::-webkit-file-upload-button{-webkit-appearance:button;font:inherit}summary{display:list-item}blockquote,dd,dl,figure,h1,h2,h3,h4,h5,h6,hr,p,pre{margin:0}fieldset{margin:0;padding:0}legend{padding:0}menu,ol,ul{list-style:none;margin:0;padding:0}dialog{padding:0}textarea{resize:vertical}input::placeholder,textarea::placeholder{opacity:1;color:#9ca3af}[role=button],button{cursor:pointer}:disabled{cursor:default}audio,canvas,embed,iframe,img,object,svg,video{display:block;vertical-align:middle}img,video{max-width:100%;height:auto}[hidden]:where(:not([hidden=until-found])){display:none}.pointer-events-none{pointer-events:none}.absolute{position:absolute}.inset-0{inset:0px}.mx-auto{margin-left:auto;margin-right:auto}.mb-1{margin-bottom:0.25rem}.mb-2{margin-bottom:0.5rem}.mb-3{margin-bottom:0.75rem}.mb-4{margin-bottom:1rem}.mb-7{margin-bottom:1.75rem}.mt-1{margin-top:0.25rem}.mt-4{margin-top:1rem}.ml-1{margin-left:0.25rem}.mt-2{margin-top:0.5rem}.mt-3{margin-top:0.75rem}.flex{display:flex}.grid{display:grid}.hidden{display:none}.h-12{height:3rem}.h-full{height:100%}.min-h-screen{min-height:100vh}.w-full{width:100%}.w-12{width:3rem}.max-w-md{max-width:28rem}.grid-cols-1{grid-template-columns:repeat(1, minmax(0, 1fr))}.grid-cols-2{grid-template-columns:repeat(2, minmax(0, 1fr))}.flex-wrap{flex-wrap:wrap}.items-center{align-items:center}.justify-center{justify-content:center}.justify-between{justify-content:space-between}.gap-1\.5{gap:0.375rem}.gap-2\.5{gap:0.625rem}.gap-2{gap:0.5rem}.gap-3{gap:0.75rem}.gap-4{gap:1rem}.overflow-x-auto{overflow-x:auto}.whitespace-nowrap{white-space:nowrap}.rounded-2xl{border-radius:1rem}.rounded-lg{border-radius:0.5rem}.rounded-md{border-radius:0.375rem}.rounded{border-radius:0.25rem}.rounded-xl{border-radius:0.75rem}.border{border-width:1px}.border-2{border-width:2px}.border-b{border-bottom-width:1px}.border-b-2{border-bottom-width:2px}.border-t{border-top-width:1px}.border-blue-600{--tw-border-opacity:1;border-color:rgb(37 99 235 / var(--tw-border-opacity, 1))}.border-blue-600\/40{border-color:rgb(37 99 235 / 0.4)}.border-green-600\/40{border-color:rgb(22 163 74 / 0.4)}.border-red-600\/40{border-color:rgb(220 38 38 / 0.4)}.border-slate-600{--tw-border-opacity:1;border-color:rgb(71 85 105 / var(--tw-border-opacity, 1))}.border-transparent{border-color:transparent}.border-yellow-600\/40{border-color:rgb(202 138 4 / 0.4)}.border-pink-600\/40{border-color:rgb(219 39 119 / 0.4)}.border-slate-700{--tw-border-opacity:1;border-color:rgb(51 65 85 / var(--tw-border-opacity, 1))}.border-yellow-400{--tw-border-opacity:1;border-color:rgb(250 204 21 / var(--tw-border-opacity, 1))}.bg-blue-600{--tw-bg-opacity:1;background-color:rgb(37 99 235 / var(--tw-bg-opacity, 1))}.bg-blue-600\/20{background-color:rgb(37 99 235 / 0.2)}.bg-gray-800{--tw-bg-opacity:1;background-color:rgb(31 41 55 / var(--tw-bg-opacity, 1))}.bg-gray-900{--tw-bg-opacity:1;background-color:rgb(17 24 39 / var(--tw-bg-opacity, 1))}.bg-green-600\/20{background-color:rgb(22 163 74 / 0.2)}.bg-red-900\/20{background-color:rgb(127 29 29 / 0.2)}.bg-transparent{background-color:transparent}.bg-yellow-600\/20{background-color:rgb(202 138 4 / 0.2)}.bg-green-500{--tw-bg-opacity:1;background-color:rgb(34 197 94 / var(--tw-bg-opacity, 1))}.bg-pink-600\/20{background-color:rgb(219 39 119 / 0.2)}.bg-red-500{--tw-bg-opacity:1;background-color:rgb(239 68 68 / var(--tw-bg-opacity, 1))}.bg-slate-700{--tw-bg-opacity:1;background-color:rgb(51 65 85 / var(--tw-bg-opacity, 1))}.bg-yellow-500{--tw-bg-opacity:1;background-color:rgb(234 179 8 / var(--tw-bg-opacity, 1))}.bg-\[radial-gradient\(circle\2c \#2563eb_1px\2c transparent_1px\)\]{background-image:radial-gradient(circle,#2563eb 1px,transparent 1px)}.bg-gradient-to-br{background-image:linear-gradient(to bottom right, var(--tw-gradient-stops))}.from-blue-800{--tw-gradient-from:#1e40af var(--tw-gradient-from-position);--tw-gradient-to:rgb(30 64 175 / 0) var(--tw-gradient-to-position);--tw-gradient-stops:var(--tw-gradient-from), var(--tw-gradient-to)}.to-blue-900{--tw-gradient-to:#1e3a8a var(--tw-gradient-to-position)}.bg-\[length\:30px_30px\]{background-size:30px 30px}.p-0{padding:0px}.p-2\.5{padding:0.625rem}.p-3{padding:0.75rem}.p-4{padding:1rem}.p-5{padding:1.25rem}.p-6{padding:1.5rem}.p-2{padding:0.5rem}.px-2{padding-left:0.5rem;padding-right:0.5rem}.px-3{padding-left:0.75rem;padding-right:0.75rem}.px-3\.5{padding-left:0.875rem;padding-right:0.875rem}.px-4{padding-left:1rem;padding-right:1rem}.py-1{padding-top:0.25rem;padding-bottom:0.25rem}.py-1\.5{padding-top:0.375rem;padding-bottom:0.375rem}.py-2{padding-top:0.5rem;padding-bottom:0.5rem}.py-2\.5{padding-top:0.625rem;padding-bottom:0.625rem}.py-3{padding-top:0.75rem;padding-bottom:0.75rem}.pl-2{padding-left:0.5rem}.text-center{text-align:center}.text-right{text-align:right}.text-3xl{font-size:1.875rem;line-height:2.25rem}.text-sm{font-size:0.875rem;line-height:1.25rem}.text-xs{font-size:0.75rem;line-height:1rem}.text-2xl{font-size:1.5rem;line-height:2rem}.text-xl{font-size:1.25rem;line-height:1.75rem}.font-bold{font-weight:700}.font-semibold{font-weight:600}.leading-relaxed{line-height:1.625}.text-blue-400{--tw-text-opacity:1;color:rgb(96 165 250 / var(--tw-text-opacity, 1))}.text-green-400{--tw-text-opacity:1;color:rgb(74 222 128 / var(--tw-text-opacity, 1))}.text-red-400{--tw-text-opacity:1;color:rgb(248 113 113 / var(--tw-text-opacity, 1))}.text-slate-100{--tw-text-opacity:1;color:rgb(241 245 249 / var(--tw-text-opacity, 1))}.text-slate-400{--tw-text-opacity:1;color:rgb(148 163 184 / var(--tw-text-opacity, 1))}.text-white{--tw-text-opacity:1;color:rgb(255 255 255 / var(--tw-text-opacity, 1))}.text-yellow-400{--tw-text-opacity:1;color:rgb(250 204 21 / var(--tw-text-opacity, 1))}.text-pink-400{--tw-text-opacity:1;color:rgb(244 114 182 / var(--tw-text-opacity, 1))}.text-slate-300{--tw-text-opacity:1;color:rgb(203 213 225 / var(--tw-text-opacity, 1))}.shadow-lg{--tw-shadow:0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);--tw-shadow-colored:0 10px 15px -3px var(--tw-shadow-color), 0 4px 6px -4px var(--tw-shadow-color);box-shadow:var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)}.transition{transition-property:color, background-color, border-color, fill, stroke, opacity, box-shadow, transform, filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter;transition-property:color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter, -webkit-text-decoration-color, -webkit-backdrop-filter;transition-timing-function:cubic-bezier(0.4, 0, 0.2, 1);transition-duration:150ms}.duration-200{transition-duration:200ms}.hover\:bg-blue-700:hover{--tw-bg-opacity:1;background-color:rgb(29 78 216 / var(--tw-bg-opacity, 1))}.hover\:bg-red-900\/30:hover{background-color:rgb(127 29 29 / 0.3)}.hover\:text-yellow-400:hover{--tw-text-opacity:1;color:rgb(250 204 21 / var(--tw-text-opacity, 1))}.focus\:border-blue-500:focus{--tw-border-opacity:1;border-color:rgb(59 130 246 / var(--tw-border-opacity, 1))}.focus\:outline-none:focus{outline:2px solid transparent;outline-offset:2px}.disabled\:opacity-75:disabled{opacity:0.75}@media (min-width: 768px){.md\:grid-cols-2{grid-template-columns:repeat(2, minmax(0, 1fr))}.md\:grid-cols-3{grid-template-columns:repeat(3, minmax(0, 1fr))}}@media (min-width: 1024px){.lg\:col-span-2{grid-column:span 2 / span 2}.lg\:grid-cols-3{grid-template-columns:repeat(3, minmax(0, 1fr))}.lg\:grid-cols-4{grid-template-columns:repeat(4, minmax(0, 1fr))}}</style>

    <!-- Login Page -->
    <div id="login-page" class="min-h-screen flex items-center justify-center">
        <div class="absolute inset-0 opacity-4 bg-[radial-gradient(circle,#2563eb_1px,transparent_1px)] bg-[length:30px_30px] pointer-events-none"></div>
        
        <div class="w-full max-w-md p-5">
            <div class="text-center mb-7">
                <div class="w-18 h-18 rounded-2xl mx-auto mb-3 bg-gradient-to-br from-blue-800 to-blue-900 border-2 border-blue-600 flex items-center justify-center text-3xl shadow-lg">🏫</div>
                <div class="text-sm font-bold">ប្រព័ន្ធគ្រប់គ្រងអប់រំ</div>
                <div class="text-xs text-slate-400 mt-1">
                    សាលាបឋមសិក្សា រោគ · ឆមាសទី១ · ២០២៥–២០២៦
                </div>
            </div>

            <div class="card p-6">
                <div class="text-sm font-bold mb-4">🔐 ចូលប្រព័ន្ធ</div>

                <div class="mb-3">
                    <div class="text-xs text-slate-400 mb-1">👤 ឈ្មោះអ្នកប្រើ</div>
                    <input id="username" type="text" placeholder="username" class="w-full bg-gray-900 border border-slate-600 rounded-lg px-4 py-2 text-sm focus:outline-none focus:border-blue-500">
                </div>
                <div class="mb-4">
                    <div class="text-xs text-slate-400 mb-1">🔒 ពាក្យសម្ងាត់</div>
                    <input id="password" type="password" placeholder="password" class="w-full bg-gray-900 border border-slate-600 rounded-lg px-4 py-2 text-sm focus:outline-none focus:border-blue-500">
                </div>

                <div id="error-message" class="hidden bg-red-900/20 border border-red-600/40 rounded-lg px-3 py-2 text-xs text-red-400 mb-3">
                    ឈ្មោះ ឬ ពាក្យសម្ងាត់មិនត្រូវ!
                </div>

                <button id="login-btn" class="w-full bg-blue-600 hover:bg-blue-700 text-white rounded-lg px-4 py-3 text-sm font-bold transition duration-200 disabled:opacity-75">
                    ចូលប្រព័ន្ធ →
                </button>

                <div class="mt-4 bg-gray-900 border border-slate-600 rounded-lg p-3">
                    <div class="text-xs text-slate-400 mb-2 font-semibold">
                        🔑 គណនីសាកល្បង (ចុចដើម្បីបំពេញ)
                    </div>
                    <div class="flex flex-wrap gap-1.5">
                        <button data-user="admin" data-pass="admin123" class="bg-blue-600/20 border border-blue-600/40 text-blue-400 rounded-md px-2 py-1 text-xs font-bold">Admin (admin)</button>
                        <button data-user="director" data-pass="director123" class="bg-green-600/20 border border-green-600/40 text-green-400 rounded-md px-2 py-1 text-xs font-bold">នាយិកា (director)</button>
                        <button data-user="teacher" data-pass="teacher123" class="bg-yellow-600/20 border border-yellow-600/40 text-yellow-400 rounded-md px-2 py-1 text-xs font-bold">គ្រូ (teacher)</button>
                    </div>
                </div>
            </div>

            <div class="text-center mt-4 text-xs text-slate-400">
                ២០២៦ · ការិយាល័យអប់រំ ស្រុកភ្នំស្រុក
            </div>
        </div>
    </div>

    <!-- Dashboard Page -->
    <div id="dashboard-page" class="hidden min-h-screen">
        <!-- Header -->
        <div class="bg-gray-800 border-b border-slate-600 p-3 flex items-center justify-between">
            <div>
                <div class="text-sm font-bold">🏫 Dashboard · សាលាបឋមសិក្សា រោគ</div>
                <div class="text-xs text-slate-400">
                    ឆមាសទី១ ២០២៥–២០២៦ · ស្ពានស្រែង · ភ្នំស្រុក
                </div>
            </div>
            <div class="flex items-center gap-2.5">
                <div class="text-right">
                    <div id="user-name" class="text-xs font-bold text-yellow-400"></div>
                    <div id="user-role-tag" class="tag">role</div>
                </div>
                <button id="logout-btn" class="bg-red-900/20 border border-red-600/40 text-red-400 rounded-md px-3 py-1.5 text-xs font-bold hover:bg-red-900/30 transition">
                    ចេញ
                </button>
            </div>
        </div>

        <!-- Tabs -->
        <div class="bg-gray-800 border-b border-slate-600 flex overflow-x-auto p-0">
            <button data-tab="overview" class="bg-transparent border-b-2 border-transparent text-slate-400 hover:text-yellow-400 px-3.5 py-2.5 text-xs font-semibold flex items-center gap-1.5 whitespace-nowrap tab-active">
                📊 ទិដ្ឋភាពទូទៅ
            </button>
            <button data-tab="students" class="bg-transparent border-b-2 border-transparent text-slate-400 hover:text-yellow-400 px-3.5 py-2.5 text-xs font-semibold flex items-center gap-1.5 whitespace-nowrap">
                👩‍🎓 សិស្ស
            </button>
            <button data-tab="results" class="bg-transparent border-b-2 border-transparent text-slate-400 hover:text-yellow-400 px-3.5 py-2.5 text-xs font-semibold flex items-center gap-1.5 whitespace-nowrap">
                📈 លទ្ធផល
            </button>
            <button data-tab="staff" class="bg-transparent border-b-2 border-transparent text-slate-400 hover:text-yellow-400 px-3.5 py-2.5 text-xs font-semibold flex items-center gap-1.5 whitespace-nowrap">
                👨‍🏫 បុគ្គលិក
            </button>
            <button data-tab="finance" class="bg-transparent border-b-2 border-transparent text-slate-400 hover:text-yellow-400 px-3.5 py-2.5 text-xs font-semibold flex items-center gap-1.5 whitespace-nowrap hidden">
                💰 ហិរញ្ញ
            </button>
        </div>

        <!-- Content Area -->
        <div id="dashboard-content" class="p-4">
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-3 mb-4">
                    <div class="kpi-card">
                        <div class="w-12 h-12 rounded-xl flex items-center justify-center text-2xl bg-blue-600/20 border border-blue-600/40">
                            👩‍🎓
                        </div>
                        <div>
                            <div class="text-2xl font-bold text-blue-400">248</div>
                            <div class="text-xs font-semibold text-slate-300 mt-1">សិស្សសរុប</div>
                            <div class="text-xs text-slate-400 mt-1">ស្រី 116 · 46.8%</div>
                        </div>
                    </div>
                    <div class="kpi-card">
                        <div class="w-12 h-12 rounded-xl flex items-center justify-center text-2xl bg-green-600/20 border border-green-600/40">
                            ✅
                        </div>
                        <div>
                            <div class="text-2xl font-bold text-green-400">97.6%</div>
                            <div class="text-xs font-semibold text-slate-300 mt-1">% ជាប់</div>
                            <div class="text-xs text-slate-400 mt-1">ជាប់ 242 · ធ្លាក់ 5</div>
                        </div>
                    </div>
                    <div class="kpi-card">
                        <div class="w-12 h-12 rounded-xl flex items-center justify-center text-2xl bg-yellow-600/20 border border-yellow-600/40">
                            👨‍🏫
                        </div>
                        <div>
                            <div class="text-2xl font-bold text-yellow-400">17</div>
                            <div class="text-xs font-semibold text-slate-300 mt-1">បុគ្គលិកសរុប</div>
                            <div class="text-xs text-slate-400 mt-1">ស្រី 13 · 76.5%</div>
                        </div>
                    </div>
                    <div class="kpi-card">
                        <div class="w-12 h-12 rounded-xl flex items-center justify-center text-2xl bg-pink-600/20 border border-pink-600/40">
                            🏛️
                        </div>
                        <div>
                            <div class="text-2xl font-bold text-pink-400">10 / 15</div>
                            <div class="text-xs font-semibold text-slate-300 mt-1">ថ្នាក់ / បន្ទប់</div>
                            <div class="text-xs text-slate-400 mt-1">ដាច់ស្រយាល · ១ កម្រង</div>
                        </div>
                    </div>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-3 gap-4 mb-4">
                    <div class="card p-4 lg:col-span-2">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">ចំនួនសិស្ស + % ជាប់ (ក្រាបរួម)</h3>
                        <div class="chart-container">
                            <canvas id="bar-chart-overview" height="0" width="0" style="display: block; box-sizing: border-box; height: 0px; width: 0px;"></canvas>
                        </div>
                    </div>

                    <div class="card p-4">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">យេនឌ័រ + ស្ថានភាព</h3>
                        <div class="chart-container">
                            <canvas id="pie-chart-gender"></canvas>
                        </div>
                        <div class="grid grid-cols-2 gap-2 mt-3">
                            <div class="bg-gray-900 rounded-lg p-2 text-center">
                                <div class="text-xl font-bold text-green-400">242</div>
                                <div class="text-xs text-slate-400">ជាប់</div>
                            </div>
                            <div class="bg-gray-900 rounded-lg p-2 text-center">
                                <div class="text-xl font-bold text-red-400">5</div>
                                <div class="text-xs text-slate-400">ធ្លាក់</div>
                            </div>
                            <div class="bg-gray-900 rounded-lg p-2 text-center">
                                <div class="text-xl font-bold text-blue-400">10</div>
                                <div class="text-xs text-slate-400">ថ្នាក់</div>
                            </div>
                            <div class="bg-gray-900 rounded-lg p-2 text-center">
                                <div class="text-xl font-bold text-yellow-400">17</div>
                                <div class="text-xs text-slate-400">គ្រូ</div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-4">
                    <div class="card p-4">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">% ការអនុវត្តកម្មវិធី</h3>
                        
                            <div class="mb-3">
                                <div class="flex justify-between text-xs mb-1">
                                    <span>ខ្មែរ</span>
                                    <span class="font-bold text-green-400">50%</span>
                                </div>
                                <div class="bg-slate-700 rounded progress-bar">
                                    <div class="h-full rounded progress-bar bg-green-500" style="width: 50%"></div>
                                </div>
                            </div>
                        
                            <div class="mb-3">
                                <div class="flex justify-between text-xs mb-1">
                                    <span>គណិត</span>
                                    <span class="font-bold text-green-400">51%</span>
                                </div>
                                <div class="bg-slate-700 rounded progress-bar">
                                    <div class="h-full rounded progress-bar bg-green-500" style="width: 51%"></div>
                                </div>
                            </div>
                        
                            <div class="mb-3">
                                <div class="flex justify-between text-xs mb-1">
                                    <span>សង្គម</span>
                                    <span class="font-bold text-yellow-400">40%</span>
                                </div>
                                <div class="bg-slate-700 rounded progress-bar">
                                    <div class="h-full rounded progress-bar bg-yellow-500" style="width: 40%"></div>
                                </div>
                            </div>
                        
                            <div class="mb-3">
                                <div class="flex justify-between text-xs mb-1">
                                    <span>វិទ្យា</span>
                                    <span class="font-bold text-yellow-400">41%</span>
                                </div>
                                <div class="bg-slate-700 rounded progress-bar">
                                    <div class="h-full rounded progress-bar bg-yellow-500" style="width: 41%"></div>
                                </div>
                            </div>
                        
                            <div class="mb-3">
                                <div class="flex justify-between text-xs mb-1">
                                    <span>អង់គ្លេស</span>
                                    <span class="font-bold text-red-400">0%</span>
                                </div>
                                <div class="bg-slate-700 rounded progress-bar">
                                    <div class="h-full rounded progress-bar bg-red-500" style="width: 0%"></div>
                                </div>
                            </div>
                        
                    </div>

                    <div class="card p-4">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">ភារៈបុគ្គលិក</h3>
                        
                            <div class="flex justify-between py-1 border-b border-slate-700 text-xs">
                                <span class="text-slate-400">នាយក/រង</span>
                                <span><b>2</b><span class="text-pink-400 ml-1">(1ស)</span></span>
                            </div>
                        
                            <div class="flex justify-between py-1 border-b border-slate-700 text-xs">
                                <span class="text-slate-400">សិក្ខាបន</span>
                                <span><b>10</b><span class="text-pink-400 ml-1">(9ស)</span></span>
                            </div>
                        
                            <div class="flex justify-between py-1 border-b border-slate-700 text-xs">
                                <span class="text-slate-400">លេខាធិការ</span>
                                <span><b>1</b><span class="text-pink-400 ml-1">(0ស)</span></span>
                            </div>
                        
                            <div class="flex justify-between py-1 border-b border-slate-700 text-xs">
                                <span class="text-slate-400">បណ្ណារក្ស</span>
                                <span><b>1</b><span class="text-pink-400 ml-1">(1ស)</span></span>
                            </div>
                        
                            <div class="flex justify-between py-1 border-b border-slate-700 text-xs">
                                <span class="text-slate-400">កសិកម្ម</span>
                                <span><b>1</b><span class="text-pink-400 ml-1">(0ស)</span></span>
                            </div>
                        
                            <div class="flex justify-between py-1 border-b border-slate-700 text-xs">
                                <span class="text-slate-400">ម.តេយ្យ</span>
                                <span><b>2</b><span class="text-pink-400 ml-1">(2ស)</span></span>
                            </div>
                        
                    </div>

                    <div class="card p-4">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">ហិរញ្ញប្បទាន</h3>
                        
                            <div class="py-2 border-b border-slate-700">
                                <div class="text-xs text-slate-400">សង្ហារឹម</div>
                                <div class="text-sm font-bold text-yellow-400">923,100 ៛</div>
                            </div>
                        
                            <div class="py-2 border-b border-slate-700">
                                <div class="text-xs text-slate-400">ការិយាល័យ</div>
                                <div class="text-sm font-bold text-blue-400">2,358,400 ៛</div>
                            </div>
                        
                            <div class="py-2 border-b border-slate-700">
                                <div class="text-xs text-slate-400">សរុប</div>
                                <div class="text-sm font-bold text-green-400">3,281,500 ៛</div>
                            </div>
                        
                        <div class="text-xs text-slate-400 mt-2 leading-relaxed">
                            💡 ប្រភព: SOF + សហគមន៍ + អង្គការទស្សនៈពិភពលោក
                        </div>
                    </div>
                </div>
            </div>

        <div class="text-center p-2.5 text-xs text-slate-400 border-t border-slate-600">
            ២៤ មេសា ២០២៦ · អ្នកធ្វើរបាយការណ៍: អ៊ុន ប៊ុនទុង · Firebase: schoolreport-a7404
        </div>
    </div>

    <script>
        // Data
        const gradeData = [
            { grade:"ទី១", total:30, female:14, pass:30, fail:0, teacher:"រ៉ែម សុភក្ដិ" },
            { grade:"ទី២", total:42, female:21, pass:42, fail:0, teacher:"ប៉ោង ស្រីពេជ្រ / លេង ចាន់លាវ" },
            { grade:"ទី៣", total:42, female:20, pass:40, fail:1, teacher:"ប៊ី ពិសី / អេង ផល្លែន" },
            { grade:"ទី៤", total:49, female:21, pass:49, fail:0, teacher:"ឆេន សាវដា / អឿន សុខៀប" },
            { grade:"ទី៥", total:50, female:23, pass:49, fail:1, teacher:"ស្វាង មនោរម្យ / រ៉ោម សម្ផស្ស" },
            { grade:"ទី៦", total:35, female:17, pass:32, fail:3, teacher:"ឈួត សេរ៉ូម" },
        ];

        const staffList = [
            { id:"01", name:"សុខ សារើន",     g:"ស", rank:"គ្រូបឋម", edu:"ថ្នាក់ទី១២",       role:"នាយិកា",    cls:"-",   tot:0,  fem:0,  phone:"0975405822" },
            { id:"02", name:"យ៉េន សារី",     g:"ប", rank:"គ្រូបឋម", edu:"ថ្នាក់ទី១២",       role:"នាយករង",   cls:"-",   tot:0,  fem:0,  phone:"085246698" },
            { id:"03", name:"អ៊ុន ប៊ុនទុង",  g:"ប", rank:"គ្រូបឋម", edu:"ស.បរិញ្ញាបត្រ",    role:"លេខាធិការ", cls:"-",   tot:0,  fem:0,  phone:"017407773" },
            { id:"04", name:"រ៉ែម សុភក្ដិ",   g:"ស", rank:"គ្រូបឋម", edu:"ស.ទុតិយភូមិ",      role:"គ្រូ",      cls:"1A",  tot:30, fem:14, phone:"0883435566" },
            { id:"05", name:"ស្វាង មនោរម្យ",  g:"ស", rank:"គ្រូបឋម", edu:"ស.បរិញ្ញាបត្រ",    role:"គ្រូ",      cls:"5A",  tot:25, fem:12, phone:"0976858898" },
            { id:"06", name:"ប៉ោង ស្រីពេជ្រ", g:"ស", rank:"គ្រូបឋម", edu:"ស.ទុតិយភូមិ",      role:"គ្រូ",      cls:"2A",  tot:21, fem:10, phone:"0889304103" },
            { id:"07", name:"លេង ចាន់លាវ",    g:"ស", rank:"គ្រូបឋម", edu:"ស.ទុតិយភូមិ",      role:"គ្រូ",      cls:"2B",  tot:21, fem:10, phone:"0884661856" },
            { id:"08", name:"អេង ផល្លែន",     g:"ស", rank:"គ្រូបឋម", edu:"ស.បរិញ្ញាបត្រ",    role:"គ្រូ",      cls:"3B",  tot:21, fem:10, phone:"092620771" },
            { id:"09", name:"ប៊ី ពិសី",       g:"ស", rank:"គ្រូបឋម", edu:"ស.ទុតិយភូមិ",      role:"គ្រូ",      cls:"3A",  tot:20, fem:11, phone:"0979339499" },
            { id:"10", name:"អឿន សុខៀប",     g:"ស", rank:"គ្រូបឋម", edu:"ស.បរិញ្ញាបត្រ",    role:"គ្រូ",      cls:"4B",  tot:24, fem:11, phone:"0974611580" },
            { id:"11", name:"ឆេន សាវដា",     g:"ស", rank:"គ្រូបឋម", edu:"ស.បរិញ្ញាបត្រ",    role:"គ្រូ",      cls:"4A",  tot:25, fem:12, phone:"0977075979" },
            { id:"12", name:"រ៉ោម សម្ផស្ស",   g:"ប", rank:"គ្រូបឋម", edu:"ស.ទុតិយភូមិ",      role:"គ្រូ",      cls:"5B",  tot:25, fem:11, phone:"0314234466" },
            { id:"13", name:"ឈួត សេរ៉ូម",     g:"ស", rank:"គ្រូបឋម", edu:"ស.បរិញ្ញាបត្រ",    role:"គ្រូ",      cls:"6A",  tot:35, fem:17, phone:"0976700999" },
            { id:"14", name:"កែវ ខន",         g:"ប", rank:"គ្រូបឋម", edu:"ថ្នាក់ទី១២",       role:"កសិកម្ម",  cls:"-",   tot:0,  fem:0,  phone:"090887118" },
            { id:"15", name:"លន់ ចាន់នឹក",    g:"ស", rank:"គ្រូបឋម", edu:"ស.ទុតិយភូមិ",      role:"បណ្ណារក្ស", cls:"-",   tot:0,  fem:0,  phone:"0888539699" },
            { id:"16", name:"ពាន ណូរ៉ា",      g:"ស", rank:"គ្រូបឋម", edu:"ក.សាកលវិទ្យាល័យ",  role:"ម.ត ខ្ពស់", cls:"ម.ត", tot:35, fem:20, phone:"0978680864" },
            { id:"17", name:"ឡុក ម៉ាក់តី",    g:"ស", rank:"គ្រូបឋម", edu:"ស.ទុតិយភូមិ",      role:"ម.ត ចម្រុះ",cls:"ម.ត", tot:40, fem:25, phone:"0886534343" },
        ];

        const curriculumData = [
            { subject:"ខ្មែរ",    avg:50 },
            { subject:"គណិត",    avg:51 },
            { subject:"សង្គម",   avg:40 },
            { subject:"វិទ្យា",   avg:41 },
            { subject:"អង់គ្លេស", avg:0 },
        ];

        // DOM Elements
        const loginPage = document.getElementById('login-page');
        const dashboardPage = document.getElementById('dashboard-page');
        const dashboardContent = document.getElementById('dashboard-content');
        const usernameInput = document.getElementById('username');
        const passwordInput = document.getElementById('password');
        const loginBtn = document.getElementById('login-btn');
        const errorMessage = document.getElementById('error-message');
        const logoutBtn = document.getElementById('logout-btn');
        const tabs = document.querySelectorAll('[data-tab]');
        const userNameElement = document.getElementById('user-name');
        const userRoleTag = document.getElementById('user-role-tag');
        const financeTab = document.querySelector('[data-tab="finance"]');

        // State
        let currentUser = null;
        const accounts = [
            { user:"admin",    pass:"admin123",    role:"admin",    name:"អ្នកគ្រប់គ្រង" },
            { user:"director", pass:"director123", role:"director", name:"សុខ សារើន (នាយិកា)" },
            { user:"teacher",  pass:"teacher123",  role:"teacher",  name:"លោកគ្រូ / អ្នកគ្រូ" },
        ];

        // Initialize
        document.addEventListener('DOMContentLoaded', function() {
            // Set up event listeners for login button and enter key
            loginBtn.addEventListener('click', handleLogin);
            passwordInput.addEventListener('keydown', function(e) {
                if (e.key === 'Enter') handleLogin();
            });

            // Set up event listeners for demo login buttons
            document.querySelectorAll('[data-user]').forEach(btn => {
                btn.addEventListener('click', function() {
                    const user = this.dataset.user;
                    const pass = this.dataset.pass;
                    usernameInput.value = user;
                    passwordInput.value = pass;
                });
            });

            // Set up tab switching
            tabs.forEach(tab => {
                tab.addEventListener('click', function() {
                    setActiveTab(this.dataset.tab);
                });
            });

            // Logout functionality
            logoutBtn.addEventListener('click', function() {
                currentUser = null;
                loginPage.classList.remove('hidden');
                dashboardPage.classList.add('hidden');
            });

            // Initial setup
            setActiveTab('overview');
        });

        function handleLogin() {
            const u = usernameInput.value.trim();
            const p = passwordInput.value.trim();

            if (!u || !p) {
                showError('សូមបញ្ចូលឈ្មោះអ្នកប្រើ និងពាក្យសម្ងាត់');
                return;
            }

            loginBtn.disabled = true;
            loginBtn.textContent = '⏳ កំពុងចូល...';

            setTimeout(() => {
                const acc = accounts.find(a => a.user === u && a.pass === p);
                if (acc) {
                    currentUser = acc;
                    showDashboard();
                } else {
                    showError('ឈ្មោះ ឬ ពាក្យសម្ងាត់មិនត្រូវ!');
                    loginBtn.disabled = false;
                    loginBtn.textContent = 'ចូលប្រព័ន្ធ →';
                }
            }, 700);
        }

        function showError(message) {
            errorMessage.textContent = message;
            errorMessage.classList.remove('hidden');
            setTimeout(() => {
                errorMessage.classList.add('hidden');
            }, 3000);
        }

        function showDashboard() {
            loginPage.classList.add('hidden');
            dashboardPage.classList.remove('hidden');
            populateDashboard();
        }

        function setActiveTab(tabId) {
            // Update active tab
            tabs.forEach(tab => {
                if (tab.dataset.tab === tabId) {
                    tab.classList.add('tab-active');
                } else {
                    tab.classList.remove('tab-active');
                }
            });

            // Show corresponding content
            renderDashboardContent(tabId);
        }

        function populateDashboard() {
            userNameElement.textContent = currentUser.name;
            
            switch(currentUser.role) {
                case 'admin':
                    userRoleTag.textContent = 'admin';
                    userRoleTag.className = 'tag';
                    financeTab.classList.remove('hidden');
                    break;
                case 'director':
                    userRoleTag.textContent = 'នាយិកា';
                    userRoleTag.className = 'tag-green';
                    financeTab.classList.remove('hidden');
                    break;
                case 'teacher':
                    userRoleTag.textContent = 'គ្រូ';
                    userRoleTag.className = 'tag-orange';
                    financeTab.classList.add('hidden');
                    break;
            }
        }

        function renderDashboardContent(tabId) {
            switch(tabId) {
                case 'overview':
                    renderOverview();
                    break;
                case 'students':
                    renderStudents();
                    break;
                case 'results':
                    renderResults();
                    break;
                case 'staff':
                    renderStaff();
                    break;
                case 'finance':
                    if (currentUser.role === 'admin') {
                        renderFinance();
                    }
                    break;
            }
        }

        function renderOverview() {
            const totalS = gradeData.reduce((a,g) => a + g.total, 0);
            const totalF = gradeData.reduce((a,g) => a + g.female, 0);
            const totalPass = gradeData.reduce((a,g) => a + g.pass, 0);
            const totalFail = gradeData.reduce((a,g) => a + g.fail, 0);
            const fStaff = staffList.filter(s => s.g === "ស").length;

            // Calculate percentages
            const passPct = totalS > 0 ? ((totalPass/totalS)*100).toFixed(1) : "0";
            const femalePct = totalS > 0 ? ((totalF/totalS)*100).toFixed(1) : "0";
            const femaleStaffPct = staffList.length > 0 ? ((fStaff/staffList.length)*100).toFixed(1) : "0";

            dashboardContent.innerHTML = `
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-3 mb-4">
                    <div class="kpi-card">
                        <div class="w-12 h-12 rounded-xl flex items-center justify-center text-2xl bg-blue-600/20 border border-blue-600/40">
                            👩‍🎓
                        </div>
                        <div>
                            <div class="text-2xl font-bold text-blue-400">${totalS}</div>
                            <div class="text-xs font-semibold text-slate-300 mt-1">សិស្សសរុប</div>
                            <div class="text-xs text-slate-400 mt-1">ស្រី ${totalF} · ${femalePct}%</div>
                        </div>
                    </div>
                    <div class="kpi-card">
                        <div class="w-12 h-12 rounded-xl flex items-center justify-center text-2xl bg-green-600/20 border border-green-600/40">
                            ✅
                        </div>
                        <div>
                            <div class="text-2xl font-bold text-green-400">${passPct}%</div>
                            <div class="text-xs font-semibold text-slate-300 mt-1">% ជាប់</div>
                            <div class="text-xs text-slate-400 mt-1">ជាប់ ${totalPass} · ធ្លាក់ ${totalFail}</div>
                        </div>
                    </div>
                    <div class="kpi-card">
                        <div class="w-12 h-12 rounded-xl flex items-center justify-center text-2xl bg-yellow-600/20 border border-yellow-600/40">
                            👨‍🏫
                        </div>
                        <div>
                            <div class="text-2xl font-bold text-yellow-400">17</div>
                            <div class="text-xs font-semibold text-slate-300 mt-1">បុគ្គលិកសរុប</div>
                            <div class="text-xs text-slate-400 mt-1">ស្រី ${fStaff} · ${femaleStaffPct}%</div>
                        </div>
                    </div>
                    <div class="kpi-card">
                        <div class="w-12 h-12 rounded-xl flex items-center justify-center text-2xl bg-pink-600/20 border border-pink-600/40">
                            🏛️
                        </div>
                        <div>
                            <div class="text-2xl font-bold text-pink-400">10 / 15</div>
                            <div class="text-xs font-semibold text-slate-300 mt-1">ថ្នាក់ / បន្ទប់</div>
                            <div class="text-xs text-slate-400 mt-1">ដាច់ស្រយាល · ១ កម្រង</div>
                        </div>
                    </div>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-3 gap-4 mb-4">
                    <div class="card p-4 lg:col-span-2">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">ចំនួនសិស្ស + % ជាប់ (ក្រាបរួម)</h3>
                        <div class="chart-container">
                            <canvas id="bar-chart-overview"></canvas>
                        </div>
                    </div>

                    <div class="card p-4">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">យេនឌ័រ + ស្ថានភាព</h3>
                        <div class="chart-container">
                            <canvas id="pie-chart-gender"></canvas>
                        </div>
                        <div class="grid grid-cols-2 gap-2 mt-3">
                            <div class="bg-gray-900 rounded-lg p-2 text-center">
                                <div class="text-xl font-bold text-green-400">${totalPass}</div>
                                <div class="text-xs text-slate-400">ជាប់</div>
                            </div>
                            <div class="bg-gray-900 rounded-lg p-2 text-center">
                                <div class="text-xl font-bold text-red-400">${totalFail}</div>
                                <div class="text-xs text-slate-400">ធ្លាក់</div>
                            </div>
                            <div class="bg-gray-900 rounded-lg p-2 text-center">
                                <div class="text-xl font-bold text-blue-400">10</div>
                                <div class="text-xs text-slate-400">ថ្នាក់</div>
                            </div>
                            <div class="bg-gray-900 rounded-lg p-2 text-center">
                                <div class="text-xl font-bold text-yellow-400">17</div>
                                <div class="text-xs text-slate-400">គ្រូ</div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-4">
                    <div class="card p-4">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">% ការអនុវត្តកម្មវិធី</h3>
                        ${curriculumData.map(subject => `
                            <div class="mb-3">
                                <div class="flex justify-between text-xs mb-1">
                                    <span>${subject.subject}</span>
                                    <span class="font-bold ${subject.avg >= 50 ? 'text-green-400' : subject.avg > 0 ? 'text-yellow-400' : 'text-red-400'}">${subject.avg}%</span>
                                </div>
                                <div class="bg-slate-700 rounded progress-bar">
                                    <div class="h-full rounded progress-bar bg-${subject.avg >= 50 ? 'green' : subject.avg > 0 ? 'yellow' : 'red'}-500" style="width: ${subject.avg}%"></div>
                                </div>
                            </div>
                        `).join('')}
                    </div>

                    <div class="card p-4">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">ភារៈបុគ្គលិក</h3>
                        ${[
                            ["នាយក/រង","2","1"],["សិក្ខាបន","10","9"],["លេខាធិការ","1","0"],
                            ["បណ្ណារក្ស","1","1"],["កសិកម្ម","1","0"],["ម.តេយ្យ","2","2"]
                        ].map(([l,t,f]) => `
                            <div class="flex justify-between py-1 border-b border-slate-700 text-xs">
                                <span class="text-slate-400">${l}</span>
                                <span><b>${t}</b><span class="text-pink-400 ml-1">(${f}ស)</span></span>
                            </div>
                        `).join('')}
                    </div>

                    <div class="card p-4">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">ហិរញ្ញប្បទាន</h3>
                        ${[
                            ["សង្ហារឹម","923,100 ៛","yellow-400"],
                            ["ការិយាល័យ","2,358,400 ៛","blue-400"],
                            ["សរុប","3,281,500 ៛","green-400"]
                        ].map(([l,v,c]) => `
                            <div class="py-2 border-b border-slate-700">
                                <div class="text-xs text-slate-400">${l}</div>
                                <div class="text-sm font-bold text-${c}">${v}</div>
                            </div>
                        `).join('')}
                        <div class="text-xs text-slate-400 mt-2 leading-relaxed">
                            💡 ប្រភព: SOF + សហគមន៍ + អង្គការទស្សនៈពិភពលោក
                        </div>
                    </div>
                </div>
            `;

            // Render charts
            renderBarChartOverview();
            renderPieChartGender();
        }

        function renderBarChartOverview() {
            const ctx = document.getElementById('bar-chart-overview').getContext('2d');
            const data = gradeData.map(g => ({
                ...g,
                passPct: Math.round((g.pass / g.total) * 100)
            }));

            new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: data.map(item => item.grade),
                    datasets: [
                        {
                            label: 'សរុប',
                            data: data.map(item => item.total),
                            backgroundColor: '#3b82f6',
                            borderRadius: 4,
                            borderSkipped: false
                        },
                        {
                            label: 'ស្រី',
                            data: data.map(item => item.female),
                            backgroundColor: '#ec4899',
                            borderRadius: 4,
                            borderSkipped: false
                        },
                        {
                            label: '% ជាប់',
                            data: data.map(item => item.passPct),
                            backgroundColor: 'transparent',
                            borderColor: '#10b981',
                            borderWidth: 2,
                            type: 'line',
                            yAxisID: 'y1'
                        }
                    ]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            labels: {
                                font: {
                                    size: 10
                                }
                            }
                        }
                    },
                    scales: {
                        x: {
                            ticks: {
                                color: '#94a3b8'
                            }
                        },
                        y: {
                            ticks: {
                                color: '#94a3b8'
                            },
                            grid: {
                                color: 'rgba(28, 51, 86, 0.3)'
                            }
                        },
                        y1: {
                            position: 'right',
                            ticks: {
                                color: '#94a3b8',
                                callback: function(value) {
                                    return value + '%';
                                }
                            },
                            grid: {
                                drawOnChartArea: false
                            }
                        }
                    }
                }
            });
        }

        function renderPieChartGender() {
            const ctx = document.getElementById('pie-chart-gender').getContext('2d');
            new Chart(ctx, {
                type: 'pie',
                data: {
                    labels: ['ប្រុស', 'ស្រី'],
                    datasets: [{
                        data: [totalS - totalF, totalF],
                        backgroundColor: ['#3b82f6', '#ec4899'],
                        borderWidth: 0
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            labels: {
                                font: {
                                    size: 10
                                }
                            }
                        }
                    }
                }
            });
        }

        function renderStudents() {
            const totalS = gradeData.reduce((a,g) => a + g.total, 0);
            const totalF = gradeData.reduce((a,g) => a + g.female, 0);
            const totalPass = gradeData.reduce((a,g) => a + g.pass, 0);
            const totalFail = gradeData.reduce((a,g) => a + g.fail, 0);

            dashboardContent.innerHTML = `
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                    <div class="card p-4">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">ចំនួនសិស្ស + លទ្ធផល តាមថ្នាក់</h3>
                        <div class="overflow-x-auto">
                            <table class="w-full text-xs">
                                <thead>
                                    <tr class="text-slate-400">
                                        ${["ថ្នាក់","សរុប","ស្រី","%ស្រី","ជាប់","ធ្លាក់","% ជាប់"].map(h => `<th class="p-1.5 text-center border-b border-slate-700">${h}</th>`).join('')}
                                    </tr>
                                </thead>
                                <tbody>
                                    ${gradeData.map((g,i) => `
                                        <tr class="table-row">
                                            <td class="p-1.5 text-center text-yellow-400 font-bold">${g.grade}</td>
                                            <td class="p-1.5 text-center font-semibold">${g.total}</td>
                                            <td class="p-1.5 text-center text-pink-400">${g.female}</td>
                                            <td class="p-1.5 text-center text-slate-400">${((g.female/g.total)*100).toFixed(1)}%</td>
                                            <td class="p-1.5 text-center text-green-400">${g.pass}</td>
                                            <td class="p-1.5 text-center ${g.fail > 0 ? 'text-red-400' : 'text-slate-400'}">${g.fail}</td>
                                            <td class="p-1.5 text-center">
                                                <span class="status-badge ${g.fail === 0 ? 'status-green' : 'status-red'}">
                                                    ${((g.pass/g.total)*100).toFixed(0)}%
                                                </span>
                                            </td>
                                        </tr>
                                    `).join('')}
                                    <tr class="border-t border-slate-700 font-bold">
                                        <td class="p-1.5 text-center text-green-400">សរុប</td>
                                        <td class="p-1.5 text-center">${totalS}</td>
                                        <td class="p-1.5 text-center text-pink-400">${totalF}</td>
                                        <td class="p-1.5 text-center">${((totalF/totalS)*100).toFixed(1)}%</td>
                                        <td class="p-1.5 text-center text-green-400">${totalPass}</td>
                                        <td class="p-1.5 text-center text-red-400">${totalFail}</td>
                                        <td class="p-1.5 text-center">
                                            <span class="status-badge status-green">
                                                ${((totalPass/totalS)*100).toFixed(0)}%
                                            </span>
                                        </td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>

                    <div class="card p-4">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">ក្រាបសរុប + ស្រី + ធ្លាក់</h3>
                        <div class="chart-container">
                            <canvas id="bar-chart-students"></canvas>
                        </div>
                    </div>
                </div>

                <div class="card p-4">
                    <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">% ជាប់ + ស្ថានភាពតាមថ្នាក់</h3>
                    <div class="flex gap-2 flex-wrap">
                        ${gradeData.map((g,i) => {
                            const pp = (g.pass/g.total)*100;
                            const statusClass = pp === 100 ? 'border-green-500/40' : pp >= 95 ? 'border-yellow-500/40' : 'border-red-500/40';
                            return `
                                <div class="flex-1 min-w-[120px] bg-gray-900 rounded-xl border ${statusClass} p-3 text-center">
                                    <div class="text-xs text-slate-400 mb-1">${g.grade}</div>
                                    <div class="text-2xl font-bold ${pp === 100 ? 'text-green-400' : pp >= 95 ? 'text-yellow-400' : 'text-red-400'}">${Math.round(pp)}%</div>
                                    <div class="text-xs text-slate-400 mt-1">ជាប់ ${g.pass}/${g.total}</div>
                                    ${g.fail > 0 ? `<div class="mt-2"><span class="tag-red">ធ្លាក់ ${g.fail}</span></div>` : ''}
                                    <div class="text-[8px] text-slate-400 mt-2 leading-tight">${g.teacher.split('/')[0].trim()}</div>
                                </div>
                            `;
                        }).join('')}
                    </div>
                </div>
            `;

            renderBarChartStudents();
        }

        function renderBarChartStudents() {
            const ctx = document.getElementById('bar-chart-students').getContext('2d');
            new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: gradeData.map(item => item.grade),
                    datasets: [
                        {
                            label: 'សរុប',
                            data: gradeData.map(item => item.total),
                            backgroundColor: '#3b82f6',
                            borderRadius: 4,
                            borderSkipped: false
                        },
                        {
                            label: 'ស្រី',
                            data: gradeData.map(item => item.female),
                            backgroundColor: '#ec4899',
                            borderRadius: 4,
                            borderSkipped: false
                        },
                        {
                            label: 'ធ្លាក់',
                            data: gradeData.map(item => item.fail),
                            backgroundColor: '#ef4444',
                            borderRadius: 4,
                            borderSkipped: false
                        }
                    ]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            labels: {
                                font: {
                                    size: 10
                                }
                            }
                        }
                    },
                    scales: {
                        x: {
                            ticks: {
                                color: '#94a3b8'
                            }
                        },
                        y: {
                            ticks: {
                                color: '#94a3b8'
                            },
                            grid: {
                                color: 'rgba(28, 51, 86, 0.3)'
                            }
                        }
                    }
                }
            });
        }

        function renderResults() {
            dashboardContent.innerHTML = `
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                    <div class="card p-4">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">% ឡើង / ត្រួត តាមថ្នាក់</h3>
                        <div class="chart-container">
                            <canvas id="bar-chart-results"></canvas>
                        </div>
                    </div>

                    <div class="card p-4">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">% ការអនុវត្តកម្មវិធីសិក្សា</h3>
                        <div class="chart-container">
                            <canvas id="bar-chart-curriculum"></canvas>
                        </div>
                    </div>
                </div>

                <div class="card p-4">
                    <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">ស្ថានភាពគ្រូ (ល្អ / មធ្យម / ខ្សោយ) ក្នុងការបង្រៀន</h3>
                    <div class="flex gap-2 flex-wrap">
                        ${[
                            { l:"ថ្នាក់ ល្អ",  n:1, c:"green",  note:"មានកិច្ចតែងការ + សម្ភារ" },
                            { l:"ថ្នាក់ មធ្យម",n:5, c:"yellow", note:"ត្រូវបន្ថែម" },
                            { l:"ថ្នាក់ ខ្សោយ",n:0, c:"red",    note:"—" },
                        ].map((i,k) => `
                            <div class="flex-1 min-w-[120px] bg-gray-900 rounded-xl border border-${i.c}-500/40 p-4 text-center">
                                <div class="text-3xl font-bold text-${i.c}-400">${i.n}</div>
                                <div class="text-xs text-slate-100 mt-1 font-semibold">${i.l}</div>
                                <div class="text-[9px] text-slate-400 mt-2">${i.note}</div>
                            </div>
                        `).join('')}
                    </div>
                </div>
            `;

            renderBarChartResults();
            renderBarChartCurriculum();
        }

        function renderBarChartResults() {
            const ctx = document.getElementById('bar-chart-results').getContext('2d');
            new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: ['ទី១','ទី២','ទី៣','ទី៤','ទី៥','ទី៦'],
                    datasets: [
                        {
                            label: '%ឡើងសរុប',
                            data: [100, 100, 95, 100, 98, 91],
                            backgroundColor: '#10b981',
                            borderRadius: 3,
                            borderSkipped: false
                        },
                        {
                            label: '%ឡើងស្រី',
                            data: [100, 100, 100, 105, 100, 88],
                            backgroundColor: '#ec4899',
                            borderRadius: 3,
                            borderSkipped: false
                        },
                        {
                            label: '%ត្រួតសរុប',
                            data: [0, 0, 2.38, 0, 2.0, 8.57],
                            backgroundColor: '#ef4444',
                            borderRadius: 3,
                            borderSkipped: false
                        },
                        {
                            label: '%ត្រួតស្រី',
                            data: [0, 0, 0, 0, 0, 11.76],
                            backgroundColor: '#fb923c',
                            borderRadius: 3,
                            borderSkipped: false
                        }
                    ]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            labels: {
                                font: {
                                    size: 10
                                }
                            }
                        }
                    },
                    scales: {
                        x: {
                            ticks: {
                                color: '#94a3b8'
                            }
                        },
                        y: {
                            ticks: {
                                color: '#94a3b8',
                                callback: function(value) {
                                    return value + '%';
                                }
                            },
                            grid: {
                                color: 'rgba(28, 51, 86, 0.3)'
                            }
                        }
                    }
                }
            });
        }

        function renderBarChartCurriculum() {
            const ctx = document.getElementById('bar-chart-curriculum').getContext('2d');
            new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: curriculumData.map(item => item.subject),
                    datasets: [{
                        label: '%',
                        data: curriculumData.map(item => item.avg),
                        backgroundColor: curriculumData.map(item => 
                            item.avg >= 50 ? '#10b981' : 
                            item.avg > 0 ? '#f59e0b' : 
                            '#ef444488'
                        ),
                        borderRadius: [0, 4, 4, 0]
                    }]
                },
                options: {
                    indexAxis: 'y',
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            labels: {
                                font: {
                                    size: 10
                                }
                            }
                        }
                    },
                    scales: {
                        x: {
                            ticks: {
                                color: '#94a3b8',
                                callback: function(value) {
                                    return value + '%';
                                }
                            },
                            grid: {
                                color: 'rgba(28, 51, 86, 0.3)'
                            },
                            min: 0,
                            max: 100
                        },
                        y: {
                            ticks: {
                                color: '#dbeafe'
                            },
                            grid: {
                                color: 'rgba(28, 51, 86, 0.3)'
                            }
                        }
                    }
                }
            });
        }

        function renderStaff() {
            const fStaff = staffList.filter(s => s.g === "ស").length;

            dashboardContent.innerHTML = `
                <div class="grid grid-cols-2 md:grid-cols-4 gap-3 mb-4">
                    ${[
                        { l:"សរុបបុគ្គលិក", v:17,  c:"blue" },
                        { l:"ស្រីសរុប",      v:fStaff, c:"pink" },
                        { l:"គ្រូបង្រៀន",   v:10,  c:"green" },
                        { l:"ម.តេយ្យ",      v:2,   c:"yellow" }
                    ].map(i => `
                        <div class="card p-3 text-center">
                            <div class="text-3xl font-bold text-${i.c}-400">${i.v}</div>
                            <div class="text-xs text-slate-400 mt-1">${i.l}</div>
                        </div>
                    `).join('')}
                </div>

                <div class="card p-4">
                    <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">បញ្ជីបុគ្គលិក (ឆមាសទី១ ២០២៥–២០២៦)</h3>
                    <div class="overflow-x-auto">
                        <table class="w-full text-xs">
                            <thead class="bg-gray-900">
                                ${["ល.រ","ឈ្មោះ","ភេទ","ការសិក្សា","ភារៈ","ថ្នាក់","សិស្សសរុប","ស្រី","ទូរស័ព្ទ"].map(h => `<th class="p-1.5 text-center border-b border-slate-700 text-slate-400 font-semibold">${h}</th>`).join('')}
                            </thead>
                            <tbody>
                                ${staffList.map((s,i) => `
                                    <tr class="table-row">
                                        <td class="p-1.5 text-center text-slate-400 text-xs">${s.id}</td>
                                        <td class="p-1.5 font-semibold">${s.name}</td>
                                        <td class="p-1.5 text-center">
                                            <span class="tag ${s.g === 'ស' ? 'tag-red' : 'tag-blue'}">${s.g}</span>
                                        </td>
                                        <td class="p-1.5 text-xs text-slate-400">${s.edu}</td>
                                        <td class="p-1.5">
                                            <span class="tag ${s.role === 'នាយិកា' || s.role === 'នាយករង' ? 'tag-orange' : 
                                                s.role === 'គ្រូ' ? 'tag-green' : 
                                                s.role === 'លេខាធិការ' ? 'tag-blue' : 'tag'}">${s.role}</span>
                                        </td>
                                        <td class="p-1.5 text-center text-yellow-400 font-bold">
                                            ${s.cls !== '-' ? s.cls : '<span class="text-slate-400">—</span>'}
                                        </td>
                                        <td class="p-1.5 text-center">${s.tot > 0 ? s.tot : '<span class="text-slate-400">—</span>'}</td>
                                        <td class="p-1.5 text-center text-pink-400">${s.fem > 0 ? s.fem : '<span class="text-slate-400">—</span>'}</td>
                                        <td class="p-1.5 text-xs text-slate-400">${s.phone}</td>
                                    </tr>
                                `).join('')}
                            </tbody>
                        </table>
                    </div>
                </div>
            `;
        }

        function renderFinance() {
            dashboardContent.innerHTML = `
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <div class="card p-4">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">សង្ខេបចំណាយ (មករា–មិថុនា ២០២៦)</h3>
                        ${[
                            { l:"សំណង់ថ្មី",         v:"0 ៛",          src:"—",          c:"gray" },
                            { l:"ជួសជុល",            v:"0 ៛",          src:"SOF",         c:"gray" },
                            { l:"សង្ហារឹម + កែលម្អ", v:"923,100 ៛",   src:"SOF",         c:"yellow" },
                            { l:"សម្ភារៈការិយាល័យ",  v:"2,358,400 ៛", src:"SOF",         c:"blue" },
                            { l:"សរុបចំណាយរួម",      v:"3,281,500 ៛", src:"SOF+សហគមន៍", c:"green" }
                        ].map(i => `
                            <div class="flex justify-between items-center py-2.5 border-b border-slate-700">
                                <div>
                                    <div class="text-sm text-slate-100">${i.l}</div>
                                    <div class="text-[10px] text-slate-400">${i.src}</div>
                                </div>
                                <div class="text-sm font-bold text-${i.c}-400">${i.v}</div>
                            </div>
                        `).join('')}
                    </div>

                    <div class="card p-4">
                        <h3 class="text-xs font-semibold text-slate-300 mb-3 border-l-3 border-yellow-400 pl-2">ចំណែក% ចំណាយ</h3>
                        <div class="chart-container">
                            <canvas id="pie-chart-finance"></canvas>
                        </div>
                        <div class="bg-blue-900/20 rounded-lg p-3 mt-3 text-xs text-slate-400 leading-relaxed">
                            💡 ប្រភព: SOF + សហគមន៍ + សប្បុរសជន + អង្គការទស្សនៈពិភពលោក
                        </div>
                    </div>
                </div>
            `;

            renderPieChartFinance();
        }

        function renderPieChartFinance() {
            const ctx = document.getElementById('pie-chart-finance').getContext('2d');
            new Chart(ctx, {
                type: 'pie',
                data: {
                    labels: ['សង្ហារឹម', 'ការិយាល័យ'],
                    datasets: [{
                        data: [923100, 2358400],
                        backgroundColor: ['#f59e0b', '#3b82f6'],
                        borderWidth: 0
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            labels: {
                                font: {
                                    size: 10
                                }
                            }
                        }
                    }
                }
            });
        }
    </script>

<script defer="" src="https://static.cloudflareinsights.com/beacon.min.js/v833ccba57c9e4d2798f2e76cebdd09a11778172276447" integrity="sha512-57MDmcccJXYtNnH+ZiBwzC4jb2rvgVCEokYN+L/nLlmO8rfYT/gIpW2A569iJ/3b+0UEasghjuZH/ma3wIs/EQ==" data-cf-beacon="{&quot;version&quot;:&quot;2024.11.0&quot;,&quot;token&quot;:&quot;e3c1c9af36de41759418005494a48906&quot;,&quot;r&quot;:1,&quot;server_timing&quot;:{&quot;name&quot;:{&quot;cfCacheStatus&quot;:true,&quot;cfEdge&quot;:true,&quot;cfExtPri&quot;:true,&quot;cfL4&quot;:true,&quot;cfOrigin&quot;:true,&quot;cfSpeedBrain&quot;:true},&quot;location_startswith&quot;:null}}" crossorigin="anonymous"></script>
</template>
<template id="tpl-attendance">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=0.85">
    <title>សាលាបឋមសិក្សា រោគ - Dashboard</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Khmer:wght@400;500;600;700&amp;display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <!-- ExcelJS + FileSaver for attendance Excel export -->
    <script src="https://cdn.jsdelivr.net/npm/exceljs/dist/exceljs.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/file-saver@2.0.5/dist/FileSaver.min.js"></script>
    <!-- Firebase -->
    <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-database-compat.js"></script>
    <style>
        * { box-sizing: border-box; }
        body { font-family: 'Noto Sans Khmer', sans-serif; margin: 0; padding: 0; }

        /* ──────── PRINT STYLES ──────── */
        @media print {
            @page { size: A4 landscape; margin: 8mm; }
            html, body { width: 100%; height: 100%; background: white; color: #000; margin: 0; padding: 8mm; }
            .no-print { display: none !important; }
            h1 { text-align: center; font-size: 16pt !important; font-weight: 700 !important; margin: 8pt 0 4pt 0 !important; line-height: 1.3 !important; color: #000 !important; }
            h2 { text-align: center; font-size: 13pt !important; font-weight: 600 !important; margin: 6pt 0 3pt 0 !important; line-height: 1.2 !important; color: #000 !important; }
            h3 { text-align: center; font-size: 14pt !important; font-weight: 700 !important; margin: 10pt 0 8pt 0 !important; line-height: 1.4 !important; color: #1a3a52 !important; }
            table { width: 100% !important; border-collapse: collapse !important; margin: 10pt 0 !important; page-break-inside: avoid !important; }
            thead { display: table-header-group !important; }
            tr { page-break-inside: avoid !important; }
            th { background-color: #d3d3d3 !important; color: #000 !important; border: 1.0pt solid #000 !important; padding: 6pt 4pt !important; font-size: 11pt !important; font-weight: 700 !important; text-align: center !important; vertical-align: middle !important; }
            td { border: 1pt solid #000 !important; padding: 5pt 4pt !important; font-size: 10pt !important; color: #000 !important; text-align: center !important; vertical-align: middle !important; word-wrap: break-word !important; }
            td.text-left { text-align: left !important; padding-left: 8pt !important; }
            .font-bold { font-weight: 700 !important; }
            .text-center { text-align: center !important; }
            .kpi-card { page-break-inside: avoid !important; border: 1pt solid #000 !important; padding: 8pt !important; margin-bottom: 8pt !important; display: block !important; }
            .kpi-value { font-size: 16pt !important; font-weight: 700 !important; color: #000 !important; }
            .kpi-label { font-size: 10pt !important; color: #333 !important; margin-top: 3pt !important; }
            .chart-container { page-break-inside: avoid !important; margin: 10pt 0 !important; text-align: center !important; }
            canvas { max-width: 100% !important; height: auto !important; }
            .badge { display: inline-block !important; padding: 2pt 4pt !important; border: 1pt solid #666 !important; font-size: 9pt !important; font-weight: 600 !important; border-radius: 2pt !important; background: #f5f5f5 !important; color: #000 !important; }
            .percentage { font-size: 12pt !important; font-weight: 700 !important; color: #000 !important; }
            .footer { margin-top: 10pt !important; padding-top: 8pt !important; border-top: 1pt solid #999 !important; font-size: 9pt !important; text-align: center !important; color: #333 !important; }
            .grid-2col { display: grid !important; grid-template-columns: 1fr 1fr !important; gap: 8pt !important; page-break-inside: avoid !important; }
            .grid-3col { display: grid !important; grid-template-columns: 1fr 1fr 1fr !important; gap: 8pt !important; page-break-inside: avoid !important; }
            .section-header { background-color: #e0e0e0 !important; border-left: 4pt solid #1a3a52 !important; padding: 6pt 8pt !important; margin: 12pt 0 8pt 0 !important; font-size: 11pt !important; font-weight: 700 !important; color: #000 !important; }
            .separator { border-top: 1pt solid #999 !important; margin: 8pt 0 !important; }
            .mb-3 { margin-bottom: 8pt !important; }
            .mt-2 { margin-top: 6pt !important; }
            .highlight-pass { color: #0d6e2e !important; font-weight: 700 !important; }
            .highlight-fail { color: #8b0000 !important; font-weight: 700 !important; }
            * { color: #000 !important; -webkit-print-color-adjust: exact !important; print-color-adjust: exact !important; }
            a { color: #0000ff !important; text-decoration: underline !important; }
        }

        /* ──────── SCREEN STYLES ──────── */
        .gradient-bg { background: linear-gradient(135deg, #0b1628 0%, #111f35 100%); }
        .card { background-color: #111f35; border: 1px solid #1c3356; border-radius: 12px; }
        .tab-active { border-bottom: 2px solid #f59e0b !important; color: #f59e0b !important; }
        .kpi-card { background-color: #111f35; border: 1px solid #1c3356; border-radius: 12px; padding: 16px; display: flex; align-items: center; gap: 14px; }
        .chart-container { position: relative; height: 210px; }
        .progress-bar { height: 6px; border-radius: 4px; }
        .tag { background-color: rgba(37,99,235,.13); color: #2563eb; border: 1px solid rgba(37,99,235,.27); border-radius: 4px; padding: 1px 7px; font-size: 10px; font-weight: 700; }
        .tag-green { background-color: rgba(16,185,129,.13); color: #10b981; border: 1px solid rgba(16,185,129,.27); }
        .tag-red { background-color: rgba(239,68,68,.13); color: #ef4444; border: 1px solid rgba(239,68,68,.27); }
        .tag-orange { background-color: rgba(245,158,11,.13); color: #f59e0b; border: 1px solid rgba(245,158,11,.27); }
        .status-badge { border-radius: 4px; padding: 1px 6px; font-weight: 700; font-size: 10px; }
        .status-green { background-color: rgba(16,185,129,.13); color: #10b981; }
        .status-red { background-color: rgba(239,68,68,.13); color: #ef4444; }
        .table-row:nth-child(even) { background-color: rgba(13,31,51,.05); }
        .table-row:hover { background-color: rgba(13,31,51,.1); }

        #loading-overlay { position: fixed; inset: 0; background: rgba(11,22,40,.85); z-index: 999; display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 12px; }
        .spinner { width: 40px; height: 40px; border: 3px solid #1c3356; border-top-color: #f59e0b; border-radius: 50%; animation: spin .8s linear infinite; }
        @keyframes spin { to { transform: rotate(360deg); } }
        .fb-dot { width: 8px; height: 8px; border-radius: 50%; display: inline-block; }
        .fb-live { background: #10b981; animation: pulse 2s infinite; }
        .fb-off  { background: #ef4444; }
        @keyframes pulse { 0%,100%{opacity:1} 50%{opacity:.4} }

        /* ──── ATTENDANCE STYLES ──── */
        .att-sig-container {
            cursor: pointer; background: #fffde7; border: 1px dashed #b45309;
            padding: 2px; min-height: 42px; display: flex; align-items: center;
            justify-content: center; border-radius: 4px; transition: background 0.2s;
        }
        .att-sig-container:hover { background: #fef9c3; }
        .att-sig-img { max-width: 100%; max-height: 46px; display: none; }
        .att-sig-placeholder { color: #b45309; font-size: 8px; }
        .att-sig-container.locked { cursor: not-allowed; background: #f1f5f9; border: 1px dashed #94a3b8; }
        .att-sig-container.locked .att-sig-placeholder { color: #94a3b8; }
        .att-sig-container.locked:hover { background: #f1f5f9; }
        .att-sig-container.open-now { background: #dcfce7; border: 1.5px dashed #16a34a; animation: pulse-green 2s infinite; }
        .att-sig-container.open-now .att-sig-placeholder { color: #16a34a; }
        @keyframes pulse-green { 0%, 100% { box-shadow: 0 0 0 0 rgba(22,163,74,0.3); } 50% { box-shadow: 0 0 0 4px rgba(22,163,74,0.1); } }
        .att-time-badge { display: inline-block; font-size: 9px; padding: 1px 5px; border-radius: 3px; margin-left: 4px; font-weight: 600; }
        .att-time-badge.open  { background: #dcfce7; color: #15803d; }
        .att-time-badge.closed { background: #fee2e2; color: #b91c1c; }
        input.att-note { width: 95%; padding: 2px; border: 1px solid #ccc; border-radius: 4px; background: transparent; text-align: left; font-size: 11px; }
    </style>



<!-- Loading Overlay -->
<div id="loading-overlay">
    <div class="spinner"></div>
    <div class="text-xs text-slate-400">កំពុងភ្ជាប់ Firebase…</div>
</div>

<!-- Login Page -->
<div id="login-page" class="hidden min-h-screen flex items-center justify-center">
    <div class="absolute inset-0 opacity-4 bg-[radial-gradient(circle,#2563eb_1px,transparent_1px)] bg-[length:30px_30px] pointer-events-none"></div>
    <div class="w-full max-w-md p-5">
        <div class="text-center mb-7">
            <div class="w-18 h-18 rounded-2xl mx-auto mb-3 bg-gradient-to-br from-blue-800 to-blue-900 border-2 border-blue-600 flex items-center justify-center text-3xl shadow-lg">🏫</div>
            <div class="text-sm font-bold">ប្រព័ន្ធគ្រប់គ្រងអប់រំ</div>
            <div class="text-xs text-slate-400 mt-1">សាលាបឋមសិក្សា រោគ · ឆមាសទី១ · ២០២៥–២០២៦</div>
        </div>
        <div class="card p-6">
            <div class="text-sm font-bold mb-4">🔐 ចូលប្រព័ន្ធ</div>
            <div class="mb-3">
                <div class="text-xs text-slate-400 mb-1">👤 ឈ្មោះអ្នកប្រើ</div>
                <input id="username" type="text" placeholder="username" class="w-full bg-gray-900 border border-slate-600 rounded-lg px-4 py-2 text-sm focus:outline-none focus:border-blue-500">
            </div>
            <div class="mb-4">
                <div class="text-xs text-slate-400 mb-1">🔒 ពាក្យសម្ងាត់</div>
                <input id="password" type="password" placeholder="password" class="w-full bg-gray-900 border border-slate-600 rounded-lg px-4 py-2 text-sm focus:outline-none focus:border-blue-500">
            </div>
            <div id="error-message" class="hidden bg-red-900/20 border border-red-600/40 rounded-lg px-3 py-2 text-xs text-red-400 mb-3">ឈ្មោះ ឬ ពាក្យសម្ងាត់មិនត្រូវ</div>
            <button id="login-btn" class="w-full bg-blue-600 hover:bg-blue-700 text-white rounded-lg px-4 py-3 text-sm font-bold transition duration-200 disabled:opacity-75">ចូលប្រព័ន្ធ →</button>
            <div class="mt-4 bg-gray-900 border border-slate-600 rounded-lg p-3">
                <div class="text-xs text-slate-400 mb-2 font-semibold">🔑 គណនីសាកល្បង</div>
                <div class="flex flex-wrap gap-1.5">
                    <button data-user="admin" data-pass="admin123" class="bg-blue-600/20 border border-blue-600/40 text-blue-400 rounded-md px-2 py-1 text-xs font-bold">Admin</button>
                    <button data-user="director" data-pass="director123" class="bg-green-600/20 border border-green-600/40 text-green-400 rounded-md px-2 py-1 text-xs font-bold">នាយិកា</button>
                    <button data-user="teacher" data-pass="teacher123" class="bg-yellow-600/20 border border-yellow-600/40 text-yellow-400 rounded-md px-2 py-1 text-xs font-bold">គ្រូបង្រៀន</button>
                </div>
            </div>
        </div>
        <div class="text-center mt-4 text-xs text-slate-400">២០២៦ · ការិយាល័យអប់រំ ស្រុកភ្នំស្រុក</div>
    </div>
</div>

<!-- Dashboard Page -->
<div id="dashboard-page" class="hidden min-h-screen">
    <!-- Top Bar -->
    <div class="bg-gray-800 border-b border-slate-600 p-3 flex items-center justify-between">
        <div>
            <div class="text-sm font-bold">🏫 Dashboard · សាលាបឋមសិក្សា រោគ</div>
            <div class="text-xs text-slate-400">ឆមាសទី១ ២០២៥–២០២៦ · ស្ពានស្រែង · ភ្នំស្រុក</div>
        </div>
        <div class="flex items-center gap-2.5">
            <div id="fb-status" class="flex items-center gap-1.5 bg-gray-900 rounded-md px-2 py-1">
                <span class="fb-dot fb-off" id="fb-dot"></span>
                <span class="text-xs text-slate-400" id="fb-label">Firebase</span>
            </div>
            <div class="text-right">
                <div id="user-name" class="text-xs font-bold text-yellow-400"></div>
                <div id="user-role-tag" class="tag">role</div>
            </div>
            <button id="logout-btn" class="bg-red-900/20 border border-red-600/40 text-red-400 rounded-md px-3 py-1.5 text-xs font-bold hover:bg-red-900/30 transition">ចេញ</button>
            <button onclick="window.print()" class="bg-blue-900/20 border border-blue-600/40 text-blue-400 rounded-md px-3 py-1.5 text-xs font-bold hover:bg-blue-900/30 transition no-print">🖨️ ព្រីន</button>
        </div>
    </div>

    <!-- Tab Bar — FIX: added tab-attendance -->
    <div class="bg-gray-800 border-b border-slate-600 flex overflow-x-auto p-0">
        <button onclick="setActiveTab('overview')" id="tab-overview" class="bg-transparent border-b-2 border-transparent text-slate-400 hover:text-yellow-400 px-3.5 py-2.5 text-xs font-semibold flex items-center gap-1.5">📊 ទិដ្ឋភាព</button>
        <button onclick="setActiveTab('students')" id="tab-students" class="bg-transparent border-b-2 border-transparent text-slate-400 hover:text-yellow-400 px-3.5 py-2.5 text-xs font-semibold flex items-center gap-1.5">👩‍🎓 សិស្ស</button>
        <button onclick="setActiveTab('results')" id="tab-results" class="bg-transparent border-b-2 border-transparent text-slate-400 hover:text-yellow-400 px-3.5 py-2.5 text-xs font-semibold flex items-center gap-1.5">📈 លទ្ធផល</button>
        <button onclick="setActiveTab('staff')" id="tab-staff" class="bg-transparent border-b-2 border-transparent text-slate-400 hover:text-yellow-400 px-3.5 py-2.5 text-xs font-semibold flex items-center gap-1.5">👨‍🏫 បុគ្គលិក</button>
        <button onclick="setActiveTab('finance')" id="tab-finance" class="bg-transparent border-b-2 border-transparent text-slate-400 hover:text-yellow-400 px-3.5 py-2.5 text-xs font-semibold flex items-center gap-1.5">💰 ហិរញ្ញ</button>
        <button onclick="setActiveTab('attendance')" id="tab-attendance" class="bg-transparent border-b-2 border-transparent text-slate-400 hover:text-yellow-400 px-3.5 py-2.5 text-xs font-semibold flex items-center gap-1.5">🔥 វត្តមាន</button>
    </div>

    <div id="dashboard-content" class="p-4"></div>

    <div class="text-center p-2.5 text-xs text-slate-400 border-t border-slate-600 no-print">
        ២៤ មេសា ២០២៦ · អ្នកធ្វើរបាយការណ៍: អ៊ុន ប៊ុនទុង · Firebase: packagedemo-b600c
    </div>
</div>

<!-- ═══════════════════════════════════════════════════════════ -->
<script>
/* ─────────────── FIREBASE INIT ─────────────── */
firebase.initializeApp({
    apiKey:            "AIzaSyB35WLr1y5_QT3j-0x7Mb2F7QaaYXLdIcQ",
    authDomain:        "packagedemo-b600c.firebaseapp.com",
    databaseURL:       "https://packagedemo-b600c-default-rtdb.asia-southeast1.firebasedatabase.app",
    projectId:         "packagedemo-b600c",
    storageBucket:     "packagedemo-b600c.firebasestorage.app",
    messagingSenderId: "601958630212",
    appId:             "1:601958630212:web:e140ee683e203f3e464d11"
});
var db = firebase.database();

/* ─────────────── GLOBAL HELPERS ─────────────── */
function toKhmer(n) {
    return String(n).replace(/[0-9]/g, function(d) { return '០១២៣៤៥៦៧៨៩'[d]; });
}

/* ─────────────── GLOBAL STATE ─────────────── */
var gradeData      = [];
var curriculumData = [];
var currentUser    = null;
var activeTabId    = 'overview';
var fbConnected    = false;
var attClockInterval = null;   // tracks attendance clock so it can be cleared

/* ─────────────── DASHBOARD STAFF (5 admin) ─────────────── */
var staffList = [
    { id:"01", name:"សុខ សារើន",    g:"ស្រី", rank:"គ្រូបឋម", edu:"ថ្នាក់ទី១២",      role:"នាយិកា",    cls:"-",  tot:0,  fem:0,  phone:"089663966" },
    { id:"02", name:"យ៉េន សារី",    g:"ប្រុស", rank:"គ្រូបឋម", edu:"ថ្នាក់ទី១២",      role:"នាយករង",   cls:"-",  tot:0,  fem:0,  phone:"085246698" },
    { id:"03", name:"អ៊ុន ប៊ុនទុង", g:"ប្រុស", rank:"គ្រូបឋម", edu:"ស.បរិញ្ញាបត្រ",   role:"លេខាធិការ", cls:"-",  tot:0,  fem:0,  phone:"017407773" },
    { id:"04", name:"រ៉ែម សុភក្ដិ",  g:"ស្រី", rank:"គ្រូបឋម", edu:"ស.ទុតិយភូមិ",     role:"គ្រូបង្រៀន",      cls:"1A", tot:30, fem:14, phone:"0444555666" },
    { id:"05", name:"ស្វាង មនោរម្យ", g:"ស្រី", rank:"គ្រូបឋម", edu:"ស.បរិញ្ញាបត្រ",   role:"គ្រូបង្រៀន",      cls:"5A", tot:25, fem:12, phone:"0976858898" },
];

/* ─────────────── ATTENDANCE STAFF (16 people) ─────────────── */
var attStaff = [
    { name:'យ៉េន សារី',    gender:'ប្រុស', position:'នាយករង',    cls:'-'   },
    { name:'អ៊ុន ប៊ុនទុង',   gender:'ប្រុស', position:'លេខាធិការ',  cls:'-'   },
    { name:'រ៉ែម សុភក្ដិ',   gender:'ស្រី',  position:'ថ្នាក់',     cls:'1A'  },
    { name:'ស្វាង មនោរម្យ',  gender:'ស្រី',  position:'ថ្នាក់',     cls:'5A'  },
    { name:'ប៉ោង ស្រីពេជ្រ', gender:'ស្រី',  position:'ថ្នាក់',     cls:'2A'  },
    { name:'លេង ចាន់លាវ',   gender:'ស្រី',  position:'ថ្នាក់',     cls:'2B'  },
    { name:'អែង ផល្លែន',    gender:'ស្រី',  position:'ថ្នាក់',     cls:'3B'  },
    { name:'ប៊ី ពិសី',       gender:'ស្រី',  position:'ថ្នាក់',     cls:'3A'  },
    { name:'អឿន សុខៀប',    gender:'ស្រី',  position:'ថ្នាក់',     cls:'4B'  },
    { name:'ឆេន សាវដា',    gender:'ស្រី',  position:'ថ្នាក់',     cls:'4A'  },
    { name:'រ៉ោម សម្ផស្ស',  gender:'ប្រុស', position:'ថ្នាក់',     cls:'5B'  },
    { name:'ឈួត សេរ៉ូម',   gender:'ស្រី',  position:'ថ្នាក់',     cls:'6A'  },
    { name:'កែវ ខន',        gender:'ប្រុស', position:'កសិកម្ម',    cls:'-'   },
    { name:'លន់ ចាន់នឹក',   gender:'ស្រី',  position:'បណ្ណារក្ស',  cls:'-'   },
    { name:'ពាន ណូរ៉ា',     gender:'ស្រី',  position:'ថ្នាក់',     cls:'ម.ត' },
    { name:'ឡុក ម៉ាក់តី',   gender:'ស្រី',  position:'ថ្នាក់',     cls:'ម.ត' },
];

/* ─────────────── ATTENDANCE TIME WINDOWS ─────────────── */
var ATT_TIME_WINDOWS = [
    { key:'m_in',  label:'ព្រឹក-ចូល',  startH:7,  startM:0,  endH:8,  endM:30 },
    { key:'m_out', label:'ព្រឹក-ចេញ',  startH:10, startM:30, endH:12, endM:0  },
    { key:'a_in',  label:'រសៀល-ចូល',  startH:13, startM:0,  endH:14, endM:30 },
    { key:'a_out', label:'រសៀល-ចេញ',  startH:16, startM:30, endH:18, endM:0  },
];

/* ─────────────── ACCOUNTS ─────────────── */
var accounts = [
    { user:"admin",    pass:"admin123",    role:"admin",    name:"អ្នកគ្រប់គ្រង" },
    { user:"director", pass:"director123", role:"director", name:"សុខ សារើន (នាយិកា)" },
    { user:"teacher",  pass:"teacher123",  role:"teacher",  name:"លោកគ្រូ / អ្នកគ្រូ" },
];

/* ══════════════════════════════════════════════════════════════
   FIREBASE LOAD
══════════════════════════════════════════════════════════════ */
function loadFromFirebase() {
    db.ref('teacherData').on('value', function(snap) {
        gradeData = [
            { grade:'ទី1A', total:30, female:14, pass:28, fail:2,  teacher:"រ៉ែម សុភក្ដិ"  },
            { grade:'ទី2A', total:21, female:10, pass:20, fail:1,  teacher:"ប៉ោង ស្រីពេជ្រ" },
            { grade:'ទី2B', total:21, female:10, pass:20, fail:1,  teacher:"លេង ចាន់លាវ" },      
{ grade:'ទី3B', total:21, female:10, pass:20, fail:1,  teacher:"អែង ផល្លែន" },
{ grade:'ទី3A', total:20, female:10, pass:19, fail:1,  teacher:"ប៊ី ពិសី" },
            { grade:'ទី4B', total:24, female:12, pass:22, fail:2,  teacher:"អឿន សុខៀប" },
  { grade:'ទី4A', total:25, female:14, pass:23, fail:2,  teacher:"ឆេន សាវដា" },
            { grade:'ទី5A', total:25, female:13, pass:17, fail:8,  teacher:"ស្វាង មនោរម្យ"  },
{ grade:'ទី5B', total:25, female:11, pass:23, fail:2,  teacher:"រ៉ោម សម្ផស្ស"  },
            { grade:'ទី6A', total:35, female:17, pass:33, fail:2,  teacher:"ឈួត សេរ៉ូម" },
        ];
        curriculumData = [
            { subject:'ភាសាខ្មែរ',    avg:75 },
            { subject:'គណិត',    avg:68 },
            { subject:'វិទ្យាសាស្ត្រ',   avg:71 },
            { subject:'សិក្សាសង្គម',   avg:80 },
            { subject:'អង់គ្លេស', avg:52 },
        ];

        fbConnected = true;
        document.getElementById('fb-dot').className    = 'fb-dot fb-live';
        document.getElementById('fb-label').textContent = 'Live';

        if (!document.getElementById('dashboard-page').classList.contains('hidden')) {
            renderDashboardContent(activeTabId);
        }
        document.getElementById('loading-overlay').style.display = 'none';
        document.getElementById('login-page').classList.remove('hidden');

    }, function(err) {
        console.warn('Firebase error:', err);
        document.getElementById('loading-overlay').style.display = 'none';
        document.getElementById('login-page').classList.remove('hidden');
        document.getElementById('fb-dot').className    = 'fb-dot fb-off';
        document.getElementById('fb-label').textContent = 'Offline';
    });
}

/* ══════════════════════════════════════════════════════════════
   DOM READY
══════════════════════════════════════════════════════════════ */
document.addEventListener('DOMContentLoaded', function() {
    loadFromFirebase();

    document.getElementById('login-btn').addEventListener('click', handleLogin);
    document.getElementById('password').addEventListener('keydown', function(e) {
        if (e.key === 'Enter') handleLogin();
    });
    document.querySelectorAll('[data-user]').forEach(function(btn) {
        btn.addEventListener('click', function() {
            document.getElementById('username').value = this.dataset.user;
            document.getElementById('password').value = this.dataset.pass;
        });
    });
    document.getElementById('logout-btn').addEventListener('click', function() {
        stopAttClock();
        currentUser = null;
        document.getElementById('login-page').classList.remove('hidden');
        document.getElementById('dashboard-page').classList.add('hidden');
    });
});

/* ══════════════════════════════════════════════════════════════
   AUTH
══════════════════════════════════════════════════════════════ */
function handleLogin() {
    var u = document.getElementById('username').value.trim();
    var p = document.getElementById('password').value.trim();
    if (!u || !p) { showError('សូមបញ្ចូលឈ្មោះអ្នកប្រើ និងពាក្យសម្ងាត់'); return; }
    var btn = document.getElementById('login-btn');
    btn.disabled = true; btn.textContent = '⏳ កំពុងចូល...';
    setTimeout(function() {
        var acc = accounts.find(function(a) { return a.user === u && a.pass === p; });
        if (acc) {
            currentUser = acc;
            showDashboard();
        } else {
            showError('ឈ្មោះ ឬ ពាក្យសម្ងាត់មិនត្រូវ!');
            btn.disabled = false; btn.textContent = 'ចូលប្រព័ន្ធ →';
        }
    }, 600);
}

function showError(msg) {
    var el = document.getElementById('error-message');
    el.textContent = msg; el.classList.remove('hidden');
    setTimeout(function() { el.classList.add('hidden'); }, 3000);
}

function showDashboard() {
    document.getElementById('login-page').classList.add('hidden');
    document.getElementById('dashboard-page').classList.remove('hidden');
    populateDashboard();
    setActiveTab('overview');
}

function populateDashboard() {
    document.getElementById('user-name').textContent = currentUser.name;
    var roleTag = document.getElementById('user-role-tag');
    switch (currentUser.role) {
        case 'admin':    roleTag.textContent = 'admin';   roleTag.className = 'tag';          break;
        case 'director': roleTag.textContent = 'នាយិកា'; roleTag.className = 'tag tag-green'; break;
        case 'teacher':  roleTag.textContent = 'គ្រូបង្រៀន';    roleTag.className = 'tag tag-orange'; break;
    }
}

/* ══════════════════════════════════════════════════════════════
   TABS — FIX 1: 'attendance' added to tab list
         FIX 2: attendance clock stopped when leaving tab
══════════════════════════════════════════════════════════════ */
function setActiveTab(tabId) {
    // Stop clock if navigating away from attendance
    if (tabId !== 'attendance') stopAttClock();

    activeTabId = tabId;
    ['overview','students','results','staff','finance','attendance'].forEach(function(id) {
        var el = document.getElementById('tab-' + id);
        if (!el) return;
        if (id === tabId) el.classList.add('tab-active');
        else              el.classList.remove('tab-active');
    });
    renderDashboardContent(tabId);
}

/* ══════════════════════════════════════════════════════════════
   RENDER DISPATCHER — FIX 3: broken switch/brace fixed,
                               finance shows "no access" for teachers
══════════════════════════════════════════════════════════════ */
function renderDashboardContent(tabId) {
    switch (tabId) {
        case 'overview':
            renderOverview();
            break;
        case 'students':
            renderStudents();
            break;
        case 'results':
            renderResults();
            break;
        case 'staff':
            renderStaff();
            break;
        case 'finance':
            if (currentUser && currentUser.role !== 'teacher') {
                renderFinance();
            } else {
                document.getElementById('dashboard-content').innerHTML =
                    '<div class="card p-6 text-center text-slate-400 text-sm">🔒 មិនមានសិទ្ធចូលមើលផ្នែកហិរញ្ញវត្ថុ</div>';
            }
            break;
        case 'attendance':
            renderAttendance();
            break;
    }
}

/* ══════════════════════════════════════════════════════════════
   RENDER: OVERVIEW
══════════════════════════════════════════════════════════════ */
function renderOverview() {
    var totalS    = gradeData.reduce(function(a,g){ return a+g.total;  }, 0);
    var totalF    = gradeData.reduce(function(a,g){ return a+g.female; }, 0);
    var totalPass = gradeData.reduce(function(a,g){ return a+g.pass;   }, 0);
    var totalFail = gradeData.reduce(function(a,g){ return a+g.fail;   }, 0);
    var passPct   = totalS > 0 ? ((totalPass/totalS)*100).toFixed(1) : "0";
    var femPct    = totalS > 0 ? ((totalF/totalS)*100).toFixed(1)    : "0";

    document.getElementById('dashboard-content').innerHTML = `
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-3 mb-4">
            <div class="kpi-card">
                <div class="w-12 h-12 rounded-xl flex items-center justify-center text-2xl bg-blue-600/20 border border-blue-600/40">👩‍🎓</div>
                <div>
                    <div class="text-2xl font-bold text-blue-400">${totalS}</div>
                    <div class="text-xs font-semibold text-slate-300 mt-1">សិស្សសរុប</div>
                    <div class="text-xs text-slate-400 mt-1">ស្រី ${totalF} · ${femPct}%</div>
                </div>
            </div>
            <div class="kpi-card">
                <div class="w-12 h-12 rounded-xl flex items-center justify-center text-2xl bg-green-600/20 border border-green-600/40">✅</div>
                <div>
                    <div class="text-2xl font-bold text-green-400">${passPct}%</div>
                    <div class="text-xs font-semibold text-slate-300 mt-1">% ជាប់</div>
                    <div class="text-xs text-slate-400 mt-1">ជាប់ ${totalPass} · ធ្លាក់ ${totalFail}</div>
                </div>
            </div>
            <div class="kpi-card">
                <div class="w-12 h-12 rounded-xl flex items-center justify-center text-2xl bg-yellow-600/20 border border-yellow-600/40">🏫</div>
                <div>
                    <div class="text-2xl font-bold text-yellow-400">${gradeData.length}</div>
                    <div class="text-xs font-semibold text-slate-300 mt-1">ថ្នាក់សរុប</div>
                    <div class="text-xs text-slate-400 mt-1">ទី១–ទី៦</div>
                </div>
            </div>
            <div class="kpi-card">
                <div class="w-12 h-12 rounded-xl flex items-center justify-center text-2xl bg-pink-600/20 border border-pink-600/40">👨‍🏫</div>
                <div>
                    <div class="text-2xl font-bold text-pink-400">${attStaff.length}</div>
                    <div class="text-xs font-semibold text-slate-300 mt-1">បុគ្គលិកសរុប</div>
                    <div class="text-xs text-slate-400 mt-1">ស្ត្រី ${attStaff.filter(function(s){return s.gender==='ស្រី';}).length} នាក់</div>
                </div>
            </div>
        </div>
        <div class="card p-4">
            <h3 class="text-xs font-semibold text-slate-300 mb-3 pl-2 border-l-2 border-yellow-400">ទិដ្ឋភាពចំណាយ</h3>
            <div class="space-y-2">
                <div class="flex justify-between py-2 border-b border-slate-700 text-xs"><span class="text-slate-300">សង្ហារឹម + កែលម្អ</span><span class="font-bold text-yellow-400">923,100 ៛</span></div>
                <div class="flex justify-between py-2 border-b border-slate-700 text-xs"><span class="text-slate-300">ការិយាល័យ</span><span class="font-bold text-blue-400">2,358,400 ៛</span></div>
                <div class="flex justify-between py-2 text-xs font-bold"><span class="text-slate-300">សរុប</span><span class="text-green-400">3,281,500 ៛</span></div>
            </div>
        </div>`;
}

/* ══════════════════════════════════════════════════════════════
   RENDER: STUDENTS
══════════════════════════════════════════════════════════════ */
function renderStudents() {
    var totalS    = gradeData.reduce(function(a,g){return a+g.total;}, 0);
    var totalF    = gradeData.reduce(function(a,g){return a+g.female;}, 0);
    var totalPass = gradeData.reduce(function(a,g){return a+g.pass;}, 0);
    var totalFail = gradeData.reduce(function(a,g){return a+g.fail;}, 0);

    document.getElementById('dashboard-content').innerHTML = `
        <div class="card p-4 mb-4">
            <h3 class="text-xs font-semibold text-slate-300 mb-3 pl-2 border-l-2 border-yellow-400">ចំនួនសិស្ស + លទ្ធផល តាមថ្នាក់</h3>
            <div class="overflow-x-auto">
                <table class="w-full text-xs">
                    <thead>
                        <tr class="text-slate-400">
                            <th class="p-1.5">ថ្នាក់</th>
                            <th class="p-1.5">សរុប</th>
                            <th class="p-1.5">ស្រី</th>
                            <th class="p-1.5">%ស្រី</th>
                            <th class="p-1.5">ជាប់</th>
                            <th class="p-1.5">ធ្លាក់</th>
                            <th class="p-1.5">% ជាប់</th>
                            <th class="p-1.5">ឈ្មោះគ្រូ</th>
                        </tr>
                    </thead>
                    <tbody>
                        ${gradeData.map(function(g) {
                            var pp = g.total > 0 ? (g.pass/g.total*100) : 0;
                            return `<tr class="table-row">
                                <td class="p-1.5 text-center text-yellow-400 font-bold">${g.grade}</td>
                                <td class="p-1.5 text-center font-semibold">${g.total}</td>
                                <td class="p-1.5 text-center text-pink-400">${g.female}</td>
                                <td class="p-1.5 text-center text-slate-400">${g.total>0?((g.female/g.total)*100).toFixed(1):'0'}%</td>
                                <td class="p-1.5 text-center text-green-400">${g.pass}</td>
                                <td class="p-1.5 text-center ${g.fail>0?'text-red-400':'text-slate-400'}">${g.fail}</td>
                                <td class="p-1.5 text-center"><span class="status-badge ${g.fail===0?'status-green':'status-red'}">${Math.round(pp)}%</span></td>
                                <td class="p-1.5 text-center text-slate-300">${g.teacher}</td>
                            </tr>`;
                        }).join('')}
                        <tr class="border-t border-slate-700 font-bold">
                            <td class="p-1.5 text-center text-green-400">សរុប</td>
                            <td class="p-1.5 text-center">${totalS}</td>
                            <td class="p-1.5 text-center text-pink-400">${totalF}</td>
                            <td class="p-1.5 text-center">${totalS>0?((totalF/totalS)*100).toFixed(1):'0'}%</td>
                            <td class="p-1.5 text-center text-green-400">${totalPass}</td>
                            <td class="p-1.5 text-center text-red-400">${totalFail}</td>
                            <td class="p-1.5 text-center"><span class="status-badge status-green">${totalS>0?((totalPass/totalS)*100).toFixed(0):'0'}%</span></td>
                            <td class="p-1.5"></td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>`;
}

/* ══════════════════════════════════════════════════════════════
   RENDER: RESULTS
══════════════════════════════════════════════════════════════ */
function renderResults() {
    document.getElementById('dashboard-content').innerHTML = `
        <div class="card p-4 mb-4">
            <h3 class="text-xs font-semibold text-slate-300 mb-3 pl-2 border-l-2 border-yellow-400">% ការអនុវត្តកម្មវិធីសិក្សា</h3>
            ${curriculumData.map(function(s) {
                var color = s.avg >= 70 ? 'green' : s.avg >= 50 ? 'yellow' : 'red';
                return `<div class="mb-3">
                    <div class="flex justify-between text-xs mb-1">
                        <span>${s.subject}</span>
                        <span class="font-bold text-${color}-400">${s.avg}%</span>
                    </div>
                    <div class="bg-slate-700 rounded progress-bar">
                        <div class="h-full rounded progress-bar bg-${color}-500" style="width:${s.avg}%"></div>
                    </div>
                </div>`;
            }).join('')}
        </div>`;
}

/* ══════════════════════════════════════════════════════════════
   RENDER: STAFF
══════════════════════════════════════════════════════════════ */
function renderStaff() {
    document.getElementById('dashboard-content').innerHTML = `
        <div class="card p-4">
            <h3 class="text-xs font-semibold text-slate-300 mb-3 pl-2 border-l-2 border-yellow-400">បញ្ជីបុគ្គលិក</h3>
            <div class="overflow-x-auto">
                <table class="w-full text-xs">
                    <thead class="bg-gray-900">
                        <tr>
                            <th class="p-1.5">ល.រ</th>
                            <th class="p-1.5">គោត្តនាម នាម</th>
                            <th class="p-1.5">ភេទ</th>
                            <th class="p-1.5">កម្រិតវប្បធម៌</th>
                            <th class="p-1.5">តួនាទី</th>
                            <th class="p-1.5">ថ្នាក់</th>
                            <th class="p-1.5">សិស្ស</th>
                            <th class="p-1.5">ស្រី</th>
                            <th class="p-1.5">ទូរស័ព្ទ</th>
                        </tr>
                    </thead>
                    <tbody>
                        ${staffList.map(function(s) {
                            return `<tr class="table-row">
                                <td class="p-1.5 text-center text-slate-400">${s.id}</td>
                                <td class="p-1.5 style="text-align: left font-semibold;">${s.name}</td>
                                <td class="p-1.5 text-center"><span class="tag ${s.g==='ស'?'tag-red':''}">${s.g}</span></td>
                                <td class="p-1.5 text-xs text-slate-400">${s.edu}</td>
                                <td class="p-1.5"><span class="tag">${s.role}</span></td>
                                <td class="p-1.5 text-center text-yellow-400 font-bold">${s.cls!=='-'?s.cls:'-'}</td>
                                <td class="p-1.5 text-center">${s.tot>0?s.tot:'-'}</td>
                                <td class="p-1.5 text-center text-pink-400">${s.fem>0?s.fem:'-'}</td>
                                <td class="p-1.5 text-xs text-slate-400">${s.phone}</td>
                            </tr>`;
                        }).join('')}
                    </tbody>
                </table>
            </div>
        </div>`;
}

/* ══════════════════════════════════════════════════════════════
   RENDER: FINANCE
══════════════════════════════════════════════════════════════ */
function renderFinance() {
    document.getElementById('dashboard-content').innerHTML = `
        <div class="card p-4">
            <h3 class="text-xs font-semibold text-slate-300 mb-3 pl-2 border-l-2 border-yellow-400">សង្ខេបចំណាយ</h3>
            <div class="space-y-2">
                <div class="flex justify-between py-2 border-b border-slate-700 text-xs"><span class="text-slate-300">សង្ហារឹម + កែលម្អ</span><span class="font-bold text-yellow-400">923,100 ៛</span></div>
                <div class="flex justify-between py-2 border-b border-slate-700 text-xs"><span class="text-slate-300">ការិយាល័យ</span><span class="font-bold text-blue-400">2,358,400 ៛</span></div>
                <div class="flex justify-between py-2 text-xs font-bold"><span class="text-slate-300">សរុប</span><span class="text-green-400">3,281,500 ៛</span></div>
            </div>
        </div>`;
}

/* ══════════════════════════════════════════════════════════════
   ATTENDANCE — HELPERS
══════════════════════════════════════════════════════════════ */
function attIsWindowOpen(win) {
    var now   = new Date();
    var nowM  = now.getHours() * 60 + now.getMinutes();
    var startM = win.startH * 60 + win.startM;
    var endM   = win.endH   * 60 + win.endM;
    return nowM >= startM && nowM <= endM;
}

function attUpdateBadges() {
    ATT_TIME_WINDOWS.forEach(function(w) {
        var el = document.getElementById('att-badge-' + w.key);
        if (!el) return;
        el.className = 'att-time-badge ' + (attIsWindowOpen(w) ? 'open' : 'closed');
    });
}

function attUpdateLockStates() {
    document.querySelectorAll('.att-sig-container').forEach(function(c) {
        var colIdx = parseInt(c.dataset.colIdx);
        var win    = ATT_TIME_WINDOWS[colIdx];
        if (!win) return;
        if (c.dataset.base64 && c.dataset.base64.startsWith('data:image')) return; // already signed
        c.classList.remove('locked','open-now');
        c.classList.add(attIsWindowOpen(win) ? 'open-now' : 'locked');
    });
}

function attConvertKhmerDate(dateInput) {
    var d = new Date(dateInput);
    var days   = ["ថ្ងៃអាទិត្យ","ថ្ងៃច័ន្ទ","ថ្ងៃអង្គារ","ថ្ងៃពុធ","ថ្ងៃព្រហស្បតិ៍","ថ្ងៃសុក្រ","ថ្ងៃសៅរ៍"];
    var months = ["មករា","កុម្ភៈ","មីនា","មេសា","ឧសភា","មិថុនា","កក្កដា","សីហា","កញ្ញា","តុលា","វិច្ឆិកា","ធ្នូ"];
    var dayName   = days[d.getDay()];
    var dayNum    = toKhmer(d.getDate());
    var monthName = months[d.getMonth()];
    var yearNum   = toKhmer(d.getFullYear());
    // solar without day name: ថ្ងៃទី${dayNum} ខែ${monthName} ឆ្នាំ${yearNum}
    var solarNoDay = 'ថ្ងៃទី' + dayNum + ' ខែ' + monthName + ' ឆ្នាំ' + yearNum;

    var titleEl  = document.getElementById('att-full-solar-title');
    var solarEl  = document.getElementById('att-solardate');
    // NOTE: never set headEl.textContent — that wipes the <span> child inside the h3
    if (titleEl) titleEl.textContent = 'សម្រាប់' + solarNoDay;
    if (solarEl) solarEl.textContent = 'រោគ ' + solarNoDay;

    // Lunar
    var baseDate      = new Date("2026-05-13");
    var diffDays      = Math.round((d - baseDate) / 86400000);
    var totalLunarDays = 9 + diffDays;
    while (totalLunarDays <= 0) totalLunarDays += 30;
    var lunarDay = totalLunarDays % 30 || 30;
    var phase    = lunarDay <= 15 ? "កើត" : "រោច";
    var phaseNum = lunarDay <= 15 ? lunarDay : lunarDay - 15 || 15;
    var lunarMonths = { 4:"ជេស្ន", 5:"អាសាឍ", 6:"ស្រាពណ៍", 7:"ភទ្របទ", 8:"អស្សុជ", 9:"កត្តិក", 10:"មិគសិរ", 11:"បុស្ស" };
    var lunarMonth = lunarMonths[d.getMonth()] || "ពិសាខ";
    var lunarEl = document.getElementById('att-lunardate');
    if (lunarEl) lunarEl.textContent = dayName + ' ' + toKhmer(phaseNum) + phase + ' ខែ' + lunarMonth + ' ឆ្នាំមមី អដ្ឋស័ក ព.ស ' + toKhmer(2570);
}

/* ── att sig data ── */
function attSetSigData(container, base64) {
    var img = container.querySelector('.att-sig-img');
    var ph  = container.querySelector('.att-sig-placeholder');
    if (base64 && base64.startsWith('data:image')) {
        img.src = base64; img.style.display = 'block'; ph.style.display = 'none';
        container.dataset.base64 = base64;
        container.classList.remove('locked','open-now');
        container.style.background = '#fffde7';
        container.style.border = '1px dashed #b45309';
        container.style.cursor = 'pointer';
    } else {
        img.src = ''; img.style.display = 'none'; ph.style.display = 'block';
        container.dataset.base64 = '';
        container.style.background = '';
        container.style.border = '';
        container.style.cursor = '';
    }
}

/* ── build one attendance row ── */
function attCreateRow(idx, s) {
    var tr = document.createElement('tr');
    tr.dataset.idx = idx;
    tr.style.borderBottom = '1px solid #e2e8f0';

    function sigCell(colIdx, label) {
        return '<td style="padding:2px;min-width:70px;"><div class="att-sig-container locked" data-col-idx="' + colIdx + '" onclick="attOpenSigModal(this,\'' + ATT_TIME_WINDOWS[colIdx].label + '\',' + colIdx + ')">' +
               '<span class="att-sig-placeholder">✍️ ' + label + '</span>' +
               '<img class="att-sig-img" src="">' +
               '</div></td>';
    }

    tr.innerHTML =
        '<td style="padding:4px;text-align:center;font-size:12px;">' + toKhmer(idx + 1) + '</td>' +
        '<td style="padding:4px;font-weight:700;font-size:12px;white-space:nowrap;">' + s.name + '</td>' +
        '<td style="padding:4px;text-align:center;font-size:12px;">' + s.gender + '</td>' +
        '<td style="padding:4px;font-size:11px;white-space:nowrap;">' + s.position + (s.cls !== '-' ? ' ' + s.cls : '') + '</td>' +
        sigCell(0,'ចូល') + sigCell(1,'ចេញ') + sigCell(2,'ចូល') + sigCell(3,'ចេញ') +
        '<td contenteditable="true" class="att-phone-cell" style="padding:4px;text-align:center;font-size:11px;min-width:90px;"></td>' +
        '<td style="padding:4px;"><input type="text" class="att-note" placeholder="..."></td>';
    return tr;
}

/* ── render the attendance table body ── */
function attRenderTable() {
    var tbody = document.getElementById('att-tbody');
    if (!tbody) return;
    tbody.innerHTML = '';
    attStaff.forEach(function(s, i) { tbody.appendChild(attCreateRow(i, s)); });
    var dateEl = document.getElementById('att-date-input');
    if (dateEl) attConvertKhmerDate(dateEl.value);
    attUpdateLockStates();
}

/* ── load attendance from Firebase ── */
function attLoadData(date) {
    if (!date) return;
    attConvertKhmerDate(date);
    db.ref('attendance/' + date).get().then(function(snap) {
        var val = snap.val() || {};
        var tbody = document.getElementById('att-tbody');
        if (!tbody) return;
        tbody.querySelectorAll('tr').forEach(function(tr) {
            var idx    = tr.dataset.idx;
            var s      = attStaff[idx];
            if (!s) return;
            var record = val[s.name] || {};
            var containers = tr.querySelectorAll('.att-sig-container');
            attSetSigData(containers[0], record.m_in);
            attSetSigData(containers[1], record.m_out);
            attSetSigData(containers[2], record.a_in);
            attSetSigData(containers[3], record.a_out);
            var phoneCell = tr.querySelector('.att-phone-cell');
            var noteInput = tr.querySelector('input.att-note');
            if (phoneCell) phoneCell.textContent = record.phone || '';
            if (noteInput) noteInput.value = record.note || '';
            // Principal sig for print footer
            if (idx == 0 && record.m_in) {
                var pSig = document.getElementById('att-principal-sig');
                if (pSig) { pSig.src = record.m_in; pSig.classList.remove('hidden'); }
            }
        });
        attUpdateLockStates();
    });
}

/* ── clock tick ── */
function attClockTick() {
    var clockEl = document.getElementById('att-clock');
    if (!clockEl) { stopAttClock(); return; }
    var now = new Date();
    clockEl.textContent =
        String(now.getHours()).padStart(2,'0') + ':' +
        String(now.getMinutes()).padStart(2,'0') + ':' +
        String(now.getSeconds()).padStart(2,'0');
    attUpdateBadges();
    attUpdateLockStates();
}

function stopAttClock() {
    if (attClockInterval) { clearInterval(attClockInterval); attClockInterval = null; }
}

/* ══════════════════════════════════════════════════════════════
   ATTENDANCE — SIGNATURE MODAL (global so onclick can call them)
══════════════════════════════════════════════════════════════ */
var attCurrentContainer = null;
var attDrawing          = false;
var attCanvas, attCtx;

function attOpenSigModal(container, type, colIdx) {
    var win = ATT_TIME_WINDOWS[colIdx];
    if (win && !attIsWindowOpen(win)) {
        var sh = toKhmer(String(win.startH).padStart(2,'0'));
        var sm = toKhmer(String(win.startM).padStart(2,'0'));
        var eh = toKhmer(String(win.endH).padStart(2,'0'));
        var em = toKhmer(String(win.endM).padStart(2,'0'));
        alert('🔒 ម៉ោង' + type + ' ត្រូវបានបិទ!\nអាចចុះហត្ថលេខាបានពី ' + sh + ':' + sm + ' ដល់ ' + eh + ':' + em + ' តែប៉ុណ្ណោះ។');
        return;
    }
    attCurrentContainer = container;
    var titleEl = document.getElementById('att-modal-title');
    if (titleEl) titleEl.textContent = 'គូសហត្ថលេខា (' + type + ')';
    attCanvas  = document.getElementById('att-sig-canvas');
    attCtx     = attCanvas.getContext('2d');
    attCtx.lineWidth = 2.5; attCtx.strokeStyle = '#000'; attCtx.lineCap = 'round';
    attCtxClear();
    document.getElementById('att-sig-modal').classList.remove('hidden');
    document.getElementById('att-sig-modal').style.display = 'flex';
}

function attCloseModal() {
    document.getElementById('att-sig-modal').classList.add('hidden');
    document.getElementById('att-sig-modal').style.display = 'none';
}

function attCtxClear() {
    if (attCtx && attCanvas) attCtx.clearRect(0, 0, attCanvas.width, attCanvas.height);
}

function attSaveSignature() {
    if (!attCurrentContainer || !attCanvas) return;
    var base64 = attCanvas.toDataURL();
    attSetSigData(attCurrentContainer, base64);
    // If it's the principal row (idx 0), update print signature
    var parentTr = attCurrentContainer.closest('tr');
    if (parentTr && parentTr.dataset.idx == 0) {
        var pSig = document.getElementById('att-principal-sig');
        if (pSig) { pSig.src = base64; pSig.classList.remove('hidden'); }
    }
    attCloseModal();
}

function attGetCanvasPos(e) {
    var rect    = attCanvas.getBoundingClientRect();
    var clientX = e.touches ? e.touches[0].clientX : e.clientX;
    var clientY = e.touches ? e.touches[0].clientY : e.clientY;
    return { x: clientX - rect.left, y: clientY - rect.top };
}

/* ── save attendance to Firebase ── */
function attSaveData() {
    var dateEl = document.getElementById('att-date-input');
    if (!dateEl || !dateEl.value) { alert('សូមជ្រើសរើសកាលបរិច្ឆេទ!'); return; }
    var dateStr = dateEl.value;
    var data = {};
    var tbody = document.getElementById('att-tbody');
    if (!tbody) return;
    tbody.querySelectorAll('tr').forEach(function(tr) {
        var idx  = tr.dataset.idx;
        var name = attStaff[idx] ? attStaff[idx].name : null;
        if (!name) return;
        var containers = tr.querySelectorAll('.att-sig-container');
        data[name] = {
            m_in:  containers[0] ? (containers[0].dataset.base64 || '') : '',
            m_out: containers[1] ? (containers[1].dataset.base64 || '') : '',
            a_in:  containers[2] ? (containers[2].dataset.base64 || '') : '',
            a_out: containers[3] ? (containers[3].dataset.base64 || '') : '',
            phone: (tr.querySelector('.att-phone-cell') || {}).textContent || '',
            note:  (tr.querySelector('input.att-note') || {}).value || '',
        };
    });
    db.ref('attendance/' + dateStr).set(data)
        .then(function() { alert('💾 បានរក្សាទុករួចរាល់!'); attLoadData(dateStr); })
        .catch(function(e) { alert('កំហុស: ' + e.message); });
}

/* ── Excel export ── */
async function attDownloadExcel() {
    if (typeof ExcelJS === 'undefined' || typeof saveAs === 'undefined') {
        alert('ExcelJS ឬ FileSaver មិនទាន់ load សូមពិនិត្យការតភ្ជាប់អ៊ីនធឺណិត!');
        return;
    }
    var dateEl = document.getElementById('att-date-input');
    var dateStr = dateEl ? dateEl.value : '';
    var workbook  = new ExcelJS.Workbook();
    var worksheet = workbook.addWorksheet('វត្តមាន');

    worksheet.mergeCells('A1:J1');
    worksheet.getCell('A1').value = 'បញ្ជីវត្តមានបុគ្គលិក កាលបរិច្ឆេទ: ' + dateStr;
    worksheet.getCell('A1').font      = { name:'Khmer OS Battambang', size:14, bold:true };
    worksheet.getCell('A1').alignment = { horizontal:'center' };

    worksheet.mergeCells('A3:A4'); worksheet.getCell('A3').value = 'ល.រ';
    worksheet.mergeCells('B3:B4'); worksheet.getCell('B3').value = 'គោត្តនាម-នាម';
    worksheet.mergeCells('C3:C4'); worksheet.getCell('C3').value = 'ភេទ';
    worksheet.mergeCells('D3:D4'); worksheet.getCell('D3').value = 'តួនាទី/ថ្នាក់';
    worksheet.mergeCells('E3:F3'); worksheet.getCell('E3').value = 'ពេលព្រឹក';
    worksheet.getCell('E4').value = 'ចូល'; worksheet.getCell('F4').value = 'ចេញ';
    worksheet.mergeCells('G3:H3'); worksheet.getCell('G3').value = 'ពេលរសៀល';
    worksheet.getCell('G4').value = 'ចូល'; worksheet.getCell('H4').value = 'ចេញ';
    worksheet.mergeCells('I3:I4'); worksheet.getCell('I3').value = 'លេខទូរស័ព្ទ';
    worksheet.mergeCells('J3:J4'); worksheet.getCell('J3').value = 'ផ្សេងៗ';

    ['3','4'].forEach(function(rowNum) {
        worksheet.getRow(rowNum).eachCell(function(cell) {
            cell.fill      = { type:'pattern', pattern:'solid', fgColor:{argb:'2563EB'} };
            cell.font      = { name:'Khmer OS Battambang', bold:true, color:{argb:'FFFFFF'}, size:11 };
            cell.alignment = { horizontal:'center', vertical:'middle' };
            cell.border    = { top:{style:'thin'}, left:{style:'thin'}, bottom:{style:'thin'}, right:{style:'thin'} };
        });
    });

    var tbody = document.getElementById('att-tbody');
    for (var i = 0; i < attStaff.length; i++) {
        var s  = attStaff[i];
        var tr = tbody ? tbody.querySelector('tr[data-idx="' + i + '"]') : null;
        var phoneVal = tr ? (tr.querySelector('.att-phone-cell') || {}).textContent || '' : '';
        var noteVal  = tr ? ((tr.querySelector('input.att-note') || {}).value || '') : '';
        var containers = tr ? tr.querySelectorAll('.att-sig-container') : [];
        var rowIndex = i + 5;

        worksheet.getRow(rowIndex).values = [
            i + 1, s.name, s.gender,
            s.position + (s.cls !== '-' ? ' ' + s.cls : ''),
            '', '', '', '', phoneVal, noteVal
        ];
        worksheet.getRow(rowIndex).height = 32;

        for (var c = 0; c < 4; c++) {
            if (containers[c] && containers[c].dataset.base64 && containers[c].dataset.base64.startsWith('data:image')) {
                var imageId = workbook.addImage({ base64: containers[c].dataset.base64, extension:'png' });
                worksheet.addImage(imageId, { tl:{ col:4+c, row:rowIndex-1 }, ext:{ width:75, height:30 } });
            }
        }
        worksheet.getRow(rowIndex).eachCell(function(cell) {
            cell.font      = { name:'Khmer OS Battambang', size:11 };
            cell.border    = { top:{style:'thin'}, left:{style:'thin'}, bottom:{style:'thin'}, right:{style:'thin'} };
            cell.alignment = { vertical:'middle', horizontal:'center' };
        });
    }
    worksheet.columns = [{wch:6},{wch:24},{wch:8},{wch:18},{wch:12},{wch:12},{wch:12},{wch:12},{wch:16},{wch:16}];

    var buffer = await workbook.xlsx.writeBuffer();
    saveAs(new Blob([buffer]), 'វត្តមាន_ចូល_ចេញ_' + dateStr + '.xlsx');
}

/* ══════════════════════════════════════════════════════════════
   RENDER: ATTENDANCE — FIX 4: injects proper HTML into
   dashboard-content (not a broken <template> + wrong element ID)
══════════════════════════════════════════════════════════════ */
function renderAttendance() {
    document.getElementById('dashboard-content').innerHTML = `
<div style="background:#fff;color:#1e293b;padding:8px;border-radius:8px;font-family:'Noto Sans Khmer',sans-serif;">

    <!-- Header (print-visible) -->
    <div style="text-align:center;font-size:13px;font-weight:700;line-height:1.6;margin-bottom:4px;">
        ព្រះរាជាណាចក្រកម្ពុជា<br>ជាតិ សាសនា ព្រះមហាក្សត្រ<br>--------*--------
    </div>
    <div style="font-size:12px;font-weight:600;line-height:1.5;margin-bottom:4px;">
        រដ្ឋបាលស្រុកភ្នំស្រុក<br>
        ការិយាល័យអប់រំ យុវជន និងកីឡាស្រុក<br>
        សាលាបឋមសិក្សា រោគ
    </div>
    <h3 id="att-date-heading" style="text-align:center;font-size:15px;font-weight:700;color:#2563eb;margin:6px 0 2px 0;">
        បញ្ជីវត្តមានបុគ្គលិក<br>
        <span id="att-full-solar-title" style="font-size:13px;"></span>
    </h3>

    <!-- Controls (no-print) -->
    <div class="no-print" style="text-align:center;margin:6px 0;font-size:12px;">
        <span>ជ្រើសរើសថ្ងៃ៖
            <input type="date" id="att-date-input"
                   style="border:1px solid #ccc;border-radius:4px;padding:2px 6px;font-size:12px;">
        </span>
        <span style="margin-left:12px;">ម៉ោង៖
            <span id="att-clock"
                  style="background:#fee2e2;color:#dc2626;padding:2px 8px;border-radius:4px;font-family:monospace;font-weight:700;">
                00:00:00
            </span>
        </span>
    </div>

    <!-- Time-window status badges (no-print) -->
    <div class="no-print" style="text-align:center;margin-bottom:6px;font-size:11px;">
        <span style="font-weight:600;color:#475569;">ម៉ោងបើក:</span>
        <span id="att-badge-m_in"  class="att-time-badge closed">ព្រឹក-ចូល ០៧:០០–០៨:៣០</span>
        <span id="att-badge-m_out" class="att-time-badge closed">ព្រឹក-ចេញ ១០:៣០–១២:០០</span>
        <span id="att-badge-a_in"  class="att-time-badge closed">រសៀល-ចូល ១៣:០០–១៤:៣០</span>
        <span id="att-badge-a_out" class="att-time-badge closed">រសៀល-ចេញ ១៦:៣០–១៨:០០</span>
    </div>

    <!-- Main Table -->
    <div style="overflow-x:auto;">
        <table style="width:100%;border-collapse:collapse;font-size:12px;table-layout:auto;">
            <colgroup>
                <col style="width:4%">
                <col style="width:16%">
                <col style="width:6%">
                <col style="width:12%">
                <col style="width:10%">
                <col style="width:10%">
                <col style="width:10%">
                <col style="width:10%">
                <col style="width:12%">
                <col style="width:10%">
            </colgroup>
            <thead>
                <tr>
                    <th rowspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ល.រ</th>
                    <th rowspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">គោត្តនាម-នាម</th>
                    <th rowspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ភេទ</th>
                    <th rowspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">តួនាទី/ថ្នាក់</th>
                    <th colspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ពេលព្រឹក</th>
                    <th colspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ពេលរសៀល</th>
                    <th rowspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">លេខទូរស័ព្ទ</th>
                    <th rowspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ផ្សេងៗ</th>
                </tr>
                <tr>
                    <th style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ចូល</th>
                    <th style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ចេញ</th>
                    <th style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ចូល</th>
                    <th style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ចេញ</th>
                </tr>
            </thead>
            <tbody id="att-tbody"></tbody>
        </table>
    </div>

    <!-- Footer grid -->
    <div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:8px;margin-top:12px;padding-top:10px;border-top:1px solid #94a3b8;font-size:11px;">
        <div style="line-height:1.7;">
            <p style="font-weight:700;color:#2563eb;font-size:12px;margin:0 0 4px 0;">📊 ស្ថិតិប្រចាំថ្ងៃ៖</p>
            <p style="margin:0;">អវត្តមាន: <strong id="att-stat-absent">០០</strong> · ស្រី <strong id="att-stat-absent-f">០០</strong></p>
            <p style="margin:0;">មានច្បាប់: <strong id="att-stat-leave">០០</strong> · ស្រី <strong id="att-stat-leave-f">០០</strong></p>
            <p style="margin:0;">ទំនេរគ្មានប្រាក់: <strong id="att-stat-nopay">០០</strong> · ស្រី <strong id="att-stat-nopay-f">០០</strong></p>
            <p style="margin:0;">បេសកកម្ម: <strong id="att-stat-mission">០០</strong> · ស្រី <strong id="att-stat-mission-f">០០</strong></p>
            <p style="margin:0;">ផ្សេងៗ: <strong id="att-stat-other">០០</strong> · ស្រី <strong id="att-stat-other-f">០០</strong></p>
        </div>
        <div style="line-height:1.7;color:#374151;">
            <p style="font-weight:700;font-size:11px;margin:0 0 4px 0;">*ប្រភេទច្បាប់ឈប់សម្រាករួមមានៈ</p>
            <p style="margin:0;">១- ច្បាប់ឈប់ប្រចាំឆ្នាំ មានរយៈពេល ១៥ ថ្ងៃ/ឆ្នាំ</p>
            <p style="margin:0;">២- ច្បាប់ឈប់រយៈពេលខ្លី មានរយៈពេល ១៥ ថ្ងៃ/ឆ្នាំ</p>
            <p style="margin:0;">៣- ច្បាប់ឈប់សម្រាកលំហែមាតុភាព មានរយៈពេល ៣ ខែ</p>
            <p style="margin:0;">៤- ច្បាប់ឈប់ព្យាបាលជម្ងឺ មានរយៈពេល ១២ ខែ</p>
            <p style="margin:0;">៥- ច្បាប់ឈប់កិច្ចការផ្ទាល់ខ្លួន មានរយៈពេល ៣ ខែ</p>
        </div>
        <div style="text-align:left;display:flex;flex-direction:column;justify-content:space-between;align-items:left;">
            <div>
                <p id="att-lunardate" style="font-weight:700;font-size:11px;margin:0;line-height:1.6;"></p>
                <p id="att-solardate" style="font-weight:700;font-size:11px;margin:0;"></p>
            </div>
            <div style="margin-top:8px;text-align:center;">
                <p style="font-weight:700;font-size:13px;color:#1e3a5f;margin:0 0 4px 0;">នាយិកា</p>
                <div style="height:56px;display:flex;align-items:center;justify-content:center;">
                    <img id="att-principal-sig" class="hidden" src="" style="max-height:56px;object-fit:contain;">
                </div>
            </div>
        </div>
    </div>

    <!-- Action Buttons (no-print) -->
    <div class="no-print" style="margin-top:12px;display:flex;flex-wrap:wrap;gap:8px;justify-content:center;">
        <button onclick="attSaveData()"
                style="background:#2563eb;color:#fff;border:none;padding:8px 16px;border-radius:6px;font-weight:700;cursor:pointer;font-size:12px;">
            💾 រក្សាទុកវត្តមាន
        </button>
        <button onclick="attDownloadExcel()"
                style="background:#16a34a;color:#fff;border:none;padding:8px 16px;border-radius:6px;font-weight:700;cursor:pointer;font-size:12px;">
            ⬇️ ទាញយកជា Excel
        </button>
        <button onclick="window.print()"
                style="background:#475569;color:#fff;border:none;padding:8px 16px;border-radius:6px;font-weight:700;cursor:pointer;font-size:12px;">
            🖨️ បោះពុម្ព
        </button>
    </div>
</div>

<!-- Signature Modal -->
<div id="att-sig-modal"
     style="display:none;position:fixed;inset:0;background:rgba(0,0,0,.5);z-index:1000;align-items:center;justify-content:center;">
    <div style="background:#fff;padding:16px;border-radius:8px;width:300px;text-align:center;">
        <h3 id="att-modal-title" style="margin:0 0 12px 0;font-weight:700;color:#1e293b;font-size:14px;">គូសហត្ថលេខា</h3>
        <canvas id="att-sig-canvas" width="270" height="120"
                style="border:1px solid #ccc;border-radius:6px;display:block;margin:0 auto 12px;background:#fff;touch-action:none;"></canvas>
        <div style="display:flex;justify-content:center;gap:8px;">
            <button onclick="attCtxClear()"
                    style="background:#f59e0b;color:#fff;border:none;padding:6px 14px;border-radius:4px;cursor:pointer;font-weight:600;">
                សម្អាត
            </button>
            <button onclick="attSaveSignature()"
                    style="background:#16a34a;color:#fff;border:none;padding:6px 14px;border-radius:4px;cursor:pointer;font-weight:600;">
                រក្សាទុក
            </button>
            <button onclick="attCloseModal()"
                    style="background:#64748b;color:#fff;border:none;padding:6px 14px;border-radius:4px;cursor:pointer;font-weight:600;">
                បោះបង់
            </button>
        </div>
    </div>
</div>`;

    /* ── Wire up after HTML is injected ── */
    var dateInput = document.getElementById('att-date-input');
    dateInput.valueAsDate = new Date();
    dateInput.addEventListener('change', function() { attLoadData(this.value); });

    /* Canvas pointer events */
    attCanvas = document.getElementById('att-sig-canvas');
    attCtx    = attCanvas ? attCanvas.getContext('2d') : null;
    if (attCanvas) {
        attCanvas.addEventListener('pointerdown', function(e) {
            attDrawing = true;
            if (!attCtx) return;
            attCtx.lineWidth = 2.5; attCtx.strokeStyle = '#000'; attCtx.lineCap = 'round';
            attCtx.beginPath();
            var pos = attGetCanvasPos(e); attCtx.moveTo(pos.x, pos.y);
        });
        attCanvas.addEventListener('pointermove', function(e) {
            if (!attDrawing || !attCtx) return;
            var pos = attGetCanvasPos(e); attCtx.lineTo(pos.x, pos.y); attCtx.stroke();
        });
        attCanvas.addEventListener('pointerup',   function() { attDrawing = false; });
        attCanvas.addEventListener('pointerleave',function() { attDrawing = false; });
    }

    /* Start clock */
    stopAttClock();
    attClockTick();
    attClockInterval = setInterval(attClockTick, 1000);

    /* Render rows and load saved data */
    attRenderTable();
    attLoadData(dateInput.value);
}


/* ══════════════════════════════════════════════════════════════
   ATTENDANCE — HELPERS
══════════════════════════════════════════════════════════════ */
function attIsWindowOpen(win) {
    var now   = new Date();
    var nowM  = now.getHours() * 60 + now.getMinutes();
    var startM = win.startH * 60 + win.startM;
    var endM   = win.endH   * 60 + win.endM;
    return nowM >= startM && nowM <= endM;
}

function attUpdateBadges() {
    ATT_TIME_WINDOWS.forEach(function(w) {
        var el = document.getElementById('att-badge-' + w.key);
        if (!el) return;
        el.className = 'att-time-badge ' + (attIsWindowOpen(w) ? 'open' : 'closed');
    });
}

function attUpdateLockStates() {
    document.querySelectorAll('.att-sig-container').forEach(function(c) {
        var colIdx = parseInt(c.dataset.colIdx);
        var win    = ATT_TIME_WINDOWS[colIdx];
        if (!win) return;
        if (c.dataset.base64 && c.dataset.base64.startsWith('data:image')) return; // already signed
        c.classList.remove('locked','open-now');
        c.classList.add(attIsWindowOpen(win) ? 'open-now' : 'locked');
    });
}

function attConvertKhmerDate(dateInput) {
    var d = new Date(dateInput);
    var days   = ["ថ្ងៃអាទិត្យ","ថ្ងៃច័ន្ទ","ថ្ងៃអង្គារ","ថ្ងៃពុធ","ថ្ងៃព្រហស្បតិ៍","ថ្ងៃសុក្រ","ថ្ងៃសៅរ៍"];
    var months = ["មករា","កុម្ភៈ","មីនា","មេសា","ឧសភា","មិថុនា","កក្កដា","សីហា","កញ្ញា","តុលា","វិច្ឆិកា","ធ្នូ"];
    var dayName   = days[d.getDay()];
    var dayNum    = toKhmer(d.getDate());
    var monthName = months[d.getMonth()];
    var yearNum   = toKhmer(d.getFullYear());
    // solar without day name: ថ្ងៃទី${dayNum} ខែ${monthName} ឆ្នាំ${yearNum}
    var solarNoDay = 'ថ្ងៃទី' + dayNum + ' ខែ' + monthName + ' ឆ្នាំ' + yearNum;

    var titleEl  = document.getElementById('att-full-solar-title');
    var solarEl  = document.getElementById('att-solardate');
    // NOTE: never set headEl.textContent — that wipes the <span> child inside the h3
    if (titleEl) titleEl.textContent = 'សម្រាប់' + solarNoDay;
    if (solarEl) solarEl.textContent = 'រោគ ' + solarNoDay;

    // Lunar
    var baseDate      = new Date("2026-05-13");
    var diffDays      = Math.round((d - baseDate) / 86400000);
    var totalLunarDays = 9 + diffDays;
    while (totalLunarDays <= 0) totalLunarDays += 30;
    var lunarDay = totalLunarDays % 30 || 30;
    var phase    = lunarDay <= 15 ? "កើត" : "រោច";
    var phaseNum = lunarDay <= 15 ? lunarDay : lunarDay - 15 || 15;
    var lunarMonths = { 4:"ជេស្ន", 5:"អាសាឍ", 6:"ស្រាពណ៍", 7:"ភទ្របទ", 8:"អស្សុជ", 9:"កត្តិក", 10:"មិគសិរ", 11:"បុស្ស" };
    var lunarMonth = lunarMonths[d.getMonth()] || "ពិសាខ";
    var lunarEl = document.getElementById('att-lunardate');
    if (lunarEl) lunarEl.textContent = dayName + ' ' + toKhmer(phaseNum) + phase + ' ខែ' + lunarMonth + ' ឆ្នាំមមី អដ្ឋស័ក ព.ស ' + toKhmer(2570);
}

/* ── att sig data ── */
function attSetSigData(container, base64) {
    var img = container.querySelector('.att-sig-img');
    var ph  = container.querySelector('.att-sig-placeholder');
    if (base64 && base64.startsWith('data:image')) {
        img.src = base64; img.style.display = 'block'; ph.style.display = 'none';
        container.dataset.base64 = base64;
        container.classList.remove('locked','open-now');
        container.style.background = '#fffde7';
        container.style.border = '1px dashed #b45309';
        container.style.cursor = 'pointer';
    } else {
        img.src = ''; img.style.display = 'none'; ph.style.display = 'block';
        container.dataset.base64 = '';
        container.style.background = '';
        container.style.border = '';
        container.style.cursor = '';
    }
}

/* ── build one attendance row ── */
function attCreateRow(idx, s) {
    var tr = document.createElement('tr');
    tr.dataset.idx = idx;
    tr.style.borderBottom = '1px solid #e2e8f0';

    function sigCell(colIdx, label) {
        return '<td style="padding:2px;min-width:70px;"><div class="att-sig-container locked" data-col-idx="' + colIdx + '" onclick="attOpenSigModal(this,\'' + ATT_TIME_WINDOWS[colIdx].label + '\',' + colIdx + ')">' +
               '<span class="att-sig-placeholder">✍️ ' + label + '</span>' +
               '<img class="att-sig-img" src="">' +
               '</div></td>';
    }

    tr.innerHTML =
        '<td style="padding:4px;text-align:center;font-size:12px;">' + toKhmer(idx + 1) + '</td>' +
        '<td style="padding:4px;font-weight:700;font-size:12px;white-space:nowrap;">' + s.name + '</td>' +
        '<td style="padding:4px;text-align:center;font-size:12px;">' + s.gender + '</td>' +
        '<td style="padding:4px;font-size:11px;white-space:nowrap;">' + s.position + (s.cls !== '-' ? ' ' + s.cls : '') + '</td>' +
        sigCell(0,'ចូល') + sigCell(1,'ចេញ') + sigCell(2,'ចូល') + sigCell(3,'ចេញ') +
        '<td contenteditable="true" class="att-phone-cell" style="padding:4px;text-align:center;font-size:11px;min-width:90px;"></td>' +
        '<td style="padding:4px;"><input type="text" class="att-note" placeholder="..."></td>';
    return tr;
}

/* ── render the attendance table body ── */
function attRenderTable() {
    var tbody = document.getElementById('att-tbody');
    if (!tbody) return;
    tbody.innerHTML = '';
    attStaff.forEach(function(s, i) { tbody.appendChild(attCreateRow(i, s)); });
    var dateEl = document.getElementById('att-date-input');
    if (dateEl) attConvertKhmerDate(dateEl.value);
    attUpdateLockStates();
}

/* ── load attendance from Firebase ── */
function attLoadData(date) {
    if (!date) return;
    attConvertKhmerDate(date);
    db.ref('attendance/' + date).get().then(function(snap) {
        var val = snap.val() || {};
        var tbody = document.getElementById('att-tbody');
        if (!tbody) return;
        tbody.querySelectorAll('tr').forEach(function(tr) {
            var idx    = tr.dataset.idx;
            var s      = attStaff[idx];
            if (!s) return;
            var record = val[s.name] || {};
            var containers = tr.querySelectorAll('.att-sig-container');
            attSetSigData(containers[0], record.m_in);
            attSetSigData(containers[1], record.m_out);
            attSetSigData(containers[2], record.a_in);
            attSetSigData(containers[3], record.a_out);
            var phoneCell = tr.querySelector('.att-phone-cell');
            var noteInput = tr.querySelector('input.att-note');
            if (phoneCell) phoneCell.textContent = record.phone || '';
            if (noteInput) noteInput.value = record.note || '';
            // Principal sig for print footer
            if (idx == 0 && record.m_in) {
                var pSig = document.getElementById('att-principal-sig');
                if (pSig) { pSig.src = record.m_in; pSig.classList.remove('hidden'); }
            }
        });
        attUpdateLockStates();
    });
}

/* ── clock tick ── */
function attClockTick() {
    var clockEl = document.getElementById('att-clock');
    if (!clockEl) { stopAttClock(); return; }
    var now = new Date();
    clockEl.textContent =
        String(now.getHours()).padStart(2,'0') + ':' +
        String(now.getMinutes()).padStart(2,'0') + ':' +
        String(now.getSeconds()).padStart(2,'0');
    attUpdateBadges();
    attUpdateLockStates();
}

function stopAttClock() {
    if (attClockInterval) { clearInterval(attClockInterval); attClockInterval = null; }
}

/* ══════════════════════════════════════════════════════════════
   ATTENDANCE — SIGNATURE MODAL (global so onclick can call them)
══════════════════════════════════════════════════════════════ */
var attCurrentContainer = null;
var attDrawing          = false;
var attCanvas, attCtx;

function attOpenSigModal(container, type, colIdx) {
    var win = ATT_TIME_WINDOWS[colIdx];
    if (win && !attIsWindowOpen(win)) {
        var sh = toKhmer(String(win.startH).padStart(2,'0'));
        var sm = toKhmer(String(win.startM).padStart(2,'0'));
        var eh = toKhmer(String(win.endH).padStart(2,'0'));
        var em = toKhmer(String(win.endM).padStart(2,'0'));
        alert('🔒 ម៉ោង' + type + ' ត្រូវបានបិទ!\nអាចចុះហត្ថលេខាបានពី ' + sh + ':' + sm + ' ដល់ ' + eh + ':' + em + ' តែប៉ុណ្ណោះ។');
        return;
    }
    attCurrentContainer = container;
    var titleEl = document.getElementById('att-modal-title');
    if (titleEl) titleEl.textContent = 'គូសហត្ថលេខា (' + type + ')';
    attCanvas  = document.getElementById('att-sig-canvas');
    attCtx     = attCanvas.getContext('2d');
    attCtx.lineWidth = 2.5; attCtx.strokeStyle = '#000'; attCtx.lineCap = 'round';
    attCtxClear();
    document.getElementById('att-sig-modal').classList.remove('hidden');
    document.getElementById('att-sig-modal').style.display = 'flex';
}

function attCloseModal() {
    document.getElementById('att-sig-modal').classList.add('hidden');
    document.getElementById('att-sig-modal').style.display = 'none';
}

function attCtxClear() {
    if (attCtx && attCanvas) attCtx.clearRect(0, 0, attCanvas.width, attCanvas.height);
}

function attSaveSignature() {
    if (!attCurrentContainer || !attCanvas) return;
    var base64 = attCanvas.toDataURL();
    attSetSigData(attCurrentContainer, base64);
    // If it's the principal row (idx 0), update print signature
    var parentTr = attCurrentContainer.closest('tr');
    if (parentTr && parentTr.dataset.idx == 0) {
        var pSig = document.getElementById('att-principal-sig');
        if (pSig) { pSig.src = base64; pSig.classList.remove('hidden'); }
    }
    attCloseModal();
}

function attGetCanvasPos(e) {
    var rect    = attCanvas.getBoundingClientRect();
    var clientX = e.touches ? e.touches[0].clientX : e.clientX;
    var clientY = e.touches ? e.touches[0].clientY : e.clientY;
    return { x: clientX - rect.left, y: clientY - rect.top };
}

/* ── save attendance to Firebase ── */
function attSaveData() {
    var dateEl = document.getElementById('att-date-input');
    if (!dateEl || !dateEl.value) { alert('សូមជ្រើសរើសកាលបរិច្ឆេទ!'); return; }
    var dateStr = dateEl.value;
    var data = {};
    var tbody = document.getElementById('att-tbody');
    if (!tbody) return;
    tbody.querySelectorAll('tr').forEach(function(tr) {
        var idx  = tr.dataset.idx;
        var name = attStaff[idx] ? attStaff[idx].name : null;
        if (!name) return;
        var containers = tr.querySelectorAll('.att-sig-container');
        data[name] = {
            m_in:  containers[0] ? (containers[0].dataset.base64 || '') : '',
            m_out: containers[1] ? (containers[1].dataset.base64 || '') : '',
            a_in:  containers[2] ? (containers[2].dataset.base64 || '') : '',
            a_out: containers[3] ? (containers[3].dataset.base64 || '') : '',
            phone: (tr.querySelector('.att-phone-cell') || {}).textContent || '',
            note:  (tr.querySelector('input.att-note') || {}).value || '',
        };
    });
    db.ref('attendance/' + dateStr).set(data)
        .then(function() { alert('💾 បានរក្សាទុករួចរាល់!'); attLoadData(dateStr); })
        .catch(function(e) { alert('កំហុស: ' + e.message); });
}

/* ── Excel export ── */
async function attDownloadExcel() {
    if (typeof ExcelJS === 'undefined' || typeof saveAs === 'undefined') {
        alert('ExcelJS ឬ FileSaver មិនទាន់ load សូមពិនិត្យការតភ្ជាប់អ៊ីនធឺណិត!');
        return;
    }
    var dateEl = document.getElementById('att-date-input');
    var dateStr = dateEl ? dateEl.value : '';
    var workbook  = new ExcelJS.Workbook();
    var worksheet = workbook.addWorksheet('វត្តមាន');

    worksheet.mergeCells('A1:J1');
    worksheet.getCell('A1').value = 'បញ្ជីវត្តមានបុគ្គលិក កាលបរិច្ឆេទ: ' + dateStr;
    worksheet.getCell('A1').font      = { name:'Khmer OS Battambang', size:14, bold:true };
    worksheet.getCell('A1').alignment = { horizontal:'center' };

    worksheet.mergeCells('A3:A4'); worksheet.getCell('A3').value = 'ល.រ';
    worksheet.mergeCells('B3:B4'); worksheet.getCell('B3').value = 'គោត្តនាម-នាម';
    worksheet.mergeCells('C3:C4'); worksheet.getCell('C3').value = 'ភេទ';
    worksheet.mergeCells('D3:D4'); worksheet.getCell('D3').value = 'តួនាទី/ថ្នាក់';
    worksheet.mergeCells('E3:F3'); worksheet.getCell('E3').value = 'ពេលព្រឹក';
    worksheet.getCell('E4').value = 'ចូល'; worksheet.getCell('F4').value = 'ចេញ';
    worksheet.mergeCells('G3:H3'); worksheet.getCell('G3').value = 'ពេលរសៀល';
    worksheet.getCell('G4').value = 'ចូល'; worksheet.getCell('H4').value = 'ចេញ';
    worksheet.mergeCells('I3:I4'); worksheet.getCell('I3').value = 'លេខទូរស័ព្ទ';
    worksheet.mergeCells('J3:J4'); worksheet.getCell('J3').value = 'ផ្សេងៗ';

    ['3','4'].forEach(function(rowNum) {
        worksheet.getRow(rowNum).eachCell(function(cell) {
            cell.fill      = { type:'pattern', pattern:'solid', fgColor:{argb:'2563EB'} };
            cell.font      = { name:'Khmer OS Battambang', bold:true, color:{argb:'FFFFFF'}, size:11 };
            cell.alignment = { horizontal:'center', vertical:'middle' };
            cell.border    = { top:{style:'thin'}, left:{style:'thin'}, bottom:{style:'thin'}, right:{style:'thin'} };
        });
    });

    var tbody = document.getElementById('att-tbody');
    for (var i = 0; i < attStaff.length; i++) {
        var s  = attStaff[i];
        var tr = tbody ? tbody.querySelector('tr[data-idx="' + i + '"]') : null;
        var phoneVal = tr ? (tr.querySelector('.att-phone-cell') || {}).textContent || '' : '';
        var noteVal  = tr ? ((tr.querySelector('input.att-note') || {}).value || '') : '';
        var containers = tr ? tr.querySelectorAll('.att-sig-container') : [];
        var rowIndex = i + 5;

        worksheet.getRow(rowIndex).values = [
            i + 1, s.name, s.gender,
            s.position + (s.cls !== '-' ? ' ' + s.cls : ''),
            '', '', '', '', phoneVal, noteVal
        ];
        worksheet.getRow(rowIndex).height = 32;

        for (var c = 0; c < 4; c++) {
            if (containers[c] && containers[c].dataset.base64 && containers[c].dataset.base64.startsWith('data:image')) {
                var imageId = workbook.addImage({ base64: containers[c].dataset.base64, extension:'png' });
                worksheet.addImage(imageId, { tl:{ col:4+c, row:rowIndex-1 }, ext:{ width:75, height:30 } });
            }
        }
        worksheet.getRow(rowIndex).eachCell(function(cell) {
            cell.font      = { name:'Khmer OS Battambang', size:11 };
            cell.border    = { top:{style:'thin'}, left:{style:'thin'}, bottom:{style:'thin'}, right:{style:'thin'} };
            cell.alignment = { vertical:'middle', horizontal:'center' };
        });
    }
    worksheet.columns = [{wch:6},{wch:24},{wch:8},{wch:18},{wch:12},{wch:12},{wch:12},{wch:12},{wch:16},{wch:16}];

    var buffer = await workbook.xlsx.writeBuffer();
    saveAs(new Blob([buffer]), 'វត្តមាន_ចូល_ចេញ_' + dateStr + '.xlsx');
}

/* ══════════════════════════════════════════════════════════════
   RENDER: ATTENDANCE — FIX 4: injects proper HTML into
   dashboard-content (not a broken <template> + wrong element ID)
══════════════════════════════════════════════════════════════ */
function renderAttendance() {
    document.getElementById('dashboard-content').innerHTML = `
<div style="background:#fff;color:#1e293b;padding:8px;border-radius:8px;font-family:'Noto Sans Khmer',sans-serif;">

    <!-- Header (print-visible) -->
    <div style="text-align:center;font-size:13px;font-weight:700;line-height:1.6;margin-bottom:4px;">
        ព្រះរាជាណាចក្រកម្ពុជា<br>ជាតិ សាសនា ព្រះមហាក្សត្រ<br>--------*--------
    </div>
    <div style="font-size:12px;font-weight:600;line-height:1.5;margin-bottom:4px;">
        រដ្ឋបាលស្រុកភ្នំស្រុក<br>
        ការិយាល័យអប់រំ យុវជន និងកីឡាស្រុក<br>
        សាលាបឋមសិក្សា រោគ
    </div>
    <h3 id="att-date-heading" style="text-align:center;font-size:15px;font-weight:700;color:#2563eb;margin:6px 0 2px 0;">
        បញ្ជីវត្តមានបុគ្គលិក<br>
        <span id="att-full-solar-title" style="font-size:13px;"></span>
    </h3>

    <!-- Controls (no-print) -->
    <div class="no-print" style="text-align:center;margin:6px 0;font-size:12px;">
        <span>ជ្រើសរើសថ្ងៃ៖
            <input type="date" id="att-date-input"
                   style="border:1px solid #ccc;border-radius:4px;padding:2px 6px;font-size:12px;">
        </span>
        <span style="margin-left:12px;">ម៉ោង៖
            <span id="att-clock"
                  style="background:#fee2e2;color:#dc2626;padding:2px 8px;border-radius:4px;font-family:monospace;font-weight:700;">
                00:00:00
            </span>
        </span>
    </div>

    <!-- Time-window status badges (no-print) -->
    <div class="no-print" style="text-align:center;margin-bottom:6px;font-size:11px;">
        <span style="font-weight:600;color:#475569;">ម៉ោងបើក:</span>
        <span id="att-badge-m_in"  class="att-time-badge closed">ព្រឹក-ចូល ០៧:០០–០៨:៣០</span>
        <span id="att-badge-m_out" class="att-time-badge closed">ព្រឹក-ចេញ ១០:៣០–១២:០០</span>
        <span id="att-badge-a_in"  class="att-time-badge closed">រសៀល-ចូល ១៣:០០–១៤:៣០</span>
        <span id="att-badge-a_out" class="att-time-badge closed">រសៀល-ចេញ ១៦:៣០–១៨:០០</span>
    </div>

    <!-- Main Table -->
    <div style="overflow-x:auto;">
        <table style="width:100%;border-collapse:collapse;font-size:12px;table-layout:auto;">
            <colgroup>
                <col style="width:4%">
                <col style="width:16%">
                <col style="width:6%">
                <col style="width:12%">
                <col style="width:10%">
                <col style="width:10%">
                <col style="width:10%">
                <col style="width:10%">
                <col style="width:12%">
                <col style="width:10%">
            </colgroup>
            <thead>
                <tr>
                    <th rowspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ល.រ</th>
                    <th rowspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">គោត្តនាម-នាម</th>
                    <th rowspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ភេទ</th>
                    <th rowspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">តួនាទី/ថ្នាក់</th>
                    <th colspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ពេលព្រឹក</th>
                    <th colspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ពេលរសៀល</th>
                    <th rowspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">លេខទូរស័ព្ទ</th>
                    <th rowspan="2" style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ផ្សេងៗ</th>
                </tr>
                <tr>
                    <th style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ចូល</th>
                    <th style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ចេញ</th>
                    <th style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ចូល</th>
                    <th style="background:#2563eb;color:#fff;border:1px solid #94a3b8;padding:5px;text-align:center;">ចេញ</th>
                </tr>
            </thead>
            <tbody id="att-tbody"></tbody>
        </table>
    </div>

    <!-- Footer grid -->
    <div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:8px;margin-top:12px;padding-top:10px;border-top:1px solid #94a3b8;font-size:11px;">
        <div style="line-height:1.7;">
            <p style="font-weight:700;color:#2563eb;font-size:12px;margin:0 0 4px 0;">📊 ស្ថិតិប្រចាំថ្ងៃ៖</p>
            <p style="margin:0;">អវត្តមាន: <strong id="att-stat-absent">០០</strong> · ស្រី <strong id="att-stat-absent-f">០០</strong></p>
            <p style="margin:0;">មានច្បាប់: <strong id="att-stat-leave">០០</strong> · ស្រី <strong id="att-stat-leave-f">០០</strong></p>
            <p style="margin:0;">ទំនេរគ្មានប្រាក់: <strong id="att-stat-nopay">០០</strong> · ស្រី <strong id="att-stat-nopay-f">០០</strong></p>
            <p style="margin:0;">បេសកកម្ម: <strong id="att-stat-mission">០០</strong> · ស្រី <strong id="att-stat-mission-f">០០</strong></p>
            <p style="margin:0;">ផ្សេងៗ: <strong id="att-stat-other">០០</strong> · ស្រី <strong id="att-stat-other-f">០០</strong></p>
        </div>
        <div style="line-height:1.7;color:#374151;">
            <p style="font-weight:700;font-size:11px;margin:0 0 4px 0;">*ប្រភេទច្បាប់ឈប់សម្រាករួមមានៈ</p>
            <p style="margin:0;">១- ច្បាប់ឈប់ប្រចាំឆ្នាំ មានរយៈពេល ១៥ ថ្ងៃ/ឆ្នាំ</p>
            <p style="margin:0;">២- ច្បាប់ឈប់រយៈពេលខ្លី មានរយៈពេល ១៥ ថ្ងៃ/ឆ្នាំ</p>
            <p style="margin:0;">៣- ច្បាប់ឈប់សម្រាកលំហែមាតុភាព មានរយៈពេល ៣ ខែ</p>
            <p style="margin:0;">៤- ច្បាប់ឈប់ព្យាបាលជម្ងឺ មានរយៈពេល ១២ ខែ</p>
            <p style="margin:0;">៥- ច្បាប់ឈប់កិច្ចការផ្ទាល់ខ្លួន មានរយៈពេល ៣ ខែ</p>
        </div>
        <div style="text-align:center;display:flex;flex-direction:column;justify-content:space-between;align-items:center;">
            <div>
                <p id="att-lunardate" style="font-weight:700;font-size:11px;margin:0;line-height:1.6;"></p>
                <p id="att-solardate" style="font-weight:700;font-size:11px;margin:0;"></p>
            </div>
            <div style="margin-top:8px;text-align:center;">
                <p style="font-weight:700;font-size:13px;color:#1e3a5f;margin:0 0 4px 0;">នាយិកា</p>
                <div style="height:56px;display:flex;align-items:center;justify-content:center;">
                    <img id="att-principal-sig" class="hidden" src="" style="max-height:56px;object-fit:contain;">
                </div>
            </div>
        </div>
    </div>

    <!-- Action Buttons (no-print) -->
    <div class="no-print" style="margin-top:12px;display:flex;flex-wrap:wrap;gap:8px;justify-content:center;">
        <button onclick="attSaveData()"
                style="background:#2563eb;color:#fff;border:none;padding:8px 16px;border-radius:6px;font-weight:700;cursor:pointer;font-size:12px;">
            💾 រក្សាទុកវត្តមាន
        </button>
        <button onclick="attDownloadExcel()"
                style="background:#16a34a;color:#fff;border:none;padding:8px 16px;border-radius:6px;font-weight:700;cursor:pointer;font-size:12px;">
            ⬇️ ទាញយកជា Excel
        </button>
        <button onclick="window.print()"
                style="background:#475569;color:#fff;border:none;padding:8px 16px;border-radius:6px;font-weight:700;cursor:pointer;font-size:12px;">
            🖨️ បោះពុម្ព
        </button>
    </div>
</div>

<!-- Signature Modal -->
<div id="att-sig-modal"
     style="display:none;position:fixed;inset:0;background:rgba(0,0,0,.5);z-index:1000;align-items:center;justify-content:center;">
    <div style="background:#fff;padding:16px;border-radius:8px;width:300px;text-align:center;">
        <h3 id="att-modal-title" style="margin:0 0 12px 0;font-weight:700;color:#1e293b;font-size:14px;">គូសហត្ថលេខា</h3>
        <canvas id="att-sig-canvas" width="270" height="120"
                style="border:1px solid #ccc;border-radius:6px;display:block;margin:0 auto 12px;background:#fff;touch-action:none;"></canvas>
        <div style="display:flex;justify-content:center;gap:8px;">
            <button onclick="attCtxClear()"
                    style="background:#f59e0b;color:#fff;border:none;padding:6px 14px;border-radius:4px;cursor:pointer;font-weight:600;">
                សម្អាត
            </button>
            <button onclick="attSaveSignature()"
                    style="background:#16a34a;color:#fff;border:none;padding:6px 14px;border-radius:4px;cursor:pointer;font-weight:600;">
                រក្សាទុក
            </button>
            <button onclick="attCloseModal()"
                    style="background:#64748b;color:#fff;border:none;padding:6px 14px;border-radius:4px;cursor:pointer;font-weight:600;">
                បោះបង់
            </button>
        </div>
    </div>
</div>`;

    /* ── Wire up after HTML is injected ── */
    var dateInput = document.getElementById('att-date-input');
    dateInput.valueAsDate = new Date();
    dateInput.addEventListener('change', function() { attLoadData(this.value); });

    /* Canvas pointer events */
    attCanvas = document.getElementById('att-sig-canvas');
    attCtx    = attCanvas ? attCanvas.getContext('2d') : null;
    if (attCanvas) {
        attCanvas.addEventListener('pointerdown', function(e) {
            attDrawing = true;
            if (!attCtx) return;
            attCtx.lineWidth = 2.5; attCtx.strokeStyle = '#000'; attCtx.lineCap = 'round';
            attCtx.beginPath();
            var pos = attGetCanvasPos(e); attCtx.moveTo(pos.x, pos.y);
        });
        attCanvas.addEventListener('pointermove', function(e) {
            if (!attDrawing || !attCtx) return;
            var pos = attGetCanvasPos(e); attCtx.lineTo(pos.x, pos.y); attCtx.stroke();
        });
        attCanvas.addEventListener('pointerup',   function() { attDrawing = false; });
        attCanvas.addEventListener('pointerleave',function() { attDrawing = false; });
    }

    /* Start clock */
    stopAttClock();
    attClockTick();
    attClockInterval = setInterval(attClockTick, 1000);

    /* Render rows and load saved data */
    attRenderTable();
    attLoadData(dateInput.value);
}
</script>

</template>
<template id="tpl-library">



  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width,initial-scale=0.9">
  <title>libraries-01030401017</title>
  <link rel="stylesheet" href="img/bootstrap.min.css">
  <link rel="stylesheet" href="style.css">
  <style>
    * { margin:0; padding:0; box-sizing:border-box; }
    
    @page { size: A4; margin: 5mm; }
    
    body { 
      font-family: "Khmer OS", "Noto Sans Khmer", Arial, sans-serif; 
      color:#2c3e50; 
      line-height:1.5;
      background:#f5f7fa;
      padding:10px;
    }
    
    .main-container {
      max-width:1000px;
      margin:0 auto;
      background:white;
      border-radius:8px;
      box-shadow:0 2px 8px rgba(0,0,0,0.1);
      overflow:hidden;
    }
    
    .header {
      text-align:center;
      background:linear-gradient(135deg, #2980b9 0%, #1a5490 100%);
      color:white;
      padding:10px;
    }
    
    .header h1 {
      font-size:20px;
      margin-bottom:8px;
    }
    
    .header p {
      font-size:12px;
      margin:4px 0;
      opacity:0.9;
    }
    
    /* Tab Navigation */
    .tab-navigation {
      display:flex;
      background:#ecf0f1;
      border-bottom:2px solid #2980b9;
      overflow-x:auto;
    }
    
    .tab-btn {
      flex:1;
      padding:12px 16px;
      border:none;
      background:transparent;
      cursor:pointer;
      font-size:12px;
      font-weight:600;
      color:#555;
      border-bottom:3px solid transparent;
      transition:all 0.3s ease;
      font-family:inherit;
      white-space:nowrap;
      min-width:120px;
    }
    
    .tab-btn:hover {
      background:rgba(41, 128, 185, 0.1);
      color:#2980b9;
    }
    
    .tab-btn.active {
      color:white;
      background:#2980b9;
      border-bottom-color:#f39c12;
    }
    
    /* Tab Content */
    .tab-content {
      display:none;
      padding:20px;
      min-height:400px;
      animation:fadeIn 0.3s ease;
    }
    
    .tab-content.active {
      display:block;
    }
    
    @keyframes fadeIn {
      from { opacity:0; }
      to { opacity:1; }
    }
    
    .container {
      padding:16px 0;
    }
    
    .section-header {
      background:#f8f9fa;
      padding:12px 16px;
      border-radius:6px;
      margin-bottom:16px;
      border-left:4px solid #2980b9;
    }
    
    .section-header h2 {
      font-size:14px;
      color:#1a5490;
      margin:0 0 6px 0;
    }
    
    .section-header p {
      font-size:10px;
      color:#666;
      line-height:1.4;
    }
    
    table {
      width:100%;
      border-collapse:collapse;
      font-size:10px;
      margin:12px 0;
      overflow-x:auto;
    }
    
    th, td {
      border:1px solid #bdc3c7;
      padding:6px;
      text-align:left;
      vertical-align:middle;
    }
    
    th {
      background:linear-gradient(135deg, #2980b9 0%, #1a5490 100%);
      color:white;
      font-weight:600;
      text-align:center;
      font-size:9px;
    }
    
    tbody tr:nth-child(odd) { background:#f8f9fa; }
    tbody tr:hover { background:#ecf0f1; }
    
    td[contenteditable] {
      background:white;
      cursor:text;
      min-height:20px;
    }
    
    td[contenteditable]:focus {
      background:#fffacd;
      outline:2px solid #f39c12;
    }
    
    input[type="date"],
    input[type="text"],
    input[type="number"],
    select {
      border:1px solid #bdc3c7;
      padding:4px;
      border-radius:3px;
      font-family:inherit;
      font-size:11px;
      width:95%;
    }
    
    .notes-box {
      background:#ecf0f1;
      padding:10px;
      border-radius:6px;
      font-size:9px;
      margin:12px 0;
      line-height:1.5;
      border-left:4px solid #2980b9;
    }
    
    .notes-box strong {
      color:#1a5490;
    }
    
    .control-panel {
      background:#f8f9fa;
      padding:12px;
      border-radius:6px;
      margin:16px 0;
      border:1px solid #ecf0f1;
      display:flex;
      gap:8px;
      flex-wrap:wrap;
      align-items:center;
    }
    
    button {
      padding:8px 12px;
      background:#2980b9;
      color:white;
      border:none;
      border-radius:4px;
      cursor:pointer;
      font-size:11px;
      font-weight:500;
      font-family:inherit;
      transition:all 0.3s ease;
    }
    
    button:hover {
      background:#1a5490;
      transform:translateY(-2px);
    }
    
    button.btn-success {
      background:#27ae60;
    }
    
    button.btn-success:hover {
      background:#229954;
    }
    
    button.btn-danger {
      background:#e74c3c;
    }
    
    button.btn-danger:hover {
      background:#c0392b;
    }
    
    button.btn-warning {
      background:#f39c12;
    }
    
    button.btn-warning:hover {
      background:#e67e22;
    }
    
    button.btn-small {
      padding:4px 8px;
      font-size:9px;
    }
    
    .input-group {
      display:flex;
      gap:12px;
      align-items:center;
      margin:8px 0;
      flex-wrap:wrap;
    }
    
    .input-group label {
      font-size:11px;
      font-weight:500;
      color:#2c3e50;
      min-width:130px;
    }
    
    .input-group input {
      padding:6px 8px;
      border:1px solid #bdc3c7;
      border-radius:4px;
      font-size:11px;
      flex:1;
      min-width:150px;
    }
    
    .status-message {
      padding:10px 12px;
      border-radius:4px;
      margin:8px 0;
      font-size:11px;
      display:none;
      border-left:4px solid;
    }
    
    .status-message.show { display:block; }
    .status-message.success { 
      background:#d4edda; 
      color:#155724; 
      border-left-color:#28a745;
    }
    .status-message.error { 
      background:#f8d7da; 
      color:#721c24; 
      border-left-color:#dc3545;
    }
    .status-message.info { 
      background:#d1ecf1; 
      color:#0c5460; 
      border-left-color:#17a2b8;
    }
    
    /* Modal */
    .modal {
      display:none;
      position:fixed;
      z-index:1000;
      left:0;
      top:0;
      width:100%;
      height:100%;
      background:rgba(0,0,0,0.7);
      overflow-y:auto;
    }
    
    .modal-content {
      background:white;
      margin:5% auto;
      padding:20px;
      border-radius:8px;
      width:90%;
      max-width:600px;
      box-shadow:0 8px 24px rgba(0,0,0,0.2);
    }
    
    .modal-header {
      display:flex;
      justify-content:space-between;
      align-items:center;
      margin-bottom:12px;
      padding-bottom:8px;
      border-bottom:2px solid #ecf0f1;
    }
    
    .modal-header h3 {
      color:#1a5490;
      font-size:15px;
      margin:0;
    }
    
    /* Form Grid inside Modal */
    .form-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 10px;
      margin-bottom: 15px;
    }
    .form-group {
      display: flex;
      flex-direction: column;
    }
    .form-group label {
      font-size: 11px;
      font-weight: 600;
      margin-bottom: 4px;
      color: #34495e;
    }
    .form-group input, .form-group select {
      width: 100%;
      padding: 6px;
    }
    
    .modal-canvas {
      border:2px dashed #2980b9;
      width:100%;
      height:150px;
      touch-action:none;
      background:#f0f4f8;
      border-radius:4px;
      cursor:crosshair;
    }
    
    .modal-footer {
      margin-top:12px;
      display:flex;
      gap:8px;
      justify-content:flex-end;
    }
    
    .table-wrapper {
      overflow-x:auto;
    }
    
    @media print {
      .no-print { display:none !important; }
      body { background:white; padding:0; }
      .main-container { box-shadow:none; }
      .tab-navigation { display:none; }
      .control-panel { display:none; }
    }
  </style>



<div class="main-container">
  <div class="header">
    <h1>📚 ប្រព័ន្ធកត់ត្រាបណ្ណាល័យ</h1>
    <p>Library Record Management System</p>
    <p id="schoolDisplay" style="margin-top:8px; font-size:13px;"></p>
  </div>

  <div class="tab-navigation no-print">
    <button class="tab-btn active" onclick="switchTab(0)">ក) បញ្ជីរួម</button>
    <button class="tab-btn" onclick="switchTab(1)">ខ) ខ្ចី-សង</button>
    <button class="tab-btn" onclick="switchTab(2)">គ) សកម្មភាព</button>
    <button class="tab-btn" onclick="switchTab(3)">ឃ) សារពើភ័ណ្ឌ</button>
  </div>

  <div class="tab-content active" id="tab0">
    <div class="container">
      <div class="section-header">
        <h2>ក) បញ្ជីរួម</h2>
           <p>Grand List - បញ្ជីរួម គឺជាបញ្ជីសម្រាប់កត់ត្រាឯកសារចូលគ្រប់ប្រភេទក្នុងបណ្ណាល័យ។ បញ្ជីនេះ ត្រូវបានប្រើ ដោយបណ្ណារក្ស គណៈគ្រប់គ្រងសាលា និងគណៈកម្មការទ្រទ្រង់/គ្រប់គ្រងសាលារៀន ក្នុងការត្រួតពិនិត្យ សៀវភៅក្នុងបណ្ណាល័យ។ មុននឹងចុះបញ្ជីរួម បណ្ណារក្សត្រូវប្រឹងប្រែងបែងចែកឯកសារ/សៀវភៅ ឱ្យដាច់ដោយឡែក ពីគ្នារវាងប្រភេទសៀវភៅអក្សរសិល្ប៍ សៀវភៅព័ត៌មាន និងសៀវភៅសិក្សា។ បញ្ជីរួម ត្រូវបានអនុវត្តដូចខាង ក្រោម៖</p>
<p style="text-align: left; font size-9px;">
• ការចុះបញ្ជីរួម មិនត្រូវឱ្យហួសរយៈពេលមួយសប្ដាហ៍ឡើយ ក្រោយពីពេលវេលាបានទទួលឯកសារថ្មី។<br>
• ធ្វើការបូកសរុប និងបិទបញ្ជីយ៉ាងទៀងទាត់ នៅរៀងរាល់ដំណាច់ឆ្នាំសិក្សា។<br>
• បណ្ណារក្ស ត្រូវធ្វើកំណត់សម្គាល់ចំនួនចំណងជើងសៀវភៅតាមប្រភេទ៖<br>
✓ ចំនួនចំណងជើងសៀវភៅអក្សរសិល្ប៍<br>
✓ ចំនួនចំណងជើងសៀវភៅព័ត៌មាន<br>
✓ ចំនួនចំណងជើងសៀវភៅសិក្សា</p>
<p>
✍️ភារកិច្ច : កត់ត្រាឯកសារចូលគ្រប់ប្រភេទក្នុងបណ្ណាល័យ។ <br>ការចុះបញ្ជីរួម មិនត្រូវឱ្យលើសពីមួយសប្ដាហ៍ក្រោយទទួលឯកសារថ្មី។</p>
      </div>
      <div class="input-group">
        <label>🏫 សាលា:</label>
        <input type="text" id="tab0_school" placeholder="សាលាបឋមសិក្សា រោគ">
        <label>📅 ខែ/ឆ្នាំ:</label>
        <input type="month" id="tab0_month">
      </div>

      <div class="table-wrapper">
        <table id="tab0Table">
          <thead>
            <tr>
              <th rowspan="3">ល.រ</th>
              <th rowspan="3">ថ្ងៃខែឆ្នាំចូល</th>
              <th rowspan="3">លេខបញ្ជី</th>
              <th colspan="6">សរុប ចំនួនចំណងជើង និង ចំនួនក្បាល</th>
              <th rowspan="3">សរុបរួម</th>
              <th rowspan="3">ប្រភព</th>
            </tr>
            <tr>
              <th colspan="2">សៀវភៅអក្សរសិល្ប៍</th>
              <th colspan="2">សៀវភៅព័ត៌មាន</th>
              <th colspan="2">សាមយិបត្រ</th>
            </tr>
            <tr style="font-size:9px;">
              <td>ចំណងជើង</td><td>ក្បាល(១)</td>
              <td>ចំណងជើង</td><td>ក្បាល(២)</td>
              <td>ចំណងជើង</td><td>ក្បាល(៣)</td>
            </tr>
          </thead>
          <tbody id="tab0Body"></tbody>
        </table>
      </div>

      <div class="control-panel no-print">
        <button onclick="addTab0Row()">➕ បន្ថែមជួរ</button>
      </div>
    </div>
  </div>

  <div class="tab-content" id="tab1">
    <div class="container">
      <div class="section-header">
        <h2>ខ) ប្រព័ន្ធខ្ចី-សងសៀវភៅ</h2>
      <p>Loan Record - បញ្ជីតារាងខ្ចី-សងសៀវៀក្បាលលម្អិតសម្រាប់តាមរយៈក្រុម និងខែ។បញ្ជីតារាងខ្ចី-សងសៀវភៅ ត្រូវមានទម្រង់ និងខ្លឹមសារដូចតារាងខាងក្រោម។ បញ្ជីនេះ ត្រូវរៀបចំជាមួយសៀវភៅលេខឈុត ដាច់ដោយឡែកពីគ្នាសម្រាប់ថ្នាក់នីមួយៗ ដើម្បីងាយស្រួលកត់ត្រា និងអាចគ្រប់គ្រងការខ្ចី-សងតាមថ្នាក់នីមួយៗជាប្រចាំខែ ត្រីមាស ឬប្រចាំឆ្នាំ។ ដោយកាត់ត្រាលម្អិតជាផ្នែកសម្រាប់លេខរៀងសៀវភៅ ខ្ចីនិងសង ដើម្បីមានភាពងាយស្រួល ជួយសន្សំទឹក សមស្របជាមួយបទប្បញ្ញត្តិ និងអាចគ្រប់គ្រងបាន។</p>
<p>នីតិវិធីនៃការអនុវត្តប្រព័ន្ធខ្ចី-សងសៀវភៅ<br>
    ក្នុងរយៈពេលពីរសប្តាហ៍ដំបូងបន្ទាប់ពីបណ្ណាល័យបើកដំណើរការ សិស្សមិនត្រូវបានអនុញ្ញាតឱ្យខ្ចីសៀវភៅឡើយ។ ក្នុងអំឡុងពេលនេះ គ្រូបង្រៀននិងបណ្ណារក្សត្រូវបង្រៀនសិស្សអំពីការប្រើប្រាស់បណ្ណាល័យ ដូចជាការខ្ចី-សងសៀវភៅ ការជ្រើសរើសប្រភេទសៀវភៅ គោលការណ៍បណ្ណាល័យ និងការថែរក្សាសៀវភៅ។ សិស្សទាំងអស់អាចចាប់ផ្តើមខ្ចីសៀវភៅយកទៅអាននៅផ្ទះ នៅសប្តាហ៍ទី៣ បន្ទាប់ពីបានរៀនសូត្រអំពីការប្រើប្រាស់បណ្ណាល័យរួច។ សិស្សជាច្រើនអាចមានពេលវេលាទំនេរច្រើននៅពេលចេញលេង ដើម្បីមកខ្ចីសៀវភៅ។ ដូច្នេះ សិស្សគរុសិស្ស គឺជាយន្តការពិសេសក្នុងការជួយបណ្ណារក្សកត់ត្រាការខ្ចី-សងដ៏មមាញឹកនេះ ឱ្យបានទៀងទាត់ ទាន់ពេលវេលា គ្រប់គ្រាន់ និងត្រឹមត្រូវ។ ខាងក្រោមនេះជាការរៀបចំបណ្ណាល័យសិស្សគរុសិស្ស និងដំណើរការខ្ចី-សងសៀវភៅ៖
</p>
      </div>

      <div class="input-group">
        <label>🏫 សាលា:</label>
        <input type="text" id="tab1_school" placeholder="សាលាបឋមសិក្សា រោគ">
        <label>📅 ខែ/ឆ្នាំ:</label>
        <input type="month" id="tab1_month">
      </div>

      <div class="control-panel no-print">
        <button class="btn-success" onclick="openLoanModal()">➕ ខ្ចីសៀវភៅថ្មី (Open Form)</button>
      </div>

      <div class="table-wrapper">
        <table id="tab1Table">
          <thead>
            <tr>
              <th>ល.រ</th>
              <th>គោត្តនាម</th>
              <th>នាមខ្លួន</th>
              <th>ភេទ</th>
              <th>ថ្នាក់</th>
              <th>ចំណងជើងសៀវភៅ</th>
              <th>លេខ Acc</th>
              <th>កាលបរិច្ឆេទខ្ចី</th>
              <th>ហត្ថលេខាខ្ចី</th>
              <th>កាលបរិច្ឆេទសង</th>
              <th>ហត្ថលេខាសង</th>
              <th>ផ្សេងៗ</th>
              <th class="no-print">សកម្មភាព</th>
            </tr>
          </thead>
          <tbody id="tab1Body"></tbody>
        </table>
      </div>
    </div>
  </div>

  <div class="tab-content" id="tab2">
    <div class="container">
      <div class="section-header">
        <h2>គ) សៀវភៅកត់ត្រាសកម្មភាពអំណាន</h2>
           <p>Activity Log - កត់ត្រាលម្អិតនៃសកម្មភាព និងលទ្ធផលក្នុងបណ្ណាល័យ។</p><p>សៀវភៅនេះ ត្រូវតម្កល់ទុកនៅក្នុងបណ្ណាល័យ សម្រាប់គ្រូប្រចាំថ្នាក់នីមួយៗកត់ត្រាពីសកម្មភាពអំណាន ដែលពួកគេបានដឹកនាំក្នុងម៉ោងបណ្ណាល័យ។ ព័ត៌មាននេះអាចជួយគណៈគ្រប់គ្រងសាលា ឱ្យដឹងអំពីសកម្មភាពដែលលោកគ្រូ អ្នកគ្រូបានធ្វើក្នុងម៉ោងបណ្ណាល័យ។
</p>
</div>

      <div class="input-group">
        <label>🏫 សាលា:</label>
        <input type="text" id="tab2_school" placeholder="សាលាបឋមសិក្សា រោគ">
        <label>📅 រយៈពេល:</label>
        <input type="month" id="tab2_month">
      </div>

      <div class="table-wrapper">
        <table id="tab2Table">
          <thead>
            <tr>
              <th>កាលបរិច្ឆេទ</th>
              <th>ថ្នាក់</th>
              <th>ប្រភេទអំណាន</th>
              <th>ចំណងជើងរឿង</th>
              <th>ចំនួនសិស្ស</th>
              <th>ឈ្មោះគ្រូ</th>
            </tr>
          </thead>
          <tbody id="tab2Body"></tbody>
        </table>
      </div>
      <div class="control-panel no-print">
        <button onclick="addTab2Row()">➕ បន្ថែមជួរ</button>
      </div>
    </div>
  </div>

  <div class="tab-content" id="tab3">
    <div class="container">
      <div class="section-header">
        <h2>ឃ) បញ្ជីសារពើភ័ណ្ឌសៀវភៅ</h2>
         <p>Inventory List - បញ្ជីលម្អិតសៀវភៅក្នុងបណ្ណាល័យ ដែលត្រូវបិទក្នុងរយៈពេលមិនលើសពីមួយខែក្រោយបញ្ជីរួម។</p><p>- លេខសារពើភ័ណ្ឌ៖ សៀវភៅមួយក្បាលមានលេខសារពើភ័ណ្ឌតែមួយគត់ ដោយផ្ដើមពីលេខ ០០០១។ បណ្ណារក្ស គួរចុះលេខសារពើភ័ណ្ឌនៅត្រាក្នុងបណ្ណាល័យ។ <br>ការណើសៀវភៅដូចៗគ្នា ចូលមកបណ្ណាល័យក្នុងថ្ងៃជាមួយគ្នា ត្រូវចុះលេខសារពើភ័ណ្ឌតែទីមួយ និងទីបញ្ចប់តែម្តង ដោយប្រើសញ្ញាព្រួញ (↓)។ <br>សូមមើលឧទាហរណ៍ របៀបចុះលេខនេះក្នុងតារាងខាងក្រោម។<br>
- ថ្ងៃខែឆ្នាំចូល៖ ត្រូវស្រង់ចេញពីបញ្ជីរួម។<br>
- ឈ្មោះអ្នកនិពន្ធ៖ សរសេរឈ្មោះពេញ និងមិនត្រូវចុះគោរមងាររបស់អ្នកនិពន្ធទេ។<br>
សម្គាល់៖<br>
□ ការចុះបញ្ជីសារពើភ័ណ្ឌ ត្រូវអនុវត្តមិនអោយលើសពីមួយខែ ក្រោយពីចុះបញ្ជីរួម។<br>
□ បញ្ជីសារពើភ័ណ្ឌ ត្រូវតែបិទជិតសៀវភៅ ដើម្បីជៀសវាងការបាត់បង់។</p>
      </div>

      <div class="input-group">
        <label>🏫 សាលា:</label>
        <input type="text" id="tab3_school" placeholder="សាលាបឋមសិក្សា រោគ">
        <label>📅 ខែ/ឆ្នាំ:</label>
        <input type="month" id="tab3_month">
      </div>

      <div class="table-wrapper">
        <table id="tab3Table">
          <thead>
            <tr>
              <th>លេខសារពើភ័ណ្ឌ</th>
              <th>ថ្ងៃខែឆ្នាំចូល</th>
              <th>ចំណងជើង</th>
              <th>ឈ្មោះអ្នកនិពន្ធ</th>
              <th>គ្រឹះស្ថាន</th>
              <th>ឆ្នាំបោះពុម្ព</th>
              <th>លេខកូដ DDC</th>
              <th>ប្រភេទផ្ដល់</th>
              <th>កម្រិត</th>
            </tr>
          </thead>
          <tbody id="tab3Body"></tbody>
        </table>
      </div>
      <div class="control-panel no-print">
        <button onclick="addTab3Row()">➕ បន្ថែមជួរ</button>
      </div>
    </div>
  </div>

  <div id="statusMsg" class="status-message"></div>

  <div class="control-panel no-print" style="margin:16px; border-top:2px solid #2980b9; padding-top:12px;">
    <div class="input-group" style="flex:1;">
      <label>🔑 Key (ឧ: 01030401017-2026-2B):</label>
      <input type="text" id="dataKey" placeholder="01030401017-2026">
    </div>
    <button class="btn-success" onclick="saveAllData()" style="margin-left:auto;">💾 រក្សាទុកទៅ Cloud</button>
    <button class="btn-warning" onclick="loadAllData()">📥 ផ្ទុកពី Cloud</button>
    <button onclick="window.print()">🖨️ Print / PDF</button>
  </div>
</div>

<div id="loanModal" class="modal">
  <div class="modal-content">
    <div class="modal-header">
      <h3 id="modalTitle">✍️ បំពេញព័ត៌មាន ខ្ចី-សងសៀវភៅ</h3>
      <button onclick="closeLoanModal()" class="btn btn-danger btn-small">បិទ X</button>
    </div>
    
    <input type="hidden" id="editRowIndex" value="">

    <div class="form-grid">
      <div class="form-group">
        <label>គោត្តនាម (Last Name)</label>
        <input type="text" id="formLastName" placeholder="ឧ: គឹម">
      </div>
      <div class="form-group">
        <label>នាមខ្លួន (First Name)</label>
        <input type="text" id="formFirstName" placeholder="ឧ: សុភ័ក្ត្រ">
      </div>
      <div class="form-group">
        <label>ភេទ (Gender)</label>
        <select id="formGender">
          <option value="ប្រុស">ប្រុស</option>
          <option value="ស្រី">ស្រី</option>
        </select>
      </div>
      <div class="form-group">
        <label>ថ្នាក់ (Class)</label>
        <input type="text" id="formClass" placeholder="ឧ: 4A">
      </div>
      <div class="form-group">
        <label>ចំណងជើងសៀវភៅ</label>
        <input type="text" id="formBookTitle" placeholder="ឈ្មោះសៀវភៅ">
      </div>
      <div class="form-group">
        <label>លេខ Acc (Accession No.)</label>
        <input type="text" id="formAccNum" placeholder="ឧ: 0124">
      </div>
      <div class="form-group">
        <label>កាលបរិច្ឆេទខ្ចី</label>
        <input type="date" id="formBorrowDate">
      </div>
      <div class="form-group">
        <label>កាលបរិច្ឆេទសង</label>
        <input type="date" id="formReturnDate">
      </div>
    </div>

    <div class="form-group" style="margin-bottom: 10px;">
      <label>ផ្សេងៗ (Remarks)</label>
      <input type="text" id="formRemarks" placeholder="ចំណាំផ្សេងៗ">
    </div>

    <div class="form-group">
      <label>✍️ ហត្ថលេខាសិស្ស (គូសលើប្រឡោះខាងក្រោម):</label>
      <canvas id="sigCanvas" class="modal-canvas"></canvas>
      <div style="margin-top: 5px; display: flex; gap: 5px;">
        <button type="button" onclick="clearSigCanvas()" class="btn-small btn-warning">លុបហត្ថលេខា</button>
        <span id="sigStatus" style="font-size:10px; color:green; align-self:center;"></span>
      </div>
    </div>

    <div class="modal-footer">
      <button onclick="closeLoanModal()" class="btn-danger">បោះបង់</button>
      <button onclick="submitLoanForm()" class="btn-success">💾 រក្សាទុកចូលតារាង</button>
    </div>
  </div>
</div>

<script src="https://www.gstatic.com/firebasejs/9.22.2/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.22.2/firebase-database-compat.js"></script>

<script>
  // Firebase Configuration
  const firebaseConfig = {
    apiKey: "AIzaSyB35WLr1y5_QT3j-0x7Mb2F7QaaYXLdIcQ",
    authDomain: "packagedemo-b600c.firebaseapp.com",
    databaseURL: "https://packagedemo-b600c-default-rtdb.asia-southeast1.firebasedatabase.app",
    projectId: "packagedemo-b600c",
    storageBucket: "packagedemo-b600c.firebasestorage.app",
    messagingSenderId: "601958630212",
    appId: "1:601958630212:web:e140ee683e203f3e464d11"
  };

  firebase.initializeApp(firebaseConfig);
  const db = firebase.database();

  // Signature Canvas Global Variables
  let sigCanvas, sigCtx, isDrawing = false, lastX, lastY;
  let currentSignatureData = ""; 

  function initSigCanvas() {
    sigCanvas = document.getElementById('sigCanvas');
    sigCtx = sigCanvas.getContext('2d');
    
    const ratio = window.devicePixelRatio || 1;
    sigCanvas.width = sigCanvas.offsetWidth * ratio;
    sigCanvas.height = sigCanvas.offsetHeight * ratio;
    sigCtx.scale(ratio, ratio);
    sigCtx.strokeStyle = '#1a5490';
    sigCtx.lineWidth = 3;
    sigCtx.lineJoin = 'round';
    sigCtx.lineCap = 'round';
  }

  // Tab Switching
  function switchTab(index) {
    document.querySelectorAll('.tab-content').forEach((el, i) => {
      el.classList.toggle('active', i === index);
    });
    document.querySelectorAll('.tab-btn').forEach((el, i) => {
      el.classList.toggle('active', i === index);
    });
  }

  // Status Message
  function showStatus(msg, type = 'info') {
    const el = document.getElementById('statusMsg');
    el.textContent = msg;
    el.className = 'status-message show ' + type;
    setTimeout(() => el.classList.remove('show'), 4000);
  }

  // TAB 0: Grand List
  function addTab0Row(data = {}) {
    const tbody = document.getElementById('tab0Body');
    const tr = document.createElement('tr');
    tr.innerHTML = `
      <td>${tbody.rows.length + 1}</td>
      <td><input type="date" value="${data.date || ''}"></td>
      <td contenteditable>${data.invNum || ''}</td>
      <td contenteditable>${data.lit1 || ''}</td>
      <td><input type="number" value="${data.lit1Total || 0}"></td>
      <td contenteditable>${data.info1 || ''}</td>
      <td><input type="number" value="${data.info1Total || 0}"></td>
      <td contenteditable>${data.mag1 || ''}</td>
      <td><input type="number" value="${data.mag1Total || 0}"></td>
      <td contenteditable>${data.total || 0}</td>
      <td contenteditable>${data.source || ''}</td>
    `;
    tbody.appendChild(tr);
  }

  // TAB 1: Loan Form Modal Open/Close
  function openLoanModal(rowIndex = null) {
    document.getElementById('loanModal').style.display = 'block';
    initSigCanvas();
    clearSigCanvas();
    
    const today = new Date().toISOString().split('T')[0];
    
    if (rowIndex === null) {
      // Mode: Add New Loan
      document.getElementById('modalTitle').textContent = "➕ ខ្ចីសៀវភៅថ្មី (Student Loan Form)";
      document.getElementById('editRowIndex').value = "";
      document.getElementById('formLastName').value = "";
      document.getElementById('formFirstName').value = "";
      document.getElementById('formGender').value = "ប្រុស";
      document.getElementById('formClass').value = "";
      document.getElementById('formBookTitle').value = "";
      document.getElementById('formAccNum').value = "";
      document.getElementById('formBorrowDate').value = today;
      document.getElementById('formReturnDate').value = "";
      document.getElementById('formRemarks').value = "";
      currentSignatureData = "";
    } else {
      // Mode: Edit / Update Return
      document.getElementById('modalTitle').textContent = "🔄 ធ្វើបច្ចុប្បន្នភាពទិន្នន័យ ខ្ចី-សង";
      document.getElementById('editRowIndex').value = rowIndex;
      
      const tr = document.getElementById('tab1Body').rows[rowIndex];
      document.getElementById('formLastName').value = tr.cells[1].innerText;
      document.getElementById('formFirstName').value = tr.cells[2].innerText;
      document.getElementById('formGender').value = tr.cells[3].innerText || "ប្រុស";
      document.getElementById('formClass').value = tr.cells[4].innerText;
      document.getElementById('formBookTitle').value = tr.cells[5].innerText;
      document.getElementById('formAccNum').value = tr.cells[6].innerText;
      document.getElementById('formBorrowDate').value = tr.cells[7].innerText;
      document.getElementById('formReturnDate').value = tr.cells[9].innerText || today;
      document.getElementById('formRemarks').value = tr.cells[11].innerText;
      
      // Load signature if exists
      const img = tr.cells[8].querySelector('img');
      currentSignatureData = img ? img.src : "";
    }
  }

  function closeLoanModal() {
    document.getElementById('loanModal').style.display = 'none';
  }

  // Submit/Save Form Data into Table Room
  function submitLoanForm() {
    const lastName = document.getElementById('formLastName').value.trim();
    const firstName = document.getElementById('formFirstName').value.trim();
    const gender = document.getElementById('formGender').value;
    const className = document.getElementById('formClass').value.trim();
    const bookTitle = document.getElementById('formBookTitle').value.trim();
    const accNum = document.getElementById('formAccNum').value.trim();
    const borrowDate = document.getElementById('formBorrowDate').value;
    const returnDate = document.getElementById('formReturnDate').value;
    const remarks = document.getElementById('formRemarks').value.trim();
    
    if(!firstName || !bookTitle) {
      alert("សូមបំពេញឈ្មោះសិស្ស និង ចំណងជើងសៀវភៅ!");
      return;
    }

    // Check canvas if student drew something new
    const blank = document.createElement('canvas');
    blank.width = sigCanvas.width;
    blank.height = sigCanvas.height;
    if (sigCanvas.toDataURL() !== blank.toDataURL()) {
      currentSignatureData = sigCanvas.toDataURL('image/png');
    }

    const rowIndex = document.getElementById('editRowIndex').value;
    const tbody = document.getElementById('tab1Body');

    let tr;
    if (rowIndex === "") {
      // Insert dynamic new row
      tr = document.createElement('tr');
      tbody.appendChild(tr);
    } else {
      // Use existing row index
      tr = tbody.rows[rowIndex];
    }

    const currentIdx = rowIndex === "" ? tbody.rows.length : parseInt(rowIndex) + 1;

    tr.innerHTML = `
      <td>${currentIdx}</td>
      <td>${lastName}</td>
      <td>${firstName}</td>
      <td>${gender}</td>
      <td>${className}</td>
      <td>${bookTitle}</td>
      <td>${accNum}</td>
      <td>${borrowDate}</td>
      <td>${currentSignatureData ? `<img src="${currentSignatureData}" style="max-height:30px; max-width:60px;">` : ''}</td>
      <td>${returnDate}</td>
      <td>${returnDate && currentSignatureData ? `<img src="${currentSignatureData}" style="max-height:30px; max-width:60px;">` : ''}</td>
      <td>${remarks}</td>
      <td class="no-print"><button class="btn-small btn-warning" onclick="openLoanModal(${currentIdx - 1})">កែប្រែ/សង</button></td>
    `;

    closeLoanModal();
  }

  // TAB 2: Activity Log
  function addTab2Row(data = {}) {
    const tbody = document.getElementById('tab2Body');
    const tr = document.createElement('tr');
    tr.innerHTML = `
      <td><input type="date" value="${data.date || ''}"></td>
      <td contenteditable>${data.class || ''}</td>
      <td contenteditable>${data.actType || ''}</td>
      <td contenteditable>${data.title || ''}</td>
      <td><input type="number" value="${data.count || 0}"></td>
      <td contenteditable>${data.teacher || ''}</td>
    `;
    tbody.appendChild(tr);
  }

  // TAB 3: Inventory
  function addTab3Row(data = {}) {
    const tbody = document.getElementById('tab3Body');
    const tr = document.createElement('tr');
    tr.innerHTML = `
      <td contenteditable>${data.accNum || ''}</td>
      <td><input type="date" value="${data.date || ''}"></td>
      <td contenteditable>${data.title || ''}</td>
      <td contenteditable>${data.author || ''}</td>
      <td contenteditable>${data.publisher || ''}</td>
      <td><input type="number" value="${data.year || 2026}"></td>
      <td contenteditable>${data.ddc || ''}</td>
      <td contenteditable>${data.type || ''}</td>
      <td contenteditable>${data.level || ''}</td>
    `;
    tbody.appendChild(tr);
  }

  // Initialize Sample Blank Tables
  for(let i = 0; i < 2; i++) {
    addTab0Row();
    addTab2Row();
    addTab3Row();
  }

  // Gather Data from All Components
  function gatherAllData() {
    const data = {
      meta: {
        school: document.getElementById('tab1_school').value || 'សាលាបឋមសិក្សារោគ',
        month: document.getElementById('tab1_month').value,
        timestamp: new Date().toISOString()
      },
      tab0: [],
      tab1: [],
      tab2: [],
      tab3: []
    };

    // Tab 0
    document.querySelectorAll('#tab0Body tr').forEach(tr => {
      if(tr.cells.length < 10) return;
      data.tab0.push({
        date: tr.cells[1].querySelector('input')?.value || '',
        invNum: tr.cells[2].innerText || '',
        lit1: tr.cells[3].innerText || '',
        lit1Total: tr.cells[4].querySelector('input')?.value || 0,
        info1: tr.cells[5].innerText || '',
        info1Total: tr.cells[6].querySelector('input')?.value || 0,
        mag1: tr.cells[7].innerText || '',
        mag1Total: tr.cells[8].querySelector('input')?.value || 0,
        source: tr.cells[10].innerText || ''
      });
    });

    // Tab 1 (Loan Records)
    document.querySelectorAll('#tab1Body tr').forEach(tr => {
      if(tr.cells.length < 11) return;
      data.tab1.push({
        lastName: tr.cells[1].innerText,
        firstName: tr.cells[2].innerText,
        gender: tr.cells[3].innerText,
        class: tr.cells[4].innerText,
        bookTitle: tr.cells[5].innerText,
        accNum: tr.cells[6].innerText,
        borrowDate: tr.cells[7].innerText,
        sigData: tr.cells[8].querySelector('img')?.src || '',
        returnDate: tr.cells[9].innerText,
        remarks: tr.cells[11].innerText
      });
    });

    // Tab 2
    document.querySelectorAll('#tab2Body tr').forEach(tr => {
      data.tab2.push({
        date: tr.cells[0].querySelector('input')?.value || '',
        class: tr.cells[1].innerText || '',
        actType: tr.cells[2].innerText || '',
        title: tr.cells[3].innerText || '',
        count: tr.cells[4].querySelector('input')?.value || 0,
        teacher: tr.cells[5].innerText || ''
      });
    });

    // Tab 3
    document.querySelectorAll('#tab3Body tr').forEach(tr => {
      data.tab3.push({
        accNum: tr.cells[0].innerText || '',
        date: tr.cells[1].querySelector('input')?.value || '',
        title: tr.cells[2].innerText || '',
        author: tr.cells[3].innerText || '',
        publisher: tr.cells[4].innerText || '',
        year: tr.cells[5].querySelector('input')?.value || 2026,
        ddc: tr.cells[6].innerText || '',
        type: tr.cells[7].innerText || '',
        level: tr.cells[8].innerText || ''
      });
    });

    return data;
  }

  // Save to Firebase Database
  function saveAllData() {
    const key = document.getElementById('dataKey').value.trim();
    if (!key) {
      showStatus('❌ សូមបញ្ចូលលេខសម្គាល់សាលា (Key)', 'error');
      return;
    }

    const data = gatherAllData();
    db.ref('libraryRecords/' + key).set(data)
      .then(() => showStatus('✅ រក្សាទុកឡើង Cloud បានជោគជ័យ', 'success'))
      .catch(e => showStatus('❌ មិនអាចរក្សាទុក: ' + e.message, 'error'));
  }

  // Load from Firebase
  function loadAllData() {
    const key = document.getElementById('dataKey').value.trim();
    if (!key) {
      showStatus('❌ សូមបញ្ចូលលេខសម្គាល់សាលា (Key)', 'error');
      return;
    }

    showStatus('⏳ កំពុងទាញយកទិន្នន័យ...', 'info');

    db.ref('libraryRecords/' + key).get().then(snap => {
      if (!snap.exists()) {
        showStatus('❌ គ្មានទិន្នន័យសម្រាប់ស្វែងរកឡើយ', 'error');
        return;
      }

      const data = snap.val();
      
      // Setup School Headers
      const schoolName = data.meta?.school || '';
      document.getElementById('tab0_school').value = schoolName;
      document.getElementById('tab1_school').value = schoolName;
      document.getElementById('tab2_school').value = schoolName;
      document.getElementById('tab3_school').value = schoolName;
      document.getElementById('schoolDisplay').textContent = "សាលា៖ " + schoolName;

      // Populate Tab 1 (Loans)
      const tbody1 = document.getElementById('tab1Body');
      tbody1.innerHTML = '';
      (data.tab1 || []).forEach((row, i) => {
        const tr = document.createElement('tr');
        tr.innerHTML = `
          <td>${i + 1}</td>
          <td>${row.lastName || ''}</td>
          <td>${row.firstName || ''}</td>
          <td>${row.gender || ''}</td>
          <td>${row.class || ''}</td>
          <td>${row.bookTitle || ''}</td>
          <td>${row.accNum || ''}</td>
          <td>${row.borrowDate || ''}</td>
          <td>${row.sigData ? `<img src="${row.sigData}" style="max-height:30px; max-width:60px;">` : ''}</td>
          <td>${row.returnDate || ''}</td>
          <td>${row.returnDate && row.sigData ? `<img src="${row.sigData}" style="max-height:30px; max-width:60px;">` : ''}</td>
          <td>${row.remarks || ''}</td>
          <td class="no-print"><button class="btn-small btn-warning" onclick="openLoanModal(${i})">កែប្រែ/សង</button></td>
        `;
        tbody1.appendChild(tr);
      });

      // Populate Tab 0
      document.getElementById('tab0Body').innerHTML = '';
      (data.tab0 || []).forEach(row => addTab0Row(row));

      // Populate Tab 2
      document.getElementById('tab2Body').innerHTML = '';
      (data.tab2 || []).forEach(row => addTab2Row(row));

      // Populate Tab 3
      document.getElementById('tab3Body').innerHTML = '';
      (data.tab3 || []).forEach(row => addTab3Row(row));

      showStatus('✅ បានផ្ទុកទិន្នន័យពី Cloud រួចរាល់', 'success');
    }).catch(e => showStatus('❌ ដំណើរការខុសប្រក្រតី: ' + e.message, 'error'));
  }

  // Signature Draw Logic
  function clearSigCanvas() {
    sigCtx.clearRect(0, 0, sigCanvas.width, sigCanvas.height);
  }

  document.addEventListener('DOMContentLoaded', () => {
    const canvas = document.getElementById('sigCanvas');
    if (canvas) {
      canvas.addEventListener('pointerdown', (e) => {
        isDrawing = true;
        const rect = canvas.getBoundingClientRect();
        lastX = e.clientX - rect.left;
        lastY = e.clientY - rect.top;
      });

      canvas.addEventListener('pointermove', (e) => {
        if (!isDrawing) return;
        const rect = canvas.getBoundingClientRect();
        const x = e.clientX - rect.left;
        const y = e.clientY - rect.top;
        sigCtx.beginPath();
        sigCtx.moveTo(lastX, lastY);
        sigCtx.lineTo(x, y);
        sigCtx.stroke();
        lastX = x; lastY = y;
      });

      canvas.addEventListener('pointerup', () => { isDrawing = false; });
      canvas.addEventListener('pointerleave', () => { isDrawing = false; });
    }
  });
</script>
<script defer="" src="https://static.cloudflareinsights.com/beacon.min.js/v833ccba57c9e4d2798f2e76cebdd09a11778172276447" integrity="sha512-57MDmcccJXYtNnH+ZiBwzC4jb2rvgVCEokYN+L/nLlmO8rfYT/gIpW2A569iJ/3b+0UEasghjuZH/ma3wIs/EQ==" data-cf-beacon="{&quot;version&quot;:&quot;2024.11.0&quot;,&quot;token&quot;:&quot;e3c1c9af36de41759418005494a48906&quot;,&quot;r&quot;:1,&quot;server_timing&quot;:{&quot;name&quot;:{&quot;cfCacheStatus&quot;:true,&quot;cfEdge&quot;:true,&quot;cfExtPri&quot;:true,&quot;cfL4&quot;:true,&quot;cfOrigin&quot;:true,&quot;cfSpeedBrain&quot;:true},&quot;location_startswith&quot;:null}}" crossorigin="anonymous"></script>
</template>
<template id="tpl-datascores">
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=0.85">
   <title>Dashboard with TPL Tabs</title>
    <style>
  .body { font-family: sans-serif; margin: 2px; background: #f0f0f0; }
  .tabs { display: flex; gap: 6px; margin-bottom: 1px; }
  .tab-btn {
    padding: 1px 5px; cursor: pointer; border: 1px solid #666; border-radius: 15px;
    background: #fff; user-select: none;
  }
  .tab-btn.active {
    background: #3b82f6; color: white; border-color: #2563eb;
  }
  
  iframe {
    width: 99%;
    height: 1000px; /* ធំជាងពីមុន 400px */
    border: 1px solid #ccc;
    border-radius: 15px;
    background: black;
  }
</style>
  
  <div class="tabs">
  <button class="tab-btn active" data-key="scores" onclick="switchTpl(event)">🎓 Score</button>
  <button class="tab-btn" data-key="tracking" onclick="switchTpl(event)">🏆 Tracking</button>
  <button class="tab-btn" data-key="rabies" onclick="switchTpl(event)">😽 rabies</button>
 <button class="tab-btn" data-key="standard" onclick="switchTpl(event)">✅ standard</button>
<button class="tab-btn" data-key="payment" onclick="switchTpl(event)">📦 payment</button>
<button class="tab-btn" data-key="ឆមាស១" onclick="switchTpl(event)">🎯 ឆមាស១</button>

</div>
   <!-- Two iframes for templates -->
  <iframe id="iframe-scores" style="display:block; height:700px;"></iframe>
  <iframe id="iframe-tracking" style="display:none; height:700px;"></iframe>
  <iframe id="iframe-rabies" style="display:none; height:700px;"></iframe>
  <iframe id="iframe-standard" style="display:none; height:700px;"></iframe>
  <iframe id="iframe-ឆមាស១" style="display:none; height:700px;"></iframe>
<iframe id="iframe-payment" style="display:none; height:700px;"></iframe>
  

<script>
function switchTpl(e) {
  const key = e.target.dataset.key;
  document.querySelectorAll('.tab-btn').forEach(b =>
    b.classList.toggle('active', b.dataset.key === key)
  );
  Object.keys(CFG).forEach(k => {
    document.getElementById('iframe-' + k).style.display = (k === key) ? 'block' : 'none';
  });
  loadTpl(key);
}
  const CFG = {
    scores: { tplId: 'tpl-scores' },
    tracking: { tplId: 'tpl-tracking' },
    rabies: { tplId: 'tpl-rabies' },
    standard: { tplId: 'tpl-standard' },
    ឆមាស១: { tplId: 'tpl-ឆមាស១' },
    payment: { tplId: 'tpl-payment' }
  }
  function loadTpl(key) {
    const cfg = CFG[key];
    if (!cfg) return;
    const tpl = document.getElementById(cfg.tplId);
    if (!tpl) {
      alert('Template ' + cfg.tplId + ' not found');
      return;
    }
    const html = tpl.innerHTML;
    const blob = new Blob([html], { type: 'text/html;charset=utf-8' });
    const url = URL.createObjectURL(blob);
    const iframe = document.getElementById('iframe-' + key);
    iframe.src = url;
    iframe.onload = () => {
      URL.revokeObjectURL(url);
    };
  }

  function switchTpl(e) {
    const key = e.target.dataset.key;
    // toggle active button
    document.querySelectorAll('.tab-btn').forEach(b =>
      b.classList.toggle('active', b.dataset.key === key)
    );
    // toggle iframes
    Object.keys(CFG).forEach(k => {
      document.getElementById('iframe-' + k).style.display = (k === key) ? 'block' : 'none';
    });
    // load template content
    loadTpl(key);
  }

  // init load default tab
  loadTpl('scores');
  </script>
<footer style="text-align:center; padding:12px 0; color:#6b7280; font-size:11px; border-top:1px solid #e5e7eb; margin-top:10px;">
    © 2026 របាយការណ៍សាលារៀន | ផលិតដោយ UN BUNTONG.
</footer>
<template id="tpl-scores">
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=0.85">
<title>គ្រប់គ្រងពិន្ទុ វត្តមានសិស្ស</title>
<link href="https://fonts.googleapis.com/css2?family=Hanuman:wght@400;700;900&amp;family=Battambang:wght@400;700&amp;display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0;padding:0;}
body{font-family:"Hanuman","Battambang",sans-serif;min-height:100vh;background:#f0f4f8;overflow-x:hidden;}
.bg1{position:fixed;top:-40px;right:-100px;width:320px;height:700px;border-radius:50%;background:radial-gradient(circle,rgba(37,99,235,.12),transparent);pointer-events:none;z-index:0;}
.bg2{position:fixed;bottom:-40px;left:-100px;width:310px;height:700px;border-radius:50%;background:radial-gradient(circle,rgba(16,185,129,.09),transparent);pointer-events:none;z-index:0;}

.grid-2{display:grid;grid-template-columns:1fr 1fr;gap:10px;}
.step-indicator{display:flex;align-items:center;justify-content:center;gap:10px;margin-bottom:14px;}
.step{width:30px;height:30px;border-radius:50%;border:2px solid #e5e7eb;display:flex;align-items:center;justify-content:center;font-size:13px;font-weight:800;color:#9ca3af;background:#fff;}
.step.active{border-color:#2563eb;color:#2563eb;background:#eff6ff;}
.step.done{border-color:#22c55e;color:#fff;background:#22c55e;}
.form-group select{width:100%;border:1.5px solid #e5e7eb;border-radius:14px;padding:10px 14px;font-size:13px;font-family:inherit;outline:none;background:#fff;}

/* ── AUTH ── */
#authWrap{display:flex;align-items:center;justify-content:center;min-height:100vh;padding:10px;position:relative;z-index:1;}
.auth-card{background:#fff;border-radius:22px;padding:20px 24px;width:100%;max-width:400px;box-shadow:0 20px 60px rgba(0,0,0,.18);animation:fadeIn .3s ease;}
@keyframes fadeIn{from{opacity:0;transform:translateY(16px)}to{opacity:1;transform:translateY(0)}}
.logo-area{text-align:center;margin-bottom:20px;}
.logo-icon{width:50px;height:50px;background:linear-gradient(135deg,#2563eb,#1d4ed8);border-radius:35px;font-size:20px;display:flex;align-items:center;justify-content:center;margin:0 auto 12px;}
.auth-title{font-size:14px;font-weight:900;color:#1e3a5f;margin-bottom:4px;}
.auth-sub{font-size:12px;color:#9ca3af;}
.err-msg{background:#fee2e2;color:#dc2626;border:1px solid #fca5a5;border-radius:10px;padding:9px 14px;font-size:13px;margin-bottom:14px;}
.form-group{margin-bottom:14px;}
.lbl{font-size:12px;font-weight:700;color:#374151;display:block;margin-bottom:10px;}
.form-group input{width:100%;border:1.5px solid #e5e7eb;border-radius:19px;padding:10px 14px;font-size:10px;font-family:inherit;outline:none;transition:border .2s;}
.form-group input:focus{border-color:#2563eb;}
.btn-primary{width:60%;padding:5px;background:linear-gradient(135deg,#2563eb,#1d4ed8);color:#fff;border:none;border-radius:12px;font-weight:800;font-size:10px;cursor:pointer;font-family:inherit;margin-top:4px;transition:opacity .2s;}
.btn-primary:hover{opacity:.9;}
.tab-links{text-align:center;margin-top:5px;font-size:13px;color:#6b7280;}
.tab-links a{color:#2563eb;font-weight:700;cursor:pointer;text-decoration:none;}

/* ── CLASS CARD ── */
.cls-card{background:#fff;border-radius:12px;padding:28px 22px;width:100%;max-width:320px;box-shadow:0 20px 60px rgba(0,0,0,.18);margin-top:5px;animation:fadeIn .3s ease;}
.tch-card-cls{display:flex;align-items:center;gap:12px;background:#f0f7ff;border:1px solid #bfdbfe;border-radius:14px;padding:12px 14px;margin-bottom:10px;}
.tch-avatar{font-size:20px;}
.status-badge{display:flex;align-items:center;gap:8px;border-radius:12px;padding:9px 13px;margin-bottom:16px;font-size:13px;font-weight:600;border:1px solid;}
.dot{width:8px;height:8px;border-radius:50%;flex-shrink:0;}
.cGrid{display:grid;grid-template-columns:repeat(2,1fr);gap:9px;}
.cBtn{background:#fff;border:1.5px solid #e5e7eb;border-radius:13px;padding:13px 7px;cursor:pointer;display:flex;flex-direction:column;align-items:center;gap:2px;font-family:"Hanuman","Battambang",sans-serif;transition:all .15s;}/* Ultra Small Buttons */
.btn-export, .btn, .abtn, .tbtn, .hbtn, .cbtn, .btn-edit, .btn-save, .btn-cancel {
    padding: 4px 9px !important;
    font-size: 0.72rem !important;
    min-height: 26px !important;
}
.cBtn:hover{border-color:#2563eb;background:#f0f7ff;}
.cBtn.hot{border-color:#2563eb;background:#eff6ff;}
.cBtn .cls-name{font-size:18px;font-weight:800;color:#1e3a5f;}
.cBtn .cls-hot{font-size:11px;color:#ef4444;}

/* ── LOADING / TOAST ── */
#loadOv{display:none;position:fixed;inset:0;background:rgba(255,255,255,.85);z-index:9998;align-items:center;justify-content:center;flex-direction:column;gap:12px;}
.spin{width:40px;height:40px;border:10px solid rgba(37,99,235,.2);border-top-color:#2563eb;border-radius:50%;animation:sp .30s linear infinite;}
@keyframes sp{to{transform:rotate(360deg)}}
#toast{position:fixed;top:14px;left:50%;transform:translateX(-50%);color:#fff;padding:10px 22px;border-radius:12px;font-weight:700;font-size:13px;white-space:nowrap;z-index:9999;display:none;box-shadow:0 8px 24px rgba(0,0,0,.3);font-family:"Hanuman","Battambang",sans-serif;}
#printFrame{display:none;position:fixed;top:0;left:0;width:100%;height:100%;border:none;z-index:99999;}

/* ── DASH ── */
#dash{display:none;flex-direction:column;height:100vh;overflow:hidden;background:#fff;}
.btn-primary{background:linear-gradient(135deg,#2563eb,#1d4ed8);color:#fff;border:none;border-radius:9px;padding:10px 16px;cursor:pointer;font-weight:700;font-size:8px;font-family:"Hanuman","Battambang",sans-serif;}
.cBar{display:flex;align-items:center;gap:5px;padding:5px 14px;background:#fff;border-bottom:1px solid #e5e7eb;flex-wrap:wrap;}
.cdiv{width:1px;height:8px;background:#e5e7eb;}
.chip{display:flex;align-items:center;gap:4px;}
.chip-icon{font-size:10px;}
.chip-label{color:#6b7280;font-size:10px;}
.chip-num{font-weight:800;font-size:10px;}
.btn-edit{background:#fff3cd;color:#7c5e00;border:1px solid #fcd34d;border-radius:7px;padding:6px 12px;cursor:pointer;font-size:10px;font-weight:700;}
/* ====================== ធ្វើប៊ូតុងតូចទាំងអស់ ====================== */

/* Teacher Dashboard */
.btn-export {
    padding: 5px 10px !important;
    font-size: 0.73rem !important;
    gap: 4px;
}

.btn-edit {
    padding: 3px 8px !important;
    font-size: 0.7rem !important;
}

/* Rabies Template */
.btn {
    padding: 4px 12px !important;
    font-size: 0.78rem !important;
    gap: 4px;
}

.btn-red {
    padding: 3px 8px !important;
    font-size: 0.72rem !important;
}

/* Payment Template */
.abtn {
    padding: 8px 12px !important;
    font-size: 7.5pt !important;
}

.tbtn, .hbtn, .cbtn {
    padding: 4px 8px !important;
    font-size: 7.5pt !important;
}

/* Modal buttons */
.btn-save, .btn-cancel {
    padding: 7px 16px !important;
    font-size: 0.82rem !important;
}

/* Tab buttons */
.tab-btn {
    padding: 7px 12px !important;
    font-size: 0.78rem !important;
}

/* General small button adjustment */
button {
    min-height: 10px !important;
    line-height: 0.9 !important;
}
.btn-save{background:linear-gradient(135deg,#22c55e,#16a34a);color:#fff;border:none;border-radius:7px;padding:6px 12px;cursor:pointer;font-size:12px;font-weight:700;}
.btn-cancel-sm{background:#fee2e2;color:#dc2626;border:1px solid #fca5a5;border-radius:7px;padding:6px 9px;cursor:pointer;font-size:12px;}
.btn-green{background:#dcfce7;color:#166534;border:1px solid #bbf7d0;border-radius:7px;padding:6px 12px;cursor:pointer;font-size:12px;font-weight:700;}
.btn-refresh{background:rgba(59,130,246,.1);color:#2563eb;border:1px solid rgba(59,130,246,.2);border-radius:7px;padding:6px 9px;cursor:pointer;font-size:13px;}
.btn-logout{background:#fee2e2;color:#dc2626;border:1px solid #fca5a5;border-radius:8px;padding:6px 12px;cursor:pointer;font-size:12px;font-weight:700;margin-left:auto;}
.btn-print-bar{background:#eff6ff;color:#1e40af;border:1px solid #93c5fd;border-radius:7px;padding:6px 12px;cursor:pointer;font-size:12px;font-weight:700;font-family:"Hanuman","Battambang",sans-serif;}
.eBanner{background:#fef3c7;border-left:4px solid #f59e0b;color:#78350f;padding:8px 18px;font-size:13px;font-weight:600;}
.semBar{display:flex;gap:9px;background:#f1f5f9;border-bottom:2px solid #e2e8f0;padding:11px 14px;flex-wrap:nowrap;}
.semBtn{background:#fff;border:2px solid #e5e7eb;border-radius:8px;padding:7px 18px;cursor:pointer;font-size:13px;font-weight:700;color:#6b7280;transition:all .15s;font-family:"Hanuman","Battambang",sans-serif;}
.semBtn.active{background:#eff6ff;font-weight:800;}
.monBar{display:flex;align-items:center;gap:9px;padding:9px 14px;background:#f8fafc;border-bottom:1px solid #e2e8f0;}
.monScroll{display:flex;gap:5px;overflow-x:auto;padding-bottom:1px;}
.monBtn{flex-shrink:0;background:#fff;border:1.5px solid #e5e7eb;border-radius:8px;padding:5px 12px;font-size:12px;cursor:pointer;font-weight:600;color:#374151;white-space:nowrap;font-family:"Hanuman","Battambang",sans-serif;}
.monBtn.active{background:#1e3a5f;color:#fff;border-color:#1e3a5f;}
.tchBar{background:#f0f7ff;border-bottom:1px solid #bfdbfe;padding:5px 15px;display:flex;align-items:center;gap:10px;flex-wrap:nowrap;}
.tchName{font-weight:800;color:#1e3a5f;font-size:12px;}/* Freeze 3rd column (index 2) */
.main-tbl th:nth-child(3),
.main-tbl td:nth-child(3) 
.tchDetail{color:#6b7280;font-size:12px;}
.itBar{display:flex;background:#fff;border-bottom:2px solid #e5e7eb;}
.iTab{flex:1;padding:10px 4px;border:none;background:none;cursor:pointer;font-size:10px;font-weight:600;color:#6b7280;border-bottom:2px solid transparent;margin-bottom:-2px;transition:all .15s;font-family:"Hanuman","Battambang",sans-serif;}
.iTab.active{color:#2563eb;border-bottom-color:#2563eb;background:#f0f7ff;}
.cont{overflow-y:auto;max-height:calc(100vh - 400px);}
.tWrap{overflow-x:auto;}
table.main-tbl{width:100%;border-collapse:collapse;font-size:12px;}
table.main-tbl th{background:#1e3a5f;color:#fff;padding:8px 5px;text-align:center;font-weight:700;font-size:12px;white-space:nowrap;position:sticky;top:0;z-index:2;}
table.main-tbl th.sum{background:#374151;}
table.main-tbl td{padding:6px 5px;border-bottom:1px solid #f1f5f9;color:#374151;white-space:nowrap;}
table.main-tbl td.center{text-align:center;}
table.main-tbl tr:nth-child(even){background:#f8fafc;}
table.main-tbl tr:nth-child(odd){background:#fff;}
.sticky-col{position:sticky;left:0;z-index:1;background:#f8fafc;box-shadow:2px 0 3px rgba(0,0,0,.04);}
{
    position: sticky;
    left: 0;
    background: #f0f7ff;
    z-index: 3;
    box-shadow: 2px 0 5px rgba(0,0,0,0.1);
}
/* Fix header of table */
.main-tbl thead th {
    position: sticky;
    top: 0;
    z-index: 4;
    background: #1e3a5f;
    color: white;
}
.name-cell{font-weight:600;color:#1e3a5f;display:flex;align-items:center;min-width:100px;}
.ndot{width:6px;height:8px;border-radius:50%;flex-shrink:0;display:inline-block;margin-right:5px;}
.g-badge{border-radius:10px;padding:2px 7px;font-size:11px;font-weight:600;white-space:nowrap;display:inline-block;}
.grade-badge{color:#fff;border-radius:18px;padding:2px 8px;font-size:11px;font-weight:800;}
.sum-cell{background:#f1f5f9!important;font-weight:800;font-size:13px;color:#1e3a5f;}
.ci{border:1px solid #93c5fd;border-radius:5px;padding:2px 5px;font-size:12px;width:80px;color:#1e3a5f;outline:none;}
.sipt{border:1px solid #93c5fd;border-radius:5px;padding:2px 2px;font-size:11px;width:40px;text-align:center;color:#1e3a5f;outline:none;}
.btn-del{background:#fee2e2;border:1px solid #fca5a5;border-radius:5px;padding:2px 7px;cursor:pointer;font-size:11px;}
.empty{text-align:center;padding:10px 10px;color:#9ca3af;}
.empty .e-icon{font-size:20px;margin-bottom:1px;}
.legend{display:flex;gap:6px;padding:5px 14px;background:#f8fafc;border-bottom:1px solid #e5e7eb;flex-wrap:nowrap;}
.foot{background:#1e3a5f;padding:9px 18px;display:flex;justify-content:space-between;color:rgba(255,255,255,.6);font-size:11px;flex-wrap:nowrap;gap:6px;}
.modal-ov{position:fixed;inset:0;background:rgba(0,0,0,.55);display:flex;align-items:center;justify-content:center;z-index:9000;padding:4px;}
.modal{background:#fff;border-radius:8px;padding:5px;width:100%;max-width:560px;max-height:100vh;overflow-y:auto;box-shadow:2 25px 60px rgba(0,0,0,.35);}
.modal h3{color:#1e3a5f;font-weight:800;font-size:16px;margin-bottom:5px;}
.modal-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(150px,1fr));gap:5px;}
.modal-btns{display:flex;gap:5px;margin-top:1px;justify-content:flex-end;}
.rTypeBar{display:flex;gap:4px;margin-bottom:2px;flex-wrap:nowrap;padding:0 4px;}
.rTypeBtn{background:#fff;border:2px solid #e5e7eb;border-radius:10px;padding:3px 14px;cursor:pointer;font-size:13px;font-weight:600;color:#374151;font-family:"Hanuman","Battambang",sans-serif;}
.rTypeBtn.active{background:#eff6ff;border-color:#2563eb;color:#2563eb;font-weight:800;}
.preview-note{background:#f0f7ff;border:1px solid #bfdbfe;border-radius:10px;padding:10px 14px;display:flex;justify-content:space-between;align-items:center;font-size:13px;color:#1e40af;margin:0 14px 12px;flex-wrap:nowrap;gap:4px;}
#previewPanel{background:#fff;border:1px solid #e5e7eb;border-radius:10px;padding:5px 14px;font-family:"Hanuman","Battambang",sans-serif;font-size:13px;line-height:2;overflow:auto;max-height:600px;margin:0 14px 12px;color:#1e293b;}
.kh-kingdom-header{display:flex;justify-content:center;margin-bottom:4px;}
.kh-center-block{text-align:center;flex:1;padding:0 8px;}
.kh-center-block .kingdom-title{font-size:13px;font-weight:700;color:#1a1a2e;}
.kh-center-block .motto{font-size:13px;color:#333;margin-top:5px;}
.kh-divider{border:none;border-top:5px solid #1e3a5f;margin:4px 0 7px;}
.doc-main-title{text-align:center;font-size:13px;font-weight:900;color:#b45309;margin:5px 0 5px;}
.doc-sub-title{text-align:center;font-size:13px;font-weight:800;color:#1e3a5f;margin-bottom:5px;}
.rank-table{width:100%;border-collapse:collapse;font-size:13px;margin-top:4px;}
.rank-table th{background:#d4e4f7;border:1px solid #93b8d8;padding:5px 12px;text-align:center;font-weight:700;color:#1e3a5f;white-space:nowrap;}
.rank-table td{border:1px solid #cbd5e1;padding:3.5px 2px;text-align:center;vertical-align:middle;}
.rank-table td.td-name{text-align:left;padding-left:4px;font-weight:600;white-space:nowrap;}
.rank-table tr:nth-child(even) td{background:#f8fafc;}
.rank-table tr:nth-child(odd) td{background:#fff;}
.g-A{color:#15803d;font-weight:800;}.g-B{color:#1d4ed8;font-weight:800;}.g-C{color:#b45309;font-weight:800;}
.g-D{color:#c2410c;font-weight:800;}.g-E{color:#dc2626;font-weight:800;}.g-F{color:#7f1d1d;font-weight:800;}
.pass{color:#16a34a;font-weight:700;}.fail{color:#dc2626;font-weight:700;}
.stats-block{margin-top:8px;font-size:12px;line-height:2.85;color:#1e293b;border:1px solid #cbd5e1;border-radius:10px;padding:12px;background:#f8fafc;}
.stats-grid{display:grid;grid-template-columns:1fr 1fr;gap:0 14px;}
.stats-grid span{display:block;}
.sig-section{display:flex;justify-content:space-between;margin-top:8px;font-size:10px;gap:4px;}
.sig-col{text-align:center;flex:1;}
.sig-col .sig-role{font-weight:700;color:#1e3a5f;font-size:12px;margin-top:2px;}
.sig-col .sig-date-line{font-size:12px;text-align:left;color:#374151;line-height:2.0;}
.sig-col .sig-name{font-weight:900;color:#1e3a5f;margin-top:0.5px;font-size:12px;padding-top:0.5px;border-top:1px dotted #94a3b8;}
@media print{.no-print{display:none!important;}body{background:white!important;padding:0;}#dash{box-shadow:none;border-radius:1;margin:0;}@page{size:A4;margin:.0cm .0cm;}}
</style>
    <div class="bg1"></div>
    <div class="bg2"></div>
    <div id="toast"></div>
    <div id="loadOv"><div class="spin">⏳ Firebase...</div></div>
    <iframe id="printFrame"></iframe>

    <!-- ════ AUTH SCREENS ════ -->
    <div id="authWrap">
        <div id="viewLogin" class="auth-card" style="display: block;">
            <div class="logo-area">
                <div class="logo-icon">🎓</div>
                <h2 class="auth-title">ប្រព័ន្ធគ្រប់គ្រងសាលារៀន</h2>
                <p class="auth-sub">ឆ្នាំសិក្សា ២០២៦ · Firebase Auth</p>
            </div>
            <div id="loginErr" class="err-msg" style="display: none"></div>
            <div class="form-group">
                <label class="lbl">📧 Email</label>
                <input type="email" id="loginEmail" placeholder="teacher@school.com">
            </div>
            <div class="form-group">
                <label class="lbl">🔒 Password</label>
                <input type="password" id="loginPass" placeholder="••••••">
            </div>
            <button class="btn-primary" id="btnLogin">🔐 ចូលប្រើប្រាស់</button>
            <div class="tab-links">
                <span></span><a onclick="window.showReg(1)">➕  register</a>
            </div>
        </div>

        <div id="viewClasses" class="cls-card" style="display: none">
            <div style="display: flex; justify-content: center; margin-bottom: 12px">
                <div style="width: 100px; height: 100px; background: linear-gradient(135deg, #2563eb, #1d4ed8); border-radius: 12px; font-size: 34px; display: flex; align-items: center; justify-content: center;">🇰🇭</div>
            </div>
            <h2 style="text-align: center; font-size: 20px; font-weight: 900; color: #1e3a5f; margin-bottom: 12px;">គ្រប់គ្រងពិន្ទុ វត្តមានសិស្ស</h2>
            <div class="tch-card-cls">
                <div class="tch-avatar" id="tchAvatar">👨‍🏫</div>
                <div style="flex: 1">
                    <div id="tchNameDisplay" style="font-weight: 800; color: #1e3a5f; font-size: 8px">—</div>
                    <div id="tchDetailDisplay" style="color: #6b7280; font-size: 8px">—</div>
                    <div id="tchEmailDisplay" style="color: #6b7280; font-size: 8px">—</div>
                </div>
                <button class="btn-logout" onclick="window.handleLogout()">⛔️</button>
            </div>
            <div class="status-badge" id="fbStatusBadge" style="background: #f0fdf4; border-color: #bbf7d0; color: #166534">
                <span class="dot" id="fbDot" style="background: #22c55e"></span>🔥 Realtime Database
            </div>
            <p style="font-weight: 800; color: #374151; font-size: 16px; margin-bottom: 10px;">ជ្រើសរើសថ្នាក់</p>
            <div class="cGrid" id="classGrid"></div>
        </div>

    <!-- ════ REGISTER STEP 1 ════ -->
    <div id="viewReg1" class="auth-card" style="display:none;max-width:500px">
        <button onclick="window.showLogin()" style="background:none;border:none;color:#2563eb;cursor:pointer;font-size:14px;font-weight:700;padding:0 0 12px;font-family:inherit">← ត្រឡប់</button>
        <div class="step-indicator">
            <div class="step active" id="st1">1</div>
            <div class="step" id="st2">2</div>
            <div class="step" id="st3">3</div>
        </div>
        <h2 class="auth-title" style="font-size:18px">👤 ព័ត៌មានគ្រូបង្រៀន</h2>
        <p class="auth-sub">ជំហានទី ១/៣</p>
        <div class="grid-2">
            <div class="form-group"><label class="lbl">គោត្តនាម</label><input type="text" id="r1Last" placeholder="ស្វាង"></div>
            <div class="form-group"><label class="lbl">នាម</label><input type="text" id="r1First" placeholder="មនោរម្យ"></div>
        </div>
        <div class="form-group">
            <label class="lbl">លោក / លោកស្រី / អ្នកគ្រូ</label>
            <select id="r1Title"><option>លោក</option><option>លោកស្រី</option><option>អ្នកគ្រូ</option></select>
        </div>
        <div class="form-group"><label class="lbl">📧 Email (សម្រាប់ Login)</label><input type="email" id="r1Email" placeholder="teacher@school.com"></div>
        <div class="form-group"><label class="lbl">🔒 Password (យ៉ាងតិច ៦ ខ្ទង់)</label><input type="password" id="r1Pass" placeholder="••••••"></div>
        <div class="form-group"><label class="lbl">📞 លេខទូរស័ព្ទ</label><input type="text" id="r1Phone" placeholder="0xx xxx xxx"></div>
        <button class="btn-primary" onclick="window.showReg(2)">បន្ទាប់ →</button>
    </div>

    <!-- ════ REGISTER STEP 2 ════ -->
    <div id="viewReg2" class="auth-card" style="display:none;max-width:500px">
        <button onclick="window.showReg(1)" style="background:none;border:none;color:#2563eb;cursor:pointer;font-size:14px;font-weight:700;padding:0 0 12px;font-family:inherit">← ថយក្រោយ</button>
        <div class="step-indicator">
            <div class="step done">✓</div><div class="step active">2</div><div class="step">3</div>
        </div>
        <h2 class="auth-title" style="font-size:18px">🏫 ព័ត៌មានសាលារៀន</h2>
        <p class="auth-sub">ជំហានទី ២/៣</p>
        <div class="form-group"><label class="lbl">ឈ្មោះសាលារៀន</label><input type="text" id="r2School" placeholder="សាលាបឋមសិក្សា ...."></div>
        <div class="form-group"><label class="lbl">លេខសម្គាល់សាលា</label><input type="text" id="r2SchoolID" placeholder="0......"></div>
        <div class="form-group">
            <label class="lbl">កម្រិតសិក្សា</label>
            <select id="r2Level"><option>បឋមសិក្សា</option><option>អនុវិទ្យាល័យ</option><option>វិទ្យាល័យ</option></select>
        </div>
        <button class="btn-primary" onclick="window.showReg(3)">បន្ទាប់ →</button>
    </div>

    <!-- ════ REGISTER STEP 3 ════ -->
    <div id="viewReg3" class="auth-card" style="display:none;max-width:500px">
        <button onclick="window.showReg(2)" style="background:none;border:none;color:#2563eb;cursor:pointer;font-size:14px;font-weight:700;padding:0 0 12px;font-family:inherit">← ថយក្រោយ</button>
        <div class="step-indicator">
            <div class="step done">✓</div><div class="step done">✓</div><div class="step active">3</div>
        </div>
        <h2 class="auth-title" style="font-size:18px">📍 ទីតាំងសាលារៀន</h2>
        <p class="auth-sub">ជំហានទី ៣/៣</p>
        <div class="grid-2">
            <div class="form-group">
                <label class="lbl">ខេត្ត/ក្រុង</label>
                <select id="r3Province">
                    <option>ភ្នំពេញ</option><option>កណ្តាល</option><option>កំពង់ចាម</option>
                    <option>បាត់ដំបង</option><option>សៀមរាប</option><option>ព្រះសីហនុ</option>
                    <option>ក្រចេះ</option><option>ស្ទឹងត្រែង</option><option>ត្បូងឃ្មុំ</option>
                    <option>បន្ទាយមានជ័យ</option><option>កំពង់ស្ពឺ</option><option>កំពង់ធំ</option>
                    <option>កំពង់ឆ្នាំង</option><option>ព្រៃវែង</option><option>ស្វាយរៀង</option>
                    <option>តាកែវ</option><option>ពោធិ៍សាត់</option><option>មណ្ឌលគីរី</option>
                    <option>រតនគីរី</option><option>ឧត្តរមានជ័យ</option><option>កែប</option><option>ប៉ៃលិន</option>
                    <option>ត្បូងឃ្មុំ</option>
                </select>
            </div>
            <div class="form-group"><label class="lbl">ស្រុក/ខណ្ឌ</label><input type="text" id="r3District"></div>
        </div>
        <div class="grid-2">
            <div class="form-group"><label class="lbl">ឃុំ/សង្កាត់</label><input type="text" id="r3Commune"></div>
            <div class="form-group"><label class="lbl">ភូមិ</label><input type="text" id="r3Village"></div>
        </div>
        <div id="regErr" class="err-msg" style="display:none"></div>
        <button class="btn-primary" id="btnFinish">✅ ចុះឈ្មោះ → Firebase 🔥</button>
    </div>

    </div><!-- end authWrap -->
    <div id="dash">
        <div class="hdr no-print">
            <div style="display: flex; align-items: center; gap: 20px; flex: 1; min-width: 50px;">
                <div class="hIco">🇰🇭</div>
                <div>
                    <div class="hT" id="dashTitle">🎓</div>
                    <div class="hS" id="dashSub">🇰🇭</div>
                </div>
            </div>
            <div style="display: flex; gap: 20px; align-items: center; flex-wrap: nowrap">
                <span class="hBadge" id="fbBadgeDash" style="background: rgba(34, 197, 94, 0.2); color: #86efac">🔥 Firebase</span>
                <span class="hBadge" id="monthBadge" style="background: rgba(253, 224, 71, 0.15); color: #fde047">📅 —</span>
            
            <button class="backBtn" onclick="window.goToClasses()">⛔️</button>
        </div>

        <div class="tchBar no-print" id="tchBar">
            <span style="font-size: 10px" id="tchBarAvatar">👨‍🏫</span>
            <span class="tchName" id="tchBarName">—</span>
             <span class="tchDetail" id="tchBarDetail">—</span>
             <span class="tchDetail" id="tchBarSchool">—</span>
        </div>

       <div class="cBar no-print">
            <div class="chip">
                <span class="chip-icon">👥</span><span class="chip-label">សរុប</span><span class="chip-num" id="cntTotal" style="color: #1e3a5f">0</span>
            </div>
            <div class="cdiv"></div>
            <div class="chip">
                <span class="chip-icon">👨</span><span class="chip-label">ប្រុស</span><span class="chip-num" id="cntMale" style="color: #2563eb">0</span>
            </div>
            <div class="cdiv"></div>
            <div class="chip">
                <span class="chip-icon">👩</span><span class="chip-label">ស្រី</span><span class="chip-num" id="cntFemale" style="color: #ec4899">0</span>
            </div>
            <div style="flex: 1"></div>
            <div id="editBtns">
                <button class="btn-edit" onclick="window.startEdit()">✏️ កែ</button>
            </div>
            <button class="btn-green no-print" id="btnAddStu" onclick="window.showAddModal()" style="display: none">➕ </button>
            <button class="btn-print-bar no-print" onclick="window.openIOModal()" title="Import/Export" style="background:#f5f3ff;color:#6d28d9;border-color:#c4b5fd">📦 IO</button>
            <button class="btn-refresh" onclick="window.loadAll()" title="Refresh">🔄</button>
        </div>
        <div class="eBanner no-print" id="editBanner" style="display: none">⚠️ ម៉ូតកែសម្រួល — ចុច "Save 🔥" ដើម្បី Sync Firebase</div>

        <div class="semBar no-print" id="semBar"></div>
        <div class="monBar no-print" id="monBarWrap">
            <span style="color: #374151; font-weight: 700; font-size: 10px; flex-shrink: 0;">📅 ខែ:</span>
            <div class="monScroll" id="monScroll"></div>
        </div>

        <div class="itBar no-print" id="itBar"></div>
        <div class="cont" id="content"></div>

        <div class="foot no-print">
            <span>🔥 potent-plasma-393819 · <span id="footTch">—</span></span>
            <span id="footLabel">—</span>
            <span id="footStatus" style="color: #22c55e">✅ Synced</span>
        </div>
    </div>

    <!-- Add Student Modal -->
    <div class="modal-ov" id="addModal" style="display: none">
        <div class="modal">
            <h3>➕ បន្ថែមសិស្សថ្មី → 🔥</h3>
            <div class="modal-grid" id="addModalGrid"></div>
            <div class="modal-btns">
                <button class="btn-primary" style="width: auto; padding: 4px 8px" onclick="window.handleAdd()">✅ Save 🔥</button>
                <button style="background: #f3f4f6; color: #374151; border: none; border-radius: 5px; padding: 4px 8px; cursor: pointer; font-weight: 700; font-size: 13px; font-family: inherit;" onclick="window.closeAddModal()">✕ បោះបង់</button>
            </div>
        </div>
    </div>

    <!-- Import/Export Modal -->
    <div class="modal-ov" id="ioModal" style="display:none">
      <div class="modal" style="max-width:520px">
        <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:14px">
          <h3 style="margin:0">📦 Import / Export</h3>
          <button onclick="document.getElementById('ioModal').style.display='none'" style="background:#f3f4f6;border:none;border-radius:8px;padding:6px 12px;cursor:pointer;font-size:13px;font-weight:700">✕</button>
        </div>
        <!-- Tabs -->
        <div style="display:flex;gap:6px;margin-bottom:14px">
          <button id="ioTabStu" onclick="window.ioSetTab('stu')" style="flex:1;padding:8px;border-radius:8px;border:2px solid #2563eb;background:#eff6ff;color:#2563eb;font-weight:800;cursor:pointer;font-family:inherit;font-size:13px">👤 សិស្ស</button>
          <button id="ioTabSco" onclick="window.ioSetTab('sco')" style="flex:1;padding:8px;border-radius:8px;border:2px solid #e5e7eb;background:#fff;color:#6b7280;font-weight:700;cursor:pointer;font-family:inherit;font-size:13px">📝 ពិន្ទុ</button>
        </div>
        <!-- Students panel -->
        <div id="ioPanelStu">
          <div style="background:#f0fdf4;border:1px solid #bbf7d0;border-radius:8px;padding:10px 12px;margin-bottom:12px;font-size:12px;color:#166534">
            📤 Export នឹង Download file <strong>CSV</strong> ដែលអាចបើកក្នុង Excel<br>
            📥 Import ត្រូវការ CSV format ដូច Export (row ដំបូង = header)
          </div>
          <div style="display:flex;gap:8px;margin-bottom:14px">
            <button onclick="window.exportStudentsCSV()" style="flex:1;padding:10px;background:linear-gradient(135deg,#2563eb,#1d4ed8);color:#fff;border:none;border-radius:8px;cursor:pointer;font-weight:700;font-size:13px;font-family:inherit">📤 Export CSV</button>
            <label style="flex:1;padding:10px;background:linear-gradient(135deg,#22c55e,#16a34a);color:#fff;border:none;border-radius:8px;cursor:pointer;font-weight:700;font-size:13px;text-align:center;display:block">
              📥 Import CSV
              <input type="file" accept=".csv" style="display:none" onchange="window.importStudentsCSV(this)">
            </label>
          </div>
          <div id="ioStuLog" style="background:#f8fafc;border:1px solid #e5e7eb;border-radius:8px;padding:8px 12px;font-size:11px;min-height:36px;color:#6b7280;line-height:1.7">រង់ចាំ...</div>
        </div>
        <!-- Scores panel -->
        <div id="ioPanelSco" style="display:none">
          <div style="background:#fef3c7;border:1px solid #fcd34d;border-radius:8px;padding:10px 12px;margin-bottom:12px;font-size:12px;color:#78350f">
            📤 Export ពិន្ទុ <strong id="ioScoLabel">—</strong><br>
            📥 Import — column ដំបូង=គោត្តនាម, ទី២=នាម, បន្ទាប់=វិញ្ញាសា (ត្រូវ Match ឈ្មោះ)
          </div>
          <div style="display:flex;gap:8px;margin-bottom:8px">
            <button onclick="window.exportScoresCSV()" style="flex:1;padding:10px;background:linear-gradient(135deg,#7c3aed,#6d28d9);color:#fff;border:none;border-radius:8px;cursor:pointer;font-weight:700;font-size:13px;font-family:inherit">📤 Export CSV</button>
            <label style="flex:1;padding:10px;background:linear-gradient(135deg,#f59e0b,#d97706);color:#fff;border:none;border-radius:8px;cursor:pointer;font-weight:700;font-size:13px;text-align:center;display:block">
              📥 Import CSV
              <input type="file" accept=".csv" style="display:none" onchange="window.importScoresCSV(this)">
            </label>
          </div>
          <div style="display:flex;gap:8px;margin-bottom:14px">
            <button onclick="window.exportScoresXLSX()" style="flex:1;padding:10px;background:linear-gradient(135deg,#16a34a,#15803d);color:#fff;border:none;border-radius:8px;cursor:pointer;font-weight:700;font-size:13px;font-family:inherit">📊 Export XLSX (Excel)</button>
            <button onclick="window.exportAllDataXLSX()" style="flex:1;padding:10px;background:linear-gradient(135deg,#0891b2,#0e7490);color:#fff;border:none;border-radius:8px;cursor:pointer;font-weight:700;font-size:13px;font-family:inherit">📋 Export លម្អិតទាំងអស់</button>
          </div>
          <div id="ioScoLog" style="background:#f8fafc;border:1px solid #e5e7eb;border-radius:8px;padding:8px 12px;font-size:11px;min-height:36px;color:#6b7280;line-height:1.7">រង់ចាំ...</div>
        </div>
      </div>
    </div>

    <script type="module">
  import { initializeApp } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-app.js";
  import { getAuth, createUserWithEmailAndPassword, signInWithEmailAndPassword, onAuthStateChanged, signOut } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-auth.js";
  import { getDatabase, ref, set, get, push, remove } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-database.js";

  const firebaseConfig = {
    apiKey: "AIzaSyAKVe4cAcYeRKk5k1EMcZ4usDf9bQtzVk8",
    authDomain: "potent-plasma-393819.firebaseapp.com",
    databaseURL: "https://potent-plasma-393819-default-rtdb.asia-southeast1.firebasedatabase.app",
    projectId: "potent-plasma-393819",
    storageBucket: "potent-plasma-393819.firebasestorage.app",
    messagingSenderId: "1021416054535",
    appId: "1:1021416054535:web:0e4bf3c7761ee184342fa2",
    measurementId: "G-TMY2JM9231",
  };

  const fireApp = initializeApp(firebaseConfig);
  const auth = getAuth(fireApp);
  const rtdb = getDatabase(fireApp);

  const CLASSES = ["1A","1B","2A","2B","3A","3B","4A","4B","5A","5B","6A","6B","ML","HL","3ក"];
  const MONTHS = ["ធ្នូ","មករា","កុម្ភៈ","មីនា","មេសា","ឧសភា","មិថុនា","កក្កដា","សីហា","កញ្ញា","តុលា","វិច្ឆិកា"];
  const SEMESTERS = [
    { id: "s1", label: "ឆមាស១", months: [0,1,2,3,4,5], color: "#2563eb" },
    { id: "s2", label: "ឆមាស២", months: [6,7,8,9,10,11], color: "#7c3aed" },
    { id: "annual", label: "ដំណាច់ឆ្នាំ", months: [], color: "#b45309" },
  ];
  const SUBJECTS = ["សមត្ថភាពស្ដាប់","សមត្ថភាពសរសេរ","សមត្ថភាពអាន","សមត្ថភាពនិយាយ","ចំនួន","រង្វាស់រង្វាល់","ធរណីមាត្រ","ពីជគណិត","ស្ថិតិ","វិទ្យាសាស្ត្រ","សិក្សាសង្គម","គេហ-សិល្បៈ","អប់រំកាយ-សុខភាព","បំណិន","ភាសាបរទេស"];

  const INNER_TABS = [
    { id: "info", icon: "👤", label: "សិស្ស" },
    { id: "scores", icon: "📝", label: "ប្រឡង" },
    { id: "attendance", icon: "✅", label: "អវត្តមាន"},
    { id: "detail", icon: "📊", label: "លម្អិត" },
    { id: "report", icon: "🖨️", label: "របាយការណ៍" },
    { id: "honor", icon: "🏆", label: "កិត្តិយស" },
    { id: "gradeanalysis", icon: "🎯", label: "និទ្ទេស" },
  ];

  const BLANK = {lastName:'',firstName:'',gender:'ប្រុស',dob:'',fatherName:'',motherName:'',village:'',commune:'',district:'',province:'',phone:''};
  const ROWS_PER_COLUMN = 17;

// ════ KHMER DATE FUNCTIONS ════
  function toKhNum(n){ const d=['០','១','២','៣','៤','៥','៦','៧','៨','៩']; return String(n).replace(/\d/g,c=>d[+c]); }
  const KH_MONTHS_SOLAR=['មករា','កុម្ភៈ','មីនា','មេសា','ឧសភា','មិថុនា','កក្កដា','សីហា','កញ្ញា','តុលា','វិច្ឆិកា','ធ្នូ'];
  const KH_WEEKDAYS=['អាទិត្យ','ចន្ទ','អង្គារ','ពុធ','ព្រហស្បតិ៍','សុក្រ','សៅរ៍'];
  const KH_ANIMALS=['ជូត','ឆ្លូវ','ខាល','ថោះ','រោង','ម្សាញ់','មមី','មមែ','វក','រកា','ច','កុរ'];
  const KH_SAK=['ឯក','ទោ','ត្រី','ចត្វា','បញ្ចស័ក','ឆ','សប្ត','អដ្ឋ','នព','សំរឹទ្ធ'];
  function moonPhase(date){ const r=new Date('2000-01-06T18:14:00Z'),syn=29.53059,diff=(date-r)/864e5+7/24; return((diff%syn)+syn)%syn; }
  function khLunarMonth(nm){ const m=nm.getMonth(),d=nm.getDate(),ranges=[[1,6,2,17,'ផល្គុន'],[2,18,3,16,'ចេត្រ'],[3,17,4,15,'វិសាខ'],[4,16,5,14,'ជេស្ឋ'],[5,15,6,13,'អាសាឍ'],[6,14,7,12,'ស្រាពណ៍'],[7,13,8,10,'ភទ្របទ'],[8,11,9,9,'អស្សុជ'],[9,10,10,8,'កក្តិក'],[10,9,11,7,'មិគសិរ'],[11,8,0,6,'បុស្ស']]; for(const[sm,sd,em,ed,name]of ranges){ if(sm>em){ if(m===sm&&d>=sd)return name; if(m===em&&d<=ed)return name; } else{ if(m===sm&&d>=sd&&(m!==em||d<=ed))return name; if(m>sm&&m<em)return name; if(m===em&&d<=ed)return name; } } return'មាឃ'; }
  function khAnimal(date){ const y=date.getFullYear(),mo=date.getMonth(),dy=date.getDate(),adj=mo<3||(mo===3&&dy<14)?y-1:y; return KH_ANIMALS[(((adj-2025+5)%12)+12)%12]; }
  function khSak(date){ return KH_SAK[(date.getFullYear()+543+8)%10]; }
  function fmtKhDate(date){ const ph=moonPhase(date),raw=Math.floor(ph); const dayType=raw<15?'កើត':'រោច',dayNum=raw<15?raw+1:raw-14; const nm=new Date(date-ph*864e5); const lunar=`ថ្ងៃ${KH_WEEKDAYS[date.getDay()]} ${toKhNum(dayNum)}${dayType} ខែ${khLunarMonth(nm)} ឆ្នាំ${khAnimal(date)} ${khSak(date)}ស័ក ព.ស ${toKhNum(date.getFullYear()+543)}`; const solar=`ថ្ងៃទី${toKhNum(date.getDate())} ខែ${KH_MONTHS_SOLAR[date.getMonth()]} ឆ្នាំ${toKhNum(date.getFullYear())}`; return{lunar,solar}; }
  function addWD(date,n){ let d=new Date(date),c=0; while(c<n){ d.setDate(d.getDate()+1); if(d.getDay()!==0&&d.getDay()!==6)c++; } return d; }

  let teacher = null, selClass = null, semester = "s1", selMonth = 0, innerTab = "info";
  let editMode = false, reportType = "monthly", detailSem = "s1";
  let students = {}, scores = {}, attendance = {}, semesterScores = {};
  let localStu = {}, localSco = {}, localAtt = {};
  let detailAllMonthsData = {};
  let newStu = { ...BLANK }, pollId = null;
  let honorPhotos = {}; // sid -> base64 photo

  const $ = (id) => document.getElementById(id);

  function toast(msg, type = "success") {
    const t = $("toast");
    t.textContent = msg;
    t.style.background = type === "error" ? "#ef4444" : type === "info" ? "#3b82f6" : "#22c55e";
    t.style.display = "block";
    clearTimeout(t._t);
    t._t = setTimeout(() => { t.style.display = "none"; }, 3000);
  }

  function loading(on) { $("loadOv").style.display = on ? "flex" : "none"; }

  function gradeOf(avg) {
    const val = Number(avg);
    if (val >= 9.5) return { l: "A", c: "#15803d" };
    if (val >= 8) return { l: "B", c: "#1d4ed8" };
    if (val >= 7.5) return { l: "C", c: "#b45309" };
    if (val >= 6) return { l: "D", c: "#c2410c" };
    if (val >= 5) return { l: "E", c: "#dc2626" };
    return { l: "F", c: "#7f1d1d" };
  }

  function resultOf(avg) { return Number(avg) >= 5 ? "ជាប់" : "ធ្លាក់"; }

  function stuList() {
    return Object.entries(localStu)
      .map(([id, v]) => ({ ...v, id }))
      .sort((a, b) => (a.lastName || "").localeCompare(b.lastName || "", "km"));
  }

  function getSco(sid, subj) { return localSco[sid]?.[subj] ?? ""; }

  function truncate2(n) { return Math.floor(Number(n) * 100) / 100; }
  function fmtAvg(n) { const v = truncate2(n); return v > 0 ? v.toFixed(2) : "0.00"; }

  function getAvg(sid, src = localSco) {
    const vals = SUBJECTS.map((s) => getSco(sid, s)).filter((v) => v !== undefined && v !== "");
    if (!vals.length) return 0;
    return truncate2(vals.reduce((a, b) => a + Number(b), 0) / vals.length);
  }

  function getTotal(sid, src = localSco) {
    return SUBJECTS.reduce((a, s) => a + (Number(getSco(sid, s)) || 0), 0);
  }

  function getRank(sid) {
    return [...stuList()]
      .sort((a, b) => getAvg(b.id) - getAvg(a.id))
      .findIndex((s) => s.id === sid) + 1;
  }

  function getSemesterAvg(sid, semesterId) {
    const cs = SEMESTERS.find(s => s.id === semesterId);
    if (!cs || cs.months.length === 0) return 0;
    let totalScore = 0, count = 0;
    cs.months.forEach(monthIdx => {
      const monthAvg = getMonthAvg(sid, monthIdx);
      if (monthAvg > 0) { totalScore += monthAvg; count++; }
    });
    return count > 0 ? truncate2(totalScore / count) : 0;
  }

  function getMonthAvg(sid, monthIdx) { return Number(getAvg(sid)); }

  function getAnnualAvg(sid) {
    const s1 = Number(getSemesterAvg(sid, 's1'));
    const s2 = Number(getSemesterAvg(sid, 's2'));
    const count = (s1 > 0 ? 1 : 0) + (s2 > 0 ? 1 : 0);
    if (count === 0) return 0;
    return count === 0 ? 0 : truncate2((s1 + s2) / count);
  }

  function getAtt(sid, day) { return localAtt[sid]?.[day] ?? ""; }

  function cntAtt(sid, type) {
    return Array.from({ length: 31 }, (_, i) => i + 1).filter((d) => getAtt(sid, d) === type).length;
  }

  function curSem() { return SEMESTERS.find((s) => s.id === semester); }

  function buildRankedList(sl) {
    const sorted = [...sl].sort((a, b) => Number(getAvg(b.id)) - Number(getAvg(a.id)));
    const result = [];
    sorted.forEach((s, i) => {
      if (i > 0 && getAvg(s.id) === getAvg(sorted[i - 1].id)) {
        result.push({ ...s, _rank: result[i - 1]._rank });
      } else {
        result.push({ ...s, _rank: i + 1 });
      }
    });
    return result;
  }

  async function dbGet(path) { const snap = await get(ref(rtdb, path)); return snap.val(); }
  async function dbSet(path, data) { await set(ref(rtdb, path), data); }
  async function dbPush(path, data) { const r = await push(ref(rtdb, path), data); return r.key; }
  async function dbDel(path) { await remove(ref(rtdb, path)); }

  async function loadMonthsForSemesters(semIds) {
    if (!selClass) return;
    loading(true);
    try {
      const fetches = [];
      semIds.forEach(semId => {
        const cs = SEMESTERS.find(s => s.id === semId);
        if (!cs) return;
        cs.months.forEach(mIdx => {
          const key = `${semId}_${mIdx}`;
          if (detailAllMonthsData[key] === undefined) {
            fetches.push(
              dbGet(`plp2026/${selClass}/scores/${semId}/${mIdx}`)
                .then(data => { detailAllMonthsData[key] = data || {}; })
            );
          }
        });
      });
      await Promise.all(fetches);
    } catch(e) { toast("❌ " + e.message, "error"); }
    loading(false);
  }

  function isMonthsLoaded(semIds) {
    return semIds.every(semId => {
      const cs = SEMESTERS.find(s => s.id === semId);
      if (!cs) return true;
      return cs.months.every(mIdx => detailAllMonthsData[`${semId}_${mIdx}`] !== undefined);
    });
  }

  function getMonthAvgFromAll(sid, semId, mIdx) {
    const key = `${semId}_${mIdx}`;
    const stuData = (detailAllMonthsData[key] || {})[sid] || {};
    const vals = SUBJECTS.map(subj => stuData[subj]).filter(v => v !== undefined && v !== "" && !isNaN(Number(v)));
    return vals.length > 0 ? vals.reduce((a, b) => a + Number(b), 0) / vals.length : null;
  }

  function getSemAvgFromAll(sid, semId) {
    const cs = SEMESTERS.find(s => s.id === semId);
    if (!cs) return null;
    
    // បង្កើត col11 = មធ្យមលេខ 3 ខែទីមួយ
    const firstThreeMonths = cs.months.slice(0, 3);
    const col11Avgs = firstThreeMonths.map(mIdx => getMonthAvgFromAll(sid, semId, mIdx)).filter(v => v !== null);
    const col11 = col11Avgs.length > 0 ? col11Avgs.reduce((a, b) => a + b, 0) / col11Avgs.length : null;
    
    // បង្កើត col12 = (col11 + ខែទី4) / 2
    if (col11 !== null && cs.months.length > 3) {
      const fourthMonthAvg = getMonthAvgFromAll(sid, semId, cs.months[3]);
      if (fourthMonthAvg !== null) {
        return (col11 + fourthMonthAvg) / 2;
      }
    }
    
    // ប្រសិនបើគ្មានខែទី4 ឬលេខអវត្តមាន ត្រឡប់ col11
    return col11;
  }

  function getCol11FromAll(sid, semId) {
    const cs = SEMESTERS.find(s => s.id === semId);
    if (!cs) return null;
    
    // col11 = មធ្យមលេខ 3 ខែទីមួយ
    const firstThreeMonths = cs.months.slice(0, 3);
    const col11Avgs = firstThreeMonths.map(mIdx => getMonthAvgFromAll(sid, semId, mIdx)).filter(v => v !== null);
    return col11Avgs.length > 0 ? col11Avgs.reduce((a, b) => a + b, 0) / col11Avgs.length : null;
  }

  // ════ 2-COLUMN LAYOUT FUNCTIONS ════
  function splitStudentsIntoColumns(studentList) {
    const totalStudents = studentList.length;
    // If >= 17 students, use 2-column layout. Otherwise, use single column
    if (totalStudents >= 17) {
      const half = Math.ceil(totalStudents / 2);
      const col1 = studentList.slice(0, half);
      const col2 = studentList.slice(half);
      return { col1, col2 };
    } else {
      // Single column: all students in col1, col2 is empty
      return { col1: studentList, col2: [] };
    }
  }
  
    function buildMonthlyReportTwoColumn(ranked) {
    const sorted = buildRankedList(ranked);
    const { col1, col2 } = splitStudentsIntoColumns(sorted);
    
    // Auto layout: use 2 columns if col2 has data, otherwise 1 column
    const gridCols = col2.length > 0 ? "1fr 1fr" : "1fr";
    let html = `<div style="display: grid; grid-template-columns: ${gridCols}; gap: 12px; margin-top: 6px;">`;
    
    // LEFT COLUMN
    html += `<table class="rank-table" style="font-size: 12px;">
      <thead>
        <tr>
          <th style="width:16px">ល.រ</th>
          <th style="min-width:100px;text-align:left">គោត្តនាម-នាម</th>
          <th style="width:16px">ភេទ</th>
          <th style="min-width:60px;text-align:center">ថ្ងៃខែឆ្នាំកំណើត</th>
          <th style="width:28px">ពិន្ទុសរុប</th>
          <th style="width:24px">ម.ប្រឡង</th>
          <th style="width:18px">ចំ.ថ្នាក់</th>
          <th style="width:20px">និទ្ទេស</th>
        </tr>
      </thead>
      <tbody>`;
    
    col1.forEach((s, idx) => {
      const total = getTotal(s.id);
      const avg = Number(getAvg(s.id));
      const avgDisp = avg > 0 ? fmtAvg(avg) : "—";
      const g = gradeOf(avg);
      const serial = idx + 1;
      
      html += `<tr>
        <td style="text-align:center;font-weight:600;font-size:12px">${serial}</td>
        <td style="text-align:left;font-weight:600;font-size:12px">${s.lastName} ${s.firstName}</td>
        <td style="text-align:center;font-size:12px">${s.gender === "ស្រី" ? "ស" : "ប"}</td>
        <td style="text-align:center;font-size:12px">${s.dob || "—"}</td>
        <td style="text-align:center;font-weight:700;color:#2563eb;font-size:12px">${total}</td>
        <td style="text-align:center;font-weight:700;font-size:12px">${avgDisp}</td>
        <td style="text-align:center;font-size:12px">${s._rank}</td>
        <td style="text-align:center"><span class="g-${g.l}" style="font-size:12px">${g.l}</span></td>
      </tr>`;
    });
    
    html += `</tbody></table>`;
    
    // RIGHT COLUMN - Only render if col2 has data
    if (col2.length > 0) {
      html += `<table class="rank-table" style="font-size: 12px;">
        <thead>
          <tr>
            <th style="width:16px">ល.រ</th>
            <th style="min-width:100px;text-align:left">គោត្តនាម-នាម</th>
            <th style="width:16px">ភេទ</th>
            <th style="min-width:60px;text-align:center">ថ្ងៃខែឆ្នាំកំណើត</th>
            <th style="width:28px">ពិន្ទុសរុប</th>
            <th style="width:24px">ម.ប្រឡង</th>
            <th style="width:18px">ចំ.ថ្នាក់</th>
            <th style="width:20px">និទ្ទេស</th>
          </tr>
        </thead>
        <tbody>`;
      
      col2.forEach((s, idx) => {
        const total = getTotal(s.id);
        const avg = Number(getAvg(s.id));
        const avgDisp = avg > 0 ? fmtAvg(avg) : "—";
        const g = gradeOf(avg);
        const serial = col1.length + idx + 1;
        
        html += `<tr>
          <td style="text-align:center;font-weight:600;font-size:12px">${serial}</td>
          <td style="text-align:left;font-weight:600;font-size:12px">${s.lastName} ${s.firstName}</td>
          <td style="text-align:center;font-size:12px">${s.gender === "ស្រី" ? "ស" : "ប"}</td>
          <td style="text-align:center;font-size:12px">${s.dob || "—"}</td>
          <td style="text-align:center;font-weight:700;color:#2563eb;font-size:12px">${total}</td>
          <td style="text-align:center;font-weight:700;font-size:12px">${avgDisp}</td>
          <td style="text-align:center;font-size:12px">${s._rank}</td>
          <td style="text-align:center"><span class="g-${g.l}" style="font-size:12px">${g.l}</span></td>
        </tr>`;
      });
      
      html += `</tbody></table>`;
    }
    
    html += `</div>`;
    return html;
  }

  function buildSemesterReportTwoColumn(ranked) {
    const cs = SEMESTERS.find(s => s.id === semester);
    const months = cs ? cs.months : [];
    const sorted = buildRankedList(ranked);
    const examMonth  = semester === "s1" ? 3 : months[months.length - 1];
    const contMonths = months.filter(m => m !== examMonth);
    const { col1, col2 } = splitStudentsIntoColumns(sorted);

    const fmtA = v => v !== null ? fmtAvg(v) : "—";

    function buildSemColRows(col, startIdx) {
      let rows = "";
      col.forEach((s, idx) => {
        const serial = startIdx + idx + 1;
        const contVals = contMonths.map(m => getMonthAvgFromAll(s.id, semester, m)).filter(v => v !== null);
        const monthlyAvg = contVals.length > 0 ? contVals.reduce((a,b) => a+b, 0) / contVals.length : null;
        const examAvg = getMonthAvgFromAll(s.id, semester, examMonth);
        const semVals = [monthlyAvg, examAvg].filter(v => v !== null);
        const semAvg = semVals.length > 0 ? semVals.reduce((a,b) => a+b, 0) / semVals.length : null;
        const g = gradeOf(semAvg ?? 0);
        rows += `<tr>
          <td style="text-align:center;font-size:12px">${serial}</td>
          <td style="text-align:left;font-weight:600;font-size:12px">${s.lastName} ${s.firstName}</td>
          <td style="text-align:center;font-size:12px">${s.gender === "ស្រី" ? "ស" : "ប"}</td>
          <td style="text-align:center;font-size:12px">${s.dob || "—"}</td>
          <td style="text-align:center;font-size:12px">${fmtA(monthlyAvg)}</td>
          <td style="text-align:center;font-size:12px">${fmtA(examAvg)}</td>
          <td style="text-align:center;font-weight:800;font-size:12px;color:#1e3a5f">${fmtA(semAvg)}</td>
          <td style="text-align:center;font-size:12px">${s._rank}</td>
          <td style="text-align:center"><span class="g-${g.l}" style="font-size:12px">${g.l}</span></td>
          <td style="text-align:center;font-size:12px" class="${(semAvg??0)>=5?'pass':'fail'}">${resultOf(semAvg??0)}</td>
        </tr>`;
      });
      return rows;
    }

    const thead = `<thead><tr>
      <th style="width:16px">ល.រ</th>
      <th style="min-width:100px;text-align:left">គោត្តនាម-នាម</th>
      <th style="width:16px">ភេទ</th>
      <th style="min-width:55px;text-align:center">ថ្ងៃខែឆ្នាំកំណើត</th>
      <th style="width:30px">ម.ប្រចាំខែ</th>
      <th style="width:30px">ម.ប្រឡង</th>
      <th style="width:30px">ម.ឆមាស</th>
      <th style="width:20px">ចំ.ថ្នាក់</th>
      <th style="width:20px">និទ្ទេស</th>
      <th style="width:26px">លទ្ធផល</th>
    </tr></thead>`;

    // Auto layout: use 2 columns if col2 has data, otherwise 1 column
    const gridCols = col2.length > 0 ? "1fr 1fr" : "1fr";
    let html = `<div style="display:grid;grid-template-columns:${gridCols};gap:12px;margin-top:6px;">`;
    
    html += `<table class="rank-table" style="font-size:12px;">${thead}<tbody>${buildSemColRows(col1, 0)}</tbody></table>`;
    
    // RIGHT COLUMN - Only render if col2 has data
    if (col2.length > 0) {
      html += `<table class="rank-table" style="font-size:12px;">${thead}<tbody>${buildSemColRows(col2, col1.length)}</tbody></table>`;
    }
    
    html += `</div>`;
    return html;
  }

  function buildDocHTML() {
    const sl = stuList();
    const tName = `${teacher?.title || ""} ${teacher?.fullName || teacher?.email || ""}`.trim();
    const school = teacher?.school || "សាលាបឋមសិក្សា";
    let html = `<div class="kh-kingdom-header"><div class="kh-center-block"><div class="kingdom-title">ព្រះរាជាណាចក្របកម្ពុជា</div><div class="motto">ជាតិ សាសនា ព្រះមហាក្សត្រ</div></div></div>`;
    html += `<div style="text-align:left;font-size:12px;color:#1e3a5f;line-height:1.8;margin-bottom:4px"><div><strong>រដ្ឋបាលស្រុកភ្នំស្រុក</strong></div><div><strong>ការិយាល័យអប់រំ យុវជន និងកីឡាស្រុក</strong></div><div><strong>កម្រងស្ពានស្រែង</strong></div><div>${school} រោគ</div></div>`;
    html += `<hr class="kh-divider"/>`;

    if (reportType === "monthly") {
      html += `<div class="doc-main-title">លទ្ធផលសិក្សាប្រចាំខែ${MONTHS[selMonth]}</div>`;
      html += `<div class="doc-sub-title">ថ្នាក់ទី${selClass}</div>`;
      html += buildMonthlyReportTwoColumn(sl);
      html += buildStatsHtmlNew(sl);
      html += buildSignatureHtml(tName, "monthly");
    } else if (reportType === "semester") {
      html += `<div class="doc-main-title">លទ្ធផលសិក្សា${curSem().label}</div>`;
      html += `<div class="doc-sub-title">ថ្នាក់ទី${selClass}</div>`;
      html += buildSemesterReportTwoColumn(sl);
      html += buildStatsHtmlNew(sl);
      html += buildSignatureHtml(tName, "semester");
    } else if (reportType === "detail") {
      html += `<div class="doc-main-title">លម្អិតលទ្ធផលសិក្សា</div>`;
      html += `<div class="doc-sub-title">ថ្នាក់ទី ${selClass}</div>`;
      html += `<div style="margin-top:14px;color:#1e3a5f;font-weight:800;font-size:13px;margin-bottom:6px">📚 ឆមាស១</div>`;
      html += buildDetailTable(sl, "s1");
      html += `<div style="margin-top:20px;color:#1e3a5f;font-weight:800;font-size:13px;margin-bottom:6px">📚 ឆមាស២</div>`;
      html += buildDetailTable(sl, "s2");
      html += buildStatsHtmlNew(sl);
      html += buildSignatureHtml(tName, "semester");
    } else if (reportType === "annual") {
      html += `<div class="doc-main-title">ចំណាត់ថ្នាក់ដំណាច់ឆ្នាំ</div>`;
      html += `<div class="doc-sub-title">ថ្នាក់ទី${selClass}</div>`;
      html += buildAnnualReportTable(sl);
      html += buildStatsHtmlNew(sl);
      html += buildSignatureHtml(tName, "annual");
    } else if (reportType === "attendance") {
      html += `<div class="doc-main-title">របាយការណ៍វត្តមាន</div>`;
      html += `<div class="doc-sub-title">ថ្នាក់ទី${selClass}</div>`;
      html += buildAttendanceTable(sl);
    }
    return html;
  }

  function getPrintableHTML() {
    const docHTML = buildDocHTML();
    return `<!DOCTYPE html><html lang="km"><head><meta charset="UTF-8"><title>លទ្ធផលសិក្សា</title><link href="https://fonts.googleapis.com/css2?family=Hanuman:wght@400;700;900&family=Battambang:wght@400;700&display=swap" rel="stylesheet"><style>*{box-sizing:border-box;margin:0;padding:0}body{font-family:'Hanuman','Battambang',sans-serif;font-size:11.5px;line-height:1.55;padding:.6cm .8cm;color:#1e293b}@page{size:A4;margin:.6cm .8cm}.kh-kingdom-header{display:flex;justify-content:center;margin-bottom:4px}.kh-center-block{text-align:center;flex:1;padding:0 8px}.kh-center-block .kingdom-title{font-size:13px;font-weight:900;color:#1a1a2e}.kh-center-block .motto{font-size:11px;color:#333;margin-top:1px}.kh-divider{border:none;border-top:2px solid #1e3a5f;margin:4px 0 7px}.doc-main-title{text-align:center;font-size:15px;font-weight:900;color:#b45309;margin:5px 0 1px}.doc-sub-title{text-align:center;font-size:13px;font-weight:800;color:#1e3a5f;margin-bottom:1px}.rank-table{width:100%;border-collapse:collapse;font-size:10px;margin-top:4px}.rank-table th{background:#d4e4f7;border:1px solid #93b8d8;padding:3px 2px;text-align:center;font-weight:700;color:#1e3a5f}.rank-table td{border:1px solid #cbd5e1;padding:2.5px 2px;text-align:center}.rank-table td.td-name{text-align:left;padding-left:4px;font-weight:600}.rank-table tr:nth-child(even) td{background:#f8fafc}.g-A{color:#15803d;font-weight:800}.g-B{color:#1d4ed8;font-weight:800}.g-C{color:#b45309;font-weight:800}.g-D{color:#c2410c;font-weight:800}.g-E{color:#dc2626;font-weight:800}.g-F{color:#7f1d1d;font-weight:800}.pass{color:#16a34a;font-weight:700}.fail{color:#dc2626;font-weight:700}.sig-section{display:flex;justify-content:space-between;margin-top:12px;font-size:10px;gap:4px}.sig-col{text-align:center;flex:1}.sig-col .sig-role{font-weight:700;color:#1e3a5f;font-size:10.5px;margin-top:2px}.sig-col .sig-date-line{font-size:9px;text-align:left;color:#374151;line-height:1.6}.sig-col .sig-name{font-weight:900;color:#1e3a5f;margin-top:20px;font-size:11px;padding-top:2px;border-top:1px dotted #94a3b8}</style></head><body>${docHTML}</body></html>`;
  }

  function doPrint() {
    const printWin = window.open('', '_blank');
    if (!printWin) {
      const frame = $('printFrame');
      const doc = frame.contentDocument || frame.contentWindow.document;
      doc.open(); doc.write(getPrintableHTML()); doc.close();
      setTimeout(() => { frame.style.display = 'block'; frame.contentWindow.focus(); frame.contentWindow.print(); setTimeout(() => { frame.style.display = 'none'; }, 2000); }, 700);
      return;
    }
    printWin.document.write(getPrintableHTML());
    printWin.document.close();
    printWin.onload = function() {
      setTimeout(() => { printWin.focus(); printWin.print(); }, 500);
    };
    setTimeout(() => {
      if (printWin && !printWin.closed) { printWin.focus(); printWin.print(); }
    }, 1200);
  }
  window.doPrint = doPrint;

  window.doPrintReport = function() {
    if (innerTab !== "report") {
      innerTab = "report";
      buildItBar();
      renderContent();
      updateEditUI();
      setTimeout(() => doPrint(), 400);
    } else {
      doPrint();
    }
  };

  window.showLogin = function () {
    ["viewReg1","viewReg2","viewReg3","viewClasses"].forEach(id => {
      const el = document.getElementById(id);
      if (el) el.style.display = "none";
    });
    $("viewLogin").style.display = "block";
  };

  // ── 3-step registration ──
  const REG_VIEWS = ["viewLogin","viewClasses","viewReg1","viewReg2","viewReg3"];
  window.showReg = function (step) {
    REG_VIEWS.forEach(id => {
      const el = document.getElementById(id);
      if (el) el.style.display = "none";
    });
    const v = document.getElementById("viewReg" + step);
    if (v) v.style.display = "block";
  };

  // Step 1 → 2: validate email + password
  document.getElementById("viewReg1").querySelector(".btn-primary").onclick = function () {
    const email = $("r1Email").value.trim();
    const pass  = $("r1Pass").value;
    const last  = $("r1Last").value.trim();
    const first = $("r1First").value.trim();
    if (!last || !first) { toast("⚠️ សូមបំពេញ គោត្តនាម និង នាម!", "error"); return; }
    if (!email || !email.includes("@")) { toast("⚠️ Email មិនត្រឹមត្រូវ!", "error"); return; }
    if (pass.length < 6) { toast("⚠️ Password យ៉ាងតិច ៦ ខ្ទង់!", "error"); return; }
    window.showReg(2);
  };

  // btnFinish: create Firebase Auth + save teacher profile
  document.getElementById("btnFinish").onclick = async function () {
    const email    = $("r1Email").value.trim();
    const pass     = $("r1Pass").value;
    const fullName = $("r1Last").value.trim() + " " + $("r1First").value.trim();
    const profile  = {
      fullName,
      title:    $("r1Title").value,
      phone:    $("r1Phone").value.trim(),
      email,
      school:   $("r2School").value.trim(),
      schoolID: $("r2SchoolID").value.trim(),
      level:    $("r2Level").value,
      province: $("r3Province").value,
      district: $("r3District").value.trim(),
      commune:  $("r3Commune").value.trim(),
      village:  $("r3Village").value.trim(),
      createdAt: Date.now(),
    };
    const errEl = $("regErr");
    errEl.style.display = "none";
    loading(true);
    try {
      const cred = await createUserWithEmailAndPassword(auth, email, pass);
      await set(ref(rtdb, "teachers/" + cred.user.uid), profile);
      toast("✅ ចុះឈ្មោះបានជោគជ័យ! 🔥", "success");
      // onAuthStateChanged will handle showClasses()
    } catch (e) {
      loading(false);
      errEl.textContent = "❌ " + e.message;
      errEl.style.display = "block";
    }
    loading(false);
  };

  $("btnLogin").onclick = async () => {
    const email = $("loginEmail").value.trim(), pass = $("loginPass").value;
    if (!email || !pass) {
      toast("⚠️ សូមបំពេញ Email និង Password!", "error");
      return;
    }
    loading(true);
    try {
      await signInWithEmailAndPassword(auth, email, pass);
    } catch (e) {
      toast("❌ " + e.message, "error");
    }
    loading(false);
  };

  window.handleLogout = async function () {
    await signOut(auth);
    teacher = null; selClass = null;
    clearInterval(pollId);
    toast("👋 ចាកចេញ", "info");
    showLogin();
  };

  onAuthStateChanged(auth, async (user) => {
    if (user) {
      loading(true);
      try {
        const data = await dbGet("teachers/" + user.uid);
        teacher = { uid: user.uid, ...(data || { email: user.email }) };
        showClasses();
      } catch (e) {
        teacher = { uid: user.uid, email: user.email, fullName: "", title: "", school: "", level: "" };
        showClasses();
      }
      loading(false);
    } else { showLogin(); }
  });

  function showClasses() {
    $("authWrap").style.display = "flex";
    $("dash").style.display = "none";
    $("viewLogin").style.display = "none";
    $("viewClasses").style.display = "block";
    const nm = teacher.fullName || teacher.email || "";
    const ttl = teacher.title || "";
    $("tchAvatar").textContent = ttl === "លោកស្រី" || ttl === "អ្នកគ្រូ" ? "👩‍🏫" : "👨‍🏫";
    $("tchNameDisplay").textContent = ttl + " " + nm;
    $("tchDetailDisplay").textContent = (teacher.level || "") + " · " + (teacher.school || "");
    $("tchEmailDisplay").textContent = "📧 " + (teacher.email || "");
    const grid = $("classGrid");
    grid.innerHTML = "";
    CLASSES.forEach((cls) => {
      const btn = document.createElement("button");
      btn.className = "cBtn" + (["3A","3B"].includes(cls) ? " hot" : "");
      btn.innerHTML = `<span class="cls-name">${cls}</span>${["3A","3B"].includes(cls) ? '<span class="cls-hot">🔥</span>' : ""}`;
      btn.onclick = () => openClass(cls);
      grid.appendChild(btn);
    });
  }

  async function openClass(cls) {
    selClass = cls;
    semester = "s1";
    selMonth = 3;
    innerTab = "info";
    editMode = false;
    detailAllMonthsData = {};
    $("authWrap").style.display = "none";
    $("dash").style.display = "block";
    await window.loadAll();
    buildSemBar();
    buildItBar();
    updateCounts();
    updateFooter();
    clearInterval(pollId);
    pollId = setInterval(() => {
      if (!editMode) window.loadAll();
    }, 15000);
    toast(`📂 ថ្នាក់ ${cls} 🔥`, "info");
  }

  window.goToClasses = function () {
    clearInterval(pollId); editMode = false;
    $("authWrap").style.display = "flex";
    $("dash").style.display = "none";
    showClasses();
  };

  window.loadAll = async function () {
    if (!selClass) return;
    loading(true);
    try {
      const [stu, sco, att] = await Promise.all([
        dbGet(`plp2026/${selClass}/students`),
        dbGet(`plp2026/${selClass}/scores/${semester}/${selMonth}`),
        semester !== "annual" ? dbGet(`plp2026/${selClass}/attendance/${semester}/${selMonth}`) : Promise.resolve(null),
      ]);
      students = stu || {};
      localStu = JSON.parse(JSON.stringify(stu || {}));
      scores = sco || {};
      localSco = JSON.parse(JSON.stringify(sco || {}));
      attendance = att || {};
      localAtt = JSON.parse(JSON.stringify(att || {}));
      $("fbBadgeDash").textContent = "🔥 ✅ Firebase";
    } catch (e) {
      $("fbBadgeDash").textContent = "🔥 ❌ Error";
      toast("❌ Firebase: " + e.message, "error");
    }
    loading(false);
    updateCounts(); renderContent(); updateFooter(); buildMonBar();
  };

  window.handleSave = async function () {
    loading(true);
    try {
      await Promise.all([
        dbSet(`plp2026/${selClass}/students`, localStu),
        semester !== "annual" ? dbSet(`plp2026/${selClass}/scores/${semester}/${selMonth}`, localSco) : Promise.resolve(),
        semester !== "annual" ? dbSet(`plp2026/${selClass}/attendance/${semester}/${selMonth}`, localAtt) : Promise.resolve(),
      ]);
      students = JSON.parse(JSON.stringify(localStu));
      scores = JSON.parse(JSON.stringify(localSco));
      attendance = JSON.parse(JSON.stringify(localAtt));
      editMode = false; updateEditUI();
      toast("💾 Firebase Saved! 🔥", "success");
    } catch (e) {
      toast("❌ Save Error: " + e.message, "error");
    }
    loading(false);
    renderContent();
  };

  window.handleAdd = async function () {
    if (!newStu.lastName || !newStu.firstName) { toast("⚠️ បំពេញ គោត្តនាម + នាម!", "error"); return; }
    loading(true);
    try {
      const id = await dbPush(`plp2026/${selClass}/students`, newStu);
      localStu[id] = { ...newStu }; students[id] = { ...newStu };
      toast("✅ បន្ថែមសិស្ស 🔥");
    } catch (e) { toast("❌ " + e.message, "error"); }
    newStu = { ...BLANK }; window.closeAddModal(); loading(false);
    updateCounts(); renderContent();
  };

  async function handleDel(sid) {
    if (!confirm("តើអ្នកពិតជាចង់លុបសិស្សនេះ?")) return;
    loading(true);
    try {
      await dbDel(`plp2026/${selClass}/students/${sid}`);
      delete localStu[sid]; delete students[sid];
      toast("🗑️ លុបហើយ", "info");
    } catch (e) { toast("❌ " + e.message, "error"); }
    loading(false); updateCounts(); renderContent();
  }

  function updateCounts() {
    const sl = stuList();
    $("cntTotal").textContent = sl.length;
    $("cntMale").textContent = sl.filter((s) => s.gender === "ប្រុស").length;
    $("cntFemale").textContent = sl.filter((s) => s.gender === "ស្រី").length;
    const tName = `${teacher?.title || ""} ${teacher?.fullName || teacher?.email || ""}`.trim();
    $("dashTitle").textContent = `PLP ២០២៦ · ថ្នាក់ ${selClass}`;
    $("dashSub").textContent = `${tName} · ${teacher?.school || ""}`;
    $("tchBarAvatar").textContent = teacher?.title === "លោកស្រី" || teacher?.title === "អ្នកគ្រូ" ? "👩‍🏫" : "👨‍🏫";
    $("tchBarName").textContent = tName;
    $("tchBarDetail").textContent = (teacher?.level || "") + " · " + (teacher?.position || "គ្រូប្រចាំថ្នាក់");
    $("tchBarSchool").textContent = "🏫 " + (teacher?.school || "");
    $("monthBadge").textContent = `📅 ${MONTHS[selMonth]}`;
    $("footTch").textContent = tName;
  }

  function updateFooter() {
    const cs = curSem();
    $("footLabel").textContent = `ថ្នាក់ ${selClass} · ${cs.label}${semester !== "annual" ? ` · ${MONTHS[selMonth]}` : ""}`;
    $("footStatus").textContent = editMode ? "⚠️ មិនទាន់ Save" : "✅ Synced";
    $("footStatus").style.color = editMode ? "#f59e0b" : "#22c55e";
  }

  window.startEdit = function () {
    editMode = true; updateEditUI(); renderContent(); toast("✏️ ម៉ូតកែសម្រួល", "info");
  };

  window.cancelEdit = function () {
    localStu = JSON.parse(JSON.stringify(students));
    localSco = JSON.parse(JSON.stringify(scores));
    localAtt = JSON.parse(JSON.stringify(attendance));
    editMode = false; updateEditUI(); renderContent();
    toast("❌ បោះបង់", "info");
  };

  function updateEditUI() {
    $("editBanner").style.display = editMode ? "block" : "none";
    $("editBtns").innerHTML = editMode
      ? `<button class="btn-save" onclick="window.handleSave()">💾 Save 🔥</button><button class="btn-cancel-sm" onclick="window.cancelEdit()">✕</button>`
      : `<button class="btn-edit" onclick="window.startEdit()">✏️ កែ</button>`;
    $("btnAddStu").style.display = innerTab === "info" ? "" : "none";
    updateFooter();
  }

  function buildSemBar() {
    const bar = $("semBar"); bar.innerHTML = "";
    SEMESTERS.forEach((sm) => {
      const btn = document.createElement("button");
      btn.className = "semBtn" + (semester === sm.id ? " active" : "");
      btn.textContent = sm.label + (semester === sm.id ? " ✓" : "");
      if (semester === sm.id) { btn.style.borderColor = sm.color; btn.style.color = sm.color; }
      btn.onclick = async () => {
        semester = sm.id;
        selMonth = sm.id === "s1" ? 3 : sm.id === "s2" ? 6 : 0;
        await window.loadAll(); buildSemBar(); buildMonBar();
        toast(`📚 ${sm.label}`, "info");
      };
      bar.appendChild(btn);
    });
  }

  function buildMonBar() {
    const cs = curSem();
    $("monBarWrap").style.display = semester !== "annual" ? "flex" : "none";
    const scroll = $("monScroll"); scroll.innerHTML = "";
    const months = semester === "annual" ? MONTHS.map((_, i) => i) : cs.months;
    months.forEach((i) => {
      const btn = document.createElement("button");
      btn.className = "monBtn" + (selMonth === i ? " active" : "");
      btn.textContent = MONTHS[i] + (selMonth === i ? " ✅" : "");
      btn.onclick = async () => { selMonth = i; await window.loadAll(); buildMonBar(); toast(`📅 ${MONTHS[i]}`, "info"); };
      scroll.appendChild(btn);
    });
  }

  function buildItBar() {
    const bar = $("itBar"); bar.innerHTML = "";
    INNER_TABS.forEach((t) => {
      const btn = document.createElement("button");
      btn.className = "iTab" + (innerTab === t.id ? " active" : "");
      btn.textContent = `${t.icon} ${t.label}`;
      btn.onclick = () => { if (innerTab === "detail" && t.id !== "detail") detailAllMonthsData = {}; innerTab = t.id; buildItBar(); renderContent(); updateEditUI(); };
      bar.appendChild(btn);
    });
  }

  window.showAddModal = function () {
    window.newStu = {};
    const grid = document.getElementById("addModalGrid");
    grid.innerHTML = "";
    const fields = [
      ["គោត្តនាម","lastName"],["នាម","firstName"],["ភេទ","gender"],["ថ្ងៃខែឆ្នាំកំណើត","dob"],
      ["អាយុ","age"],["ឈ្មោះឪពុក","fatherName"],["ឈ្មោះម្តាយ","motherName"],
      ["ភូមិ","village"],["ឃុំ","commune"],["ស្រុក","district"],["ខេត្ត","province"],["ទូរស័ព្ទ","phone"],
    ];
    fields.forEach(([lb, k]) => {
      const d = document.createElement("div");
      d.style.cssText = "display:flex;flex-direction:column;gap:3px";
      const lbl = document.createElement("label");
      lbl.className = "lbl"; lbl.textContent = lb;
      let inp;
      if (k === "dob") {
        inp = document.createElement("input"); inp.type = "date"; inp.id = "dobInput";
        inp.style.cssText = "padding:6px 10px;border:1.5px solid #e5e7eb;border-radius:7px;font-size:13px;color:#1e3a5f;outline:none;font-family:inherit";
        inp.oninput = (e) => { newStu[k] = e.target.value; };
      } else if (k === "gender") {
        const sel = document.createElement("select");
        sel.style.cssText = "padding:6px 10px;border:1.5px solid #e5e7eb;border-radius:7px;font-size:13px;color:#1e3a5f;outline:none;font-family:inherit";
        ["ប្រុស","ស្រី"].forEach((g) => { const o = document.createElement("option"); o.value = g; o.textContent = g; sel.appendChild(o); });
        sel.onchange = (e) => (newStu.gender = e.target.value);
        d.appendChild(lbl); d.appendChild(sel); grid.appendChild(d); return;
      } else {
        inp = document.createElement("input"); inp.type = "text";
        inp.style.cssText = "padding:6px 10px;border:1.5px solid #e5e7eb;border-radius:7px;font-size:13px;color:#1e3a5f;outline:none;font-family:inherit";
        inp.oninput = (e) => (newStu[k] = e.target.value);
      }
      d.appendChild(lbl); d.appendChild(inp); grid.appendChild(d);
    });
    document.getElementById("addModal").style.display = "flex";
  };

  window.closeAddModal = function () { $("addModal").style.display = "none"; };

  // ════ STATISTICS 2 COLUMNS ════
  function buildStatsHtmlNew(sl) {
  const total_s = sl.length;
  const male_s = sl.filter((s) => s.gender === "ប្រុស").length;
  const female_s = sl.filter((s) => s.gender === "ស្រី").length;
  const passArr = sl.filter((s) => Number(getAvg(s.id)) >= 5);
  const failArr = sl.filter((s) => Number(getAvg(s.id)) < 5);

  const passC = passArr.length;
  const failC = failArr.length;
  const passFemale = passArr.filter((s) => s.gender === "ស្រី").length;
  const failFemale = failArr.filter((s) => s.gender === "ស្រី").length;

  const grades = ["A", "B", "C", "D", "E", "F"];
  const gradeCounts = grades.map((g) => {
    const arr = sl.filter((s) => gradeOf(Number(getAvg(s.id))).l === g);
    const femaleCount = arr.filter((s) => s.gender === "ស្រី").length;
    return {
      g,
      total: arr.length,
      female: femaleCount,
      pct: total_s > 0 ? ((arr.length / total_s) * 100).toFixed(0) : 0,
      femalePct: female_s > 0 ? ((femaleCount / female_s) * 100).toFixed(0) : 0,
    };
  });
  const pct = (n, t) => (t ? ((n / t) * 100).toFixed(0) : 0);

    let html = `<div style="border:1px solid #cbd5e1;border-radius:10px;padding:12px;margin:12px 0;background:#f8fafc">
    <div style="display:grid;grid-template-columns:1fr 1fr;gap:16px;font-size:12px;line-height:1.8;color:#1e293b">
      <div>
        <div style="font-weight:800;color:#1e3a5f;margin-bottom:8px;font-size:12px">👥 សិស្សទាំងអស់</div>
        <div style="margin-bottom:4px">
          -សរុប <strong>${total_s}</strong>នាក់ ប្រុស <strong>${male_s}</strong>នាក់ (${pct(male_s, total_s)}%) ស្រី <strong>${female_s}</strong>នាក់ (${pct(female_s, total_s)}%)
        </div>
        <div style="margin-top:12px;font-weight:800;color:#1e3a5f;font-size:12px">📊 ចំណាត់ថ្នាក់ដោយនិទ្ទេស</div>`;
  gradeCounts.forEach((gc) => {
    const gradeColor = {
      A: "#15803d",
      B: "#1d4ed8",
      C: "#b45309",
      D: "#c2410c",
      E: "#dc2626",
      F: "#7f1d1d",
    }[gc.g];
    html += `-សិស្សនិទ្ទេស <strong style="color:${gradeColor}">${gc.g}</strong> សរុប <strong>${gc.total}</strong>នាក់ (${gc.pct}%) ស្រី <strong>${gc.female}</strong>នាក់ (${gc.femalePct}%)<br/>`;
  });
  html += `</div>
      
      <div>
        <div style="font-weight:800;color:#1e3a5f;margin-bottom:8px;font-size:12px">✅ លទ្ធផលការប្រឡង</div>
        <div style="margin-bottom:4px">
          -ជាប់ <strong style="color:#16a34a">${passC}</strong>នាក់ (${pct(passC, total_s)}%) ស្រី <strong>${passFemale}</strong>នាក់ (${passC > 0 ? ((passFemale / passC) * 100).toFixed(0) : 0}%) 
        </div>
        <div style="margin-bottom:12px">
          -ធ្លាក់ <strong style="color:#dc2626">${failC}</strong>នាក់ (${pct(failC, total_s)}%) ស្រី <strong>${failFemale}</strong>នាក់ (${failC > 0 ? ((failFemale / failC) * 100).toFixed(0) : 0}%) 
        </div>

        <div style="margin-top:12px;font-weight:800;color:#1e3a5f;font-size:12px">📈 អត្រាប្រឡង</div>
        <div>-អត្រាជាប់ ${pct(passC, total_s)}%</div>
        <div>-អត្រាធ្លាក់ ${pct(failC, total_s)}%</div>
      </div>
    </div>
  </div>`;
  return html;
}


  function getThreeWorkingDates() {
    // MONTHS array: ["ធ្នូ","មករា","កុម្ភៈ","មីនា","មេសា","ឧសភា","មិថុនា","កក្កដា","សីហា","កញ្ញា","តុលា","វិច្ឆិកា"]
    // index:            0      1      2       3      4       5       6        7       8      9      10      11
    // Map to JS Date month (0=Jan ... 11=Dec):
    const MONTH_MAP = [11, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
    const calMonth = MONTH_MAP[selMonth];
    const today = new Date();
    // Academic year 2026: ធ្នូ(Dec) belongs to 2025, others to 2026
    let year = today.getFullYear();
    if (selMonth === 0) {
      // ធ្នូ = December — use previous calendar year if we're past Jan
      year = today.getMonth() >= 1 ? year - 1 : year;
    }
    let d0 = new Date(year, calMonth, 23);
    while (d0.getDay() === 0 || d0.getDay() === 6) { d0.setDate(d0.getDate() + 1); }
    const d1 = addWD(d0, 1);
    const d2 = addWD(d0, 2);
    return { d0: fmtKhDate(d0), d1: fmtKhDate(d1), d2: fmtKhDate(d2) };
  }

  function getOffDaysBetween(dateFrom, dateTo) {
    const offDays = [];
    let current = new Date(dateFrom);
    current.setDate(current.getDate() + 1);
    while (current < dateTo) {
      const day = current.getDay();
      if (day === 0 || day === 6) { offDays.push(`${KH_WEEKDAYS[day]} ${toKhNum(current.getDate())}`); }
      current.setDate(current.getDate() + 1);
    }
    return offDays;
  }

  function buildSignatureHtml(tName, sigType = "monthly") {
    const dates = getThreeWorkingDates();
    const offDays1 = getOffDaysBetween(dates.d0, dates.d1);
    const offDays2 = getOffDaysBetween(dates.d1, dates.d2);
    let sigHtml = `<div class="sig-section" style="margin-top:20px">`;
    sigHtml += `
      <div class="sig-col">
        <div style="font-size:12px;font-weight:600;color:#1e3a5f">បានឃើញ និងឯកភាព</div>
        <div class="sig-date-line">${dates.d2.lunar}</div>
        <div class="sig-date-line">ស្ពានស្រែង ${dates.d2.solar}</div>
        <div class="sig-role">នាយកកម្រង</div>
      </div>
      ${offDays1.length > 0 ? `<div style="text-align:center;padding:0 8px;color:#ea580c;font-size:12px;font-weight:600">ឈប់: ${offDays1.join(', ')}</div>` : ''}
      <div class="sig-col">
        <div style="font-size:12px;font-weight:600;color:#1e3a5f">បានឃើញ និងពិនិត្យ</div>
        <div class="sig-date-line">${dates.d1.lunar}</div>
        <div class="sig-date-line">រោគ ${dates.d1.solar}</div>
        <div class="sig-role">នាយក/នាយិកា</div>
      </div>
      ${offDays2.length > 0 ? `<div style="text-align:center;padding:0 8px;color:#ea580c;font-size:12px;font-weight:600">ឈប់: ${offDays2.join(', ')}</div>` : ''}
      <div class="sig-col">
        <div class="sig-date-line">${dates.d0.lunar}</div>
        <div class="sig-date-line">រោគ ${dates.d0.solar}</div>
        <div class="sig-role">គ្រូប្រចាំថ្នាក់</div>
        <div class="sig-name">${tName}</div>
      </div>`;
    sigHtml += `</div>`;
    return sigHtml;
  }

  function buildDetailTable(ranked, semesterId) {
    const cs = SEMESTERS.find(s => s.id === semesterId);
    if (!cs) return "";
    const sorted = buildRankedList(ranked);
    const months = cs.months;
    const monthLabels = months.map(m => MONTHS[m]);
    let html = `<table class="rank-table"><thead><tr>
      <th style="width:22px">ល.រ</th>
      <th style="min-width:100px;text-align:left">គោត្តនាម-នាម</th>
      <th style="width:20px">ភេទ</th>
      <th style="min-width:100px;text-align:left">ថ្ងៃខែឆ្នាំកំណើត</th>`;
    monthLabels.forEach(ml => { html += `<th style="width:38px;font-size:10px">ខែ${ml}</th>`; });
    html += `
      <th style="width:44px">ម.ប្រចាំខែ</th>
      <th style="width:44px">ម.ប្រចាំឆមាស</th>
      <th style="width:28px">ចំ.ថ្នាក់</th>
      <th style="width:26px">និទ្ទេស</th>
    </tr></thead><tbody>`;
    sorted.forEach((s, i) => {
      html += `<tr>
        <td style="text-align:center">${i + 1}</td>
        <td class="td-name">${s.lastName} ${s.firstName}</td>
        <td style="text-align:center">${s.gender === "ស្រី" ? "ស្រី" : "ប្រុស"}</td>
        <td style="text-align:center">${s.dob || "—"}</td>`;
      let monthAvgs = [];
      months.forEach(mIdx => {
        const mAvg = getMonthAvgFromAll(s.id, semesterId, mIdx);
        monthAvgs.push(mAvg);
        const disp = mAvg !== null ? fmtAvg(mAvg) : "—";
        const color = mAvg !== null ? (mAvg >= 5 ? "#16a34a" : "#dc2626") : "#d1d5db";
        html += `<td style="text-align:center;font-weight:700;font-size:11px;color:${color}">${disp}</td>`;
      });
      // គណនា col11 = មធ្យម 3 ខែទីមួយ
      const firstThreeMonthsAvgs = monthAvgs.slice(0, 3).filter(v => v !== null);
      const col11 = firstThreeMonthsAvgs.length > 0 ? truncate2(firstThreeMonthsAvgs.reduce((a, b) => a + b, 0) / firstThreeMonthsAvgs.length) : null;
      
      // គណនា col12 = (col11 + ខែទី4) / 2
      let col12 = null;
      if (col11 !== null && monthAvgs.length > 3 && monthAvgs[3] !== null) {
        col12 = truncate2((col11 + monthAvgs[3]) / 2);
      } else if (col11 !== null) {
        col12 = col11;
      }
      
      const g = gradeOf(col12 === null ? 0 : col12);
      html += `
        <td style="text-align:center;font-weight:800;color:#2563eb">${col11 !== null ? fmtAvg(col11) : "—"}</td>
        <td style="text-align:center;font-weight:900;font-size:12px;color:#1e3a5f">${col12 !== null ? fmtAvg(col12) : "—"}</td>
        <td style="text-align:center;font-weight:700">${s._rank}</td>
        <td style="text-align:center"><span class="grade-badge" style="background:${g.c}">${g.l}</span></td>
      </tr>`;
    });
    html += `</tbody></table>`;
    return html;
  }

  function buildSemesterReportTable(ranked) {
    const cs = SEMESTERS.find(s => s.id === semester);
    const months = cs ? cs.months : [];
    const sorted = buildRankedList(ranked);
    const examMonth  = semester === "s1" ? 3 : months[months.length - 1];
    const contMonths = months.filter(m => m !== examMonth);

    let html = `<table class="rank-table"><thead><tr>
      <th style="width:22px">ល.រ</th>
      <th style="min-width:100px;text-align:left">គោត្តនាម-នាម</th>
      <th style="width:20px">ភេទ</th>
      <th style="min-width:100px;text-align:center">ថ្ងៃខែឆ្នាំកំណើត</th>
      <th style="width:42px">ម.ប្រចាំខែ</th>
      <th style="width:42px">ម.ប្រឡង</th>
      <th style="width:42px">ម.ឆមាស</th>
      <th style="width:28px">ចំ.ថ្នាក់</th>
      <th style="width:26px">និទ្ទេស</th>
      <th style="width:32px">លទ្ធផល</th>
    </tr></thead><tbody>`;

    sorted.forEach((s, i) => {
      // គណនា col11 = មធ្យម 3 ខែដំបូង
      const firstThreeMonths = months.slice(0, 3);
      const col11Vals = firstThreeMonths.map(m => getMonthAvgFromAll(s.id, semester, m)).filter(v => v !== null);
      const col11 = col11Vals.length > 0 ? col11Vals.reduce((a,b) => a+b, 0) / col11Vals.length : null;
      
      // ពិន្ទុប្រឡង
      const examAvg = getMonthAvgFromAll(s.id, semester, examMonth);
      
      // គណនា col12 = (col11 + examAvg) / 2
      let col12 = null;
      if (col11 !== null && examAvg !== null) {
        col12 = (col11 + examAvg) / 2;
      } else if (col11 !== null) {
        col12 = col11;
      }
      
      const fmt = v => v !== null ? fmtAvg(truncate2(v)) : "—";
      const g = gradeOf(col12 ?? 0);
      html += `<tr>
        <td style="text-align:center">${i + 1}</td>
        <td class="td-name">${s.lastName} ${s.firstName}</td>
        <td style="text-align:center">${s.gender === "ស្រី" ? "ស្រី" : "ប្រុស"}</td>
        <td style="text-align:center">${s.dob || "—"}</td>
        <td style="text-align:center">${fmt(col11)}</td>
        <td style="text-align:center">${fmt(examAvg)}</td>
        <td style="text-align:center"><strong>${fmt(col12)}</strong></td>
        <td style="text-align:center">${s._rank}</td>
        <td style="text-align:center"><span class="g-${g.l}">${g.l}</span></td>
        <td style="text-align:center" class="${(col12??0) >= 5 ? 'pass' : 'fail'}">${resultOf(col12 ?? 0)}</td>
      </tr>`;
    });
    html += `</tbody></table>`;
    return html;
  }

  function buildAnnualReportTable(ranked) {
    const sorted = buildRankedList(ranked);
    let html = `<table class="rank-table"><thead><tr>
      <th style="width:22px">ល.រ</th>
      <th style="min-width:100px;text-align:left">គោត្តនាម-នាម</th>
      <th style="width:20px">ភេទ</th>
      <th style="min-width:100px;text-align:center">ថ្ងៃខែឆ្នាំកំណើត</th>
      <th style="min-width:150px;text-align:center">អាសយដ្ឋាន</th>
      <th style="width:36px">ឆមាស១</th>
      <th style="width:36px">ឆមាស២</th>
      <th style="width:36px">ម.ប្រចាំឆ្នាំ</th>
      <th style="width:28px">ចំ.ថ្នាក់</th>
      <th style="width:26px">និទ្ទេស</th>
      <th style="width:32px">លទ្ធផល</th>
    </tr></thead><tbody>`;
    sorted.forEach((s, i) => {
      const s1 = getSemAvgFromAll(s.id, 's1');
      const s2 = getSemAvgFromAll(s.id, 's2');
      const bothVals = [s1, s2].filter(v => v !== null);
      const annual = bothVals.length > 0 ? bothVals.reduce((a, b) => a + b, 0) / bothVals.length : null;
      const fmt = v => v !== null ? fmtAvg(truncate2(v)) : "—";
      const g = gradeOf(annual !== null ? annual : 0);
      const addr = `${s.village || ""} ${s.commune || ""} ${s.district || ""}`.trim();
      html += `<tr>
        <td style="text-align:center">${i + 1}</td>
        <td class="td-name">${s.lastName} ${s.firstName}</td>
        <td style="text-align:center">${s.gender === "ស្រី" ? "ស្រី" : "ប្រុស"}</td>
        <td style="text-align:center;font-size:12px">${s.dob || "—"}</td>
        <td style="text-align:left;font-size:12px">${addr || "—"}</td>
        <td style="text-align:center"><strong>${fmt(s1)}</strong></td>
        <td style="text-align:center"><strong>${fmt(s2)}</strong></td>
        <td style="text-align:center"><strong style="font-size:12px;color:#1e3a5f">${fmt(annual)}</strong></td>
        <td style="text-align:center">${s._rank}</td>
        <td style="text-align:center"><span class="g-${g.l}">${g.l}</span></td>
        <td style="text-align:center" class="${(annual||0) >= 5 ? 'pass' : 'fail'}">${resultOf(annual || 0)}</td>
      </tr>`;
    });
    html += `</tbody></table>`;
    return html;
  }

  function buildAttendanceTable(sl) {
    let html = `<table class="rank-table"><thead><tr><th style="width:22px">ល.រ</th><th style="min-width:100px;text-align:left">ឈ្មោះ</th>`;
    for (let d = 1; d <= 31; d++) { html += `<th style="width:18px;font-size:9px">${d}</th>`; }
    html += `<th style="width:28px">ច្បាប់</th><th style="width:28px">អត់</th></tr></thead><tbody>`;
    sl.forEach((s, i) => {
      const p = cntAtt(s.id, 'P');
      const a = cntAtt(s.id, 'A');
      html += `<tr><td style="text-align:center">${i+1}</td><td class="td-name">${s.lastName} ${s.firstName}</td>`;
      for (let d = 1; d <= 31; d++) {
        const val = getAtt(s.id, d);
        const bgColor = val === 'P' ? '#dcfce7' : val === 'A' ? '#fee2e2' : 'transparent';
        const txtColor = val === 'P' ? '#16a34a' : val === 'A' ? '#dc2626' : '#d1d5db';
        html += `<td style="text-align:center;background:${bgColor};color:${txtColor};font-weight:700;font-size:12px">${val || '·'}</td>`;
      }
      html += `<td style="text-align:center;color:#16a34a;font-weight:700">${p}</td><td style="text-align:center;color:#dc2626;font-weight:700">${a}</td></tr>`;
    });
    html += `</tbody></table>`;
    return html;
  }

  function renderContent() {
    const cont = $("content"); cont.innerHTML = "";
    const sl = stuList();

    if (innerTab === "info") {
      $("btnAddStu").style.display = "";
      if (!sl.length) { cont.appendChild(emptyEl("👤","មិនទាន់មានសិស្ស — ចុច ➕ ដើម្បីបន្ថែម")); return; }
      const wrap = document.createElement("div"); wrap.className = "tWrap";
      const tbl = makeTbl(["ល.រ","គោត្តនាម","នាម","ភេទ","ថ្ងៃខែឆ្នាំកំណើត","អាយុ","ឈ្មោះឪពុក","ឈ្មោះម្តាយ","ភូមិ","ឃុំ","ស្រុក","ខេត្ត","ទូរស័ព្ទ","✕"]);
      const tbody = tbl.querySelector("tbody");
      sl.forEach((s, i) => {
        const tr = document.createElement("tr");
        const cells = [
          tdC(i + 1),
          editMode ? tdInput(localStu[s.id]?.lastName||"",(v)=>{ if(localStu[s.id]) localStu[s.id].lastName=v; }) : td(s.lastName),
          editMode ? tdInput(localStu[s.id]?.firstName||"",(v)=>{ if(localStu[s.id]) localStu[s.id].firstName=v; }) : td(s.firstName),
          tdGender(s.gender),
          td(s.dob),
          td(s.age || "—"),
          ...["fatherName","motherName","village","commune","district","province","phone"].map((k) => td(s[k]||"—")),
          tdDel(s.id),
        ];
        cells.forEach((c) => tr.appendChild(c));
        tbody.appendChild(tr);
      });
      wrap.appendChild(tbl); cont.appendChild(wrap);
    } else if (innerTab === "scores") {
      $("btnAddStu").style.display = "none";
      if (!sl.length) { cont.appendChild(emptyEl("📝","មិនទាន់មានសិស្ស")); return; }
      const wrap = document.createElement("div"); wrap.className = "tWrap";
      const tbl = makeTbl(["គោត្តនាម-នាម", "ភេទ", ...SUBJECTS, "ពិន្ទុសរុប","មធ្យមភាគ","ចំណាត់ថ្នាក់","លទ្ធផល","និទ្ទេស"],[],true);
      const tbody = tbl.querySelector("tbody");
      sl.forEach((s, i) => {
        const avg = getAvg(s.id), g = gradeOf(avg), tr = trOf(i,[]);
        const ntd = document.createElement("td");
        ntd.className = "sticky-col";
        ntd.appendChild(nameCell(s));
        tr.appendChild(ntd);  tr.appendChild(tdC(s.gender==="ស្រី"?"👩":"👨"));
        SUBJECTS.forEach((subj) => {
          const cell = document.createElement("td"); cell.className = "center";
          if (editMode) {
            const inp = document.createElement("input"); inp.type="number"; inp.min=0; inp.max=10; inp.className="sipt";
            inp.value = getSco(s.id,subj)||""; inp.placeholder="—";
            inp.oninput = (e) => { const v = Math.min(10,Math.max(0,parseInt(e.target.value)||0)); if (!localSco[s.id]) localSco[s.id] = {}; localSco[s.id][subj] = v; };
            cell.appendChild(inp);
          } else {
            const v = getSco(s.id,subj);
            const sp = document.createElement("span");
            sp.style.cssText = `font-weight:700;font-size:12px;color:${Number(v)>=5?"#16a34a":"#9ca3af"}`;
            sp.textContent = v||"—"; cell.appendChild(sp);
          }
          tr.appendChild(cell);
        });
        tr.appendChild(tdSum(getTotal(s.id))); tr.appendChild(tdSum(fmtAvg(avg))); tr.appendChild(tdSum(getRank(s.id)));
        tr.appendChild(tdC(resultOf(avg),avg>=5?"#16a34a":"#dc2626")); tr.appendChild(tdGrade(g));
        tbody.appendChild(tr);
      });
      wrap.appendChild(tbl); cont.appendChild(wrap);
    } else if (innerTab === "attendance") {
      $("btnAddStu").style.display = "none";
      if (!sl.length) { cont.appendChild(emptyEl("✅","មិនទាន់មានសិស្ស")); return; }
      const wrap = document.createElement("div"); wrap.className = "tWrap";
      const leg = document.createElement("div"); leg.className = "legend";
      leg.innerHTML = `<span style="color:#16a34a;font-weight:700;font-size:12px">✅ P=វត្តមាន</span><span style="color:#dc2626;font-weight:700;font-size:12px">❌ A=អវត្តមាន</span>${editMode?'<span style="color:#6b7280;font-size:11px">· ចុចក្រឡា → រក្សាទុក</span>':""}`;
      wrap.appendChild(leg);
      const days = Array.from({length:31},(_,i)=>i+1);
      const tbl = makeTbl(["ល.រ","គោត្តនាម-នាម","ភេទ",...days.map((d)=>d.toString()),"ច្បាប់","អត់","សរុប"],[],false,true);
      const tbody = tbl.querySelector("tbody");
      sl.forEach((s, i) => {
        const p = cntAtt(s.id,"P"), a = cntAtt(s.id,"A");
        const tr = trOf(i,[]); tr.appendChild(tdC(i+1));
        const ntd = document.createElement("td"); ntd.appendChild(nameCell(s)); tr.appendChild(ntd);
        tr.appendChild(tdC(s.gender==="ស្រី"?"👩":"👨"));
        days.forEach((day) => {
          const val = getAtt(s.id,day);
          const cell = document.createElement("td"); cell.className = "center";
          cell.style.cssText = `padding:2px;background:${val==="P"?"#dcfce7":val==="A"?"#fee2e2":"transparent"};cursor:${editMode?"pointer":"default"}`;
          const sp = document.createElement("span");
          sp.style.cssText = `font-size:10px;font-weight:700;color:${val==="P"?"#16a34a":val==="A"?"#dc2626":"#d1d5db"}`;
          sp.textContent = val||"·"; cell.appendChild(sp);
          if (editMode) cell.onclick = () => { const cur=getAtt(s.id,day); const nxt=cur===""?"P":cur==="P"?"A":""; localAtt[s.id]=localAtt[s.id]||{}; localAtt[s.id][day]=nxt; renderContent(); };
          tr.appendChild(cell);
        });
        tr.appendChild(tdSum(p,"#16a34a")); tr.appendChild(tdSum(a,"#dc2626")); tr.appendChild(tdSum(p+a));
        tbody.appendChild(tr);
      });
      wrap.appendChild(tbl); cont.appendChild(wrap);
    } else if (innerTab === "detail") {
      $("btnAddStu").style.display = "none";
      if (!sl.length) { cont.appendChild(emptyEl("📊", "មិនទាន់មានសិស្ស")); return; }
      const detailBar = document.createElement("div");
      detailBar.className = "semBar no-print";
      detailBar.style.paddingLeft = "14px";
      SEMESTERS.filter(s => s.id !== "annual").forEach((sm) => {
        const btn = document.createElement("button");
        btn.className = "semBtn" + (detailSem === sm.id ? " active" : "");
        btn.textContent = sm.label + (detailSem === sm.id ? " ✓" : "");
        if (detailSem === sm.id) { btn.style.borderColor = sm.color; btn.style.color = sm.color; }
        btn.onclick = async () => { detailSem = sm.id; detailAllMonthsData = {}; renderContent(); };
        detailBar.appendChild(btn);
      });
      cont.appendChild(detailBar);
      const wrap = document.createElement("div");
      wrap.className = "tWrap";
      if (!isMonthsLoaded([detailSem])) {
        const loadMsg = document.createElement("div");
        loadMsg.style.cssText = "text-align:center;padding:32px;color:#6b7280;font-size:14px;font-weight:700";
        loadMsg.textContent = "⏳ កំពុងទាញទិន្នន័យទាំងអស់...";
        wrap.appendChild(loadMsg);
        cont.appendChild(wrap);
        loadMonthsForSemesters([detailSem]).then(() => renderContent());
        return;
      }
      const html = buildDetailTable(sl, detailSem);
      wrap.innerHTML = html;
      cont.appendChild(wrap);
    } else if (innerTab === "report") {
      $("btnAddStu").style.display = "none";
      const pd = document.createElement("div"); pd.style.padding = "0";
      const bar = document.createElement("div"); bar.className = "rTypeBar no-print";
      [["monthly","📅 ប្រចាំខែ"],["semester","📚 ឆមាស"],["detail","📊 លម្អិត"],["annual","🏆 ដំណាច់ឆ្នាំ"],["attendance","✅ វត្តមាន"]].forEach(([id,lb]) => {
        const btn = document.createElement("button");
        btn.className = "rTypeBtn"+(reportType===id?" active":"");
        btn.textContent = lb;
        btn.onclick = () => { reportType = id; detailAllMonthsData = {}; renderContent(); };
        bar.appendChild(btn);
      });
      const printBtn = document.createElement("button");
      printBtn.style.cssText = "background:linear-gradient(135deg,#22c55e,#16a34a);color:#fff;border:none;border-radius:50px;padding:7px 14px;cursor:pointer;font-size:12px;font-weight:700;font-family:inherit;margin-left:auto";
      printBtn.textContent = "🖨️ Print PDF";
      printBtn.onclick = () => doPrint();
      bar.appendChild(printBtn);
      pd.appendChild(bar);

      const needsAllMonths = ["semester","detail","annual"].includes(reportType);
      const reportSems = (reportType === "annual" || reportType === "detail") ? ["s1","s2"] : [semester];

      if (needsAllMonths && !isMonthsLoaded(reportSems)) {
        const loadMsg = document.createElement("div");
        loadMsg.style.cssText = "text-align:center;padding:40px;color:#6b7280;font-size:12px;font-weight:700";
        loadMsg.textContent = "⏳ កំពុងទាញទិន្នន័យ...";
        pd.appendChild(loadMsg);
        cont.appendChild(pd);
        loadMonthsForSemesters(reportSems).then(() => renderContent());
        return;
      }

      const note = document.createElement("div"); note.className = "preview-note no-print";
      const tName = `${teacher?.title||""} ${teacher?.fullName||""}`.trim();
      note.innerHTML = `<span>👁️ Preview — ចុច 🖨️ ដើម្បីបោះពុម្ព</span><span style="color:#22c55e;font-weight:700">ឈ្មោះគ្រូ: ${tName}</span>`;
      pd.appendChild(note);
      const prev = document.createElement("div"); prev.id = "previewPanel";
      prev.innerHTML = buildDocHTML();
      pd.appendChild(prev);
      cont.appendChild(pd);
    } else if (innerTab === "honor") {
      $("btnAddStu").style.display = "none";
      renderHonorTab(cont);
    } else if (innerTab === "gradeanalysis") {
      $("btnAddStu").style.display = "none";
      renderGradeAnalysisTab(cont);
    }
  }

  // ════ GRADE ANALYSIS TAB ════
  const GRADE_KEYS = ["A","B","C","D","E","F"];
  const GRADE_COLORS_GA = { A:{bg:"#dcfce7",text:"#166534",bar:"#22c55e"}, B:{bg:"#dbeafe",text:"#1e40af",bar:"#3b82f6"}, C:{bg:"#fef9c3",text:"#854d0e",bar:"#eab308"}, D:{bg:"#ffedd5",text:"#9a3412",bar:"#f97316"}, E:{bg:"#fce7f3",text:"#9d174d",bar:"#ec4899"}, F:{bg:"#fee2e2",text:"#991b1b",bar:"#ef4444"} };

  const SUBJ_GROUPS = {
    all:   { label:"មុខវិជ្ជាទាំងអស់ (មធ្យមភាគ)", indices: [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14] },
    khmer: { label:"ភាសាខ្មែរ (ស្ដាប់·សរសេរ·អាន·និយាយ)", indices: [0,1,2,3] },
    math:  { label:"គណិតវិទ្យា (ចំនួន·រង្វាស់·ធរណី·ពីជ·ស្ថិតិ)", indices: [4,5,6,7,8] },
    sci:   { label:"វិទ្យាសាស្ត្រ + សង្គម", indices: [9,10] },
  };

  function getSubjAvgForGroup(sid, groupKey) {
    const grp = SUBJ_GROUPS[groupKey];
    const vals = grp.indices.map(i => getSco(sid, SUBJECTS[i])).filter(v => v !== "" && v !== undefined);
    if (!vals.length) return null;
    return truncate2(vals.reduce((a,b) => a + Number(b), 0) / vals.length);
  }

  function renderGradeAnalysisTab(cont) {
    const sl = stuList();
    if (!sl.length) { cont.appendChild(emptyEl("🎯","មិនទាន់មានសិស្ស")); return; }
    const bar = document.createElement("div");
    bar.style.cssText = "display:flex;align-items:center;gap:10px;padding:10px 14px;background:#fff;border-bottom:1px solid #e5e7eb;flex-wrap:wrap;";
    bar.innerHTML = `<span style="font-weight:800;color:#1e3a5f;font-size:13px">🎯 វិភាគនិទ្ទេស A–F</span>
      <span style="color:#6b7280;font-size:12px">· ថ្នាក់ ${selClass} · ${SEMESTERS.find(s=>s.id===semester)?.label} · ខែ${MONTHS[selMonth]}</span>
      <div style="margin-left:auto;display:flex;gap:8px;align-items:center;flex-wrap:wrap;">
        <label style="font-size:12px;color:#374151;font-weight:700;">មុខវិជ្ជា:</label>
        <select id="gaSubjSel" style="padding:5px 10px;border:1.5px solid #e5e7eb;border-radius:8px;font-family:inherit;font-size:12px;color:#1e3a5f;" onchange="window._gaRender()">
          <option value="all">មុខវិជ្ជាទាំងអស់</option>
          <option value="khmer">📖 ភាសាខ្មែរ</option>
          <option value="math">🔢 គណិតវិទ្យា</option>
          <option value="sci">🔬 វិទ្យា+សង្គម</option>
        </select>
      </div>`;
    cont.appendChild(bar);
    const body = document.createElement("div");
    body.id = "gaBody";
    body.style.cssText = "padding:14px;";
    cont.appendChild(body);
    window._gaRender = function() {
      const grpKey = document.getElementById("gaSubjSel")?.value || "all";
      _buildGradeAnalysis(sl, grpKey, body);
    };
    window._gaRender();
  }

  function _buildGradeAnalysis(sl, grpKey, container) {
    const grp = SUBJ_GROUPS[grpKey];
    const rows = sl.map(s => {
      const avg = getSubjAvgForGroup(s.id, grpKey);
      const g = avg !== null ? gradeOf(avg) : null;
      return { ...s, avg, grade: g?.l || null };
    });
    const total = rows.filter(r => r.grade).length;
    const counts = {};
    GRADE_KEYS.forEach(g => { counts[g] = { total:0, f:0, m:0 }; });
    rows.forEach(r => {
      if (!r.grade) return;
      counts[r.grade].total++;
      if (r.gender === "ស្រី") counts[r.grade].f++; else counts[r.grade].m++;
    });
    const passCount = GRADE_KEYS.filter(g => g !== "F").reduce((a,g) => a + counts[g].total, 0);
    const failCount = counts["F"].total;
    const passF = GRADE_KEYS.filter(g => g !== "F").reduce((a,g) => a + counts[g].f, 0);

    let html = `<div style="display:grid;grid-template-columns:repeat(4,1fr);gap:10px;margin-bottom:16px;">
      <div style="background:#f0f9ff;border:1px solid #bae6fd;border-radius:10px;padding:12px;text-align:center;">
        <div style="font-size:20px;font-weight:900;color:#0369a1;">${sl.length}</div>
        <div style="font-size:11px;color:#6b7280;margin-top:2px;">សិស្សសរុប</div>
      </div>
      <div style="background:#f0fdf4;border:1px solid #bbf7d0;border-radius:10px;padding:12px;text-align:center;">
        <div style="font-size:20px;font-weight:900;color:#15803d;">${passCount}<span style="font-size:12px;"> (${total>0?((passCount/total)*100).toFixed(0):0}%)</span></div>
        <div style="font-size:11px;color:#6b7280;margin-top:2px;">✅ ជាប់</div>
      </div>
      <div style="background:#fef2f2;border:1px solid #fecaca;border-radius:10px;padding:12px;text-align:center;">
        <div style="font-size:20px;font-weight:900;color:#dc2626;">${failCount}<span style="font-size:12px;"> (${total>0?((failCount/total)*100).toFixed(0):0}%)</span></div>
        <div style="font-size:11px;color:#6b7280;margin-top:2px;">❌ ធ្លាក់ (F)</div>
      </div>
      <div style="background:#faf5ff;border:1px solid #e9d5ff;border-radius:10px;padding:12px;text-align:center;">
        <div style="font-size:13px;font-weight:800;color:#7c3aed;">👩${passF} / 👦${passCount-passF}</div>
        <div style="font-size:11px;color:#6b7280;margin-top:3px;">ស្រី/ប្រុស ជាប់</div>
      </div>
    </div>`;

    html += `<div style="background:#fff;border:1px solid #e5e7eb;border-radius:12px;padding:14px;margin-bottom:16px;">
      <div style="font-weight:800;color:#1e3a5f;font-size:13px;margin-bottom:12px;">📊 ${grp.label}</div>`;
    GRADE_KEYS.forEach(g => {
      const c = counts[g];
      const pct  = total > 0 ? (c.total/total*100) : 0;
      const fpct = total > 0 ? (c.f/total*100)     : 0;
      const mpct = total > 0 ? (c.m/total*100)     : 0;
      const gc = GRADE_COLORS_GA[g];
      html += `<div style="display:flex;align-items:center;gap:8px;margin-bottom:10px;">
        <div style="width:30px;height:30px;border-radius:8px;background:${gc.bg};display:flex;align-items:center;justify-content:center;font-weight:900;font-size:14px;color:${gc.text};flex-shrink:0;">${g}</div>
        <div style="flex:1;">
          <div style="height:14px;background:#f1f5f9;border-radius:99px;overflow:hidden;margin-bottom:3px;">
            <div style="height:100%;width:${pct.toFixed(1)}%;background:${gc.bar};border-radius:99px;transition:width .5s;"></div>
          </div>
          <div style="display:flex;gap:8px;font-size:10px;">
            <span style="color:#ec4899;font-weight:700;">👩${c.f} (${fpct.toFixed(0)}%)</span>
            <span style="color:#3b82f6;font-weight:700;">👦${c.m} (${mpct.toFixed(0)}%)</span>
          </div>
        </div>
        <div style="min-width:80px;text-align:right;font-size:12px;">
          <span style="font-weight:900;color:${gc.text};">${c.total}នាក់</span>
          <span style="color:#9ca3af;font-size:11px;"> (${pct.toFixed(1)}%)</span>
        </div>
      </div>`;
    });
    html += `</div>`;

    html += `<div style="background:#fff;border:1px solid #e5e7eb;border-radius:12px;overflow:hidden;">
      <div style="padding:10px 14px;font-weight:800;color:#1e3a5f;font-size:13px;border-bottom:1px solid #e5e7eb;">📋 បញ្ជីសិស្សតាមនិទ្ទេស</div>
      <div style="overflow-x:auto;"><table style="width:100%;border-collapse:collapse;font-size:12px;">
        <thead><tr style="background:#1e3a5f;color:#fff;">
          <th style="padding:7px 8px;text-align:center;width:30px;">ល.រ</th>
          <th style="padding:7px 8px;text-align:left;min-width:120px;">ឈ្មោះ</th>
          <th style="padding:7px 8px;text-align:center;width:40px;">ភេទ</th>
          <th style="padding:7px 8px;text-align:center;width:65px;">មធ្យមភាគ</th>
          <th style="padding:7px 8px;text-align:center;width:55px;">និទ្ទេស</th>
          <th style="padding:7px 8px;text-align:center;width:55px;">លទ្ធផល</th>
        </tr></thead><tbody>`;

    const gradeOrder = {A:0,B:1,C:2,D:3,E:4,F:5};
    const sorted = [...rows].filter(r=>r.grade).sort((a,b)=>(gradeOrder[a.grade]??9)-(gradeOrder[b.grade]??9)||(b.avg??0)-(a.avg??0));
    let no = 1, lastGrade = null;
    sorted.forEach(r => {
      const gc = GRADE_COLORS_GA[r.grade];
      if (r.grade !== lastGrade) {
        const cnt = counts[r.grade];
        html += `<tr style="background:${gc.bg};"><td colspan="6" style="padding:5px 10px;font-weight:800;font-size:11px;color:${gc.text};">
          🏷️ និទ្ទេស ${r.grade} — ${cnt.total}នាក់ · 👩${cnt.f} 👦${cnt.m}
        </td></tr>`;
        lastGrade = r.grade;
      }
      const rowBg = no%2===0?"#f8fafc":"#fff";
      html += `<tr style="background:${rowBg};">
        <td style="padding:5px 8px;text-align:center;color:#9ca3af;">${no++}</td>
        <td style="padding:5px 8px;font-weight:600;color:#1e3a5f;">${r.lastName} ${r.firstName}</td>
        <td style="padding:5px 8px;text-align:center;">${r.gender==="ស្រី"?"👩":"👦"}</td>
        <td style="padding:5px 8px;text-align:center;font-weight:800;color:${gc.text};">${r.avg!==null?fmtAvg(r.avg):"—"}</td>
        <td style="padding:5px 8px;text-align:center;"><span style="background:${gc.bg};color:${gc.text};border-radius:20px;padding:2px 10px;font-weight:900;font-size:11px;">${r.grade}</span></td>
        <td style="padding:5px 8px;text-align:center;font-weight:700;color:${r.grade!=="F"?"#15803d":"#dc2626"};">${r.grade!=="F"?"ជាប់":"ធ្លាក់"}</td>
      </tr>`;
    });
    html += `</tbody></table></div></div>`;
    container.innerHTML = html;
  }

  // ════ HONOR ROLL ════
  const GRADE_COLOR = { A:"#15803d", B:"#1d4ed8", C:"#b45309", D:"#c2410c", E:"#dc2626", F:"#7f1d1d" };
  const MEDAL = ["🥇","🥈","🥉","④","⑤"];

  function getHonorTop(n) {
    const sl = stuList();
    return buildRankedList(sl).slice(0, n);
  }

  function renderHonorTab(cont) {
    const sl = stuList();
    if (!sl.length) { cont.appendChild(emptyEl("🏆","មិនទាន់មានសិស្ស")); return; }
    const ranked = buildRankedList(sl);

    const bar = document.createElement("div");
    bar.style.cssText = "display:flex;align-items:center;gap:10px;padding:10px 14px;background:#fff;border-bottom:1px solid #e5e7eb;flex-wrap:wrap;";
    bar.innerHTML = `<span style="font-weight:800;color:#1e3a5f;font-size:13px">🏆 តារាងកិត្តិយស</span>
      <span style="color:#6b7280;font-size:12px">· ថ្នាក់ ${selClass} · ${curSem().label}</span>
      <div style="margin-left:auto;display:flex;gap:8px;flex-wrap:wrap;">
        <button onclick="window.doPrintHonorAll()" style="background:linear-gradient(135deg,#2563eb,#1d4ed8);color:#fff;border:none;border-radius:50px;padding:7px 16px;cursor:pointer;font-size:12px;font-weight:700;font-family:inherit">🖨️ ព្រីន តារាងទាំងអស់</button>
        <button onclick="window.doPrintHonor()" style="background:linear-gradient(135deg,#f59e0b,#d97706);color:#fff;border:none;border-radius:50px;padding:7px 16px;cursor:pointer;font-size:12px;font-weight:700;font-family:inherit">🥇 ព្រីន Rank 1–5</button>
      </div>`;
    cont.appendChild(bar);

    const grid = document.createElement("div");
    grid.style.cssText = "display:grid;grid-template-columns:repeat(auto-fill,minmax(130px,1fr));gap:12px;padding:14px;";

    ranked.forEach((s) => {
      const avg = Number(getAvg(s.id));
      const g = gradeOf(avg);
      const photo = honorPhotos[s.id] || null;
      const medal = s._rank <= 5 ? MEDAL[s._rank-1] : "";
      const borderCol = s._rank===1?"#f59e0b":s._rank===2?"#94a3b8":s._rank===3?"#b45309":"#e5e7eb";

      const card = document.createElement("div");
      card.style.cssText = `background:#fff;border-radius:14px;border:2px solid ${borderCol};padding:10px 8px;text-align:center;position:relative;box-shadow:${s._rank<=3?"0 4px 12px rgba(245,158,11,0.18)":"0 2px 6px rgba(0,0,0,0.06)"};`;

      if (medal) {
        const rb = document.createElement("div");
        rb.style.cssText = "position:absolute;top:-10px;right:-6px;font-size:20px;line-height:1;";
        rb.textContent = medal;
        card.appendChild(rb);
      }
      const rn = document.createElement("div");
      rn.style.cssText = "position:absolute;top:6px;left:8px;font-size:10px;font-weight:800;color:#94a3b8;";
      rn.textContent = "#" + s._rank;
      card.appendChild(rn);

      const photoWrap = document.createElement("div");
      photoWrap.style.cssText = "width:72px;height:72px;border-radius:50%;margin:8px auto 6px;overflow:hidden;border:3px solid "+borderCol+";background:#f1f5f9;display:flex;align-items:center;justify-content:center;cursor:pointer;position:relative;";

      const img = document.createElement("img");
      img.style.cssText = "width:100%;height:100%;object-fit:cover;display:"+(photo?"block":"none")+";";
      if (photo) img.src = photo;

      const placeholder = document.createElement("div");
      placeholder.style.cssText = "font-size:28px;display:"+(photo?"none":"flex")+";align-items:center;justify-content:center;width:100%;height:100%;";
      placeholder.textContent = s.gender === "ស្រី" ? "👩" : "👨";

      const fileIn = document.createElement("input");
      fileIn.type = "file"; fileIn.accept = "image/*"; fileIn.style.display = "none";
      const sid = s.id;
      fileIn.onchange = (e) => {
        const file = e.target.files[0]; if (!file) return;
        const reader = new FileReader();
        reader.onload = (ev) => { honorPhotos[sid] = ev.target.result; renderContent(); };
        reader.readAsDataURL(file);
      };

      const hint = document.createElement("div");
      hint.style.cssText = "position:absolute;bottom:0;left:0;right:0;background:rgba(0,0,0,0.45);color:#fff;font-size:9px;padding:2px 0;border-radius:0 0 50px 50px;text-align:center;";
      hint.textContent = "📷";

      photoWrap.appendChild(img); photoWrap.appendChild(placeholder);
      photoWrap.appendChild(hint); photoWrap.appendChild(fileIn);
      photoWrap.onclick = () => fileIn.click();
      card.appendChild(photoWrap);

      const nm = document.createElement("div");
      nm.style.cssText = "font-weight:800;font-size:11px;color:#1e3a5f;line-height:1.3;margin-bottom:4px;";
      nm.textContent = s.lastName+" "+s.firstName;
      card.appendChild(nm);

      const av = document.createElement("div");
      av.style.cssText = "font-size:13px;font-weight:900;color:"+GRADE_COLOR[g.l]+";margin-bottom:3px;";
      av.textContent = fmtAvg(avg);
      card.appendChild(av);

      const gb = document.createElement("div");
      gb.style.cssText = "display:inline-block;background:"+g.c+";color:#fff;border-radius:20px;padding:2px 10px;font-size:10px;font-weight:800;";
      gb.textContent = "និទ្ទេស "+g.l;
      card.appendChild(gb);

      grid.appendChild(card);
    });
    cont.appendChild(grid);
  }

  function buildHonorPrintHTML() {
  const top5 = getHonorTop(5);
  const tName = (teacher?.title || "") + " " + (teacher?.fullName || teacher?.email || "");
  const school = teacher?.school || "សាលាបឋមសិក្សា";
  const dates = getThreeWorkingDates();
  const RANK_BORDER = ["#f59e0b", "#94a3b8", "#b45309", "#6b7280", "#6b7280"];
  const RANK_BG = ["#fffbeb", "#f8fafc", "#fff7ed", "#fff", "#fff"];
  const GRADE_C = { A: "#15803d", B: "#1d4ed8", C: "#b45309", D: "#c2410c", E: "#dc2626", F: "#7f1d1d" };
  const MDL = ["🥇", "🥈", "🥉", "④", "⑤"];

  // Header (Kingdom + school info)
  let hdr = `
    <div style="display:flex;justify-content:center;margin-bottom:4px">
      <div style="text-align:center">
        <div style="font-size:16px;font-weight:900;color:#1a1a2e;letter-spacing:0.5px">ព្រះរាជាណាចក្របកម្ពុជា</div>
        <div style="font-size:16px;color:#333;margin-top:2px">ជាតិ សាសនា ព្រះមហាក្សត្រ</div>
      </div>
    </div>
    <div style="text-align:left;font-size:16px;color:#1e3a5f;line-height:2;margin-bottom:4px">
      <div><strong>រដ្ឋបាលស្រុកភ្នំស្រុក</strong></div>
      <div><strong>ការិយាល័យអប់រំ យុវជន និងកីឡាស្រុក</strong></div>
      <div><strong>កម្រងស្ពានស្រែង</strong></div>
      <div>${school} រោគ</div>
    </div>
    <hr style="border:none;border-top:2.5px solid #1e3a5f;margin:4px 0 10px"/>
    <div style="text-align:center;font-size:20px;font-weight:900;color:#b45309;margin:6px 0 3px">🏆 តារាងកិត្តិយស</div>
    <div style="text-align:center;font-size:14px;font-weight:800;color:#1e3a5f;margin-bottom:18px">ថ្នាក់ទី ${selClass} · ${curSem().label} · ខែ${MONTHS[selMonth]}</div>
  `;

  function makeCard(s, i) {
    const avg = Number(getAvg(s.id));
    const g = gradeOf(avg);
    const photo = honorPhotos[s.id] || null;
    const bc = RANK_BORDER[i] || "#e5e7eb";
    const bgc = RANK_BG[i] || "#fff";
    const photoSize = i === 0 ? 100 : 88;
    const cardW = i === 0 ? 155 : 140;
    const photoHtml = photo
      ? `<img src="${photo}" style="width:${photoSize}px;height:${photoSize}px;object-fit:cover;border-radius:50%;border:4px solid ${bc};display:block;">`
      : `<div style="width:${photoSize}px;height:${photoSize}px;border-radius:50%;border:4px solid ${bc};background:#f1f5f9;display:flex;align-items:center;justify-content:center;font-size:${i === 0 ? 42 : 36}px;line-height:1;">${s.gender === "ស្រី" ? "👩" : "👨"}</div>`;
    const medalBadge = MDL[i] ? `<div style="font-size:${i === 0 ? 26 : 22}px;line-height:1;margin-bottom:6px;">${MDL[i]}</div>` : "";
    return `
      <div style="text-align:center;width:${cardW}px;background:${bgc};border-radius:18px;border:2.5px solid ${bc};padding:16px 12px 14px;box-shadow:0 4px 18px rgba(0,0,0,0.13);">
        ${medalBadge}
        <div style="margin:0 auto 10px;display:flex;justify-content:center;">${photoHtml}</div>
        <div style="font-weight:900;font-size:${i === 0 ? 14 : 13}px;color:#1e3a5f;line-height:1.3;margin-bottom:4px;">${s.lastName} ${s.firstName}</div>
        <div style="font-size:${i === 0 ? 16 : 14}px;font-weight:900;color:${GRADE_C[g.l]};margin-bottom:5px;">${fmtAvg(avg)}</div>
        <div style="display:inline-block;background:${g.c};color:#fff;border-radius:20px;padding:3px 12px;font-size:${i === 0 ? 12 : 11}px;font-weight:800;">និទ្ទេស ${g.l}</div>
        <div style="font-size:11px;color:#6b7280;margin-top:3px;">ចំណាត់ថ្នាក់ ${s._rank}</div>
      </div>
    `;
  }

  // Official block: cards arranged with 3 columns and rows as pyramid
  const empty = `<div style="width:155px;"></div>`;
  let official = `<div style="display:flex;flex-direction:column;gap:16px;margin-bottom:30px;align-items:center;">`;
  official += `<div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:16px;align-items:end;width:480px;">${empty}${makeCard(top5[0], 0)}${empty}</div>`;
  official += `<div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:16px;align-items:start;width:480px;">${makeCard(top5[1], 1)}${empty}${makeCard(top5[2], 2)}</div>`;
  official += `<div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:16px;align-items:start;width:480px;">${makeCard(top5[3], 3)}${empty}${makeCard(top5[4], 4)}</div>`;
  official += `</div>`;

  // Signature block below official
  let sig = `<div style="display:flex;justify-content:space-between;margin-top:40px;font-size:11px;gap:4px;">
    <div style="text-align:center;flex:1;">
      <div style="font-size:14px;font-weight:700;color:#1e3a5f;">បានឃើញ និងឯកភាព</div>
      <div style="font-size:14px;text-align:left;color:#374151;line-height:1.8;margin-top:3px;">${dates.d2.lunar}</div>
      <div style="font-size:14px;text-align:left;">ស្ពានស្រែង ${dates.d2.solar}</div>
      <div style="font-weight:700;color:#1e3a5f;font-size:14px;margin-top:3px;">នាយកកម្រង</div>
      <div style="margin-top:36px;font-size:12px;color:#1e3a5f;padding-top:3px;border-top:1px dotted #94a3b8;"> </div>
    </div>
    <div style="text-align:center;flex:1;">
      <div style="font-size:14px;font-weight:700;color:#1e3a5f;">បានឃើញ និងពិនិត្យ</div>
      <div style="font-size:14px;text-align:left;color:#374151;line-height:1.8;margin-top:3px;">${dates.d1.lunar}</div>
      <div style="font-size:14px;text-align:left;">រោគ ${dates.d1.solar}</div>
      <div style="font-weight:700;color:#1e3a5f;font-size:14px;margin-top:3px;">នាយក/នាយិកា</div>
      <div style="margin-top:36px;font-size:12px;color:#1e3a5f;padding-top:3px;border-top:1px dotted #94a3b8;"> </div>
    </div>
    <div style="text-align:center;flex:1;">
      <div style="font-size:14px;text-align:left;color:#374151;line-height:1.8;margin-top:3px;">${dates.d0.lunar}</div>
      <div style="font-size:14px;text-align:left;">រោគ ${dates.d0.solar}</div>
      <div style="font-weight:700;color:#1e3a5f;font-size:11px;margin-top:3px;">គ្រូប្រចាំថ្នាក់</div>
      <div style="margin-top:36px;font-weight:900;color:#1e3a5f;font-size:14px;padding-top:3px;border-top:1px dotted #94a3b8;">${tName.trim()}</div>
    </div>
  </div>`;

  return `<!DOCTYPE html>
    <html lang="km">
    <head>
      <meta charset="UTF-8">
      <title>តារាងកិត្តិយស</title>
      <link href="https://fonts.googleapis.com/css2?family=Hanuman:wght@400;700;900&family=Battambang:wght@400;700&display=swap" rel="stylesheet">
      <style>
        *{box-sizing:border-box;margin:0;padding:0}
        body{font-family:'Hanuman','Battambang',sans-serif;padding:.6cm .8cm;color:#1e293b;font-size:11px}
        @page{size:A4;margin:.6cm .8cm}
      </style>
    </head>
    <body>
      ${hdr}
      ${official}
      ${sig}
    </body>
    </html>`;
}
  window.doPrintHonor = function() {
    const html = buildHonorPrintHTML();
    const printWin = window.open('','_blank');
    if (!printWin) {
      const frame = $('printFrame');
      const doc = frame.contentDocument||frame.contentWindow.document;
      doc.open(); doc.write(html); doc.close();
      setTimeout(()=>{ frame.style.display='block'; frame.contentWindow.focus(); frame.contentWindow.print(); setTimeout(()=>{ frame.style.display='none'; },2000); },700);
      return;
    }
    printWin.document.write(html); printWin.document.close();
    setTimeout(()=>{ printWin.focus(); printWin.print(); },800);
  };

  function buildHonorAllPrintHTML() {
    const sl = stuList();
    const ranked = buildRankedList(sl);
    const tName = (teacher?.title||"")+" "+(teacher?.fullName||"");
    const school = teacher?.school || "សាលាបឋមសិក្សា";
    const dates = getThreeWorkingDates();

    let hdr = `<div style="display:flex;justify-content:center;margin-bottom:4px"><div style="text-align:center"><div style="font-size:14px;font-weight:900;color:#1a1a2e">ព្រះរាជាណាចក្របកម្ពុជា</div><div style="font-size:12px;color:#333;margin-top:2px">ជាតិ សាសនា ព្រះមហាក្សត្រ</div></div></div>`;
    hdr += `<div style="text-align:left;font-size:12px;color:#1e3a5f;line-height:2;margin-bottom:4px"><div><strong>រដ្ឋបាលស្រុកភ្នំស្រុក</strong></div><div><strong>ការិយាល័យអប់រំ យុវជន និងកីឡាស្រុក</strong></div><div><strong>កម្រងស្ពានស្រែង</strong></div><div>${school} រោគ</div></div>`;
    hdr += `<hr style="border:none;border-top:2.5px solid #1e3a5f;margin:4px 0 8px"/>`;
    hdr += `<div style="text-align:center;font-size:16px;font-weight:900;color:#b45309;margin:5px 0 2px">🏆 តារាងកិត្តិយស</div>`;
    hdr += `<div style="text-align:center;font-size:14px;font-weight:800;color:#1e3a5f;margin-bottom:10px">ថ្នាក់ទី ${selClass} · ${curSem().label} · ខែ${MONTHS[selMonth]}</div>`;

    // Build two-column table of all students
    const half = Math.ceil(ranked.length / 2);
    const col1 = ranked.slice(0, half);
    const col2 = ranked.slice(half);
    const MEDAL = ["🥇","🥈","🥉","④","⑤"];
    const GRADE_C = { A:"#15803d", B:"#1d4ed8", C:"#b45309", D:"#c2410c", E:"#dc2626", F:"#7f1d1d" };

    function buildCol(students, startIdx) {
      let rows = "";
      students.forEach((s, idx) => {
        const avg = Number(getAvg(s.id));
        const g = gradeOf(avg);
        const medal = s._rank <= 5 ? MEDAL[s._rank-1] : "";
        const isTop3 = s._rank <= 3;
        const bg = s._rank===1?"#fffbeb":s._rank===2?"#f8fafc":s._rank===3?"#fff7ed":"#fff";
        rows += `<tr style="background:${bg}">
          <td style="text-align:center;font-weight:700;font-size:12px;padding:4px 2px;">${s._rank}${medal}</td>
          <td style="text-align:left;font-weight:${isTop3?"900":"600"};font-size:12px;padding:4px 4px;color:${isTop3?"#1e3a5f":"#374151"}">${s.lastName} ${s.firstName}</td>
          <td style="text-align:center;font-size:12px;padding:4px 2px;">${s.gender==="ស្រី"?"ស":"ប"}</td>
          <td style="text-align:center;font-weight:800;font-size:12px;padding:4px 2px;color:${GRADE_C[g.l]}">${fmtAvg(avg)}</td>
          <td style="text-align:center;padding:4px 2px;"><span style="background:${g.c};color:#fff;border-radius:10px;padding:2px 7px;font-size:12px;font-weight:800;">${g.l}</span></td>
        </tr>`;
      });
      return rows;
    }

    const thStyle = `background:#d4e4f7;border:1px solid #93b8d8;padding:5px 3px;text-align:center;font-weight:700;color:#1e3a5f;font-size:12px;`;
    const tblStyle = `width:100%;border-collapse:collapse;font-size:10px;`;
    const tblHeader = `<tr><th style="${thStyle}width:30px">ចំ.ថ្នាក់</th><th style="${thStyle}text-align:left;min-width:90px">គោត្តនាម-នាម</th><th style="${thStyle}width:22px">ភេទ</th><th style="${thStyle}width:36px">ម.ប</th><th style="${thStyle}width:28px">និទ្ទេស</th></tr>`;
     
   // កែសម្រួល block cards ក្នុង buildHonorPrintHTML()
const empty = `<div style="width:155px;"></div>`;
let cards = `<div style="display:flex;flex-direction:column;gap:16px;margin-bottom:5px;align-items:center;">`;

// Header: card 1 កណ្ដាល
cards += `<div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:16px;align-items:end;width:480px;">${empty}${makeCard(top5[0],0)}${empty}</div>`;

// បន្ទាប់: card 2 និង 3 ជួរតែមួយ និង card 4 និង 5 ជួរតែមួយ
cards += `<div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:16px;align-items:start;width:480px;">${makeCard(top5[1],1)}${empty}${makeCard(top5[2],2)}</div>`;
cards += `<div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:16px;align-items:start;width:480px;">${makeCard(top5[3],3)}${empty}${makeCard(top5[4],4)}</div>`;

cards += `</div>`;
   
    // Stats summary
    const total_s = ranked.length;
    const passC = ranked.filter(s => Number(getAvg(s.id)) >= 5).length;
    const failC = total_s - passC;
    const females = ranked.filter(s => s.gender === "ស្រី").length;
    const statsHTML = `<div style="margin-top:8px;font-size:10px;color:#1e293b;border:1px solid #cbd5e1;border-radius:8px;padding:8px 12px;background:#f8fafc;display:grid;grid-template-columns:1fr 1fr;gap:0 16px;">
      <span>សិស្សសរុប: <strong>${total_s}</strong>នាក់ · ស្រី: <strong>${females}</strong>នាក់</span>
      <span>ជាប់: <strong style="color:#16a34a">${passC}</strong>នាក់ · ធ្លាក់: <strong style="color:#dc2626">${failC}</strong>នាក់</span>
    </div>`;

    const sig = `<div style="display:flex;justify-content:space-between;margin-top:18px;font-size:14px;gap:4px;">
      <div style="text-align:center;flex:1;"><div style="font-size:14px;font-weight:700;color:#1e3a5f;">បានឃើញ និងឯកភាព</div>
        <div style="font-size:12px;text-align:left;color:#374151;line-height:1.8;margin-top:2px;">${dates.d2.lunar}</div>
        <div style="font-size:12px;text-align:left;">ស្ពានស្រែង ${dates.d2.solar}</div>
        <div style="font-weight:700;color:#1e3a5f;font-size:11px;margin-top:3px;">នាយកកម្រង</div>
        <div style="margin-top:32px;font-size:12px;color:#1e3a5f;padding-top:3px;border-top:1px dotted #94a3b8;"> </div></div>
      <div style="text-align:center;flex:1;"><div style="font-size:12px;font-weight:700;color:#1e3a5f;">បានឃើញ និងពិនិត្យ</div>
        <div style="font-size:12px;text-align:left;color:#374151;line-height:1.8;margin-top:2px;">${dates.d1.lunar}</div>
        <div style="font-size:12px;text-align:left;">រោគ ${dates.d1.solar}</div>
        <div style="font-weight:700;color:#1e3a5f;font-size:13px;margin-top:3px;">នាយក/នាយិកា</div>
        <div style="margin-top:32px;font-size:12px;color:#1e3a5f;padding-top:3px;border-top:1px dotted #94a3b8;"> </div></div>
      <div style="text-align:center;flex:1;">
        <div style="font-size:12px;text-align:left;color:#374151;line-height:1.8;margin-top:2px;">${dates.d0.lunar}</div>
        <div style="font-size:11px;text-align:left;">រោគ ${dates.d0.solar}</div>
        <div style="font-weight:700;color:#1e3a5f;font-size:11px;margin-top:3px;">គ្រូប្រចាំថ្នាក់</div>
        <div style="margin-top:32px;font-weight:900;color:#1e3a5f;font-size:12px;padding-top:3px;border-top:1px dotted #94a3b8;">${tName.trim()}</div></div>
    </div>`;

    return `<!DOCTYPE html><html lang="km"><head><meta charset="UTF-8"><title>តារាងកិត្តិយស PLP 2026</title><link href="https://fonts.googleapis.com/css2?family=Hanuman:wght@400;700;900&family=Battambang:wght@400;700&display=swap" rel="stylesheet"><style>*{box-sizing:border-box;margin:0;padding:0}body{font-family:'Hanuman','Battambang',sans-serif;font-size:11px;padding:.6cm .8cm;color:#1e293b}@page{size:A4;margin:.6cm .8cm}table{border-collapse:collapse}td,th{border:1px solid #cbd5e1}</style></head><body>${hdr}${tableHTML}${statsHTML}${sig}</body></html>`;
  }

  window.doPrintHonorAll = function() {
    const html = buildHonorAllPrintHTML();
    const printWin = window.open('','_blank');
    if (!printWin) {
      const frame = $('printFrame');
      const doc = frame.contentDocument||frame.contentWindow.document;
      doc.open(); doc.write(html); doc.close();
      setTimeout(()=>{ frame.style.display='block'; frame.contentWindow.focus(); frame.contentWindow.print(); setTimeout(()=>{ frame.style.display='none'; },2000); },700);
      return;
    }
    printWin.document.write(html); printWin.document.close();
    setTimeout(()=>{ printWin.focus(); printWin.print(); },800);
  };

  function makeTbl(headers, classes=[], sticky=false, attMode=false) {
    const tbl = document.createElement("table"); tbl.className = "main-tbl";
    const thead = document.createElement("thead"); const tr = document.createElement("tr");
    headers.forEach((h,i)=>{
      const th = document.createElement("th");
      if (classes[i]==="sum") th.classList.add("sum");
      th.style.minWidth = i===0?"30px":attMode&&i>2&&i<headers.length-3?"22px":"auto";
      if (attMode&&i>2&&i<headers.length-3) th.style.fontSize="10px";
      if (sticky&&i===0) th.classList.add("sticky-col");
      th.textContent = h; tr.appendChild(th);
    });
    thead.appendChild(tr); tbl.appendChild(thead);
    const tbody = document.createElement("tbody"); tbl.appendChild(tbody);
    return tbl;
  }

  function trOf(i, cells) { const tr = document.createElement("tr"); cells.forEach((c)=>tr.appendChild(c)); return tr; }
  function td(txt) { const c = document.createElement("td"); c.textContent = txt; return c; }
  function tdC(txt, color="") { const c = document.createElement("td"); c.className="center"; c.textContent=txt; if(color) c.style.color=color; return c; }
  function tdSum(txt, color="") { const c = document.createElement("td"); c.className="center sum-cell"; c.textContent=txt; if(color) c.style.color=color; return c; }
  function tdInput(val, onChange) { const c=document.createElement("td"); const inp=document.createElement("input"); inp.className="ci"; inp.type="text"; inp.value=val; inp.oninput=(e)=>onChange(e.target.value); c.appendChild(inp); return c; }
  function tdGender(g) {
    const c=document.createElement("td"); c.className="center";
    const sp=document.createElement("span"); sp.className="g-badge";
    sp.style.background=g==="ស្រី"?"#fce7f3":"#dbeafe"; sp.style.color=g==="ស្រី"?"#9d174d":"#1e40af";
    sp.textContent=(g==="ស្រី"?"👩 ":"👨 ")+g; c.appendChild(sp); return c;
  }
  function tdGrade(g) {
    const c=document.createElement("td"); c.className="center";
    const sp=document.createElement("span"); sp.className="grade-badge"; sp.style.background=g.c; sp.textContent=g.l; c.appendChild(sp); return c;
  }
  function tdDel(sid) {
    const c=document.createElement("td"); c.className="center";
    if (editMode) { const btn=document.createElement("button"); btn.className="btn-del"; btn.textContent="🗑️"; btn.onclick=()=>handleDel(sid); c.appendChild(btn); }
    return c;
  }
  function nameCell(s) {
    const d=document.createElement("div"); d.className="name-cell";
    const dot=document.createElement("span"); dot.className="ndot"; dot.style.background=s.gender==="ស្រី"?"#ec4899":"#3b82f6";
    const txt=document.createTextNode(`${s.lastName} ${s.firstName}`);
    d.appendChild(dot); d.appendChild(txt); return d;
  }
  function emptyEl(icon, msg) { const d=document.createElement("div"); d.className="empty"; d.innerHTML=`<div class="e-icon">${icon}</div><div>${msg}</div>`; return d; }



// ════ CSV HELPERS ════
  function csvEscape(v) {
    const s = String(v ?? "");
    return s.includes(",") || s.includes('"') || s.includes("\n") ? `"${s.replace(/"/g,'""')}"` : s;
  }
  function csvRow(arr) { return arr.map(csvEscape).join(","); }
  function downloadCSV(filename, rows) {
    const bom = "\uFEFF"; // UTF-8 BOM for Excel
    const content = bom + rows.join("\r\n");
    const blob = new Blob([content], { type: "text/csv;charset=utf-8;" });
    const url = URL.createObjectURL(blob);
    const a = document.createElement("a"); a.href = url; a.download = filename;
    document.body.appendChild(a); a.click();
    document.body.removeChild(a); URL.revokeObjectURL(url);
  }
  function parseCSV(text) {
    const lines = text.replace(/\r\n/g,"\n").replace(/\r/g,"\n").split("\n").filter(l=>l.trim());
    return lines.map(line => {
      const cols = []; let cur = "", inQ = false;
      for (let i = 0; i < line.length; i++) {
        const c = line[i];
        if (c === '"') { if (inQ && line[i+1]==='"') { cur+='"'; i++; } else inQ=!inQ; }
        else if (c === ',' && !inQ) { cols.push(cur.trim()); cur=""; }
        else cur += c;
      }
      cols.push(cur.trim()); return cols;
    });
  }

  // ════ STUDENTS EXPORT/IMPORT ════
  const STU_FIELDS = ["lastName","firstName","gender","dob","age","fatherName","motherName","village","commune","district","province","phone"];
  const STU_HEADERS = ["គោត្តនាម","នាម","ភេទ","ថ្ងៃខែឆ្នាំកំណើត","អាយុ","ឈ្មោះឪពុក","ឈ្មោះម្តាយ","ភូមិ","ឃុំ","ស្រុក","ខេត្ត","ទូរស័ព្ទ"];

  window.exportStudentsCSV = function() {
    const sl = stuList();
    if (!sl.length) { toast("⚠️ មិនមានសិស្ស", "error"); return; }
    const rows = [csvRow(STU_HEADERS)];
    sl.forEach(s => rows.push(csvRow(STU_FIELDS.map(f => s[f] || ""))));
    downloadCSV(`students_${selClass}_${new Date().toISOString().slice(0,10)}.csv`, rows);
    $("ioStuLog").innerHTML = `✅ Export <strong>${sl.length}</strong>នាក់ ដោយជោគជ័យ`;
    toast("📤 Export ដោយជោគជ័យ");
  };

  window.importStudentsCSV = async function(input) {
    const file = input.files[0]; if (!file) return;
    const log = $("ioStuLog");
    log.textContent = "⏳ កំពុងដំណើរការ...";
    try {
      const text = await file.text();
      const rows = parseCSV(text);
      if (rows.length < 2) { log.textContent = "❌ File ទទេ ឬ Format ខុស"; return; }
      const header = rows[0];
      // Map header to field index
      const fieldIdx = STU_HEADERS.map(h => header.indexOf(h));
      // Also try English fallback
      const engHeaders = STU_FIELDS;
      const fieldIdxFb = STU_FIELDS.map(f => header.indexOf(f));
      const getIdx = (i) => fieldIdx[i] >= 0 ? fieldIdx[i] : fieldIdxFb[i];
      let added = 0, skipped = 0;
      for (let r = 1; r < rows.length; r++) {
        const row = rows[r];
        if (row.every(c => !c)) continue;
        const stu = {};
        STU_FIELDS.forEach((f, i) => { const idx = getIdx(i); stu[f] = idx >= 0 ? (row[idx] || "") : ""; });
        if (!stu.lastName && !stu.firstName) { skipped++; continue; }
        if (!stu.gender) stu.gender = "ប្រុស";
        await dbPush(`plp2026/${selClass}/students`, stu);
        added++;
      }
      await window.loadAll();
      log.innerHTML = `✅ Import <strong>${added}</strong>នាក់ ✓   ⚠️ Skip <strong>${skipped}</strong>row`;
      toast(`✅ Import ${added} សិស្ស`);
    } catch(e) { log.textContent = "❌ Error: " + e.message; toast("❌ Import Error", "error"); }
    input.value = "";
  };

  // ════ SCORES EXPORT/IMPORT ════
  window.exportScoresCSV = function() {
    const sl = stuList();
    if (!sl.length) { toast("⚠️ មិនមានសិស្ស", "error"); return; }
    const headers = ["គោត្តនាម","នាម","ភេទ", ...SUBJECTS];
    const rows = [csvRow(headers)];
    sl.forEach(s => {
      const subScores = SUBJECTS.map(subj => getSco(s.id, subj) !== "" ? getSco(s.id, subj) : "");
      rows.push(csvRow([s.lastName, s.firstName, s.gender, ...subScores]));
    });
    const semLabel = SEMESTERS.find(s=>s.id===semester)?.label || semester;
    downloadCSV(`scores_${selClass}_${semLabel}_${MONTHS[selMonth]}_${new Date().toISOString().slice(0,10)}.csv`, rows);
    $("ioScoLog").innerHTML = `✅ Export ពិន្ទុ <strong>${sl.length}</strong>នាក់ ខែ${MONTHS[selMonth]}`;
    toast("📤 Export ពិន្ទុ ដោយជោគជ័យ");
  };

  window.importScoresCSV = async function(input) {
    const file = input.files[0]; if (!file) return;
    const log = $("ioScoLog");
    log.textContent = "⏳ កំពុងដំណើរការ...";
    try {
      const text = await file.text();
      const rows = parseCSV(text);
      if (rows.length < 2) { log.textContent = "❌ File ទទេ ឬ Format ខុស"; return; }
      const header = rows[0];
      // Find subject column indices
      const subjIdx = SUBJECTS.map(subj => header.indexOf(subj));
      const lastIdx = header.indexOf("គោត្តនាម");
      const firstIdx = header.indexOf("នាម");
      if (lastIdx < 0 || firstIdx < 0) { log.textContent = "❌ រក column 'គោត្តនាម' ឬ 'នាម' មិនឃើញ"; return; }
      // Build name→id map from localStu
      const nameMap = {};
      stuList().forEach(s => { nameMap[`${s.lastName}_${s.firstName}`] = s.id; });
      let matched = 0, notFound = 0, updated = 0;
      const newSco = JSON.parse(JSON.stringify(localSco));
      for (let r = 1; r < rows.length; r++) {
        const row = rows[r];
        if (row.every(c => !c)) continue;
        const ln = row[lastIdx] || "", fn = row[firstIdx] || "";
        const sid = nameMap[`${ln}_${fn}`];
        if (!sid) { notFound++; continue; }
        matched++;
        if (!newSco[sid]) newSco[sid] = {};
        let changed = false;
        SUBJECTS.forEach((subj, i) => {
          const ci = subjIdx[i];
          if (ci < 0) return;
          const raw = row[ci];
          if (raw === "" || raw === undefined) return;
          const val = parseFloat(raw);
          if (!isNaN(val) && val >= 0 && val <= 10) { newSco[sid][subj] = val; changed = true; }
        });
        if (changed) updated++;
      }
      // Save to Firebase
      await dbSet(`plp2026/${selClass}/scores/${semester}/${selMonth}`, newSco);
      localSco = newSco; scores = JSON.parse(JSON.stringify(newSco));
      renderContent();
      log.innerHTML = `✅ Match <strong>${matched}</strong>នាក់ · Update <strong>${updated}</strong>នាក់ · NotFound <strong>${notFound}</strong>row`;
      toast(`✅ Import ពិន្ទុ ${updated} សិស្ស 🔥`);
    } catch(e) { log.textContent = "❌ Error: " + e.message; toast("❌ Import Error", "error"); }
    input.value = "";
  };

  // ════ XLSX EXPORT ════
  function loadSheetJS(cb) {
    if (window.XLSX) { cb(); return; }
    const s = document.createElement('script');
    s.src = 'https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js';
    s.onload = cb; document.head.appendChild(s);
  }

  window.exportScoresXLSX = function() {
    const sl = stuList();
    if (!sl.length) { toast("⚠️ មិនមានសិស្ស", "error"); return; }
    loadSheetJS(() => {
      const ranked = buildRankedList(sl);
      const semLabel = SEMESTERS.find(s=>s.id===semester)?.label || semester;
      const wb = XLSX.utils.book_new();

      // Sheet 1: ពិន្ទុ (Scores)
      const headers = ["ល.រ", "ចំណាត់ថ្នាក់", "គោត្តនាម", "នាម", "ភេទ", ...SUBJECTS, "ពិន្ទុសរុប", "មធ្យមភាគ", "លទ្ធផល", "និទ្ទេស"];
      const rows = [headers];
      ranked.forEach((s, i) => {
        const avg = getAvg(s.id);
        const total = getTotal(s.id);
        const g = gradeOf(avg);
        const subScores = SUBJECTS.map(subj => {
          const v = getSco(s.id, subj);
          return v !== "" ? Number(v) : "";
        });
        rows.push([i+1, s._rank, s.lastName, s.firstName, s.gender, ...subScores, total, Number(fmtAvg(avg)), resultOf(avg), g.l]);
      });
      const ws = XLSX.utils.aoa_to_sheet(rows);
      // Style header row width
      ws['!cols'] = [
        {wch:5},{wch:8},{wch:14},{wch:12},{wch:8},
        ...SUBJECTS.map(()=>({wch:14})),
        {wch:10},{wch:10},{wch:8},{wch:8}
      ];
      XLSX.utils.book_append_sheet(wb, ws, `ពិន្ទុ_${MONTHS[selMonth]}`);

      // Sheet 2: Rank Summary
      const hdrs2 = ["ល.រ","ចំណាត់ថ្នាក់","គោត្តនាម-នាម","ភេទ","ពិន្ទុសរុប","មធ្យមភាគ","លទ្ធផល","និទ្ទេស"];
      const rows2 = [hdrs2];
      ranked.forEach((s, i) => {
        const avg = getAvg(s.id);
        const g = gradeOf(avg);
        rows2.push([i+1, s._rank, `${s.lastName} ${s.firstName}`, s.gender, getTotal(s.id), Number(fmtAvg(avg)), resultOf(avg), g.l]);
      });
      const ws2 = XLSX.utils.aoa_to_sheet(rows2);
      ws2['!cols'] = [{wch:5},{wch:8},{wch:22},{wch:8},{wch:10},{wch:10},{wch:8},{wch:8}];
      XLSX.utils.book_append_sheet(wb, ws2, "ចំណាត់ថ្នាក់");

      const fname = `scores_${selClass}_${semLabel}_${MONTHS[selMonth]}_${new Date().toISOString().slice(0,10)}.xlsx`;
      XLSX.writeFile(wb, fname);
      $("ioScoLog").innerHTML = `✅ Export XLSX <strong>${sl.length}</strong>នាក់ ដោយជោគជ័យ`;
      toast("📊 Export XLSX ដោយជោគជ័យ");
    });
  };

  window.exportAllDataXLSX = function() {
    const sl = stuList();
    if (!sl.length) { toast("⚠️ មិនមានសិស្ស", "error"); return; }
    loadSheetJS(() => {
      const ranked = buildRankedList(sl);
      const wb = XLSX.utils.book_new();

      // Sheet 1: Student Info
      const hStu = ["ល.រ","គោត្តនាម","នាម","ភេទ","ថ្ងៃខែឆ្នាំកំណើត","អាយុ","ឈ្មោះឪពុក","ឈ្មោះម្តាយ","ភូមិ","ឃុំ","ស្រុក","ខេត្ត","ទូរស័ព្ទ"];
      const rStu = [hStu];
      sl.forEach((s,i) => rStu.push([i+1,s.lastName,s.firstName,s.gender,s.dob||"",s.age||"",s.fatherName||"",s.motherName||"",s.village||"",s.commune||"",s.district||"",s.province||"",s.phone||""]));
      const wsStu = XLSX.utils.aoa_to_sheet(rStu);
      wsStu['!cols'] = [{wch:5},{wch:14},{wch:12},{wch:8},{wch:16},{wch:6},{wch:16},{wch:16},{wch:14},{wch:14},{wch:14},{wch:14},{wch:12}];
      XLSX.utils.book_append_sheet(wb, wsStu, "ព័ត៌មានសិស្ស");

      // Sheet 2: Scores + Rank
      const hSco = ["ល.រ","ចំណាត់ថ្នាក់","គោត្តនាម","នាម","ភេទ",...SUBJECTS,"ពិន្ទុសរុប","មធ្យមភាគ","លទ្ធផល","និទ្ទេស"];
      const rSco = [hSco];
      ranked.forEach((s,i) => {
        const avg = getAvg(s.id);
        const g = gradeOf(avg);
        rSco.push([i+1, s._rank, s.lastName, s.firstName, s.gender,
          ...SUBJECTS.map(subj => { const v = getSco(s.id,subj); return v!==""?Number(v):""; }),
          getTotal(s.id), Number(fmtAvg(avg)), resultOf(avg), g.l
        ]);
      });
      const wsSco = XLSX.utils.aoa_to_sheet(rSco);
      wsSco['!cols'] = [{wch:5},{wch:8},{wch:14},{wch:12},{wch:8},...SUBJECTS.map(()=>({wch:14})),{wch:10},{wch:10},{wch:8},{wch:8}];
      XLSX.utils.book_append_sheet(wb, wsSco, `ពិន្ទុ_${MONTHS[selMonth]}`);

      // Sheet 3: Attendance
      const hAtt = ["ល.រ","គោត្តនាម-នាម","ភេទ",...Array.from({length:31},(_,i)=>String(i+1)),"វត្តមាន(P)","អវត្តមាន(A)"];
      const rAtt = [hAtt];
      sl.forEach((s,i) => {
        const p = cntAtt(s.id,"P"), a = cntAtt(s.id,"A");
        rAtt.push([i+1,`${s.lastName} ${s.firstName}`,s.gender,...Array.from({length:31},(_,d)=>getAtt(s.id,d+1)||""),p,a]);
      });
      const wsAtt = XLSX.utils.aoa_to_sheet(rAtt);
      wsAtt['!cols'] = [{wch:5},{wch:22},{wch:8},...Array.from({length:31},()=>({wch:4})),{wch:10},{wch:10}];
      XLSX.utils.book_append_sheet(wb, wsAtt, "វត្តមាន");

      const semLabel = SEMESTERS.find(s=>s.id===semester)?.label||semester;
      const fname = `PLP_${selClass}_${semLabel}_${MONTHS[selMonth]}_${new Date().toISOString().slice(0,10)}.xlsx`;
      XLSX.writeFile(wb, fname);
      $("ioScoLog").innerHTML = `✅ Export XLSX លម្អិត <strong>${sl.length}</strong>នាក់ (ព័ត៌មាន+ពិន្ទុ+វត្តមាន)`;
      toast("📋 Export ទិន្នន័យទាំងអស់ XLSX ✅");
    });
  };

  // ════ IO MODAL ════
  window.openIOModal = function() {
    $("ioScoLabel").textContent = `${SEMESTERS.find(s=>s.id===semester)?.label||""} · ខែ${MONTHS[selMonth]}`;
    $("ioStuLog").textContent = "រង់ចាំ...";
    $("ioScoLog").textContent = "រង់ចាំ...";
    window.ioSetTab("stu");
    $("ioModal").style.display = "flex";
  };

  window.ioSetTab = function(tab) {
    const isStu = tab === "stu";
    $("ioPanelStu").style.display = isStu ? "" : "none";
    $("ioPanelSco").style.display = isStu ? "none" : "";
    $("ioTabStu").style.cssText = isStu
      ? "flex:1;padding:8px;border-radius:8px;border:2px solid #2563eb;background:#eff6ff;color:#2563eb;font-weight:800;cursor:pointer;font-family:inherit;font-size:13px"
      : "flex:1;padding:8px;border-radius:8px;border:2px solid #e5e7eb;background:#fff;color:#6b7280;font-weight:700;cursor:pointer;font-family:inherit;font-size:13px";
    $("ioTabSco").style.cssText = isStu
      ? "flex:1;padding:8px;border-radius:8px;border:2px solid #e5e7eb;background:#fff;color:#6b7280;font-weight:700;cursor:pointer;font-family:inherit;font-size:13px"
      : "flex:1;padding:8px;border-radius:8px;border:2px solid #7c3aed;background:#f5f3ff;color:#6d28d9;font-weight:800;cursor:pointer;font-family:inherit;font-size:13px";
  };
    </script>
<script defer="" src="https://static.cloudflareinsights.com/beacon.min.js/v8c78df7c7c0f484497ecbca7046644da1771523124516" integrity="sha512-8DS7rgIrAmghBFwoOTujcf6D9rXvH8xm8JQ1Ja01h9QX8EzXldiszufYa4IFfKdLUKTTrnSFXLDkUEOTrZQ8Qg==" data-cf-beacon="{" version":"2024.11.0","token":"e3c1c9af36de41759418005494a48906","r":1,"server_timing":{"name":{"cfcachestatus":true,"cfedge":true,"cfextpri":true,"cfl4":true,"cforigin":true,"cfspeedbrain":true},"location_startswith":null}}"="" crossorigin="anonymous"></script>
</div></template>
<template id="tpl-standard">
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=0.85">
<title>ស្វ័យវាយតម្លៃ ២០២៦</title>
<link href="https://fonts.googleapis.com/css2?family=Hanuman:wght@400;700&amp;family=Battambang:wght@400;700&amp;display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js"></script>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:"Hanuman","Battambang",sans-serif;background:#eef2f7;font-size:13px}

/* toolbar */
#toolbar{background:linear-gradient(135deg,#1565c0,#1976d2);color:#fff;
  padding:8px 14px;display:flex;align-items:center;gap:6px;flex-wrap:wrap;
  position:sticky;top:0;z-index:200;box-shadow:0 2px 8px rgba(0,0,0,.3)}
#toolbar h1{font-size:13px;font-weight:700;margin-right:4px;white-space:nowrap}
.sep{width:1px;height:22px;background:rgba(255,255,255,.3);margin:0 2px}
.tb{display:inline-flex;align-items:center;gap:5px;padding:5px 11px;
  border-radius:6px;border:none;font-family:inherit;font-size:12px;
  font-weight:600;cursor:pointer;white-space:nowrap;transition:all .18s}
.tb:hover{filter:brightness(1.1);transform:translateY(-1px)}
.g{background:#43a047;color:#fff}.b{background:#0288d1;color:#fff}
.o{background:#f57c00;color:#fff}.p{background:#7b1fa2;color:#fff}
.e{background:#2e7d32;color:#fff}.s{background:#546e7a;color:#fff}
#schoolInput{padding:5px 9px;border-radius:6px;border:2px solid rgba(255,255,255,.35);
  background:rgba(255,255,255,.15);color:#fff;font-family:inherit;font-size:12px;width:170px}
#schoolInput::placeholder{color:rgba(255,255,255,.65)}
#st{margin-left:auto;font-size:11px;padding:3px 8px;border-radius:4px;white-space:nowrap}
.ok{background:rgba(76,175,80,.35)}.err{background:rgba(244,67,54,.35)}
.busy{background:rgba(255,193,7,.4);color:#000}

/* tabs */
#tabs{background:#0d47a1;display:flex;padding:0 12px;overflow-x:auto;gap:2px}
.tab{padding:9px 16px;color:rgba(255,255,255,.65);border:none;background:transparent;
  font-family:inherit;font-size:13px;font-weight:700;cursor:pointer;
  border-bottom:3px solid transparent;white-space:nowrap;transition:all .18s}
.tab.active{color:#fff;border-bottom-color:#ffeb3b}
.tab:hover{color:#fff}

/* content */
#content{padding:10px}
.tab-pane{display:none}.tab-pane.active{display:block}

/* ==========================================================================
   1. TABLE STYLES (ទម្រង់តារាងទូទៅ)
   ========================================================================== */
.std-table {
  border-collapse: collapse;
  width: 100%;
  background: #fff;
  box-shadow: 0 1px 6px rgba(0,0,0,.12);
  border-radius: 4px;
  overflow: hidden;
}

.std-table th, 
.std-table td {
  border: 1px solid #bdc3c7;
  padding: 10px 8px;                 /* បង្កើន padding ឱ្យមើលទៅធំទូលាយល្មម */
  vertical-align: middle !important; /* បង្ខំឱ្យអក្សរខ្មែរចំកណ្តាលលើក្រោម */
  line-height: 1.0 !important;       /* គម្លាតជួរអក្សរខ្មែរមានលំនឹងមិនជាន់គ្នា */
  font-family: 'Khmer OS Battambang', 'Hanuman', sans-serif;
  font-size: 11px;                   /* ទំហំអក្សរទូទៅក្នុងតារាង */
  text-align: left;
}

/* សម្រាប់ក្បាលតារាងពណ៌ខៀវ */
.std-table thead th {
  background: #1565c0;
  color: #fff;
  font-weight: 700;
  text-align: center;                /* ឱ្យក្បាលតារាងរត់ទៅចំកណ្តាលឆ្វេងស្តាំ */
  vertical-align: middle !important;
}

.std-table tbody tr:nth-child(even) {
  background: #f9fbff;
}

.std-table tr:hover {
  background: #e8f4fd;
}

/* ==========================================================================
   2. ROW TYPES (ប្រភេទជួរដេក និងការបែងចែក Level)
   ========================================================================== */
tr.sec-hdr th, 
tr.sec-hdr td {
  background: #1a237e;
  color: #fff;
  font-weight: 700;
  text-align: left;
  padding: 12px 8px;
  vertical-align: middle !important;
}

tr.sub-hdr td {
  background: #e3f2fd;
  font-weight: 700;
  color: #0d47a1;
  text-align: left;
  padding: 10px 9px;
  vertical-align: middle !important;
}

tr.sum-row td {
  background: #e8f5e9;
  font-weight: 700;
  color: #1b5e20;
  text-align: left;
  padding: 10px 8px;
  vertical-align: middle !important;
}

tr.sum-row td:nth-last-child(-n+2) {
  text-align: center;
}

/* ==========================================================================
   3. EDITABLE ELEMENTS (ទម្រង់ Form សម្រាប់បញ្ចូលទិន្នន័យ)
   ========================================================================== */
td.sc {
  width: 40px;
  text-align: center;                /* ឱ្យលេខ ល.រ នៅចំកណ្តាល */
}

td.cc {
  min-width: 100px;
}

select.ss {
  width: 100%;
  padding: 3px;
  border: 1.5px solid #90caf9;
  border-radius: 4px;
  font-family: inherit;
  font-size: 11px;
  background: #e3f2fd;
  cursor: pointer;
}

select.ss:focus {
  outline: none;
  border-color: #1565c0;
  background: #fff;
}

textarea.ct {
  width: 100%;
  min-height: 15px;
  padding: 3px;
  border: 1.5px solid #ce93d8;
  border-radius: 4px;
  font-family: inherit;
  font-size: 11px;
  resize: vertical;
  background: #fce4ec;
}

textarea.ct:focus {
  outline: none;
  border-color: #7b1fa2;
  background: #fff;
}

/* Badges (ស្លាកសញ្ញាស្ថានភាព) */
.sv {
  display: inline-block;
  padding: 2px 7px;
  background: #c8e6c9;
  border-radius: 10px;
  font-weight: 700;
  color: #1b5e20;
}

.pv {
  display: inline-block;
  padding: 2px 7px;
  background: #fff9c4;
  border-radius: 10px;
  font-weight: 700;
  color: #5d4037;
  margin-left: 3px;
}

/* ==========================================================================
   4. TEXT UTILITIES (Class ជំនួយសម្រាប់គ្រប់គ្រងទំហំអក្សរ)
   ========================================================================== */
/* ធ្វើឱ្យអក្សរពន្យល់ចុះបន្ទាត់មកតូច និងមានពណ៌រលោងស្អាត */
.sub-text {
  display: block;               /* បង្ខំឱ្យចុះបន្ទាត់ដោយស្វ័យប្រវត្តិ */
  font-size: 11px !important;    /* ធ្វើឱ្យអក្សរតូចជាងមុន */
  color: #666666 !important;    /* ប្ដូរពណ៌ទៅប្រផេះក្រម៉ៅ */
  font-weight: normal !important; /* ដកអក្សរដិតចេញ */
  margin-top: 4px;              /* បន្ថែមគម្លាតបន្តិចពីអក្សរខាងលើ */
}

.text-small {
  font-size: 11px !important; 
}

.text-lowercase {
  text-transform: lowercase !important;
}

/* ── SUMMARY PAGE ── */
#pane-summary { padding:4px 0; }
.sum-grid { display:grid; grid-template-columns:1fr 1fr; gap:14px; margin-bottom:16px; }
@media(max-width:700px){ .sum-grid{ grid-template-columns:1fr; } }
.sum-card { background:#fff; border-radius:10px; box-shadow:0 1px 6px rgba(0,0,0,.1); padding:14px 16px; }
.sum-card h3 { font-size:13px; font-weight:700; color:#1565c0; margin-bottom:10px; border-bottom:2px solid #e3f2fd; padding-bottom:6px; }
.sum-tbl { border-collapse:collapse; width:100%; font-size:12px; }
.sum-tbl th { background:#1565c0; color:#fff; padding:5px 7px; text-align:left; }
.sum-tbl th:last-child,.sum-tbl td:last-child { text-align:center; }
.sum-tbl td { border:1px solid #ddd; padding:5px 7px; vertical-align:middle; }
.sum-tbl tr:nth-child(even) td { background:#f5f9ff; }
.sum-tbl tr:hover td { background:#e3f2fd; }
.sum-tbl .tr-std td { background:#1a237e!important; color:#fff; font-weight:700; }
.sum-tbl .tr-sub td { background:#e8eaf6!important; font-weight:700; color:#1a237e; }
.score-badge { display:inline-block; padding:2px 8px; border-radius:10px; font-weight:700; font-size:12px; }
.chart-wrap { position:relative; height:260px; }
.chart-wrap2{ position:relative; height:220px; }
.full-card { grid-column:1/-1; }

@media print{
  #toolbar,#tabs{display:none}
  .tab-pane{display:block!important}
  .std-table{page-break-inside:auto}
  select.ss{border:none;background:transparent;-webkit-appearance:none;appearance:none}
  textarea.ct{border:none;background:transparent;resize:none;overflow:hidden}
}
</style>
<div id="toolbar">
  <h1>🏫 ស្វ័យវាយតម្លៃ ២០២៦</h1>
  <div class="sep"></div>
  <input id="schoolInput" type="text" placeholder="ឈ្មោះ/លេខកូដសាលា…">
  <div class="sep"></div>
  <button class="tb g" onclick="fbSave()">💾 រក្សាទុក</button>
  <button class="tb b" onclick="fbLoad()">📥 ទាញយក</button>
  <div class="sep"></div>
  <button class="tb e" onclick="exportExcel()">📊 Excel</button>
  <button class="tb o" onclick="exportJSON()">📄 JSON</button>
  <label class="tb p" style="cursor:pointer">
    📤 Import JSON
    <input type="file" id="impFile" accept=".json" style="display:none" onchange="importJSON(event)">
  </label>
  <div class="sep"></div>
  <button class="tb s" onclick="window.print()">🖨️ Print</button>
  <div id="st" class="ok">✅ រួចរាល់</div>
</div>

<div id="tabs">
  <button class="tab active" onclick="switchTab('std1',this)">ស្តង់ដាទី១</button>
  <button class="tab" onclick="switchTab('std2',this)">ស្តង់ដាទី២</button>
  <button class="tab" onclick="switchTab('std3',this)">ស្តង់ដាទី៣</button>
  <button class="tab" onclick="switchTab('std4',this)">ស្តង់ដាទី៤</button>
  <button class="tab" onclick="switchTab('std5',this)">ស្តង់ដាទី៥</button>
  <button class="tab" id="tab-summary" onclick="switchTab('summary',this);buildSummary()">📊 សង្ខេបរួម</button>
</div>

<div id="content">
<div id="pane-std1" class="tab-pane active"><table class="std-table" data-std="std1" id="standard-1">
  <thead>
  <tr>
    <th rowspan="2"> <br>ល.រ </th>
    <th rowspan="2"> <br>ស្តង់ដានិងសូចនាករ </th>
    <th rowspan="2"> <br>កម្រិតផ្ទៀងផ្ទាត់សូចនាករ </th>
    <th colspan="5"> <br>កម្រិតផ្ទៀងផ្ទាត់លទ្ធផល </th>
    <th rowspan="2"> <br>ពិន្ទុ </th>
    <th rowspan="2"> <br>យោបល់ </th>
  </tr>
  <tr>
    <th> <br>ពិន្ទុ១ </th>
    <th> <br>ពិន្ទុ២ </th>
    <th> <br>ពិន្ទុ៣ </th>
    <th> <br>ពិន្ទុ៤ </th>
    <th> <br>ពិន្ទុ៥ </th>
  </tr></thead>
<tbody>
  <tr>
    <td colspan="10"> <br>ស្តង់ដាទី១ ៖ លទ្ធផលសិក្សារបស់សិស្ស (មាន៥ សូចនាករគន្លឹះ ១២ សូចនាកររង) </td>
  </tr>
  <tr>
    <td colspan="8"> <br>1.1 ការប្រមូលកុមារចូលរៀន </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td> <br>1.1.1 </td>
    <td> <br>ភាគរយកុមារថ្នាក់ទី១ចូលរៀនត្រឹមត្រូវតាមអាយុ </td>
    <td> <br>-  ស្ថិតិសិស្សថ្នាក់ទី១ ដែលមានអាយុ៦ឆ្នាំ ឬ ៧០ខែ និងស្ថិតិកុមារអាយុ៧ឆ្នាំឡើងទៅ នៅដើមឆ្នាំ </td>
    <td> <br>≤ ៩០ </td>
    <td> <br>&gt;៩០% </td>
    <td> <br>&gt;៩៥% </td>
    <td> <br>&gt;៩៧% </td>
    <td> <br>≥៩៩% </td>
    <td> <br>3 </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី១ នៃស្ដង់ដាទី១ </td>
    <td> <br>3 </td>
    <td> <br>60.00 </td>
  </tr>
  <tr>
    <td colspan="8"> <br>1.2 កុមាររៀនបានគង់វង្សក្នុងសាលារៀន </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td> <br>1.2.1 </td>
    <td> <br>អត្រាបោះបង់ការសិក្សា </td>
    <td> <br>-  របាយការណ៍ចុងឆ្នាំសិក្សា ដោយមានស្ថិតិសិស្សបោះបង់ការសិក្សា </td>
    <td> <br>≥៥% </td>
    <td> <br>&gt;៣% </td>
    <td> <br>&gt;២% </td>
    <td> <br>&gt;១% </td>
    <td> <br>≤១% </td>
    <td> <br>0 </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td> <br>1.2.2 </td>
    <td> <br>អត្រាត្រួតថ្នាក់ </td>
    <td> <br>-  របាយការណ៍ចុងឆ្នាំសិក្សា ដោយមានស្ថិតិសិស្សធ្លាក់មធ្យមភាគ និងដាក់ឱ្យរៀនត្រួតថ្នាក់ </td>
    <td> <br>≥១០% </td>
    <td> <br>&gt;៦% </td>
    <td> <br>&gt;៤% </td>
    <td> <br>&gt;២% </td>
    <td> <br>≤២% </td>
    <td> <br>0 </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី២ នៃស្ដង់ដាទី១ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>1.3 លទ្ធផលនៃការសិក្សារបស់សិស្ស </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td> <br>1.3.1 </td>
    <td> <br>ភាគរយសិស្សមាននិទ្ទេស A B និង C មុខវិជ្ជាភាសាខ្មែរ </td>
    <td> <br>-  របាយការណ៍នៃការធ្វើតេស្តចុងឆ្នាំសិក្សា ដោយបូកសរុបសិស្ស ថ្នាក់ទី១-៦ មាននិទ្ទេស A B និង C មុខវិជ្ជាភាសាខ្មែរ ចែកនឹង ចំនួនសិស្សសរុបក្នុងសាលារៀន </td>
    <td> <br>≤២០% </td>
    <td> <br>&gt;២០% </td>
    <td> <br>&gt;៤០% </td>
    <td> <br>&gt;៦០% </td>
    <td> <br>≥៨០% </td>
    <td> <br>0 </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td> <br>1.3.2 </td>
    <td> <br>ភាគរយសិស្សមាននិទ្ទេស A B និង C មុខវិជ្ជាគណិតវិទ្យា </td>
    <td> <br>-  របាយការណ៍នៃការធ្វើតេស្តចុងឆ្នាំសិក្សា ដោយបូកសរុប សិស្សថ្នាក់ទី១-៦ មាននិទ្ទេស A B និង C មុខវិជ្ជាគណិតវិទ្យា ចែកនឹងចំនួនសិស្សសរុបក្នុងសាលារៀន </td>
    <td> <br>≤២០% </td>
    <td> <br>&gt;២០% </td>
    <td> <br>&gt;៤០% </td>
    <td> <br>&gt;៦០% </td>
    <td> <br>≥៨០% </td>
    <td> <br>0 </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td> <br>1.3.3 </td>
    <td> <br>ភាគរយសិស្សថ្នាក់ទី៣ មានសមត្ថភាព អានតាមស្តង់ដា (៤៥ ទៅ ៦០ពាក្យ ក្នុងមួយនាទី) </td>
    <td> <br>-  របាយការណ៍នៃការប្រឡងអំណានចុងឆ្នាំសិក្សា ដោយបូកសរុប សិស្សថ្នាក់ទី៣ ដែលបានអានដោយល្បឿនចាប់ពី៤៥ពាក្យ/នាទី ឡើងទៅ ចែកនឹងចំនួនសិស្សថ្នាក់ទី៣សរុបក្នុងសាលារៀន </td>
    <td> <br>≤៥០% </td>
    <td> <br>&gt;៥០% </td>
    <td> <br>&gt;៦០% </td>
    <td> <br>&gt;៧០% </td>
    <td> <br>≥៨០% </td>
    <td> <br>0 </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td> <br>1.3.4 </td>
    <td> <br>ភាគរយសិស្សថ្នាក់ជាតិទី៦ មាន សមត្ថភាពអានតាមស្តង់ដា (១០០ ទៅ ១២០ពាក្យ ក្នុងមួយនាទី) </td>
    <td> <br>-  របាយការណ៍នៃការប្រឡងអំណានចុងឆ្នាំសិក្សា ដោយបូកសរុប សិស្សថ្នាក់ទី៦ ដែលបានអានដោយល្បឿនចាប់ពី១០០ពាក្យ/នាទី ឡើងទៅ ចែកនឹងចំនួនសិស្សថ្នាក់ទី៦សរុបក្នុងសាលារៀន </td>
    <td> <br>≤៥០% </td>
    <td> <br>&gt;៥០% </td>
    <td> <br>&gt;៦០% </td>
    <td> <br>&gt;៧០% </td>
    <td> <br>≥៨០% </td>
    <td> <br>0 </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី២ នៃស្ដង់ដាទី១ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>1.4 ស្ថានភាពអាហារូបត្ថម្ភ </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="2"> <br>1.4.1 </td>
    <td rowspan="2"> <br>ភាគរយសិស្សមានស្ថានភាព<br> <br>អាហារូបត្ថម្ភធម្មតា </td>
    <td> <br>-  បញ្ជីកត់ត្រាស្ថានភាពអាហារូបត្ថម្ភសិស្ស (អាយុ ទម្ងន់ កម្ពស់) </td>
    <td rowspan="2"> <br>≤៧០% </td>
    <td rowspan="2"> <br>&gt;៧០% </td>
    <td rowspan="2"> <br>&gt;៨០% </td>
    <td rowspan="2"> <br>&gt;៨៥% </td>
    <td rowspan="2"> <br>≥៩០% </td>
    <td rowspan="2"> <br>0 </td>
    <td rowspan="2"> <br><br> <br></td>
  </tr>
  <tr>
    <td> <br>-  សៀវភៅតាមដានសុខភាពសិស្សម្នាក់ៗ </td>
  </tr>
  <tr>
    <td rowspan="2"> <br>1.4.2 </td>
    <td rowspan="2"> <br>ភាគរយសិស្សដែលមានបញ្ហា<br> <br>អាហារូបត្ថម្ភទទួលបានកិច្ចអន្តរាគមន៍ </td>
    <td> <br>-  របាយការណ៍ត្រឡប់ពីមាតាបិតាឬអ្នកអាណាព្យាបាល ក្នុងការសហការជួយអន្តរាគមន៍ ឬការនាំកុមារទៅរក សេវាគាំទ្រ </td>
    <td rowspan="2"> <br>≤១៥% </td>
    <td rowspan="2"> <br>&gt;១៥% </td>
    <td rowspan="2"> <br>&gt;២០% </td>
    <td rowspan="2"> <br>&gt;៥០% </td>
    <td rowspan="2"> <br>≥៦០% </td>
    <td rowspan="2"> <br>0 </td>
    <td rowspan="2"> <br><br> <br></td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍ពីកិច្ចអន្តរាគមន៍របស់សេវាសុខាភិបាល មូលដ្ឋាន តាមរយៈគណៈកម្មការសុខភាពសិក្សា តាមសាលារៀន </td>
  </tr>
  <tr>
    <td> <br>1.4.3 </td>
    <td> <br>ភាគរយសិស្សក្រីក្រទទួលបានអាហា រូបករណ៍ ឬ ការឧបត្ថម្ភនានា </td>
    <td> <br>-  របាយការណ៍ស្តីពីការផ្តល់អាហារូបករណ៍របស់កម្មវិធីជាតិ ឬកម្មវិធីគាំទ្ររបស់ដៃគូអភិវឌ្ឍ </td>
    <td> <br>≤៧០% </td>
    <td> <br>&gt;៧០% </td>
    <td> <br>&gt;៨០% </td>
    <td> <br>&gt;៩០% </td>
    <td> <br>100% </td>
    <td> <br>0 </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៤ នៃស្ដង់ដាទី១ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>1.5 សីលធម៌និងឥរិយាបថសិស្ស </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="2"> <br>1.5.1 </td>
    <td rowspan="2"> <br>ភាគរយកុមារទទួលបានការប្រឹក្សា យោបល់ </td>
    <td> <br>-  របាយការណ៍អំពីចំនួនករណីហិង្សា ឬ វិបត្តិផ្លូវចិត្តនានា </td>
    <td rowspan="2"> <br>≤៥០% </td>
    <td rowspan="2"> <br>&gt;៥០% </td>
    <td rowspan="2"> <br>&gt;៦០% </td>
    <td rowspan="2"> <br>&gt;៧០% </td>
    <td rowspan="2"> <br>≥៨០% </td>
    <td rowspan="2"> <br>0 </td>
    <td rowspan="2"> <br><br> <br></td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍អំពីចំនួនកុមារដែលរងហិង្សា ឬ មានវិបត្តិផ្លូវចិត្ត បានទទួលប្រឹក្សាយោបល់ </td>
  </tr>
  <tr>
    <td rowspan="2"> <br>1.5.2 </td>
    <td rowspan="2"> <br>ភាគរយថ្នាក់រៀនដាក់ពិន្ទុ បំណិន សម្បទា និងចរិយាសម្បទាដល់សិស្ស ប្រចាំឆ្នាំ </td>
    <td> <br>-  របាយការណ៍អំពីចំនួនថ្នាក់រៀនដែលបានដាក់ពិន្ទុបំណិនសម្បទា និងចរិយាសម្បទាដល់សិស្ស ប្រចាំឆ្នាំ ធៀបជាមួយចំនួនថ្នាក់រៀនសរុប </td>
    <td rowspan="2"> <br>≤៥០% </td>
    <td rowspan="2"> <br>&gt;៥០% </td>
    <td rowspan="2"> <br>&gt;៧០% </td>
    <td rowspan="2"> <br>&gt;៩០% </td>
    <td rowspan="2"> <br>≥៩០% </td>
    <td rowspan="2"> <br>0 </td>
    <td rowspan="2"> <br><br> <br></td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយបញ្ជីពិន្ទុ សៀវភៅតាមដានការសិក្សា និងសៀវភៅសិក្ខាគារិក </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៥ នៃស្ដង់ដាទី១ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>សរុបពិន្ទុនិងភាគរយស្តង់ដាទី១៖ លទ្ធផលសិក្សារបស់សិស្ស (មាន៥ សូចនាករគន្លឹះ ១២ សូចនាកររង) </td>
    <td> <br>0 </td>
    <td> <br>0.00 </td>
  </tr>
</tbody></table></div>
<div id="pane-std2" class="tab-pane "><table class="std-table" data-std="std2" id="tpl-standat2">
  <thead>
  <tr>
    <th rowspan="2"> <br>ល.រ </th>
    <th rowspan="2"> <br>ស្តង់ដានិងសូចនាករ</th>
    <th rowspan="2"> <br>កម្រិតផ្ទៀងផ្ទាត់សូចនាករ </th>
    <th colspan="5"> <br>កម្រិតផ្ទៀងផ្ទាត់លទ្ធផល </th>
    <th rowspan="2"> <br>ពិន្ទុ </th>
    <th rowspan="2"> <br>យោបល់ </th>
  </tr>
  <tr>
    <td> <br>ពិន្ទុ១ </td>
    <td> <br>ពិន្ទុ២ </td>
    <td> <br>ពិន្ទុ៣ </td>
    <td> <br>ពិន្ទុ៤ </td>
    <td> <br>ពិន្ទុ៥ </td>
  </tr></thead>
  <tbody><tr>
    <th colspan="10" style="text-align: left;">ស្តង់ដាទី២៖ ការបង្រៀននិងរៀន (១០សូចនាករគន្លឹះ និង ២៩សូចនាកររង) </th>
  </tr>
</tbody><tbody>
  <tr>
    <td colspan="8"> <br>2.1- ការអនុវត្តវិធីសាស្ត្របង្រៀន </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.1.1 </td>
    <td rowspan="3"> <br>ភាគរយគ្រូបង្រៀនថ្នាក់ទី១ និង/ឬ ទី២ និង/ឬ ទី៣ អនុវត្តកញ្ចប់<br> <br>សម្ភារៈអំណាន ថ្នាក់ដំបូង កម្រិត ២ និង៣ </td>
    <td> <br>-  របាយការណ៍សង្កេតការបង្រៀន គ្រូបង្រៀនថ្នាក់ទី១ និង/ឬ ទី២ និង/ឬ ទី៣ ស្តីពីអនុវត្តកញ្ចប់សម្ភារៈ អំណានថ្នាក់ដំបូង </td>
    <td rowspan="3"> <br>≤ ៦០% </td>
    <td rowspan="3"> <br>&gt;៦០% </td>
    <td rowspan="3"> <br>&gt;៧០% </td>
    <td rowspan="3"> <br>&gt;៨០% </td>
    <td rowspan="3"> <br>≥៩០% </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍បូកសរុបលទ្ធផលសង្កេតការបង្រៀន ដោយចំនួនគ្រូបង្រៀនថ្នាក់ទី១ និង/ឬ ទី២ និង/ឬ ទី៣ អនុវត្ត កញ្ចប់ សម្ភារៈអំណានថ្នាក់ដំបូង កម្រិតទី២និង៣ ចែកនឹងគ្រូ បង្រៀន ថ្នាក់ទី១ និង/ឬ ទី២ និង/ឬ ទី៣ សរុប </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ទិន្នន័យតាមរយៈប្រព័ន្ធ KOBO របស់កម្មវិធីប្រឹក្សា គរុកោសល្យ </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.1.2 </td>
    <td rowspan="3"> <br>ភាគរយគ្រូបង្រៀនថ្នាក់ទី១ និង/ឬ ទី២ និង/ឬ ទី៣ អនុវត្តកញ្ចប់<br> <br>សម្ភារៈ គណិតវិទ្យាថ្នាក់ដំបូង កម្រិត ២ និង៣ </td>
    <td> <br>-  របាយការណ៍សង្កេតការបង្រៀន គ្រូបង្រៀនថ្នាក់ទី១ និង/ឬ ទី២ និង/ឬ ទី៣ ស្តីពីអនុវត្តកញ្ចប់សម្ភារៈគណិតវិទ្យាថ្នាក់ដំបូង </td>
    <td rowspan="3"> <br>≤ ៦០% </td>
    <td rowspan="3"> <br>&gt;៦០% </td>
    <td rowspan="3"> <br>&gt;៧០% </td>
    <td rowspan="3"> <br>&gt;៨០% </td>
    <td rowspan="3"> <br>≥៩០% </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍បូកសរុបលទ្ធផលសង្កេតការបង្រៀន ដោយចំនួន គ្រូបង្រៀនថ្នាក់ទី១ និង/ឬ ទី២ និង/ឬ ទី៣ អនុវត្តកញ្ចប់ សម្ភារៈគណិតវិទ្យាថ្នាក់ដំបូង កម្រិតទី២និង៣ ចែកនឹងគ្រូ បង្រៀនថ្នាក់ទី១ និង/ឬ ទី២ និង/ឬ ទី៣ សរុប </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ទិន្នន័យតាមរយៈប្រព័ន្ធ KOBO របស់កម្មវិធីប្រឹក្សា គរុកោសល្យ </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.1.3 </td>
    <td rowspan="3"> <br>ភាគរយគ្រូបង្រៀនចូលរៀនវគ្គអភិវឌ្ឍសមត្ថភាពប្រចាំឆ្នាំ (កញ្ចប់សម្ភារៈ អំណាននិងគណិតវិទ្យាថ្នាក់ដំបូង ការប្រឹក្សាគរុកោសល្យ វិធីសាស្ត្រ បង្រៀននានា ការអប់រំ <br> <br>វិន័យបែបវិជ្ជមាន វិធីសាស្ត្រអំណានក្នុងបណ្ណាល័យ...) </td>
    <td> <br>-  របាយការណ៍លទ្ធផលនៃការបណ្តុះបណ្តាល ឬ បំប៉ន សមត្ថភាព គ្រូបង្រៀនទាំងអស់ក្នុងសាលា/ឆ្នាំសិក្សា </td>
    <td rowspan="3"> <br>≤២០% </td>
    <td rowspan="3"> <br>&gt;២០% </td>
    <td rowspan="3"> <br>&gt;៤០% </td>
    <td rowspan="3"> <br>&gt;៦០% </td>
    <td rowspan="3"> <br>≥៨០% </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍បូកសរុបលទ្ធផលនៃការបណ្តុះបណ្តាល ឬ បំប៉ន សមត្ថភាព ចែកនឹងចំនួនគ្រូបង្រៀនសរុបក្នុងសាលា </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយនឹងការសាកសួរសាមីខ្លួន និងវិញ្ញាបនបត្រ បញ្ជាក់ការសិក្សា </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>2.1.4 </td>
    <td rowspan="4"> <br>ចំនួនកិច្ចការជាគម្រោង ដែលគ្រូ ថ្នាក់ទី៤-៦ បានដាក់ឱ្យសិស្សអនុវត្ត ក្នុងមួយឆ្នាំ (គិតជាមធ្យម ក្នុងថ្នាក់ /សាលា) </td>
    <td> <br>-  របាយការណ៍ស្តីពីការដាក់កិច្ចការជាគម្រោងឱ្យសិស្សធ្វើរបស់គ្រូបង្រៀនម្នាក់ៗ </td>
    <td rowspan="4"> <br>≤២ </td>
    <td rowspan="4"> <br>&gt;២ </td>
    <td rowspan="4"> <br>&gt;៤ </td>
    <td rowspan="4"> <br>&gt;៦ </td>
    <td rowspan="4"> <br>≥៨ </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  សន្លឹកកិច្ចការ ឬ បទបង្ហាញ ឬ ឯកសារដែលសិស្សសិក្សាស្រាវជ្រាវ </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសកម្មភាពស្រាវជ្រាវក្នុងបណ្ណាល័យ </td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍ចុងឆ្នាំរបស់សាលារៀន </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.1.5 </td>
    <td rowspan="3"> <br>ភាគរយសិស្សបានធ្វើកិច្ចការផ្ទះតាម មេរៀននៃមុខវិជ្ជាភាសាខ្មែរ និងគណិតវិទ្យា និងមានការកែពីគ្រូ </td>
    <td> <br>-  របាយការណ៍របស់គ្រូប្រចាំថ្នាក់ម្នាក់ៗ ប្រចាំសប្តាហ៍ ប្រចាំខែ ត្រីមាស ឆមាស និងឆ្នាំ </td>
    <td rowspan="3"> <br>≤៥០% </td>
    <td rowspan="3"> <br>&gt;៥០% </td>
    <td rowspan="3"> <br>&gt;៦៥% </td>
    <td rowspan="3"> <br>&gt;៨០% </td>
    <td rowspan="3"> <br>≥៩០% </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍បូកសរុបរបស់សាលារៀន ប្រចាំខែ ត្រីមាស ឆមាស និងឆ្នាំ </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសិស្សម្នាក់ៗ តាមរយៈការបញ្ជាក់ពីសិស្សានុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី១ នៃស្ដង់ដាទី២ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>2.2 ការអនុវត្តកម្មវិធីសិក្សានិងការរៀបចំផែនការបង្រៀន </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.2.1 </td>
    <td rowspan="3"> <br>ភាគរយថ្នាក់រៀនដែលមានបំណែងចែកកម្មវិធីសិក្សាគ្រប់មុខវិជ្ជាសិក្សាគោល </td>
    <td> <br>-  របាយការណ៍របស់គ្រូប្រចាំថ្នាក់នីមួយៗ </td>
    <td rowspan="3"> <br>≤៨០% </td>
    <td rowspan="3"> <br>&gt; ៨០% </td>
    <td rowspan="3"> <br>&gt;៩០% </td>
    <td rowspan="3"> <br>&gt;៩៥% </td>
    <td rowspan="3"> <br>100% </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍បូកសរុបរបស់សាលារៀន </td>
  </tr>
  <tr>
    <td> <br>-  បំណែងចែកកម្មវិធីសិក្សា ដែលមានព្យួរនៅលើតារាងកម្មវិធីសក្សា ឬ រក្សាទុកនៅទីចាត់ការ </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.2.2 </td>
    <td rowspan="3"> <br>ភាគរយគ្រូដែលបានរៀបចំកិច្ចតែងការបង្រៀនថ្មី ឬ បានធ្វើបច្ចុប្បន្នកម្ម គ្រប់មេរៀន និងគ្រប់មុខវិជ្ជា </td>
    <td> <br>-  របាយការណ៍បូកសរុបស្តីពីការរៀបចំកិច្ចតែងការបង្រៀន របស់សាលារៀន </td>
    <td rowspan="3"> <br>≤៥០% </td>
    <td rowspan="3"> <br>&gt; ៥០% </td>
    <td rowspan="3"> <br>&gt;៧០% </td>
    <td rowspan="3"> <br>&gt;៨៥% </td>
    <td rowspan="3"> <br>≥៩៥% </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  សៀវភៅកិច្ចតែងការបង្រៀនរបស់គ្រូបង្រៀនម្នាក់ៗ ដែលមាន យ៉ាងតិច ៤មុខវិជ្ជា </td>
  </tr>
  <tr>
    <td> <br>-  កិច្ចតែងការនីមួយៗ ត្រូវមានការចុះទិដ្ឋាការទទួលស្គាល់ដោយ នាយកសាលា ឬ នាយករងទទួលបន្ទុកបច្ចេកទេស </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.2.3 </td>
    <td rowspan="3"> <br>ចំនួនដងថ្នាក់រៀនបិទទ្វារ (សរុបថ្នាក់ ទាំងអស់គិតជាមធ្យម) </td>
    <td> <br>-  របាយការណ៍បូកសរុបបញ្ជីគ្រប់គ្រងវត្តមាន របស់សាលារៀន </td>
    <td rowspan="3"> <br>≥៥ </td>
    <td rowspan="3"> <br>&gt;៣ </td>
    <td rowspan="3"> <br>&gt;២ </td>
    <td rowspan="3"> <br>&gt;១ </td>
    <td rowspan="3"> <br>≤១ </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  បញ្ជីវត្តមានប្រចាំថ្ងៃ </td>
  </tr>
  <tr>
    <td> <br>-  ការបញ្ជាក់ពីក្រុមប្រឹក្សាកុមារ ឬ សិស្សានុសិស្ស និងពីប្រភព ផ្សេងៗទៀត </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.2.4 </td>
    <td rowspan="3"> <br>ចំនួនថ្ងៃសាលាបិទទ្វារមិនតាមប្រតិទិនសិក្សាប្រចាំឆ្នាំ </td>
    <td> <br>-  របាយការណ៍បូកសរុបបញ្ជីគ្រប់គ្រងវត្តមានរបស់សាលារៀន </td>
    <td rowspan="3"> <br>≥៥ </td>
    <td rowspan="3"> <br>&gt;៣ </td>
    <td rowspan="3"> <br>&gt;២ </td>
    <td rowspan="3"> <br>&gt;១ </td>
    <td rowspan="3"> <br>≤១ </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  បញ្ជីវត្តមានប្រចាំថ្ងៃ </td>
  </tr>
  <tr>
    <td> <br>-  ការបញ្ជាក់ពីក្រុមប្រឹក្សាកុមារ ឬ សិស្សានុសិស្ស និងពីប្រភពផ្សេងៗទៀត </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>2.2.5 </td>
    <td rowspan="4"> <br>ភាគរយថ្នាក់ទី៤ -៦ បានបង្រៀនភាសា បរទេស </td>
    <td> <br>-  របាយការណ៍បូកសរុបស្តីពីការបង្រៀនភាសាបរទេសរបស់សាលារៀន </td>
    <td rowspan="4"> <br>≤៥០% </td>
    <td rowspan="4"> <br>&gt; ៥០% </td>
    <td rowspan="4"> <br>&gt;៧០% </td>
    <td rowspan="4"> <br>&gt;៨៥% </td>
    <td rowspan="4"> <br>≥៩៥% </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  បំណែងចែកកាលវិភាគ និងភារកិច្ចរបស់គ្រូបង្រៀន </td>
  </tr>
  <tr>
    <td> <br>-  មានបញ្ចូលពិន្ទុភាសាបរទេសក្នុងបញ្ជីពិន្ទុ សៀវភៅតាមដានការសិក្សា និងសៀវភៅសិក្ខាគារិកជាដើម </td>
  </tr>
  <tr>
    <td> <br>-  ការបញ្ជាក់ពីសិស្សានុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>2.2.6 </td>
    <td rowspan="4"> <br>ភាគរយថ្នាក់ទី៤-៦បានបង្រៀនមេរៀន បំណិនជីវិតមូលដ្ឋាន </td>
    <td> <br>-  របាយការណ៍បូកសរុបស្តីពីការបង្រៀនបំណិនជីវិតមូលដ្ឋានរបស់សាលារៀន </td>
    <td rowspan="4"> <br>≤៥០% </td>
    <td rowspan="4"> <br>&gt; ៥០% </td>
    <td rowspan="4"> <br>&gt;៧០% </td>
    <td rowspan="4"> <br>&gt;៨៥% </td>
    <td rowspan="4"> <br>≥៩៥% </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  បំណែងចែកកាលវិភាគ និងមេរៀនដែលត្រូវបង្រៀនសិស្ស </td>
  </tr>
  <tr>
    <td> <br>-  មានបញ្ចូលពិន្ទុភាសាបរទេសក្នុងបញ្ជីពិន្ទុ សៀវភៅតាមដានការសិក្សា និងសៀវភៅសិក្ខាគារិកជាដើម </td>
  </tr>
  <tr>
    <td> <br>-  ការបញ្ជាក់ពីសិស្សានុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>2.2.7 </td>
    <td rowspan="4"> <br>ភាគរយសិស្សអវត្តមានលើស៤ដងក្នុងមួយឆ្នាំសិក្សា </td>
    <td> <br>-  របាយការណ៍បូកសរុបស្តីពីសិស្សអវត្តមានប្រចាំឆ្នាំរបស់ សាលារៀន </td>
    <td rowspan="4"> <br>≥១០% </td>
    <td rowspan="4"> <br>&gt;៧% </td>
    <td rowspan="4"> <br>&gt;៤% </td>
    <td rowspan="4"> <br>&gt;១% </td>
    <td rowspan="4"> <br>≤១% </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  បញ្ជីហៅឈ្មោះសិស្សរបស់ថ្នាក់រៀននីមួយៗ </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយចំនួនវត្តមានរបស់សិស្សម្នាក់ៗ ជាមួយ សៀវភៅតាមដានការសិក្សា និងសៀវភៅសិក្ខាគារិកជាដើម </td>
  </tr>
  <tr>
    <td> <br>-  ការបញ្ជាក់ពីសិស្សានុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី២ នៃស្ដង់ដាទី២ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>2.3 សម្ភារៈរៀននិងបង្រៀន </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="2"> <br>2.3.1 </td>
    <td rowspan="2"> <br>ភាគរយសិស្សមានសៀវភៅសិក្សា គោលតាមនិយាម </td>
    <td> <br>-  របាយការណ៍ស្ថិតិសៀវភៅសិក្សាគោលដែលសាលាប្រមូលបានពីសិស្សឆ្នាំចាស់ និងសៀវភៅដែលទទួលបានឆ្នាំថ្មី ធៀបនឹងចំនួន សិស្សតាមកម្រិតថ្នាក់ តាមមុខវិជ្ជា </td>
    <td rowspan="2"> <br>≤៩០% </td>
    <td rowspan="2"> <br>&gt;៩០% </td>
    <td rowspan="2"> <br>&gt;៩៥% </td>
    <td rowspan="2"> <br>&gt;៩៨% </td>
    <td rowspan="2"> <br>100% </td>
    <td rowspan="2"> <br>0 </td>
    <td rowspan="2"> <br><br> <br></td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសិស្សម្នាក់ៗ តាមរយៈការបញ្ជាក់ពី សិស្សានុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.3.2 </td>
    <td rowspan="3"> <br>ភាគរយសិស្សថ្នាក់ទី១ និង/ឬ ទី២ និង/ឬ ទី៣ មានកញ្ចប់សម្ភារៈអំណាន និងគណិតវិទ្យាថ្នាក់ដំបូង ដែលមាតា បិតាទិញឱ្យ </td>
    <td> <br>-  របាយការណ៍ប្រជុំណែនាំមាតាបិតា អ្នកអាណាព្យាបាលសិស្ស មុនដំណើរការឆ្នាំសិក្សាថ្មី </td>
    <td rowspan="3"> <br>≤៨០% </td>
    <td rowspan="3"> <br>&gt;៨០% </td>
    <td rowspan="3"> <br>&gt;៩០% </td>
    <td rowspan="3"> <br>&gt;៩៥% </td>
    <td rowspan="3"> <br>100% </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍របស់គ្រូបង្រៀនកម្រិតថ្នាក់ដំបូង អំពីចំនួនសិស្ស ដែលទិញកញ្ចប់សម្ភារៈអំណាន និងគណិតវិទ្យាថ្នាក់ដំបូង </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសិស្សម្នាក់ៗ តាមរយៈការបញ្ជាក់ពីសិស្សា នុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.3.3 </td>
    <td rowspan="3"> <br>ភាគរយគ្រូបង្រៀនផលិតនិងប្រើប្រាស់សម្ភារឧបទេសជាប្រចាំ </td>
    <td> <br>-  របាយការណ៍របស់គ្រូបង្រៀនម្នាក់ៗ អំពីចំនួនសិស្សដែលទិញ កញ្ចប់សម្ភារៈអំណាន និងគណិតវិទ្យាថ្នាក់ដំបូង </td>
    <td rowspan="3"> <br>≤៦០% </td>
    <td rowspan="3"> <br>&gt;៦០% </td>
    <td rowspan="3"> <br>&gt;៧០% </td>
    <td rowspan="3"> <br>&gt;៨០% </td>
    <td rowspan="3"> <br>≥៩៥% </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយវីដេអូ ឬ រូបថតនៃសកម្មភាពផលិត និងប្រើប្រាស់ សម្ភារឧបទេស និងសម្ភារដែលផលិតហើយបានរក្សាទុក សម្រាប់ ប្រើប្រាស់មេរៀនផ្សេងទៀត ឬ ឆ្នាំសិក្សាបន្ទាប់ </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសិស្សម្នាក់ៗ តាមរយៈការបញ្ជាក់ពី សិស្សានុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.3.4 </td>
    <td rowspan="3"> <br>ភាគរយគ្រូបង្រៀនប្រើប្រាស់បច្ចេកវិទ្យាបម្រើឱ្យការរៀននិងបង្រៀន </td>
    <td> <br>-  របាយការណ៍របស់សាលារៀន អំពីបន្ទប់រៀនដែលបំពាក់ឧបករណ៍ បច្ចេកវិទ្យាបម្រើឱ្យការៀននិងបង្រៀន </td>
    <td rowspan="3"> <br>≤២០% </td>
    <td rowspan="3"> <br>&gt;២០% </td>
    <td rowspan="3"> <br>&gt;៣០% </td>
    <td rowspan="3"> <br>&gt;៤០% </td>
    <td rowspan="3"> <br>≥៥០% </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  ចំនួនគ្រូបង្រៀនដែលមានកុំព្យូទ័រយួរដៃ ឬ លើតុ ឬ ថេប្លេត សម្រាប់ប្រើប្រាស់បម្រើឱ្យការបង្រៀននិងរៀន </td>
  </tr>
  <tr>
    <td> <br>-  ចំនួនគ្រូបង្រៀនដែលមានសមត្ថភាពប្រើប្រាស់កម្មវិធីកុំព្យូទ័រ សម្រាប់រៀបចំខ្លឹមសារមេរៀន </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៣ នៃស្ដង់ដាទី២ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>2.4 ការជួយគាំទ្រសិស្ស </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.4.1 </td>
    <td rowspan="3"> <br>ភាគរយសិស្សនិងមាតាបិតាបានចុះកិច្ច ព្រមព្រៀងរៀនសូត្រប្រចាំឆ្នាំជាមួយគ្រូ </td>
    <td> <br>-  របាយការណ៍របស់សាលារៀនស្តីពីចំនួនមាតាបិតា អ្នកអាណាព្យាបាលចុះកិច្ចព្រមព្រៀងលើការរៀនសូត្ររបស់កូនៗប្រចាំឆ្នាំ </td>
    <td rowspan="3"> <br>≤ ៣០% </td>
    <td rowspan="3"> <br>&gt;៣០% </td>
    <td rowspan="3"> <br>&gt;៤០% </td>
    <td rowspan="3"> <br>&gt;៥០% </td>
    <td rowspan="3"> <br>≥៦០% </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  កិច្ចព្រមព្រៀងដែលគ្រូប្រចាំថ្នាក់នីមួយៗរក្សាទុក </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសិស្សម្នាក់ៗ តាមរយៈការបញ្ជាក់ពីសិស្សានុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td rowspan="2"> <br>2.4.2 </td>
    <td rowspan="2"> <br>ភាគរយថ្នាក់រៀនមានការប្រជុំជាមួយ មាតាបិតា ពិនិត្យតាមដានការរៀនសូត្រ ទៀងទាត់ </td>
    <td> <br>-  របាយការណ៍របស់សាលារៀនស្តីពីការប្រជុំរវាងគ្រូប្រចាំថ្នាក់ និងមាតាបិតា អ្នកអាណាព្យាបាល ដើម្បីពិភាក្សាអំពីការសិក្សារបស់កូនៗ ប្រចាំឆ្នាំ </td>
    <td rowspan="2"> <br>≤ ៨០% </td>
    <td rowspan="2"> <br>&gt;៨០% </td>
    <td rowspan="2"> <br>&gt;៩០% </td>
    <td rowspan="2"> <br>&gt;៩៥% </td>
    <td rowspan="2"> <br>100% </td>
    <td rowspan="2"> <br>0 </td>
    <td rowspan="2"> <br><br> <br></td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសិស្សម្នាក់ៗ តាមរយៈការបញ្ជាក់ពីសិស្សានុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td rowspan="2"> <br>2.4.3 </td>
    <td rowspan="2"> <br>ភាគរយយសិស្សរៀនយឺតបានទទួល ការជួយប្រចាំខែ ផ្អែកតាមលទ្ធផល តេស្តស្តង់ដាប្រចាំខែ </td>
    <td> <br>-  របាយការណ៍របស់សាលារៀនស្តីពីការជួយសិស្សរៀនយឺតរបស់គ្រូប្រចាំថ្នាក់ ឬ គ្រូបង្រៀនស្ម័គ្រចិត្តជួយបង្រៀនសិស្សរៀនយឺតក្រៅម៉ោងសិក្សា </td>
    <td rowspan="2"> <br>≤ ៥០% </td>
    <td rowspan="2"> <br>&gt;៥០% </td>
    <td rowspan="2"> <br>&gt;៦៥% </td>
    <td rowspan="2"> <br>&gt;៧៥% </td>
    <td rowspan="2"> <br>≥ ៩០% </td>
    <td rowspan="2"> <br>0 </td>
    <td rowspan="2"> <br><br> <br></td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសិស្សម្នាក់ៗ តាមរយៈការបញ្ជាក់ពីសិស្សានុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៤ នៃស្ដង់ដាទី២ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>2.5 ដំណើរការបណ្ណាល័យ </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.5.1 </td>
    <td rowspan="3"> <br>ចំនួនសៀវភៅដែលសិស្សម្នាក់ៗ ខ្ចី-សង ក្នុងមួយឆ្នាំ </td>
    <td> <br>-  របាយការណ៍របស់បណ្ណារក្ស និងសាលារៀនអំពីចំនួនសៀវភៅ ដែលសិស្សម្នាក់ៗ ខ្ចី-សង ក្នុងមួយឆ្នាំ </td>
    <td rowspan="3"> <br>≤១០ </td>
    <td rowspan="3"> <br>&gt;១០ </td>
    <td rowspan="3"> <br>&gt;២០ </td>
    <td rowspan="3"> <br>&gt;២៥ </td>
    <td rowspan="3"> <br>≥៣០ </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  បញ្ជីកត់ត្រាសៀវភៅ ខ្ចី-សង នៅក្នុងបណ្ណាល័យ </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសិស្សម្នាក់ៗ តាមរយៈការបញ្ជាក់ពីសិស្សានុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.5.2 </td>
    <td rowspan="3"> <br>ចំនួនដង គ្រូបង្រៀនម្នាក់ៗក្នុងមួយឆ្នាំ នាំសិស្សចូលបណ្ណាល័យអនុវត្ត សកម្មភាពអានដោយប្រើប្រាស់វិធីសាស្ត្រអំណាន </td>
    <td> <br>-  ថ្នាក់រៀននីមួយៗ មានកាលវិភាគបញ្ជាក់អំពីម៉ោងដែលសិស្សចូល បណ្ណាល័យ </td>
    <td rowspan="3"> <br>≤១០ </td>
    <td rowspan="3"> <br>&gt;១០ </td>
    <td rowspan="3"> <br>&gt;២០ </td>
    <td rowspan="3"> <br>&gt;២៥ </td>
    <td rowspan="3"> <br>≥៣០ </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍របស់បណ្ណារក្ស និងសាលារៀនអំពីចំនួនគ្រូប្រចាំ ថ្នាក់ម្នាក់ៗ ដឹកនាំសិក្សចូលអានសៀវភៅក្នុងបណ្ណាល័យ ដោយបញ្ជាក់អំពីការអនុវត្តសកម្មភាពអំណាន ដោយប្រើប្រាស់ វិធីសាស្ត្រអំណានក្នុងបណ្ណាល័យ ក្នុងមួយឆ្នាំ </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសិស្សម្នាក់ៗ តាមរយៈការបញ្ជាក់ពីសិស្សា នុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៥ នៃស្ដង់ដាទី២ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>2.6 ការធ្វើអធិការកិច្ចផ្ទៃក្នុង </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>2.6.1 </td>
    <td rowspan="4"> <br>ភាគរយគ្រូបង្រៀនទទួលបានការផ្ដល់ប្រឹក្សាគរុកោសល្យ/អធិការកិច្ចថ្នាក់រៀន យ៉ាងតិចម្តង/ខែ </td>
    <td> <br>-  សាលារៀនមានលិខិតបង្គាប់ការចាត់តាំងគ្រូបង្រៀន និង/ឬនាយករងទទួលបន្ទុកបច្ចេកទេស ជាទីប្រឹក្សាគរុកោសល្យ </td>
    <td rowspan="4"> <br>≤ ៥០% </td>
    <td rowspan="4"> <br>&gt;៥០% </td>
    <td rowspan="4"> <br>&gt;៦០% </td>
    <td rowspan="4"> <br>&gt;៧៥% </td>
    <td rowspan="4"> <br>≥៩០% </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  ទីប្រឹក្សាគរុកោសល្យម្នាក់ៗ មានផែនការចុះជួយគ្រូបង្រៀនផ្សេង ទៀតក្នងសាលា ឬ កម្រងសាលារៀន </td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍ស្តីពីការចុះផ្តល់ប្រឹក្សាគរុកោសល្យ/អធិការកិច្ចថ្នាក់ រៀន ប្រចាំខែ </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ទិន្នន័យតាមរយៈប្រព័ន្ធ KOBO របស់កម្មវិធីប្រឹក្សាគរុកោសល្យ </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៦ នៃស្ដង់ដាទី២ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>2.7 ការប្រជុំបច្ចេកទេស </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="2"> <br>2.7.1 </td>
    <td rowspan="2"> <br>ចំនួនដងសាលារៀនរៀបចំប្រជុំបច្ចេកទេស </td>
    <td> <br>-  សាលារៀនមានរៀបចំផែនការស្តីពីការប្រជុំបច្ចេកទេស តាមការណែនាំរបស់ក្រសួង ឬ មន្ទីរ </td>
    <td rowspan="2"> <br>≤ ៥ </td>
    <td rowspan="2"> <br>&gt;៥ </td>
    <td rowspan="2"> <br>&gt;៧ </td>
    <td rowspan="2"> <br>&gt;៩ </td>
    <td rowspan="2"> <br>≥ ៩ </td>
    <td rowspan="2"> <br>0 </td>
    <td rowspan="2"> <br><br> <br></td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍ស្តីពីការប្រជុំបច្ចេកទេសប្រចាំខែ ឬ តាមផែនការ </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៧ នៃស្ដង់ដាទី២ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>2.8 ការអនុវត្តកម្មវិធីសិក្សាក្រៅម៉ោង </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>2.8.1 </td>
    <td rowspan="4"> <br>ចំនួនដងប្រកួតប្រជែងអំណាន និងធ្វើ លំហាត់គណិតវិទ្យា ក្នុងមួយឆ្នាំ </td>
    <td> <br>-  សាលារៀនមានរៀបចំផែនការស្តីពីការប្រកួតប្រជែងអំណាន និងធ្វើលំហាត់ គណិតវិទ្យាប្រចាំឆ្នាំ </td>
    <td rowspan="4"> <br>≤ ២ </td>
    <td rowspan="4"> <br>&gt;២ </td>
    <td rowspan="4"> <br>&gt; ៥ </td>
    <td rowspan="4"> <br>&gt; ៨ </td>
    <td rowspan="4"> <br>≥ ១០ </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  នាយកសាលារៀបចំយន្តការ និងចេញលិខិតបង្គាប់ការគ្រូបង្រៀន ឬ បុគ្គលិកអប់រំឱ្យទទួលបន្ទុកសម្របសម្រួលការប្រកួតប្រជែង ឬ ប្រឡងប្រណាំងនានា </td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍ស្តីពីស្តីពីការប្រកួតប្រជែងអំណាន និងធ្វើលំហាត់ គណិតវិទ្យាប្រចាំឆ្នាំ </td>
  </tr>
  <tr>
    <td> <br>-  លទ្ធផល និងជ័យលាភីដែលសិស្សានុសិស្សទទួលបាន </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>2.8.2 </td>
    <td rowspan="4"> <br>ចំនួនក្លឹបសិក្សាបានបង្កើតដើម្បីជួយ សិស្សរៀនយឺត និងជួយការងារផ្សេងៗ របស់សាលា </td>
    <td> <br>-  របាយការណ៍ក្រុមប្រឹក្សាកុមារប្រចាំសប្តាហ៍ និងខែ </td>
    <td rowspan="4"> <br>≤៥ </td>
    <td rowspan="4"> <br>&gt;៥ </td>
    <td rowspan="4"> <br>&gt; ១០ </td>
    <td rowspan="4"> <br>&gt; ១៥ </td>
    <td rowspan="4"> <br>≥ ២០ </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍របស់គ្រូប្រចាំថ្នាក់ម្នាក់ៗ ប្រចាំខែ ត្រីមាស ឆមាស និងឆ្នាំ </td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍បូកសរុបរបស់សាលារៀន ត្រីមាស ឆមាស និងឆ្នាំ </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសិស្សម្នាក់ៗ តាមរយៈការបញ្ជាក់ពីសិស្សានុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>2.8.3 </td>
    <td rowspan="4"> <br>ចំនួនដងសិស្សានុសិស្សបានចុះទស្សនកិច្ចសិក្សានៅតាមទីកន្លែងនានា ក្នុង មួយឆ្នាំសិក្សា </td>
    <td> <br>-  សាលារៀនមានរៀបចំផែនការស្តីពីកម្មវិធីទស្សនកិច្ច ទាំងក្នុងមូលដ្ឋាន និងតាមទីកន្លែងប្រវត្តិសាស្ត្រ សារៈមន្ទីរ ឬ តំបន់ទេសចរណ៍នានា </td>
    <td rowspan="4"> <br>≤១ </td>
    <td rowspan="4"> <br>&gt;១ </td>
    <td rowspan="4"> <br>&gt; ២ </td>
    <td rowspan="4"> <br>&gt; ៣ </td>
    <td rowspan="4"> <br>≥ ៥ </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  គ្រូប្រចាំថ្នាក់នីមួយៗរៀបចំផែនការទស្សនកិច្ចប្រចាំឆ្នាំ ផ្អែកតាមការពិភាក្សាជាមួយគណៈកម្មការគ្រប់គ្រងថ្នាក់រៀន និងមាតាបិតា អ្នកអាណាព្យាបាល </td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍បូកសរុបលទ្ធផលទស្សនកិច្ច </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសិស្សម្នាក់ៗ តាមរយៈការបញ្ជាក់ពីសិស្សានុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៨ នៃស្ដង់ដាទី២ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>2.9 ការអនុវត្តការអប់រំសីលធម៌ ចរិយាធម៌ </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>2.9.1 </td>
    <td rowspan="4"> <br>សាលារៀនមានកម្មវិធីលើកកម្ពស់ចរិយាធម៌(ស្អាត សុភាព របៀប ទៀងពេល និងសមាធិ) </td>
    <td> <br>-  សាលារៀនមានរៀបចំផែនការស្តីពីការលើកកម្ពស់ចរិយាធម៌ និងផ្សព្វផ្សាយឱ្យបានទូលំទូលាយ និងជាប្រចាំ </td>
    <td rowspan="4"> <br>មាន១/៥ </td>
    <td rowspan="4"> <br>មាន២/៥ </td>
    <td rowspan="4"> <br>មាន៣/៥ </td>
    <td rowspan="4"> <br>មាន៤/៥ </td>
    <td rowspan="4"> <br>មានទាំងអស់ </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍ស្តីពីការអនុវត្ត និងការពិនិត្យតាមដាន និងជំរុញការ អនុវត្ត </td>
  </tr>
  <tr>
    <td> <br>-  បញ្ជីពិន្ទុ សៀវភៅតាមដានការសិក្សា និងសៀវភៅសិក្ខាគារិក មានការផ្តល់ពិន្ទុលើការអប់រំចរិយាធម៌ </td>
  </tr>
  <tr>
    <td> <br>-  សិស្សានុសិស្សបង្ហាញការអនុវត្តជាក់ស្តែងទាំងនៅក្នុងសាលា នៅផ្ទះ និងតាមទីកន្លែងនានា </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>2.9.2 </td>
    <td rowspan="3"> <br>ចំនួនដងព្រះសង្ឃនិមន្តមកផ្តល់ធម៌ ទេសនាអប់រំ ក្នុងមួយឆ្នាំ </td>
    <td> <br>-  សាលារៀនមានរៀបចំផែនការស្តីពីការនិមន្តព្រះសង្ឃ ឬ អញ្ជើញចាស់ព្រឹទ្ធាចារ្យ ផ្តល់ធម៌ទេសនា ឬ ការអប់រំ ប្រចាំឆ្នាំ ដោយរំលេចប្រធានបទជាក់លាក់ </td>
    <td rowspan="3"> <br>≤១ </td>
    <td rowspan="3"> <br>&gt;១ </td>
    <td rowspan="3"> <br>&gt; ៤ </td>
    <td rowspan="3"> <br>&gt; ៦ </td>
    <td rowspan="3"> <br>≥ ១០ </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍ស្តីពីការអនុវត្ត និងការពិនិត្យតាមដាន និងជំរុញការ អនុវត្ត </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសិស្សម្នាក់ៗ តាមរយៈការបញ្ជាក់ពីសិស្សា នុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>2.9.3 </td>
    <td rowspan="4"> <br>សាលារៀនមានសកម្មភាពអប់រំ<br> <br>សិល្បៈ (ចម្រៀង គំនូរ របាំ តន្ត្រី) </td>
    <td> <br>-  សាលារៀនមានរៀបចំផែនការស្តីពីការអប់រំសិល្បៈ </td>
    <td rowspan="4"> <br>មាន១ </td>
    <td rowspan="4"> <br>មាន២ </td>
    <td rowspan="4"> <br>មាន៣ </td>
    <td rowspan="4"> <br>ទាំងអស់ </td>
    <td rowspan="4"> <br>សិស្សអាចសម្តែង បាន/មានស្នាដៃ </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  ថ្នាក់រៀននីមួយៗមានរៀបចំកាលវិភាគម៉ោងអប់រំសិល្បៈ </td>
  </tr>
  <tr>
    <td> <br>-  របាយការណ៍ស្តីពីការអនុវត្ត និងការពិនិត្យតាមដាន និងជំរុញការអនុវត្ត </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសិស្សម្នាក់ៗ តាមរយៈការបញ្ជាក់ពីសិស្សានុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៩ នៃស្ដង់ដាទី២ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>សរុបពិន្ទុនិងភាគរយស្តង់ដាទី២៖ ការបង្រៀន និងរៀន(១០សូចនាករគន្លឹះ និង ២៩សូចនាកររង) </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
</tbody></table></div>
<div id="pane-std3" class="tab-pane "><table class="std-table" data-std="std3" id="tpl-standard3">
  <thead>
  <tr>
    <th rowspan="2"> <br>ល.រ </th>
    <th rowspan="2"> <br>ស្តង់ដានិងសូចនាករ</th>
    <th rowspan="2"> <br>កម្រិតផ្ទៀងផ្ទាត់សូចនាករ </th>
    <th colspan="5"> <br>កម្រិតផ្ទៀងផ្ទាត់លទ្ធផល </th>
    <th rowspan="2"> <br>ពិន្ទុ </th>
    <th rowspan="2"> <br>យោបល់ </th>
  </tr>
  <tr>
    <th> <br>ពិន្ទុ</th>
    <th> <br>ពិន្ទុ២</th>
    <th> <br>ពិន្ទុ៣
    </th><th> <br>ពិន្ទុ៤</th>
    <th> <br>ពិន្ទុ៥</th>
  </tr>
  <tr>
    <th colspan="10"> <br>ស្តង់ដាទី៣៖ ការចូលរួមរបស់សហគមន៍ (៣សូចនាករគន្លឹះ និង ៥សូចនាកររង) </th>
  </tr></thead>
<tbody>
  <tr>
    <td colspan="10"> <br>3.1 ការបង្កើតនិងដំណើរការគណៈកម្មការគ្រប់គ្រងសាលារៀន និងថ្នាក់រៀន </td>
  </tr>
  <tr>
    <td rowspan="5"> <br>3.1.1 </td>
    <td rowspan="5"> <br>ចំនួនដងគណៈកម្មការគ្រប់គ្រងសាលារៀន (គ.គ.ស.) ប្រជុំក្នុង មួយឆ្នាំ </td>
    <td> <br>-  សាលារៀនមានរបាយការណ៍ប្រជុំស្តីពីការបង្កើតគណៈកម្មការគ្រប់គ្រងសាលារៀន </td>
    <td rowspan="5"> <br>≤៣ </td>
    <td rowspan="5"> <br>&gt;៣ </td>
    <td rowspan="5"> <br>&gt; ៥ </td>
    <td rowspan="5"> <br>&gt; ៧ </td>
    <td rowspan="5"> <br>≥ ៩ </td>
    <td rowspan="5"> <br>0 </td>
    <td rowspan="5"> <br><br> <br><br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  លិខិតបង្គាប់ការគណៈកម្មការគ្រប់គ្រងសាលារៀន មានការទទួល ស្គាល់ តាមការណែនាំ </td>
  </tr>
  <tr>
    <td> <br>-  គ.គ.ស. មានរចនាសម្ព័ន្ធ និងតួនាទីភារកិច្ចច្បាស់លាស់ តាមការ ណែនាំ </td>
  </tr>
  <tr>
    <td> <br>-  គ.គ.ស. មានរបាយការណ៍ប្រជុំ និងរបាយការណ៍វឌ្ឍនភាពតាម ការណែនាំ </td>
  </tr>
  <tr>
    <td> <br>-  គ.គ.ស. មានរបាយការណ៍បង្ហាញអំពីការគាំទ្រឱ្យសាលារៀនមាន ការអភិវឌ្ឍទាំងលទ្ធផលសិក្សារបស់សិស្ស និងការកែលម្អបរិស្ថាន សាលារៀន </td>
  </tr>
  <tr>
    <td rowspan="5"> <br>3.1.2 </td>
    <td rowspan="5"> <br>ភាគរយថ្នាក់រៀនបង្កើតនិងដំណើរការ គណៈកម្មការគ្រប់គ្រងថ្នាក់រៀន (គ.គ.ថ.) </td>
    <td> <br>-  ថ្នាក់រៀនមានរបាយការណ៍ប្រជុំស្តីពីការបង្កើតគណៈកម្មការគ្រប់គ្រងថ្នាក់រៀន </td>
    <td rowspan="5"> <br>≤ ៧០% </td>
    <td rowspan="5"> <br>&gt;៧០% </td>
    <td rowspan="5"> <br>&gt; ៨០% </td>
    <td rowspan="5"> <br>&gt;៩០% </td>
    <td rowspan="5"> <br>100% </td>
    <td rowspan="5"> <br>0 </td>
    <td rowspan="5"> <br><br> <br><br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  លិខិតបង្គាប់ការគណៈកម្មការគ្រប់គ្រងថ្នាក់រៀន មានការទទួល ស្គាល់ តាមការណែនាំ </td>
  </tr>
  <tr>
    <td> <br>-  គ.គ.ថ. មានរចនាសម្ព័ន្ធ និងតួនាទីភារកិច្ចច្បាស់លាស់ តាមការណែនាំ </td>
  </tr>
  <tr>
    <td> <br>-  គ.គ.ថ. មានរបាយការណ៍ប្រជុំ និងរបាយការណ៍វឌ្ឍនភាព តាមការណែនាំ </td>
  </tr>
  <tr>
    <td> <br>-  គ.គ.ថ. មានរបាយការណ៍បង្ហាញអំពីការគាំទ្រឱ្យថ្នាក់រៀនមាន ការអភិវឌ្ឍទាំងលទ្ធផលសិក្សារបស់សិស្សការកែលម្អ បរិស្ថានថ្នាក់រៀន និងសកម្មភាពបម្រើឱ្យការសិក្សារបស់សិស្ស </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី១ នៃស្ដង់ដាទី៣ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>3.2 ការចូលរួមរបស់សហគមន៍ </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="5"> <br>3.2.1 </td>
    <td rowspan="5"> <br>សាលារៀនមាន កិច្ចសហប្រតិបត្តិការ ភាពជាដៃគូវិនិយោគជាមួយ វិស័យសាធារណៈ វិស័យឯកជន និងដៃគូអភិវឌ្ឍ </td>
    <td> <br>-  សាលារៀនមានរៀបចំផែនការស្តីពីការអភិវឌ្ឍហេដ្ឋារចនាសម្ព័ន្ធ និងមានប្លង់មេច្បាស់លាស់ </td>
    <td rowspan="5"> <br>សាងសង់និងដំណើរការអាហារដ្ឋាន </td>
    <td rowspan="5"> <br>បូកបន្ថែមដោយ សាងសង់និងដំណើរការទីលានកីឡា </td>
    <td rowspan="5"> <br>បូកបន្ថែមដោយ សាងសង់និងដំណើរការអគារពហុបំណង </td>
    <td rowspan="5"> <br>បូកបន្ថែមដោយ ជួសជុល/សាងសង់ ហេដ្ឋារចនា សម្ព័ន្ធ និងដំណើរការកម្មវិធីសិក្សា </td>
    <td rowspan="5"> <br>បូកបន្ថែមដោយ ជួសជុល/សាងសង់ ហេដ្ឋារចនា សម្ព័ន្ធ និងដំណើរការកម្មវិធីសិក្សាទំនើប </td>
    <td rowspan="5"> <br>0 </td>
    <td rowspan="5"> <br><br> <br><br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  គណៈគ្រប់គ្រងសាលារៀន និង គ.គ.ស. បានពិភាក្សា អំពីការកៀរគររកដៃគូវិនិយោគ លើការរៀបចំអាហារដ្ឋាន ទីលានកីឡា សាលប្រជុំ អគារពហុបំណង ការដាក់ឱ្យអនុវត្តកម្មវិធីសិក្សាទំនើបជាដើម </td>
  </tr>
  <tr>
    <td> <br>-  គណៈគ្រប់គ្រងសាលារៀន និង គ.គ.ស. ស្វែងរកដៃគូ សហប្រតិបត្តិការ និងវិនិយោគ ទៅតាមផែនការមេ និងតម្រូវការ </td>
  </tr>
  <tr>
    <td> <br>-  មានការចុះកិច្ចព្រមព្រៀង ដោយឈរលើផលប្រយោជន៍សិស្សជាធំ </td>
  </tr>
  <tr>
    <td> <br>-  សិស្សានុសិស្សបានទទួលផលពីការសហប្រតិបត្តិការ </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>3.2.2 </td>
    <td rowspan="4"> <br>ភាគរយសិស្សត្រៀមនឹងបោះបង់ ឬ បោះបង់ការសិក្សា បានត្រឡប់មករៀន វិញទៀងទាត់ ក្រោមការគាំទ្រពី សហគមន៍ </td>
    <td> <br>-  សាលារៀនមានរៀបចំប្រជុំណែនាំដល់គ្រូប្រចាំថ្នាក់ អំពីការកំណត់អត្តសញ្ញាណសិស្សត្រៀមបោះបង់ការសិក្សា </td>
    <td rowspan="4"> <br>≤៥០% </td>
    <td rowspan="4"> <br>&gt;៥០% </td>
    <td rowspan="4"> <br>&gt;៦៥% </td>
    <td rowspan="4"> <br>&gt;៨០% </td>
    <td rowspan="4"> <br>≥ ៩០% </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  គ្រូប្រចាំថ្នាក់រាយការណ៍អំពីស្ថិតិសិស្សត្រៀមបោះបង់ការសិក្សា </td>
  </tr>
  <tr>
    <td> <br>-  នាយកសាលា គ្រូប្រចាំថ្នាក់ និងគ.គ.ស. ប្រជុំពិភាក្សាអំពីការទប់ស្កាត់សិស្សកុំឱ្យបោះបង់ការសិក្សា និងគាំទ្រពួកគេដើម្បីបានមករៀនទៀតទាត់ </td>
  </tr>
  <tr>
    <td> <br>-  ផ្ទៀងផ្ទាត់ជាមួយសិស្សម្នាក់ៗ តាមរយៈការបញ្ជាក់ពីសិស្សានុសិស្ស និងអ្នកពាក់ព័ន្ធផ្សេងទៀត </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី២ នៃស្ដង់ដាទី៣ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>3.3 ការគាំទ្ររបស់សហគមន៍ </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>3.3.1 </td>
    <td rowspan="3"> <br>បរិមាណចំណូលមូលនិធិបង់ចូលសាលារៀន </td>
    <td> <br>-  សាលារៀនមានរៀបចំផែនការអភិវឌ្ឍសាលារៀន ទាំង៤ </td>
    <td rowspan="3"> <br>ស្មើថវិការដ្ឋផ្ដល់ជូនប្រចាំឆ្នាំ </td>
    <td rowspan="3"> <br>កើន២ដង </td>
    <td rowspan="3"> <br>កើន៣ដង </td>
    <td rowspan="3"> <br>កើន៤ដង </td>
    <td rowspan="3"> <br>កើនលើស៥ដង </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  នាយកសាលា និង គ.គ.ស. បង្ហាញអំពីបរិមាណចំណូលចំណាយ ទាំងថវិការដ្ឋ (លើកលែងមូលនិធិដំណើរការសាលារៀនបន្ថែម) និងថវិកាដែលមានមកពីប្រភព ៣ផ្សេងទៀត ដូចមានចែងក្នុងសៀវភៅ SOF </td>
  </tr>
  <tr>
    <td> <br>-  ធ្វើការប្រៀបធៀបចំណូលថវិការដ្ឋ និងថវិកាពីប្រភពទាំង៣ </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៣ នៃស្ដង់ដាទី៣ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>សរុបពិន្ទុនិងភាគរយស្តង់ដាទី៣(៣សូចនាករគន្លឹះ និង ៥សូចនាកររង) </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
</tbody></table></div>
<div id="pane-std4" class="tab-pane "><table class="std-table" data-std="std4" id="tpl-standard4">
  <thead>
  <tr>
    <th rowspan="2"> <br>ល.រ </th>
    <th rowspan="2"> <br>ស្តង់ដានិងសូចនាករ</th>
    <th rowspan="2"> <br>កម្រិតផ្ទៀងផ្ទាត់សូចនាករ </th>
    <th colspan="5"> <br>កម្រិតផ្ទៀងផ្ទាត់លទ្ធផល </th>
    <th rowspan="2"> <br>ពិន្ទុ </th>
    <th rowspan="2"> <br>យោបល់ </th>
  </tr>
  <tr>
    <th> <br>ពិន្ទុ</th>
    <th> <br>ពិន្ទុ២</th>
    <th> <br>ពិន្ទុ៣
    </th><th> <br>ពិន្ទុ៤</th>
    <th> <br>ពិន្ទុ៥</th>
  </tr>
  <tr>
    <th colspan="10" style="text-align: left;">ស្តង់ដាទី៤៖ ដំណើរប្រតិបត្តិការ និងរដ្ឋបាលសាលារៀន<br> (៦សូចនាករគន្លឹះ និង ២១សូចនាកររង) </th>
  </tr>
  <tr>
    <td colspan="8"> <br>4.1 ការគ្រប់គ្រងរដ្ឋបាលទូទៅ </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>4.1.1 </td>
    <td rowspan="4"> <br>ការរៀបចំទីចាត់ការ ទុកដាក់ឯកសារ មានសណ្តាប់ធ្នាប់ និងរបៀបរៀបរយ </td>
    <td> <br>-  ទីចាត់ការស្អាត រៀបចំមានសណ្តាប់ធ្នាប់របៀបរៀបរយ និងផា សុកភាព </td>
    <td rowspan="4"> <br>ទីចាត់ការស្អាត </td>
    <td rowspan="4"> <br>ទីចាត់ការស្អាត ការទុកដាក់ឯកសារ ងាយស្រួលស្វែងរក </td>
    <td rowspan="4"> <br>បន្ថែមដោយ ប្រើប្រាស់កុំព្យូទ័រក្នុងការបំពេញការងារ </td>
    <td rowspan="4"> <br>បន្ថែមដោយ មានបំណែងចែកតួនាទីភារកិច្ចច្បាស់លាស់ </td>
    <td rowspan="4"> <br>មានការតុបតែងទីចាត់ការ មានរាល់ឯកសារនិងព័ត៌មានគ្រប់គ្រាន់ </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  មានទូរដាក់ឯកសារ តុនិងកៅអីសម្រាប់បុគ្គលិកទីចាត់ការ និង កន្លែងទទួលភ្ញៀវ </td>
  </tr>
  <tr>
    <td> <br>-  មានកុំព្យូទ័រ ព្រីនទ័រ និងម៉ាស៊ីនថតចម្លង សម្រាប់ការងាររដ្ឋបាល ស្ថិតិ និងរបាយការណ៍ជាដើម </td>
  </tr>
  <tr>
    <td> <br>-  ទីចាត់ការមានសម្ភារៈប្រើប្រាស់សមស្របតាមតម្រូវការ </td>
  </tr>
  <tr>
    <td rowspan="5"> <br>4.1.2 </td>
    <td rowspan="5"> <br>សាលារៀនប្រើប្រាស់ App សម្រាប់ប្រព័ន្ធ គ្រប់គ្រងទិន្នន័យសាលារៀន </td>
    <td> <br>-  សាលារៀនប្រើប្រាស់ប្រព័ន្ធព័ត៌មានគ្រប់គ្រងហិរញ្ញវត្ថុ (FMIS) </td>
    <td rowspan="5"> <br>មាន App </td>
    <td rowspan="5"> <br>បញ្ចូលទិន្នន័យ </td>
    <td rowspan="5"> <br>ធ្វើបច្ចុប្បន្នកម្មទិន្នន័យ </td>
    <td rowspan="5"> <br>មានទិន្នន័យសព្វគ្រប់ </td>
    <td rowspan="5"> <br>ប្រើប្រាស់ទិន្នន័យ </td>
    <td rowspan="5"> <br>0 </td>
    <td rowspan="5"> <br><br> <br><br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមាន App សម្រាប់គ្រប់គ្រងទិន្នន័យរបស់សាលារៀន </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានចាត់តាំងបុគ្គលិកអប់រំឱ្យទទួលខុសត្រូវលើការគ្រប់គ្រងទិន្នន័យ និងអាចទាញយកជារបាយការណ៍តាមតម្រូវការ </td>
  </tr>
  <tr>
    <td> <br>-  នាយកសាលាធានាសុចរិតភាពនៃទិន្នន័យដែលបានបញ្ចូលទៅក្នុងប្រព័ន្ធ ឬ App </td>
  </tr>
  <tr>
    <td> <br>-  ទិន្នន័យរបស់សាលារៀនត្រូវបានផ្សព្វផ្សាយដល់សាធារណៈជន ជាពិសេសមាតាបិតា អ្នកអាណាព្យាបាល សហគមន៍ អាជ្ញាធរដែនដី </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>4.1.3 </td>
    <td rowspan="4"> <br>ភាគរយគ្រូលើស-ខ្វះ បានថយចុះ </td>
    <td> <br>-  សាលារៀនមានរៀបចំផែនការស្តីពីការគ្រប់គ្រងបុគ្គលិក និងមានផែនការចំណោលសិស្ស ថ្នាក់រៀន បន្ទប់រៀនជាដើម </td>
    <td rowspan="4"> <br>&lt;១០% </td>
    <td rowspan="4"> <br>&lt;៦% </td>
    <td rowspan="4"> <br>&lt;៤% </td>
    <td rowspan="4"> <br>&lt;២% </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  នាយកសាលា បានប្រើប្រាស់សិទ្ធិក្នុងការមិនទទួលយកគ្រូបង្រៀន ដែលមន្ទីរ ឬ ការិយាល័យផ្តល់ជូន ពេលដឹងថាសាលាខ្លួនមានគ្រូ បង្រៀនគ្រប់គ្រាន់ ឬ កំពុងលើសគ្រូ </td>
  </tr>
  <tr>
    <td> <br>-  ករណីសាលាកំពុងខ្វះគ្រូ នាយកសាលារៀបចំសំណើសុំ គ្រូបង្រៀនចេញថ្មី ឬ គ្រូបង្រៀនជាប់កិច្ចសន្យា ឬ គ្រូបង្រៀន ពីរថ្នាក់ពីរវេន </td>
  </tr>
  <tr>
    <td> <br>-  ករណីខ្វះគ្រូ ហើយស្នើសុំគ្រូបន្ថែមមិនបាន សាលារៀនមាន រៀបចំការប្រជុំជាមួយ គ.គ.ស. មាតាបិតា អ្នកអាណាព្យាបាល អាជ្ញាធរដែនដី ដើម្បីរកមូលនិធិសមធម៌ ក្នុងការជួល គ្រូបង្រៀនស្ម័គ្រចិត្តមកបង្រៀនសិស្ស ឬ អាចបង្រៀនភាសាបរទេស កុំព្យូទ័រ បណ្ណារក្សជាដើម </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី១ នៃស្ដង់ដាទី៤ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>4.2 ការៀបចំផែនការអភិវឌ្ឍសាលារៀន </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>4.2.1 </td>
    <td rowspan="4"> <br>ផែនការយុទ្ធសាស្ត្រអភិវឌ្ឍន៍សាលារៀន ៥ឆ្នាំ ផែនការយុទ្ធសាស្ត្រ ថវិកា៣ឆ្នាំ ផែនការថវិកាប្រចាំឆ្នាំ និងផែនការប្រតិបត្តិប្រចាំឆ្នាំ បានរៀបចំតាមការណែនាំ </td>
    <td> <br>-  សាលារៀនមានរៀបចំការប្រជុំពិភាក្សាអំពីការរៀបចំផែនការទាំង៤ តាមការណែនាំ </td>
    <td rowspan="4"> <br>មាន១ </td>
    <td rowspan="4"> <br>មាន២ </td>
    <td rowspan="4"> <br>មាន៣ </td>
    <td rowspan="4"> <br>មាន៤ </td>
    <td rowspan="4"> <br>មាន៤ និងអនុវត្តបានចាប់ពី ៩០% ឡើងទៅ </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  ការប្រជុំមានការចូលរួមពីគ្រប់អ្នកពាក់ព័ន្ធ តាមការណែនាំ </td>
  </tr>
  <tr>
    <td> <br>-  មានរបាយការណ៍ពិនិត្យនិងវាយតម្លៃការអនុវត្តផែនការសកម្មភាពដែលបានគ្រោង </td>
  </tr>
  <tr>
    <td> <br>-  មានការឆ្លុះបញ្ចាំងអំពីការអនុវត្តផែនការ ធៀបនឹងលទ្ធផល សិក្សារបស់សិស្ស និងវឌ្ឍនភាពរបស់សាលារៀន </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី២ នៃស្ដង់ដាទី៤ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>4.3 ការវាយតម្លៃការបំពេញការងាររបស់បុគ្គលិក </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>4.3.1 </td>
    <td rowspan="3"> <br>ភាគរយគ្រូបង្រៀន និងបុគ្គលិកអប់រំ បានចុះកិច្ចព្រមព្រៀងលទ្ធផលការងារ ប្រចាំឆ្នាំ </td>
    <td> <br>-  នាយកសាលាបានរៀបចំប្រជុំផ្សព្វផ្សាយអំពីគោលការណ៍នៃការចុះកិច្ចព្រមព្រៀងរវាងនាយកសាលានិងគ្រូបង្រៀន ក្រោមការអនុម័តពី ប្រធាន គ.គ.ស. </td>
    <td rowspan="3"> <br>≤ ៥០% </td>
    <td rowspan="3"> <br>&gt;៥០% </td>
    <td rowspan="3"> <br>&gt; ៧០% </td>
    <td rowspan="3"> <br>&gt;៩០% </td>
    <td rowspan="3"> <br>100% </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  គ្រូបង្រៀន បុគ្គលិកអប់រំ និងនាយកសាលាបានចុះកិច្ចព្រមព្រៀង លទ្ធផលការងារប្រចាំឆ្នាំ ដោយមានកំណត់ចំណុចដៅនៃសូចនាករ លទ្ធផលច្បាស់លាស់ </td>
  </tr>
  <tr>
    <td> <br>-  នាយកសាលា និង គ.គ.ស. បានធ្វើការវាយតម្លៃនៃការអនុវត្ត កិច្ចព្រមព្រៀងរបស់គ្រូបង្រៀននិងបុគ្គលិកអប់រំ នៅចុងឆ្នាំ ព្រមទាំងមានការផ្តល់ការសរសើរ និងរង្វាន់លើកទឹកចិត្តជាដើម </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>4.3.2 </td>
    <td rowspan="3"> <br>ចំនួននាយកសាលានិងនាយករងបានចុះកិច្ចព្រមព្រៀងលទ្ធផលការងារប្រចាំឆ្នាំ </td>
    <td> <br>-  នាយកសាលាទទួលបានការណែនាំអំពីការចុះកិច្ចព្រមព្រៀងប្រចាំឆ្នាំរវាងនាយកសាលា នាយករង និងប្រធាន គ.គ.ស. </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br>1 </td>
    <td rowspan="3"> <br>2 </td>
    <td rowspan="3"> <br>3 </td>
    <td rowspan="3"> <br>ទាំងអស់ (ករណីមាននាយក ១នាក់ ឬ ២នាក់ ក៏ដោយ បើបានចុះកិច្ចព្រមព្រៀងគ្រប់គ្នា) </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  នាយកសាលា នាយករង និងប្រធាន គ.គ.ស. បានចុះកិច្ចព្រមព្រៀងលទ្ធផលការងារប្រចាំឆ្នាំ ដោយមានកំណត់ចំណុចដៅនៃសូចនាករលទ្ធផលច្បាស់លាស់ </td>
  </tr>
  <tr>
    <td> <br>-  នាយកសាលា និង គ.គ.ស. បានធ្វើការវាយតម្លៃនៃការអនុវត្តកិច្ចព្រមព្រៀងរបស់នាយករង និងនាយកសាលាខ្លួនឯង នៅចុងឆ្នាំ ព្រមទាំងមានការផ្តល់ការសរសើរ និងរង្វាន់លើកទឹកចិត្តជាដើម </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៣ នៃស្ដង់ដាទី៤ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>4.4 រង្វាយតម្លៃលទ្ធផលសិក្សា </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>4.4.1 </td>
    <td rowspan="4"> <br>ការរៀបចំធ្វើតេស្តស្តង់ដាដើមឆ្នាំឬចុងឆ្នាំ ប្រចាំខែ ឆមាស និងតេស្តស្តង់ដា ថ្នាក់ទី៣ និងទី៦ បានរៀបចំទៀងទាត់ </td>
    <td> <br>-  នាយកសាលាបានរៀបចំប្រជុំផ្សព្វផ្សាយអំពីគោលការណ៍នៃការនៃការរៀបចំនិងអនុវត្តតេស្តស្តង់ដាសម្រាប់ការប្រឡងនានា </td>
    <td rowspan="4"> <br>1 </td>
    <td rowspan="4"> <br>2 </td>
    <td rowspan="4"> <br>3 </td>
    <td rowspan="4"> <br>4 </td>
    <td rowspan="4"> <br>5 </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  គណៈគ្រប់គ្រងសាលារៀបចំយន្តការនៃការធ្វើតេស្តស្តង់ដា ដោយបែងចែកសកម្មភាព មុនពេល អំឡុងពេល និងក្រោយពេលនៃការធ្វើតេស្តស្តង់ដា </td>
  </tr>
  <tr>
    <td> <br>-  គ.គ.ស. គ.គ.ថ. និងមាតាបិតា អ្នកអាណាព្យាបាល ពិនិត្យតាមដាន និងចូលរួមអនុវត្តតេស្តស្តង់ដា </td>
  </tr>
  <tr>
    <td> <br>-  លទ្ធផលតេស្តស្តង់ដា ត្រូវបានយកទៅប្រើជាមូលដ្ឋាន ក្នុងការរៀបចំផែនការអភិវឌ្ឍសាលារៀន ផែនការថ្នាក់រៀន និងការចុះកិច្ចព្រមព្រៀងលទ្ធផលរវាងគ្រូបង្រៀនជាមួយនាយក និងគ្រូបង្រៀនជាមួយមាតាបិតា អ្នកអាណាព្យាបាល </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៤ នៃស្ដង់ដាទី៤ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>4.5 ការលើកកម្ពស់សុខភាព និងអាហារូបត្ថម្ភ </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="5"> <br>4.5.1 </td>
    <td rowspan="5"> <br>ការលើកកម្ពស់សេវាថែទាំសុខភាពបឋម </td>
    <td> <br>-       គណៈកម្មការសុខភាពសិក្សានៅតាមគ្រឹះស្ថានសិក្សា មានសមាសភាព តួនាទីភារកិច្ចច្បាស់លាស់ និងមាន នីត្យានុកូល </td>
    <td rowspan="5"> <br>បង្កើតគណៈកម្មការសុខភាព </td>
    <td rowspan="5"> <br>សម្ភារៈសង្គ្រោះបឋម </td>
    <td rowspan="5"> <br>បរិក្ខារនិងសម្ភារៈសង្គ្រោះបឋម </td>
    <td rowspan="5"> <br>បន្ទប់សុខភាព </td>
    <td rowspan="5"> <br>សហការជាមួយកម្មវិធីជាតិ </td>
    <td rowspan="5"> <br>0 </td>
    <td rowspan="5"> <br><br> <br><br><br><br></td>
  </tr>
  <tr>
    <td> <br>-       ភស្តុតាងនៃបរិក្ខារនិងសម្ភារៈសង្គ្រោះបឋម </td>
  </tr>
  <tr>
    <td> <br>-       របាយការណ៍ស្តីពីការផ្ដល់ថ្នាំបង្ការតាមកម្មវិធីជាតិ ផ្ដល់ថ្នាំបង្ការ ឬថ្នាំទម្លាក់ដង្កូវព្រូន </td>
  </tr>
  <tr>
    <td> <br>-       បន្ទប់សុខភាពនិងសម្ភារៈប្រើប្រាស់ជាមូលដ្ឋានចាំបាច់ </td>
  </tr>
  <tr>
    <td> <br>-       យន្តការគ្រប់គ្រងកិច្ចដំណើរការបន្ទប់សុខភាព </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>4.5.2 </td>
    <td rowspan="3"> <br>ការពិនិត្យសុខភាពសិស្ស </td>
    <td> <br>-       ផែនការពិនិត្យសុខភាពសិស្ស និងសៀវភៅតាមដានសុខភាព សិស្ស </td>
    <td rowspan="3"> <br>ពិនិត្យស្ថានភាពអាហារូបត្ថម្ភសិស្ស (អាយុ ទម្ងន់ កម្ពស់) </td>
    <td rowspan="3"> <br>ពិនិត្យ ការស្តាប់ និងគំហើញ </td>
    <td rowspan="3"> <br>ពិនិត្យសុខភាពផ្លូវចិត្ត ឬស្ថានភាពសុខភាពផ្សេងៗ </td>
    <td rowspan="3"> <br>បានពិនិត្យ គ្រប់មុខ </td>
    <td rowspan="3"> <br>បានពិនិត្យ និងផ្តល់សេវា គ្រប់មុខ </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-       របាយការណ៍ទិន្នន័យស្តីពីការពិនិត្យសុខភាពសិស្ស ឬការផ្តល់សេវាសុខភាពផ្សេងៗ </td>
  </tr>
  <tr>
    <td> <br>-       របាយការណ៍ស្តីពីកិច្ចអន្តរាគមន៍ចំពោះសិស្សដែល មានបញ្ហាសុខភាពមិនល្អបានទៅទទួលសេវាគាំទ្រ </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>4.5.3 </td>
    <td rowspan="4"> <br>ការលើកកម្ពស់ទឹកស្អាត និងអនាម័យ </td>
    <td> <br>-       បង្គន់អនាម័យ កន្លែងលាងសម្អាតដៃ បណ្តាញទឹកស្អាត </td>
    <td rowspan="4"> <br>បណ្តាញ ទឹកស្អាត </td>
    <td rowspan="4"> <br>កន្លែងលាងដៃ </td>
    <td rowspan="4"> <br>បង្គន់អនាម័យ </td>
    <td rowspan="4"> <br>បង្គន់អនាម័យតាមស្តង់ដា </td>
    <td rowspan="4"> <br>គ្រប់ជ្រុង ជ្រោយ </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-       កម្មវិធីការគ្រប់គ្រងអនាម័យពេលមករដូវរបស់កុមារី </td>
  </tr>
  <tr>
    <td> <br>-       បណ្ដាញទឹកស្អាតសម្រាប់ទទួលទានរបស់គ្រូ សិស្ស </td>
  </tr>
  <tr>
    <td> <br>-       កាលវិភាគស្តីពីការលាងសម្អាតដៃនិងដុសសម្អាតធ្មេញជាក្រុមសម្រាប់សិស្សទាំងអស់ </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>4.5.4 </td>
    <td rowspan="3"> <br>ការលើកកម្ពស់សុវត្ថិភាពចំណីរ អាហារ និងអាហារប្រកបដោយ សុខភាព </td>
    <td> <br>-       ការបិទផ្សាយគោលការណ៍ណែនាំស្តីពីការលើកកម្ពស់ សុវត្ថិភាពចំណីអាហារនិងអាហារប្រកបដោយសុខភាព </td>
    <td rowspan="3"> <br>បានអប់រំផ្សព្វ ផ្សាយអំពីសុវត្ថិភាពចំណីអាហារនិងអាហារប្រកបដោយសុខភាព </td>
    <td rowspan="3"> <br>អនុវត្តគោលការណ៍ណែនាំស្ដីពីសុវត្ថិភាពចំណីអាហារនិងអហារប្រកបដោយសុខភាព(កិច្ចសន្យាច្បាស់លាស់) </td>
    <td rowspan="3"> <br>មានយន្តការត្រួតពិនិត្យពីសុវត្ថិភាពចំណីអាហារនិងអាហារប្រកបដោយសុខភាពជាប្រចាំ </td>
    <td rowspan="3"> <br>រៀបចំអាហារដ្ឋានប្រកបដោយអនាម័យស្អាតជាប់ជាប្រចាំ </td>
    <td rowspan="3"> <br>លើកកម្ពស់អ្នកផលិតក្នុងមូលដ្ឋានតាមរយៈការផ្ដល់ ឬលក់អាហារដែលមានសុវត្ថិភាពនិងប្រកបដោយសុខភាព </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-       អ្នកលក់មានកិច្ចសន្យាច្បាស់លាស់ជាមួយនាយកសាលា ឬអាជ្ញាធរមានសមត្ថកិច្ច </td>
  </tr>
  <tr>
    <td> <br>-       យន្តការត្រួតពិនិត្យសុវត្ថិភាពចំណីអាហារនិងអាហារ ប្រកបដោយសុខភាព </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>4.5.5 </td>
    <td rowspan="4"> <br>ការអនុវត្តមុខវិជ្ជាអប់រំសុខភាព </td>
    <td> <br>-       ផែនការបង្រៀន និងកាលវិភាគបង្រៀនមុខវិជ្ជាអប់រំ សុខភាព </td>
    <td rowspan="4"> <br>បានរៀបចំផែនការបង្រៀននិងកាលវិភាគបង្រៀនមុខវិជ្ជាអប់រំសុខភាព </td>
    <td rowspan="4"> <br>បានរៀបចំការបង្រៀនមុខវិជ្ជាអប់រំសុខភាព តាមកាលវិភាគកំណត់និងមានគ្រូទទួលបន្ទុកច្បាស់លាស់ </td>
    <td rowspan="4"> <br>បានអប់រំផ្សព្វ ផ្សាយពីការបង្ការជំងឺ ការបង្ការគ្រោះថ្នាក់ផ្សេងៗដែលកើតមានញឹកញាប់ក្នុងសហគមន៍ </td>
    <td rowspan="4"> <br>បានរៀបចំការប្រឡងប្រចាំខែ ត្រីមាស ឆមាស មុខវិជ្ជាអប់រំ<br> <br>សុខភាព </td>
    <td rowspan="4"> <br>លទ្ធផលពិន្ទុជាប់មធ្យមភាគមុខវិជ្ជាអប់រំសុខភាព ≥៧៥% </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-       សៀវភៅតាមដានការបង្រៀនមុខវិជ្ជាអប់រំសុខភាព </td>
  </tr>
  <tr>
    <td> <br>-       របាយការណ៍ពីការអប់រំផ្សព្វផ្សាយពីសារសុខភាពផ្សេងៗគ្រប់ រូបភាព </td>
  </tr>
  <tr>
    <td> <br>-       កម្មវិធីប្រឡងមុខវិជ្ជាអប់រំសុខភាព និងតារាងសម្រង់ពិន្ទុ មុខវិជ្ជាអប់រំសុខភាពរបស់សិស្ស </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>4.5.6 </td>
    <td rowspan="4"> <br>ការលើកកម្ពស់បរិស្ថានស្អាត បៃតង សុវត្ថិភាព អនាម័យ និងមេត្រីភាព </td>
    <td> <br>-       ធុងសំរាមបានរៀបចំស្របតាមលក្ខណៈបច្ចេកទេស ឬមានឡដុតសំរាមតាមស្តង់ដាបច្ចេកទេស </td>
    <td rowspan="4"> <br>បានរៀបចំការញែកសំរាមតាមលក្ខណៈ បច្ចេកទេស </td>
    <td rowspan="4"> <br>បានរៀប ចំសួនបន្លែវិលជុំ និងសួនជីវៈចម្រុះ </td>
    <td rowspan="4"> <br>បានរៀបចំសួនកុមារទីធ្លាលេងកំសាន្តបងអង្គុយ </td>
    <td rowspan="4"> <br>រៀបចំវេន សម្អាតនិងមានការត្រួតពិនិត្យជាប់ជាប្រចាំគ្រប់វេនសិក្សា </td>
    <td rowspan="4"> <br>មានអនាម័យ សោភ័ ណភាពបរិស្ថានស្អាតជាប់ជាប្រចាំ និងគ្មានថង់ផ្លាស្ទិក </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-       សួនផ្កាលម្អ រុក្ខជាតិ ដើមឈើ សួនបន្លែវិលជុំ សួនជីវៈចម្រុះ </td>
  </tr>
  <tr>
    <td> <br>-       យន្តការត្រួតពិនិត្យនិងការសម្អាតអនាម័យ </td>
  </tr>
  <tr>
    <td> <br>-       សាលារៀនគ្មានប្រើប្រាស់ថង់ប្លាស្ទិក </td>
  </tr>
  <tr>
    <td rowspan="2"> <br>4.5.7 </td>
    <td rowspan="2"> <br>ការរក្សាសន្តិសុខ សណ្ដាប់ធ្នាប់ ការការពារ កុមារ ការបង្ការគ្រោះមហន្តរាយនានា </td>
    <td> <br><br> </td>
    <td rowspan="2"> <br>មានរបង និងទ្វារត្រឹមត្រូវនិងមានគោលការណ៍សាលារៀន ថ្នាក់រៀន </td>
    <td rowspan="2"> <br>បានរៀបចំយន្តការផ្ទៃក្នុងក្នុងការរក្សាសន្តិសុខ សណ្តាប់ធ្នាប់<br> <br>និងបានផ្សព្វផ្សាយពីកិច្ចការពារកុមារពីគ្រប់ទម្រង់នៃអំពើហិង្សា </td>
    <td rowspan="2"> <br>សហការជាមួយអាជ្ញាធរ ពាក់ព័ន្ធ ដើម្បីធានា សន្តិសុខ និងសុវត្ថិភាព របស់សិស្ស </td>
    <td rowspan="2"> <br>មានបំពាក់ស្លាកសញ្ញាសម្ភារៈ ឧបករណ៍សម្រាប់ជូនដំណឹងអំពីភាព អាសន្ន </td>
    <td rowspan="2"> <br>មានយន្តការឆ្លើយតបពេលមាន គ្រោះអាសន្ន </td>
    <td rowspan="2"> <br>0 </td>
    <td rowspan="2"> <br><br> <br></td>
  </tr>
  <tr>
    <td> <br>-       សាលារៀនមានរបង ទ្វារចេញចូល-       សាលារៀនមានប្រព័ន្ធកិច្ចការពារកុមារ ការរៀបចំយន្តការ សណ្តាប់ធ្នាប់ រក្សាសុវត្ថិភាព ការដាក់ស្លាកសញ្ញាចរាចរណ៍ ការបង្ការការលង់ទឹក សម្ភារៈបរិក្ខារជូនដំណឹង ពីសញ្ញា គ្រោះថ្នាក់ បំពង់ពន្លត់អគ្គីភ័យ </td>
  </tr>
  <tr>
    <td rowspan="2"> <br>4.5.8 </td>
    <td rowspan="2"> <br>ការអនុវត្តសកម្មភាពអប់រំកាយនិងកីឡា </td>
    <td> <br>-       ទីធ្លាសម្រាប់ធ្វើសកម្មភាពអប់រំកាយនិងកីឡា - តារាងវាយតម្លៃលទ្ធផលការសិក្សារបស់សិស្សពីមុខវិជ្ជា អប់រំកាយនិងកីឡា </td>
    <td rowspan="2"> <br>មានកាលវិភាគបង្រៀនមុខវិជ្ជាអប់រំកាយ និងកីឡា ប្រចាំ សប្តាហ៍គ្រប់កម្រិតថ្នាក់ </td>
    <td rowspan="2"> <br>មានសៀវភៅសិក្សាគោលមុខវិជ្ជាអប់រំកាយ និងកីឡា គ្រប់កម្រិតថ្នាក់ </td>
    <td rowspan="2"> <br>មានទីលានគ្រប់គ្រាន់ សម្រាប់អនុវត្ត កម្មវិធីសិក្សាមុខវិជ្ជាអប់រំកាយ និងកីឡាគ្រប់កម្រិតថ្នាក់ </td>
    <td rowspan="2"> <br>មានសម្ភារគ្រប់គ្រាន់ សម្រាប់អនុវត្តកម្មវិធីសិក្សា មុខវិជ្ជាអប់រំកាយ និងកីឡាគ្រប់កម្រិតថ្នាក់ </td>
    <td rowspan="2"> <br>សីស្សម្នាក់ លេងកីឡា១ប្រភេទ </td>
    <td rowspan="2"> <br>0 </td>
    <td rowspan="2"> <br><br> <br></td>
  </tr>
  <tr>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៥ នៃស្ដង់ដាទី៤ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>4.6 ការអភិវឌ្ឍហេដ្ឋារចនាសម្ព័ន្ធ </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>4.6.1 </td>
    <td rowspan="4"> <br>សាលារៀនមានបណ្តាញអគិ្គសនី បំពាក់អ៊ីនធើណិត </td>
    <td> <br>-  សាលារៀនមានតបណ្តាញអគ្គិសនីចូល </td>
    <td rowspan="4"> <br>មាន១ </td>
    <td rowspan="4"> <br>មានទាំង២ </td>
    <td rowspan="4"> <br>អគ្គិសនី និងអ៊ីនធើណិតមានតែក្នុងទីចាត់ការ </td>
    <td rowspan="4"> <br>អគ្គិសនី និងអ៊ីនធើណិតមានគ្រប់បន្ទប់ </td>
    <td rowspan="4"> <br>បន្ថែមដោយភ្លើងបំភ្លឺពេលយប់ </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  បណ្តាញអគ្គិសនីត្រូវបានតភ្ជាប់ទៅទីចាត់ការ និងគ្រប់បន្ទប់រៀន និងបន្ទប់ផ្សេងៗទៀត ប្រកបដោយសណ្តាប់ធ្នាប់ និងសុវត្ថិភាព </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានតបណ្តាញអ៊ីនធើណិត </td>
  </tr>
  <tr>
    <td> <br>-  បណ្តាញអ៊ីនធើណិតត្រូវបានតភ្ជាប់ទៅទីចាត់ការ និងគ្រប់បន្ទប់រៀន និងបន្ទប់ផ្សេងៗទៀត ប្រកបដោយសណ្តាប់ធ្នាប់ និងគុណភាព </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>4.6.2 </td>
    <td rowspan="3"> <br>ភាគរយបន្ទប់រៀនបំពាក់ឧបករណ៍សិក្សាទំនើប (LCD, Smart TV, Smart Board…) </td>
    <td> <br>-  សាលារៀនមានផែនការបំពាក់ឧបករណ៍សិក្សាទំនើបតាមបន្ទប់ រៀន និងការបណ្តុះបណ្តាលគ្រូបង្រៀនឱ្យចេះប្រើប្រាស់ </td>
    <td rowspan="3"> <br>≤ ៥% </td>
    <td rowspan="3"> <br>&gt;៥% </td>
    <td rowspan="3"> <br>&gt; ១០% </td>
    <td rowspan="3"> <br>&gt;១៥% </td>
    <td rowspan="3"> <br>&gt;២០% </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  គណៈគ្រងសាលា និង គ.គ.ស. ពិភាក្សាអំពីការស្នើសុំទៅក្រសួង ឬ អង្កការដៃគូអភិវឌ្ឍ ឬ កៀរគរមូលនិធិពីមាតាបិតា សប្បុរសជន ដើម្បីបំពាក់ឧករណ៍សិក្សាទំនើប </td>
  </tr>
  <tr>
    <td> <br>-  គ្រូបង្រៀន ពិភាក្សាជាមួយ គ.គ.ថ. ដើម្បីកៀរគរមូលនិធិ ដើម្បីបំពាក់ឧករណ៍សិក្សាទំនើប នៅតាមបន្ទប់រៀនរបស់ខ្លួន </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>4.6.3 </td>
    <td rowspan="4"> <br>សាលារៀនមានបណ្ណាល័យ </td>
    <td> <br>-  សាលារៀនមានសៀវភៅណែនាំប្រតិបត្តិស្តីពីបណ្ណាល័យ បឋមសិក្សា </td>
    <td rowspan="4"> <br>កៀនបណ្ណាល័យ </td>
    <td rowspan="4"> <br>បណ្ណាល័យក្នុងទីចាត់ការ </td>
    <td rowspan="4"> <br>បណ្ណាល័យជាបន្ទប់ </td>
    <td rowspan="4"> <br>បណ្ណាល័យជាអគារ </td>
    <td rowspan="4"> <br>បណ្ណាល័យទំនើប </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានអគារ ឬ បន្ទប់សម្រាប់រៀបចំបង្កើត និងដំណើរការបណ្ណាល័យ </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានបណ្ណាល័យតាមស្តង់ដា និងកំពុងដំណើរការ </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានបណ្ណាល័យ តែមិនមានបណ្ណារក្ស ឬ មិនទាន់ មានសង្ហារឹមនិងសៀវភៅអានតាមស្តង់ដា នាយកសាលា និង គ.គ.ស. ត្រូវពិភាក្សាគ្នាដើម្បីកៀរគរមូលនិធិពីមាតាបិតា សប្បុរសជន ដើម្បីបំពាក់គ្រឿងសង្ហារឹម ទិញសៀវភៅអានបន្ថែម និងជួលបណ្ណារក្សាស្ម័គ្រចិត្តជាដើម </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>4.6.4 </td>
    <td rowspan="3"> <br>សាលារៀនមានបន្ទប់កុំព្យូទ័រសម្រាប់សិស្សរៀន </td>
    <td> <br>-  សាលារៀនមានអគារ ឬ បន្ទប់សម្រាប់រៀបចំបង្កើតនិង ដំណើរការបន្ទប់កុំព្យូទ័រ </td>
    <td rowspan="3"> <br>មានកុំព្យូទ័រសម្រាប់សិស្សរៀន </td>
    <td rowspan="3"> <br>រៀបចំបន្ទប់កុំព្យូទ័រ និងមានកុំព្យូទ័រ </td>
    <td rowspan="3"> <br>រៀបចំបន្ទប់កុំព្យូទ័រ និងមានកុំព្យូទ័រយ៉ាងតិច ៣០គ្រឿង </td>
    <td rowspan="3"> <br>សិស្សថ្នាក់ទី៤-៦ ទាំងអស់បានរៀនកុំព្យូទ័រ យ៉ាងតិច ១ម៉ោង/សប្តាហ៍ </td>
    <td rowspan="3"> <br>សិស្សថ្នាក់ទី៤-៦ ចេះប្រើប្រាស់កុំព្យូទ័រសម្រាប់ការរៀន </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានបន្ទប់កុំព្យូទ័រ និងកំពុងដំណើរការ </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានបន្ទប់កុំព្យូទ័រ តែមិនមានគ្រូកុំព្យូទ័រ ឬ មិនទាន់ មានកុំព្យូទ័រគ្រប់គ្រាន់សម្រាប់សិស្សរៀន នាយកសាលា និង គ.គ.ស. ត្រូវពិភាក្សាគ្នាដើម្បីកៀរគរមូលនិធិពីមាតាបិតា សប្បុរសជន ដើម្បីទិញកុំព្យូទ័របន្ថែម និងជួលគ្រូបង្រៀន កុំព្យូទរ័ស្ម័គ្រចិត្តជាដើម </td>
  </tr>
  <tr>
    <td rowspan="3"> <br>4.6.5 </td>
    <td rowspan="3"> <br>សាលារៀនមានទីលានកីឡារួមមាន តារាងបាល់ទះ បាល់ទាត់ បាល់បោះ វាយសី... </td>
    <td> <br>-  សាលារៀនមានទីតាំងសមស្របសម្រាប់រៀបចំទីលានកីឡា </td>
    <td rowspan="3"> <br>មានទីលានអត្តពលកម្ម </td>
    <td rowspan="3"> <br>បន្ថែមដោយតារាងបាល់ទះ </td>
    <td rowspan="3"> <br>បន្ថែមដោយតារាងបាល់ទាត់ </td>
    <td rowspan="3"> <br>បន្ថែមដោយតារាងបាល់បោះ វាយសី </td>
    <td rowspan="3"> <br>សិស្សម្នាក់ៗចូលរួមកម្មភាពកីឡា យ៉ាងតិចមួយជំនាញ </td>
    <td rowspan="3"> <br>0 </td>
    <td rowspan="3"> <br><br> <br><br></td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានទីលានលេងកីឡាគ្រប់ប្រភេទ និងកំពុងដំណើរការ </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានទីលានកីឡា តែមានសកម្មភាព ឬ មិនទាន់មានទីលានកីឡាគ្រប់គ្រាន់ នាយកសាលា និង គ.គ.ស. ត្រូវពិភាក្សាគ្នាដើម្បីកៀរគរមូលនិធិពីមាតាបិតា សប្បុរសជន ដើម្បីវិនិយោគ និងជួលគ្រូបង្រៀនឯកទេសកីឡាស្ម័គ្រចិត្តជាដើម </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៦ នៃស្ដង់ដាទី៤ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>សរុបពិន្ទុនិងភាគរយស្តង់ដាទី៤(៦សូចនាករគន្លឹះ និង ២១សូចនាកររង) </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
</thead></table></div>
<div id="pane-std5" class="tab-pane "><table class="std-table" data-std="std5" id="tpl-standart5">
  <thead>
  <tr>
    <th rowspan="2"> <br>ល.រ </th>
    <th rowspan="2"> <br>ស្តង់ដានិងសូចនាករ</th>
    <th rowspan="2"> <br>កម្រិតផ្ទៀងផ្ទាត់សូចនាករ </th>
    <th colspan="5"> <br>កម្រិតផ្ទៀងផ្ទាត់លទ្ធផល </th>
    <th rowspan="2"> <br>ពិន្ទុ </th>
    <th rowspan="2"> <br>យោបល់ </th>
  </tr>
  <tr>
    <th> <br>ពិន្ទុ</th>
    <th> <br>ពិន្ទុ២</th>
    <th> <br>ពិន្ទុ៣
    </th><th> <br>ពិន្ទុ៤</th>
    <th> <br>ពិន្ទុ៥</th>
  </tr>
  <tr>
    <th colspan="10" style="text-align: left;">ស្តង់ដាទី៥៖ គណនេយ្យភាព (៣សូចនាករគន្លឹះ និង ៥សូចនាកររង) </th>
  </tr></thead>
<tbody>
  <tr>
    <td colspan="8"> <br>5.1 វេទិកាសាធារណៈ </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="6"> <br>5.1.1 </td>
    <td rowspan="6"> <br>ការជួបប្រជុំមាតាបិតាសិស្ស </td>
    <td> <br>-  សាលារៀនមានផែនការសាលារៀន </td>
    <td rowspan="6"> <br>១ឆ្នាំ/ម្តង </td>
    <td rowspan="6"> <br>៦ខែ/ម្តង </td>
    <td rowspan="6"> <br>៣ខែ/ម្តង </td>
    <td rowspan="6"> <br>១ខែ/ម្តង </td>
    <td rowspan="6"> <br>មានកំណត់ហេតុ ឬ របាយការណ៍ប្រជុំ </td>
    <td rowspan="6"> <br>0 </td>
    <td rowspan="6"> <br><br> <br><br><br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  ប្រធានបទ៖ ណែនាំអំពី ការកាត់បន្ថយនិងលុបបំបាត់អំពីហិង្សា នៅក្នុងគ្រួសារ និងសាលារៀន, លទ្ធផលសិក្សានិងជំរុញ ការសិក្សារៀនសូត្រ, ការលើកកម្ពស់អាហារូបត្ថម្ភ, គ្រឿងញៀន, ច្បាប់ចរាចរណ៍ និងការងារផ្សេងៗទៀត </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានបិទផ្សាយឯកសារសកម្មភាព ឬស្នាដៃ កុមារ និងព័ត៌មានផ្សេងៗ </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនបានផ្តល់របាយការណ៍លទ្ធផលនៃការអភិវឌ្ឍ របស់កុមារយឺត ឱ្យមាតាបិតា អ្នកអាណាព្យាបាល និង សហគមន៍ </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានសកម្មភាពការងាររបស់សាលារៀន </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានរបាយការណ៍ការងារប្រចាំខែ ប្រចាំ ត្រីមាស ប្រចាំឆមាស និងប្រចាំឆ្នាំ </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី១ នៃស្ដង់ដាទី៥ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>5.2 ការផ្សព្វផ្សាយព័ត៌មានជាសាធារណៈ </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="5"> <br>5.2.1 </td>
    <td rowspan="5"> <br>លទ្ធផលតេស្តវាយតម្លៃស្តង់ដានិងព័ត៌មាននានាត្រូវបានអនុម័តដោយ គ.គ.ស. និង/ឬ បិទផ្សាយ ជាសាធារណៈ </td>
    <td> <br>-  សាលារៀនមានផែនការសាលារៀន </td>
    <td rowspan="5"> <br>១ឆ្នាំម្ដង </td>
    <td rowspan="5"> <br>១ឆមាសម្ដង </td>
    <td rowspan="5"> <br>១ត្រីមាសម្ដង </td>
    <td rowspan="5"> <br>១ខែម្ដង </td>
    <td rowspan="5"> <br>មានឯកសារតម្កល់ទុក </td>
    <td rowspan="5"> <br>0 </td>
    <td rowspan="5"> <br><br> <br><br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានបិទផ្សាយឯកសារសកម្មភាព ឬស្នាដៃ កុមារ និងព័ត៌មានផ្សេងៗ </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនបានផ្តល់របាយការណ៍លទ្ធផលនៃការអភិវឌ្ឍ របស់កុមារយឺត ឱ្យមាតាបិតា អ្នកអាណាព្យាបាល និង សហគមន៍ </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានសកម្មភាពការងាររបស់សាលារៀន </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានរបាយការណ៍ការងារប្រចាំខែ ប្រចាំ ត្រីមាស ប្រចាំឆមាស និងប្រចាំឆ្នាំ </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី២ នៃស្ដង់ដាទី៥ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>5.3 ការទទួលបានការគំាទ្រពីថ្នាក់ជាតិ </td>
    <td> <br><br> </td>
    <td> <br><br> </td>
  </tr>
  <tr>
    <td rowspan="2"> <br>5.3.1 </td>
    <td rowspan="2"> <br>ចំនួនដងនាយកសាលានិងនាយករង បានទទួលការហ្វឹកហាត់អនុវត្តស្តង់ដាសាលារៀនគំរូ ពីនាយកសាលាផ្សេង ឬ មកពីថ្នាក់លើ </td>
    <td> <br>-  សាលារៀនមានបញ្ជីរាយនាមនាយក នាយករង ទទួល ការហ្វឹកហាត់ការអនុវត្តការគ្រប់គ្រងតាមសាលារៀន និង កម្មវិធីសាលារៀនគំរូ </td>
    <td rowspan="2"> <br>1-2 </td>
    <td rowspan="2"> <br>3-4 </td>
    <td rowspan="2"> <br>5-6 </td>
    <td rowspan="2"> <br>7-8 </td>
    <td rowspan="2"> <br>លើស8ដង </td>
    <td rowspan="2"> <br>0 </td>
    <td rowspan="2"> <br><br> <br></td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានរបាយការណ៍លទ្ធផលនៃការអនុវត្ត </td>
  </tr>
  <tr>
    <td rowspan="2"> <br>5.3.2 </td>
    <td rowspan="2"> <br>ភាគរយគ្រូបង្រៀនបានទទួលការហ្វឹកហាត់ការអនុវត្តកញ្ចប់សម្ភារៈអំណាន និងគណិតវិទ្យាថ្នាក់ដំបូង និង/ឬ វិធីសាស្ត្របង្រៀនភាសាខ្មែរ និងគណិតវិទ្យា </td>
    <td> <br>-  សាលារៀនមានគ្រូបង្រៀន ក្រុមបច្ចេកទេស និង គណៈគ្រប់គ្រងសាលារៀន មានបញ្ជីកត់ត្រាជំនួយ បច្ចេកទេស ពីថ្នាក់ក្រោមជាតិ និងថ្នាក់ជាតិ </td>
    <td rowspan="2"> <br>≤ ៣០% </td>
    <td rowspan="2"> <br>&gt;៣០% </td>
    <td rowspan="2"> <br>&gt; ៤០% </td>
    <td rowspan="2"> <br>&gt;៥០% </td>
    <td rowspan="2"> <br>≥ ៦០% </td>
    <td rowspan="2"> <br>0 </td>
    <td rowspan="2"> <br><br> <br></td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានតារាងកត់ត្រាទិន្នន័យ ព័ត៌មាន និងផ្តល់ យោបល់ពីការជួយសម្រាប់សាលារៀន ក្នុងការអនុវត្ត យុទ្ធសាស្រ្តសហគមន៍សាលារៀនពីថ្នាក់ក្រោមជាតិ ថ្នាក់ជាតិ និងអ្នកពាក់ព័ន្ធ </td>
  </tr>
  <tr>
    <td rowspan="4"> <br>5.3.3 </td>
    <td rowspan="4"> <br>ភាគរយគ្រូបង្រៀន បំពេញទស្សនកិច្ច សិក្សា ទៅសាលាផ្សេងក្នុងមួយឆ្នាំ </td>
    <td> <br>-  សាលារៀនមានផែនការទស្សនកិច្ចសិក្សារបស់គ្រូបង្រៀននិងបុគ្គលិកអប់រំប្រចាំឆ្នាំ </td>
    <td rowspan="4"> <br>≤ ៣០% </td>
    <td rowspan="4"> <br>&gt;៣០% </td>
    <td rowspan="4"> <br>&gt; ៤០% </td>
    <td rowspan="4"> <br>&gt;៥០% </td>
    <td rowspan="4"> <br>≥ ៦០% </td>
    <td rowspan="4"> <br>0 </td>
    <td rowspan="4"> <br><br> <br><br><br></td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានមូលនិធិដើម្បីគំាទ្រដល់ដំណើរទស្សនកិច្ចសិក្សា </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនមានរបាយការណ៍ នៃដំណើរទស្សនកិច្ចសិក្សា </td>
  </tr>
  <tr>
    <td> <br>-  សាលារៀនបង្ហាញលទ្ធផលនៃការអនុវត្ត ដោយយកតាមឧត្តមានុវត្តន៍នៃសាលារៀនដែលគ្រូបង្រៀននិងបុគ្គលិកអប់រំបានទៅបំពេញទស្សនកិច្ច </td>
  </tr>
  <tr>
    <td colspan="8"> <br>លទ្ធផលសូចនាករគោលទី៣ នៃស្ដង់ដាទី៥ </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
  <tr>
    <td colspan="8"> <br>សរុបពិន្ទុនិងភាគរយស្តង់ដាទី៥៖ គណនេយ្យភាព(៣សូចនាករគន្លឹះ និង ៥សូចនាកររង) </td>
    <td> <br>0 </td>
    <td> <br>- </td>
  </tr>
</tbody></table></div>

<div id="pane-summary" class="tab-pane">
  <div class="sum-grid">

    <!-- Full summary table -->
    <div class="sum-card full-card">
      <h3>📋 តារាងសង្ខេបពិន្ទុ ស្តង់ដាទាំង៥</h3>
      <table class="sum-tbl" id="mainSumTbl">
        <thead><tr>
          <th style="width:36px">ល.រ</th>
          <th>ស្តង់ដានិងសូចនាករ</th>
          <th style="width:60px">ពិន្ទុ</th>
          <th style="width:72px">ភាគរយ</th>
        </tr></thead>
        <tbody id="mainSumBody"></tbody>
      </table>
    </div>

    <!-- Bar chart: score per standard -->
    <div class="sum-card">
      <h3>📊 ពិន្ទុសរុបតាមស្តង់ដា</h3>
      <div class="chart-wrap"><canvas id="chartBar"></canvas></div>
    </div>

    <!-- Radar chart -->
    <div class="sum-card">
      <h3>🕸️ Radar — ប្រៀបធៀបស្តង់ដា</h3>
      <div class="chart-wrap"><canvas id="chartRadar"></canvas></div>
    </div>

    <!-- Doughnut: overall -->
    <div class="sum-card">
      <h3>🍩 ភាគរយស្តង់ដានីមួយៗ</h3>
      <div class="chart-wrap2"><canvas id="chartDoughnut"></canvas></div>
    </div>

    <!-- Horizontal bar: indicators per std -->
    <div class="sum-card">
      <h3>📈 ពិន្ទុមធ្យមមាន/អតិបរមា</h3>
      <div class="chart-wrap2"><canvas id="chartHBar"></canvas></div>
    </div>

  </div>
</div>

</div>

<!-- Firebase -->
<script type="module">
import{initializeApp}from"https://www.gstatic.com/firebasejs/10.12.0/firebase-app.js";
import{getDatabase,ref,set,get,child}from"https://www.gstatic.com/firebasejs/10.12.0/firebase-database.js";
const cfg={
  apiKey:"AIzaSyC5T2ec-mxeO0lzknVe5SEBBXlp7IWmmuE",
  authDomain:"schoolreport-a7404.firebaseapp.com",
  databaseURL:"https://schoolreport-a7404-default-rtdb.asia-southeast1.firebasedatabase.app",
  projectId:"schoolreport-a7404",
  storageBucket:"schoolreport-a7404.firebasestorage.app",
  messagingSenderId:"62869703269",
  appId:"1:62869703269:web:d1a763f78ae8906d48c"
};
const app=initializeApp(cfg);
const db=getDatabase(app);
// Firebase keys cannot contain dots → replace with pipe char
const _s=(o)=>{ if(!o||typeof o!=='object') return o; const r={}; for(const k in o) r[k.replace(/\./g,'|')]=_s(o[k]); return r; };
const _d=(o)=>{ if(!o||typeof o!=='object') return o; const r={}; for(const k in o) r[k.replace(/\|/g,'.')]=_d(o[k]); return r; };
window.__fbSave=async(id,data)=>{ await set(ref(db,`schoolStandards/${id}`),_s(data)); };
window.__fbLoad=async(id)=>{ const s=await get(child(ref(db),`schoolStandards/${id}`)); return s.exists()?_d(s.val()):null; };
window.__fbReady=true;
console.log("Firebase ready");
</script>

<script>
// ═══════════════════════════════════════════
//  ROW DETECTION  (works for thead & tbody)
// ═══════════════════════════════════════════
const IND_RE=/^\d+\.\d+\.\d+$/;

function isAllTh(tr){ return tr.cells.length>0 && [...tr.cells].every(c=>c.tagName==='TH'); }

function rowType(tr){
  const c=tr.cells;
  if(!c.length) return 'skip';
  if(isAllTh(tr)) return 'header';
  const cs=parseInt(c[0].getAttribute('colspan')||'1');
  const txt=(c[0].textContent||'').trim();
  if(cs>=9) return 'sechdr';        // full-width section title
  if(cs>=7){
    if(txt.includes('លទ្ធផល')||txt.includes('សរុប')) return 'summary';
    return 'subhdr';
  }
  if(IND_RE.test(txt)) return 'indicator';
  return 'other';
}

// ═══════════════════════════════════════════
//  PROCESS TABLE  – add select & textarea
// ═══════════════════════════════════════════
function processTable(table){
  const std=table.dataset.std;
  Array.from(table.querySelectorAll('tr')).forEach(tr=>{
    const type=rowType(tr);
    if(type==='header'||type==='other'||type==='skip') return;
    if(type==='sechdr'){ tr.classList.add('sec-hdr'); return; }
    if(type==='subhdr'){ tr.classList.add('sub-hdr'); return; }

    if(type==='summary'){
      tr.classList.add('sum-row');
      const n=tr.cells.length;
      if(n>=2){
        tr.cells[n-2].innerHTML='<span class="sv" data-as>0</span>';
        tr.cells[n-1].innerHTML='<span class="pv" data-ap>-</span>';
      }
      return;
    }

    if(type==='indicator'){
      const n=tr.cells.length;
      if(n<2) return;
      const key=(tr.cells[0].textContent||'').trim();
      // collect metadata: name(col1), levels(col3-7)
      const nm = n>1?(tr.cells[1].textContent||'').replace(/\s+/g,' ').trim():'';
      const lvls=[];
      for(let i=3;i<=7&&i<n-2;i++) lvls.push((tr.cells[i].textContent||'').replace(/\s+/g,' ').trim());
      const sc=tr.cells[n-2];
      const cc=tr.cells[n-1];
      sc.className='sc';
      sc.innerHTML=`<select class="ss"
        data-k="${key}" data-s="${std}"
        data-nm="${encodeURIComponent(nm)}"
        data-lv="${encodeURIComponent(JSON.stringify(lvls))}"
        onchange="onChange(this)">
        <option value="">-</option>
        <option value="1">1</option><option value="2">2</option>
        <option value="3">3</option><option value="4">4</option>
        <option value="5">5</option></select>`;
      cc.className='cc';
      cc.innerHTML=`<textarea class="ct" data-k="${key}" data-s="${std}" rows="2" oninput="dirty()"></textarea>`;
    }
  });
}

// ═══════════════════════════════════════════
//  RECALC SUMMARIES
// ═══════════════════════════════════════════
function recalc(){
  document.querySelectorAll('.std-table').forEach(tbl=>{
    let scores=[],max=0;
    Array.from(tbl.querySelectorAll('tr')).forEach(tr=>{
      if(tr.classList.contains('sec-hdr')){ scores=[];max=0; return; }
      if(tr.classList.contains('sub-hdr')) return;
      if(tr.classList.contains('sum-row')){
        const sum=scores.reduce((a,b)=>a+b,0);
        const pct=max>0?((sum/max)*100).toFixed(1)+'%':'-';
        const as=tr.querySelector('[data-as]');
        const ap=tr.querySelector('[data-ap]');
        if(as) as.textContent=sum;
        if(ap) ap.textContent=pct;
        scores=[];max=0; return;
      }
      const sel=tr.querySelector('select.ss');
      if(sel){ scores.push(parseInt(sel.value)||0); max+=5; }
    });
  });
}

function onChange(s){ recalc(); dirty(); if(document.getElementById("pane-summary").classList.contains("active")) buildSummary(); }

// ═══════════════════════════════════════════
//  DATA
// ═══════════════════════════════════════════
function collect(){
  const d={};
  document.querySelectorAll('select.ss').forEach(s=>{
    const {s:std,k:key}=s.dataset;
    if(!d[std])d[std]={};
    if(!d[std][key])d[std][key]={};
    d[std][key].id    = key;
    d[std][key].name  = decodeURIComponent(s.dataset.nm||'');
    try{ d[std][key].levels = JSON.parse(decodeURIComponent(s.dataset.lv||'[]'));
    }catch(e){ d[std][key].levels=[]; }
    d[std][key].score = s.value===''?null:parseInt(s.value);
  });
  document.querySelectorAll('textarea.ct').forEach(t=>{
    const {s:std,k:key}=t.dataset;
    if(!d[std])d[std]={};
    if(!d[std][key])d[std][key]={};
    d[std][key].comment=t.value||'';
  });
  return d;
}

function populate(data){
  if(!data)return;
  document.querySelectorAll('select.ss').forEach(s=>{
    const {s:std,k:key}=s.dataset;
    const v=data[std]&&data[std][key]&&data[std][key].score!=null?data[std][key].score:'';
    s.value=v===null?'':String(v);
  });
  document.querySelectorAll('textarea.ct').forEach(t=>{
    const {s:std,k:key}=t.dataset;
    if(data[std]&&data[std][key]&&data[std][key].comment!=null)
      t.value=data[std][key].comment;
  });
  recalc();
}

// ═══════════════════════════════════════════
//  FIREBASE
// ═══════════════════════════════════════════
let _dirty=false;
function dirty(){ _dirty=true; st('⚠️ មិនទាន់រក្សា','busy'); }

async function fbSave(){
  const id=(document.getElementById('schoolInput').value||'').trim();
  if(!id){alert('សូមបញ្ចូលឈ្មោះ/លេខកូដសាលា');return;}
  if(!window.__fbReady){st('⏳ Firebase មិនទាន់ ready…','busy');return;}
  st('⏳ កំពុងរក្សា…','busy');
  try{
    await window.__fbSave(id,collect());
    _dirty=false;
    st('✅ រក្សាទុករួច '+ts(),'ok');
  }catch(e){st('❌ '+e.message,'err');}
}

async function fbLoad(){
  const id=(document.getElementById('schoolInput').value||'').trim();
  if(!id){alert('សូមបញ្ចូលឈ្មោះ/លេខកូដសាលា');return;}
  if(!window.__fbReady){st('⏳ Firebase មិនទាន់ ready…','busy');return;}
  st('⏳ កំពុងទាញ…','busy');
  try{
    const data=await window.__fbLoad(id);
    if(!data){st('⚠️ រកមិនឃើញទិន្នន័យ','err');return;}
    populate(data);
    _dirty=false;
    st('✅ ទាញយករួច '+ts(),'ok');
  }catch(e){st('❌ '+e.message,'err');}
}

// ═══════════════════════════════════════════
//  EXPORT JSON
// ═══════════════════════════════════════════
function exportJSON(){
  const data=collect();
  const json=JSON.stringify(data,null,2);
  const blob=new Blob([json],{type:'application/json;charset=utf-8'});
  const school=(document.getElementById('schoolInput').value||'school').trim();
  dlBlob(blob,'standards_'+school+'.json');
  st('✅ Export JSON រួច','ok');
}

// ═══════════════════════════════════════════
//  IMPORT JSON
// ═══════════════════════════════════════════
function importJSON(e){
  const f=e.target.files[0];
  if(!f)return;
  const r=new FileReader();
  r.onload=ev=>{
    try{
      const data=JSON.parse(ev.target.result);
      populate(data);
      st('✅ Import រួច','ok');
    }catch(err){st('❌ JSON ខុស: '+err.message,'err');}
    e.target.value='';
  };
  r.readAsText(f);
}

// ═══════════════════════════════════════════
//  EXPORT EXCEL
// ═══════════════════════════════════════════
function exportExcel(){
  const wb=XLSX.utils.book_new();
  [['std1','ស្តង់ដា១'],['std2','ស្តង់ដា២'],['std3','ស្តង់ដា៣'],['std4','ស្តង់ដា៤'],['std5','ស្តង់ដា៥']]
  .forEach(([sid,name])=>{
    const rows=[['ល.រ','ពិន្ទុ','យោបល់']];
    document.querySelectorAll(`select.ss[data-s="${sid}"]`).forEach(s=>{
      const ta=document.querySelector(`textarea.ct[data-k="${s.dataset.k}"][data-s="${sid}"]`);
      rows.push([s.dataset.k, s.value||'', ta?ta.value:'']);
    });
    const ws=XLSX.utils.aoa_to_sheet(rows);
    ws['!cols']=[{wch:10},{wch:8},{wch:45}];
    XLSX.utils.book_append_sheet(wb,ws,name);
  });
  const school=(document.getElementById('schoolInput').value||'school').trim();
  XLSX.writeFile(wb,'standards_'+school+'.xlsx');
  st('✅ Excel រួច','ok');
}

// ═══════════════════════════════════════════
//  HELPERS
// ═══════════════════════════════════════════
function switchTab(id,btn){
  document.querySelectorAll('.tab-pane').forEach(p=>p.classList.remove('active'));
  document.querySelectorAll('.tab').forEach(b=>b.classList.remove('active'));
  document.getElementById('pane-'+id).classList.add('active');
  btn.classList.add('active');
}

function st(msg,cls){
  const el=document.getElementById('st');
  el.textContent=msg;
  el.className=cls;
}

function ts(){
  return new Date().toLocaleTimeString('km-KH');
}

function dlBlob(blob,fname){
  const url=URL.createObjectURL(blob);
  const a=document.createElement('a');
  a.href=url;
  a.download=fname;
  a.style.display='none';
  document.body.appendChild(a);
  a.click();
  setTimeout(()=>{ document.body.removeChild(a); URL.revokeObjectURL(url); },2000);
}

// ═══════════════════════════════════════════
//  INIT
// ═══════════════════════════════════════════

// ═══════════════════════════════════════════
//  SUMMARY PAGE
// ═══════════════════════════════════════════
const STD_INFO = [
  { id:'std1', name:'ស្តង់ដាទី១ លទ្ធផលសិក្សារបស់សិស្ស', label:'ស.១', maxPer:5 },
  { id:'std2', name:'ស្តង់ដាទី២ ការបង្រៀន និងរៀន', label:'ស.២', maxPer:5 },
  { id:'std3', name:'ស្តង់ដាទី៣ ការចូលរួមរបស់សហគមន៍', label:'ស.៣', maxPer:5 },
  { id:'std4', name:'ស្តង់ដាទី៤ ដំណើរការប្រត្តិបត្តិរបស់សាលរៀន', label:'ស.៤', maxPer:5 },
  { id:'std5', name:'ស្តង់ដាទី៥ គណនេយ្យភាពរបស់សាលារៀន', label:'ស.៥', maxPer:5 },
];

let _barChart=null,_radarChart=null,_doughChart=null,_hbarChart=null;
function destroyCharts(){
  [_barChart,_radarChart,_doughChart,_hbarChart].forEach(c=>{ if(c) c.destroy(); });
}

function getScoreColor(pct){
  if(pct>=80) return '#2e7d32';
  if(pct>=60) return '#1565c0';
  if(pct>=40) return '#f57c00';
  return '#c62828';
}

function buildSummary(){
  // Collect per-standard data
  const stdData = STD_INFO.map(info=>{
    const sels = [...document.querySelectorAll(`select.ss[data-s="${info.id}"]`)];
    let total=0, maxScore=0;
    const indicators = sels.map(s=>{
      const v = s.value===''?0:parseInt(s.value);
      total += v;
      maxScore += 5;
      const ta = document.querySelector(`textarea.ct[data-k="${s.dataset.k}"][data-s="${info.id}"]`);
      return {
        id: s.dataset.k,
        name: decodeURIComponent(s.dataset.nm||''),
        score: v,
        max: 5,
        pct: v>0?(v/5*100).toFixed(1):'0.0'
      };
    });
    return {
      ...info,
      indicators,
      total,
      maxScore,
      pct: maxScore>0?(total/maxScore*100).toFixed(1):'0.0'
    };
  });

  // ── Build table ──
  const tbody = document.getElementById('mainSumBody');
  tbody.innerHTML='';
  let grandTotal=0, grandMax=0;
  let rowNum=0;

  stdData.forEach(std=>{
    grandTotal += std.total;
    grandMax   += std.maxScore;

    // Standard header row
    const pctNum = parseFloat(std.pct);
    const color  = getScoreColor(pctNum);
    const badge  = `<span class="score-badge" style="background:${color}22;color:${color}">${std.pct}%</span>`;
    const tr0 = tbody.insertRow();
    tr0.className='tr-std';
    tr0.innerHTML=`<td colspan="2">${std.name}</td><td style="text-align:center;color:#fff;font-weight:700">${std.total}/${std.maxScore}</td><td>${badge}</td>`;

    // Indicator rows
    std.indicators.forEach(ind=>{
      rowNum++;
      const pN = parseFloat(ind.pct);
      const col = getScoreColor(pN);
      const bdg = ind.score>0?`<span class="score-badge" style="background:${col}22;color:${col}">${ind.pct}%</span>`:'<span style="color:#999">-</span>';
      const row = tbody.insertRow();
      row.innerHTML=`<td style="text-align:center;color:#888">${ind.id}</td>
        <td style="text-align:left;font-size:11.5px">${ind.name||ind.id}</td>
        <td style="text-align:center;font-weight:700">${ind.score>0?ind.score:'-'}</td>
        <td>${bdg}</td>`;
    });
  });

  // Grand total row
  const gPct = grandMax>0?(grandTotal/grandMax*100).toFixed(1):'0.0';
  const gColor = getScoreColor(parseFloat(gPct));
  const gRow = tbody.insertRow();
  gRow.className='tr-std';
  gRow.innerHTML=`<td colspan="2" style="text-align:left">🏆 សរុបរួម (ស្តង់ដាទាំង៥)</td>
    <td style="text-align:center;color:#fff;font-weight:700">${grandTotal}/${grandMax}</td>
    <td><span class="score-badge" style="background:${gColor}33;color:${gColor}">${gPct}%</span></td>`;

  // ── Charts ──
  destroyCharts();

  const labels  = stdData.map(s=>s.label);
  const totals  = stdData.map(s=>s.total);
  const maxes   = stdData.map(s=>s.maxScore);
  const pcts    = stdData.map(s=>parseFloat(s.pct));
  const bgColors= stdData.map(s=>getScoreColor(parseFloat(s.pct)));
  const bgAlpha = bgColors.map(c=>c+'33');

  // Bar chart
  _barChart = new Chart(document.getElementById('chartBar'),{
    type:'bar',
    data:{
      labels,
      datasets:[
        { label:'ពិន្ទុសរុប', data:totals, backgroundColor:bgAlpha, borderColor:bgColors, borderWidth:2, borderRadius:6 },
        { label:'អតិបរមា',    data:maxes,  backgroundColor:'#0000001a', borderColor:'#999', borderWidth:1, borderRadius:6, type:'bar' }
      ]
    },
    options:{
      responsive:true, maintainAspectRatio:false,
      plugins:{ legend:{position:'bottom',labels:{font:{size:11}}} },
      scales:{
        y:{ beginAtZero:true, title:{display:true,text:'ពិន្ទុ',font:{size:11}} },
        x:{ ticks:{font:{size:12}} }
      }
    }
  });

  // Radar chart
  _radarChart = new Chart(document.getElementById('chartRadar'),{
    type:'radar',
    data:{
      labels,
      datasets:[{
        label:'ភាគរយ(%)',
        data:pcts,
        backgroundColor:'rgba(21,101,192,0.15)',
        borderColor:'#1565c0',
        borderWidth:2,
        pointBackgroundColor:bgColors,
        pointRadius:5
      }]
    },
    options:{
      responsive:true, maintainAspectRatio:false,
      scales:{ r:{ min:0,max:100,ticks:{stepSize:20,font:{size:10}}, pointLabels:{font:{size:12}} } },
      plugins:{ legend:{position:'bottom',labels:{font:{size:11}}} }
    }
  });

  // Doughnut
  _doughChart = new Chart(document.getElementById('chartDoughnut'),{
    type:'doughnut',
    data:{
      labels:stdData.map(s=>s.name),
      datasets:[{ data:pcts, backgroundColor:bgAlpha, borderColor:bgColors, borderWidth:2 }]
    },
    options:{
      responsive:true, maintainAspectRatio:false,
      plugins:{
        legend:{position:'bottom',labels:{font:{size:11}}},
        tooltip:{ callbacks:{ label: ctx => ctx.label+': '+ctx.parsed.toFixed(1)+'%' } }
      }
    }
  });

  // Horizontal bar: score vs max per standard
  _hbarChart = new Chart(document.getElementById('chartHBar'),{
    type:'bar',
    data:{
      labels,
      datasets:[
        { label:'ពិន្ទុបាន', data:totals, backgroundColor:bgAlpha, borderColor:bgColors, borderWidth:2, borderRadius:4 },
        { label:'អតិបរមា',   data:maxes,  backgroundColor:'#e0e0e033', borderColor:'#bbb', borderWidth:1, borderRadius:4 }
      ]
    },
    options:{
      indexAxis:'y',
      responsive:true, maintainAspectRatio:false,
      plugins:{ legend:{position:'bottom',labels:{font:{size:11}}} },
      scales:{
        x:{ beginAtZero:true, title:{display:true,text:'ពិន្ទុ',font:{size:11}} },
        y:{ ticks:{font:{size:12}} }
      }
    }
  });
}

window.buildSummary=buildSummary;

window.switchTab=switchTab;
window.fbSave=fbSave;
window.fbLoad=fbLoad;
window.exportJSON=exportJSON;
window.importJSON=importJSON;
window.exportExcel=exportExcel;
window.onChange=onChange;
window.dirty=dirty;

document.addEventListener('DOMContentLoaded',()=>{
  document.querySelectorAll('.std-table').forEach(processTable);
  recalc();
  st('✅ រួចរាល់','ok');
  // debug: count selects per standard
  ['std1','std2','std3','std4','std5'].forEach(sid=>{
    const n=document.querySelectorAll(`select.ss[data-s="${sid}"]`).length;
    console.log(sid+': '+n+' selects');
  });
});
</script>
</template>
<!-- You can embed your entire teacher template body here -->
  <template id="tpl-rabies">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=0.85">
    <title>ទម្រង់ផ្តល់មតិត្រឡប់លើមេរៀនបណ្តុះបណ្តាល</title>
    <link href="https://fonts.googleapis.com/css2?family=Hanuman:wght@400;700&amp;family=Noto+Serif+Khmer:wght@400;600;700&amp;display=swap" rel="stylesheet">
    <!-- Firebase Realtime Database SDK (compat) -->
    <script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-database-compat.js"></script>
    <script src="https://cdn.sheetjs.com/xlsx-latest/package/dist/xlsx.full.min.js"></script>
    <style>
      :root {
        --blue-dark: #1a3a6e;
        --blue-mid: #1e5daa;
        --blue-light: #d6e8ff;
        --blue-pale: #eef5ff;
        --gold: #c8a84b;
        --green: #1b7c4e;
        --green-light: #e6f7ef;
        --red: #c0392b;
        --border: #c5d5e8;
        --bg: #f0f4fa;
        --white: #ffffff;
        --row-even: #f7faff;
        --summary-bg: #d6e8ff;
      }

      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      body {
        font-family: 'Hanuman', 'Noto Serif Khmer', serif;
        background: var(--bg);
        min-height: 100vh;
        padding: 24px 12px;
        color: #1a2744;
      }

      .wrapper {
        max-width: 1280px;
        margin: 0 auto;
        background: var(--white);
        border-radius: 12px;
        box-shadow: 0 4px 32px rgba(26, 58, 110, 0.13);
        overflow: hidden;
      }
      
      #loginModal {
       display: none !important;
     }

      /* ── Header ── */
      .header {
        background: linear-gradient(135deg, var(--blue-dark) 0%, var(--blue-mid) 100%);
        color: white;
        padding: 18px 28px 14px;
        border-bottom: 5px solid var(--gold);
      }

      .header-top {
        text-align: center;
        margin-bottom: 12px;
      }

      .header-top h1 {
        font-size: 1.2rem;
        font-weight: 700;
        line-height: 1.7;
        margin-bottom: 12px;
      }

      .header-form-title {
        font-size: 1.1rem;
        font-weight: 700;
        line-height: 1.7;
        text-align: center;
      }

      color: var(--gold);
      text-align: center;
      }

      .header-divider {
        color: var(--gold);
        margin: 2px 0;
      }

      .header-body {
        display: flex;
        justify-content: space-between;
        align-items: flex-end;
        flex-wrap: wrap;
        gap: 8px;
      }

      .header-office {
        font-size: 1.1rem;
        line-height: 1.8;
        opacity: 0.93;
        text-align: left;
        margin-bottom: 18px;
      }

      .header-form-title {
        font-size: 1.1rem;
        font-weight: 700;
      }

      color: var(--gold);
      text-align: center;
      }

      /* ── DB Indicator ── */
      #dbIndicator {
        display: flex;
        align-items: center;
        gap: 8px;
        padding: 8px 20px;
        background: #1a2744;
        color: #aac8ff;
        font-size: 0.05rem;
        font-weight: 600;
        letter-spacing: 0.02em;
      }

      .dot {
        width: 10px;
        height: 5px;
        border-radius: 50%;
        background: #555;
        transition: background 0.4s;
      }

      .dot.online {
        background: #22c55e;
        box-shadow: 0 0 6px #22c55e;
      }

      .dot.offline {
        background: var(--red);
      }

      .dot.syncing {
        background: var(--gold);
        animation: pulse 0.8s infinite alternate;
      }

      @keyframes pulse {
        to {
          opacity: 0.4;
        }
      }

      /* ── Status bar ── */
      #statusBar {
        display: none;
        padding: 9px 24px;
        font-size: 0.05rem;
        font-weight: 600;
        align-items: center;
        gap: 10px;
      }

      #statusBar.success {
        background: var(--green-light);
        color: var(--green);
        display: flex;
      }

      #statusBar.error {
        background: #fde8e8;
        color: var(--red);
        display: flex;
      }

      #statusBar.loading {
        background: var(--blue-pale);
        color: var(--blue-mid);
        display: flex;
      }

      /* ── Info ── */
      .info-section {
        padding: 16px 28px;
        background: var(--blue-pale);
        border-bottom: 1px solid var(--border);
        font-size: 0.85rem;
        line-height: 1.9;
        color: #334;
      }

      .info-section ul {
        padding-left: 20px;
        margin-top: 4px;
      }

      /* ── Toolbar ── */
      .toolbar {
        padding: 5px 8px;
        border-bottom: 1px solid var(--border);
        display: flex;
        gap: 3px;
        flex-wrap: wrap;
        align-items: center;
        justify-content: space-between;
        background: #f7faff;
      }

      .toolbar-left {
        display: flex;
        gap: 8px;
        flex-wrap: wrap;
        align-items: center;
      }

      /* ── Buttons ── */
      .btn {
        padding: 8px 16px;
        border: none;
        border-radius: 7px;
        font-family: inherit;
        font-size: 0.85rem;
        font-weight: 700;
        cursor: pointer;
        transition: background 0.2s, transform 0.1s;
        display: inline-flex;
        align-items: center;
        gap: 5px;
      }

      .btn:active {
        transform: scale(0.97);
      }

      .btn-blue {
        background: var(--blue-mid);
        color: white;
      }

      .btn-blue:hover {
        background: var(--blue-dark);
      }

      .btn-green {
        background: var(--green);
        color: white;
      }

      .btn-green:hover {
        background: #155c3a;
      }

      .btn-gold {
        background: var(--gold);
        color: white;
      }

      .btn-gold:hover {
        background: #a8882f;
      }

      .btn-red {
        background: var(--red);
        color: white;
        font-size: 0.76rem;
        padding: 4px 9px;
        border-radius: 5px;
      }

      .btn-red:hover {
        background: #a93226;
      }

      .badge {
        background: var(--blue-light);
        color: var(--blue-dark);
        border-radius: 20px;
        padding: 3px 12px;
        font-size: 0.8rem;
        font-weight: 700;
      }

      /* ── Table ── */
      .table-wrapper {
        overflow-x: auto;
      }

      table {
        width: 100%;
        border-collapse: collapse;
        font-size: 0.8rem;
      }

      thead th {
        background: var(--blue-dark);
        color: white;
        padding: 7px 5px;
        text-align: center;
        border: 1px solid #2a4f8a;
        line-height: 1.4;
        white-space: nowrap;
      }

      thead tr:nth-child(2) th {
        background: var(--blue-mid);
      }

      thead tr:nth-child(3) th {
        background: #2a6bc7;
      }

      thead tr:first-child th {
        background: #0f2550;
        font-size: 0.82rem;
      }

      tbody tr:nth-child(even) td {
        background: var(--row-even);
      }

      tbody tr:nth-child(odd) td {
        background: #fff;
      }

      tbody tr:hover td {
        background: #e8f0fc !important;
      }

      td {
        border: 1px solid var(--border);
        padding: 4px 3px;
        text-align: center;
        vertical-align: middle;
      }

      td input {
        width: 100%;
        border: 1px solid transparent;
        padding: 3px 3px;
        text-align: center;
        font-family: inherit;
        font-size: 0.8rem;
        background: transparent;
        border-radius: 4px;
        color: #1a2744;
        transition: border-color 0.15s, background 0.15s;
      }

      td input:focus {
        outline: none;
        border-color: var(--blue-mid);
        background: white;
        box-shadow: 0 0 0 2px rgba(30, 93, 170, 0.15);
      }

      td input[type="date"] {
        min-width: 108px;
      }

      td input.name-input {
        min-width: 108px;
        text-align: left;
      }

      td input.class-input {
        min-width: 42px;
      }

      td.total-cell {
        background: #dbeeff !important;
        font-weight: 700;
        color: var(--blue-dark);
      }

      td.bite-cell {
        color: var(--red);
        font-weight: 700;
      }

      .summary-row td {
        background: var(--summary-bg) !important;
        font-weight: 700;
        color: var(--blue-dark);
        border-color: #a0bde0;
      }

      #s_pt,
      #s_pf {
        background: #bbd6ff !important;
      }

      #s_bite {
        color: var(--red);
      }

      /* ── Coord row in thead ── */
      .coord-input {
        background: rgba(255, 255, 255, 0.15);
        border: 1px solid rgba(255, 255, 255, 0.4);
        border-radius: 5px;
        padding: 3px 8px;
        color: white;
        font-family: inherit;
        font-size: 0.82rem;
        width: 150px;
      }

      .coord-input::placeholder {
        color: rgba(255, 255, 255, 0.5);
      }

      .coord-input:focus {
        outline: none;
        background: rgba(255, 255, 255, 0.25);
      }

      /* ── Footer ── */
      .footer-section {
        padding: 20px 28px;
        border-top: 0px solid var(--border);
        font-size: 0.85rem;
        line-height: 1.8;
        color: #334;
      }

      .footer-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 24px;
        margin-top: 14px;
      }

      @media (max-width: 640px) {
        .footer-grid {
          grid-template-columns: 1fr;
        }
      }

      .signature-box {
        text-align: center;
      }

      .sig-title {
        font-weight: 700;
        color: var(--blue-dark);
      }

      .signature-line {
        border-bottom: 1px solid #aaa;
        width: 80%;
        margin: 44px auto 4px;
      }

      .comment-lines .line {
        border-bottom: 1px solid #ccc;
        height: 26px;
        margin-bottom: 8px;
      }

      /* Spinner */
      .spinner {
        display: inline-block;
        width: 14px;
        height: 14px;
        border: 2px solid currentColor;
        border-top-color: transparent;
        border-radius: 50%;
        animation: spin 0.7s linear infinite;
      }

      @keyframes spin {
        to {
          transform: rotate(360deg);
        }
      }

      @media print {

        .btn,
        /* លាក់ប៊ូតុងទាំងអស់ */
        .delete-col,
        /* លាក់កូឡុំលុប */
        .btn-red {
          display: none !important;
        }

        /* លាក់ប៊ូតុង delete ផង */
        /* លាក់ column លុប ក្នុងតារាង */
        table#feedbackTable th.delete-col,
        table#feedbackTable td.delete-col {
          display: none !important;
        }
      }

    </style>
  
  

 
    <div class="wrapper">
      <!-- Header -->
      <div class="header">
        <div class="header-top">
          <h1>ព្រះរាជាណាចក្រកម្ពុជា <br>ជាតិ   សាសនា   ព្រះមហាក្សត្រ </h1>
          <div class="header-divider">✦✦✦✦✦✦✦</div>
        </div>
        <div class="header-body">
          <div class="header-office"> ការិយាល័យអប់រំ យុវជន និងកីឡានៃរដ្ឋបាលស្រុកភ្នំស្រុក <br> សាលាបឋមសិក្សា រោគ </div>
        </div>
        <div class="header-form-title">ទម្រង់ផ្តល់មតិត្រឡប់លើមេរៀនបណ្តុះបណ្តាល</div>
      </div>
    </div>

    <!-- Info -->
    <div class="info-section">
      <p>ទម្រង់នេះ មានសារៈសំខាន់ណាស់ដើម្បីប្រមូលទិន្នន័យអំពីចំនួនសិស្សដែលបានចូលរួមក្នុងការអប់រំទាក់ទងនឹងជំងឺឆ្កែឆ្កួត។</p>
      <ul>
        <li>បន្ទាប់ពីបញ្ចប់មេរៀននីមួយៗ សូមលោកគ្រូ អ្នកគ្រូ ជួយបំពេញព័ត៌មានក្នុងតារាងរបាយការណ៍ខាងក្រោម។</li>
        <li>សូមផ្តល់របាយការណ៍ជូនបុគ្គលិកទីចាត់ការសាលារៀន។</li>
      </ul>
    </div>
    <!-- Toolbar -->
    <div class="toolbar">
      <div class="toolbar-left">
        <!-- បន្ថែមប៊ូតុងក្នុង toolbar -->
        <button class="btn btn-blue" onclick="printPDF()">🖨️ Print PDF</button>
        <button class="btn btn-blue" onclick="downloadXLSX()">⬇️  XLSX</button>
        <button class="btn btn-blue" onclick="downloadJSON()">⬇️  JSON</button>
        <button class="btn btn-green" onclick="addRow()">＋ បន្ថែមជួរ</button>
        <button class="btn btn-blue" onclick="saveAll()">
          <span id="saveIcon">💾</span> រក្សាទុក </button>
        <button class="btn btn-gold" onclick="loadOnce()">↺ ផ្ទុកឡើងវិញ</button>
       <span class="badge" id="rowCount">0 ជួរ</span>
      </div>
      <div style="display:flex; gap:8px; align-items:center; flex-wrap:wrap;">
        <span style="font-size:0.82rem; color:var(--blue-dark); font-weight:600;">Live sync:</span>
        <label style="display:flex;align-items:center;gap:5px;font-size:0.82rem;cursor:pointer;">
          <input type="checkbox" id="liveToggle" onchange="toggleLive(this.checked)" checked=""> បើក Auto-sync </label>
      </div>
    </div>
    <!-- Table -->
    <div class="table-wrapper">
      <table id="feedbackTable">
        <thead>
          <!-- Coordinator row -->
          <tr>
            <th colspan="8" style="text-align:left; padding-left:15px;"> ឈ្មោះបុគ្គលិកទីចាត់ការ (លេខា) : <input class="coord-input" id="coordinatorName" value="អ៊ុន ប៊ុនទុង" placeholder="ឈ្មោះ..."> ទូរស័ព្ទ: <input class="coord-input" id="phoneNumber" style="width:120px;" value="17407773" placeholder="លេខ...">
            </th>
            <th colspan="6"></th>
            <th colspan="2">
              <button class="btn btn-gold" style="padding:4px 10px; font-size:0.78rem;" onclick="saveCoordinator()">💾 រក្សាទុក</button>
            </th>
            <th></th>
          </tr>
          <tr>
            <th rowspan="3">កាលបរិច្ឆេទ</th>
            <th rowspan="3">ឈ្មោះគ្រូ</th>
            <th rowspan="3">ថ្នាក់</th>
            <th colspan="10">ចន្លោះអាយុសិស្ស</th>
            <th colspan="2" rowspan="2">ចំនួនសិស្ស <br>ចូលរួម </th>
            <th rowspan="3">ចំនួនសិស្ស <br>ត្រូវឆ្កែខាំ <br>១ឆ្នាំមុន </th>
            <th class="delete-col" rowspan="4">លុប</th>
          </tr>
          <tr>
            <th colspan="2">ក្រោម៦ឆ្នាំ</th>
            <th colspan="2">៦–៧ឆ្នាំ</th>
            <th colspan="2">៨–៩ឆ្នាំ</th>
            <th colspan="2">១០–១១ឆ្នាំ</th>
            <th colspan="2">ចាប់ពី១២ឆ្នាំឡើង</th>
          </tr>
          <tr>
            <th>សរុប</th>
            <th>ស្រី</th>
            <th>សរុប</th>
            <th>ស្រី</th>
            <th>សរុប</th>
            <th>ស្រី</th>
            <th>សរុប</th>
            <th>ស្រី</th>
            <th>សរុប</th>
            <th>ស្រី</th>
            <th>សរុប</th>
            <th>ស្រី</th>
          </tr>
        </thead>
        <tbody id="tableBody"></tbody>
        <tfoot>
          <tr class="summary-row">
            <td colspan="3" style="text-align:left;padding-left:10px;">សរុបរួម</td>
            <td id="s_u6t"></td>
            <td id="s_u6f"></td>
            <td id="s_67t"></td>
            <td id="s_67f"></td>
            <td id="s_89t"></td>
            <td id="s_89f"></td>
            <td id="s_1011t"></td>
            <td id="s_1011f"></td>
            <td id="s_12t"></td>
            <td id="s_12f"></td>
            <td id="s_pt"></td>
            <td id="s_pf"></td>
            <td id="s_bite"></td>
            <td></td>
          </tr>
        </tfoot>
      </table>
    </div>
    <!-- Footer -->
    <div class="footer-section">
      <p> - ពេលបំពេញទម្រង់នេះរួចរាល់ សូមផ្ញើទម្រង់នេះទៅកាន់មន្ត្រីអប់រំខណ្ឌ។ ប្រសិនបើមានរូបថតពេលបង្រៀន ក៏សូមផ្ញើទៅកាន់មន្ត្រីអប់រំខណ្ឌផងដែរ។ <br> - ប្រសិនលោកគ្រូ អ្នកគ្រូ មានសំណួរ ឬការប្រឈមទាក់ទងនឹងទម្រង់ សូមមេត្តាទំនាក់ទំនងមកកាន់មន្ត្រីអប់រំខណ្ឌ ឬគ្រុបតេឡេក្រាមគ្រូបង្រៀនប្រចាំខេត្តរបស់ខ្លួន។ </p>
    </div>
    <div class="footer-grid" style="grid-template-columns: 1fr 1fr;">
      <div>
        <p style="font-weight:700; color: var(--blue-dark);">ផ្តល់មតិយោបល់ ឬសំណូមពរប្រសិនបើមាន៖</p>
        <div class="comment-lines" style="margin-top:10px;">
          <div class="line"></div>
          <div class="line"></div>
          <div class="line"></div>
        </div>
      </div>

<div class="signature-box" style="display: flex; flex-direction: column; gap: 4px; align-items: flex-end; width: fit-content;">
    <p id="khmer-lunar" style="font-size:0.83rem; color:#555; align-left: flex-start; margin: 0;"></p>
<div style="font-size:0.83rem; color:#555; align-self: flex-start;">រោគ <span id="khmer-solar" style="font-size:0.83rem; color:#555; align-left; margin: 0;"><p></p>
    </span></div>
    <p class="sig-title" style="width: 100%; text-align: center; margin-top: 8px; font-weight: bold;">នាយិកាសាលា</p>
</div>
</div>   
<script>
  function toKhNum(n){ const d=['០','១','២','៣','៤','៥','៦','៧','៨','៩']; return String(n).replace(/\d/g,c=>d[+c]); }
  const KH_MONTHS_SOLAR=['មករា','កុម្ភៈ','មីនា','មេសា','ឧសភា','មិថុនា','កក្កដា','សីហា','កញ្ញា','តុលា','វិច្ឆិកា','ធ្នូ'];
  const KH_WEEKDAYS=['អាទិត្យ','ចន្ទ','អង្គារ','ពុធ','ព្រហស្បតិ៍','សុក្រ','សៅរ៍'];
  const KH_ANIMALS=['ជូត','ឆ្លូវ','ខាល','ថោះ','រោង','ម្សាញ់','មមី','មមែ','វក','រកា','ច','កុរ'];
  const KH_SAK=['ឯក','ទោ','ត្រី','ចត្វា','បញ្ចស័ក','ឆ','សប្ត','អដ្ឋ','នព','សំរឹទ្ធ'];
  
  function moonPhase(date){ const r=new Date('2000-01-06T18:14:00Z'),syn=29.53059,diff=(date-r)/864e5+7/24; return((diff%syn)+syn)%syn; }
  
  function khLunarMonth(nm){ const m=nm.getMonth(),d=nm.getDate(),ranges=[[1,6,2,17,'ផល្គុន'],[2,18,3,16,'ចេត្រ'],[3,17,4,15,'វិសាខ'],[4,16,5,14,'ជេស្ឋ'],[5,15,6,13,'អាសាឍ'],[6,14,7,12,'ស្រាពណ៍'],[7,13,8,10,'ភទ្របទ'],[8,11,9,9,'អស្សុជ'],[9,10,10,8,'កក្តិក'],[10,9,11,7,'មិគសិរ'],[11,8,0,6,'បុស្ស']]; for(const[sm,sd,em,ed,name]of ranges){ if(sm>em){ if(m===sm&&d>=sd)return name; if(m===em&&d<=ed)return name; } else{ if(m===sm&&d>=sd&&(m!==em||d<=ed))return name; if(m>sm&&m<em)return name; if(m===em&&d<=ed)return name; } } return'មាឃ'; }
  
  function khAnimal(date){ const y=date.getFullYear(),mo=date.getMonth(),dy=date.getDate(),adj=mo<3||(mo===3&&dy<14)?y-1:y; return KH_ANIMALS[(((adj-2025+5)%12)+12)%12]; }
  
  function khSak(date){ return KH_SAK[(date.getFullYear()+543+8)%10]; }
  
  function fmtKhDate(date){ const ph=moonPhase(date),raw=Math.floor(ph); const dayType=raw<15?'កើត':'រោច',dayNum=raw<15?raw+1:raw-14; const nm=new Date(date-ph*864e5); const lunar=`ថ្ងៃ${KH_WEEKDAYS[date.getDay()]} ${toKhNum(dayNum)}${dayType} ខែ${khLunarMonth(nm)} ឆ្នាំ${khAnimal(date)} ${khSak(date)}ស័ក ព.ស ${toKhNum(date.getFullYear()+543+1)}`; const solar=`ថ្ងៃទី${toKhNum(date.getDate())} ខែ${KH_MONTHS_SOLAR[date.getMonth()]} ឆ្នាំ${toKhNum(date.getFullYear())}`; return{lunar,solar}; }

  // ══════ RUN AUTOMATICALLY ON LOAD ══════
  const today = new Date();
  const khmerDate = fmtKhDate(today);
  
  // ចាក់ទិន្នន័យចូលទៅក្នុង HTML tags
  document.getElementById('khmer-lunar').innerText = khmerDate.lunar;
  document.getElementById('khmer-solar').innerText = khmerDate.solar;
</script>

  <div class="modal-bg" id="loginModal" style="display:flex;">
  <div class="modal" style="max-width: 360px; padding: 24px;">
    <div class="modal-head" style="justify-content: center;">
      <h2>Login</h2>
    </div>
    <div class="modal-body" style="padding: 20px 0;">
      <div class="form-field">
        <label for="loginUsername">Username</label>
        <input type="text" id="loginUsername" placeholder="Enter username">
      </div>
      <div class="form-field" style="margin-top: 12px;">
        <label for="loginPassword">Password</label>
        <input type="password" id="loginPassword" placeholder="Enter password">
      </div>
      <button onclick="login()" style="
        margin-top: 25px;
        width: 100%;
        background: var(--mid);
        color: white;
        border: none;
        border-radius: 14px;
        padding: 15px;
        font-weight: 600;
        cursor: pointer;">Login</button>
    </div>
 </div>

     <script>
  // Simple login function with hardcoded credentials for demo
  function login() {
    const user = document.getElementById('loginUsername').value.trim();
    const pass = document.getElementById('loginPassword').value;
    if (user === 'teacher' && pass === '01030401017') {
      document.getElementById('loginModal').style.display = 'none';
      document.getElementById('loginModal').style.display = 'none';
      alert('Welcome, ' + user + '!');
      // Place additional init code here if needed after login
    } else {
      alert('Invalid username or password!');
    }
  }
</script>

    <!-- /wrapper -->
    <script>
      // ═══════════════════════════════════════════════
      //  Firebase — Realtime Database
      // ═══════════════════════════════════════════════
      const firebaseConfig = {
        apiKey: "AIzaSyB35WLr1y5_QT3j-0x7Mb2F7QaaYXLdIcQ",
        authDomain: "packagedemo-b600c.firebaseapp.com",
        databaseURL: "https://packagedemo-b600c-default-rtdb.asia-southeast1.firebasedatabase.app",
        projectId: "packagedemo-b600c",
        storageBucket: "packagedemo-b600c.firebasestorage.app",
        messagingSenderId: "601958630212",
        appId: "1:601958630212:web:e140ee683e203f3e464d11"
      };
      firebase.initializeApp(firebaseConfig);
      const db = firebase.database();
      const rowsRef = db.ref("feedbackRows");
      const coordRef = db.ref("coordinator");
      // ═══════════════════════════════════════════════
      //  Connection state indicator
      // ═══════════════════════════════════════════════
      db.ref(".info/connected").on("value", snap => {
        const online = snap.val() === true;
        const dot = document.getElementById("dbDot");
        const label = document.getElementById("dbLabel");
        dot.className = "dot " + (online ? "online" : "offline");
        label.textContent = online ? "✅ ភ្ជាប់ Firebase Realtime Database រួចរាល់" : "❌ បាត់ការភ្ជាប់ — កំពុងព្យាយាមភ្ជាប់ម្តងទៀត...";
      });



      // ═══════════════════════════════════════════════
      //  Status bar
      // ═══════════════════════════════════════════════
      let statusTimer;

      function showStatus(msg, type = "success", spinner = false) {
        clearTimeout(statusTimer);
        const bar = document.getElementById("statusBar");
        bar.innerHTML = (spinner ? ' < span class = "spinner" >< /span> ' : '') + msg;
        bar.className = type;
        if (type === "success") statusTimer = setTimeout(() => bar.style.display = "none", 3500);
      }
      // ═══════════════════════════════════════════════
      //  Seed data
      // ═══════════════════════════════════════════════
      const seedData = [{
        date: "2026-05-09",
        teacher: "ស្វាង មនោរម្យ",
        cls: "5A",
        u6t: "",
        u6f: "",
        r67t: "",
        r67f: "",
        r89t: "",
        r89f: "",
        r1011t: "23",
        r1011f: "11",
        r12t: "1",
        r12f: "0",
        pt: "24",
        pf: "11",
        bite: "3"
      }, {
        date: "2026-05-09",
        teacher: "ឈួត សេរ៉ូម",
        cls: "6A",
        u6t: "",
        u6f: "",
        r67t: "",
        r67f: "",
        r89t: "",
        r89f: "",
        r1011t: "25",
        r1011f: "14",
        r12t: "7",
        r12f: "1",
        pt: "32",
        pf: "15",
        bite: "0"
      }, {
        date: "2026-05-09",
        teacher: "ប៊ី ពិសី",
        cls: "3A",
        u6t: "",
        u6f: "",
        r67t: "",
        r67f: "",
        r89t: "15",
        r89f: "9",
        r1011t: "6",
        r1011f: "2",
        r12t: "1",
        r12f: "1",
        pt: "22",
        pf: "12",
        bite: "0"
      }, {
        date: "2026-05-09",
        teacher: "ប៉ោង ស្រីពេជ្រ",
        cls: "2A",
        u6t: "",
        u6f: "",
        r67t: "18",
        r67f: "11",
        r89t: "",
        r89f: "",
        r1011t: "",
        r1011f: "",
        r12t: "",
        r12f: "",
        pt: "18",
        pf: "11",
        bite: "3"
      }, {
        date: "2026-05-11",
        teacher: "ឆេន សាវដា",
        cls: "4A",
        u6t: "",
        u6f: "",
        r67t: "",
        r67f: "",
        r89t: "",
        r89f: "",
        r1011t: "16",
        r1011f: "9",
        r12t: "7",
        r12f: "1",
        pt: "23",
        pf: "10",
        bite: "4"
      }, {
        date: "2026-05-11",
        teacher: "លេង ចាន់លាវ",
        cls: "2B",
        u6t: "",
        u6f: "",
        r67t: "21",
        r67f: "10",
        r89t: "1",
        r89f: "0",
        r1011t: "",
        r1011f: "",
        r12t: "",
        r12f: "",
        pt: "22",
        pf: "10",
        bite: "5"
      }, {
        date: "2026-05-11",
        teacher: "រ៉ោម សម្ផស្ស",
        cls: "5B",
        u6t: "",
        u6f: "",
        r67t: "",
        r67f: "",
        r89t: "",
        r89f: "",
        r1011t: "14",
        r1011f: "5",
        r12t: "9",
        r12f: "6",
        pt: "23",
        pf: "11",
        bite: "0"
      }, {
        date: "2026-05-11",
        teacher: "អឿន សុខៀប",
        cls: "4B",
        u6t: "",
        u6f: "",
        r67t: "",
        r67f: "",
        r89t: "",
        r89f: "",
        r1011t: "22",
        r1011f: "11",
        r12t: "2",
        r12f: "0",
        pt: "24",
        pf: "11",
        bite: "2"
      }, {
        date: "2026-05-12",
        teacher: "អេង ផល្លែន",
        cls: "3B",
        u6t: "",
        u6f: "",
        r67t: "",
        r67f: "",
        r89t: "16",
        r89f: "9",
        r1011t: "",
        r1011f: "",
        r12t: "",
        r12f: "",
        pt: "16",
        pf: "9",
        bite: "2"
      }, {
        date: "2026-05-12",
        teacher: "ពាន ណូរ៉ា",
        cls: "ម.ត",
        u6t: "35",
        u6f: "20",
        r67t: "",
        r67f: "",
        r89t: "",
        r89f: "",
        r1011t: "",
        r1011f: "",
        r12t: "",
        r12f: "",
        pt: "35",
        pf: "20",
        bite: "3"
      }];
      // ═══════════════════════════════════════════════
      //  Row builder
      // ═══════════════════════════════════════════════
      let rowCounter = 0;
      const FIELDS = ["date", "teacher", "cls", "u6t", "u6f", "r67t", "r67f", "r89t", "r89f", "r1011t", "r1011f", "r12t", "r12f", "pt", "pf", "bite"];

      function buildRow(d = {}, key = null) {
        const tr = document.createElement("tr");
        if (key) tr.dataset.key = key;
        FIELDS.forEach(f => {
          const td = document.createElement("td");
          if (f === "pt" || f === "pf") td.className = "total-cell";
          if (f === "bite") td.className = "bite-cell";
          const inp = document.createElement("input");
          inp.type = f === "date" ? "date" : "text";
          inp.value = d[f] !== undefined ? d[f] : "";
          inp.dataset.field = f;
          if (f === "teacher") inp.className = "name-input";
          if (f === "cls") inp.className = "class-input";
          inp.oninput = () => {
            updateSummary();
            autoSaveRow(tr);
          };
          td.appendChild(inp);
          tr.appendChild(td);
        });
        // Delete btn
        const tdDel = document.createElement("td");
        const btn = document.createElement("button");
        btn.textContent = "✕";
        btn.className = "btn btn-red";
        btn.onclick = () => deleteRow(tr);
        tdDel.appendChild(btn);
        tr.appendChild(tdDel);
        return tr;
      }

      function addRow(data = {}, key = null) {
        const tr = buildRow(data, key);
        document.getElementById("tableBody").appendChild(tr);
        updateSummary();
        updateCount();
        return tr;
      }
      // ═══════════════════════════════════════════════
      //  Summary + count
      // ═══════════════════════════════════════════════
      const SUM_FIELDS = ["u6t", "u6f", "r67t", "r67f", "r89t", "r89f", "r1011t", "r1011f", "r12t", "r12f", "pt", "pf", "bite"];
      const SUM_IDS = ["s_u6t", "s_u6f", "s_67t", "s_67f", "s_89t", "s_89f", "s_1011t", "s_1011f", "s_12t", "s_12f", "s_pt", "s_pf", "s_bite"];

      function updateSummary() {
        const tot = {};
        SUM_FIELDS.forEach(f => tot[f] = 0);
        document.querySelectorAll("#tableBody tr").forEach(tr => {
          SUM_FIELDS.forEach(f => {
            const inp = tr.querySelector(`input[data-field="${f}"]`);
            if (inp) tot[f] += parseInt(inp.value) || 0;
          });
        });
        SUM_FIELDS.forEach((f, i) => {
          const el = document.getElementById(SUM_IDS[i]);
          if (el) el.textContent = tot[f] || "";
        });
      }

      function updateCount() {
        const n = document.querySelectorAll("#tableBody tr").length;
        document.getElementById("rowCount").textContent = n + " ជួរ";
      }
      // ═══════════════════════════════════════════════
      //  Collect row data
      // ═══════════════════════════════════════════════
      function rowToObj(tr) {
        const obj = {};
        tr.querySelectorAll("input[data-field]").forEach(inp => {
          obj[inp.dataset.field] = inp.value;
        });
        return obj;
      }
      // ═══════════════════════════════════════════════
      //  Live sync (Realtime Database listener)
      // ═══════════════════════════════════════════════
      let liveListener = null;
      let ignoreNext = false; // prevent echo when we write
      function toggleLive(on) {
        if (on) {
          startLive();
        } else {
          if (liveListener) {
            rowsRef.off("value", liveListener);
            liveListener = null;
          }
          showStatus("⏸ Auto-sync បិទ — ត្រូវវាយដៃ រក្សាទុក", "loading");
        }
      }

      function startLive() {
        if (liveListener) rowsRef.off("value", liveListener);
        liveListener = rowsRef.on("value", snap => {
          if (ignoreNext) {
            ignoreNext = false;
            return;
          }
          const val = snap.val();
          renderFromDB(val);
        }, err => {
          showStatus("❌ Live sync error: " + err.message, "error");
        });
        showStatus("🔴 Live auto-sync បានបើក", "success");
      }

      function renderFromDB(val) {
        const tbody = document.getElementById("tableBody");
        tbody.innerHTML = "";
        rowCounter = 0;
        if (val) {
          // val is an object keyed by push-id
          const sorted = Object.entries(val).sort((a, b) => (a[1].order || 0) - (b[1].order || 0));
          sorted.forEach(([key, data]) => addRow(data, key));
        } else {
          // No data — load seed
          seedData.forEach(d => addRow(d));
          showStatus("⚠️ គ្មានទិន្នន័យ — ប្រើ seed data", "loading");
        }
      }
      // ═══════════════════════════════════════════════
      //  Save all rows (replaces entire /feedbackRows)
      // ═══════════════════════════════════════════════
      async function saveAll() {
        document.getElementById("saveIcon").textContent = "⏳";
        showStatus("កំពុងរក្សាទុក...", "loading", true);
        try {
          const obj = {};
          let i = 0;
          document.querySelectorAll("#tableBody tr").forEach(tr => {
            const key = tr.dataset.key || rowsRef.push().key;
            tr.dataset.key = key;
            obj[key] = {
              ...rowToObj(tr),
              order: i++,
              updatedAt: Date.now()
            };
          });
          ignoreNext = true;
          await rowsRef.set(obj);
          showStatus("✅ រក្សាទុករួចរាល់! (" + i + " ជួរ)", "success");
        } catch (e) {
          showStatus("❌ " + e.message, "error");
        }
        document.getElementById("saveIcon").textContent = "💾";
      }
      // ═══════════════════════════════════════════════
      //  Auto-save single row on edit
      // ═══════════════════════════════════════════════
      const saveTimers = {};

      function autoSaveRow(tr) {
        const key = tr.dataset.key;
        if (!key || !document.getElementById("liveToggle").checked) return;
        clearTimeout(saveTimers[key]);
        saveTimers[key] = setTimeout(async () => {
          try {
            ignoreNext = true;
            await rowsRef.child(key).update({
              ...rowToObj(tr),
              updatedAt: Date.now()
            });
            const dot = document.getElementById("dbDot");
            dot.className = "dot syncing";
            setTimeout(() => dot.className = "dot online", 600);
          } catch (e) {
            console.error(e);
          }
        }, 800);
      }
      // ═══════════════════════════════════════════════
      //  Delete single row
      // ═══════════════════════════════════════════════
      async function deleteRow(tr) {
        const key = tr.dataset.key;
        tr.remove();
        updateSummary();
        updateCount();
        if (key) {
          try {
            ignoreNext = true;
            await rowsRef.child(key).remove();
          } catch (e) {
            showStatus("❌ " + e.message, "error");
          }
        }
      }
      // ═══════════════════════════════════════════════
      //  Manual reload
      // ═══════════════════════════════════════════════
      async function loadOnce() {
        showStatus("កំពុងផ្ទុក...", "loading", true);
        try {
          const snap = await rowsRef.once("value");
          renderFromDB(snap.val());
          showStatus("✅ ផ្ទុករួចរាល់!", "success");
        } catch (e) {
          showStatus("❌ " + e.message, "error");
        }
      }
      // ═══════════════════════════════════════════════
      //  Save coordinator
      // ═══════════════════════════════════════════════
      async function saveCoordinator() {
        showStatus("កំពុងរក្សាទុកព័ត៌មានបុគ្គលិក...", "loading", true);
        try {
          await coordRef.set({
            name: document.getElementById("coordinatorName").value,
            phone: document.getElementById("phoneNumber").value,
            updatedAt: Date.now()
          });
          showStatus("✅ ព័ត៌មានបុគ្គលិករក្សាទុករួច!", "success");
        } catch (e) {
          showStatus("❌ " + e.message, "error");
        }
      }
      // ═══════════════════════════════════════════════
      //  Init
      // ═══════════════════════════════════════════════
      (async () => {
        // Load coordinator
        try {
          const snap = await coordRef.once("value");
          const c = snap.val();
          if (c) {
            document.getElementById("coordinatorName").value = c.name || "";
            document.getElementById("phoneNumber").value = c.phone || "";
          }
        } catch (e) {
          /* ignore */
        }
        // Start live listener
        startLive();
      })();
      // Print PDF (using browser print)
      function printPDF() {
        window.print();
      }
      // Download JSON file
      function downloadJSON() {
        const data = [];
        document.querySelectorAll("#tableBody tr").forEach(tr => {
          const rowData = {};
          tr.querySelectorAll("input[data-field]").forEach(inp => {
            rowData[inp.dataset.field] = inp.value;
          });
          data.push(rowData);
        });
        const blob = new Blob([JSON.stringify(data, null, 2)], {
          type: "application/json"
        });
        const url = URL.createObjectURL(blob);
        const a = document.createElement("a");
        a.href = url;
        a.download = "feedback_data.json";
        a.click();
        URL.revokeObjectURL(url);
      }

      function downloadXLSX() {
        // Prepare worksheet data: header + rows
        const ws_data = [];
        // Get headers text from table
        const headers = Array.from(document.querySelectorAll("#feedbackTable thead tr:last-child th")).map(th => th.textContent.trim());
        ws_data.push(headers);
        // Get rows data
        document.querySelectorAll("#tableBody tr").forEach(tr => {
          const row = [];
          tr.querySelectorAll("input[data-field]").forEach(inp => {
            row.push(inp.value);
          });
          // Add empty for delete button cell
          row.push("");
          ws_data.push(row);
        });
        const ws = XLSX.utils.aoa_to_sheet(ws_data);
        const wb = XLSX.utils.book_new();
        XLSX.utils.book_append_sheet(wb, ws, "Feedback");
        XLSX.writeFile(wb, "feedback_data.xlsx");
      }
    </script>
    <script defer="" src="https://static.cloudflareinsights.com/beacon.min.js/v8c78df7c7c0f484497ecbca7046644da1771523124516" integrity="sha512-8DS7rgIrAmghBFwoOTujcf6D9rXvH8xm8JQ1Ja01h9QX8EzXldiszufYa4IFfKdLUKTTrnSFXLDkUEOTrZQ8Qg==" data-cf-beacon="{" version":"2024.11.0","token":"e3c1c9af36de41759418005494a48906","r":1,"server_timing":{"name":{"cfcachestatus":true,"cfedge":true,"cfextpri":true,"cfl4":true,"cforigin":true,"cfspeedbrain":true},"location_startswith":null}}"="" crossorigin="anonymous"></script>
  </div></template>
  
  
  
<template id="tpl-tracking">
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width,initial-scale=1">
    <title>
        ប្រព័ន្ធតាមដាន PLP ២០២៦</title><link href="https://fonts.googleapis.com/css2?family=Kantumruy+Pro:wght@300;400;500;600;700&amp;family=Noto+Sans+Khmer:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet">
      <script type="module">
        import { initializeApp } from 'https://www.gstatic.com/firebasejs/10.12.0/firebase-app.js';
        		import { getDatabase, ref, set, get } from 'https://www.gstatic.com/firebasejs/10.12.0/firebase-database.js';
        		const cfg = {
        			apiKey: 'AIzaSyD2e2b8kZkKmWvId_U3ZY1b5c09K2HGxzs',
        			authDomain: 'sanghariomequipmet.firebaseapp.com',
        			databaseURL: 'https://sanghariomequipmet-default-rtdb.asia-southeast1.firebasedatabase.app',
        			projectId: 'sanghariomequipmet',
        			storageBucket: 'sanghariomequipmet.firebasestorage.app',
        			messagingSenderId: '559169888408',
        			appId: '1:559169888408:web:fa4e8807982c52aa95b0ed',
        		};
        		const app = initializeApp(cfg);
        		const db = getDatabase(app);
        		window._db = db;
        		window._rdb = { ref, set, get };
        		window._fbReady = true;
        		window.dispatchEvent(new Event('fbReady'));
      </script>
      <style>
        :root{--navy:#0f2044;--blue:#1a3a6e;--mid:#2155a3;--acc:#3b82f6;--sky:#60a5fa;--light:#eff6ff;--gold:#f59e0b;--green:#10b981;--red:#ef4444;--orange:#f97316;--text:#1e293b;--muted:#64748b;--bdr:#e2e8f0;--bg:#f8fafc;--fem:#ec4899;--mal:#3b82f6}*{margin:0;padding:0;box-sizing:border-box}body{font-family:'Kantumruy Pro','Noto Sans Khmer',sans-serif;background:var(--bg);color:var(--text);min-height:100vh}#loginPage{min-height:100vh;background:linear-gradient(135deg,var(--navy),var(--blue) 45%,var(--mid));display:flex;align-items:center;justify-content:center;padding:20px;position:relative;overflow:hidden}#loginPage::before{content:'';position:absolute;width:560px;height:560px;border-radius:50%;background:rgba(59,130,246,.07);top:-180px;right:-80px}#loginPage::after{content:'';position:absolute;width:380px;height:380px;border-radius:50%;background:rgba(96,165,250,.05);bottom:-130px;left:-80px}.lcard{background:#fff;border-radius:24px;padding:44px 38px;width:100%;max-width:500px;box-shadow:0 25px 60px rgba(0,0,0,.3);position:relative;z-index:1;animation:su .45s ease}@keyframes su{from{opacity:0;transform:translateY(28px)}to{opacity:1;transform:translateY(0)}}.llogo{text-align:center;margin-bottom:28px}.llogo .iw{width:70px;height:70px;background:linear-gradient(135deg,var(--mid),var(--sky));border-radius:18px;display:inline-flex;align-items:center;justify-content:center;margin-bottom:14px;box-shadow:0 8px 20px rgba(33,85,163,.4)}.llogo .iw svg{width:34px;height:34px;fill:#fff}.llogo h1{font-size:1.35rem;font-weight:700;color:var(--navy);line-height:1.35}.llogo p{color:var(--muted);font-size:.85rem;margin-top:4px}.flbl{display:block;font-weight:600;color:var(--navy);margin-bottom:10px;font-size:.9rem}.cgrid{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;margin-bottom:14px}.cbtn{padding:10px 6px;border:2px solid var(--bdr);border-radius:10px;background:#fff;cursor:pointer;font-family:'Kantumruy Pro',sans-serif;font-size:.9rem;font-weight:600;color:var(--blue);transition:all .18s;text-align:center;line-height:1.5}.cbtn:hover{border-color:var(--acc);background:var(--light);transform:translateY(-2px)}.cbtn.sel{border-color:var(--mid);background:linear-gradient(135deg,var(--mid),var(--acc));color:#fff;box-shadow:0 4px 12px rgba(33,85,163,.4);transform:translateY(-2px)}.cbtn .ds{font-size:.58rem;color:var(--green);display:block;margin-top:1px}.cbtn.sel .ds{color:#bbf7d0}.cbtn.has-data{border-color:#86efac;background:#f0fdf4}.cbtn.has-data .ds{color:#059669;font-weight:700}.cbtn.has-data:hover:not(.sel){border-color:#22c55e;background:#dcfce7}.cbtn.no-data .ds{color:#cbd5e1}.cls-status{margin-bottom:14px;background:var(--light);border-radius:12px;padding:13px 16px;border:1px solid #bfdbfe}.cls-status-title{font-size:.8rem;font-weight:700;color:var(--navy);margin-bottom:9px;display:flex;align-items:center;gap:5px}.cls-status-row{display:flex;flex-wrap:wrap;gap:5px;margin-bottom:5px}.cls-ok{background:#dcfce7;border:1px solid #86efac;color:#166534;padding:3px 9px;border-radius:20px;font-size:.7rem;font-weight:700;white-space:nowrap;cursor:default}.cls-ok:hover{background:#bbf7d0}.cls-none{background:#f1f5f9;border:1px solid var(--bdr);color:var(--muted);padding:3px 9px;border-radius:20px;font-size:.7rem;white-space:nowrap}.cls-sum{display:flex;gap:14px;font-size:.74rem;border-top:1px solid #bfdbfe;padding-top:8px;margin-top:8px;flex-wrap:wrap;color:var(--muted)}.cls-sum .ok-c{color:var(--green);font-weight:800}.cls-sum .no-c{color:#f97316;font-weight:800}.cls-progress-bar{height:6px;background:#e2e8f0;border-radius:99px;overflow:hidden;margin-bottom:10px}.cls-progress-fill{height:100%;background:linear-gradient(90deg,var(--green),#34d399);border-radius:99px;transition:width .5s ease}.fbst{display:flex;align-items:center;gap:8px;padding:9px 13px;border-radius:9px;font-size:.78rem;font-weight:500;margin-bottom:14px;background:#f1f5f9;color:var(--muted);border:1px solid var(--bdr)}.fbst .d{width:8px;height:8px;border-radius:50%;background:#cbd5e1;flex-shrink:0;transition:all .3s}.fbst.ok{background:#f0fdf4;color:#166534;border-color:#bbf7d0}.fbst.ok .d{background:var(--green);box-shadow:0 0 0 3px rgba(16,185,129,.25)}.fbst.err{background:#fef2f2;color:#991b1b;border-color:#fecaca}.fbst.err .d{background:var(--red)}.lbtn{width:100%;padding:13px;background:linear-gradient(135deg,var(--navy),var(--mid));color:#fff;border:none;border-radius:12px;font-family:'Kantumruy Pro',sans-serif;font-size:1rem;font-weight:700;cursor:pointer;transition:all .3s;box-shadow:0 4px 15px rgba(15,32,68,.3)}.lbtn:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(15,32,68,.4)}.lbtn:disabled{opacity:.45;cursor:not-allowed;transform:none}#appPage{display:none}.topbar{background:linear-gradient(90deg,var(--navy),var(--blue));padding:0 20px;height:60px;display:flex;align-items:center;justify-content:space-between;box-shadow:0 2px 12px rgba(0,0,0,.2);position:sticky;top:0;z-index:100}.tbl{display:flex;align-items:center;gap:10px}.tlogo{width:32px;height:32px;background:rgba(255,255,255,.14);border-radius:9px;display:flex;align-items:center;justify-content:center}.tlogo svg{width:17px;height:17px;fill:#fff}.ttit{color:#fff;font-weight:700;font-size:.9rem}.tsub{color:rgba(255,255,255,.5);font-size:.68rem}.tbr{display:flex;align-items:center;gap:8px}.cbadge{background:rgba(255,255,255,.14);color:#fff;padding:4px 12px;border-radius:20px;font-weight:700;font-size:.85rem;border:1px solid rgba(255,255,255,.18)}.mbadge{background:rgba(251,191,36,.2);color:#fcd34d;padding:4px 10px;border-radius:20px;font-size:.72rem;border:1px solid rgba(251,191,36,.3);font-weight:600}.sbadge{background:rgba(16,185,129,.2);color:#6ee7b7;padding:3px 9px;border-radius:20px;font-size:.7rem;border:1px solid rgba(16,185,129,.3)}.sbadge.syn{animation:pulse 1s infinite}@keyframes pulse{0%,100%{opacity:1}50%{opacity:.45}}.lgbtn{background:rgba(255,255,255,.1);border:1px solid rgba(255,255,255,.22);color:#fff;padding:5px 12px;border-radius:7px;cursor:pointer;font-family:'Kantumruy Pro',sans-serif;font-size:.78rem;transition:all .2s}.lgbtn:hover{background:rgba(255,255,255,.2)}.ntabs{background:#fff;border-bottom:2px solid var(--bdr);display:flex;overflow-x:auto;padding:0 18px;gap:0}.ntab{padding:12px 14px;border:none;background:0 0;color:var(--muted);font-family:'Kantumruy Pro',sans-serif;font-size:.82rem;font-weight:600;cursor:pointer;border-bottom:3px solid transparent;margin-bottom:-2px;white-space:nowrap;transition:all .2s}.ntab:hover{color:var(--mid)}.ntab.act{color:var(--mid);border-bottom-color:var(--mid)}.mc{padding:20px 16px;max-width:1200px;margin:0 auto}.month-bar{background:#fff;border-radius:14px;padding:16px 18px;margin-bottom:16px;box-shadow:0 1px 3px rgba(0,0,0,.05),0 4px 10px rgba(0,0,0,.04);display:flex;align-items:center;gap:12px;flex-wrap:wrap}.month-bar label{font-weight:700;color:var(--navy);font-size:.88rem;white-space:nowrap}.month-scroll{display:flex;gap:6px;overflow-x:auto;flex:1;padding-bottom:2px}.mbtn{padding:7px 14px;border:2px solid var(--bdr);border-radius:20px;background:#fff;cursor:pointer;font-family:'Kantumruy Pro',sans-serif;font-size:.8rem;font-weight:600;color:var(--muted);transition:all .18s;white-space:nowrap;flex-shrink:0}.mbtn:hover{border-color:var(--acc);color:var(--mid)}.mbtn.mact{border-color:var(--mid);background:var(--mid);color:#fff;box-shadow:0 2px 8px rgba(33,85,163,.35)}.mbtn .ms{font-size:.58rem;display:block;margin-top:1px}.mbtn.mact .ms{color:#c7d7f8}.card{background:#fff;border-radius:14px;box-shadow:0 1px 3px rgba(0,0,0,.05),0 4px 10px rgba(0,0,0,.04);padding:20px;margin-bottom:16px}.shdr{display:flex;align-items:center;gap:9px;margin-bottom:16px;flex-wrap:wrap}.sico{width:36px;height:36px;border-radius:9px;display:flex;align-items:center;justify-content:center;flex-shrink:0}.sico svg{width:18px;height:18px;fill:#fff}.sico.bl{background:linear-gradient(135deg,var(--mid),var(--acc))}.sico.go{background:linear-gradient(135deg,#d97706,var(--gold))}.sico.gr{background:linear-gradient(135deg,#059669,var(--green))}.sico.pk{background:linear-gradient(135deg,#db2777,var(--fem))}.sico.or{background:linear-gradient(135deg,#ea580c,var(--orange))}.stit{font-size:.95rem;font-weight:700;color:var(--navy)}.ssub{font-size:.74rem;color:var(--muted)}.plp-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-bottom:14px}.plp-box{background:var(--light);border-radius:10px;padding:13px;border:1px solid #bfdbfe}.plp-box.pk-box{background:#fff5f9;border-color:#fbcfe8}.plp-title{font-size:.75rem;font-weight:700;color:var(--navy);margin-bottom:8px;display:flex;align-items:center;gap:5px}.plp-row{display:flex;align-items:center;justify-content:space-between;margin-bottom:6px}.plp-row:last-child{margin-bottom:0}.plp-lbl{font-size:.76rem;color:var(--muted);font-weight:500}.plp-inputs{display:flex;gap:5px;align-items:center}.ni{width:60px;padding:5px 6px;border:2px solid var(--bdr);border-radius:7px;font-family:'Kantumruy Pro',sans-serif;font-size:.85rem;text-align:center;transition:all .2s}.ni:focus{outline:0;border-color:var(--acc);box-shadow:0 0 0 3px rgba(59,130,246,.12)}.ni.nf{border-color:#fce7f3;background:#fff5f9}.ni.nf:focus{border-color:var(--fem);box-shadow:0 0 0 3px rgba(236,72,153,.1)}.ni.nm{border-color:#dbeafe;background:#f5f8ff}.ni.nm:focus{border-color:var(--mal);box-shadow:0 0 0 3px rgba(59,130,246,.1)}.plp-pct{font-size:.78rem;font-weight:700;color:var(--mid);min-width:38px;text-align:right}.plp-stats{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;margin-top:10px}.plp-stat{text-align:center;background:#fff;border-radius:8px;padding:9px 4px;box-shadow:0 1px 4px rgba(0,0,0,.05)}.plp-stat .pv{font-size:1.1rem;font-weight:800;color:var(--navy)}.plp-stat .pl{font-size:.65rem;color:var(--muted);margin-top:1px}.plp-stat.fst .pv{color:var(--fem)}.plp-stat.mst .pv{color:var(--mal)}.gt{width:100%;border-collapse:separate;border-spacing:0;font-size:.83rem}.gt th{background:var(--navy);color:#fff;padding:8px 7px;text-align:center;font-weight:600;font-size:.74rem}.gt th:first-child{border-radius:8px 0 0 0;text-align:left;padding-left:12px}.gt th:last-child{border-radius:0 8px 0 0}.gt td{padding:7px 6px;border-bottom:1px solid var(--bdr);text-align:center}.gt td:first-child{text-align:left;padding-left:12px}.gt tr:last-child td{border-bottom:none}.gt tr:hover td{background:#fafbff}.totrow td{background:var(--light)!important;font-weight:700;color:var(--navy);border-top:2px solid var(--bdr)}.gb{display:inline-flex;width:24px;height:24px;border-radius:6px;align-items:center;justify-content:center;font-weight:800;font-size:.85rem}.gA{background:#dcfce7;color:#166534}.gB{background:#dbeafe;color:#1e40af}.gC{background:#fef9c3;color:#854d0e}.gD{background:#ffedd5;color:#9a3412}.gE{background:#fce7f3;color:#9d174d}.gF{background:#fee2e2;color:#991b1b}.gtag{display:inline-flex;align-items:center;gap:2px;font-size:.68rem;font-weight:600;padding:2px 6px;border-radius:20px}.tgf{background:#fce7f3;color:#9d174d}.tgm{background:#dbeafe;color:#1e40af}.bm{height:6px;background:var(--bdr);border-radius:99px;overflow:hidden;width:48px;display:inline-block;vertical-align:middle;margin-left:3px}.bmf{height:100%;border-radius:99px;transition:width .5s ease}.fA{background:#22c55e}.fB{background:#3b82f6}.fC{background:#eab308}.fD{background:#f97316}.fE{background:#ec4899}.fF{background:#ef4444}.sumbox{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;background:var(--light);border-radius:10px;padding:12px;margin-bottom:13px}.smi{text-align:center}.smv{font-size:1.15rem;font-weight:800;color:var(--navy)}.sml{font-size:.67rem;color:var(--muted);margin-top:2px}.fv{color:var(--fem)!important}.mv{color:var(--mal)!important}.cbtn2{background:linear-gradient(135deg,var(--navy),var(--mid));color:#fff;border:none;padding:11px 24px;border-radius:10px;font-family:'Kantumruy Pro',sans-serif;font-size:.9rem;font-weight:700;cursor:pointer;transition:all .3s;box-shadow:0 4px 12px rgba(15,32,68,.28)}.cbtn2:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(15,32,68,.3)}.cbtn2.gbtn{background:linear-gradient(135deg,#059669,#10b981)}.alrt{padding:10px 14px;border-radius:9px;font-size:.8rem;font-weight:500;margin-bottom:14px;display:flex;align-items:flex-start;gap:7px}.aw{background:#fef9c3;color:#854d0e;border:1px solid #fde68a}.aok{background:#dcfce7;color:#166534;border:1px solid #bbf7d0}.rgrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(290px,1fr));gap:13px;margin-bottom:16px}.rc{background:#fff;border-radius:14px;overflow:hidden;box-shadow:0 1px 3px rgba(0,0,0,.05),0 4px 10px rgba(0,0,0,.04);transition:all .22s}.rc:hover{transform:translateY(-3px);box-shadow:0 8px 22px rgba(0,0,0,.09)}.rch{padding:11px 16px;background:linear-gradient(135deg,var(--navy),var(--blue));color:#fff;display:flex;align-items:center;justify-content:space-between}.rcn{font-size:.95rem;font-weight:800}.rct{font-size:.65rem;opacity:.6}.rcb{padding:13px 15px}.plp-mini{display:flex;gap:8px;margin-bottom:10px;flex-wrap:wrap}.plp-chip{background:var(--light);border-radius:7px;padding:5px 9px;font-size:.72rem;font-weight:600;color:var(--navy);border:1px solid #bfdbfe;flex:1;min-width:80px;text-align:center}.plp-chip .pv{font-size:1rem;font-weight:800;color:var(--mid)}.plp-chip .pf{color:var(--fem);font-size:.65rem}.plp-chip .pm{color:var(--mal);font-size:.65rem}.stjt{font-size:.7rem;font-weight:700;color:var(--muted);text-transform:uppercase;letter-spacing:.4px;margin-bottom:7px}.br{display:flex;align-items:center;gap:5px;margin-bottom:2px}.bgl{width:18px;font-weight:800;font-size:.78rem;text-align:center;flex-shrink:0}.btr{flex:1;height:10px;background:var(--bdr);border-radius:99px;overflow:hidden}.bfi{height:100%;border-radius:99px;transition:width .55s ease}.bv{width:34px;font-size:.74rem;font-weight:700;text-align:right;flex-shrink:0}.gir{display:flex;gap:3px;font-size:.65rem;padding-left:23px;margin-bottom:2px;color:var(--muted)}.gif{color:var(--fem);font-weight:600}.gim{color:var(--mal);font-weight:600}.rdiv{height:1px;background:var(--bdr);margin:8px 0}.nd{background:var(--light);border:2px dashed var(--bdr);text-align:center;padding:16px;color:var(--muted);font-size:.78rem;border-radius:10px}.comp-controls{background:#fff;border-radius:14px;padding:16px 18px;margin-bottom:16px;box-shadow:0 1px 3px rgba(0,0,0,.05),0 4px 10px rgba(0,0,0,.04);display:flex;align-items:center;gap:12px;flex-wrap:wrap}.comp-controls label{font-weight:700;color:var(--navy);font-size:.88rem}.csel{padding:7px 12px;border:2px solid var(--bdr);border-radius:8px;font-family:'Kantumruy Pro',sans-serif;font-size:.85rem;color:var(--text);background:#fff;cursor:pointer;transition:all .2s}.csel:focus{outline:0;border-color:var(--acc)}.comp-table-wrap{overflow-x:auto;border-radius:12px;box-shadow:0 1px 3px rgba(0,0,0,.05)}.ctbl{width:100%;border-collapse:separate;border-spacing:0;font-size:.78rem;min-width:700px}.ctbl th{background:var(--navy);color:#fff;padding:9px 10px;text-align:center;font-weight:600;font-size:.72rem;white-space:nowrap}.ctbl th:first-child{border-radius:10px 0 0 0;text-align:left;padding-left:14px;min-width:80px}.ctbl th:last-child{border-radius:0 10px 0 0}.ctbl th.sec{background:#1a3a6e}.ctbl td{padding:8px 9px;border-bottom:1px solid var(--bdr);text-align:center;background:#fff}.ctbl td:first-child{text-align:left;padding-left:14px;font-weight:700;background:#fafbff}.ctbl tr:last-child td{border-bottom:none}.ctbl tr:hover td{background:#f0f6ff}.ctbl tr:hover td:first-child{background:#e8f0fe}.up{color:#166534;font-weight:700}.dn{color:#991b1b;font-weight:700}.eq{color:var(--muted)}.trend-icon{font-size:.65rem;margin-left:2px}.cell-hi{background:#dcfce7!important}.cell-lo{background:#fee2e2!important}.cell-warn{background:#fef9c3!important}.pct-bar{display:flex;align-items:center;gap:4px;justify-content:center}.pct-bar-track{width:40px;height:6px;background:var(--bdr);border-radius:99px;overflow:hidden}.pct-bar-fill{height:100%;border-radius:99px}.plp-fill{background:var(--mid)}.test-fill{background:var(--green)}.comhdr{background:linear-gradient(135deg,var(--navy),var(--mid));border-radius:16px;padding:22px;color:#fff;margin-bottom:16px;box-shadow:0 8px 28px rgba(15,32,68,.25)}.comtit{font-size:1rem;font-weight:800;margin-bottom:14px;display:flex;align-items:center;gap:7px}.comgrid{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}.comi{background:rgba(255,255,255,.1);border-radius:10px;padding:12px;text-align:center;border:1px solid rgba(255,255,255,.12)}.comi .gl{font-size:1.1rem;font-weight:900;margin-bottom:1px}.comi .gp{font-size:1.35rem;font-weight:800}.comi .gd{font-size:.65rem;opacity:.6;margin-top:2px}.comi .gg{font-size:.68rem;margin-top:4px;display:flex;justify-content:center;gap:6px}.comi .ggf{color:#f9a8d4;font-weight:700}.comi .ggm{color:#93c5fd;font-weight:700}.sstrip{display:flex;gap:10px;margin-bottom:16px;flex-wrap:wrap}.schi{background:#fff;border-radius:10px;padding:12px 14px;text-align:center;box-shadow:0 2px 8px rgba(0,0,0,.05);flex:1;min-width:80px}.schi .sv{font-size:1.35rem;font-weight:800;color:var(--navy)}.schi .sl{font-size:.7rem;color:var(--muted);margin-top:2px}.schi.fc .sv{color:var(--fem)}.schi.mc .sv{color:var(--mal)}.schi.gc .sv{color:var(--green)}.schi.oc .sv{color:var(--orange)}.dtbl{width:100%;border-collapse:separate;border-spacing:0;font-size:.74rem}.dtbl th{background:var(--navy);color:#fff;padding:7px 7px;text-align:center;font-weight:600;font-size:.7rem}.dtbl th:first-child{border-radius:8px 0 0 0;text-align:left;padding-left:10px}.dtbl th:last-child{border-radius:0 8px 0 0}.dtbl td{padding:6px 7px;border-bottom:1px solid var(--bdr);text-align:center}.dtbl td:first-child{text-align:left;font-weight:700;padding-left:10px}.dtbl tr:hover td{background:var(--light)}.dttot{background:var(--light)!important;font-weight:700;color:var(--navy)}.tcol{display:grid;grid-template-columns:1fr 1fr;gap:14px}.empty{text-align:center;padding:50px 20px;color:var(--muted)}.empty svg{width:56px;height:56px;fill:var(--bdr);margin-bottom:12px}.empty h3{font-size:.9rem;font-weight:700;color:var(--text);margin-bottom:4px}.export-buttons{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:16px}.tc{display:none}.tc.act{display:block}.hid{display:none!important}@media (max-width:600px){.lcard{padding:24px 14px}.cgrid{grid-template-columns:repeat(3,1fr)}.mc{padding:10px 8px}.topbar{padding:0 10px}.comgrid{grid-template-columns:repeat(2,1fr)}.tcol{grid-template-columns:1fr}.sumbox{grid-template-columns:repeat(2,1fr)}.plp-grid{grid-template-columns:1fr}.ni{width:50px;font-size:.8rem}.plp-stats{grid-template-columns:repeat(2,1fr)}.export-buttons{gap:6px}.export-buttons button{font-size:.8rem;padding:7px 12px}}
      </style>
        <div id="loginPage">
        <div class="lcard">
          <div class="llogo">
            <div class="iw">
              <svg viewBox="0 0 24 24">
                <path d="M5 13.18v4L12 21l7-3.82v-4L12 17l-7-3.82zM12 3L1 9l11 6 9-4.91V17h2V9L12 3z"></path>
              </svg>
            </div>
            <h1>🇰🇭 ការតាមដាន PLP<br>ឆ្នាំសិក្សា២០២៥-២០២៦</h1>
            <p>ប្រព័ន្ធតាមដានការពង្រឹងអំណាន និងគណនា</p>
          </div>
          <div class="fbst ok" id="fbst">
            <div class="d"></div>
            <span id="fbstxt">🔥 Realtime Database ភ្ជាប់រួចរាល់</span>
          </div>
          <label class="flbl">ជ្រើសរើសថ្នាក់</label>
          <div class="cgrid" id="classGrid"><button class="cbtn no-data" data-cls="1A">1A<span class="ds">⏳</span></button><button class="cbtn no-data" data-cls="1B">1B<span class="ds">⏳</span></button><button class="cbtn no-data" data-cls="2A">2A<span class="ds">⏳</span></button><button class="cbtn no-data" data-cls="2B">2B<span class="ds">⏳</span></button><button class="cbtn no-data" data-cls="3A">3A<span class="ds">⏳</span></button><button class="cbtn no-data" data-cls="3B">3B<span class="ds">⏳</span></button><button class="cbtn no-data" data-cls="4A">4A<span class="ds">⏳</span></button><button class="cbtn no-data" data-cls="4B">4B<span class="ds">⏳</span></button><button class="cbtn no-data" data-cls="5A">5A<span class="ds">⏳</span></button><button class="cbtn no-data" data-cls="5B">5B<span class="ds">⏳</span></button><button class="cbtn no-data" data-cls="6A">6A<span class="ds">⏳</span></button><button class="cbtn no-data" data-cls="6B">6B<span class="ds">⏳</span></button></div>
          <div id="clsStatusPanel" style="display:none"></div>
          <button class="lbtn" id="loginBtn" disabled="" onclick="doLogin()">
            ចូលប្រើប្រាស់
          </button>
        </div>
      </div>
      <div id="appPage">
        <div class="topbar">
          <div class="tbl">
            <div class="tlogo">
              <svg viewBox="0 0 24 24">
                <path d="M5 13.18v4L12 21l7-3.82v-4L12 17l-7-3.82zM12 3L1 9l11 6 9-4.91V17h2V9L12 3z"></path>
              </svg>
            </div>
            <div>
              <div class="ttit">តាមដាន PLP ២០២៦</div>
              <div class="tsub">Firebase Realtime</div>
            </div>
          </div>
          <div class="tbr">
            <span class="sbadge" id="syncBadge">🔥 Firebase</span><span class="mbadge" id="monBadge">ខែ --</span><span class="cbadge" id="clsBadge">ថ្នាក់ --</span><button class="lgbtn" onclick="doLogout()">⬅ ចេញ</button>
          </div>
        </div>
        <div class="ntabs">
          <button class="ntab act" onclick="sw(" input",this)"="">✏️ បញ្ចូល</button><button class="ntab" onclick="sw(" results",this)"="">
            📊 លទ្ធផលថ្នាក់</button><button class="ntab" onclick="sw(" compare",this)"="">
            📈 ប្រៀបធៀបខែ</button><button class="ntab" onclick="sw(" combined",this)"="">🏆 រួម</button>
        </div>
        <div id="tc-input" class="tc act">
          <div class="mc">
            <div class="month-bar">
              <label>📅 ខែ:</label>
              <div class="month-scroll" id="monthBar"></div>
            </div>
            <div class="card">
              <div class="shdr">
                <div class="sico bl">
                  <svg viewBox="0 0 24 24">
                    <path d="M21 5c-1.11-.35-2.33-.5-3.5-.5-1.95 0-4.05.4-5.5 1.5-1.45-1.1-3.55-1.5-5.5-1.5S2.45 4.9 1 6v14.65c0 .25.25.5.5.5.1 0 .15-.05.25-.05C3.1 20.45 5.05 20 6.5 20c1.95 0 4.05.4 5.5 1.5 1.35-.85 3.8-1.5 5.5-1.5 1.65 0 3.35.3 4.75 1.05.1.05.15.05.25.05.25 0 .5-.25.5-.5V6c-.6-.45-1.25-.75-2-1z"></path>
                  </svg>
                </div>
                <div>
                  <div class="stit">📖 ភាសាខ្មែរ</div>
                  <div class="ssub">PLP + ចំនួនសិស្ស ស្រី/ប្រុស</div>
                </div>
                <div style="margin-left:auto;text-align:right">
                  <div style="font-size:.72rem;color:var(--muted)">
                    សិស្សសរុប
                  </div>
                  <div style="font-size:1rem;font-weight:800;color:var(--navy)" id="kTotDisp">
                    0
                  </div>
                </div>
              </div>
              <div class="plp-grid">
                <div class="plp-box">
                  <div class="plp-title">🎓 សិស្សសរុបចុះឈ្មោះ</div>
                  <div class="plp-row">
                    <span class="plp-lbl">👩 ស្រី</span>
                    <div class="plp-inputs">
                      <input type="number" min="0" class="ni nf" id="k_enr_f" value="0" oninput="recalcPlp(" k")"=""><span id="k_enr_f_pct" class="plp-pct">--</span>
                    </div>
                  </div>
                  <div class="plp-row">
                    <span class="plp-lbl">👦 ប្រុស</span>
                    <div class="plp-inputs">
                      <input type="number" min="0" class="ni nm" id="k_enr_m" value="0" oninput="recalcPlp(" k")"=""><span id="k_enr_m_pct" class="plp-pct">--</span>
                    </div>
                  </div>
                </div>
                <div class="plp-box">
                  <div class="plp-title">📗 សិស្សរៀន PLP</div>
                  <div class="plp-row">
                    <span class="plp-lbl">👩 ស្រី</span>
                    <div class="plp-inputs">
                      <input type="number" min="0" class="ni nf" id="k_plp_f" value="0" oninput="recalcPlp(" k")"=""><span id="k_plp_f_pct" class="plp-pct" style="color:var(--fem)">--</span>
                    </div>
                  </div>
                  <div class="plp-row">
                    <span class="plp-lbl">👦 ប្រុស</span>
                    <div class="plp-inputs">
                      <input type="number" min="0" class="ni nm" id="k_plp_m" value="0" oninput="recalcPlp(" k")"=""><span id="k_plp_m_pct" class="plp-pct" style="color:var(--mal)">--</span>
                    </div>
                  </div>
                </div>
                <div class="plp-box pk-box">
                  <div class="plp-title">📝 សិស្សបានធ្វើតេស្ត PLP</div>
                  <div class="plp-row">
                    <span class="plp-lbl">👩 ស្រី</span>
                    <div class="plp-inputs">
                      <input type="number" min="0" class="ni nf" id="k_tst_f" value="0" oninput="recalcPlp(" k")"=""><span id="k_tst_f_pct" class="plp-pct" style="color:var(--fem)">--</span>
                    </div>
                  </div>
                  <div class="plp-row">
                    <span class="plp-lbl">👦 ប្រុស</span>
                    <div class="plp-inputs">
                      <input type="number" min="0" class="ni nm" id="k_tst_m" value="0" oninput="recalcPlp(" k")"=""><span id="k_tst_m_pct" class="plp-pct" style="color:var(--mal)">--</span>
                    </div>
                  </div>
                </div>
                <div class="plp-box" style="background:#f0fdf4;border-color:#bbf7d0">
                  <div class="plp-title">📊 សង្ខេប PLP</div>
                  <div id="k_plp_summary" style="font-size:.78rem;color:var(--navy);line-height:1.8">
                    --
                  </div>
                </div>
              </div>
              <div class="plp-stats">
                <div class="plp-stat">
                  <div class="pv" id="k_s_enr">0</div>
                  <div class="pl">📋 ចុះឈ្មោះ</div>
                </div>
                <div class="plp-stat fst">
                  <div class="pv" id="k_s_plp_pct">--%</div>
                  <div class="pl">📗 % រៀន PLP</div>
                </div>
                <div class="plp-stat mst">
                  <div class="pv" id="k_s_tst_pct">--%</div>
                  <div class="pl">📝 % ធ្វើតេស្ត</div>
                </div>
                <div class="plp-stat">
                  <div class="pv" id="k_s_pass_pct" style="color:var(--green)">
                    --%
                  </div>
                  <div class="pl">✅ % ក្រៅ F</div>
                </div>
              </div>
              <div style="margin-top:14px">
                <div class="shdr" style="margin-bottom:12px">
                  <div>
                    <div class="stit" style="font-size:.88rem">
                      លទ្ធផលនិទ្ទេស
                    </div>
                    <div class="ssub">ចំនួនសិស្ស ស្រី/ប្រុស</div>
                  </div>
                  <div style="margin-left:auto;font-size:.78rem;color:var(--muted)">
                    សិស្សសរុបក្នុងតារាង:<span style="font-weight:800;color:var(--navy)" id="kTotAll">0</span>
                  </div>
                </div>
                <div class="sumbox">
                  <div class="smi">
                    <div class="smv fv" id="k_tf">0</div>
                    <div class="sml">👩 ស្រី</div>
                  </div>
                  <div class="smi">
                    <div class="smv mv" id="k_tm">0</div>
                    <div class="sml">👦 ប្រុស</div>
                  </div>
                  <div class="smi">
                    <div class="smv" id="k_ta">0</div>
                    <div class="sml">🎓 សរុប</div>
                  </div>
                  <div class="smi">
                    <div class="smv" id="k_st" style="font-size:.85rem">--</div>
                    <div class="sml">ស្ថានភាព</div>
                  </div>
                </div>
                <div style="overflow-x:auto">
                  <table class="gt">
                    <thead>
                      <tr>
                        <th style="width:52px">និទ្ទេស</th>
                        <th><span class="gtag tgf">👩</span></th>
                        <th><span class="gtag tgm">👦</span></th>
                        <th>សរុប</th>
                        <th>%</th>
                        <th>% ស្រី</th>
                        <th>% ប្រុស</th>
                      </tr>
                    </thead>
                    <tbody id="kBody"></tbody>
                    <tfoot>
                      <tr class="totrow">
                        <td>សរុប</td>
                        <td id="k_sf" style="text-align:center">0</td>
                        <td id="k_sm" style="text-align:center">0</td>
                        <td id="k_sa" style="text-align:center;font-weight:800">
                          0
                        </td>
                        <td style="text-align:center">--</td>
                        <td id="k_sfp" style="text-align:center;color:var(--fem)">
                          --
                        </td>
                        <td id="k_smp" style="text-align:center;color:var(--mal)">
                          --
                        </td>
                      </tr>
                    </tfoot>
                  </table>
                </div>
              </div>
            </div>
            <div class="card">
              <div class="shdr">
                <div class="sico go">
                  <svg viewBox="0 0 24 24">
                    <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-5 14H7v-2h7v2zm3-4H7v-2h10v2zm0-4H7V7h10v2z"></path>
                  </svg>
                </div>
                <div>
                  <div class="stit">🔢 គណិតវិទ្យា</div>
                  <div class="ssub">PLP + ចំនួនសិស្ស ស្រី/ប្រុស</div>
                </div>
                <div style="margin-left:auto;text-align:right">
                  <div style="font-size:.72rem;color:var(--muted)">
                    សិស្សសរុប
                  </div>
                  <div style="font-size:1rem;font-weight:800;color:var(--navy)" id="mTotDisp">
                    0
                  </div>
                </div>
              </div>
              <div class="plp-grid">
                <div class="plp-box">
                  <div class="plp-title">🎓 សិស្សសរុបចុះឈ្មោះ</div>
                  <div class="plp-row">
                    <span class="plp-lbl">👩 ស្រី</span>
                    <div class="plp-inputs">
                      <input type="number" min="0" class="ni nf" id="m_enr_f" value="0" oninput="recalcPlp(" m")"=""><span id="m_enr_f_pct" class="plp-pct">--</span>
                    </div>
                  </div>
                  <div class="plp-row">
                    <span class="plp-lbl">👦 ប្រុស</span>
                    <div class="plp-inputs">
                      <input type="number" min="0" class="ni nm" id="m_enr_m" value="0" oninput="recalcPlp(" m")"=""><span id="m_enr_m_pct" class="plp-pct">--</span>
                    </div>
                  </div>
                </div>
                <div class="plp-box">
                  <div class="plp-title">📗 សិស្សរៀន PLP</div>
                  <div class="plp-row">
                    <span class="plp-lbl">👩 ស្រី</span>
                    <div class="plp-inputs">
                      <input type="number" min="0" class="ni nf" id="m_plp_f" value="0" oninput="recalcPlp(" m")"=""><span id="m_plp_f_pct" class="plp-pct" style="color:var(--fem)">--</span>
                    </div>
                  </div>
                  <div class="plp-row">
                    <span class="plp-lbl">👦 ប្រុស</span>
                    <div class="plp-inputs">
                      <input type="number" min="0" class="ni nm" id="m_plp_m" value="0" oninput="recalcPlp(" m")"=""><span id="m_plp_m_pct" class="plp-pct" style="color:var(--mal)">--</span>
                    </div>
                  </div>
                </div>
                <div class="plp-box pk-box">
                  <div class="plp-title">📝 សិស្សបានធ្វើតេស្ត PLP</div>
                  <div class="plp-row">
                    <span class="plp-lbl">👩 ស្រី</span>
                    <div class="plp-inputs">
                      <input type="number" min="0" class="ni nf" id="m_tst_f" value="0" oninput="recalcPlp(" m")"=""><span id="m_tst_f_pct" class="plp-pct" style="color:var(--fem)">--</span>
                    </div>
                  </div>
                  <div class="plp-row">
                    <span class="plp-lbl">👦 ប្រុស</span>
                    <div class="plp-inputs">
                      <input type="number" min="0" class="ni nm" id="m_tst_m" value="0" oninput="recalcPlp(" m")"=""><span id="m_tst_m_pct" class="plp-pct" style="color:var(--mal)">--</span>
                    </div>
                  </div>
                </div>
                <div class="plp-box" style="background:#f0fdf4;border-color:#bbf7d0">
                  <div class="plp-title">📊 សង្ខេប PLP</div>
                  <div id="m_plp_summary" style="font-size:.78rem;color:var(--navy);line-height:1.8">
                    --
                  </div>
                </div>
              </div>
              <div class="plp-stats">
                <div class="plp-stat">
                  <div class="pv" id="m_s_enr">0</div>
                  <div class="pl">📋 ចុះឈ្មោះ</div>
                </div>
                <div class="plp-stat fst">
                  <div class="pv" id="m_s_plp_pct">--%</div>
                  <div class="pl">📗 % រៀន PLP</div>
                </div>
                <div class="plp-stat mst">
                  <div class="pv" id="m_s_tst_pct">--%</div>
                  <div class="pl">📝 % ធ្វើតេស្ត</div>
                </div>
                <div class="plp-stat">
                  <div class="pv" id="m_s_pass_pct" style="color:var(--green)">
                    --%
                  </div>
                  <div class="pl">✅ % ក្រៅ F</div>
                </div>
              </div>
              <div style="margin-top:14px">
                <div class="shdr" style="margin-bottom:12px">
                  <div>
                    <div class="stit" style="font-size:.88rem">
                      លទ្ធផលនិទ្ទេស
                    </div>
                  </div>
                  <div style="margin-left:auto;font-size:.78rem;color:var(--muted)">
                    សរុប:<span style="font-weight:800;color:var(--navy)" id="mTotAll">0</span>
                  </div>
                </div>
                <div class="sumbox">
                  <div class="smi">
                    <div class="smv fv" id="m_tf">0</div>
                    <div class="sml">👩 ស្រី</div>
                  </div>
                  <div class="smi">
                    <div class="smv mv" id="m_tm">0</div>
                    <div class="sml">👦 ប្រុស</div>
                  </div>
                  <div class="smi">
                    <div class="smv" id="m_ta">0</div>
                    <div class="sml">🎓 សរុប</div>
                  </div>
                  <div class="smi">
                    <div class="smv" id="m_st" style="font-size:.85rem">--</div>
                    <div class="sml">ស្ថានភាព</div>
                  </div>
                </div>
                <div style="overflow-x:auto">
                  <table class="gt">
                    <thead>
                      <tr>
                        <th style="width:52px">និទ្ទេស</th>
                        <th><span class="gtag tgf">👩</span></th>
                        <th><span class="gtag tgm">👦</span></th>
                        <th>សរុប</th>
                        <th>%</th>
                        <th>% ស្រី</th>
                        <th>% ប្រុស</th>
                      </tr>
                    </thead>
                    <tbody id="mBody"></tbody>
                    <tfoot>
                      <tr class="totrow">
                        <td>សរុប</td>
                        <td id="m_sf" style="text-align:center">0</td>
                        <td id="m_sm" style="text-align:center">0</td>
                        <td id="m_sa" style="text-align:center;font-weight:800">
                          0
                        </td>
                        <td style="text-align:center">--</td>
                        <td id="m_sfp" style="text-align:center;color:var(--fem)">
                          --
                        </td>
                        <td id="m_smp" style="text-align:center;color:var(--mal)">
                          --
                        </td>
                      </tr>
                    </tfoot>
                  </table>
                </div>
              </div>
            </div>
            <div style="display:flex;gap:10px;flex-wrap:wrap;align-items:center;margin-bottom:16px">
              <button class="cbtn2" id="saveBtn" onclick="saveData()">
                🔥 រក្សាទុកទៅ Firebase</button><button class="cbtn2 gbtn" onclick="sw(" results",document.queryselector(".ntab:nth-child(2)"))"="">
                📊 មើលលទ្ធផល →</button><span id="saveSt" style="font-size:.78rem;color:var(--muted)"></span>
            </div>
            <div class="export-buttons">
              <button class="cbtn2" style="background:linear-gradient(135deg,#059669,#10b981);font-size:.85rem;padding:8px 14px" onclick="exportInputTab(" xlsx")"="">
                📥 XLSX</button><button class="cbtn2" style="background:linear-gradient(135deg,#0891b2,#06b6d4);font-size:.85rem;padding:8px 14px" onclick="exportInputTab(" html")"="">
                📄 HTML</button><button class="cbtn2" style="background:linear-gradient(135deg,#7c3aed,#a855f7);font-size:.85rem;padding:8px 14px" onclick="exportInputTab(" json")"="">
                📋 JSON
              </button>
            </div>
          </div>
        </div>
        <div id="tc-results" class="tc">
          <div class="mc">
            <div class="export-buttons">
              <button class="cbtn2" style="background:linear-gradient(135deg,#059669,#10b981);font-size:.85rem;padding:8px 14px" onclick="exportTab(" results","xlsx")"="">
                📥 XLSX</button><button class="cbtn2" style="background:linear-gradient(135deg,#0891b2,#06b6d4);font-size:.85rem;padding:8px 14px" onclick="exportTab(" results","html")"="">
                📄 HTML</button><button class="cbtn2" style="background:linear-gradient(135deg,#7c3aed,#a855f7);font-size:.85rem;padding:8px 14px" onclick="exportTab(" results","json")"="">
                📋 JSON
              </button>
            </div>
            <div class="sstrip">
              <div class="schi">
                <div class="sv" id="stDone">0</div>
                <div class="sl">ថ្នាក់បានបញ្ចូល</div>
              </div>
              <div class="schi">
                <div class="sv">12</div>
                <div class="sl">ថ្នាក់សរុប</div>
              </div>
              <div class="schi fc">
                <div class="sv" id="stTF">0</div>
                <div class="sl">👩 ស្រី</div>
              </div>
              <div class="schi mc">
                <div class="sv" id="stTM">0</div>
                <div class="sl">👦 ប្រុស</div>
              </div>
              <div class="schi gc">
                <div class="sv" id="stPlp">--%</div>
                <div class="sl">📗 % PLP</div>
              </div>
              <div class="schi oc">
                <div class="sv" id="stTst">--%</div>
                <div class="sl">📝 % តេស្ត</div>
              </div>
            </div>
            <div id="rcont"></div>
          </div>
        </div>
        <div id="tc-compare" class="tc">
          <div class="mc">
            <div class="export-buttons">
              <button class="cbtn2" style="background:linear-gradient(135deg,#059669,#10b981);font-size:.85rem;padding:8px 14px" onclick="exportTab(" compare","xlsx")"="">
                📥 XLSX</button><button class="cbtn2" style="background:linear-gradient(135deg,#0891b2,#06b6d4);font-size:.85rem;padding:8px 14px" onclick="exportTab(" compare","html")"="">
                📄 HTML</button><button class="cbtn2" style="background:linear-gradient(135deg,#7c3aed,#a855f7);font-size:.85rem;padding:8px 14px" onclick="exportTab(" compare","json")"="">
                📋 JSON
              </button>
            </div>
            <div class="comp-controls">
              <label>🏫 ថ្នាក់:</label><select class="csel" id="compClassSel" onchange="renderCompare()">
                <option value="ALL">📊 គ្រប់ថ្នាក់ (មធ្យម)</option></select><label>📚 មុខវិជ្ជា:</label><select class="csel" id="compSubjSel" onchange="renderCompare()">
                <option value="both">ភាសាខ្មែរ + គណិត</option>
                <option value="khmer">📖 ភាសាខ្មែរ</option>
                <option value="math">🔢 គណិតវិទ្យា</option></select><label>👤 ភេទ:</label><select class="csel" id="compGenderSel" onchange="renderCompare()">
                <option value="all">ទាំងអស់</option>
                <option value="f">👩 ស្រី</option>
                <option value="m">👦 ប្រុស</option>
              </select>
            </div>
            <div id="compareContainer"></div>
          </div>
        </div>
        <div id="tc-combined" class="tc">
          <div class="mc">
            <div class="export-buttons">
              <button class="cbtn2" style="background:linear-gradient(135deg,#059669,#10b981);font-size:.85rem;padding:8px 14px" onclick="exportTab(" combined","xlsx")"="">
                📥 XLSX</button><button class="cbtn2" style="background:linear-gradient(135deg,#0891b2,#06b6d4);font-size:.85rem;padding:8px 14px" onclick="exportTab(" combined","html")"="">
                📄 HTML</button><button class="cbtn2" style="background:linear-gradient(135deg,#7c3aed,#a855f7);font-size:.85rem;padding:8px 14px" onclick="exportTab(" combined","json")"="">
                📋 JSON
              </button>
            </div>
            <div class="comp-controls" style="margin-bottom:16px">
              <label>📅 ខែ:</label><select class="csel" id="combMonthSel" onchange="renderCombined()">
                <option value="ALL">📊 គ្រប់ខែ (មធ្យម)</option>
              </select>
            </div>
            <div id="ccont"></div>
          </div>
        </div>
      </div>
      <footer style="text-align:center;padding:12px 0;color:#64748b;font-size:.85rem;border-top:1px solid #e2e8f0;margin-top:30px">
        តំបន់១ ខេត្តបន្ទាយមានជ័យ ស្រុកភ្នំស្រុក. រៀបចំដោយ UN BUNTONG.
      </footer>
      <script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
      <script>
        const CLS = ['1A','1B','2A','2B','3A','3B','4A','4B','5A','5B','6A','6B'];
        	const GR  = ['A','B','C','D','E','F'];
        	const MONTHS = [
        		{k:'M01',l:'មករា'},{k:'M02',l:'កុម្ភៈ'},{k:'M03',l:'មីនា'},
        		{k:'M04',l:'មេសា'},{k:'M05',l:'ឧសភា'},{k:'M06',l:'មិថុនា'},
        		{k:'M07',l:'កក្កដា'},{k:'M08',l:'សីហា'},{k:'M09',l:'កញ្ញា'},
        		{k:'M10',l:'តុលា'},{k:'M11',l:'វិច្ឆិកា'},{k:'M12',l:'ធ្នូ'}
        	];
        	const GCOL = {
        		A:{t:'#166534',b:'fA'},B:{t:'#1e40af',b:'fB'},C:{t:'#854d0e',b:'fC'},
        		D:{t:'#9a3412',b:'fD'},E:{t:'#9d174d',b:'fE'},F:{t:'#991b1b',b:'fF'}
        	};

        	let curCls = null, curMon = 'M01';
        	let allData = {};

        	window.addEventListener('fbReady', () => {
        		setFbSt('ok','🔥 Realtime Database ភ្ជាប់រួចរាល់');
        		loadAll();
        	});
        	setTimeout(()=>{ if(!window._fbReady) setFbSt('err','❌ Firebase ភ្ជាប់មិនបាន'); }, 8000);

        	function setFbSt(c,m){ const e=document.getElementById('fbst'),t=document.getElementById('fbstxt'); e.className='fbst '+c; t.textContent=m; }

        	async function loadAll(){
        		try{
        			const {get,ref}=window._rdb;
        			const snap=await get(ref(window._db,'plp2026'));
        			if(snap.exists()){ const v=snap.val(); Object.keys(v).forEach(k=>{ allData[k]=v[k]; }); }
        			buildCGrid(); renderResults(); renderCompare(); renderCombined();
        		}catch(e){ setFbSt('err','❌ Load: '+e.message); }
        	}

        	async function fbSave(cls, mon, payload){
        		const {set,ref}=window._rdb;
        		await set(ref(window._db,`plp2026/${cls}/${mon}`), payload);
        	}

        	function buildCGrid(){
        		const g=document.getElementById('classGrid'); g.innerHTML='';
        		CLS.forEach(c=>{
        			const b=document.createElement('button'); b.className='cbtn'; b.dataset.cls=c;
        			const months=allData[c]?Object.keys(allData[c]).length:0;
        			const hasDat=months>0;
        			if(hasDat) b.classList.add('has-data'); else b.classList.add('no-data');
        			b.innerHTML=`${c}<span class="ds">${hasDat?'🔥 '+months+'ខែ':'⏳'}</span>`;
        			b.onclick=()=>selCls(c); g.appendChild(b);
        		});
        		buildStatusPanel();
        	}

        	function buildStatusPanel(){
        		const panel=document.getElementById('clsStatusPanel');
        		if(!panel) return;
        		const withData=CLS.filter(c=>allData[c]&&Object.keys(allData[c]).length>0);
        		const noData=CLS.filter(c=>!allData[c]||Object.keys(allData[c]).length===0);
        		if(withData.length===0){ panel.style.display='none'; return; }
        		panel.style.display='block'; panel.className='cls-status';
        		const fillPct=Math.round((withData.length/CLS.length)*100);
        		const wHtml=withData.map(c=>{
        			const mons=Object.keys(allData[c]).sort();
        			const latest=MONTHS.find(m=>m.k===mons[mons.length-1])?.l||'';
        			const monLabels=mons.map(mk=>MONTHS.find(m=>m.k===mk)?.l||mk).join(', ');
        			return `<span class="cls-ok" title="ខែ: ${monLabels}">✅ ${c} · ${mons.length}ខែ${latest?' ('+latest+')':''}</span>`;
        		}).join('');
        		const nHtml=noData.map(c=>`<span class="cls-none">⏳ ${c}</span>`).join('');
        		panel.innerHTML=`
        			<div class="cls-status-title">📊 ស្ថានភាពបញ្ចូលទិន្នន័យ — <strong>${withData.length}/${CLS.length}</strong> ថ្នាក់</div>
        			<div class="cls-progress-bar"><div class="cls-progress-fill" style="width:${fillPct}%"></div></div>
        			${withData.length?`<div style="font-size:.7rem;font-weight:700;color:var(--green);margin-bottom:5px;">✅ ថ្នាក់មានទិន្នន័យ (${withData.length})</div><div class="cls-status-row">${wHtml}</div>`:''}
        			${noData.length?`<div style="font-size:.7rem;font-weight:700;color:var(--orange);margin-bottom:5px;margin-top:${withData.length?'9px':'0'};">⏳ ថ្នាក់មិនទាន់មានទិន្នន័យ (${noData.length})</div><div class="cls-status-row">${nHtml}</div>`:''}
        			<div class="cls-sum">
        				<span>✅ <span class="ok-c">${withData.length}</span> ថ្នាក់មានទិន្នន័យ</span>
        				<span>⏳ <span class="no-c">${noData.length}</span> ថ្នាក់នៅខ្វះ</span>
        				<span style="color:var(--navy);font-weight:600">📚 ${fillPct}% បានបញ្ចូល</span>
        			</div>`;
        	}

        	function selCls(c){
        		document.querySelectorAll('.cbtn').forEach(b=>b.classList.remove('sel'));
        		document.querySelector(`.cbtn[data-cls="${c}"]`).classList.add('sel');
        		curCls=c; document.getElementById('loginBtn').disabled=false;
        	}
        	function doLogin(){
        		if(!curCls)return;
        		document.getElementById('loginPage').style.display='none';
        		document.getElementById('appPage').style.display='block';
        		document.getElementById('clsBadge').textContent='ថ្នាក់ '+curCls;
        		buildMonthBar(); buildCompClassSel(); buildCombMonthSel(); loadMonthData();
        	}
        	function doLogout(){
        		document.getElementById('appPage').style.display='none';
        		document.getElementById('loginPage').style.display='flex';
        		curCls=null; document.getElementById('loginBtn').disabled=true;
        		buildCGrid(); sw('input',document.querySelector('.ntab'));
        	}

        	function buildMonthBar(){
        		const bar=document.getElementById('monthBar'); bar.innerHTML='';
        		MONTHS.forEach(m=>{
        			const b=document.createElement('button'); b.className='mbtn'; b.dataset.mk=m.k;
        			const hasDat=!!(allData[curCls]&&allData[curCls][m.k]);
        			b.innerHTML=`${m.l}<span class="ms">${hasDat?'✅':''}</span>`;
        			b.onclick=()=>selectMonth(m.k); bar.appendChild(b);
        		});
        		selectMonth(curMon);
        	}
        	function selectMonth(mk){
        		curMon=mk;
        		document.querySelectorAll('.mbtn').forEach(b=>b.classList.remove('mact'));
        		const btn=document.querySelector(`.mbtn[data-mk="${mk}"]`);
        		if(btn) btn.classList.add('mact');
        		const ml=MONTHS.find(m=>m.k===mk)?.l||mk;
        		document.getElementById('monBadge').textContent='📅 '+ml;
        		loadMonthData();
        	}
        	function loadMonthData(){
        		const sv=(allData[curCls]&&allData[curCls][curMon])||{};
        		buildSubj('k','kBody',sv.khmer||{});
        		buildSubj('m','mBody',sv.math||{});
        		['k','m'].forEach(pfx=>{
        			const subj=pfx==='k'?'khmer':'math';
        			const enr=sv[`${subj}_enr`]||{f:0,m:0};
        			const plp=sv[`${subj}_plp`]||{f:0,m:0};
        			const tst=sv[`${subj}_tst`]||{f:0,m:0};
        			setV(`${pfx}_enr_f`,enr.f||0); setV(`${pfx}_enr_m`,enr.m||0);
        			setV(`${pfx}_plp_f`,plp.f||0); setV(`${pfx}_plp_m`,plp.m||0);
        			setV(`${pfx}_tst_f`,tst.f||0); setV(`${pfx}_tst_m`,tst.m||0);
        			recalcPlp(pfx);
        		});
        		document.getElementById('saveSt').textContent=sv.savedAt?'✅ '+sv.savedAt:'';
        	}
        	function setV(id,v){ const e=document.getElementById(id); if(e&&'value'in e)e.value=v; }

        	function buildSubj(pfx,tbid,dat){
        		const tb=document.getElementById(tbid); tb.innerHTML='';
        		GR.forEach(g=>{
        			const f=dat[g]?.f??0, m=dat[g]?.m??0;
        			const tr=document.createElement('tr');
        			tr.innerHTML=`
        				<td><span class="gb g${g}">${g}</span></td>
        				<td style="text-align:center"><input type="number" min="0" class="ni nf" id="${pfx}_${g}_f" value="${f}" oninput="recalcGrade('${pfx}')"></td>
        				<td style="text-align:center"><input type="number" min="0" class="ni nm" id="${pfx}_${g}_m" value="${m}" oninput="recalcGrade('${pfx}')"></td>
        				<td style="text-align:center;font-weight:700" id="${pfx}_${g}_tot">-</td>
        				<td style="text-align:center"><span style="font-weight:700;color:${GCOL[g].t}" id="${pfx}_${g}_pct">-</span><div class="bm"><div class="bmf ${GCOL[g].b}" id="${pfx}_${g}_bar" style="width:0%"></div></div></td>
        				<td style="text-align:center;color:var(--fem);font-size:.78rem" id="${pfx}_${g}_fp">-</td>
        				<td style="text-align:center;color:var(--mal);font-size:.78rem" id="${pfx}_${g}_mp">-</td>`;
        			tb.appendChild(tr);
        		});
        		recalcGrade(pfx);
        	}

        	function recalcGrade(pfx){
        		let totF=0,totM=0; const ct={};
        		GR.forEach(g=>{
        			const f=parseInt(document.getElementById(`${pfx}_${g}_f`)?.value)||0;
        			const m=parseInt(document.getElementById(`${pfx}_${g}_m`)?.value)||0;
        			ct[g]={f,m}; totF+=f; totM+=m;
        		});
        		const grand=totF+totM;
        		GR.forEach(g=>{
        			const {f,m}=ct[g],tot=f+m;
        			const pct=grand>0?((tot/grand)*100).toFixed(1):'-';
        			const fp=grand>0&&f>0?((f/grand)*100).toFixed(1):'-';
        			const mp=grand>0&&m>0?((m/grand)*100).toFixed(1):'-';
        			st(`${pfx}_${g}_tot`,tot);
        			st(`${pfx}_${g}_pct`,pct!=='-'?pct+'%':'-');
        			st(`${pfx}_${g}_fp`,fp!=='-'?fp+'%':'-');
        			st(`${pfx}_${g}_mp`,mp!=='-'?mp+'%':'-');
        			const bar=document.getElementById(`${pfx}_${g}_bar`); if(bar)bar.style.width=(grand>0?(tot/grand)*100:0)+'%';
        		});
        		const pre=pfx==='k'?'k':'m';
        		st(`${pre}_sf`,totF); st(`${pre}_sm`,totM); st(`${pre}_sa`,grand);
        		st(`${pre}_sfp`,grand>0?((totF/grand)*100).toFixed(1)+'%':'--');
        		st(`${pre}_smp`,grand>0?((totM/grand)*100).toFixed(1)+'%':'--');
        		st(`${pre}_tf`,totF); st(`${pre}_tm`,totM); st(`${pre}_ta`,grand);
        		st(`${pre}_st`,grand>0?grand+' នាក់':'--');
        		st(`${pre}TotAll`,grand); st(`${pre}TotDisp`,grand);
        		const passF=GR.filter(g=>g!=='F').reduce((a,g)=>a+(ct[g].f+ct[g].m),0);
        		st(`${pre}_s_pass_pct`,grand>0?((passF/grand)*100).toFixed(1)+'%':'--');
        	}

        	function recalcPlp(pfx){
        		const enrF=parseInt(document.getElementById(`${pfx}_enr_f`)?.value)||0;
        		const enrM=parseInt(document.getElementById(`${pfx}_enr_m`)?.value)||0;
        		const plpF=parseInt(document.getElementById(`${pfx}_plp_f`)?.value)||0;
        		const plpM=parseInt(document.getElementById(`${pfx}_plp_m`)?.value)||0;
        		const tstF=parseInt(document.getElementById(`${pfx}_tst_f`)?.value)||0;
        		const tstM=parseInt(document.getElementById(`${pfx}_tst_m`)?.value)||0;
        		const enr=enrF+enrM, plp=plpF+plpM, tst=tstF+tstM;
        		const pct=(n,d)=>d>0?((n/d)*100).toFixed(1)+'%':'--';
        		st(`${pfx}_enr_f_pct`, enrF>0?enrF+' នាក់':'');
        		st(`${pfx}_enr_m_pct`, enrM>0?enrM+' នាក់':'');
        		st(`${pfx}_plp_f_pct`, pct(plpF,enrF));
        		st(`${pfx}_plp_m_pct`, pct(plpM,enrM));
        		st(`${pfx}_tst_f_pct`, pct(tstF,enrF));
        		st(`${pfx}_tst_m_pct`, pct(tstM,enrM));
        		const pre=pfx==='k'?'k':'m';
        		st(`${pre}_s_enr`, enr);
        		st(`${pre}_s_plp_pct`, pct(plp,enr));
        		st(`${pre}_s_tst_pct`, pct(tst,enr));
        		const sumEl=document.getElementById(`${pfx}_plp_summary`);
        		if(sumEl) sumEl.innerHTML=`
        			📋 ចុះឈ្មោះ: <strong>${enr}</strong> (👩${enrF} 👦${enrM})<br>
        			📗 រៀន PLP: <strong>${plp}</strong> = <strong style="color:var(--mid)">${pct(plp,enr)}</strong><br>
        			📝 ធ្វើតេស្ត: <strong>${tst}</strong> = <strong style="color:var(--green)">${pct(tst,enr)}</strong>`;
        	}

        	function st(id,v){ const e=document.getElementById(id); if(e)e.textContent=v; }

        	async function saveData(){
        		const btn=document.getElementById('saveBtn'), stEl=document.getElementById('saveSt');
        		const khmer={}, math={};
        		GR.forEach(g=>{
        			khmer[g]={f:parseInt(document.getElementById(`k_${g}_f`)?.value)||0, m:parseInt(document.getElementById(`k_${g}_m`)?.value)||0};
        			math[g] ={f:parseInt(document.getElementById(`m_${g}_f`)?.value)||0, m:parseInt(document.getElementById(`m_${g}_m`)?.value)||0};
        		});
        		const payload={
        			khmer, math,
        			khmer_enr:{f:parseInt(document.getElementById('k_enr_f')?.value)||0,m:parseInt(document.getElementById('k_enr_m')?.value)||0},
        			khmer_plp:{f:parseInt(document.getElementById('k_plp_f')?.value)||0,m:parseInt(document.getElementById('k_plp_m')?.value)||0},
        			khmer_tst:{f:parseInt(document.getElementById('k_tst_f')?.value)||0,m:parseInt(document.getElementById('k_tst_m')?.value)||0},
        			math_enr: {f:parseInt(document.getElementById('m_enr_f')?.value)||0,m:parseInt(document.getElementById('m_enr_m')?.value)||0},
        			math_plp: {f:parseInt(document.getElementById('m_plp_f')?.value)||0,m:parseInt(document.getElementById('m_plp_m')?.value)||0},
        			math_tst: {f:parseInt(document.getElementById('m_tst_f')?.value)||0,m:parseInt(document.getElementById('m_tst_m')?.value)||0},
        			savedAt: new Date().toLocaleString('km-KH'), month: curMon
        		};
        		btn.textContent='⏳ កំពុងរក្សាទុក…'; btn.disabled=true;
        		document.getElementById('syncBadge').classList.add('syn');
        		document.getElementById('syncBadge').textContent='⏳ Syncing…';
        		try{
        			await fbSave(curCls, curMon, payload);
        			if(!allData[curCls]) allData[curCls]={};
        			allData[curCls][curMon]=payload;
        			btn.textContent='✅ Firebase ✓'; btn.style.background='linear-gradient(135deg,#059669,#10b981)';
        			stEl.textContent='🔥 Saved '+MONTHS.find(m=>m.k===curMon)?.l+': '+payload.savedAt;
        			document.getElementById('syncBadge').textContent='🔥 ✅';
        			buildMonthBar(); buildCGrid(); renderResults(); renderCompare(); renderCombined();
        		}catch(e){ btn.textContent='❌ Error'; stEl.textContent=e.message; }
        		document.getElementById('syncBadge').classList.remove('syn');
        		setTimeout(()=>{btn.textContent='🔥 រក្សាទុកទៅ Firebase';btn.style.background='';btn.disabled=false;},2500);
        	}

        	function pcts(dat){
        		let tF=0,tM=0;
        		GR.forEach(g=>{tF+=dat[g]?.f||0;tM+=dat[g]?.m||0;});
        		const grand=tF+tM, res={_tF:tF,_tM:tM,_tot:grand};
        		GR.forEach(g=>{
        			const f=dat[g]?.f||0,m=dat[g]?.m||0,s=f+m;
        			res[g]={f,m,s,
        				pct:grand>0?+((s/grand)*100).toFixed(1):0,
        				fp:grand>0?+((f/grand)*100).toFixed(1):0,
        				mp:grand>0?+((m/grand)*100).toFixed(1):0};
        		});
        		return res;
        	}

        	function getPlpPct(d, subjKey){
        		const enr=(d[`${subjKey}_enr`]||{f:0,m:0}), plp=(d[`${subjKey}_plp`]||{f:0,m:0}), tst=(d[`${subjKey}_tst`]||{f:0,m:0});
        		const enrT=enr.f+enr.m, plpT=plp.f+plp.m, tstT=tst.f+tst.m;
        		return{enrF:enr.f,enrM:enr.m,enrT,plpF:plp.f,plpM:plp.m,plpT,tstF:tst.f,tstM:tst.m,tstT,
        			plpPct:enrT>0?+((plpT/enrT)*100).toFixed(1):0,
        			tstPct:enrT>0?+((tstT/enrT)*100).toFixed(1):0,
        			plpFPct:enr.f>0?+((plp.f/enr.f)*100).toFixed(1):0,
        			plpMPct:enr.m>0?+((plp.m/enr.m)*100).toFixed(1):0,
        			tstFPct:enr.f>0?+((tst.f/enr.f)*100).toFixed(1):0,
        			tstMPct:enr.m>0?+((tst.m/enr.m)*100).toFixed(1):0};
        	}

        	// ════════════ RESULTS TAB ════════════
        	function renderResults(){
        		const mon=curMon;
        		let done=0, tf=0, tm=0, plpEnr=0, plpSt=0, plpTst=0;
        		CLS.forEach(c=>{
        			const d=allData[c]?.[mon]; if(!d)return; done++;
        			const enrF = Math.max(d.khmer_enr?.f||0, d.math_enr?.f||0);
        			const enrM = Math.max(d.khmer_enr?.m||0, d.math_enr?.m||0);
        			tf += enrF;
        			tm += enrM;
        			['khmer','math'].forEach(sk=>{
        				plpEnr+=(d[`${sk}_enr`]?.f||0)+(d[`${sk}_enr`]?.m||0);
        				plpSt +=(d[`${sk}_plp`]?.f||0)+(d[`${sk}_plp`]?.m||0);
        				plpTst+=(d[`${sk}_tst`]?.f||0)+(d[`${sk}_tst`]?.m||0);
        			});
        		});
        		st('stDone',done); st('stTF',tf); st('stTM',tm);
        		st('stPlp',plpEnr>0?((plpSt/plpEnr)*100).toFixed(1)+'%':'--');
        		st('stTst',plpEnr>0?((plpTst/plpEnr)*100).toFixed(1)+'%':'--');

        		let html='<div class="rgrid">';
        		CLS.forEach(c=>{
        			const d=allData[c]?.[mon];
        			if(!d){ html+=`<div class="rc"><div class="rch"><span class="rcn">ថ្នាក់ ${c}</span><span class="rct">${MONTHS.find(m=>m.k===mon)?.l||mon}</span></div><div class="rcb"><div class="nd">⏳ មិនទាន់មានទិន្នន័យ</div></div></div>`; }
        			else html+=buildRC(c,d);
        		});
        		html+='</div>';
        		document.getElementById('rcont').innerHTML=html;
        	}

        	function buildRC(c,d){
        		const kp=pcts(d.khmer||{}),mp=pcts(d.math||{});
        		const kPlp=getPlpPct(d,'khmer'), mPlp=getPlpPct(d,'math');
        		function bars(p){ return GR.map(g=>{
        			const v=p[g],w=p._tot>0?(v.s/p._tot*100):0;
        			return `<div class="br"><span class="bgl" style="color:${GCOL[g].t}">${g}</span>
        				<div class="btr"><div class="bfi ${GCOL[g].b}" style="width:${w.toFixed(1)}%"></div></div>
        				<span class="bv">${v.pct}%</span></div>
        				<div class="gir"><span class="gif">👩${v.f}(${v.fp}%)</span><span class="gim">👦${v.m}(${v.mp}%)</span></div>`;
        		}).join('');}
        		return `<div class="rc">
        			<div class="rch"><span class="rcn">ថ្នាក់ ${c}</span><span class="rct">${d.savedAt||''}</span></div>
        			<div class="rcb">
        				<div class="plp-mini">
        					<div class="plp-chip">📗 PLP ភាសាខ្មែរ<br><span class="pv">${kPlp.plpPct}%</span><br><span class="pf">👩${kPlp.plpFPct}%</span> <span class="pm">👦${kPlp.plpMPct}%</span></div>
        					<div class="plp-chip">📝 តេស្ត ភាសាខ្មែរ<br><span class="pv" style="color:var(--green)">${kPlp.tstPct}%</span><br><span class="pf">👩${kPlp.tstFPct}%</span> <span class="pm">👦${kPlp.tstMPct}%</span></div>
        					<div class="plp-chip">📗 PLP គណិតវិទ្យា<br><span class="pv">${mPlp.plpPct}%</span><br><span class="pf">👩${mPlp.plpFPct}%</span> <span class="pm">👦${mPlp.plpMPct}%</span></div>
        					<div class="plp-chip">📝 តេស្ត គណិត<br><span class="pv" style="color:var(--green)">${mPlp.tstPct}%</span><br><span class="pf">👩${mPlp.tstFPct}%</span> <span class="pm">👦${mPlp.tstMPct}%</span></div>
        				</div>
        				<div class="stjt">📖 ភាសាខ្មែរ (${kp._tot}·👩${kp._tF} 👦${kp._tM})</div>
        				${bars(kp)}<div class="rdiv"></div>
        				<div class="stjt">🔢 គណិតវិទ្យា (${mp._tot}·👩${mp._tF} 👦${mp._tM})</div>
        				${bars(mp)}
        			</div>
        		</div>`;
        	}

        	function buildCompClassSel(){
        		const sel=document.getElementById('compClassSel');
        		sel.innerHTML='<option value="ALL">📊 គ្រប់ថ្នាក់ (មធ្យម)</option>';
        		CLS.forEach(c=>{ const o=document.createElement('option'); o.value=c; o.textContent='ថ្នាក់ '+c; sel.appendChild(o); });
        	}

        	function renderCompare(){
        		const cont=document.getElementById('compareContainer');
        		const selCls=document.getElementById('compClassSel')?.value||'ALL';
        		const selSubj=document.getElementById('compSubjSel')?.value||'both';
        		const selGender=document.getElementById('compGenderSel')?.value||'all';
        		const hasData=CLS.some(c=>allData[c]&&Object.keys(allData[c]).length>0);
        		if(!hasData){ cont.innerHTML=`<div class="empty"><svg viewBox="0 0 24 24"><path d="M3 13h8V3H3v10zm0 8h8v-6H3v6zm10 0h8V11h-8v10zm0-18v6h8V3h-8z"/></svg><h3>មិនទាន់មានទិន្នន័យ</h3><p>បញ្ចូលទិន្នន័យយ៉ាងហោចណាស់ ១ ខែ</p></div>`; return; }
        		const clsList=selCls==='ALL'?CLS:[selCls];
        		const subjList=selSubj==='both'?['khmer','math']:selSubj==='khmer'?['khmer']:['math'];
        		const monthRows=MONTHS.map(mon=>{
        			let enrF=0,enrM=0,plpF=0,plpM=0,tstF=0,tstM=0;
        			let gradeAll={};
        			GR.forEach(g=>{gradeAll[g]=0;});
        			let grandF=0,grandM=0,hasAny=false;
        			clsList.forEach(c=>{
        				const d=allData[c]?.[mon.k]; if(!d)return; hasAny=true;
        				subjList.forEach(sk=>{
        					const plpData=getPlpPct(d,sk);
        					enrF+=plpData.enrF; enrM+=plpData.enrM;
        					if(selGender==='all'||selGender==='f'){ plpF+=plpData.plpF; tstF+=plpData.tstF; }
        					if(selGender==='all'||selGender==='m'){ plpM+=plpData.plpM; tstM+=plpData.tstM; }
        					const gdat=d[sk]||{};
        					GR.forEach(g=>{
        						const gf=gdat[g]?.f||0, gm=gdat[g]?.m||0;
        						if(selGender==='all'||selGender==='f'){ grandF+=gf; }
        						if(selGender==='all'||selGender==='m'){ grandM+=gm; }
        						gradeAll[g]+=(selGender==='f'?gf:selGender==='m'?gm:gf+gm);
        					});
        				});
        			});
        			if(!hasAny)return null;
        			const grand=grandF+grandM;
        			const enr=(selGender==='all'?enrF+enrM:selGender==='f'?enrF:enrM);
        			const plp=(selGender==='all'?plpF+plpM:selGender==='f'?plpF:plpM);
        			const tst=(selGender==='all'?tstF+tstM:selGender==='f'?tstF:tstM);
        			const gradePct={};
        			GR.forEach(g=>{ gradePct[g]=grand>0?+((gradeAll[g]/grand)*100).toFixed(1):0; });
        			return{ key:mon.k, label:mon.l, enr, plp, tst,
        				plpPct:enr>0?+((plp/enr)*100).toFixed(1):0,
        				tstPct:enr>0?+((tst/enr)*100).toFixed(1):0, gradePct, grand };
        		}).filter(r=>r!==null);
        		if(!monthRows.length){ cont.innerHTML=`<div class="empty"><svg viewBox="0 0 24 24"><path d="M3 13h8V3H3v10zm0 8h8v-6H3v6zm10 0h8V11h-8v10zm0-18v6h8V3h-8z"/></svg><h3>គ្មានទិន្នន័យ</h3><p>ថ្នាក់ "${selCls}" មិនទាន់មានទិន្នន័យ</p></div>`; return; }
        		function trend(cur,prev,key){
        			if(prev===undefined||prev===null)return `<span class="eq">--</span>`;
        			const c=cur[key],p=prev[key],diff=(c-p).toFixed(1);
        			if(diff>0) return `<span class="up">${c}% <span class="trend-icon">▲${diff}</span></span>`;
        			if(diff<0) return `<span class="dn">${c}% <span class="trend-icon">▼${Math.abs(diff)}</span></span>`;
        			return `<span class="eq">${c}% ━</span>`;
        		}
        		function trendGrade(cur,prev,g){
        			if(!prev)return `<span class="eq">${cur.gradePct[g]}%</span>`;
        			const c=cur.gradePct[g],p=prev.gradePct[g],diff=(c-p).toFixed(1);
        			const cls2=(g==='F'?(diff>0?'dn':diff<0?'up':'eq'):(diff>0?'up':diff<0?'dn':'eq'));
        			const icon=diff>0?'▲':diff<0?'▼':'━';
        			return `<span class="${cls2}">${c}%<span class="trend-icon">${icon}${Math.abs(diff)}</span></span>`;
        		}
        		function cellClass(row,g){ const v=row.gradePct[g]; if(g==='F'&&v>20)return 'cell-lo'; if(g==='F'&&v<10)return 'cell-hi'; if(g==='A'&&v>30)return 'cell-hi'; if(g==='E'||g==='F')return v>25?'cell-lo':v<10?'cell-warn':''; return ''; }
        		let html=`<div class="card"><div class="shdr"><div class="sico gr"><svg viewBox="0 0 24 24"><path d="M16 6l2.29 2.29-4.88 4.88-4-4L2 16.59 3.41 18l6-6 4 4 6.3-6.29L22 12V6z"/></svg></div>
        			<div><div class="stit">📈 ប្រៀបធៀប % PLP រៀន / ធ្វើតេស្ត តាមខែ</div>
        			<div class="ssub">${selCls==='ALL'?'គ្រប់ថ្នាក់':'ថ្នាក់ '+selCls} · ${selSubj==='both'?'ខ.ខ+គ':selSubj==='khmer'?'ភ.ខ':'គណិត'} · ${selGender==='all'?'ទាំងអស់':selGender==='f'?'👩ស្រី':'👦ប្រុស'}</div></div></div>
        			<div class="comp-table-wrap"><table class="ctbl"><thead><tr>
        				<th>ខែ</th><th>📋 ចុះឈ្មោះ</th><th>📗 រៀន PLP</th><th>% រៀន</th>
        				<th>📝 ធ្វើតេស្ត</th><th>% តេស្ត</th>
        				${GR.map(g=>`<th class="sec">${g}</th>`).join('')}
        				<th class="sec">🎓 ក្រៅF</th>
        			</tr></thead><tbody>`;
        		monthRows.forEach((row,i)=>{
        			const prev=i>0?monthRows[i-1]:null;
        			const passVal=GR.filter(g=>g!=='F').reduce((a,g)=>a+row.gradePct[g],0).toFixed(1);
        			html+=`<tr><td><strong>${row.label}</strong></td><td>${row.enr}</td><td>${row.plp}</td>
        				<td>${prev?trend(row,prev,'plpPct'):'<span class="eq">'+row.plpPct+'%</span>'}</td>
        				<td>${row.tst}</td>
        				<td>${prev?trend(row,prev,'tstPct'):'<span class="eq">'+row.tstPct+'%</span>'}</td>
        				${GR.map(g=>`<td class="${cellClass(row,g)}">${prev?trendGrade(row,prev,g):'<span class="eq">'+row.gradePct[g]+'%</span>'}</td>`).join('')}
        				<td class="${+passVal>70?'cell-hi':+passVal<50?'cell-lo':'cell-warn'}">${passVal}%</td></tr>`;
        		});
        		html+=`</tbody></table></div></div>`;
        		if(monthRows.length>1){
        			const bestPlp=monthRows.reduce((a,b)=>b.plpPct>a.plpPct?b:a);
        			const bestTst=monthRows.reduce((a,b)=>b.tstPct>a.tstPct?b:a);
        			const worstF=monthRows.reduce((a,b)=>b.gradePct['F']>a.gradePct['F']?b:a);
        			const bestA=monthRows.reduce((a,b)=>b.gradePct['A']>a.gradePct['A']?b:a);
        			html+=`<div class="card"><div class="shdr"><div class="sico or"><svg viewBox="0 0 24 24"><path d="M11.5 2C6.81 2 3 5.81 3 10.5S6.81 19 11.5 19h.5v3c4.86-2.34 8-7 8-11.5C20 5.81 16.19 2 11.5 2zm1 14.5h-2v-2h2v2zm0-4h-2c0-3.25 3-3 3-5 0-1.1-.9-2-2-2s-2 .9-2 2h-2c0-2.21 1.79-4 4-4s4 1.79 4 4c0 2.5-3 2.75-3 5z"/></svg></div>
        				<div><div class="stit">🔍 ការវិភាគ</div></div></div>
        				<div style="display:grid;grid-template-columns:repeat(2,1fr);gap:10px;font-size:.82rem;">
        					<div style="background:var(--light);padding:12px;border-radius:10px;border-left:4px solid var(--green)"><strong>📗 ខែ PLP ល្អបំផុត:</strong><br><span style="font-size:1.1rem;font-weight:800;color:var(--mid)">${bestPlp.label}</span> — ${bestPlp.plpPct}%</div>
        					<div style="background:var(--light);padding:12px;border-radius:10px;border-left:4px solid var(--acc)"><strong>📝 ខែតេស្តល្អបំផុត:</strong><br><span style="font-size:1.1rem;font-weight:800;color:var(--green)">${bestTst.label}</span> — ${bestTst.tstPct}%</div>
        					<div style="background:#fee2e2;padding:12px;border-radius:10px;border-left:4px solid var(--red)"><strong>⚠️ ខែ F ច្រើនបំផុត:</strong><br><span style="font-size:1.1rem;font-weight:800;color:var(--red)">${worstF.label}</span> — ${worstF.gradePct['F']}%</div>
        					<div style="background:#dcfce7;padding:12px;border-radius:10px;border-left:4px solid var(--green)"><strong>🏆 ខែ A ច្រើនបំផុត:</strong><br><span style="font-size:1.1rem;font-weight:800;color:#166534">${bestA.label}</span> — ${bestA.gradePct['A']}%</div>
        				</div></div>`;
        		}
        		if(selCls==='ALL'){
        			const availMonths=MONTHS.filter(m=>CLS.some(c=>allData[c]?.[m.k]));
        			if(availMonths.length){
        				html+=`<div class="card"><div class="shdr"><div class="sico bl"><svg viewBox="0 0 24 24"><path d="M3 13h8V3H3v10zm0 8h8v-6H3v6zm10 0h8V11h-8v10zm0-18v6h8V3h-8z"/></svg></div><div><div class="stit">% PLP រៀន — ប្រៀបធៀបថ្នាក់×ខែ</div></div></div>
        				<div style="overflow-x:auto"><table class="ctbl"><thead><tr><th>ថ្នាក់</th>${availMonths.map(m=>`<th>${m.l}</th>`).join('')}</tr></thead><tbody>`;
        				CLS.forEach(c=>{
        					html+=`<tr><td>${c}</td>`;
        					availMonths.forEach(m=>{
        						const d=allData[c]?.[m.k];
        						if(!d){ html+=`<td style="color:var(--muted);font-size:.7rem">--</td>`; return; }
        						let enr=0,plp=0;
        						subjList.forEach(sk=>{ const p=getPlpPct(d,sk); enr+=p.enrT; plp+=p.plpT; });
        						const pct=enr>0?((plp/enr)*100).toFixed(0):0;
        						const bg=+pct>=80?'cell-hi':+pct>=60?'cell-warn':+pct<40?'cell-lo':'';
        						html+=`<td class="${bg}">${pct}%</td>`;
        					});
        					html+=`</tr>`;
        				});
        				html+=`</tbody></table></div></div>`;
        				html+=`<div class="card"><div class="shdr"><div class="sico pk"><svg viewBox="0 0 24 24"><path d="M16 6l2.29 2.29-4.88 4.88-4-4L2 16.59 3.41 18l6-6 4 4 6.3-6.29L22 12V6z"/></svg></div><div><div class="stit">% F — ប្រៀបធៀបថ្នាក់×ខែ (ទាប=ល្អ)</div></div></div>
        				<div style="overflow-x:auto"><table class="ctbl"><thead><tr><th>ថ្នាក់</th>${availMonths.map(m=>`<th>${m.l}</th>`).join('')}</tr></thead><tbody>`;
        				CLS.forEach(c=>{
        					html+=`<tr><td>${c}</td>`;
        					availMonths.forEach(m=>{
        						const d=allData[c]?.[m.k];
        						if(!d){ html+=`<td style="color:var(--muted);font-size:.7rem">--</td>`; return; }
        						let allPct={};
        						subjList.forEach(sk=>{ const p=pcts(d[sk]||{}); GR.forEach(g=>{ allPct[g]=(allPct[g]||0)+(p[g]?.pct||0); }); });
        						const fPct=(allPct['F']/(subjList.length||1)).toFixed(0);
        						const bg=+fPct>25?'cell-lo':+fPct<10?'cell-hi':'';
        						html+=`<td class="${bg}">${fPct}%</td>`;
        					});
        					html+=`</tr>`;
        				});
        				html+=`</tbody></table></div></div>`;
        			}
        		}
        		cont.innerHTML=html;
        	}

        	function buildCombMonthSel(){
        		const sel=document.getElementById('combMonthSel');
        		sel.innerHTML='<option value="ALL">📊 គ្រប់ខែ (មធ្យម)</option>';
        		MONTHS.forEach(m=>{ const o=document.createElement('option'); o.value=m.k; o.textContent='📅 '+m.l; sel.appendChild(o); });
        	}

        	function renderCombined(){
        		const cont=document.getElementById('ccont');
        		const selMon=document.getElementById('combMonthSel')?.value||'ALL';
        		const monList=selMon==='ALL'?MONTHS.map(m=>m.k):[selMon];
        		const cls=CLS.filter(c=>allData[c]&&monList.some(mk=>allData[c][mk]));
        		if(!cls.length){ cont.innerHTML=`<div class="empty"><svg viewBox="0 0 24 24"><path d="M3 13h8V3H3v10zm0 8h8v-6H3v6zm10 0h8V11h-8v10zm0-18v6h8V3h-8z"/></svg><h3>មិនទាន់មានទិន្នន័យ</h3></div>`; return; }
        		const ka={},ma={},oa={}; GR.forEach(g=>{ka[g]={f:0,m:0};ma[g]={f:0,m:0};oa[g]={f:0,m:0};});
        		let gKF=0,gKM=0,gMF=0,gMM=0, totalEnr=0,totalPlp=0,totalTst=0, samples=0;
        		cls.forEach(c=>{ monList.forEach(mk=>{
        			const d=allData[c]?.[mk]; if(!d)return; samples++;
        			GR.forEach(g=>{
        				ka[g].f+=d.khmer?.[g]?.f||0; ka[g].m+=d.khmer?.[g]?.m||0;
        				ma[g].f+=d.math?.[g]?.f||0;  ma[g].m+=d.math?.[g]?.m||0;
        			});
        			gKF+=GR.reduce((a,g)=>a+(d.khmer?.[g]?.f||0),0); gKM+=GR.reduce((a,g)=>a+(d.khmer?.[g]?.m||0),0);
        			gMF+=GR.reduce((a,g)=>a+(d.math?.[g]?.f||0),0);  gMM+=GR.reduce((a,g)=>a+(d.math?.[g]?.m||0),0);
        			['khmer','math'].forEach(sk=>{
        				totalEnr+=(d[`${sk}_enr`]?.f||0)+(d[`${sk}_enr`]?.m||0);
        				totalPlp+=(d[`${sk}_plp`]?.f||0)+(d[`${sk}_plp`]?.m||0);
        				totalTst+=(d[`${sk}_tst`]?.f||0)+(d[`${sk}_tst`]?.m||0);
        			});
        		});});
        		GR.forEach(g=>{ oa[g].f=ka[g].f+ma[g].f; oa[g].m=ka[g].m+ma[g].m; });
        		const gK=gKF+gKM,gM=gMF+gMM,gA=gK+gM, gF=gKF+gMF,gMl=gKM+gMM;
        		function agg(obj,grand){ const r={};
        			GR.forEach(g=>{ const s=obj[g].f+obj[g].m;
        				r[g]={f:obj[g].f,m:obj[g].m,s,pct:grand>0?+((s/grand)*100).toFixed(1):0,
        					fp:grand>0?+((obj[g].f/grand)*100).toFixed(1):0,mp:grand>0?+((obj[g].m/grand)*100).toFixed(1):0};});
        			r._t=grand;r._tF=GR.reduce((a,g)=>a+obj[g].f,0);r._tM=GR.reduce((a,g)=>a+obj[g].m,0); return r;
        		}
        		const KA=agg(ka,gK),MA=agg(ma,gM),OA=agg(oa,gA);
        		const fPct=OA['F']?.pct||0;
        		const plpPct=totalEnr>0?((totalPlp/totalEnr)*100).toFixed(1):0;
        		const tstPct=totalEnr>0?((totalTst/totalEnr)*100).toFixed(1):0;
        		const alrt=fPct>20
        			?`<div class="alrt aw">⚠️ ជាមធ្យម <strong>${fPct}%</strong> (${OA['F'].s} ករណី) ទទួល F — ត្រូវការជំរុញ!</div>`
        			:`<div class="alrt aok">✅ ជាមធ្យម <strong>${fPct}%</strong> (${OA['F'].s} ករណី) ទទួល F — ស្ថានភាពល្អ</div>`;
        		const citems=GR.map(g=>`<div class="comi"><div class="gl">${g}</div><div class="gp">${OA[g].pct}%</div>
        			<div class="gd">${OA[g].s} ករណី</div>
        			<div class="gg"><span class="ggf">👩${OA[g].fp}%</span><span class="ggm">👦${OA[g].mp}%</span></div></div>`).join('');
        		function subBars(a){ return GR.map(g=>`<div class="br">
        			<span class="bgl" style="color:${GCOL[g].t}">${g}</span>
        			<div class="btr"><div class="bfi ${GCOL[g].b}" style="width:${a[g].pct}%"></div></div>
        			<span class="bv">${a[g].pct}%</span></div>
        			<div class="gir"><span class="gif">👩${a[g].fp}%</span><span class="gim">👦${a[g].mp}%</span></div>`).join('');}
        		const dtHead=`<tr><th>ថ្នាក់</th>${GR.map(g=>`<th colspan="3">${g}</th>`).join('')}</tr>
        			<tr><th></th>${GR.map(()=>'<th>%</th><th style="color:#f9a8d4;font-size:.65rem">👩</th><th style="color:#93c5fd;font-size:.65rem">👦</th>').join('')}</tr>`;
        		function subjRows(sk){
        			return cls.map(c=>{
        				let combined={}; GR.forEach(g=>{combined[g]={f:0,m:0};});
        				monList.forEach(mk=>{ const d=allData[c]?.[mk]; if(!d)return;
        					GR.forEach(g=>{combined[g].f+=d[sk]?.[g]?.f||0;combined[g].m+=d[sk]?.[g]?.m||0;});});
        				const p=pcts(combined);
        				return `<tr><td>${c}</td>${GR.map(g=>`<td>${p[g].pct}%</td><td style="color:var(--fem)">${p[g].f}</td><td style="color:var(--mal)">${p[g].m}</td>`).join('')}</tr>`;
        			}).join('');
        		}
        		function totRow(a){ return `<tr class="dttot"><td>ផ្នត់</td>${GR.map(g=>`<td>${a[g].pct}%</td><td style="color:var(--fem)">${a[g].f}</td><td style="color:var(--mal)">${a[g].m}</td>`).join('')}</tr>`;}
        		cont.innerHTML=`
        			${alrt}
        			<div class="sstrip">
        				<div class="schi gc"><div class="sv">${plpPct}%</div><div class="sl">📗 % PLP រៀន</div></div>
        				<div class="schi oc"><div class="sv">${tstPct}%</div><div class="sl">📝 % ធ្វើតេស្ត</div></div>
        				<div class="schi fc"><div class="sv">${gF}</div><div class="sl">👩 ស្រី</div></div>
        				<div class="schi mc"><div class="sv">${gMl}</div><div class="sl">👦 ប្រុស</div></div>
        				<div class="schi"><div class="sv">${gA>0?((gF/gA)*100).toFixed(0)+'%':'--'}</div><div class="sl">% ស្រី</div></div>
        			</div>
        			<div class="comhdr">
        				<div class="comtit">🏆 ១២ថ្នាក់ — ${cls.length} ថ្នាក់ · ${samples} ខែ (👩${gF} 👦${gMl} = ${gA})</div>
        				<div class="comgrid">${citems}</div>
        			</div>
        			<div class="tcol">
        				<div class="card"><div class="shdr"><div class="sico bl"><svg viewBox="0 0 24 24"><path d="M21 5c-1.11-.35-2.33-.5-3.5-.5-1.95 0-4.05.4-5.5 1.5-1.45-1.1-3.55-1.5-5.5-1.5S2.45 4.9 1 6v14.65c0 .25.25.5.5.5.1 0 .15-.05.25-.05C3.1 20.45 5.05 20 6.5 20c1.95 0 4.05.4 5.5 1.5 1.35-.85 3.8-1.5 5.5-1.5 1.65 0 3.35.3 4.75 1.05.1.05.15.05.25.05.25 0 .5-.25.5-.5V6c-.6-.45-1.25-.75-2-1z"/></svg></div>
        					<div><div class="stit">📖 ភាសាខ្មែរ (${gK}·👩${gKF} 👦${gKM})</div></div></div>
        					${subBars(KA)}</div>
        				<div class="card"><div class="shdr"><div class="sico go"><svg viewBox="0 0 24 24"><path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2z"/></svg></div>
        					<div><div class="stit">🔢 គណិតវិទ្យា (${gM}·👩${gMF} 👦${gMM})</div></div></div>
        					${subBars(MA)}</div>
        			</div>
        			<div class="card"><div class="shdr"><div class="sico bl"><svg viewBox="0 0 24 24"><path d="M3 13h8V3H3v10zm0 8h8v-6H3v6zm10 0h8V11h-8v10zm0-18v6h8V3h-8z"/></svg></div><div><div class="stit">📖 ភាសាខ្មែរ — ស្រី/ប្រុស លម្អិត</div></div></div>
        				<div style="overflow-x:auto"><table class="dtbl"><thead>${dtHead}</thead><tbody>${subjRows('khmer')}</tbody><tfoot>${totRow(KA)}</tfoot></table></div></div>
        			<div class="card"><div class="shdr"><div class="sico go"><svg viewBox="0 0 24 24"><path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2z"/></svg></div><div><div class="stit">🔢 គណិតវិទ្យា — ស្រី/ប្រុស លម្អិត</div></div></div>
        				<div style="overflow-x:auto"><table class="dtbl"><thead>${dtHead}</thead><tbody>${subjRows('math')}</tbody><tfoot>${totRow(MA)}</tfoot></table></div></div>`;
        	}

        	function sw(n,btn){
        		document.querySelectorAll('.tc').forEach(t=>t.classList.remove('act'));
        		document.querySelectorAll('.ntab').forEach(b=>b.classList.remove('act'));
        		document.getElementById('tc-'+n).classList.add('act');
        		if(btn)btn.classList.add('act');
        		if(n==='results')renderResults();
        		if(n==='compare')renderCompare();
        		if(n==='combined')renderCombined();
        	}

        	// ════════════ EXPORT FUNCTIONS ════════════
        	function exportInputTab(format){
        		const timestamp = new Date().toLocaleString('km-KH').replace(/[\s:/]/g,'-');
        		const cls = curCls, month = curMon;
        		const monLabel = MONTHS.find(m=>m.k===month)?.l || month;

        		if(format==='xlsx'){
        			const ws = XLSX.utils.aoa_to_sheet([
        				['PLP ២០២៦ — ទិន្នន័យបញ្ចូល'],
        				['ថ្នាក់: '+cls],
        				['ខែ: '+monLabel],
        				[''],
        				['ភាសាខ្មែរ — ក្រដាស់ដែលបង្ហាញលម្អិត'],
        				['និទ្ទេស','👩 ស្រី','👦 ប្រុស','សរុប','%'],
        				...GR.map(g=>[
        					g,
        					document.getElementById(`k_${g}_f`)?.value||0,
        					document.getElementById(`k_${g}_m`)?.value||0,
        					(parseInt(document.getElementById(`k_${g}_f`)?.value||0) + parseInt(document.getElementById(`k_${g}_m`)?.value||0)).toString(),
        					document.getElementById(`k_${g}_pct`)?.textContent||'-'
        				]),
        				[''],
        				['គណិតវិទ្យា — ក្រដាស់ដែលបង្ហាញលម្អិត'],
        				['និទ្ទេស','👩 ស្រី','👦 ប្រុស','សរុប','%'],
        				...GR.map(g=>[
        					g,
        					document.getElementById(`m_${g}_f`)?.value||0,
        					document.getElementById(`m_${g}_m`)?.value||0,
        					(parseInt(document.getElementById(`m_${g}_f`)?.value||0) + parseInt(document.getElementById(`m_${g}_m`)?.value||0)).toString(),
        					document.getElementById(`m_${g}_pct`)?.textContent||'-'
        				]),
        				[''],
        				['PLP ស្ថិតិ'],
        				['ភាសាខ្មែរ'],
        				['ចុះឈ្មោះ: '+document.getElementById('k_enr_f').value+' ស្រី + '+document.getElementById('k_enr_m').value+' ប្រុស'],
        				['រៀន PLP: '+document.getElementById('k_plp_f').value+' ស្រី + '+document.getElementById('k_plp_m').value+' ប្រុស'],
        				['ធ្វើតេស្ត: '+document.getElementById('k_tst_f').value+' ស្រី + '+document.getElementById('k_tst_m').value+' ប្រុស'],
        				[''],
        				['គណិតវិទ្យា'],
        				['ចុះឈ្មោះ: '+document.getElementById('m_enr_f').value+' ស្រី + '+document.getElementById('m_enr_m').value+' ប្រុស'],
        				['រៀន PLP: '+document.getElementById('m_plp_f').value+' ស្រី + '+document.getElementById('m_plp_m').value+' ប្រុស'],
        				['ធ្វើតេស្ត: '+document.getElementById('m_tst_f').value+' ស្រី + '+document.getElementById('m_tst_m').value+' ប្រុស']
        			]);
        			const wb = XLSX.utils.book_new();
        			XLSX.utils.book_append_sheet(wb, ws, 'Input');
        			XLSX.writeFile(wb, `PLP_${cls}_${month}_${timestamp}.xlsx`);
        		}
        		else if(format==='html'){
        			const html = `<!DOCTYPE html>
        <html lang="km">
        <head><meta charset="UTF-8"><title>PLP ${cls} ${monLabel}</title>
        <style>body{font-family:'Kantumruy Pro',sans-serif;margin:20px;background:#f8fafc}
        .card{background:#fff;padding:20px;margin:20px 0;border-radius:10px;box-shadow:0 2px 8px rgba(0,0,0,.1)}
        h1,h2{color:#0f2044}table{width:100%;border-collapse:collapse;margin:10px 0}
        th{background:#0f2044;color:#fff;padding:10px;text-align:left}
        td{padding:8px;border-bottom:1px solid #e2e8f0}
        .stat{display:inline-block;margin:10px 20px 10px 0}
        .stat-val{font-size:24px;font-weight:bold;color:#0f2044}
        .stat-lbl{font-size:12px;color:#64748b}
        </style></head>
        <body><div class="card">
        <h1>ប្រព័ន្ធតាមដាន PLP ២០២៦</h1>
        <p><strong>ថ្នាក់:</strong> ${cls} | <strong>ខែ:</strong> ${monLabel}</p>
        <p><strong>កាលបរិច្ឆេទ:</strong> ${new Date().toLocaleString('km-KH')}</p>
        </div>
        <div class="card"><h2>📖 ភាសាខ្មែរ</h2>
        <table><tr><th>និទ្ទេស</th><th>👩 ស្រី</th><th>👦 ប្រុស</th><th>សរុប</th><th>%</th></tr>
        ${GR.map(g=>`<tr><td>${g}</td><td>${document.getElementById(`k_${g}_f`)?.value||0}</td><td>${document.getElementById(`k_${g}_m`)?.value||0}</td><td>${parseInt(document.getElementById(`k_${g}_f`)?.value||0) + parseInt(document.getElementById(`k_${g}_m`)?.value||0)}</td><td>${document.getElementById(`k_${g}_pct`)?.textContent||'-'}</td></tr>`).join('')}
        </table><div><div class="stat"><div class="stat-val">${document.getElementById('k_enr_f').value || 0}</div><div class="stat-lbl">👩 ចុះឈ្មោះ</div></div>
        <div class="stat"><div class="stat-val">${document.getElementById('k_enr_m').value || 0}</div><div class="stat-lbl">👦 ចុះឈ្មោះ</div></div>
        <div class="stat"><div class="stat-val">${document.getElementById('k_plp_f').value || 0}</div><div class="stat-lbl">👩 រៀន PLP</div></div>
        <div class="stat"><div class="stat-val">${document.getElementById('k_plp_m').value || 0}</div><div class="stat-lbl">👦 រៀន PLP</div></div></div>
        </div><div class="card"><h2>🔢 គណិតវិទ្យា</h2>
        <table><tr><th>និទ្ទេស</th><th>👩 ស្រី</th><th>👦 ប្រុស</th><th>សរុប</th><th>%</th></tr>
        ${GR.map(g=>`<tr><td>${g}</td><td>${document.getElementById(`m_${g}_f`)?.value||0}</td><td>${document.getElementById(`m_${g}_m`)?.value||0}</td><td>${parseInt(document.getElementById(`m_${g}_f`)?.value||0) + parseInt(document.getElementById(`m_${g}_m`)?.value||0)}</td><td>${document.getElementById(`m_${g}_pct`)?.textContent||'-'}</td></tr>`).join('')}
        </table><div><div class="stat"><div class="stat-val">${document.getElementById('m_enr_f').value || 0}</div><div class="stat-lbl">👩 ចុះឈ្មោះ</div></div>
        <div class="stat"><div class="stat-val">${document.getElementById('m_enr_m').value || 0}</div><div class="stat-lbl">👦 ចុះឈ្មោះ</div></div>
        <div class="stat"><div class="stat-val">${document.getElementById('m_plp_f').value || 0}</div><div class="stat-lbl">👩 រៀន PLP</div></div>
        <div class="stat"><div class="stat-val">${document.getElementById('m_plp_m').value || 0}</div><div class="stat-lbl">👦 រៀន PLP</div></div></div>
        </div></body></html>`;
        			const blob = new Blob([html], {type:'text/html'});
        			const url = URL.createObjectURL(blob);
        			const a = document.createElement('a');
        			a.href = url;
        			a.download = `PLP_${cls}_${month}_${timestamp}.html`;
        			a.click();
        			URL.revokeObjectURL(url);
        		}
        		else if(format==='json'){
        			const jsonData = {
        				class: cls,
        				month: { key: month, label: monLabel },
        				exportedAt: new Date().toISOString(),
        				khmer: {
        					enrollment: {f: parseInt(document.getElementById('k_enr_f').value)||0, m: parseInt(document.getElementById('k_enr_m').value)||0},
        					plp: {f: parseInt(document.getElementById('k_plp_f').value)||0, m: parseInt(document.getElementById('k_plp_m').value)||0},
        					test: {f: parseInt(document.getElementById('k_tst_f').value)||0, m: parseInt(document.getElementById('k_tst_m').value)||0},
        					grades: {}
        				},
        				math: {
        					enrollment: {f: parseInt(document.getElementById('m_enr_f').value)||0, m: parseInt(document.getElementById('m_enr_m').value)||0},
        					plp: {f: parseInt(document.getElementById('m_plp_f').value)||0, m: parseInt(document.getElementById('m_plp_m').value)||0},
        					test: {f: parseInt(document.getElementById('m_tst_f').value)||0, m: parseInt(document.getElementById('m_tst_m').value)||0},
        					grades: {}
        				}
        			};
        			GR.forEach(g=>{
        				jsonData.khmer.grades[g] = {f: parseInt(document.getElementById(`k_${g}_f`)?.value)||0, m: parseInt(document.getElementById(`k_${g}_m`)?.value)||0};
        				jsonData.math.grades[g] = {f: parseInt(document.getElementById(`m_${g}_f`)?.value)||0, m: parseInt(document.getElementById(`m_${g}_m`)?.value)||0};
        			});
        			const blob = new Blob([JSON.stringify(jsonData, null, 2)], {type:'application/json'});
        			const url = URL.createObjectURL(blob);
        			const a = document.createElement('a');
        			a.href = url;
        			a.download = `PLP_${cls}_${month}_${timestamp}.json`;
        			a.click();
        			URL.revokeObjectURL(url);
        		}
        	}

        	function exportTab(tabName, format){
        		const timestamp = new Date().toLocaleString('km-KH').replace(/[\s:/]/g,'-');
        		const cont = document.getElementById('tc-'+tabName);
        		if(!cont) return;

        		if(format==='xlsx'){
        			const table = cont.querySelector('table');
        			if(!table){
        				alert('No table found in this tab');
        				return;
        			}
        			const ws = XLSX.utils.table_to_sheet(table);
        			const wb = XLSX.utils.book_new();
        			XLSX.utils.book_append_sheet(wb, ws, tabName);
        			XLSX.writeFile(wb, `PLP_${tabName}_${timestamp}.xlsx`);
        		}
        		else if(format==='html'){
        			const html = `<!DOCTYPE html>
        <html lang="km">
        <head><meta charset="UTF-8"><title>PLP ${tabName}</title>
        <style>body{font-family:'Kantumruy Pro',sans-serif;margin:20px;background:#f8fafc}
        .content{background:#fff;padding:20px;border-radius:10px;box-shadow:0 2px 8px rgba(0,0,0,.1)}
        table{width:100%;border-collapse:collapse}th{background:#0f2044;color:#fff;padding:10px}
        td{padding:8px;border-bottom:1px solid #e2e8f0}</style>
        </head><body><div class="content"><h1>PLP ${tabName} - ${new Date().toLocaleString('km-KH')}</h1>${cont.innerHTML}</div></body></html>`;
        			const blob = new Blob([html], {type:'text/html'});
        			const url = URL.createObjectURL(blob);
        			const a = document.createElement('a');
        			a.href = url;
        			a.download = `PLP_${tabName}_${timestamp}.html`;
        			a.click();
        			URL.revokeObjectURL(url);
        		}
        		else if(format==='json'){
        			const tables = cont.querySelectorAll('table');
        			const jsonData = {
        				tab: tabName,
        				exportedAt: new Date().toISOString(),
        				tablesCount: tables.length,
        				data: []
        			};
        			tables.forEach((table,idx)=>{
        				const rows = [];
        				table.querySelectorAll('tr').forEach(tr=>{
        					const row = [];
        					tr.querySelectorAll('th,td').forEach(cell=>{
        						row.push(cell.textContent.trim());
        					});
        					rows.push(row);
        				});
        				jsonData.data.push({tableIndex: idx, rows});
        			});
        			const blob = new Blob([JSON.stringify(jsonData, null, 2)], {type:'application/json'});
        			const url = URL.createObjectURL(blob);
        			const a = document.createElement('a');
        			a.href = url;
        			a.download = `PLP_${tabName}_${timestamp}.json`;
        			a.click();
        			URL.revokeObjectURL(url);
        		}
        	}

        	buildCGrid();
        	
         </script>
      
   </template>
<template id="tpl-payment">
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=0.85">
<title>ប្រព័ន្ធទូទាត់ថវិកា</title>
<script src="https://www.gstatic.com/firebasejs/10.12.2/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/10.12.2/firebase-firestore-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/10.12.2/firebase-auth-compat.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Siemreap',Arial,sans-serif;font-size:10.5pt;background:#eef1f7;min-height:100vh}

/* ══════════ AUTH ══════════ */
#auth-screen{min-height:100vh;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,#1155cc,#0d47a1)}
.auth-box{background:#fff;border-radius:14px;padding:32px 30px;width:370px;box-shadow:0 16px 48px rgba(0,0,0,.3)}
.auth-logo{text-align:center;font-size:28px;margin-bottom:6px}
.auth-title{text-align:center;font-family:Siemreap;font-size:13pt;color:#1155cc;margin-bottom:20px}
.auth-tabs{display:flex;border-bottom:2px solid #e0e0e0;margin-bottom:20px}
.auth-tab{flex:1;padding:8px;text-align:center;cursor:pointer;font-family:Siemreap;font-size:10.5pt;color:#888;border-bottom:3px solid transparent;margin-bottom:-2px;transition:.2s}
.auth-tab.active{color:#1155cc;border-bottom-color:#1155cc;font-weight:bold}
.auth-form{display:none}.auth-form.active{display:block}
.frow{margin-bottom:13px}
.frow label{display:block;font-size:8.5pt;color:#555;margin-bottom:3px;font-family:Siemreap}
.frow input{width:100%;border:1.5px solid #ddd;border-radius:6px;padding:9px 11px;font-family:Siemreap;font-size:10.5pt;outline:none;transition:.2s}
.frow input:focus{border-color:#5b95f9;box-shadow:0 0 0 3px rgba(91,149,249,.15)}
.abtn{width:100%;background:#1155cc;color:#fff;border:none;padding:11px;border-radius:7px;cursor:pointer;font-family:Siemreap;font-size:11pt;font-weight:bold;margin-top:4px;transition:.2s}
.abtn:hover{background:#0d47a1}.abtn:disabled{background:#aaa;cursor:not-allowed}
.auth-err{color:#c62828;font-size:9pt;text-align:center;margin-top:10px;min-height:18px;font-family:Siemreap}
.auth-info{background:#e8f5e9;border-radius:6px;padding:9px 12px;font-size:9pt;color:#2e7d32;margin-bottom:14px;font-family:Siemreap;line-height:1.6}

/* ══════════ MAIN TABS ══════════ */
#main-app{display:none}
.main-tab-bar{display:flex;background:#0d3a91;padding:0 10px;position:sticky;top:0;z-index:100;box-shadow:0 2px 8px rgba(0,0,0,.3)}
.main-tab{flex:1;padding:11px 6px;text-align:center;cursor:pointer;font-family:Siemreap;font-size:10.5pt;color:rgba(255,255,255,.65);border-bottom:3px solid transparent;transition:.2s;white-space:nowrap}
.main-tab:hover{color:#fff;background:rgba(255,255,255,.07)}
.main-tab.active{color:#fff;border-bottom-color:#5b95f9;font-weight:bold;background:rgba(255,255,255,.1)}
.tab-panel{display:none;padding:10px}
.tab-panel.active{display:block}

/* ══════════ APP BAR ══════════ */
.app-bar{display:flex;align-items:center;justify-content:space-between;margin-bottom:9px;flex-wrap:wrap;gap:6px;background:#1155cc;padding:8px 14px;border-radius:9px;color:#fff}
.app-title{font-size:12pt;font-family:Siemreap;font-weight:bold}
.user-info{font-size:9pt;font-family:Siemreap;display:flex;align-items:center;gap:8px}
.user-badge{background:rgba(255,255,255,.2);padding:3px 10px;border-radius:12px;font-size:9pt}
.logout-btn{background:rgba(255,255,255,.15);border:1px solid rgba(255,255,255,.4);color:#fff;padding:3px 11px;border-radius:5px;cursor:pointer;font-family:Siemreap;font-size:9pt}
.logout-btn:hover{background:rgba(255,255,255,.3)}
.toolbar{display:flex;gap:6px;flex-wrap:wrap;align-items:center;margin-bottom:9px}
.tbtn{border:none;padding:3px 8px;border-radius:5px;cursor:pointer;font-family:Siemreap;font-size:8pt;font-weight:bold}
.tb-blue{background:#1155cc;color:#fff}.tb-green{background:#34a853;color:#fff}
.tb-orange{background:#e65100;color:#fff}
.tbtn:hover{opacity:.84}
.sync-dot{width:10px;height:10px;border-radius:50%;background:#fbbc04;display:inline-block;margin-right:4px;transition:.3s}
.sync-dot.ok{background:#34a853}.sync-dot.err{background:#ea4335}
.sync-lbl{font-size:9pt;color:#555;font-family:Siemreap}
.rt-badge{background:#e8f5e9;border:1px solid #a5d6a7;color:#2e7d32;font-size:8pt;padding:2px 8px;border-radius:10px;font-family:Siemreap;margin-left:4px}
.rt-badge.busy{background:#fff8e1;border-color:#ffe082;color:#f57f17}

/* ══════════ PERIOD BAR ══════════ */
.period-bar{display:flex;align-items:center;gap:6px;flex-wrap:wrap;background:#fff;border:1.5px solid #c5cae9;border-radius:9px;padding:7px 12px;margin-bottom:9px}
.period-bar .plbl{font-family:Siemreap;font-size:9pt;color:#555;margin-right:4px;white-space:nowrap}
.yr-sel{border:1.5px solid #aaa;border-radius:5px;padding:4px 8px;font-family:Siemreap;font-size:10pt;outline:none;cursor:pointer}
.q-tabs{display:flex;gap:4px;flex-wrap:wrap}
.q-tab{border:1.5px solid #aaa;background:#f5f5f5;border-radius:6px;padding:5px 13px;cursor:pointer;font-family:Siemreap;font-size:10pt;transition:.2s;white-space:nowrap}
.q-tab:hover{background:#e3f2fd;border-color:#5b95f9}
.q-tab.active{background:#1155cc;color:#fff;border-color:#1155cc;font-weight:bold}
.q-tab .qmonths{font-size:7.5pt;opacity:.8;display:block}
.period-badge{background:#e8f5e9;border:1px solid #a5d6a7;color:#1b5e20;font-size:8.5pt;padding:2px 9px;border-radius:10px;font-family:Siemreap;margin-left:auto;white-space:nowrap}

/* ══════════ TABLE ══════════ */
.tbl-wrap{overflow-x:auto}
table{border-collapse:collapse;width:100%;background:#fff;min-width:960px}
td{border:1px solid #666;padding:2px 3px;vertical-align:middle;font-size:10pt}
.th-main td{background:#5b95f9;text-align:center;font-weight:bold;font-family:Siemreap;font-size:10pt;padding:4px 3px}
.g-h1 td{background:#1155cc;color:#fff;font-family:Siemreap}
.g-h1 input,.g-h1 select{background:transparent;color:#fff;border:none;width:100%;font-family:Siemreap;font-size:10pt;outline:none}
.g-h1 select option{color:#000;background:#fff}
.g-h1 .tc{text-align:center}.g-h1 .tr{text-align:right;padding-right:5px;font-weight:bold}
.g-h2 td{background:#cfd8f6;padding:3px 8px}
.hbtn{background:none;border:1px solid #aaa;border-radius:4px;cursor:pointer;padding:2px 8px;font-size:11px;margin-right:3px;font-family:Siemreap}
.hbtn:hover{background:#e0e0e0}
.d-row td{background:#fff;font-family:Siemreap}
.d-row td.emp{background:#fafafa;border-color:#ddd}
.d-row td.tr{text-align:right;padding-right:5px}.d-row td.tc{text-align:center}
.d-row input{border:none;width:100%;font-family:Siemreap;font-size:10pt;outline:none;background:transparent}
.d-row input[type=number]{text-align:right}
.g-r3{display:none}
.g-r3 td{background:#e8f0fe;border-top:2px solid #5b95f9;padding:5px 6px}
.r3w{display:flex;gap:4px;align-items:center;flex-wrap:wrap}
.r3w input{border:1px solid #aaa;border-radius:3px;padding:4px 6px;font-family:Siemreap;font-size:10pt;outline:none}
.r3w input:focus{border-color:#5b95f9}
.r3w .fl{flex:1;min-width:140px}.r3w .fs{width:68px}.r3w .fm{width:96px}
.cbtns{display:flex;justify-content:flex-end;gap:4px;flex-wrap:wrap;margin-top:4px}
.cbtn{border:none;border-radius:4px;padding:4px 11px;cursor:pointer;font-family:Siemreap;font-size:10pt;font-weight:bold}
.cb-add{background:#34a853;color:#fff}.cb-edit{background:#fbbc04;color:#000}
.cb-del{background:#ea4335;color:#fff}.cb-save{background:#1155cc;color:#fff}
.cbtn:hover{opacity:.83}
.total-row td{background:#fce8b2;font-weight:bold;font-family:Siemreap;border-top:2px solid #000}

/* ══════════ SETUP TOOL ══════════ */
.setup-wrap{max-width:480px;margin:0 auto}
.card{background:#fff;border-radius:16px;padding:32px 28px;width:100%;box-shadow:0 8px 32px rgba(0,0,0,.15)}
.card .logo{text-align:center;font-size:36px;margin-bottom:8px}
.card h1{text-align:center;font-family:Siemreap;font-size:14pt;color:#1155cc;margin-bottom:4px}
.card .sub{text-align:center;font-size:9pt;color:#888;font-family:Siemreap;margin-bottom:24px}
.btn{width:100%;padding:12px;border:none;border-radius:8px;cursor:pointer;font-family:Siemreap;font-size:11pt;font-weight:bold;margin-top:6px;transition:.2s}
.btn-blue{background:#1155cc;color:#fff}.btn-blue:hover{background:#0d47a1}
.btn-green{background:#34a853;color:#fff}.btn-green:hover{background:#2e7d32}
.btn-red{background:#ea4335;color:#fff}.btn-red:hover{background:#c62828}
.btn:disabled{background:#bbb;cursor:not-allowed}
.s-status{border-radius:8px;padding:12px 14px;margin-top:14px;font-family:Siemreap;font-size:10pt;line-height:1.8;display:none}
.s-status.info{background:#e3f2fd;color:#0d47a1;display:block}
.s-status.ok{background:#e8f5e9;color:#1b5e20;display:block}
.s-status.err{background:#ffebee;color:#b71c1c;display:block}
.prog-wrap{margin-top:14px;display:none}
.prog-bar-bg{background:#e0e0e0;border-radius:8px;height:14px;overflow:hidden}
.prog-bar{background:#34a853;height:100%;width:0%;transition:.3s;border-radius:8px}
.prog-lbl{text-align:center;font-size:9pt;color:#555;font-family:Siemreap;margin-top:4px}
.preview{margin-top:18px;display:none}
.preview h3{font-family:Siemreap;font-size:11pt;color:#333;margin-bottom:8px}
.sect-list{max-height:220px;overflow-y:auto;border:1px solid #e0e0e0;border-radius:8px}
.sect-item{padding:10px 14px;border-bottom:1px solid #f0f0f0;font-family:Siemreap;font-size:9.5pt}
.sect-item:last-child{border-bottom:none}
.sect-item .snum{color:#1155cc;font-weight:bold;margin-right:6px}
.sect-item .sitems{color:#888;font-size:8.5pt}
.sect-item .stot{float:right;color:#e65100;font-weight:bold}
.period-wrap{margin-bottom:18px}
.period-wrap h3{font-family:Siemreap;font-size:10.5pt;color:#333;margin-bottom:10px}
.yr-row{display:flex;align-items:center;gap:8px;margin-bottom:10px}
.yr-row label{font-family:Siemreap;font-size:9pt;color:#555}
.q-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.q-card{border:2px solid #e0e0e0;border-radius:9px;padding:10px 12px;cursor:pointer;transition:.2s;text-align:center;font-family:Siemreap}
.q-card:hover{border-color:#5b95f9;background:#e8f0fe}
.q-card.active{border-color:#1155cc;background:#1155cc;color:#fff}
.q-card .qlbl{font-size:12pt;font-weight:bold;display:block}
.q-card .qmonth{font-size:8.5pt;opacity:.8;display:block;margin-top:2px}
.col-badge{background:#e3f2fd;border:1px solid #90caf9;border-radius:6px;padding:6px 12px;font-family:monospace;font-size:10pt;color:#0d47a1;text-align:center;margin-top:10px;display:none}
.warn{background:#fff8e1;border:1px solid #ffe082;border-radius:7px;padding:10px 13px;font-family:Siemreap;font-size:9pt;color:#f57f17;line-height:1.7;margin-bottom:14px}
.divider{border:none;border-top:1px solid #eee;margin:18px 0}

/* PRINT */
@media print{
  body{background:#fff;padding:4px}
  .no-print{display:none!important}
  .g-h2,.g-r3,.app-bar,.toolbar,.main-tab-bar,.period-bar{display:none!important}
  table{min-width:unset}
  .print-header{display:block!important}
  td{font-size:9.5pt;padding:1px 3px}
}
.print-header{display:none;text-align:center;margin-bottom:10px}
.print-header h2{font-family:Siemreap;font-size:14pt}
.print-header p{font-family:Siemreap;font-size:10pt}
</style>
<!-- ══════════ AUTH SCREEN ══════════ -->
<div id="auth-screen">
  <div class="auth-box">
    <div class="auth-logo">📋</div>
    <div class="auth-title">ប្រព័ន្ធទូទាត់ថវិកា</div>
    <div class="auth-tabs">
      <div class="auth-tab active" onclick="switchAuthTab('login')">🔑 ចូលប្រើ</div>
      <div class="auth-tab" onclick="switchAuthTab('register')">📝 ចុះឈ្មោះ</div>
    </div>
    <div class="auth-form active" id="tab-login">
      <div class="frow"><label>អ៊ីមែល</label><input id="l-email" type="email" placeholder="user@example.com" onkeydown="if(event.key==='Enter')doLogin()"></div>
      <div class="frow"><label>លេខសម្ងាត់</label><input id="l-pass" type="password" placeholder="••••••••" onkeydown="if(event.key==='Enter')doLogin()"></div>
      <button class="abtn" id="login-btn" onclick="doLogin()">ចូលប្រើ</button>
      <div class="auth-err" id="l-err"></div>
    </div>
    <div class="auth-form" id="tab-register">
      <div class="auth-info">⚠️ ត្រូវការ Admin បើក Email/Password ក្នុង Firebase Console → Authentication → Sign-in method</div>
      <div class="frow"><label>ឈ្មោះ</label><input id="r-name" type="text" placeholder="ឈ្មោះអ្នកប្រើ"></div>
      <div class="frow"><label>អ៊ីមែល</label><input id="r-email" type="email" placeholder="user@example.com"></div>
      <div class="frow"><label>លេខសម្ងាត់ (យ៉ាងតិច ៦ ខ្ទង់)</label><input id="r-pass" type="password" placeholder="••••••••"></div>
      <div class="frow"><label>បញ្ជាក់លេខសម្ងាត់</label><input id="r-pass2" type="password" placeholder="••••••••" onkeydown="if(event.key==='Enter')doRegister()"></div>
      <button class="abtn" id="reg-btn" onclick="doRegister()">ចុះឈ្មោះ</button>
      <div class="auth-err" id="r-err"></div>
    </div>
  </div>
</div>

<!-- ══════════ MAIN APP ══════════ -->
<div id="main-app">

  <!-- TAB BAR -->
  <div class="main-tab-bar no-print">
    <div class="main-tab active" id="mtab-report" onclick="switchMainTab('report')">📋 របាយការណ៍</div>
    <div class="main-tab" id="mtab-setup" onclick="switchMainTab('setup')">⚙️ Setup Tool</div>
    <div style="display:flex;align-items:center;padding:0 8px;gap:6px;margin-left:auto">
      <span class="rt-badge" id="rt-badge" style="font-size:7.5pt">● real-time</span>
      <span style="background:rgba(255,255,255,.15);padding:3px 9px;border-radius:12px;font-size:8.5pt;color:#fff;font-family:Siemreap" id="user-badge-top">👤 —</span>
      <button style="background:rgba(255,255,255,.15);border:1px solid rgba(255,255,255,.4);color:#fff;padding:3px 10px;border-radius:5px;cursor:pointer;font-family:Siemreap;font-size:8.5pt" onclick="doLogout()">🚪 ចេញ</button>
    </div>
  </div>

  <!-- ── PANEL 1: REPORT ── -->
  <div class="tab-panel active" id="panel-report">
    <div class="print-header">
      <div style="text-align:center;font-weight:bold">ព្រះរាជាណាចក្រកម្ពុជា</div>
      <div style="text-align:center;font-weight:bold">ជាតិ សាសនា ព្រះមហាក្សត្រ</div>
      <div style="text-align:left">រដ្ឋបាលស្រុកភ្នំស្រុក</div>
      <div style="text-align:left">ការិយាល័យអប់រំ យុវជន និងកីឡាស្រុក</div>
      <div style="text-align:left">សាលាបឋមសិក្សា រោគ</div>
      <h2>របាយការណ៍ទូទាត់ថវិកា ម.ដ.ស.ប្រចាំ<p id="print-period"></p></h2>
    </div>
    <div class="period-bar no-print">
      <span class="plbl">📅 ជ្រើស:</span>
      <select class="yr-sel" id="yr-sel" onchange="onPeriodChange()"></select>
      <div class="q-tabs">
        <div class="q-tab" data-q="Q1" onclick="selectQ('Q1')">ត្រីមាសទី1<span class="qmonths">មករា–មីនា</span></div>
        <div class="q-tab" data-q="Q2" onclick="selectQ('Q2')">ត្រីមាសទី2<span class="qmonths">មេសា–មិថុនា</span></div>
        <div class="q-tab" data-q="Q3" onclick="selectQ('Q3')">ត្រីមាសទី3<span class="qmonths">កក្កដា–កញ្ញា</span></div>
        <div class="q-tab" data-q="Q4" onclick="selectQ('Q4')">ត្រីមាសទី4<span class="qmonths">តុលា–ធ្នូ</span></div>
      </div>
      <span class="period-badge" id="period-badge">— ជ្រើស Period —</span>
    </div>
    <div class="toolbar no-print">
      <button class="tbtn tb-blue" onclick="addSection()">+ បង្កើត</button>
      <button class="tbtn tb-green" onclick="doPrint()">🖨️ ព្រីន</button>
      <button class="tbtn tb-orange" onclick="exportXLSX()">📥 XLSX</button>
      <span><span class="sync-dot" id="sync-dot"></span><span class="sync-lbl" id="sync-lbl">រង់ចាំ...</span></span>
    </div>
    <div class="tbl-wrap">
      <table id="tbl">
        <colgroup>
          <col style="width:34px"><col style="width:66px"><col style="width:110px">
          <col style="width:66px"><col style="width:215px"><col style="width:56px">
          <col style="width:56px"><col style="width:92px"><col style="width:108px">
          <col style="width:78px"><col style="width:68px">
        </colgroup>
        <tbody id="tbody">
          <tr class="th-main">
            <td>ល.រ</td><td>លេខបណ្ណ</td><td>កាលបរិច្ឆេទ</td><td>អនុគណនី</td>
            <td>កម្មវត្ថុចំណាយ</td><td>ឯកតា</td><td>បរិមាណ</td>
            <td>តម្លៃឯកតា(រៀល)</td><td>ទឹកប្រាក់សរុប(រៀល)</td>
            <td>ផ្សេងៗ</td><td class="no-print">សកម្មភាព</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>

  <!-- ── PANEL 2: SETUP ── -->
  <div class="tab-panel" id="panel-setup">
    <div class="setup-wrap">
      <div class="card">
        <div class="logo">⚙️</div>
        <h1>Setup Tool</h1>
        <p class="sub">ផ្ទុក Data ទៅ Firestore · project: create-adf92</p>
        <div class="period-wrap">
          <h3>📅 ជ្រើស Period សម្រាប់ Import</h3>
          <div class="yr-row">
            <label>ឆ្នាំ:</label>
            <select class="yr-sel" id="s-yr-sel" onchange="sOnYearChange()"></select>
          </div>
          <div class="q-grid">
            <div class="q-card" id="sqc-Q1" onclick="sSelectQ('Q1')">
              <span class="qlbl">Q1</span><span class="qmonth">មករា – មីនា</span>
            </div>
            <div class="q-card" id="sqc-Q2" onclick="sSelectQ('Q2')">
              <span class="qlbl">Q2</span><span class="qmonth">មេសា – មិថុនា</span>
            </div>
            <div class="q-card" id="sqc-Q3" onclick="sSelectQ('Q3')">
              <span class="qlbl">Q3</span><span class="qmonth">កក្កដា – កញ្ញា</span>
            </div>
            <div class="q-card" id="sqc-Q4" onclick="sSelectQ('Q4')">
              <span class="qlbl">Q4</span><span class="qmonth">តុលា – ធ្នូ</span>
            </div>
          </div>
          <div class="col-badge" id="s-col-badge">📦 Collection: —</div>
        </div>
        <div class="warn">
          ⚠️ Tool នេះនឹង <strong>លុបទិន្នន័យចាស់ក្នុង Period ដែលជ្រើស</strong> ហើយ import ទិន្នន័យថ្មី។<br>
          Period ផ្សេងៗ <strong>មិនប៉ះពាល់</strong>! សូម backup មុន import!
        </div>
        <div class="preview" id="s-preview-box">
          <h3>📋 ទិន្នន័យដែលនឹង Import (៧ ក្រុម)</h3>
          <div class="sect-list" id="s-sect-list"></div>
        </div>
        <div style="margin-top:14px;display:flex;gap:8px;flex-wrap:wrap">
          <button class="btn btn-green" id="import-btn" onclick="doImport()" style="flex:1" disabled="">📥 Import ទៅ Firestore</button>
          <button class="btn btn-red" id="clear-btn" onclick="doClear()" style="flex:1" disabled="">🗑️ លុបទិន្នន័យទាំងអស់</button>
        </div>
        <div class="prog-wrap" id="s-prog-wrap">
          <div class="prog-bar-bg"><div class="prog-bar" id="s-prog-bar"></div></div>
          <div class="prog-lbl" id="s-prog-lbl">0 / 0</div>
        </div>
        <div class="s-status" id="s-status-box"></div>
      </div>
    </div>
  </div>

</div><!-- /main-app -->

<script>
// ══════════════════════════════════
//  FIREBASE INIT
// ══════════════════════════════════
var FB_CFG = {
  apiKey: "AIzaSyDwYGbelzf1vVOaMmTPm63yDtsjTOGIxnU",
  authDomain: "create-adf92.firebaseapp.com",
  projectId: "create-adf92",
  storageBucket: "create-adf92.firebasestorage.app",
  messagingSenderId: "529723873139",
  appId: "1:529723873139:web:3cf7388700eebd8d9a1706"
};
window.addEventListener('load', function() {
  try {
    firebase.initializeApp(FB_CFG);
    window.auth = firebase.auth();
    window.db   = firebase.firestore();
    initAuth();
  } catch(e) {
    document.getElementById('l-err').textContent = '❌ Firebase មានបញ្ហា: ' + e.message;
  }
});

// ══════════════════════════════════
//  TAB SWITCHER
// ══════════════════════════════════
function switchMainTab(tab) {
  ['report','setup'].forEach(function(t) {
    document.getElementById('mtab-'+t).classList.toggle('active', t===tab);
    document.getElementById('panel-'+t).classList.toggle('active', t===tab);
  });
  if (tab==='setup') { sBuildYearSel(); sRenderPreview(); }
}

// ══════════════════════════════════
//  AUTH
// ══════════════════════════════════
var currentUser = null;
var rtUnsubscribe = null;
var currentYear = new Date().getFullYear();
var currentQ    = '';

function initAuth() {
  window.auth.onAuthStateChanged(function(user) {
    if (user) {
      currentUser = user;
      document.getElementById('auth-screen').style.display = 'none';
      document.getElementById('main-app').style.display   = 'block';
      document.getElementById('user-badge-top').textContent = '👤 ' + (user.displayName || user.email);
      buildYearSel();
      var m = new Date().getMonth() + 1;
      selectQ(m<=3?'Q1':m<=6?'Q2':m<=9?'Q3':'Q4');
    } else {
      currentUser = null;
      document.getElementById('auth-screen').style.display = 'flex';
      document.getElementById('main-app').style.display   = 'none';
      clearTable();
    }
  });
}
function switchAuthTab(t) {
  var il=(t==='login');
  document.querySelectorAll('.auth-tab').forEach(function(el,i){ el.classList.toggle('active',i===(il?0:1)); });
  document.querySelectorAll('.auth-form').forEach(function(el,i){ el.classList.toggle('active',i===(il?0:1)); });
}
function setAuthLoading(id,on) {
  var b=document.getElementById(id); if(!b) return;
  b.disabled=on; b.textContent=on?'⏳ ...':(id==='login-btn'?'ចូលប្រើ':'ចុះឈ្មោះ');
}
function doLogin() {
  var email=document.getElementById('l-email').value.trim();
  var pass=document.getElementById('l-pass').value;
  var err=document.getElementById('l-err'); err.textContent='';
  if (!email||!pass){err.textContent='⚠️ សូមបញ្ចូលអ៊ីមែល និងលេខសម្ងាត់';return;}
  setAuthLoading('login-btn',true);
  window.auth.signInWithEmailAndPassword(email,pass).catch(function(e){
    err.textContent='❌ '+authErr(e.code); setAuthLoading('login-btn',false);
  });
}
function doRegister() {
  var n=document.getElementById('r-name').value.trim();
  var e=document.getElementById('r-email').value.trim();
  var p=document.getElementById('r-pass').value;
  var p2=document.getElementById('r-pass2').value;
  var err=document.getElementById('r-err'); err.textContent='';
  if(!n||!e||!p){err.textContent='⚠️ សូមបំពេញព័ត៌មានទាំងអស់';return;}
  if(p!==p2){err.textContent='❌ លេខសម្ងាត់មិនដូចគ្នា';return;}
  if(p.length<6){err.textContent='❌ លេខសម្ងាត់ត្រូវការយ៉ាងតិច ៦ ខ្ទង់';return;}
  setAuthLoading('reg-btn',true);
  window.auth.createUserWithEmailAndPassword(e,p)
    .then(function(c){return c.user.updateProfile({displayName:n});})
    .catch(function(e){err.textContent='❌ '+authErr(e.code);setAuthLoading('reg-btn',false);});
}
function doLogout() {
  if(!confirm('ចេញពីប្រព័ន្ធ?')) return;
  if(rtUnsubscribe){rtUnsubscribe();rtUnsubscribe=null;}
  window.auth.signOut();
}
function authErr(c) {
  var M={'auth/user-not-found':'រកមិនឃើញអ្នកប្រើ','auth/wrong-password':'លេខសម្ងាត់មិនត្រឹមត្រូវ',
    'auth/invalid-email':'អ៊ីមែលមិនត្រឹមត្រូវ','auth/email-already-in-use':'អ៊ីមែលនេះបានប្រើហើយ',
    'auth/weak-password':'លេខសម្ងាត់ខ្សោយពេក','auth/too-many-requests':'ព្យាយាមច្រើនដង សូមរង់ចាំ',
    'auth/invalid-credential':'អ៊ីមែល ឬ លេខសម្ងាត់មិនត្រឹមត្រូវ','auth/network-request-failed':'បណ្តាញមានបញ្ហា'};
  return M[c]||c;
}

// ══════════════════════════════════
//  REPORT: PERIOD
// ══════════════════════════════════
function getCollectionName(){return 'payment_'+currentYear+'_'+currentQ;}
function buildYearSel(){
  var sel=document.getElementById('yr-sel'); if(!sel) return;
  sel.innerHTML='';
  var y=new Date().getFullYear();
  for(var i=y-1;i<=y+1;i++){
    var o=document.createElement('option'); o.value=i; o.textContent=i;
    if(i===y) o.selected=true; sel.appendChild(o);
  }
  currentYear=y;
}
function onPeriodChange(){
  currentYear=parseInt(document.getElementById('yr-sel').value);
  if(currentQ) switchPeriod(currentYear,currentQ);
}
function selectQ(q){
  currentQ=q;
  document.querySelectorAll('.q-tab').forEach(function(t){t.classList.toggle('active',t.dataset.q===q);});
  switchPeriod(currentYear,q);
}
function switchPeriod(yr,q){
  var qN={Q1:'មករា–មីនា',Q2:'មេសា–មិថុនា',Q3:'កក្កដា–កញ្ញា',Q4:'តុលា–ធ្នូ'};
  var b=document.getElementById('period-badge');
  if(b) b.textContent=yr+' · '+q+' ('+(qN[q]||'')+')';
  var ph=document.getElementById('print-period');
  if(ph) ph.textContent='ត្រីមាស'+q+' ('+(qN[q]||'')+') ឆ្នាំ '+yr;
  startRealtime();
}

// ══════════════════════════════════
//  REPORT: REALTIME
// ══════════════════════════════════
function setSyncUI(s,msg){
  var dot=document.getElementById('sync-dot'), lbl=document.getElementById('sync-lbl'), rt=document.getElementById('rt-badge');
  if(s==='ok'){dot.className='sync-dot ok';lbl.textContent='Synced ✔';rt.className='rt-badge';}
  else if(s==='busy'){dot.className='sync-dot';lbl.textContent='Saving...';rt.className='rt-badge busy';}
  else{dot.className='sync-dot err';lbl.textContent=msg||'Error!';rt.className='rt-badge busy';}
}
function startRealtime(){
  if(!currentQ) return;
  if(rtUnsubscribe){rtUnsubscribe();rtUnsubscribe=null;}
  clearTable(); setSyncUI('busy');
  rtUnsubscribe=window.db.collection(getCollectionName()).onSnapshot(function(snap){
    var docs=snap.docs.map(function(d){return Object.assign({},d.data(),{_docId:d.id});})
      .sort(function(a,b){return (a.id||0)-(b.id||0);});
    rebuildTable(docs); setSyncUI('ok');
  },function(e){
    setSyncUI('error','Error: '+(e.code||e.message||'unknown'));
    setTimeout(function(){if(currentUser) startRealtime();},5000);
  });
}
function rebuildTable(docs){clearTable();secCnt=0;itemCnt=0;docs.forEach(function(d){buildSection(d);});renderTotal();}

// ✅ FIX: 'sig-r7' បានបន្ថែម
var FOOTER_IDS=['total-row','words-row','stop-row','sig-r1','sig-r2','sig-r3','sig-r4','sig-r5','sig-r6','sig-r7'];
function clearTable(){
  var tbody=document.getElementById('tbody');
  tbody.querySelectorAll('[data-sid]').forEach(function(r){r.remove();});
  FOOTER_IDS.forEach(function(id){var el=document.getElementById(id);if(el) el.remove();});
}

// ══════════════════════════════════
//  KHMER UTILS
// ══════════════════════════════════
function toKN(s){return String(s).replace(/[0-9]/g,function(d){return '០១២៣៤៥៦៧៨៩'[d];});}
function fmt(n){return n?Number(n).toLocaleString():'';}
function getLunar(date){
  var a=Math.floor((14-date.getMonth()-1)/12),y=date.getFullYear()+4800-a,m=(date.getMonth()+1)+12*a-3;
  var jd=date.getDate()+Math.floor((153*m+2)/5)+365*y+Math.floor(y/4)-Math.floor(y/100)+Math.floor(y/400)-32045;
  var lm=['មិគសិរ','បុស្ស','មាឃ','ផល្គុន','ចេត្រ','ពិសាខ','ជេស្ឥ','អាសាឍ','ស្រាពណ៍','ភទ្របទ','អស្សុជ','កក្ដិក'];
  var dse=jd-2451550.1,ld=Math.floor(dse%29.530588853)+1,mi=Math.floor(dse/29.530588853)%12;
  return{month:lm[(mi+12)%12],day:Math.min(ld<=15?ld:ld-15,15),phase:ld<=15?'កើត':'រោច'};
}
function khmerDateFull(date){
  var kd=['អាទិត្យ','ច័ន្ទ','អង្គារ','ពុធ','ព្រហស្បតិ៍','សុក្រ','សៅរ៍'];
  var ay=['ជូត','ឆ្លូវ','ខាល','ថោះ','រោង','ម្សាញ់','មមី','ម្ត','វក','រកា','ច','កុរ'];
  var ec=['ឯកស័ក','ទោស័ក','ត្រីស័ក','ចត្វាស័ក','បញ្ចស័ក','ឆស័ក','សប្តស័ក','អដ្ឋស័ក','នព្វស័ក','សំរឹទ្ធិស័ក'];
  var l=getLunar(date);
  return 'ថ្ងៃ'+kd[date.getDay()]+' '+toKN(l.day)+l.phase+' ខែ'+l.month+' ឆ្នាំ'+ay[(date.getFullYear()+4)%12]+' '+ec[(date.getFullYear()+5)%10]+' ព.ស '+toKN(date.getFullYear()+544);
}
function addWorkdays(date,days){
  var d=new Date(date),added=0;
  while(added<days){d.setDate(d.getDate()+1);var dow=d.getDay();if(dow!==0&&dow!==6)added++;}
  return d;
}
function westernDate(date){
  var km=['មករា','កុម្ភៈ','មីនា','មេសា','ឧសភា','មិថុនា','កក្កដា','សីហា','កញ្ញា','តុលា','វិច្ឆិកា','ធ្នូ'];
  return 'ថ្ងៃទី'+toKN(date.getDate())+' ខែ'+km[date.getMonth()]+' ឆ្នាំ'+toKN(date.getFullYear());
}
function solarKhDate(iso){if(!iso) return '';var d=new Date(iso+'T00:00:00');return isNaN(d)?iso:westernDate(d);}
function khmerDate(iso){return solarKhDate(iso);}
function numToWord(n){
  n=Math.round(n); if(!n) return 'សូន្យរៀលគត់';
  var O=['','មួយ','ពីរ','បី','បួន','ប្រាំ','ប្រាំមួយ','ប្រាំពីរ','ប្រាំបី','ប្រាំបួន'];
  var T=['','ដប់','ម្ភៃ','សាមសិប','សែសិប','ហាសិប','ហុកសិប','ចិតសិប','ប៉ែតសិប','កៅសិប'];
  function cs(x){
    if(x===0) return '';
    var h=Math.floor(x/100),r=x%100,t=Math.floor(r/10),o=r%10;
    return (h>0?O[h]+'រយ':'')+(t>0?T[t]:'')+(o>0?O[o]:'');
  }
  var billions=Math.floor(n/1e9),millions=Math.floor((n%1e9)/1e6),thousands=Math.floor((n%1e6)/1e3),rem=n%1e3;
  var res='';
  if(billions>0) res+=cs(billions)+'លាន';
  if(millions>0) res+=cs(millions)+'លាន';
  if(thousands>0) res+=cs(thousands)+'ពាន់';
  if(rem>0) res+=cs(rem);
  return res+'រៀលគត់';
}

// ══════════════════════════════════
//  REPORT: TABLE BUILD
// ══════════════════════════════════
var CATS=['កិច្ចដំណើរការរដ្ឋបាល','ការថែទាំ និងជួសជុលផ្សេងៗ',
  'ការចូលរៀនដោយ​សមធម៌ និងបង្ការសិស្សបោះបង់','សម្ភារៈបង្រៀន និងរៀន',
  'សម្ភារៈរៀន និងបង្រៀន','ការកែលម្អបរិស្ថាន',
  'ការអប់រំបំណិនជីវិត កីឡា ការងារយុវជន និងកុមារ',
  'អប់រំបំណិនជីវិត កីឡា ការងារយុវជន និងកុមារ'];
var ACCS=['60028','60058','61058','61108','62025','62028'];
var secCnt=0,itemCnt=0;
function catOpts(sel){return '<option value="">‹ជ្រើស›</option>'+CATS.map(function(c){return '<option'+(c===sel?' selected':'')+'>'+c+'</option>';}).join('');}
function accOpts(sel){return '<option value="">‹ជ្រើស›</option>'+ACCS.map(function(a){return '<option'+(a===sel?' selected':'')+'>'+a+'</option>';}).join('');}

function buildSection(d){
  secCnt++;
  var sid='s'+secCnt;
  var tbody=document.getElementById('tbody');
  var h1=document.createElement('tr');
  h1.className='g-h1';h1.dataset.sid=sid;h1.dataset.docid=d._docId||'';
  h1.innerHTML=
    '<td class="tc">'+d.id+'</td>'+
    '<td><input data-f="bon" type="text" value="'+(d.bon||'')+'" onchange="schedSave(\''+sid+'\')"></td>'+
    '<td><input data-f="date" type="date" value="'+(d.date||'')+'" onchange="onDateChange(\''+sid+'\',this.value);schedSave(\''+sid+'\')"</td>'+
    '<td><select data-f="acc" onchange="schedSave(\''+sid+'\')">'+accOpts(d.acc)+'</select></td>'+
    '<td><select data-f="cat" id="cat-'+sid+'" onchange="onCatChange(\''+sid+'\');schedSave(\''+sid+'\')">'+catOpts(d.cat)+'</select></td>'+
    '<td></td><td></td><td></td>'+
    '<td class="tr" id="gtot-'+sid+'">'+fmt(d.total)+'</td>'+
    '<td><input data-f="note" type="text" value="'+(d.note||'')+'" onchange="schedSave(\''+sid+'\')"></td>'+
    '<td class="no-print tc"><button class="hbtn" style="color:#c62828" onclick="delSection(\''+sid+'\')">✖</button></td>';
  tbody.appendChild(h1);
  var h2=document.createElement('tr');
  h2.className='g-h2 no-print';h2.dataset.sid=sid;
  h2.innerHTML='<td colspan="11">'+
    '<button class="hbtn" style="color:#2e7d32" onclick="toggleItems(\''+sid+'\',true)">➕ បង្ហាញ</button>'+
    '<button class="hbtn" style="color:#e65100" onclick="toggleItems(\''+sid+'\',false)">➖ លាក់</button>'+
    '<button class="hbtn" style="color:#c62828" onclick="delSection(\''+sid+'\')">✖️ លុបក្រុម</button></td>';
  tbody.appendChild(h2);
  (d.items||[]).forEach(function(it,i){addItemRow(sid,it,i+1,false);});
  var r3=document.createElement('tr');
  r3.className='g-r3 no-print';r3.id='r3-'+sid;r3.dataset.sid=sid;
  r3.innerHTML=
    '<td colspan="4" class="emp"></td>'+
    '<td colspan="4"><div class="r3w">'+
      '<input class="fl" id="r3n-'+sid+'" placeholder="ឈ្មោះទំនិញ / សេវា">'+
      '<input class="fs" id="r3u-'+sid+'" placeholder="ឯកតា">'+
      '<input class="fs" type="number" id="r3q-'+sid+'" placeholder="បរិមាណ" oninput="r3Calc(\''+sid+'\')">'+
      '<input class="fm" type="number" id="r3p-'+sid+'" placeholder="តម្លៃ/ឯកតា" oninput="r3Calc(\''+sid+'\')">'+
      '<input class="fm" id="r3s-'+sid+'" placeholder="សរុប" readonly style="background:#eef;text-align:right">'+
    '</div></td>'+
    '<td colspan="3"><div class="cbtns">'+
      '<button class="cbtn cb-add" onclick="crudAdd(\''+sid+'\')">➕ Add</button>'+
      '<button class="cbtn cb-edit" onclick="crudEdit(\''+sid+'\')">✏️ Edit</button>'+
      '<button class="cbtn cb-del" onclick="crudDel(\''+sid+'\')">🗑️ Del</button>'+
      '<button class="cbtn cb-save" onclick="crudSave(\''+sid+'\')">💾 Save</button>'+
    '</div></td>';
  tbody.appendChild(r3);
  if(d.cat) r3.style.display='table-row';
}
function addItemRow(sid,it,seq,doRecalc){
  if(doRecalc===undefined) doRecalc=true;
  itemCnt++;
  var iid='i'+itemCnt;
  var anchor=document.getElementById('r3-'+sid);
  var dr=document.createElement('tr');
  dr.className='d-row';dr.dataset.sid=sid;dr.dataset.iid=iid;
  dr.innerHTML=
    '<td class="emp tc" style="color:#bbb;font-size:8.5pt">'+seq+'</td>'+
    '<td class="emp"></td><td class="emp"></td><td class="emp"></td>'+
    '<td style="padding-left:12px"><input data-f="name" type="text" value="'+(it.name||'')+'" oninput="schedSave(\''+sid+'\')"></td>'+
    '<td class="tc"><input data-f="unit" type="text" value="'+(it.unit||'')+'" style="text-align:center" oninput="schedSave(\''+sid+'\')"></td>'+
    '<td class="tr"><input data-f="qty" type="number" value="'+(it.qty||'')+'" style="width:100%;text-align:right" oninput="recalc(\''+sid+'\')"></td>'+
    '<td class="tr"><input data-f="price" type="number" value="'+(it.price||'')+'" style="width:100%;text-align:right" oninput="recalc(\''+sid+'\')"></td>'+
    '<td class="tr" id="sub-'+iid+'">'+fmt((it.qty||0)*(it.price||0))+'</td>'+
    '<td><input data-f="note" type="text" value="'+(it.note||'')+'" oninput="schedSave(\''+sid+'\')"></td>'+
    '<td class="no-print tc"><button class="hbtn" style="color:#c62828;font-size:8px" onclick="delItemRow(this,\''+sid+'\')">✖</button></td>';
  if(anchor) anchor.before(dr); else document.getElementById('tbody').appendChild(dr);
  if(doRecalc) recalc(sid);
}
function onCatChange(sid){
  var el=document.getElementById('cat-'+sid),v=el?el.value:'';
  var r3=document.getElementById('r3-'+sid);
  if(r3) r3.style.display=v?'table-row':'none';
}
function onDateChange(sid,val){}
function toggleItems(sid,show){
  document.querySelectorAll('.d-row[data-sid="'+sid+'"]').forEach(function(r){r.style.display=show?'':'none';});
}
function delSection(sid){
  if(!confirm('លុបក្រុមទាំងអស់?')) return;
  var h1=document.querySelector('.g-h1[data-sid="'+sid+'"]'),docId=h1?h1.dataset.docid:'';
  document.querySelectorAll('[data-sid="'+sid+'"]').forEach(function(r){r.remove();});
  renderTotal();
  if(docId) window.db.collection(getCollectionName()).doc(docId).delete().catch(console.error);
}
function delItemRow(btn,sid){btn.closest('tr').remove();recalc(sid);}
function recalc(sid){
  var sum=0;
  document.querySelectorAll('.d-row[data-sid="'+sid+'"]').forEach(function(r){
    var q=parseFloat((r.querySelector('[data-f=qty]')||{}).value)||0;
    var p=parseFloat((r.querySelector('[data-f=price]')||{}).value)||0;
    var s=q*p;
    var sc=document.getElementById('sub-'+r.dataset.iid);
    if(sc) sc.textContent=s?fmt(s):'';
    sum+=s;
  });
  var gt=document.getElementById('gtot-'+sid);
  if(gt) gt.textContent=sum?fmt(sum):'';
  renderTotal(); schedSave(sid);
}

// ══════════════════════════════════
//  REPORT: RENDER TOTAL + FOOTER
// ══════════════════════════════════
function renderTotal(){
  FOOTER_IDS.forEach(function(id){var el=document.getElementById(id);if(el) el.remove();});
  var grand=0;
  document.querySelectorAll('.g-h1').forEach(function(r){
    var g=r.querySelector('[id^="gtot-"]');
    grand+=parseFloat(g?(g.textContent||'').replace(/,/g,''):0)||0;
  });
  var lastSeq=0;
  document.querySelectorAll('.g-h1').forEach(function(r){
    var n=parseInt(r.querySelector('td:first-child').textContent)||0;
    if(n>lastSeq) lastSeq=n;
  });
  var today=new Date();
  var dateAnuPdth=addWorkdays(today,1),datePdth=addWorkdays(today,2);
  var tbody=document.getElementById('tbody');
  var BS='border:none;font-family:Siemreap;font-size:10pt;background:#fff;white-space:nowrap;';
  function mkRow(id,html){var r=document.createElement('tr');r.id=id;r.innerHTML=html;tbody.appendChild(r);return r;}

  mkRow('total-row',
    '<td colspan="8" style="background:#fce8b2;font-weight:bold;border-top:2px solid #000;text-align:right;padding-right:10px;font-size:11pt;font-family:Siemreap">សរុបទឹកប្រាក់</td>'+
    '<td style="background:#fce8b2;font-weight:bold;border-top:2px solid #000;text-align:right;padding-right:6px;font-size:11pt;font-family:Siemreap">'+fmt(grand)+'</td>'+
    '<td colspan="2" style="background:#fce8b2;border-top:2px solid #000"></td>'
  );
  mkRow('stop-row',
    '<td colspan="11" style="'+BS+'padding:6px 10px;border-top:2px solid #000">'+
    'បានបញ្ឈប់បញ្ជីត្រឹមលេខរៀងទី <strong>'+toKN(lastSeq)+'</strong>'+
    '   ចំនួនទឹកប្រាក់សរុប <strong>'+toKN(Number(grand).toLocaleString('en-US'))+'</strong> រៀល'+
    '   ជាអក្សរ : <strong>'+numToWord(grand)+'</strong></td>'
  );
  mkRow('sig-r2',
    '<td colspan="3" style="'+BS+'text-align:center">បានឃើញ និងឯកភាព</td>'+
    '<td colspan="3" style="'+BS+'text-align:center">បានឃើញ និងពិនិត្យត្រឹមត្រូវ</td>'+
    '<td colspan="3" style="'+BS+'text-align:left">'+khmerDateFull(today)+'</td>'+
    '<td colspan="2" style="'+BS+'"></td>'
  );
  mkRow('sig-r3',
    '<td colspan="3" style="'+BS+'text-align:left">'+khmerDateFull(datePdth)+'</td>'+
    '<td colspan="3" style="'+BS+'text-align:left">'+khmerDateFull(dateAnuPdth)+'</td>'+
    '<td colspan="3" style="'+BS+'text-align:left">រោគ '+westernDate(today)+'</td>'+
    '<td colspan="2" style="'+BS+'"></td>'
  );
  mkRow('sig-r4',
    '<td colspan="3" style="'+BS+'text-align:left">រោគ '+westernDate(datePdth)+'</td>'+
    '<td colspan="3" style="'+BS+'text-align:left">រោគ '+westernDate(dateAnuPdth)+'</td>'+
    '<td colspan="3" style="'+BS+'text-align:center;font-weight:bold">ហេរញ្ញិក</td>'+
    '<td colspan="2" style="'+BS+'"></td>'
  );
  mkRow('sig-r5',
    '<td colspan="3" style="'+BS+'text-align:center;font-weight:bold">ប្រធានគ.ម.ស.</td>'+
    '<td colspan="3" style="'+BS+'text-align:center;font-weight:bold">អនុប្រធានគ.ម.ស.</td>'+
    '<td colspan="3" style="'+BS+'"></td>'+
    '<td colspan="2" style="'+BS+'"></td>'
  );
  mkRow('sig-r6','<td colspan="11" style="'+BS+'height:55px"></td>');
  mkRow('sig-r7',
    '<td colspan="3" style="'+BS+'text-align:center">ឈ្មោះ…………….</td>'+
    '<td colspan="3" style="'+BS+'text-align:center">ឈ្មោះ…………….</td>'+
    '<td colspan="3" style="'+BS+'text-align:center"></td>'+
    '<td colspan="2" style="'+BS+'"></td>'
  );
}

function r3Calc(sid){
  var q=parseFloat((document.getElementById('r3q-'+sid)||{}).value)||0;
  var p=parseFloat((document.getElementById('r3p-'+sid)||{}).value)||0;
  var s=document.getElementById('r3s-'+sid);
  if(s) s.value=q&&p?fmt(q*p):'';
}
function crudAdd(sid){
  var nEl=document.getElementById('r3n-'+sid),n=nEl?nEl.value.trim():'';
  if(!n){alert('សូមបញ្ចូលឈ្មោះ');return;}
  var u=document.getElementById('r3u-'+sid),q=document.getElementById('r3q-'+sid),p=document.getElementById('r3p-'+sid);
  var cnt=document.querySelectorAll('.d-row[data-sid="'+sid+'"]').length+1;
  addItemRow(sid,{name:n,unit:u?u.value:'',qty:parseFloat(q?q.value:0)||0,price:parseFloat(p?p.value:0)||0},cnt,true);
  ['r3n-','r3u-','r3q-','r3p-','r3s-'].forEach(function(x){var e=document.getElementById(x+sid);if(e) e.value='';});
}
function crudEdit(sid){
  var rows=Array.from(document.querySelectorAll('.d-row[data-sid="'+sid+'"]'));
  if(!rows.length) return;
  var last=rows[rows.length-1];
  var nEl=document.getElementById('r3n-'+sid),uEl=document.getElementById('r3u-'+sid);
  var qEl=document.getElementById('r3q-'+sid),pEl=document.getElementById('r3p-'+sid);
  if(nEl) nEl.value=(last.querySelector('[data-f=name]')||{}).value||'';
  if(uEl) uEl.value=(last.querySelector('[data-f=unit]')||{}).value||'';
  if(qEl) qEl.value=(last.querySelector('[data-f=qty]')||{}).value||'';
  if(pEl) pEl.value=(last.querySelector('[data-f=price]')||{}).value||'';
  r3Calc(sid); last.style.background='#fff9c4'; setTimeout(function(){last.style.background='';},1200);
}
function crudDel(sid){
  var rows=Array.from(document.querySelectorAll('.d-row[data-sid="'+sid+'"]'));
  if(!rows.length){alert('គ្មានជួរ');return;}
  if(confirm('លុបជួរចុងក្រោយ?')){rows[rows.length-1].remove();recalc(sid);}
}
function crudSave(sid){saveToDB(sid);}
function addSection(){
  var newId=document.querySelectorAll('.g-h1').length+1;
  window.db.collection(getCollectionName()).add({
    id:newId,bon:'',date:'',acc:'',cat:'',total:0,note:'',items:[],
    _editBy:currentUser?(currentUser.displayName||currentUser.email||''):'',
    _editAt:new Date().toLocaleString()
  }).then(function(){setSyncUI('ok');}).catch(function(e){console.error(e);setSyncUI('error');});
}

// ══════════════════════════════════
//  REPORT: SAVE
// ══════════════════════════════════
function collectSection(sid){
  var h1=document.querySelector('.g-h1[data-sid="'+sid+'"]'); if(!h1) return null;
  var items=[];
  document.querySelectorAll('.d-row[data-sid="'+sid+'"]').forEach(function(r){
    var q=parseFloat((r.querySelector('[data-f=qty]')||{}).value)||0;
    var p=parseFloat((r.querySelector('[data-f=price]')||{}).value)||0;
    items.push({name:(r.querySelector('[data-f=name]')||{}).value||'',unit:(r.querySelector('[data-f=unit]')||{}).value||'',qty:q,price:p,sub:q*p,note:(r.querySelector('[data-f=note]')||{}).value||''});
  });
  function gsel(f){var el=h1.querySelector('[data-f='+f+']');return el?(el.value||''):'';}
  var gtEl=document.getElementById('gtot-'+sid);
  return{id:parseInt(h1.querySelector('td:first-child').textContent)||0,bon:gsel('bon'),date:gsel('date'),acc:gsel('acc'),cat:gsel('cat'),total:parseFloat(gtEl?(gtEl.textContent||'').replace(/,/g,''):0)||0,note:gsel('note'),items:items,_editBy:currentUser?(currentUser.displayName||currentUser.email||''):'',_editAt:new Date().toLocaleTimeString()};
}
var _tmr={};
function schedSave(sid){clearTimeout(_tmr[sid]);_tmr[sid]=setTimeout(function(){saveToDB(sid);},1000);}
function saveToDB(sid){
  if(!currentUser||!window.db) return;
  var data=collectSection(sid);if(!data) return;
  var h1=document.querySelector('.g-h1[data-sid="'+sid+'"]');
  var docId=h1?h1.dataset.docid||'':'';
  setSyncUI('busy');
  var p=docId?window.db.collection(getCollectionName()).doc(docId).set(data):window.db.collection(getCollectionName()).add(data).then(function(ref){if(h1)h1.dataset.docid=ref.id;});
  p.then(function(){setSyncUI('ok');}).catch(function(e){console.error(e);setSyncUI('error');});
}

// ══════════════════════════════════
//  PRINT & XLSX
// ══════════════════════════════════
function doPrint(){window.print();}
function exportXLSX(){
  if(typeof XLSX==='undefined'){alert('SheetJS not loaded');return;}
  var wb=XLSX.utils.book_new();
  var qN={Q1:'មករា–មីនា',Q2:'មេសា–មិថុនា',Q3:'កក្កដា–កញ្ញា',Q4:'តុលា–ធ្នូ'};
  var rows=[['របាយការណ៍ទូទាត់ថវិកា — ត្រីមាស '+currentQ+' ('+(qN[currentQ]||'')+') ឆ្នាំ '+currentYear,'','','','','','','','',''],Array(10).fill(''),['ល.រ','លេខបណ្ណ','កាលបរិច្ឆេទ','អនុគណនី','កម្មវត្ថុចំណាយ','ឯកតា','បរិមាណ','តម្លៃឯកតា(រៀល)','ទឹកប្រាក់សរុប(រៀល)','ផ្សេងៗ']];
  var grand=0,lastSeq=0;
  document.querySelectorAll('.g-h1').forEach(function(h1){
    var sid=h1.dataset.sid;
    function gv(f){var el=h1.querySelector('[data-f='+f+']');return el?(el.value||''):'';}
    var gtEl=document.getElementById('gtot-'+sid);
    var tot=parseFloat(gtEl?(gtEl.textContent||'').replace(/,/g,''):0)||0;
    grand+=tot;
    var seq=parseInt(h1.querySelector('td:first-child').textContent)||0;
    if(seq>lastSeq) lastSeq=seq;
    rows.push([seq,gv('bon'),khmerDate(gv('date')),gv('acc'),gv('cat'),'','','',tot,gv('note')]);
    document.querySelectorAll('.d-row[data-sid="'+sid+'"]').forEach(function(r){
      var q=parseFloat((r.querySelector('[data-f=qty]')||{}).value)||0;
      var p=parseFloat((r.querySelector('[data-f=price]')||{}).value)||0;
      rows.push(['','','','',(r.querySelector('[data-f=name]')||{}).value||'',(r.querySelector('[data-f=unit]')||{}).value||'',q||'',p||'',q*p||'',(r.querySelector('[data-f=note]')||{}).value||'']);
    });
  });
  rows.push(Array(10).fill(''),['','','','','','','','','សរុបទឹកប្រាក់',fmt(grand)]);
  rows.push(['ជាអក្សរ : '+numToWord(grand),'','','','','','','','','']);
  var today=new Date();
  rows.push(Array(10).fill(''));
  rows.push(['បានឃើញ និងឯកភាព','','','បានឃើញ និងពិនិត្យត្រឹមត្រូវ','','','',khmerDateFull(today),'','']);
  rows.push(['ប្រធានគ.ម.ស.','','','អនុប្រធានគ.ម.ស.','','','','ហេរញ្ញិក','','']);
  rows.push(Array(10).fill(''),Array(10).fill(''));
  var ws=XLSX.utils.aoa_to_sheet(rows);
  ws['!cols']=[4,9,22,10,32,8,8,15,17,12].map(function(w){return{wch:w};});
  XLSX.utils.book_append_sheet(wb,ws,'របាយការណ៍');
  XLSX.writeFile(wb,'payment_'+currentYear+'_'+currentQ+'_'+new Date().toISOString().slice(0,10)+'.xlsx');
}

// ══════════════════════════════════
//  SETUP TOOL
// ══════════════════════════════════
var sYear=new Date().getFullYear(), sQ='';
function sGetCol(){return sQ?'payment_'+sYear+'_'+sQ:'';}
var SECTIONS=[
  {id:1,bon:'001',date:'2026-02-16',acc:'60028',cat:'កិច្ចដំណើរការរដ្ឋបាល',note:'',total:601000,items:[{name:'កាវបិទថ្លា ៥០០មល',unit:'ដប',qty:12,price:5000,sub:60000},{name:'ក្រដាសរ៉ាម Doubble A',unit:'កេស',qty:4,price:60000,sub:240000},{name:'តារាងរដ្ឋបាលថ្នាក់រៀន',unit:'ឈុត',qty:12,price:7500,sub:90000},{name:'បញ្ជីស្រង់ពិន្ទុសិស្ស',unit:'ក្បាល',qty:12,price:5500,sub:66000},{name:'បញ្ជីហៅឈ្មោះសិស្ស',unit:'ក្បាល',qty:12,price:5500,sub:66000},{name:'សៀវភៅតាមដាន',unit:'ដុំ',qty:1,price:49000,sub:49000},{name:'ស្គុតថ្លា',unit:'ដុំ',qty:6,price:5000,sub:30000}]},
  {id:2,bon:'002',date:'2026-02-18',acc:'60058',cat:'សម្ភារៈរៀន និងបង្រៀន',note:'',total:929500,items:[{name:'ក្ដារចំនួន០ដល់២០',unit:'ឈុត',qty:4,price:45000,sub:180000},{name:'ក្ដារស្រះនិស្ស័យ',unit:'ឈុត',qty:4,price:45000,sub:180000},{name:'ក្ដារព្យញ្ជនៈ៣៣តួ',unit:'ឈុត',qty:4,price:45000,sub:180000},{name:'គូល័រឈើ',unit:'ប្រអប់',qty:12,price:12000,sub:144000},{name:'ហ្វឺតសរសេរក្ដារខៀន',unit:'ប្រអប់',qty:3,price:52500,sub:157500},{name:'ទឹកហ្វឺត(ខៀវ)',unit:'ប្រអប់',qty:1,price:55000,sub:55000},{name:'ទឹកហ្វឺត(ក្រហម)',unit:'ដប',qty:6,price:5500,sub:33000}]},
  {id:3,bon:'003',date:'2026-02-20',acc:'60058',cat:'សម្ភារៈរៀន និងបង្រៀន',note:'',total:336600,items:[{name:'ក្រដាសរ៉ាមDoubble A(ពណ៌)',unit:'ដុំ',qty:4,price:15500,sub:62000},{name:'ហ្វឺតTOYO(Blue)',unit:'ប្រអប់',qty:5,price:25500,sub:127500},{name:'ហ្វឺតTOYO(Red)',unit:'ប្រអប់',qty:5,price:25500,sub:127500},{name:'ថង់ស្រោបរូបភាព',unit:'ដុំ',qty:1,price:19600,sub:19600}]},
  {id:4,bon:'004',date:'2026-03-05',acc:'60058',cat:'អប់រំបំណិនជីវិត កីឡា ការងារយុវជន និងកុមារ',note:'',total:355500,items:[{name:'បាល់ទាត់(Mikasa)',unit:'គ្រាប់',qty:3,price:66000,sub:198000},{name:'បាល់ទះ(Mikasa)',unit:'គ្រាប់',qty:2,price:66000,sub:132000},{name:'ប្រេងកូឡា',unit:'ប្រអប់',qty:5,price:5100,sub:25500}]},
  {id:5,bon:'005',date:'2026-03-09',acc:'61058',cat:'ការកែលម្អបរិស្ថាន',note:'',total:403300,items:[{name:'អំបោសស្មៅ',unit:'ដើម',qty:10,price:7000,sub:70000},{name:'អំបោសធាងដូង',unit:'ដើម',qty:10,price:12000,sub:120000},{name:'ធុងសំរាមជ័រ',unit:'ធុង',qty:5,price:22000,sub:110000},{name:'ច្រាសដុសបង្គន់',unit:'ដើម',qty:10,price:8000,sub:80000},{name:'អំបោសជូតការ៉ូ',unit:'ដើម',qty:1,price:23300,sub:23300}]},
  {id:6,bon:'006',date:'2026-03-11',acc:'61058',cat:'ការថែទាំ និងជួសជុលផ្សេងៗ',note:'',total:322100,items:[{name:'ទឹកថ្នាំព្រីនRefill ink 70ml',unit:'ឈុត',qty:1,price:50000,sub:50000},{name:'ដុំទឹកថ្នាំPrinter',unit:'ឈុត',qty:2,price:105000,sub:210000},{name:'USB Connect Wifi',unit:'ឈុត',qty:1,price:62100,sub:62100}]},
  {id:7,bon:'007',date:'2026-03-12',acc:'61108',cat:'ការចូលរៀនដោយ​សមធម៌ និងបង្ការសិស្សបោះបង់',note:'',total:333500,items:[{name:'ប្រដាប់កិបក្រដាសម៉ាក Kangaro',unit:'ប្រអប់',qty:2,price:40000,sub:80000},{name:'ហ្វឺតHighLight ជីរ៉ាហ្វ',unit:'ដើម',qty:20,price:5000,sub:100000},{name:'ក្រដាសផ្ទាំងធំ',unit:'ដុំ',qty:1,price:53500,sub:53500},{name:'ក្រដាសរ៉ាមDoubble A',unit:'កេស',qty:1,price:60000,sub:60000},{name:'កន្ត្រៃ',unit:'ដើម',qty:10,price:4000,sub:40000}]}
];
function sBuildYearSel(){
  var sel=document.getElementById('s-yr-sel');if(!sel) return;
  sel.innerHTML='';
  var y=new Date().getFullYear();
  for(var i=y-1;i<=y+2;i++){
    var o=document.createElement('option');o.value=i;o.textContent=i;
    if(i===y) o.selected=true; sel.appendChild(o);
  }
  sYear=y;
}
function sOnYearChange(){sYear=parseInt(document.getElementById('s-yr-sel').value);if(sQ) sUpdateColBadge();}
function sSelectQ(q){
  sQ=q;
  ['Q1','Q2','Q3','Q4'].forEach(function(x){
    var el=document.getElementById('sqc-'+x);if(el) el.classList.toggle('active',x===q);
  });
  sUpdateColBadge();
  document.getElementById('import-btn').disabled=false;
  document.getElementById('clear-btn').disabled=false;
}
function sUpdateColBadge(){
  var b=document.getElementById('s-col-badge');
  if(b){b.style.display='block';b.textContent='📦 Collection: '+sGetCol();}
}
function sFmt(n){return n?Number(n).toLocaleString():'0';}
function sRenderPreview(){
  var list=document.getElementById('s-sect-list');if(!list) return;
  list.innerHTML='';
  SECTIONS.forEach(function(s){
    var div=document.createElement('div');div.className='sect-item';
    div.innerHTML='<span class="snum">'+s.id+'. '+s.bon+'</span><strong>'+s.cat.substring(0,20)+(s.cat.length>20?'...':'')+'</strong><span class="stot">៛'+sFmt(s.total)+'</span><br><span class="sitems">📅 '+s.date+' · '+s.items.length+' ទំនិញ · '+s.acc+'</span>';
    list.appendChild(div);
  });
  document.getElementById('s-preview-box').style.display='block';
}
function sSetStatus(msg,type){
  var el=document.getElementById('s-status-box');
  el.className='s-status '+type;el.innerHTML=msg;el.style.display='block';
}
function sSetProgress(done,total){
  var pct=total?Math.round(done/total*100):0;
  document.getElementById('s-prog-bar').style.width=pct+'%';
  document.getElementById('s-prog-lbl').textContent=done+' / '+total+' ('+pct+'%)';
}
async function doImport(){
  var btn=document.getElementById('import-btn'),clrBtn=document.getElementById('clear-btn');
  btn.disabled=true;clrBtn.disabled=true;btn.textContent='⏳ កំពុង Import...';
  document.getElementById('s-prog-wrap').style.display='block';
  sSetProgress(0,SECTIONS.length);sSetStatus('🔄 កំពុង Import ទិន្នន័យ...','info');
  try{
    var col=sGetCol();
    if(!col){sSetStatus('❌ សូមជ្រើស Period មុន!','err');btn.disabled=false;clrBtn.disabled=false;btn.textContent='📥 Import ទៅ Firestore';return;}
    sSetStatus('🗑️ កំពុងលុបទិន្នន័យចាស់ក្នុង '+col+'...','info');
    var existing=await window.db.collection(col).get();
    var delBatch=window.db.batch();
    existing.docs.forEach(function(d){delBatch.delete(d.ref);});
    if(existing.docs.length>0) await delBatch.commit();
    var user=window.auth.currentUser;
    var editBy=user?(user.displayName||user.email||''):'';
    var editAt=new Date().toLocaleString();
    for(var i=0;i<SECTIONS.length;i++){
      var s=Object.assign({},SECTIONS[i],{_editBy:editBy,_editAt:editAt});
      await window.db.collection(col).add(s);
      sSetProgress(i+1,SECTIONS.length);
    }
    sSetStatus('✅ Import <strong>'+col+'</strong> បានជោគជ័យ!<br>📦 ក្រុម: <strong>'+SECTIONS.length+'</strong><br>🗂️ ទំនិញសរុប: <strong>'+SECTIONS.reduce(function(a,s){return a+s.items.length;},0)+'</strong><br>💰 ទឹកប្រាក់សរុប: <strong>៛'+sFmt(SECTIONS.reduce(function(a,s){return a+s.total;},0))+'</strong>','ok');
    btn.textContent='✅ Import រួចហើយ';
  }catch(e){
    sSetStatus('❌ Error: '+(e.message||e.code||'unknown'),'err');
    btn.disabled=false;btn.textContent='📥 Import ទៅ Firestore';
  }
  clrBtn.disabled=false;
}
async function doClear(){
  if(!confirm('លុបទិន្នន័យទាំងអស់ក្នុង Firestore? មិនអាច undo បានទេ!')) return;
  var btn=document.getElementById('clear-btn'),impBtn=document.getElementById('import-btn');
  btn.disabled=true;impBtn.disabled=true;btn.textContent='⏳ កំពុងលុប...';
  sSetStatus('🗑️ កំពុងលុប...','info');
  try{
    var col=sGetCol();
    if(!col){sSetStatus('❌ សូមជ្រើស Period មុន!','err');btn.disabled=false;impBtn.disabled=false;btn.textContent='🗑️ លុបទិន្នន័យទាំងអស់';return;}
    var snap=await window.db.collection(col).get();
    var batch=window.db.batch();
    snap.docs.forEach(function(d){batch.delete(d.ref);});
    await batch.commit();
    sSetStatus('✅ លុបបានជោគជ័យ! ('+snap.docs.length+' documents)','ok');
    btn.textContent='✅ លុបរួចហើយ';
  }catch(e){
    sSetStatus('❌ Error: '+(e.message||e.code),'err');
    btn.disabled=false;btn.textContent='🗑️ លុបទិន្នន័យទាំងអស់';
  }
  impBtn.disabled=false;
}
</script>
<script defer="" src="https://static.cloudflareinsights.com/beacon.min.js/v8c78df7c7c0f484497ecbca7046644da1771523124516" integrity="sha512-8DS7rgIrAmghBFwoOTujcf6D9rXvH8xm8JQ1Ja01h9QX8EzXldiszufYa4IFfKdLUKTTrnSFXLDkUEOTrZQ8Qg==" data-cf-beacon="{" version":"2024.11.0","token":"e3c1c9af36de41759418005494a48906","r":1,"server_timing":{"name":{"cfcachestatus":true,"cfedge":true,"cfextpri":true,"cfl4":true,"cforigin":true,"cfspeedbrain":true},"location_startswith":null}}"="" crossorigin="anonymous"></script>
</template>

<template id="tpl-ឆមាស១">
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=0.85">
  <title>របាយការណ៍បូកសរុបលទ្ធផលការងារអប់រំ</title>
  <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-app-compat.js"></script>
  <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-database-compat.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Kantumruy+Pro:wght@300;400;500;600;700&display=swap');
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { font-family: 'Kantumruy Pro', sans-serif; line-height: 1.3; color: #222; background: #f0f4f8; }


/* TAB NAV */
.tab-nav { display: flex; background: #1565c0; padding: 0 16px; gap: 4px; position: sticky; top: 0; z-index: 100; box-shadow: 0 2px 8px rgba(0,0,0,0.3); }
.tab-nav button { font-family: 'Kantumruy Pro', sans-serif; font-size: 13px; font-weight: 600; padding: 10px 20px; border: none; background: transparent; color: rgba(255,255,255,0.7); cursor: pointer; border-bottom: 3px solid transparent; transition: all 0.2s; white-space: nowrap; }
.tab-nav button:hover { color: #fff; background: rgba(255,255,255,0.1); }
.tab-nav button.active { color: #fff; border-bottom-color: #ffd600; background: rgba(255,255,255,0.15); }

.tab-page { display: none; }
.tab-page.active { display: block; }

.page-inner { max-width: 1020px; margin: 16px auto; padding: 16px 20px; background: #fff; border-radius: 6px; box-shadow: 0 1px 4px rgba(0,0,0,0.12); }

h1 { font-size: 13px; font-weight: 700; margin: 14px 0 4px; background: #1565c0; color: #fff; padding: 5px 10px; border-radius: 4px; }
h2 { font-size: 12px; font-weight: 600; margin: 10px 0 4px; color: #1565c0; border-left: 3px solid #1565c0; padding-left: 6px; }
h3 { font-size: 12px; font-weight: 600; margin: 10px 0 4px; color: #333; }

.header { text-align: center; font-size: 13px; font-weight: 700; line-height: 1.6; margin-bottom: 4px; }
.title  { text-align: left; font-size: 13px; font-weight: 700; line-height: 1.6; margin-bottom: 4px; }

table { width: 100%; border-collapse: collapse; margin-top: 4px; background: #fff; font-size: 12px; }
th, td { border: 1px solid #aaa; padding: 2px 5px; text-align: center; white-space: nowrap; }
td { text-align: left; }
tr:nth-child(even) td { background: #f9f9f9; }
th { background: #e3eaf5; color: #1a237e; }
table thead tr:first-child th { background: #1565c0; color: #fff; }

.editable { background: #fffde7; border-bottom: 1px dashed #bbb; display: inline-block; min-width: 28px; text-align: center; outline: none; padding: 1px 4px; font-size: 12px; font-family: 'Kantumruy Pro', sans-serif; border-radius: 2px; }
.editable:focus { background: #fff9c4; border-bottom-color: #f9a825; }

/* ===== TOOLBAR ===== */
.toolbar { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 12px; padding: 8px 10px; background: #f0f4f8; border-radius: 6px; border: 1px solid #d0d7de; align-items: center; }
.toolbar button, .toolbar label { font-family: 'Kantumruy Pro', sans-serif; font-size: 12px; padding: 5px 12px; border-radius: 4px; border: 1px solid #999; background: #fff; cursor: pointer; transition: all 0.2s; color: #333; font-weight: 600; }
.toolbar button:hover, .toolbar label:hover { background: #e2e8f0; border-color: #666; }
.toolbar .btn-print   { background: #e8f5e9; border-color: #4caf50; color: #2e7d32; }
.toolbar .btn-xlsx    { background: #e3f2fd; border-color: #2196f3; color: #1565c0; }
.toolbar .btn-json    { background: #fff3e0; border-color: #ff9800; color: #e65100; }
.toolbar .btn-save    { background: #fce4ec; border-color: #e91e63; color: #880e4f; }
.toolbar .btn-load    { background: #e8f5e9; border-color: #388e3c; color: #1b5e20; }
.toolbar .btn-import  { background: #f3e5f5; border-color: #9c27b0; color: #4a148c; }
.toolbar .btn-list    { background: #e8eaf6; border-color: #3f51b5; color: #1a237e; }

/* Firebase name input row */
.fb-row { display: flex; align-items: center; gap: 6px; width: 100%; background: #e3f2fd; border: 1px solid #90caf9; border-radius: 6px; padding: 6px 10px; margin-bottom: 4px; }
.fb-row label { font-size: 12px; font-weight: 700; color: #1565c0; white-space: nowrap; }
.fb-row input, .fb-row select { font-family: 'Kantumruy Pro', sans-serif; font-size: 12px; padding: 4px 8px; border-radius: 4px; border: 1px solid #64b5f6; flex: 1; min-width: 120px; color: #1a237e; background: #fff; }
.fb-row input:focus, .fb-row select:focus { outline: none; border-color: #1565c0; box-shadow: 0 0 0 2px rgba(21,101,192,0.2); }

#fbStatus { font-size: 11px; padding: 4px 10px; border-radius: 20px; display: none; font-weight: bold; }
#fbStatus.ok  { background: #4caf50; color: white; display: inline-block; }
#fbStatus.err { background: #f44336; color: white; display: inline-block; }
#fbStatus.info { background: #1565c0; color: white; display: inline-block; }
.online-dot { height: 8px; width: 8px; background-color: #fff; border-radius: 50%; display: inline-block; margin-right: 5px; }

/* Save list modal */
.modal-overlay { display: none; position: fixed; inset: 0; background: rgba(0,0,0,0.5); z-index: 999; align-items: center; justify-content: center; }
.modal-overlay.open { display: flex; }
.modal-box { background: #fff; border-radius: 8px; padding: 20px; min-width: 340px; max-width: 500px; max-height: 80vh; overflow-y: auto; box-shadow: 0 8px 32px rgba(0,0,0,0.3); }
.modal-box h2 { font-size: 14px; color: #1565c0; margin-bottom: 12px; border-bottom: 2px solid #1565c0; padding-bottom: 6px; }
.report-item { display: flex; align-items: center; justify-content: space-between; padding: 8px 10px; border: 1px solid #e0e0e0; border-radius: 4px; margin-bottom: 6px; background: #f9f9f9; }
.report-item:hover { background: #e3f2fd; border-color: #1565c0; }
.report-item .ri-name { font-size: 13px; font-weight: 600; color: #1a237e; }
.report-item .ri-time { font-size: 11px; color: #777; margin-top: 2px; }
.report-item .ri-btns { display: flex; gap: 4px; }
.ri-btn-load { font-family: 'Kantumruy Pro', sans-serif; font-size: 11px; padding: 3px 10px; border-radius: 3px; border: 1px solid #388e3c; background: #e8f5e9; color: #1b5e20; cursor: pointer; font-weight: 600; }
.ri-btn-del  { font-family: 'Kantumruy Pro', sans-serif; font-size: 11px; padding: 3px 10px; border-radius: 3px; border: 1px solid #c62828; background: #ffebee; color: #c62828; cursor: pointer; font-weight: 600; }
.modal-close { font-family: 'Kantumruy Pro', sans-serif; width: 100%; margin-top: 10px; padding: 7px; border-radius: 4px; border: 1px solid #999; background: #f5f5f5; cursor: pointer; font-size: 12px; font-weight: 600; }
.empty-msg { text-align: center; color: #999; font-size: 13px; padding: 20px; }

.btn-group { display: flex; gap: 3px; justify-content: center; }
.btn-inc, .btn-dec { font-family: 'Kantumruy Pro', sans-serif; font-size: 11px; padding: 2px 7px; border-radius: 3px; border: 1px solid #888; cursor: pointer; transition: background 0.2s; }
.btn-inc { background: #e3f2fd; border-color: #42a5f5; }
.btn-inc:hover { background: #bbdefb; }
.btn-dec { background: #fce4ec; border-color: #ef9a9a; }
.btn-dec:hover { background: #ffcdd2; }

.note { margin-top: 6px; font-style: italic; color: #555; font-size: 12px; }
.table-cell { border: 1px solid #aaa; padding: 3px 6px; }
.p-2 { padding: 3px 5px; }
.p-3 { padding: 4px 7px; }
.text-center { text-align: center !important; }
.font-bold { font-weight: 700; }
.hover-row:hover td { background: #e8f4fd !important; }
.header-cell th { background: #dce8f5; font-weight: 600; }
.table-container { overflow-x: auto; margin-bottom: 12px; }
.table-container table { font-size: 11px; }
.tg-wrap { overflow-x: auto; margin-bottom: 12px; }

@media print {
  .tab-nav, .toolbar, #fbStatus, .fb-row, .modal-overlay { display: none !important; }
  .tab-page { display: block !important; }
  .page-inner { box-shadow: none; margin: 0; padding: 8px; }
  body { background: #fff; }
  .editable { border: none; background: transparent; }
  thead { display: table-header-group; }
}


  </style>



<!-- MODAL: List of saved reports -->

<div class="modal-overlay" id="modalOverlay">
  <div class="modal-box">
    <h2>📋 របាយការណ៍ដែលបានរក្សាទុក</h2>
    <div id="reportList"><div class="empty-msg">⏳ កំពុងផ្ទុក...</div></div>
    <button class="modal-close" id="modalClose">✕ បិទ</button>
  </div>
</div>

<!-- TAB NAV -->

<div class="tab-nav">
  <button class="active" data-tab="tab1">📋 របាយការណ៍</button>
  <button data-tab="tab2">📊 ស្ថិតិ</button>
  <button data-tab="tab3">👥 បញ្ជីបុគ្គលិក</button>
</div>

<!-- ===================== TAB 1 ===================== -->

<div id="tab1" class="tab-page active">
  <div class="page-inner">

<!-- HEADER -->
<div class="header">ព្រះរាជាណាចក្រកម្ពុជា<br>ជាតិ សាសនា ព្រះមហាក្សត្រ<br>-------xxx-------</div>
<div style="display:flex; justify-content:space-between; font-size:13px; margin:4px 0;">
  <div class="title">រដ្ឋបាលស្រុកភ្នំស្រុក<br>ការិយាល័យអប់រំ យុវជន និងកីឡាស្រុក<br>កម្រងស្ពានស្រែង<br>សាលាបឋមសិក្សា រោគ</div>
</div>
<div class="header" style="margin:6px 0; font-weight:800;">
  របាយការណ៍បូកសរុបលទ្ធផលការងារអប់រំ ផ្នែកបឋមសិក្សា<br>
  (នាឆមាសទី១ ឆ្នាំសិក្សា២០២៥-២០២៦)
</div>

<!-- FIREBASE NAME ROW -->
<div class="fb-row">
  <label>🏫 ឈ្មោះសាលា / ID :</label>
  <input type="text" id="reportName" placeholder="ឧ. ស្ពានស្រែង_រោគ_2026" value="ស្ពានស្រែង_រោគ_2026">
  <label>📅 ឆ្នាំ :</label>
  <select id="reportYear">
    <option value="2025-2026" selected="">២០២៥-២០២៦</option>
    <option value="2024-2025">២០២៤-២០២៥</option>
    <option value="2026-2027">២០២៦-២០២៧</option>
  </select></div>
  <label>📝 ឆមាស :</label>
  <select id="reportSem">
    <option value="sem1" selected="">ឆមាសទី១</option>
    <option value="sem2">ឆមាសទី២</option>
  </select>
</div>

<!-- TOOLBAR -->
<div class="toolbar">
  <button class="btn-print" id="btnPrint">🖨️ Print</button>
  <button class="btn-xlsx" id="btnXlsx">📊 XLSX</button>
  <button class="btn-json" id="btnJson">📄 JSON</button>
  <button class="btn-save" id="btnSave">☁️ រក្សាទុក Firebase</button>
  <button class="btn-load" id="btnLoadCurrent">📥 ហៅ​ (Load)</button>
  <button class="btn-list" id="btnList">📋 បញ្ជី</button>
  <span id="fbStatus"></span>
</div>

<!-- I -->
<h1>I. បម្រែបម្រួលផ្នែកបរិមាណ</h1>
<h2>១. សាលារៀន</h2>
<div class="table-container"><table id="schoolDataTable">
  <tbody>
    <tr>
      <td>ចំនួនកម្រងសាលារៀន :</td><td><span contenteditable="" class="editable">1</span></td><td>កម្រង</td>
      <td>ទីប្រជុំជន</td><td><span contenteditable="" class="editable">0</span></td>
      <td>ធម្មតា</td><td><span contenteditable="" class="editable">0</span></td>
      <td>ដាច់ស្រយាល</td><td><span contenteditable="" class="editable">1</span></td>
      <td>មិនធម្មតា</td><td><span contenteditable="" class="editable">0</span></td>
    </tr>
    <tr>
      <td>ចំនួនសាលារៀន បិទទ្វារ :</td><td><span contenteditable="" class="editable">0</span></td><td>សាលា</td>
      <td colspan="2">មូលហេតុដែលបិទ :</td><td colspan="6"><span contenteditable="" class="editable">.................</span></td>
    </tr>
    <tr>
      <td>ចំនួនសាលារៀន មានគ្រប់កម្រិតថ្នាក់ :</td><td><span contenteditable="" class="editable">1</span></td><td colspan="2">សាលា</td>
      <td colspan="5">ចំនួនសាលារៀន មិនមានគ្រប់កម្រិតថ្នាក់ :</td><td><span contenteditable="" class="editable">0</span></td><td>សាលា</td>
    </tr>
    <tr>
      <td>ចំនួនបន្ទប់ សរុប :</td><td><span contenteditable="" class="editable">15</span></td><td>បន្ទប់</td>
      <td colspan="2">បន្ទប់បង្រៀន</td><td><span contenteditable="" class="editable">12</span></td><td>បន្ទប់</td>
      <td colspan="2">បន្ទប់មិនបង្រៀន</td><td><span contenteditable="" class="editable">3</span></td><td>បន្ទប់</td>
    </tr>
  </tbody>
</table></div>

<h2>២. ប្រៀបធៀបចំនួនសិស្ស បវេសនកាល</h2>
<div class="table-container"><table id="studentComparisonTable">
  <tbody>
    <tr>
      <th>ចំនួនសិស្សសរុបរួម :</th><th id="totalStudents">248</th>
      <th>នាក់ ស្រី :</th><th id="totalFemale">116</th>
      <th>នាក់</th><th colspan="6"> </th>
    </tr>
    <tr data-grade="1">
      <td>សិស្សសរុបថ្នាក់ទី១ :</td>
      <td><span contenteditable="" class="editable grade-total" data-grade="1">30</span></td>
      <td>នាក់ ស្រី :</td>
      <td><span contenteditable="" class="editable grade-female" data-grade="1">14</span></td>
      <td>នាក់</td>
      <td><div class="btn-group"><button class="btn-inc" data-grade="1">កើន</button><button class="btn-dec" data-grade="1">ថយ</button></div></td>
      <td><span class="change-count" data-grade="1">0</span></td>
      <td>នាក់ / មូលហេតុ</td>
      <td><select class="change-reason" data-grade="1"><option>----</option><option>ផ្ទេរចូល</option><option>ផ្ទេរចេញ</option><option>ប្ដូរទីលំនៅ</option><option>ឈឺ</option><option>ស្លាប់</option></select></td>
      <td><span contenteditable="" class="editable cause-count" data-grade="1">0</span></td><td>នាក់</td>
    </tr>
    <tr data-grade="2">
      <td>សិស្សសរុបថ្នាក់ទី២ :</td>
      <td><span contenteditable="" class="editable grade-total" data-grade="2">42</span></td>
      <td>នាក់ ស្រី :</td>
      <td><span contenteditable="" class="editable grade-female" data-grade="2">21</span></td>
      <td>នាក់</td>
      <td><div class="btn-group"><button class="btn-inc" data-grade="2">កើន</button><button class="btn-dec" data-grade="2">ថយ</button></div></td>
      <td><span class="change-count" data-grade="2">0</span></td>
      <td>នាក់ / មូលហេតុ</td>
      <td><select class="change-reason" data-grade="2"><option>----</option><option>ផ្ទេរចូល</option><option>ផ្ទេរចេញ</option><option>ប្ដូរទីលំនៅ</option><option>ឈឺ</option><option>ស្លាប់</option></select></td>
      <td><span contenteditable="" class="editable cause-count" data-grade="2">0</span></td><td>នាក់</td>
    </tr>
    <tr data-grade="3">
      <td>សិស្សសរុបថ្នាក់ទី៣ :</td>
      <td><span contenteditable="" class="editable grade-total" data-grade="3">42</span></td>
      <td>នាក់ ស្រី :</td>
      <td><span contenteditable="" class="editable grade-female" data-grade="3">20</span></td>
      <td>នាក់</td>
      <td><div class="btn-group"><button class="btn-inc" data-grade="3">កើន</button><button class="btn-dec" data-grade="3">ថយ</button></div></td>
      <td><span class="change-count" data-grade="3">0</span></td>
      <td>នាក់ / មូលហេតុ</td>
      <td><select class="change-reason" data-grade="3"><option>----</option><option>ផ្ទេរចូល</option><option>ផ្ទេរចេញ</option><option>ប្ដូរទីលំនៅ</option><option>ឈឺ</option><option>ស្លាប់</option></select></td>
      <td><span contenteditable="" class="editable cause-count" data-grade="3">0</span></td><td>នាក់</td>
    </tr>
    <tr data-grade="4">
      <td>សិស្សសរុបថ្នាក់ទី៤ :</td>
      <td><span contenteditable="" class="editable grade-total" data-grade="4">49</span></td>
      <td>នាក់ ស្រី :</td>
      <td><span contenteditable="" class="editable grade-female" data-grade="4">21</span></td>
      <td>នាក់</td>
      <td><div class="btn-group"><button class="btn-inc" data-grade="4">កើន</button><button class="btn-dec" data-grade="4">ថយ</button></div></td>
      <td><span class="change-count" data-grade="4">0</span></td>
      <td>នាក់ / មូលហេតុ</td>
      <td><select class="change-reason" data-grade="4"><option>----</option><option>ផ្ទេរចូល</option><option>ផ្ទេរចេញ</option><option>ប្ដូរទីលំនៅ</option><option>ឈឺ</option><option>ស្លាប់</option></select></td>
      <td><span contenteditable="" class="editable cause-count" data-grade="4">0</span></td><td>នាក់</td>
    </tr>
    <tr data-grade="5">
      <td>សិស្សសរុបថ្នាក់ទី៥ :</td>
      <td><span contenteditable="" class="editable grade-total" data-grade="5">50</span></td>
      <td>នាក់ ស្រី :</td>
      <td><span contenteditable="" class="editable grade-female" data-grade="5">23</span></td>
      <td>នាក់</td>
      <td><div class="btn-group"><button class="btn-inc" data-grade="5">កើន</button><button class="btn-dec" data-grade="5">ថយ</button></div></td>
      <td><span class="change-count" data-grade="5">0</span></td>
      <td>នាក់ / មូលហេតុ</td>
      <td><select class="change-reason" data-grade="5"><option>----</option><option>ផ្ទេរចូល</option><option>ផ្ទេរចេញ</option><option>ប្ដូរទីលំនៅ</option><option>ឈឺ</option><option>ស្លាប់</option></select></td>
      <td><span contenteditable="" class="editable cause-count" data-grade="5">0</span></td><td>នាក់</td>
    </tr>
    <tr data-grade="6">
      <td>សិស្សសរុបថ្នាក់ទី៦ :</td>
      <td><span contenteditable="" class="editable grade-total" data-grade="6">35</span></td>
      <td>នាក់ ស្រី :</td>
      <td><span contenteditable="" class="editable grade-female" data-grade="6">17</span></td>
      <td>នាក់</td>
      <td><div class="btn-group"><button class="btn-inc" data-grade="6">កើន</button><button class="btn-dec" data-grade="6">ថយ</button></div></td>
      <td><span class="change-count" data-grade="6">0</span></td>
      <td>នាក់ / មូលហេតុ</td>
      <td><select class="change-reason" data-grade="6"><option>----</option><option>ផ្ទេរចូល</option><option>ផ្ទេរចេញ</option><option>ប្ដូរទីលំនៅ</option><option>ឈឺ</option><option>ស្លាប់</option></select></td>
      <td><span contenteditable="" class="editable cause-count" data-grade="6">0</span></td><td>នាក់</td>
    </tr>
  </tbody>
</table></div>
<p class="note"><strong>បញ្ជាក់៖</strong> ចំពោះសិស្សទាំងនេះគឺយកសិស្សពិតប្រាកដនៅ ឆមាសទី១ ឆ្នាំសិក្សា ២០២៤-២០២៥។</p>

<h2>៣. ចំនួនថ្នាក់តាមកម្រិត ៖</h2>
<div class="table-container"><table id="classLevelsTable">
  <tbody>
    <tr><th>ថ្នាក់សរុប :</th><th id="totalClasses">10</th><th>ថ្នាក់</th></tr>
    <tr><td>កម្រិតថ្នាក់ទី១ :</td><td><span contenteditable="" class="editable class-count">1</span></td><td>ថ្នាក់</td></tr>
    <tr><td>កម្រិតថ្នាក់ទី២ :</td><td><span contenteditable="" class="editable class-count">2</span></td><td>ថ្នាក់</td></tr>
    <tr><td>កម្រិតថ្នាក់ទី៣ :</td><td><span contenteditable="" class="editable class-count">2</span></td><td>ថ្នាក់</td></tr>
    <tr><td>កម្រិតថ្នាក់ទី៤ :</td><td><span contenteditable="" class="editable class-count">2</span></td><td>ថ្នាក់</td></tr>
    <tr><td>កម្រិតថ្នាក់ទី៥ :</td><td><span contenteditable="" class="editable class-count">2</span></td><td>ថ្នាក់</td></tr>
    <tr><td>កម្រិតថ្នាក់ទី៦ :</td><td><span contenteditable="" class="editable class-count">1</span></td><td>ថ្នាក់</td></tr>
    <tr><td>ថ្នាក់គួប :</td><td><span contenteditable="" class="editable class-count">0</span></td><td>ថ្នាក់</td></tr>
  </tbody>
</table></div>

<h2>៤. អំពី​មន្រ្តី​អប់រំ</h2>
<div class="table-container"><table>
  <tbody>
        <tr>
          <th colspan="2">សរុប មន្រ្តី ថ្នាក់សាលារៀន :</th>
          <th contenteditable="" class="editable">17</th><th>នាក់ ស្រី</th>
          <th colspan="2" contenteditable="" class="editable">13<span>នាក់</span></th>
        </tr>
        <tr><th colspan="5" style="text-align:left;">ក្នុងនោះមាន :</th></tr>
        <tr><td>នាយក/រង (មិនបង្រៀន)</td><td>:</td><td><span contenteditable="" class="editable">2</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">1</span> នាក់</td></tr>
        <tr><td>នាយក/រង (បង្រៀន)</td><td>:</td><td><span contenteditable="" class="editable">0</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">0</span> នាក់</td></tr>
        <tr><td>សិក្ខាបនធារី សរុប</td><td>:</td><td><span contenteditable="" class="editable">10</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">9</span> នាក់</td></tr>
        <tr><td>សិក្ខាបនធារី បង្រៀន២ពេល</td><td>:</td><td><span contenteditable="" class="editable">0</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">0</span> នាក់</td></tr>
        <tr><td>សិក្ខាបនធារី ថ្នាក់គួប</td><td>:</td><td><span contenteditable="" class="editable">0</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">0</span> នាក់</td></tr>
        <tr><td>លេខាធិការ</td><td>:</td><td><span contenteditable="" class="editable">1</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">0</span> នាក់</td></tr>
        <tr><td>កាន់បណ្ណាល័យ</td><td>:</td><td><span contenteditable="" class="editable">1</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">1</span> នាក់</td></tr>
        <tr><td>កាន់ រោងជាង</td><td>:</td><td><span contenteditable="" class="editable">0</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">0</span> នាក់</td></tr>
        <tr><td>កាន់ សិល្បះ</td><td>:</td><td><span contenteditable="" class="editable">0</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">0</span> នាក់</td></tr>
        <tr><td>កាន់ កសិកម្ម</td><td>:</td><td><span contenteditable="" class="editable">1</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">0</span> នាក់</td></tr>
        <tr><td>កាន់ គេហៈ</td><td>:</td><td><span contenteditable="" class="editable">0</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">0</span> នាក់</td></tr>
        <tr><td>កាន់កីឡា</td><td>:</td><td><span contenteditable="" class="editable">0</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">0</span> នាក់</td></tr>
        <tr><td>ផ្សេង ៗ</td><td>:</td><td><span contenteditable="" class="editable">0</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">0</span> នាក់</td></tr>
        <tr><td>បង្រៀន មត្តេយ្យ</td><td>:</td><td><span contenteditable="" class="editable">2</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">2</span> នាក់</td></tr>
        <tr><td>ឈឺ</td><td>:</td><td><span contenteditable="" class="editable">0</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">0</span> នាក់</td></tr>
        <tr><td>លំហែ</td><td>:</td><td><span contenteditable="" class="editable">0</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">0</span> នាក់</td></tr>
        <tr><td>ត្រៀមចូលនិវត្តន៍</td><td>:</td><td><span contenteditable="" class="editable">0</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">0</span> នាក់</td></tr>
        <tr><td>ព្យួរ</td><td>:</td><td><span contenteditable="" class="editable">0</span></td><td>នាក់ ស្រី</td><td><span contenteditable="" class="editable">0</span> នាក់</td></tr>
      </tbody>
</table></div>

   <h2>៥. ហិរញ្ញប្បទាន ៖ (ចាប់​ពី​ មករា ដល់ ខែមិថុនា)</h2>
    <div class="table-container"><table>
      <tbody>
        <tr><th colspan="2">សំណង់ថ្មី</th><td>:</td><td><span contenteditable="" class="editable">0</span></td><td>ខ្នង</td><td><span contenteditable="" class="editable">0</span></td><td>បន្ទប់ អស់ថវិកា</td><td colspan="2"><span contenteditable="" class="editable">_ ៛</span></td></tr>
        <tr><td colspan="2">ប្រភពផ្តល់</td><td>:</td><td colspan="6"><span contenteditable="" class="editable">សហគមន៍ ,សប្បុរសជន លោកគ្រូអ្នកគ្រូ និងគាំទ្រសម្ភារៈសាងសង់ដោយ អង្គការទស្សនៈពិភពលោក</span></td></tr>
        <tr><td colspan="2">ជួសជុល</td><td>:</td><td><span contenteditable="" class="editable">0</span></td><td>ខ្នង</td><td><span contenteditable="" class="editable">0</span></td><td>បន្ទប់ អស់ថវិកា</td><td colspan="2">- ៛</td></tr>
        <tr><td colspan="2">ប្រភពផ្តល់</td><td>:</td><td colspan="6"><span contenteditable="" class="editable">ថវិកា (SOF)</span></td></tr>
        <tr><td colspan="2">សង្ហារឹម និងកែលម្អ</td><td>:</td><td colspan="3"><span contenteditable="" class="editable">........................................</span></td><td>អស់ថវិកា</td><td colspan="2"><span contenteditable="" class="editable">923,100 ៛</span></td></tr>
        <tr><td colspan="2">សម្ភារៈ ការិយាល័យ</td><td>:</td><td colspan="3"><span contenteditable="" class="editable">…………….................................</span></td><td>អស់ថវិកា</td><td colspan="2"><span contenteditable="" class="editable">2,358,400 ៛</span></td></tr>
        <tr><td colspan="2">សរុបចំណាយរួម</td><td>:</td><td colspan="3"><span contenteditable="" class="editable">……………................................</span></td><td>អស់ថវិកា</td><td colspan="2"><span contenteditable="" class="editable">3,281,500 ៛</span></td></tr>
      </tbody>
    </table></div>

    <h2>៦. ការងារ​បណ្ណាល័យ​<br>ក. ផ្នែកកម្រងសាលា</h2>
    <div class="table-container"><table>
      <tbody>
        <tr><th colspan="9">កម្រងសាលាដែលមានបណ្ណាល័យហើយមានដំណើរការជាប្រចាំចំនួនប៉ុន្មានកម្រង?</th></tr>
        <tr><td colspan="2">(សូមបញ្ជាក់ឈ្មោះកម្រង)</td><td>:</td><td>1 កម្រង</td><td colspan="5" contenteditable="" class="editable">ស្ពានស្រែង</td></tr>
        <tr><td colspan="9" contenteditable="" class="editable">សិស្សានុសិស្សចូលបណ្ណាល័យជាប្រចាំ តាមម៉ោងកាលវិភាគ និងម៉ោងសេរី</td></tr>
        <tr><td colspan="9">កម្រងសាលាដែលមានបណ្ណាល័យហើយមានដំណើរការមិនសូវបានល្អ :</td></tr>
        <tr><td colspan="2">(សូមបញ្ជាក់ឈ្មោះកម្រង និងមូលហេតុ)</td><td>:</td><td colspan="6"><span contenteditable="" class="editable">.................................</span></td></tr>
      </tbody>
    </table></div>

    <!-- II -->
    <h1>II. ការងារ​ធនាគុណភាព</h1>
    <h2>១. លទ្ធផល​សិក្សា​ឆមាសទី១</h2>
    <div class="table-container"><table id="resultsTable">
      <thead>
        <tr>
          <th rowspan="4">ថ្នាក់ទី</th>
          <th colspan="12">លទ្ធផល​សិក្សារបស់សិស្ស</th>
          <th rowspan="4">ផ្សេងៗ</th>
        </tr>
        <tr>
          <th colspan="2">សិស្សឆមាសទី១</th><th colspan="2">សិស្សបវេសនកាល</th>
          <th colspan="2">សិស្សចូលថ្មីថែម</th><th colspan="2">សិស្សជាប់</th>
          <th colspan="2">សិស្សធ្លាក់</th><th colspan="2">សិស្ស​បោះបង់</th>
        </tr>
        <tr>
          <td>សរុប</td><td>ស្រី</td><td>សរុប</td><td>ស្រី</td>
          <td>សរុប</td><td>ស្រី</td><td>សរុប</td><td>ស្រី</td>
          <td>សរុប</td><td>ស្រី</td><td>សរុប</td><td>ស្រី</td>
        </tr>
        <tr><td>១=៣+៥</td><td>២=៤+៦</td><td>៣</td><td>៤</td><td>៥</td><td>៦</td><td>៧</td><td>៨</td><td>៩</td><td>១០</td><td>១១</td><td>១២</td></tr>
      </thead>
      <tbody>
        <tr><td>1</td><td><span contenteditable="" class="editable r-s1">30</span></td><td><span contenteditable="" class="editable r-f1">14</span></td><td>30</td><td>14</td><td>0</td><td>0</td><td><span contenteditable="" class="editable r-pass1">30</span></td><td><span contenteditable="" class="editable r-fpas1">14</span></td><td><span contenteditable="" class="editable r-fail1">0</span></td><td><span contenteditable="" class="editable r-ffai1">0</span></td><td>0</td><td>0</td><td>0</td></tr>
        <tr><td>2</td><td><span contenteditable="" class="editable r-s2">42</span></td><td><span contenteditable="" class="editable r-f2">21</span></td><td>42</td><td>21</td><td>0</td><td>0</td><td><span contenteditable="" class="editable r-pass2">42</span></td><td><span contenteditable="" class="editable r-fpas2">21</span></td><td><span contenteditable="" class="editable r-fail2">0</span></td><td><span contenteditable="" class="editable r-ffai2">0</span></td><td>0</td><td>0</td><td>0</td></tr>
        <tr><td>3</td><td><span contenteditable="" class="editable r-s3">42</span></td><td><span contenteditable="" class="editable r-f3">20</span></td><td>41</td><td>21</td><td>0</td><td>0</td><td><span contenteditable="" class="editable r-pass3">38</span></td><td><span contenteditable="" class="editable r-fpas3">19</span></td><td><span contenteditable="" class="editable r-fail3">3</span></td><td><span contenteditable="" class="editable r-ffai3">2</span></td><td>0</td><td>0</td><td>0</td></tr>
        <tr><td>4</td><td><span contenteditable="" class="editable r-s4">49</span></td><td><span contenteditable="" class="editable r-f4">21</span></td><td>49</td><td>22</td><td>0</td><td>0</td><td><span contenteditable="" class="editable r-pass4">45</span></td><td><span contenteditable="" class="editable r-fpas4">20</span></td><td><span contenteditable="" class="editable r-fail4">4</span></td><td><span contenteditable="" class="editable r-ffai4">2</span></td><td>0</td><td>0</td><td>0</td></tr>
        <tr><td>5</td><td><span contenteditable="" class="editable r-s5">50</span></td><td><span contenteditable="" class="editable r-f5">23</span></td><td>50</td><td>23</td><td>0</td><td>0</td><td><span contenteditable="" class="editable r-pass5">40</span></td><td><span contenteditable="" class="editable r-fpas5">21</span></td><td><span contenteditable="" class="editable r-fail5">10</span></td><td><span contenteditable="" class="editable r-ffai5">2</span></td><td>0</td><td>0</td><td>0</td></tr>
        <tr><td>6</td><td><span contenteditable="" class="editable r-s6">35</span></td><td><span contenteditable="" class="editable r-f6">17</span></td><td>35</td><td>17</td><td>0</td><td>0</td><td><span contenteditable="" class="editable r-pass6">32</span></td><td><span contenteditable="" class="editable r-fpas6">15</span></td><td><span contenteditable="" class="editable r-fail6">3</span></td><td><span contenteditable="" class="editable r-ffai6">2</span></td><td>0</td><td>0</td><td>0</td></tr>
        <tr>
          <th>សរុប</th>
          <th id="rTotalS">248</th><th id="rTotalF">116</th>
          <th id="rTotalS2">248</th><th id="rTotalF2">116</th>
          <th>0</th><th>0</th>
          <th id="rTotalPass">227</th><th id="rTotalFPass">110</th>
          <th id="rTotalFail">20</th><th id="rTotalFFail">8</th>
          <th>0</th><th>0</th><th>0</th>
        </tr>
      </tbody>
    </table></div>

    <h2>២. លទ្ធផលសិក្សាសិស្សឆមាសទី១ គិតជា % ៖</h2>
    <div class="table-container"><table id="pctTable">
      <thead>
        <tr>
          <th class="table-cell p-3 text-center font-semibold">ថ្នាក់ទី</th>
          <th class="table-cell p-3 text-center font-semibold" colspan="2">%ឡើង</th>
          <th class="table-cell p-3 text-center font-semibold" colspan="2">%ត្រួត</th>
          <th class="table-cell p-3 text-center font-semibold" colspan="2">%បោះបង់</th>
          <th class="table-cell p-3 text-center font-semibold" colspan="2">ផ្សេងៗ</th>
        </tr>
        <tr class="header-cell">
          <th class="table-cell p-2 text-center">-</th>
          <th class="table-cell p-2 text-center">សរុប</th><th class="table-cell p-2 text-center">ស្រី</th>
          <th class="table-cell p-2 text-center">សរុប</th><th class="table-cell p-2 text-center">ស្រី</th>
          <th class="table-cell p-2 text-center">សរុប</th><th class="table-cell p-2 text-center">ស្រី</th>
          <th class="table-cell p-2 text-center">សរុប</th><th class="table-cell p-2 text-center">ស្រី</th>
        </tr>
      </thead>
      <tbody>
        <tr class="hover-row"><td class="table-cell p-3 text-center font-medium">1</td><td class="table-cell p-3 text-center">100%</td><td class="table-cell p-3 text-center">100%</td><td class="table-cell p-3 text-center">0.00%</td><td class="table-cell p-3 text-center">0.00%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td></tr>
        <tr class="hover-row"><td class="table-cell p-3 text-center font-medium">2</td><td class="table-cell p-3 text-center">100%</td><td class="table-cell p-3 text-center">100%</td><td class="table-cell p-3 text-center">0.00%</td><td class="table-cell p-3 text-center">0.00%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td></tr>
        <tr class="hover-row"><td class="table-cell p-3 text-center font-medium">3</td><td class="table-cell p-3 text-center">90%</td><td class="table-cell p-3 text-center">95%</td><td class="table-cell p-3 text-center">7.14%</td><td class="table-cell p-3 text-center">10.00%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td></tr>
        <tr class="hover-row"><td class="table-cell p-3 text-center font-medium">4</td><td class="table-cell p-3 text-center">92%</td><td class="table-cell p-3 text-center">95%</td><td class="table-cell p-3 text-center">8.16%</td><td class="table-cell p-3 text-center">9.52%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td></tr>
        <tr class="hover-row"><td class="table-cell p-3 text-center font-medium">5</td><td class="table-cell p-3 text-center">80%</td><td class="table-cell p-3 text-center">91%</td><td class="table-cell p-3 text-center">20.00%</td><td class="table-cell p-3 text-center">8.70%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td></tr>
        <tr class="hover-row"><td class="table-cell p-3 text-center font-medium">6</td><td class="table-cell p-3 text-center">91%</td><td class="table-cell p-3 text-center">88%</td><td class="table-cell p-3 text-center">8.57%</td><td class="table-cell p-3 text-center">11.76%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td></tr>
        <tr class="header-cell font-bold"><th class="table-cell p-3 text-center">សរុប</th><td class="table-cell p-3 text-center">92%</td><td class="table-cell p-3 text-center">95%</td><td class="table-cell p-3 text-center">8.06%</td><td class="table-cell p-3 text-center">6.90%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td><td class="table-cell p-3 text-center">0%</td></tr>
      </tbody>
    </table></div>

    <h2>៣. ការបង្រៀន និងការអនុវត្តកម្មវិធីសិក្សា ៖</h2>
    <div class="table-container"><table id="curriculumTable">
      <thead>
        <tr>
          <th rowspan="3">ថ្នាក់ទី</th>
          <th colspan="6">ចំនួនគ្រូបង្រៀន</th>
          <th colspan="5">ការអនុវត្តកម្មវិធីសិក្សា (គិតជា %)</th>
        </tr>
        <tr>
          <th colspan="2">ល្អ</th><th colspan="2">មធ្យម</th><th colspan="2">ខ្សោយ</th>
          <th rowspan="2">ភាសាខ្មែរ</th><th rowspan="2">គណិតវិទ្យា</th>
          <th rowspan="2">សិក្សាសង្គម</th><th rowspan="2">វិទ្យាសាស្ត្រ</th><th rowspan="2">ភាសាអង់គ្លេស</th>
        </tr>
        <tr><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th></tr>
      </thead>
      <tbody>
        <tr data-grade="1"><td>1</td><td><span contenteditable="" class="editable t-good-s" data-grade="1">1</span></td><td><span contenteditable="" class="editable t-good-f" data-grade="1">1</span></td><td><span contenteditable="" class="editable t-mid-s" data-grade="1">0</span></td><td><span contenteditable="" class="editable t-mid-f" data-grade="1">0</span></td><td><span contenteditable="" class="editable t-weak-s" data-grade="1">0</span></td><td><span contenteditable="" class="editable t-weak-f" data-grade="1">0</span></td><td><span contenteditable="" class="editable p-kh" data-grade="1">50</span></td><td><span contenteditable="" class="editable p-math" data-grade="1">55</span></td><td><span contenteditable="" class="editable p-soc" data-grade="1">40</span></td><td><span contenteditable="" class="editable p-sci" data-grade="1">45</span></td><td><span contenteditable="" class="editable p-eng" data-grade="1">0</span></td></tr>
        <tr data-grade="2"><td>2</td><td><span contenteditable="" class="editable t-good-s">0</span></td><td><span contenteditable="" class="editable t-good-f">0</span></td><td><span contenteditable="" class="editable t-mid-s">1</span></td><td><span contenteditable="" class="editable t-mid-f">1</span></td><td><span contenteditable="" class="editable t-weak-s">0</span></td><td><span contenteditable="" class="editable t-weak-f">0</span></td><td><span contenteditable="" class="editable p-kh">50</span></td><td><span contenteditable="" class="editable p-math">50</span></td><td><span contenteditable="" class="editable p-soc">40</span></td><td><span contenteditable="" class="editable p-sci">40</span></td><td><span contenteditable="" class="editable p-eng">0</span></td></tr>
        <tr data-grade="3"><td>3</td><td><span contenteditable="" class="editable t-good-s">0</span></td><td><span contenteditable="" class="editable t-good-f">0</span></td><td><span contenteditable="" class="editable t-mid-s">1</span></td><td><span contenteditable="" class="editable t-mid-f">1</span></td><td><span contenteditable="" class="editable t-weak-s">0</span></td><td><span contenteditable="" class="editable t-weak-f">0</span></td><td><span contenteditable="" class="editable p-kh">50</span></td><td><span contenteditable="" class="editable p-math">50</span></td><td><span contenteditable="" class="editable p-soc">40</span></td><td><span contenteditable="" class="editable p-sci">40</span></td><td><span contenteditable="" class="editable p-eng">0</span></td></tr>
        <tr data-grade="4"><td>4</td><td><span contenteditable="" class="editable t-good-s">0</span></td><td><span contenteditable="" class="editable t-good-f">0</span></td><td><span contenteditable="" class="editable t-mid-s">1</span></td><td><span contenteditable="" class="editable t-mid-f">1</span></td><td><span contenteditable="" class="editable t-weak-s">0</span></td><td><span contenteditable="" class="editable t-weak-f">0</span></td><td><span contenteditable="" class="editable p-kh">50</span></td><td><span contenteditable="" class="editable p-math">50</span></td><td><span contenteditable="" class="editable p-soc">40</span></td><td><span contenteditable="" class="editable p-sci">40</span></td><td><span contenteditable="" class="editable p-eng">0</span></td></tr>
        <tr data-grade="5"><td>5</td><td><span contenteditable="" class="editable t-good-s">0</span></td><td><span contenteditable="" class="editable t-good-f">0</span></td><td><span contenteditable="" class="editable t-mid-s">1</span></td><td><span contenteditable="" class="editable t-mid-f">1</span></td><td><span contenteditable="" class="editable t-weak-s">0</span></td><td><span contenteditable="" class="editable t-weak-f">0</span></td><td><span contenteditable="" class="editable p-kh">50</span></td><td><span contenteditable="" class="editable p-math">50</span></td><td><span contenteditable="" class="editable p-soc">40</span></td><td><span contenteditable="" class="editable p-sci">40</span></td><td><span contenteditable="" class="editable p-eng">0</span></td></tr>
        <tr data-grade="6"><td>6</td><td><span contenteditable="" class="editable t-good-s">0</span></td><td><span contenteditable="" class="editable t-good-f">0</span></td><td><span contenteditable="" class="editable t-mid-s">1</span></td><td><span contenteditable="" class="editable t-mid-f">1</span></td><td><span contenteditable="" class="editable t-weak-s">0</span></td><td><span contenteditable="" class="editable t-weak-f">0</span></td><td><span contenteditable="" class="editable p-kh">50</span></td><td><span contenteditable="" class="editable p-math">50</span></td><td><span contenteditable="" class="editable p-soc">40</span></td><td><span contenteditable="" class="editable p-sci">40</span></td><td><span contenteditable="" class="editable p-eng">0</span></td></tr>
        <tr style="background:#eee;font-weight:bold;">
          <td>សរុប</td>
          <td id="sum-good-s">1</td><td id="sum-good-f">1</td>
          <td id="sum-mid-s">5</td><td id="sum-mid-f">5</td>
          <td id="sum-weak-s">0</td><td id="sum-weak-f">0</td>
          <td id="avg-kh">50</td><td id="avg-math">51</td><td id="avg-soc">40</td><td id="avg-sci">41</td><td id="avg-eng">0</td>
        </tr>
      </tbody>
    </table></div>
    <p style="font-size:12px;">លក្ខណៈវិនិច្ឆ័យ ល្អ : <span contenteditable="" class="editable">មានកិច្ចតែងការ និងសម្ភារបង្រៀន</span></p>
    <p style="font-size:12px;">លក្ខណៈវិនិច្ឆ័យ មធ្យម : <span contenteditable="" class="editable">............</span></p>
    <p style="font-size:12px;">លក្ខណៈវិនិច្ឆ័យ ខ្សោយ : <span contenteditable="" class="editable">.............</span></p>

    <!-- III -->
    <h1>III. សកម្មភាពអប់រំក្រៅសាលា ក្រៅថ្នាក់</h1>
    <h2>១. ការងារសង្គម</h2>
    <p style="font-size:12px;">ខ្លឹមសារ : <span contenteditable="" class="editable">.........................................</span></p>
    <p style="font-size:12px;">លទ្ធផល : <span contenteditable="" class="editable">.........................................</span></p>
    <h2>២. ផលិតកម្ម បង្ករបង្កើនផល</h2>
    <p style="font-size:12px;">ខ្លឹមសារ : <span contenteditable="" class="editable">ដំាដំណាំចម្រុះ ដូចជា ត្រកួន ត្រប់ សណ្ដែក</span></p>
    <p style="font-size:12px;">លទ្ធផល : <span contenteditable="" class="editable">សិស្សានុសិស្ស បានប្រមូលផល</span></p>
    <h2>៣. ទស្សនកិច្ចសិក្សា</h2>
    <p style="font-size:12px;">ខ្លឹមសារ : <span contenteditable="" class="editable">........................................</span></p>
    <p style="font-size:12px;">លទ្ធផល : <span contenteditable="" class="editable">.........................................</span></p>
    <h2>៤. កីឡា</h2>
    <div class="table-container"><table><tbody>
      <tr><td>-ការប្រកួត :</td><td><span contenteditable="" class="editable">1</span></td><td>លើក</td><td>កម្រិតកម្រង : </td><td><span contenteditable="" class="editable">1</span></td><td>ដង</td><td>កម្រិតថ្នាក់ស្រុក :</td><td><span contenteditable="" class="editable">0</span></td><td>ដង</td><td>កម្រិតថ្នាក់ខេត្ត :</td><td><span contenteditable="" class="editable">0</span></td><td>ដង</td></tr>
      <tr><td>-ខ្លឹមសារ :</td><td colspan="11"><span contenteditable="" class="editable">ការប្រកួតកីឡាបាល់ទាត់ផ្នែកបុរស</span></td></tr>
      <tr><td>-លទ្ធផល :</td><td colspan="11"><span contenteditable="" class="editable">ចំណាត់ថ្នាក់លេខ២ (ចំនួនកីឡាករ និងបទពិសោធន៍)</span></td></tr>
    </tbody></table></div>
    <h2>៥. សិល្បៈ</h2>
    <div class="table-container"><table><tbody>
      <tr><td>-ការសំដែង :</td><td><span contenteditable="" class="editable">1</span></td><td>លើក</td><td>កម្រិតកម្រង : </td><td><span contenteditable="" class="editable">1</span></td><td>ដង</td><td>កម្រិតថ្នាក់ស្រុក :</td><td><span contenteditable="" class="editable">0</span></td><td>ដង</td><td>កម្រិតថ្នាក់ខេត្ត :</td><td><span contenteditable="" class="editable">0</span></td><td>ដង</td></tr>
      <tr><td>-ខ្លឹមសារ :</td><td colspan="11"><span contenteditable="" class="editable">របាំជូនពរ ក្នុងកម្មវិធី.......................</span></td></tr>
      <tr><td>-លទ្ធផល :</td><td colspan="11"><span contenteditable="" class="editable">សម្តែងបានល្អ និងចេះសាមគ្គីគ្នា</span></td></tr>
    </tbody></table></div>
    <h2>៦. អធិការកិច្ច</h2>
    <div class="table-container"><table><tbody>
      <tr><td colspan="2">-ថ្នាក់ក្រសួងចុះពិនិត្យ :</td><td><span contenteditable="" class="editable">2</span></td><td>លើក</td><td>ស្មើនិង</td><td><span contenteditable="" class="editable">10</span></td><td>ថ្នាក់</td></tr>
      <tr><td colspan="2">-មន្ទីរអប់រំចុះពិនិត្យ :</td><td><span contenteditable="" class="editable">2</span></td><td>លើក</td><td>ស្មើនិង</td><td><span contenteditable="" class="editable">10</span></td><td>ថ្នាក់</td></tr>
      <tr><td colspan="2">-រដ្ឋបាលស្រុកចុះពិនិត្យ :</td><td><span contenteditable="" class="editable">8</span></td><td>លើក</td><td>ស្មើនិង</td><td><span contenteditable="" class="editable">12</span></td><td>ថ្នាក់</td></tr>
      <tr><td colspan="2">-ថ្នាក់កម្រងចុះពិនិត្យ :</td><td><span contenteditable="" class="editable">2</span></td><td>លើក</td><td>ស្មើនិង</td><td><span contenteditable="" class="editable">12</span></td><td>ថ្នាក់</td></tr>
      <tr><td colspan="2">-ខ្លឹមសារជួយណែនាំ</td><td colspan="5"><span contenteditable="" class="editable">សូមឲ្យលោកគ្រូអ្នកគ្រូយកចិត្តទុកដាក់ក្នុងការបង្រៀន ដោយបានទៀងទាត់</span></td></tr>
    </tbody></table></div>
    <h2>៧. ការងារសហគមន៍</h2>
    <div class="table-container"><table><tbody>
      <tr><td colspan="5">-ឈ្មោះកម្រងសាលាដែលសហគមន៍បានចូលរួម :</td><td colspan="4"><span contenteditable="" class="editable">កម្រងស្ពានស្រែង</span></td></tr>
      <tr><td>-ខ្លឹមសារ :</td><td>ប្រជុំ</td><td><span contenteditable="" class="editable">ជាមួយសហគមន៍</span></td><td><span contenteditable="" class="editable">ប្រចាំខែ</span></td><td>សាងសង់</td><td><span contenteditable="" class="editable">បណ្ណាល័យ</span></td><td><span contenteditable="" class="editable">១ខ្នង</span></td><td>ផ្តល់បទពិសោធន៍</td><td><span contenteditable="" class="editable">........................................</span></td></tr>
      <tr><td>-លទ្ធផល :</td><td colspan="8"><span contenteditable="" class="editable">.............................................</span></td></tr>
    </tbody></table></div>

<!-- IV & V -->
<h1>IV. ទិសដៅឆមាសទី ២</h1>
<div class="table-container"><table><tbody>
  <tr><td><span contenteditable="" class="editable">លើកកម្ពស់អភិបាលកិច្ចសាលារៀនរួមមាន៖ ការងាររដ្ឋបាល ការងារគ្រប់គ្រងបុគ្គលិក អនុវត្តកម្មវិធីសិក្សានិងម៉ោងសិក្សា អនុវត្តវិធីសាស្រ្តបង្រៀនថ្មីៗ វាយតម្លៃការសិក្សា។</span></td></tr>
</tbody></table></div>

<h1>V. សន្និដ្ឋានៈ</h1>
<div class="table-container"><table><tbody>
  <tr><td><span contenteditable="" class="editable">ជាមួយសមិទ្ធផលនៃការអនុវត្តផែនការប្រតិបត្តិប្រចាំឆ្នាំ២០២៥ ក្នុងត្រីឆមាសទី១ សាលាបឋមសិក្សារោគ សម្រេចបាននូវលទ្ធផលសំខាន់ៗ។</span></td></tr>
</tbody></table></div>

<div id="signatureContainer" style="margin-top:30px;"></div>


  </div>


<!-- ===================== TAB 2 ===================== -->

<div id="tab2" class="tab-page">
  <div class="page-inner">
    <div class="header">ព្រះរាជាណាចក្រកម្ពុជា<br>ជាតិ សាសនា ព្រះមហាក្សត្រ<br>-------xxx-------</div>
    <div style="display:flex; justify-content:space-between; font-size:13px; margin:4px 0;">
      <div class="title">រដ្ឋបាលស្រុកភ្នំស្រុក<br>ការិយាល័យអប់រំ យុវជន និងកីឡាស្រុក<br>កម្រងស្ពានស្រែង<br>សាលាបឋមសិក្សា រោគ</div>
    </div>
    <div class="header" style="margin:6px 0;font-weight:800;">របាយការណ៍បូកសរុបលទ្ធផលការងារអប់រំ ផ្នែកបឋមសិក្សា<br>(នាឆមាសទី១ ឆ្នាំសិក្សា២០២៥-២០២៦) (ត)</div>
    <hr style="border:none;border-top:1px solid #aaa;margin:4px 0;">

    <div class="title">១. តារាងស្ថិតិសាលារៀន អគារ និងសិស្ស</div>
    <div class="table-container"><table border="1"><thead><tr><th rowspan="2">ល.រ</th><th rowspan="2">ឈ្មោះសាលា</th><th rowspan="2">អគារ</th><th colspan="3">ចំនួនបន្ទប់</th><th colspan="3">ថ្នាក់ទី១</th><th colspan="3">ថ្នាក់ទី២</th><th colspan="3">ថ្នាក់ទី៣</th><th colspan="3">ថ្នាក់ទី៤</th><th colspan="3">ថ្នាក់ទី៥</th><th colspan="3">ថ្នាក់ទី៦</th><th colspan="3">សរុបរួម</th></tr><tr><th>ប.បរ</th><th>ផ្សេងៗ</th><th>សរុប</th><th>ថ្នាក់</th><th>សរុប</th><th>ស្រី</th><th>ថ្នាក់</th><th>សរុប</th><th>ស្រី</th><th>ថ្នាក់</th><th>សរុប</th><th>ស្រី</th><th>ថ្នាក់</th><th>សរុប</th><th>ស្រី</th><th>ថ្នាក់</th><th>សរុប</th><th>ស្រី</th><th>ថ្នាក់</th><th>សរុប</th><th>ស្រី</th><th>ថ្នាក់</th><th>សរុប</th><th>ស្រី</th></tr></thead>
    <tbody><tr><td>1</td><td>សាលារោគ</td><td contenteditable="true">4</td><td contenteditable="true">12</td><td contenteditable="true">3</td><td contenteditable="true">15</td><td contenteditable="true">1</td><td contenteditable="true">30</td><td contenteditable="true">14</td><td contenteditable="true">2</td><td contenteditable="true">42</td><td contenteditable="true">21</td><td contenteditable="true">2</td><td contenteditable="true">41</td><td contenteditable="true">21</td><td contenteditable="true">2</td><td contenteditable="true">49</td><td contenteditable="true">22</td><td contenteditable="true">1</td><td contenteditable="true">50</td><td contenteditable="true">23</td><td contenteditable="true">2</td><td contenteditable="true">35</td><td contenteditable="true">17</td><td contenteditable="true">10</td><td contenteditable="true">247</td><td contenteditable="true">118</td></tr></tbody>
    </table></div>

    <div class="title">១. តារាងស្ថិតិបុគ្គលិកបង្រៀន និងមិនបង្រៀន(ត)</div>
    <div class="table-container"><table border="1"><thead><tr><th rowspan="3">ល.រ</th><th rowspan="3">ឈ្មោះសាលា</th><th colspan="4">មិនបង្រៀន</th><th colspan="10">បុគ្គលិកបង្រៀន</th><th colspan="2" rowspan="2">ក្នុងនោះ</th><th colspan="2" rowspan="2">ជួយប.រ</th><th colspan="2" rowspan="2">ក្របខ័ណ្ឌសរុប</th></tr><tr><th colspan="2">នាយក/រង</th><th colspan="2">ទីចាត់ការ</th><th colspan="2">បរ.សុទ្ធ</th><th colspan="2">គូប</th><th colspan="2">នាយករង</th><th colspan="2">កិ.ស</th><th colspan="2">សរុប</th></tr><tr><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th></tr></thead>
    <tbody><tr><td>1</td><td>សាលារោគ</td><td contenteditable="true">2</td><td contenteditable="true">1</td><td contenteditable="true">1</td><td contenteditable="true">0</td><td contenteditable="true">10</td><td contenteditable="true">9</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">4</td><td contenteditable="true">2</td><td contenteditable="true">17</td><td contenteditable="true">13</td></tr></tbody>
    </table></div>

    <div class="title">២.លទ្ធផលសិក្សា ឆមាសទី ១</div>
    <div class="table-container"><table border="1" id="t2Results">
      <thead><tr><th rowspan="3">ល.រ</th><th rowspan="3">ថ្នាក់</th><th colspan="24">សិស្សសរុបឆមាសទី១ ពីថ្នាក់ទី១ - ៦</th></tr><tr><th colspan="2">សិស្សបវេសនកាស</th><th colspan="2">សិស្សឆមាសទី១</th><th colspan="2">សិស្សចូលថ្មី</th><th colspan="2">សិស្សជាប់មធ្យម</th><th colspan="4">សិស្សធ្លាក់ (០-៤.៩៩)</th><th colspan="4">សិស្សធ្លាក់ (៤-៤.៩៩)</th><th colspan="4">សិស្សបោះបង់</th><th colspan="4">ផ្សេងៗ/សរុប</th></tr><tr><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>%</th><th>សរុប</th><th>%</th><th>សរុប</th><th>%</th><th>សរុប</th><th>%</th><th>សរុប</th><th>%</th><th>សរុប</th><th>%</th><th>សរុប</th><th>%</th><th>សរុប</th><th>%</th><th>សរុប</th><th>%</th><th>សរុប</th><th>%</th></tr></thead>
      <tbody>
        <tr><td>1</td><td>ទី១</td><td contenteditable="true">30</td><td contenteditable="true">14</td><td contenteditable="true">30</td><td contenteditable="true">14</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">30</td><td contenteditable="true">100.0%</td><td contenteditable="true">0</td><td contenteditable="true">0.0%</td><td contenteditable="true">0</td><td contenteditable="true">0.0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td></tr>
        <tr><td>2</td><td>ទី២</td><td contenteditable="true">42</td><td contenteditable="true">21</td><td contenteditable="true">42</td><td contenteditable="true">21</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">42</td><td contenteditable="true">100.0%</td><td contenteditable="true">0</td><td contenteditable="true">0.0%</td><td contenteditable="true">0</td><td contenteditable="true">0.0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td></tr>
        <tr><td>3</td><td>ទី៣</td><td contenteditable="true">42</td><td contenteditable="true">20</td><td contenteditable="true">42</td><td contenteditable="true">20</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">38</td><td contenteditable="true">90.5%</td><td contenteditable="true">3</td><td contenteditable="true">7.1%</td><td contenteditable="true">2</td><td contenteditable="true">10.0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td></tr>
        <tr><td>4</td><td>ទី៤</td><td contenteditable="true">49</td><td contenteditable="true">21</td><td contenteditable="true">49</td><td contenteditable="true">21</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">45</td><td contenteditable="true">91.8%</td><td contenteditable="true">4</td><td contenteditable="true">8.2%</td><td contenteditable="true">2</td><td contenteditable="true">9.5%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td></tr>
        <tr><td>5</td><td>ទី៥</td><td contenteditable="true">50</td><td contenteditable="true">23</td><td contenteditable="true">50</td><td contenteditable="true">23</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">40</td><td contenteditable="true">80.0%</td><td contenteditable="true">10</td><td contenteditable="true">20.0%</td><td contenteditable="true">2</td><td contenteditable="true">8.7%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td></tr>
        <tr><td>6</td><td>ទី៦</td><td contenteditable="true">35</td><td contenteditable="true">17</td><td contenteditable="true">35</td><td contenteditable="true">17</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">32</td><td contenteditable="true">91.4%</td><td contenteditable="true">3</td><td contenteditable="true">8.6%</td><td contenteditable="true">2</td><td contenteditable="true">11.8%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td><td contenteditable="true">0</td><td contenteditable="true">0%</td></tr>
        <tr><th>សរុប</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0%</th><th>0</th><th>0%</th><th>0</th><th>0%</th><th>0</th><th>0%</th><th>0</th><th>0%</th><th>0</th><th>0%</th><th>0</th><th>0%</th><th>0</th><th>0%</th><th>0</th><th>0%</th><th>0</th><th>0%</th></tr>
      </tbody>
    </table></div>

    <h3>៣.ស្ថិតិមន្រ្តីបម្រើការ</h3>
    <div class="tg-wrap"><table id="tb3" border="1"><thead><tr><th rowspan="5">ល.រ</th><th rowspan="5">ឈ្មោះសាលា</th><th colspan="16">ថ្នាក់សាលារៀន</th></tr><tr><th rowspan="4">សរុបរួម</th><th rowspan="4">ស្រី</th><th colspan="14">បុគ្គលិកទីចាត់ការ</th></tr><tr><th rowspan="3">សរុប</th><th rowspan="3">ស្រី</th><th colspan="6">នាយក</th><th colspan="6">នាយករង</th></tr><tr><th rowspan="2">សរុប</th><th rowspan="2">ស្រី</th><th colspan="2">បង្រៀន</th><th colspan="2">មិនបង្រៀន</th><th rowspan="2">សរុបរួម</th><th rowspan="2">ស្រី</th><th colspan="2">បង្រៀន</th><th colspan="2">មិនបង្រៀន</th></tr><tr><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th></tr></thead>
 <tbody><tr><td>1</td><td>បស.រោគ</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td></tr></tbody></table></div>

    <h3>៣.ស្ថិតិមន្រ្តីបម្រើការ(ត)</h3>
    <div class="tg-wrap"><table id="tb4" border="1"><thead><tr><th rowspan="5">ល.រ</th><th rowspan="5">ឈ្មោះសាលា</th><th colspan="20">ថ្នាក់សាលារៀន</th></tr><tr><th colspan="6">បុគ្គលិកទីចាត់ការ</th><th colspan="14">សិក្ខាបនធារី(គ្រូឈេថ្នាក់)</th></tr><tr><th colspan="6">មន្រ្តីទីចាត់ការ</th><th rowspan="3">សរុប</th><th rowspan="3">ស្រី</th><th colspan="6">គ្រូក្របខ័ណ្ឌ</th><th colspan="6">គ្រូក្រៅក្របខ័ណ្ឌ(ជាប់កិច្ចសន្យា)</th></tr><tr><th rowspan="2">សរុប</th><th rowspan="2">ស្រី</th><th colspan="2">បង្រៀន</th><th colspan="2">មិនបង្រៀន</th><th rowspan="2">សរុប</th><th rowspan="2">ស្រី</th><th colspan="2">បង្រៀន1ពេល1ថ្នាក់</th><th colspan="2">បង្រៀន2ពេល2ថ្នាក់</th><th rowspan="2">សរុប</th><th rowspan="2">ស្រី</th><th colspan="2">បង្រៀន1ពេល1ថ្នាក់</th><th colspan="2">បង្រៀន2ពេល2ថ្នាក់</th></tr><tr><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th></tr></thead>
      <tbody><tr><td>1</td><td>បស.រោគ</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td></tr></tbody></table></div>

    <h3>៤.កំណត់សម្គាល់អំពីតួនាទីបុគ្គលិកបង្រៀននីមួយៗ</h3>
    <div class="tg-wrap"><table id="tb5" border="1"><thead><tr><th rowspan="3">ល.រ</th><th rowspan="3">ឈ្មោះសាលា</th><th colspan="12">បុគ្គលិកទីចាត់ការ</th><th colspan="6">បុគ្គលិកជួយបង្រៀន</th><th colspan="2">ពីរពេល</th></tr><tr><th colspan="2">លេខា</th><th colspan="2">កម្មករ</th><th colspan="2">រៀនបន្ត</th><th colspan="2">អ្នកឈឺ</th><th colspan="2">ត្រៀមចូលនិវត្តន៍</th><th colspan="2">ព្យួរក្របខ័ណ្ឌ</th><th colspan="2">បណ្ណារក្ស</th><th colspan="2">កីឡា</th><th colspan="2">រោងជាង</th><th colspan="2">បណ្ណារក្ស</th></tr><tr><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th></tr></thead>
       <tbody><tr><td>1</td><td>បស.រោគ</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td></tr></tbody></table>
    <h3>៥.ស្ថិតិ សកម្មភាពបណ្ណាល័យ(1)</h3>
    <div class="tg-wrap"><table id="tb6" border="1"><thead><tr><th rowspan="3">ល.រ</th><th rowspan="3">ឈ្មោះ<br>សាលា</th><th colspan="2">ចំនួនសិស្ស</th><th colspan="5">បណ្ណាល័យ</th><th colspan="4">បណ្ណារក្ស</th><th colspan="4">សម្ភារៈ</th><th colspan="2" rowspan="3">ឈ្មោះអង្គការដែលឧបត្ថម្ភបណ្ណាល័យ</th></tr><tr><th rowspan="2">សរុប</th><th rowspan="2">ស្រី</th><th rowspan="2">បណ្ណាល័យសរុប</th><th colspan="2">បណ្ណាល័យដាច់ដោយឡែក</th><th colspan="2">បណ្ណាល័យក្នុងទីចាត់ការ</th><th colspan="2">បណ្ណារក្សបានបណ្ដុះបណ្ដាល</th><th colspan="2">បណ្ណារក្សមិនបានបណ្ដុះបណ្ដាល</th><th colspan="2" rowspan="2">សៀវភៅក្នុងបណ្ណាល័យ</th><th rowspan="2">ធ្នើរមុខ១</th><th rowspan="2">ធ្នើរមុខ២</th></tr><tr><th>ម្ចាស់ការ</th><th>ឧបត្ថម្ភ</th><th>ម្ចាស់ការ</th><th>ឧបត្ថម្ភ</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th></tr></thead>
    <tbody><tr><td>1</td><td>បស.រោគ</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td colspan="2" contenteditable="true">2136</td><td contenteditable="true">3</td><td contenteditable="true">6</td><td colspan="2" contenteditable="true">អង្គការទស្សនៈពិភពលោក</td></tr></tbody></table></div>

    <h3>៥.ស្ថិតិ សកម្មភាពបណ្ណាល័យ(2)</h3>
    <div class="tg-wrap"><table id="tb7" border="1"><thead><tr><th rowspan="3">ល.រ</th><th rowspan="3">ឈ្មោះ<br>សាលា</th><th colspan="3">គ្មានបណ្ណាល័យ</th><th colspan="3">ចំនួនបណ្ណាល័យ</th><th colspan="5">ប្រភេទបណ្ណល័យ</th><th colspan="5">ចំនួនបណ្ណារក្ស</th></tr><tr><th rowspan="2">សរុប</th><th rowspan="2">មានបន្ទប់ធ្វើបបណ្ណាល័យ</th><th rowspan="2">គ្មានបន្ទប់ធ្វើបណ្ណាល័យ</th><th rowspan="2">សរុប</th><th rowspan="2">ស្របស្តង់ដារ</th><th rowspan="2">មិនស្របស្ដង់ដារ</th><th rowspan="2">អាគារ</th><th rowspan="2">បន្ទប់</th><th rowspan="2">ក្នុងទីចាត់ការ</th><th colspan="2">បើកទ្វារ</th><th rowspan="2">សរុប</th><th rowspan="2">បានបំប៉ន</th><th rowspan="2">មិនបានបំប៉ន</th><th colspan="2">ធ្វើការ</th></tr><tr><th>១ពេល</th><th>២ពេល</th><th>១ពេល</th><th>២ពេល</th></tr></thead>
    <tbody><tr><td>1</td><td>បស.រោគ</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td></tr></tbody></table></div>

    <h3>៦.ស្ថិតិ សាលាមានការប្រើប្រាស់ បង្គន់អនាម័យ និង ទឹកស្អាត</h3>
    <div class="tg-wrap"><table id="tb9" border="1"><thead><tr><th rowspan="2">ល.រ</th><th rowspan="2">ឈ្មោះសាលា</th><th colspan="4">ចំនួនបង្គន់</th><th colspan="3">ស្រះទឹក</th><th colspan="3">អណ្ដូងលូ</th><th colspan="3">អណ្ដូងស្នប់</th><th colspan="3">អាងទឹក</th><th colspan="3">ធុងចម្រោះ</th><th rowspan="2">សេវាទឹកស្អាត</th></tr><tr><td>ចំ.ខ្នង</td><td>ចំ.បង្គន់</td><td>បានប្រើ</td><td>%</td><td>ចំនួន</td><td>បានប្រើ</td><td>%</td><td>ចំនួន</td><td>បានប្រើ</td><td>%</td><td>ចំនួន</td><td>បានប្រើ</td><td>%</td><td>ចំនួន</td><td>បានប្រើ</td><td>%</td><td>ចំនួន</td><td>បានប្រើ</td><td>%</td></tr></thead>
    <tbody><tr><td>1</td><td>បស.រោគ</td><td contenteditable="true">2</td><td contenteditable="true">2</td><td contenteditable="true">2</td><td>100%</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td>0%</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td>0%</td><td contenteditable="true">2</td><td contenteditable="true">1</td><td>50%</td><td contenteditable="true">1</td><td contenteditable="true">1</td><td>100%</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td>0%</td><td contenteditable="true">1</td></tr></tbody></table></div>

    <h3>៧.ស្ថិតិសិស្សស្នើសុំអាហារូបករណ៍ជាសាច់ប្រាក់សម្រាប់សាលាបឋមសិក្សាគោលដៅ</h3>
    <div class="tg-wrap"><table id="tb10" border="1"><thead><tr><th rowspan="2">ល.រ</th><th rowspan="2">ឈ្មោះសាលា</th><th colspan="2" rowspan="2">ឈ្មោះកម្រង</th><th colspan="2" rowspan="2">ឈ្មោះឃុំ</th><th colspan="2">ចំនួនសិស្សសរុប</th><th colspan="4">សិស្សសរុបដែលទទួលបានអាហារូបករណ៍</th><th>ផ្សេងៗ</th></tr><tr><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>%</th><th>ស្រី</th><th>%</th><th></th></tr></thead>
    <tbody><tr><td>1</td><td>រោគ</td><td colspan="2">ស្ពានស្រែង</td><td colspan="2">ស្ពានស្រែង</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td>0%</td><td contenteditable="true">0</td><td>0%</td><td contenteditable="true">0</td></tr></tbody></table></div>

    <h3>៨.ស្ថិតិសាលា ដែល​មាន​ការទម្លាក់​ព្រូន និង​មាន​ហិប​សង្រ្គោះ(1)</h3>
    <div class="tg-wrap"><table id="tb11" border="1"><thead><tr><th rowspan="3">ល.រ</th><th rowspan="3">ឈ្មោះសាលា</th><th colspan="6">ការទម្លាក់ព្រូន ជុំទី១</th><th colspan="6">ការទម្លាក់ព្រូនជុំទី២</th><th colspan="3">ហិបសង្រ្គោះទទួល</th></tr><tr><th colspan="2">សិស្សសរុប</th><th colspan="4">ចំ.សិស្សបានទម្លាក់ព្រូន</th><th colspan="2">សិស្សសរុប</th><th colspan="4">ចំ.សិស្សបានទម្លាក់ព្រូន</th><th rowspan="2">ក្រសួង</th><th rowspan="2">មន្ទីរ</th><th rowspan="2">ប្រភពផ្សេងៗ</th></tr><tr><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>%</th><th>ស្រី</th><th>%</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>%</th><th>ស្រី</th><th>%</th></tr></thead>
    <tbody><tr><td>1</td><td>បស.រោគ</td><td>0</td><td>111</td><td contenteditable="true">0</td><td>0%</td><td contenteditable="true">0</td><td>0%</td><td>0</td><td>111</td><td contenteditable="true">0</td><td>0%</td><td contenteditable="true">0</td><td>0%</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td></tr></tbody></table></div>

    <h3>៨.ស្ថិតិ សាលាបឋមសិក្សាមានសកម្មភាព កីឡា សិល្បៈ និង បំណិនជីវិត(2)</h3>
    <div class="tg-wrap"><table id="tb12" border="1"><thead><tr><th rowspan="2">ល.រ</th><th rowspan="2">ឈ្មោះសាលា</th><th colspan="2" rowspan="2">ចំនួនសាលា<br>មានកីឡា</th><th colspan="2" rowspan="2">ចំនួនគ្រូកីឡា</th><th colspan="2" rowspan="2">ចំនួនសាលា<br>មានសិល្បះ</th><th colspan="2" rowspan="2">ចំនួនគ្រូសិល្បះ</th><th colspan="2" rowspan="2">ចំនួនសាលា<br>មានរោងជាង</th><th colspan="2" rowspan="2">ចំនួន<br>គ្រូរោងជាង</th><th colspan="2" rowspan="2">ចំនួនសាលា<br>មានកសិកម្ម</th><th colspan="2" rowspan="2">ចំនួនគ្រូកសិកម្ម</th><th colspan="2" rowspan="2">ចំនួនសាលា<br>មានគេហកិច្ច</th><th colspan="2" rowspan="2">ចំនួនគ្រូ<br>គេហកិច្ច</th></tr><tr></tr></thead>
    <tbody><tr><td>1</td><td>រោគ</td><td colspan="2" contenteditable="true">0</td><td colspan="2" contenteditable="true">0</td><td colspan="2" contenteditable="true">0</td><td colspan="2" contenteditable="true">0</td><td colspan="2" contenteditable="true">0</td><td colspan="2" contenteditable="true">0</td><td colspan="2" contenteditable="true">0</td><td colspan="2" contenteditable="true">0</td><td colspan="2" contenteditable="true">0</td><td colspan="2" contenteditable="true">0</td></tr></tbody></table></div>

    <h3>៩.ស្ថិតិ សាលារៀនគោលដៅដែលបានអនុវត្ដកម្មវិធីទីប្រឹក្សាកុមារី</h3>
    <div class="tg-wrap"><table id="tb16" border="1"><thead><tr><th rowspan="2">ល.រ</th><th rowspan="2">ឈ្មោះសាលា</th><th colspan="4">ចំនួនកុមារីគោលដៅទី៤/៦</th><th colspan="8">ចំនួនកុមារីមានបញ្ហាទី៤/៦</th><th colspan="8">ចំនួនកុមារីមានបញ្ហាបានជួយ</th></tr><tr><th>ទី៤</th><th>ទី៥</th><th>ទី៦</th><th>សរុប</th><th>ទី៤</th><th>%</th><th>ទី៥</th><th>%</th><th>ទី៦</th><th>%</th><th>សរុប</th><th>%</th><th>ទី៤</th><th>%</th><th>ទី៥</th><th>%</th><th>ទី៦</th><th>%</th><th>សរុប</th><th>%</th></tr></thead>
    <tbody><tr><td>1</td><td>បស.រោគ</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td>0</td><td>0%</td><td contenteditable="true">0</td><td>0%</td><td contenteditable="true">0</td><td>0%</td><td contenteditable="true">0</td><td>0%</td><td contenteditable="true">0</td><td>0%</td><td contenteditable="true">0</td><td>0%</td><td contenteditable="true">0</td><td>0%</td></tr></tbody></table></div>

    <h3>១០.ស្ថិតិ សិស្សក្រីក្រ</h3>
    <div class="tg-wrap"><table id="tb18" border="1"><thead><tr><th rowspan="2">ល.រ</th><th rowspan="2">ថ្នាក់</th><th colspan="2">មានឪពុកម្ដាយ</th><th colspan="2">កំព្រាឪពុក</th><th colspan="2">កំព្រាម្ដាយ</th><th colspan="2">កំព្រាឪពុកម្ដាយ</th><th rowspan="2">សរុបរួម</th><th rowspan="2">ស្រី</th><th rowspan="2">ផ្សេងៗ</th></tr><tr><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th></tr></thead>
    <tbody>
      <tr><td>1</td><td>ទី១</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td>0</td><td>0</td><td contenteditable="true">0</td></tr>
      <tr><td>2</td><td>ទី២</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td>0</td><td>0</td><td contenteditable="true">0</td></tr>
      <tr><td>3</td><td>ទី៣</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td>0</td><td>0</td><td contenteditable="true">0</td></tr>
      <tr><td>4</td><td>ទី៤</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td>0</td><td>0</td><td contenteditable="true">0</td></tr>
      <tr><td>5</td><td>ទី៥</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td>0</td><td>0</td><td contenteditable="true">0</td></tr>
      <tr><td>6</td><td>ទី៦</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td>0</td><td>0</td><td contenteditable="true">0</td></tr>
      <tr><th colspan="2">សរុប</th><th id="tb18-s2">0</th><th id="tb18-f2">0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th id="tb18-tot">0</th><th id="tb18-fem">0</th><th>0</th></tr>
    </tbody></table></div>

    <h3>១១.ស្ថិតិ សិស្សពិការ</h3>
    <div class="tg-wrap"><table id="tb17" border="1"><thead><tr><th rowspan="4">ល.រ</th><th rowspan="4">ថ្នាក់</th><th colspan="18">ប្រភេទពិការ</th><th colspan="2" rowspan="3">ពិការខាង<br>ក្រៅសាលា<br>គ្រប់ប្រភេទ</th></tr><tr><th colspan="10">ពិការកាយសម្បទា</th><th colspan="2" rowspan="2">បញ្ហាសតិបញ្ញា</th><th colspan="2" rowspan="2">បញ្ហាផ្លូវចិត្ត</th><th colspan="2" rowspan="2">បញ្ហាផ្សេងៗ</th><th rowspan="3">សរុប<br>រួម</th><th rowspan="3">ស្រី</th></tr><tr><th colspan="2">បញ្ហាធ្វើចលនា</th><th colspan="2">បញ្ហាស្ដាប់</th><th colspan="2">បញ្ហានិយាយ</th><th colspan="2">បញ្ហាមើល</th><th colspan="2">បញ្ហាសរីរាងខាងក្នុង</th></tr><tr><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th><th>សរុប</th><th>ស្រី</th></tr></thead>
    <tbody>
      <tr><td>1</td><td>ទី ១</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td></tr>
      <tr><td>2</td><td>ទី ២</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td></tr>
      <tr><td>3</td><td>ទី ៣</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td></tr>
      <tr><td>4</td><td>ទី ៤</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td></tr>
      <tr><td>5</td><td>ទី ៥</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td></tr>
      <tr><td>6</td><td>ទី ៦</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td><td contenteditable="true">0</td></tr>
      <tr><th colspan="2">សរុប</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th><th>0</th></tr>
    </tbody></table></div>

    <h3>១២.ការងារសហគមន៏និងសំណូមពរ នានា</h3>
    <div class="tg-wrap"><table id="tb19" border="1"><thead><tr><th rowspan="2">ល.រ</th><th rowspan="2">ឈ្មោះសាលា</th><th colspan="4">គណះកម្មការទ្រទ្រងសាលារៀន</th></tr><tr><th>សរុប</th><th>ស្រី</th><th colspan="2">សកម្មភាពចូលរួមធ្វើអ្វីខ្លះ?</th></tr></thead>
    <tbody><tr><td>1</td><td>បស.រោគ</td><td contenteditable="true">11</td><td contenteditable="true">4</td><td colspan="2" contenteditable="true">.........................</td></tr></tbody></table></div>

    <h3>១៣.ស្ថិតិ សាលារៀនទ្រទ្រង់ និងឧប្ថម្ភរបស់អង្គការជាតិ អន្តរជាតិ បវេសនាកាល</h3>
    <div class="tg-wrap"><table id="tb20" border="1"><thead><tr><th>ល.រ</th><th>ឈ្មោះសាលា</th><th>ឈ្មោះអង្គការ រឺ កម្មវិធី</th><th>សកម្មភាព</th></tr></thead>
    <tbody><tr><td>1</td><td>បស.រោគ</td><td contenteditable="true">………….</td><td contenteditable="true">………….</td></tr><tr><td>2</td><td>បស.រោគ</td><td contenteditable="true">………….</td><td contenteditable="true">………….</td></tr></tbody></table></div>

    <h3>១៤.តារាងពិសេស</h3>
    <div class="tg-wrap"><table id="tb21" border="1"><thead><tr><th colspan="2">បញ្ជាក់សកម្មភាពផ្សេងៗ និងសំណូមពរដែលគ្មានក្នុងស្ថិតិ</th></tr></thead>
    <tbody><tr><td>ចំណុច</td><td>ការពណ៌នា</td></tr><tr><td>1</td><td contenteditable="true">………….</td></tr><tr><td>2</td><td contenteditable="true">………….</td></tr><tr><td>3</td><td contenteditable="true">………….</td></tr><tr><td>4</td><td contenteditable="true">………….</td></tr></tbody></table></div>

    <!-- SIGNATURE PAGE 2 -->
    <div id="signatureContainer2" style="margin-top:30px;"></div>

  </div><!-- /page-inner -->
</div><!-- /tab2 -->


<div id="signatureContainer2" style="margin-top:30px;"></div>


  </div>


<!-- ===================== TAB 3 ===================== -->

<div id="tab3" class="tab-page">
  <div class="page-inner">
    <div class="header">ព្រះរាជាណាចក្រកម្ពុជា<br>ជាតិ សាសនា ព្រះមហាក្សត្រ<br>-------xxx-------</div>
    <div style="display:flex; justify-content:space-between; font-size:13px; margin:4px 0;">
      <div class="title">រដ្ឋបាលស្រុកភ្នំស្រុក<br>ការិយាល័យអប់រំ យុវជន និងកីឡាស្រុក<br>កម្រងស្ពានស្រែង<br>សាលាបឋមសិក្សា រោគ</div>
    </div>
    <div class="header" style="margin:6px 0;font-weight:800;">
      បញ្ជីរាយនាមបុគ្គលិក ឆមាសទី១ ឆ្នាំសិក្សា ២០២៥ - ២០២៦
    </div>


<h1>I - បុគ្គលិកទីចាត់ការ</h1>
<div class="table-container">
<table id="officer" border="1">
  <thead><tr><th>ល.រ</th><th>នាមត្រកូល.នាម</th><th>ភេទ</th><th>ក្របខ័ណ្ឌ</th><th>កម្រិតវប្បធម៌</th><th colspan="3">មុខងារ</th><th colspan="3">លេខទូរស័ព្ទ</th><th>ផ្សេងៗ</th></tr></thead>
  <tbody>
    <tr><td class="text-center">1</td><td contenteditable="true">សុខ សារើន</td><td class="text-center" contenteditable="true">ស</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ថ្នាក់ទី១២</td><td colspan="3" contenteditable="true">នាយិកា</td><td colspan="3" contenteditable="true">0975405822</td><td contenteditable="true"></td></tr>
    <tr><td class="text-center">2</td><td contenteditable="true">យ៉េន សារី</td><td class="text-center" contenteditable="true">ប</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ថ្នាក់ទី១២</td><td colspan="3" contenteditable="true">នាយករង</td><td colspan="3" contenteditable="true">085246698</td><td contenteditable="true"></td></tr>
    <tr><td class="text-center">3</td><td contenteditable="true">អ៊ុន ប៊ុនទុង</td><td class="text-center" contenteditable="true">ប</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ស.បរិញ្ញាបត្រ</td><td colspan="3" contenteditable="true">លេខាធិការ</td><td colspan="3" contenteditable="true">017407773</td><td contenteditable="true"></td></tr>
  </tbody>
</table>
</div>

<h1>II - បុគ្គលិកបង្រៀន</h1>
<div class="table-container">
<table id="teacher" border="1">
  <thead>
    <tr><th colspan="2" rowspan="2">នាមត្រកូល.នាម</th><th rowspan="2">ភេទ</th><th rowspan="2">ក្របខ័ណ្ឌ</th><th rowspan="2">កម្រិតវប្បធម៌</th><th rowspan="2">ថ្នាក់</th><th colspan="2">ចំនួនសិស្ស</th><th colspan="2">វេន</th><th rowspan="2">លេខទូរស័ព្ទ</th><th rowspan="2">ផ្សេងៗ</th></tr>
    <tr><th>សរុប</th><th>ស្រី</th><th>ព្រឹក</th><th>ល្ងាច</th></tr>
  </thead>
  <tbody>
    <tr><td class="text-center">4</td><td contenteditable="true">រ៉ែម សុភក្ដិ</td><td class="text-center" contenteditable="true">ស</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ស.ទុតិយភូមិ</td><td class="text-center" contenteditable="true">1A</td><td class="text-center" contenteditable="true">30</td><td class="text-center" contenteditable="true">14</td><td class="text-center">√</td><td></td><td contenteditable="true">0883435566</td><td contenteditable="true"></td></tr>
    <tr><td class="text-center">5</td><td contenteditable="true">ស្វាង មនោរម្យ</td><td class="text-center" contenteditable="true">ស</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ស.បរិញ្ញាបត្រ</td><td class="text-center" contenteditable="true">5A</td><td class="text-center" contenteditable="true">25</td><td class="text-center" contenteditable="true">12</td><td class="text-center">√</td><td></td><td contenteditable="true">0976858898</td><td contenteditable="true"></td></tr>
    <tr><td class="text-center">6</td><td contenteditable="true">ប៉ោង ស្រីពេជ្រ</td><td class="text-center" contenteditable="true">ស</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ស.ទុតិយភូមិ</td><td class="text-center" contenteditable="true">2A</td><td class="text-center" contenteditable="true">21</td><td class="text-center" contenteditable="true">10</td><td class="text-center">√</td><td></td><td contenteditable="true">0889304103</td><td contenteditable="true"></td></tr>
    <tr><td class="text-center">7</td><td contenteditable="true">លេង ចាន់លាវ</td><td class="text-center" contenteditable="true">ស</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ស.ទុតិយភូមិ</td><td class="text-center" contenteditable="true">2B</td><td class="text-center" contenteditable="true">21</td><td class="text-center" contenteditable="true">10</td><td class="text-center">√</td><td></td><td contenteditable="true">0884661856</td><td contenteditable="true"></td></tr>
    <tr><td class="text-center">8</td><td contenteditable="true">អេង ផល្លែន</td><td class="text-center" contenteditable="true">ស</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ស.បរិញ្ញាបត្រ</td><td class="text-center" contenteditable="true">3B</td><td class="text-center" contenteditable="true">21</td><td class="text-center" contenteditable="true">10</td><td class="text-center">√</td><td></td><td contenteditable="true">092620771</td><td contenteditable="true"></td></tr>
    <tr><td class="text-center">9</td><td contenteditable="true">ប៊ី ពិសី</td><td class="text-center" contenteditable="true">ស</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ស.ទុតិយភូមិ</td><td class="text-center" contenteditable="true">3A</td><td class="text-center" contenteditable="true">20</td><td class="text-center" contenteditable="true">11</td><td class="text-center">√</td><td></td><td contenteditable="true">0979339499</td><td contenteditable="true"></td></tr>
    <tr><td class="text-center">10</td><td contenteditable="true">អឿន សុខៀប</td><td class="text-center" contenteditable="true">ស</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ស.បរិញ្ញាបត្រ</td><td class="text-center" contenteditable="true">4B</td><td class="text-center" contenteditable="true">24</td><td class="text-center" contenteditable="true">11</td><td class="text-center">√</td><td></td><td contenteditable="true">0974611580</td><td contenteditable="true"></td></tr>
    <tr><td class="text-center">11</td><td contenteditable="true">ឆេន សាវដា</td><td class="text-center" contenteditable="true">ស</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ស.បរិញ្ញាបត្រ</td><td class="text-center" contenteditable="true">4A</td><td class="text-center" contenteditable="true">25</td><td class="text-center" contenteditable="true">12</td><td class="text-center">√</td><td></td><td contenteditable="true">0977075979</td><td contenteditable="true"></td></tr>
    <tr><td class="text-center">12</td><td contenteditable="true">រ៉ោម សម្ផស្ស</td><td class="text-center" contenteditable="true">ប</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ស.ទុតិយភូមិ</td><td class="text-center" contenteditable="true">5B</td><td class="text-center" contenteditable="true">25</td><td class="text-center" contenteditable="true">11</td><td class="text-center">√</td><td></td><td contenteditable="true">0314234466</td><td contenteditable="true"></td></tr>
    <tr><td class="text-center">13</td><td contenteditable="true">ឈួត សេរ៉ូម</td><td class="text-center" contenteditable="true">ស</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ស.បរិញ្ញាបត្រ</td><td class="text-center" contenteditable="true">6A</td><td class="text-center" contenteditable="true">35</td><td class="text-center" contenteditable="true">17</td><td class="text-center">√</td><td></td><td contenteditable="true">0976700999</td><td contenteditable="true"></td></tr>
    <tr><td class="text-center">12</td><td contenteditable="true">រ៉ោម សម្ផស្ស</td><td class="text-center" contenteditable="true">ប</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ស.ទុតិយភូមិ</td><td class="text-center" contenteditable="true">5B</td><td class="text-center" contenteditable="true">25</td><td class="text-center" contenteditable="true">11</td><td class="text-center">√</td><td></td><td contenteditable="true">0314234466</td><td contenteditable="true"></td></tr>
    <tr><td class="text-center">13</td><td contenteditable="true">ឈួត សេរ៉ូម</td><td class="text-center" contenteditable="true">ស</td><td contenteditable="true">គ្រូបឋម</td><td contenteditable="true">ស.បរិញ្ញាបត្រ</td><td class="text-center" contenteditable="true">6A</td><td class="text-center" contenteditable="true">35</td><td class="text-center" contenteditable="true">17</td><td class="text-center">√</td><td></td><td contenteditable="true">0976700999</td><td contenteditable="true"></td></tr>
    <tr style="background:#e3eaf5;"><th colspan="6">សរុបរួម</th><th class="text-center">247</th><th class="text-center">118</th><th colspan="4"></th></tr>
  </tbody>
</table>
</div>

<div style="display:flex;justify-content:space-between;margin-top:15px;text-align:center;">
  <div style="width:50%;"><div style="font-weight:bold;">បានឃើញ និងឯកភាព</div><div style="font-weight:bold;margin-bottom:10px;">ប្រធានការិយាល័យអប់រំ</div><div style="margin-top:35px;">..........................................</div></div>
  <div style="width:50%;text-align:left;"><div>រោគ ថ្ងៃទី២៤ ខែមេសា ឆ្នាំ២០២៦</div><div style="text-align:center;font-weight:bold;margin-top:5px;">នាយិកា</div><div style="margin-top:60px;font-weight:bold;text-align:center;">សុខ សារើន</div></div>
</div>


  </div>
</div>

<!-- SCRIPTS -->

<script type="module">
  // ===== TAB SWITCHING =====
  document.querySelectorAll('.tab-nav button').forEach(btn => {
    btn.addEventListener('click', () => {
      document.querySelectorAll('.tab-nav button').forEach(b => b.classList.remove('active'));
      document.querySelectorAll('.tab-page').forEach(p => p.classList.remove('active'));
      btn.classList.add('active');
      document.getElementById(btn.dataset.tab).classList.add('active');
    });
  });

  // ===== FIREBASE SETUP =====
  const firebaseConfig = {
    apiKey: "AIzaSyC5T2ec-mxeO0lzknVe5SEBBXlp7IWmmuE",
    authDomain: "schoolreport-a7404.firebaseapp.com",
    databaseURL: "https://schoolreport-a7404-default-rtdb.asia-southeast1.firebasedatabase.app",
    projectId: "schoolreport-a7404",
    storageBucket: "schoolreport-a7404.firebasestorage.app",
    messagingSenderId: "62869703269",
    appId: "1:62869703269:web:d1a763f78eb8ae8906d48c"
  };
  if (!firebase.apps.length) firebase.initializeApp(firebaseConfig);
  const db = firebase.database();

  // ===== HELPERS =====
  function showStatus(msg, type = 'ok') {
    const st = document.getElementById('fbStatus');
    st.innerHTML = type === 'ok' ? `<span class="online-dot"></span>${msg}` : msg;
    st.className = type;
    setTimeout(() => { st.style.display = 'none'; }, 5000);
  }

  // Build a safe Firebase key from school name + year + semester
  function buildKey() {
    const name = (document.getElementById('reportName').value || 'unknown').trim()
      .replace(/\s+/g, '_').replace(/[.#$\[\]\/]/g, '-');
    const year = document.getElementById('reportYear').value;
    const sem  = document.getElementById('reportSem').value;
    return `${name}__${year}__${sem}`;
  }

  // Collect ALL editable content + selects
  function collectData() {
    const fields = {};
    document.querySelectorAll('[contenteditable="true"],[contenteditable=""]').forEach((el, i) => {
      fields[`f${i}`] = el.textContent.trim();
    });
    document.querySelectorAll('select.change-reason').forEach((el, i) => {
      fields[`sel${i}`] = el.value;
    });
    return {
      fields,
      meta: {
        reportName: document.getElementById('reportName').value.trim(),
        reportYear: document.getElementById('reportYear').value,
        reportSem:  document.getElementById('reportSem').value,
        savedAt:    new Date().toISOString()
      }
    };
  }

  // Apply saved data back to the DOM
  function applyData(data) {
    if (!data || !data.fields) return false;
    const allEditable = document.querySelectorAll('[contenteditable="true"],[contenteditable=""]');
    allEditable.forEach((el, i) => {
      if (data.fields[`f${i}`] !== undefined) el.textContent = data.fields[`f${i}`];
    });
    document.querySelectorAll('select.change-reason').forEach((el, i) => {
      if (data.fields[`sel${i}`] !== undefined) el.value = data.fields[`sel${i}`];
    });
    // Restore filter fields from meta
    if (data.meta) {
      if (data.meta.reportName) document.getElementById('reportName').value = data.meta.reportName;
      if (data.meta.reportYear) document.getElementById('reportYear').value = data.meta.reportYear;
      if (data.meta.reportSem)  document.getElementById('reportSem').value  = data.meta.reportSem;
    }
    updateAllCalculations();
    return true;
  }

  // ===== SAVE =====
  document.getElementById('btnSave').addEventListener('click', async () => {
    const key = buildKey();
    const payload = collectData();
    showStatus('⏳ កំពុងរក្សាទុក...', 'info');
    try {
      await db.ref(`reports/${key}`).set(payload);
      showStatus(`✅ បានរក្សាទុក: ${key}`, 'ok');
    } catch(e) {
      showStatus(`❌ ${e.message}`, 'err');
    }
  });

  // ===== LOAD CURRENT =====
  document.getElementById('btnLoadCurrent').addEventListener('click', async () => {
    const key = buildKey();
    showStatus(`⏳ កំពុងហៅ: ${key}...`, 'info');
    try {
      const snap = await db.ref(`reports/${key}`).once('value');
      const data = snap.val();
      if (!data) {
        showStatus(`⚠️ រកមិនឃើញ: ${key}`, 'err');
        return;
      }
      const ok = applyData(data);
      showStatus(ok ? `✅ បានហៅ: ${key}` : '❌ ទិន្នន័យមិនត្រឹមត្រូវ', ok ? 'ok' : 'err');
    } catch(e) {
      showStatus(`❌ ${e.message}`, 'err');
    }
  });

  // ===== LIST ALL REPORTS =====
  document.getElementById('btnList').addEventListener('click', async () => {
    document.getElementById('modalOverlay').classList.add('open');
    document.getElementById('reportList').innerHTML = '<div class="empty-msg">⏳ កំពុងផ្ទុកបញ្ជី...</div>';
    try {
      const snap = await db.ref('reports').once('value');
      const all = snap.val();
      if (!all || Object.keys(all).length === 0) {
        document.getElementById('reportList').innerHTML = '<div class="empty-msg">📭 មិនទាន់មានរបាយការណ៍ណាមួយ</div>';
        return;
      }
      const keys = Object.keys(all).sort();
      let html = '';
      keys.forEach(key => {
        const meta = all[key]?.meta || {};
        const savedAt = meta.savedAt ? new Date(meta.savedAt).toLocaleString('km-KH') : 'មិនដឹង';
        const displayName = meta.reportName || key;
        const year = meta.reportYear || '';
        const sem  = meta.reportSem  || '';
        html += `
          <div class="report-item">
            <div>
              <div class="ri-name">🏫 ${displayName}</div>
              <div class="ri-time">📅 ${year} · ${sem} · ${savedAt}</div>
            </div>
            <div class="ri-btns">
              <button class="ri-btn-load" data-key="${key}">📥 ហៅ</button>
              <button class="ri-btn-del"  data-key="${key}">🗑️ លុប</button>
            </div>
          </div>`;
      });
      document.getElementById('reportList').innerHTML = html;

      // Load button handlers
      document.querySelectorAll('.ri-btn-load').forEach(btn => {
        btn.addEventListener('click', async () => {
          const k = btn.dataset.key;
          document.getElementById('modalOverlay').classList.remove('open');
          showStatus(`⏳ កំពុងហៅ: ${k}...`, 'info');
          const s = await db.ref(`reports/${k}`).once('value');
          const d = s.val();
          const ok = applyData(d);
          showStatus(ok ? `✅ បានហៅ: ${k}` : '❌ ទិន្នន័យខ្សោយ', ok ? 'ok' : 'err');
        });
      });

      // Delete button handlers
      document.querySelectorAll('.ri-btn-del').forEach(btn => {
        btn.addEventListener('click', async () => {
          const k = btn.dataset.key;
          if (!confirm(`⚠️ តើអ្នកចង់លុប "${k}" ពិតមែនទេ?`)) return;
          await db.ref(`reports/${k}`).remove();
          btn.closest('.report-item').remove();
          if (!document.querySelector('.report-item'))
            document.getElementById('reportList').innerHTML = '<div class="empty-msg">📭 មិនទាន់មានរបាយការណ៍ណាមួយ</div>';
        });
      });

    } catch(e) {
      document.getElementById('reportList').innerHTML = `<div class="empty-msg">❌ ${e.message}</div>`;
    }
  });

  document.getElementById('modalClose').addEventListener('click', () => {
    document.getElementById('modalOverlay').classList.remove('open');
  });
  document.getElementById('modalOverlay').addEventListener('click', (e) => {
    if (e.target === document.getElementById('modalOverlay'))
      document.getElementById('modalOverlay').classList.remove('open');
  });

  // ===== PRINT / XLSX / JSON =====
  document.getElementById('btnPrint').addEventListener('click', () => window.print());

  document.getElementById('btnXlsx').addEventListener('click', () => {
    const wb = XLSX.utils.book_new();
    document.querySelectorAll('table').forEach((tbl, idx) => {
      const ws = XLSX.utils.table_to_sheet(tbl);
      XLSX.utils.book_append_sheet(wb, ws, `Table_${idx+1}`);
    });
    XLSX.writeFile(wb, `Educational_Report_${buildKey()}.xlsx`);
  });

  document.getElementById('btnJson').addEventListener('click', () => {
    const data = collectData();
    const blob = new Blob([JSON.stringify(data, null, 2)], { type: 'application/json' });
    const a = document.createElement('a');
    a.href = URL.createObjectURL(blob);
    a.download = `${buildKey()}.json`;
    a.click();
  });

  // ===== CALCULATIONS =====
  const getVal = el => el ? (parseInt(el.textContent.replace(/[^0-9]/g, '')) || 0) : 0;

  function updateAllCalculations() {
    let totalS = 0, totalF = 0;
    for (let g = 1; g <= 6; g++) {
      totalS += getVal(document.querySelector(`.grade-total[data-grade="${g}"]`));
      totalF += getVal(document.querySelector(`.grade-female[data-grade="${g}"]`));
    }
    document.getElementById('totalStudents').textContent = totalS;
    document.getElementById('totalFemale').textContent = totalF;

    let sumS=0, sumF=0, sumPass=0, sumFPass=0, sumFail=0, sumFFail=0;
    for (let g = 1; g <= 6; g++) {
      const s = getVal(document.querySelector(`.grade-total[data-grade="${g}"]`));
      const f = getVal(document.querySelector(`.grade-female[data-grade="${g}"]`));
      const pS = getVal(document.querySelector(`.r-pass${g}`));
      const pF = getVal(document.querySelector(`.r-fpas${g}`));
      const fS = getVal(document.querySelector(`.r-fail${g}`));
      const fF = getVal(document.querySelector(`.r-ffai${g}`));
      const pctRows = document.querySelectorAll('#pctTable tbody tr');
      const row = pctRows[g-1];
      if (row) {
        row.cells[1].textContent = s > 0 ? Math.round(pS/s*100)+'%' : '0%';
        row.cells[2].textContent = f > 0 ? Math.round(pF/f*100)+'%' : '0%';
        row.cells[3].textContent = s > 0 ? (fS/s*100).toFixed(2)+'%' : '0.00%';
        row.cells[4].textContent = f > 0 ? (fF/f*100).toFixed(2)+'%' : '0.00%';
      }
      sumS+=s; sumF+=f; sumPass+=pS; sumFPass+=pF; sumFail+=fS; sumFFail+=fF;
    }
    const set = (id, v) => { const el = document.getElementById(id); if (el) el.textContent = v; };
    set('rTotalS', sumS); set('rTotalF', sumF);
    set('rTotalS2', sumS); set('rTotalF2', sumF);
    set('rTotalPass', sumPass); set('rTotalFPass', sumFPass);
    set('rTotalFail', sumFail); set('rTotalFFail', sumFFail);

    const totalPctRow = document.querySelectorAll('#pctTable tbody tr')[6];
    if (totalPctRow) {
      totalPctRow.cells[1].textContent = sumS > 0 ? Math.round(sumPass/sumS*100)+'%' : '0%';
      totalPctRow.cells[2].textContent = sumF > 0 ? Math.round(sumFPass/sumF*100)+'%' : '0%';
      totalPctRow.cells[3].textContent = sumS > 0 ? (sumFail/sumS*100).toFixed(2)+'%' : '0.00%';
      totalPctRow.cells[4].textContent = sumF > 0 ? (sumFFail/sumF*100).toFixed(2)+'%' : '0.00%';
    }

    // Sync tab2 totals
    set('t2sum1', sumS); set('t2sum2', sumF);
    set('t2sum3', sumS); set('t2sum4', sumF);
    set('t2sumPass', sumPass);
    set('t2sumPassPct', sumS > 0 ? Math.round(sumPass/sumS*100)+'%' : '0%');
    set('t2sumFail', sumFail);
    set('t2sumFailPct', sumS > 0 ? Math.round(sumFail/sumS*100)+'%' : '0%');
    set('t2sumFailF', sumFFail);
    set('t2sumFailFPct', sumF > 0 ? Math.round(sumFFail/sumF*100)+'%' : '0%');
  }

  // Inc/Dec buttons
  document.querySelectorAll('.btn-inc, .btn-dec').forEach(btn => {
    btn.addEventListener('click', function() {
      const grade = this.dataset.grade;
      const el    = document.querySelector(`.grade-total[data-grade="${grade}"]`);
      const chgEl = document.querySelector(`.change-count[data-grade="${grade}"]`);
      let val = getVal(el), chg = getVal(chgEl);
      if (this.classList.contains('btn-inc')) { val++; chg++; }
      else if (val > 0) { val--; chg++; }
      el.textContent  = val;
      chgEl.textContent = chg;
      updateAllCalculations();
    });
  });

  document.addEventListener('input', e => {
    if (e.target.matches('[contenteditable]')) updateAllCalculations();
  });

  // ===== SIGNATURES =====
  function renderSignatures() {
    const d = new Date();
    const months = ['មករា','កុម្ភៈ','មីនា','មេសា','ឧសភា','មិថុនា','កក្កដា','សីហា','កញ្ញា','តុលា','វិច្ឆិកា','ធ្នូ'];
    const kn = n => String(n).replace(/\d/g, c => '០១២៣៤៥៦៧៨៩'[+c]);
    const solar = `រោគ ថ្ងៃទី${kn(d.getDate())} ខែ${months[d.getMonth()]} ឆ្នាំ${kn(d.getFullYear())}`;
    const html = `
      <div style="display:flex;justify-content:space-between;margin-top:30px;text-align:center;">
        <div style="width:50%;"><div style="font-weight:bold;">បានឃើញ និងឯកភាព</div><div style="font-weight:bold;margin-bottom:10px;">ប្រធានការិយាល័យអប់រំ យុវជន និងកីឡា</div><div style="margin-top:35px;">..........................................</div></div>
        <div style="width:50%;text-align:left;"><div>${solar}</div><div style="text-align:center;font-weight:bold;margin-top:5px;">អ្នកធ្វើរបាយការណ៍</div><div style="text-align:center;margin-top:60px;font-weight:bold;">អ៊ុន ប៊ុនទុង</div></div>
      </div>`;
    ['signatureContainer','signatureContainer2'].forEach(id => {
      const el = document.getElementById(id);
      if (el) el.innerHTML = html;
    });
  }

  // ===== AUTO-LOAD on start =====
  window.addEventListener('DOMContentLoaded', async () => {
    renderSignatures();
    updateAllCalculations();

    // Try to load the default key on startup
    try {
      const key = buildKey();
      const snap = await db.ref(`reports/${key}`).once('value');
      const data = snap.val();
      if (data) {
        applyData(data);
        showStatus(`✅ បានផ្ទុក: ${key}`, 'ok');
      }
    } catch(e) {
      // silent – first time use
    }
  });
 </script>

 </template>

</template>
<template id="tpl-dataclass">
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=0.85">
<title>Teacher Data Management</title>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Khmer:wght@300;400;500;600;700&amp;family=Manrope:wght@400;500;600;700;800&amp;display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf-autotable/3.5.28/jspdf.plugin.autotable.min.js"></script>
<style>
:root{
  --navy:#0d2b4e; --navy2:#1a4271; --navy3:#2e6da4;
  --gold:#f0a500; --gold2:#fbbf24;
  --green:#166534; --green2:#16a34a;
  --red:#991b1b; --red2:#dc2626;
  --bg:#edf2f9; --surface:#fff;
  --border:#dde4ee; --text:#1e2a3b; --muted:#6b7a8d;
  --font:'Manrope','Noto Sans Khmer',sans-serif;
}
*{box-sizing:border-box;margin:0;padding:0}
html,body{height:100%;font-family:var(--font);background:var(--bg);color:var(--text);font-size:14px}

/* ── HEADER ──────────────────────────────────────────────────── */
.hdr{background:linear-gradient(135deg,var(--navy) 0%,#193762 50%,#0d2b4e 100%);
  color:#fff;padding:14px 22px;display:flex;align-items:center;justify-content:space-between;
  gap:12px;flex-wrap:wrap;box-shadow:0 4px 18px rgba(0,0,0,.35);position:relative;z-index:20}
.hdr-title{display:flex;align-items:center;gap:10px}
.hdr-title i{color:var(--gold);font-size:1.5rem}
.hdr-title h1{font-size:1.15rem;font-weight:800;letter-spacing:-.02em}
.hdr-title p{font-size:.75rem;opacity:.7;margin-top:1px}

/* export buttons */
.export-bar{display:flex;gap:6px;flex-wrap:wrap}
.ebtn{display:inline-flex;align-items:center;gap:5px;padding:7px 13px;border:none;border-radius:7px;
  font-size:.78rem;font-weight:700;cursor:pointer;transition:.18s;font-family:var(--font);white-space:nowrap;letter-spacing:.02em}
.ebtn:hover{transform:translateY(-2px);box-shadow:0 6px 18px rgba(0,0,0,.25)}
.ebtn-xlsx {background:#166534;color:#fff}
.ebtn-json {background:#b45309;color:#fff}
.ebtn-pdf  {background:#9b1c1c;color:#fff}
.ebtn-html {background:#5b21b6;color:#fff}
.ebtn-print{background:#374151;color:#fff}

/* ── TOOLBAR ──────────────────────────────────────────────────── */
.toolbar{display:flex;align-items:center;justify-content:space-between;
  padding:12px 18px;border-bottom:1px solid var(--border);background:#f5f8fc;
  flex-wrap:wrap;gap:10px}
.srch{position:relative}
.srch i{position:absolute;left:10px;top:50%;transform:translateY(-50%);color:var(--muted);font-size:.8rem}
.srch input{padding:7px 12px 7px 32px;border:1.5px solid var(--border);border-radius:8px;
  font:inherit;font-size:.82rem;outline:none;width:220px;transition:.15s}
.srch input:focus{border-color:var(--navy);box-shadow:0 0 0 3px rgba(13,43,78,.1)}
.rpp{display:flex;align-items:center;gap:7px;font-size:.82rem;color:var(--muted)}
.rpp select{border:1.5px solid var(--border);border-radius:6px;padding:5px 10px;font:inherit;font-size:.82rem;outline:none;background:#fff}
.record-badge{background:var(--navy);color:#fff;padding:3px 10px;border-radius:99px;font-size:.75rem;font-weight:700}

/* ── CARD ─────────────────────────────────────────────────────── */
.wrap{padding:18px}
.card{background:var(--surface);border-radius:14px;box-shadow:0 2px 16px rgba(0,0,0,.07);overflow:hidden}

/* ── TABLE ────────────────────────────────────────────────────── */
.tbl-scroll{overflow:auto;max-height:64vh}
table{border-collapse:collapse;width:100%}
thead th{padding:7px 8px;text-align:center;border:1px solid #3b6fa5;
  white-space:nowrap;position:sticky;z-index:10;font-size:.72rem}
.th-row1 th{background:var(--navy);color:#fff;font-weight:700;top:0}
.th-row2 th{background:#1a4f8a;color:#cfe2ff;font-weight:600;font-size:.7rem;top:33px}
.th-act{background:var(--navy)!important;color:#fff!important}
.th-s1{background:#1e4d8c!important}
.th-s2{background:#1a5c38!important}
.th-s1-sub{background:#2563eb!important;color:#fff!important}
.th-s2-sub{background:#16a34a!important;color:#fff!important}
tbody td{padding:5px 7px;text-align:center;border:1px solid #e4eaf3;
  white-space:nowrap;font-size:.75rem;transition:.1s}
tbody tr:hover td{background:#eff6ff!important}
tbody tr:nth-child(even) td{background:#f7faff}
.val-zero{color:#c8d4e8}
.val-num{font-variant-numeric:tabular-nums}

/* action buttons */
.ab{padding:3px 9px;border:none;border-radius:4px;cursor:pointer;font-size:.72rem;
  font-weight:700;transition:.15s;font-family:var(--font)}
.ab-edit{background:#3b82f6;color:#fff;margin-right:3px}
.ab-edit:hover{background:#2563eb}
.ab-del{background:#ef4444;color:#fff}
.ab-del:hover{background:#dc2626}

/* ── PAGINATION ───────────────────────────────────────────────── */
.pager{display:flex;align-items:center;justify-content:space-between;
  padding:11px 18px;border-top:1px solid var(--border);background:#f5f8fc;
  flex-wrap:wrap;gap:10px;font-size:.8rem;color:var(--muted)}
.pg-btns{display:flex;gap:4px}
.pg-btn{padding:4px 11px;border:1.5px solid var(--border);background:#fff;
  border-radius:6px;cursor:pointer;font-size:.78rem;font-family:var(--font);transition:.15s}
.pg-btn:hover,.pg-btn.on{background:var(--navy);color:#fff;border-color:var(--navy)}
.pg-btn:disabled{opacity:.4;cursor:default}

/* ── LOADING ──────────────────────────────────────────────────── */
#loading{position:fixed;inset:0;background:linear-gradient(135deg,rgba(13,43,78,.92),rgba(26,66,113,.88));
  display:flex;flex-direction:column;align-items:center;justify-content:center;z-index:999;gap:18px;color:#fff}
.spin{width:48px;height:48px;border:5px solid rgba(255,255,255,.25);
  border-top-color:var(--gold);border-radius:50%;animation:sp .7s linear infinite}
@keyframes sp{to{transform:rotate(360deg)}}
.loading-text{font-size:.95rem;opacity:.9}

/* ── MODAL ────────────────────────────────────────────────────── */
.mbdp{position:fixed;inset:0;background:rgba(0,0,0,.55);z-index:600;
  display:none;align-items:center;justify-content:center;padding:20px}
.mbdp.show{display:flex}
.modal{background:#fff;border-radius:16px;width:100%;max-width:860px;
  max-height:92vh;display:flex;flex-direction:column;
  box-shadow:0 24px 64px rgba(0,0,0,.35);animation:min .22s ease}
@keyframes min{from{transform:translateY(24px);opacity:0}to{transform:none;opacity:1}}
.mhdr{background:linear-gradient(135deg,var(--navy),#1a4271);color:#fff;
  padding:16px 22px;border-radius:16px 16px 0 0;display:flex;align-items:center;justify-content:space-between}
.mhdr h2{font-size:1rem;font-weight:800;display:flex;align-items:center;gap:9px}
.mhdr h2 i{color:var(--gold)}
.mclose{background:none;border:none;color:#fff;font-size:1.1rem;cursor:pointer;
  padding:5px 9px;border-radius:5px;transition:.15s}
.mclose:hover{background:rgba(255,255,255,.2)}
/* tabs */
.mtabs{display:flex;padding:0 22px;background:#f0f4fa;border-bottom:2px solid var(--border)}
.mtab{padding:10px 18px;cursor:pointer;font-size:.83rem;font-weight:700;color:var(--muted);
  border-bottom:2.5px solid transparent;margin-bottom:-2px;transition:.15s;
  font-family:'Noto Sans Khmer','Manrope',sans-serif}
.mtab:hover{color:var(--navy)}
.mtab.on{color:var(--navy);border-bottom-color:var(--navy)}
/* modal body */
.mbody{flex:1;overflow-y:auto;padding:20px 22px}
.tab-pane{display:none}
.tab-pane.on{display:block}
.fsec{margin-bottom:22px}
.fsec-title{font-size:.72rem;font-weight:800;text-transform:uppercase;letter-spacing:.06em;
  color:var(--navy2);border-bottom:2px solid #dbeafe;padding-bottom:5px;margin-bottom:12px;
  font-family:'Noto Sans Khmer','Manrope',sans-serif}
.fgrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(130px,1fr));gap:10px}
.ff{display:flex;flex-direction:column;gap:4px}
.ff label{font-size:.71rem;font-weight:700;color:var(--muted);font-family:'Noto Sans Khmer','Manrope',sans-serif}
.ff input{padding:7px 10px;border:1.5px solid var(--border);border-radius:7px;
  font:inherit;font-size:.82rem;outline:none;transition:.15s;background:#fafcff}
.ff input:focus{border-color:var(--navy);background:#fff;box-shadow:0 0 0 3px rgba(13,43,78,.08)}
/* modal footer */
.mfoot{padding:14px 22px;border-top:1px solid var(--border);background:#f5f8fc;
  border-radius:0 0 16px 16px;display:flex;justify-content:flex-end;gap:10px}
.btn-cancel{background:#fff;color:var(--muted);border:1.5px solid var(--border);
  padding:8px 20px;border-radius:7px;cursor:pointer;font:inherit;font-weight:700;font-size:.83rem}
.btn-save{background:var(--navy);color:#fff;border:none;padding:8px 24px;
  border-radius:7px;cursor:pointer;font:inherit;font-weight:700;font-size:.83rem;transition:.15s}
.btn-save:hover{background:var(--navy2)}

/* ── TOAST ────────────────────────────────────────────────────── */
.toast{position:fixed;bottom:22px;right:22px;padding:11px 18px;border-radius:10px;
  font-size:.83rem;z-index:9999;animation:tin .25s ease;display:flex;align-items:center;gap:9px;
  box-shadow:0 8px 24px rgba(0,0,0,.25);color:#fff;font-weight:600;font-family:var(--font)}
.toast.ok{background:#1e3a1e;border-left:4px solid #22c55e}
.toast.err{background:#3b1111;border-left:4px solid #ef4444}
@keyframes tin{from{transform:translateX(110%);opacity:0}to{transform:none;opacity:1}}

/* ── EMPTY STATE ──────────────────────────────────────────────── */
.empty{padding:56px 0;text-align:center;color:var(--muted)}
.empty i{font-size:3rem;opacity:.25;margin-bottom:12px;display:block}

/* ── PRINT ────────────────────────────────────────────────────── */
@media print{
  .hdr .export-bar,.toolbar,.pager,.ab,.mbdp{display:none!important}
  .hdr{background:var(--navy)!important;-webkit-print-color-adjust:exact;print-color-adjust:exact}
  .wrap{padding:0}.card{box-shadow:none;border-radius:0}
  .tbl-scroll{max-height:none;overflow:visible}
  body{background:#fff}
  table{font-size:7px}
  thead th{-webkit-print-color-adjust:exact;print-color-adjust:exact}
}
</style>
<!-- Loading -->
<div id="loading">
  <div class="spin"></div>
  <p class="loading-text">⏳ ...</p>
</div>

<!-- Header -->
<header class="hdr">
  <div class="hdr-title">
    <i class="fas fa-graduation-cap"></i>
    <div>
      <h1>Teacher Data Management</h1>
      <p>ប្រព័ន្ធគ្រប់គ្រងទិន្នន័យបុគ្គលិក</p>
    </div>
  </div>
  <div class="export-bar">
    <button class="ebtn ebtn-xlsx" id="btnXLSX"><i class="fas fa-file-excel"></i> XLSX</button>
    <button class="ebtn ebtn-json" id="btnJSON"><i class="fas fa-code"></i> JSON</button>
    <button class="ebtn ebtn-pdf" id="btnPDF"><i class="fas fa-file-pdf"></i> PDF</button>
    <button class="ebtn ebtn-html" id="btnHTML"><i class="fab fa-html5"></i> HTML</button>
    <button class="ebtn ebtn-print" id="btnPrint"><i class="fas fa-print"></i> Print</button>
  </div>
</header>
<!-- Main -->
<div class="wrap">
  <div class="card">
    <!-- Toolbar -->
    <div class="toolbar">
      <div class="rpp">
        <span>ចំនួនជួរ:</span>
        <select id="rpp">
          <option>50</option><option>25</option><option selected="">10</option>
          <option>100</option><option value="999999">ទាំងអស់</option>
        </select>
        <span class="record-badge" id="totalBadge">0 records</span>
      </div>
      <div class="srch">
        <i class="fas fa-search"></i>
        <input id="srchBox" type="text" placeholder="ស្វែងរក / Search…">
      </div>
    </div>

    <!-- Table -->
    <div class="tbl-scroll" id="tblWrap">
      <table>
        <thead id="thead"></thead>
        <tbody id="tbody"></tbody>
      </table>
    </div>

    <!-- Pagination -->
    <div class="pager">
      <span id="pgInfo"></span>
      <div class="pg-btns" id="pgBtns"></div>
    </div>
  </div>
</div>
<!-- Edit Modal -->
<div class="mbdp" id="editModal">
  <div class="modal" onclick="event.stopPropagation()">
    <div class="mhdr">
      <h2><i class="fas fa-user-pen"></i> Edit Teacher Record</h2>
      <button class="mclose" onclick="closeModal()"><i class="fas fa-xmark"></i></button>
    </div>
    <div class="mtabs">
      <div class="mtab on" data-tab="0">ព័ត៌មានទូទៅ</div>
      <div class="mtab" data-tab="1">ឆមាស ១</div>
      <div class="mtab" data-tab="2">ឆមាស ២</div>
    </div>
    <div class="mbody" id="mBody"></div>
    <div class="mfoot">
      <button class="btn-cancel" onclick="closeModal()"><i class="fas fa-xmark"></i> បោះបង់</button>
      <button class="btn-save" onclick="saveRecord()"><i class="fas fa-floppy-disk"></i> រក្សាទុក</button>
    </div>
  </div>
</div>

<!-- ─── Firebase + Logic ──────────────────────────────────────── -->
<script type="module">
import { initializeApp }                       from "https://www.gstatic.com/firebasejs/9.22.1/firebase-app.js";
import { getDatabase, ref, onValue, set, remove } from "https://www.gstatic.com/firebasejs/9.22.1/firebase-database.js";

const app = initializeApp({
  apiKey:"AIzaSyB35WLr1y5_QT3j-0x7Mb2F7QaaYXLdIcQ",
  authDomain:"packagedemo-b600c.firebaseapp.com",
  databaseURL:"https://packagedemo-b600c-default-rtdb.asia-southeast1.firebasedatabase.app",
  projectId:"packagedemo-b600c",
  storageBucket:"packagedemo-b600c.firebasestorage.app",
  messagingSenderId:"601958630212",
  appId:"1:601958630212:web:e140ee683e203f3e464d11"
});
const db = getDatabase(app);

// ── Column definitions ──────────────────────────────────────────
const COLS = [
  // Fixed / basic (rowspan 2)
  {k:'year',                    lbl:'Years',        fix:true, type:'text'},
  {k:'schoolCode',              lbl:'School Code',  fix:true, type:'text'},
  {k:'schoolName',              lbl:'School Name',  fix:true, type:'text'},
  {k:'position',                lbl:'Position',     fix:true, type:'text'},
  {k:'teacherId',               lbl:'Teacher ID',   fix:true, type:'text'},
  {k:'teacherName',             lbl:'Teacher Name', fix:true, type:'text'},
  {k:'grade',                   lbl:'Grade',        fix:true, type:'text'},
  {k:'studentTotal',            lbl:'Student Total',fix:true, type:'number'},
  {k:'female',                  lbl:'Female',       fix:true, type:'number'},
  // ── Semester 1 ──
  {k:'s1_students_total',       lbl:'សរុប', g:'s1a', gL:'សិស្សឆមាស១',            sem:1,type:'number'},
  {k:'s1_students_female',      lbl:'ស្រី',  g:'s1a', gL:'សិស្សឆមាស១',            sem:1,type:'number'},
  {k:'s1_enrollment_total',     lbl:'សរុប', g:'s1b', gL:'សិស្សបវេសនកាល',           sem:1,type:'number'},
  {k:'s1_enrollment_female',    lbl:'ស្រី',  g:'s1b', gL:'សិស្សបវេសនកាល',           sem:1,type:'number'},
  {k:'s1_change_total',         lbl:'សរុប', g:'s1c', gL:'សិស្សប្រែប្រួល',           sem:1,type:'number'},
  {k:'s1_change_female',        lbl:'ស្រី',  g:'s1c', gL:'សិស្សប្រែប្រួល',           sem:1,type:'number'},
  {k:'s1_passAvg_total',        lbl:'សរុប', g:'s1d', gL:'សិស្សជាប់មធ្យមភាគ',        sem:1,type:'number'},
  {k:'s1_passAvg_female',       lbl:'ស្រី',  g:'s1d', gL:'សិស្សជាប់មធ្យមភាគ',        sem:1,type:'number'},
  {k:'s1_fail0to499_total',     lbl:'សរុប', g:'s1e', gL:'ធ្លាក់(0-4.99)',           sem:1,type:'number'},
  {k:'s1_fail0to499_female',    lbl:'ស្រី',  g:'s1e', gL:'ធ្លាក់(0-4.99)',           sem:1,type:'number'},
  {k:'s1_fail4to499_total',     lbl:'សរុប', g:'s1f', gL:'ធ្លាក់(4-4.99)',           sem:1,type:'number'},
  {k:'s1_fail4to499_female',    lbl:'ស្រី',  g:'s1f', gL:'ធ្លាក់(4-4.99)',           sem:1,type:'number'},
  {k:'s1_dropout_total',        lbl:'សរុប', g:'s1g', gL:'សិស្សបោះបង់',             sem:1,type:'number'},
  {k:'s1_dropout_female',       lbl:'ស្រី',  g:'s1g', gL:'សិស្សបោះបង់',             sem:1,type:'number'},
  {k:'s1_curriculum_khmer',     lbl:'%ខ្មែរ',   g:'s1h', gL:'ការអនុវត្ត',            sem:1,type:'number'},
  {k:'s1_curriculum_math',      lbl:'%គណិត',     g:'s1h', gL:'ការអនុវត្ត',            sem:1,type:'number'},
  {k:'s1_curriculum_science',   lbl:'%វិទ្យា',    g:'s1h', gL:'ការអនុវត្ត',            sem:1,type:'number'},
  {k:'s1_curriculum_social',    lbl:'%សង្គម',     g:'s1h', gL:'ការអនុវត្ត',            sem:1,type:'number'},
  {k:'s1_curriculum_foreign',   lbl:'%បរទេស',     g:'s1h', gL:'ការអនុវត្ត',            sem:1,type:'number'},
  {k:'s1_lessonPlan_signed',    lbl:'ចុះHT',  g:'s1i', gL:'កិច្ចតែងការ',            sem:1,type:'number'},
  {k:'s1_lessonPlan_unsigned',  lbl:'មិនចុះ', g:'s1i', gL:'កិច្ចតែងការ',            sem:1,type:'number'},
  {k:'s1_jan_abc', lbl:'ABC',   g:'s1_jan', gL:'មករា',   sem:1,type:'number'},
  {k:'s1_jan_def', lbl:'DEF',   g:'s1_jan', gL:'មករា',   sem:1,type:'number'},
  {k:'s1_feb_abc', lbl:'ABC',   g:'s1_feb', gL:'កុម្ភៈ',  sem:1,type:'number'},
  {k:'s1_feb_def', lbl:'DEF',   g:'s1_feb', gL:'កុម្ភៈ',  sem:1,type:'number'},
  {k:'s1_mar_abc', lbl:'ABC',   g:'s1_mar', gL:'មីនា',   sem:1,type:'number'},
  {k:'s1_mar_def', lbl:'DEF',   g:'s1_mar', gL:'មីនា',   sem:1,type:'number'},
  {k:'s1_apr_abc', lbl:'ABC',   g:'s1_apr', gL:'មេសា',   sem:1,type:'number'},
  {k:'s1_apr_def', lbl:'DEF',   g:'s1_apr', gL:'មេសា',   sem:1,type:'number'},
  // ── Semester 2 ──
  {k:'s2_students_total',       lbl:'សរុប', g:'s2a', gL:'សិស្សឆមាស២',             sem:2,type:'number'},
  {k:'s2_students_female',      lbl:'ស្រី',  g:'s2a', gL:'សិស្សឆមាស២',             sem:2,type:'number'},
  {k:'s2_sem1_total',           lbl:'សរុប', g:'s2b', gL:'សិស្សឆមាស១',             sem:2,type:'number'},
  {k:'s2_sem1_female',          lbl:'ស្រី',  g:'s2b', gL:'សិស្សឆមាស១',             sem:2,type:'number'},
  {k:'s2_change_total',         lbl:'សរុប', g:'s2c', gL:'សិស្សប្រែប្រួល',          sem:2,type:'number'},
  {k:'s2_change_female',        lbl:'ស្រី',  g:'s2c', gL:'សិស្សប្រែប្រួល',          sem:2,type:'number'},
  {k:'s2_passAvg_total',        lbl:'សរុប', g:'s2d', gL:'សិស្សជាប់មធ្យមភាគ',       sem:2,type:'number'},
  {k:'s2_passAvg_female',       lbl:'ស្រី',  g:'s2d', gL:'សិស្សជាប់មធ្យមភាគ',       sem:2,type:'number'},
  {k:'s2_fail0to499_total',     lbl:'សរុប', g:'s2e', gL:'ធ្លាក់(0-4.99)',          sem:2,type:'number'},
  {k:'s2_fail0to499_female',    lbl:'ស្រី',  g:'s2e', gL:'ធ្លាក់(0-4.99)',          sem:2,type:'number'},
  {k:'s2_fail4to499_total',     lbl:'សរុប', g:'s2f', gL:'ធ្លាក់(4-4.99)',          sem:2,type:'number'},
  {k:'s2_fail4to499_female',    lbl:'ស្រី',  g:'s2f', gL:'ធ្លាក់(4-4.99)',          sem:2,type:'number'},
  {k:'s2_dropout_total',        lbl:'សរុប', g:'s2g', gL:'សិស្សបោះបង់',             sem:2,type:'number'},
  {k:'s2_dropout_female',       lbl:'ស្រី',  g:'s2g', gL:'សិស្សបោះបង់',             sem:2,type:'number'},
  {k:'s2_curriculum_khmer',     lbl:'%ខ្មែរ',   g:'s2h', gL:'ការអនុវត្ត',            sem:2,type:'number'},
  {k:'s2_curriculum_math',      lbl:'%គណិត',     g:'s2h', gL:'ការអនុវត្ត',            sem:2,type:'number'},
  {k:'s2_curriculum_science',   lbl:'%វិទ្យា',    g:'s2h', gL:'ការអនុវត្ត',            sem:2,type:'number'},
  {k:'s2_curriculum_social',    lbl:'%សង្គម',     g:'s2h', gL:'ការអនុវត្ត',            sem:2,type:'number'},
  {k:'s2_curriculum_foreign',   lbl:'%បរទេស',     g:'s2h', gL:'ការអនុវត្ត',            sem:2,type:'number'},
  {k:'s2_lessonPlan_signed',    lbl:'ចុះHT',  g:'s2i', gL:'កិច្ចតែងការ',            sem:2,type:'number'},
  {k:'s2_lessonPlan_unsigned',  lbl:'មិនចុះ', g:'s2i', gL:'កិច្ចតែងការ',            sem:2,type:'number'},
  {k:'s2_may_abc', lbl:'ABC',   g:'s2_may', gL:'ឧសភា',   sem:2,type:'number'},
  {k:'s2_may_def', lbl:'DEF',   g:'s2_may', gL:'ឧសភា',   sem:2,type:'number'},
  {k:'s2_jun_abc', lbl:'ABC',   g:'s2_jun', gL:'មិថុនា',  sem:2,type:'number'},
  {k:'s2_jun_def', lbl:'DEF',   g:'s2_jun', gL:'មិថុនា',  sem:2,type:'number'},
  {k:'s2_jul_abc', lbl:'ABC',   g:'s2_jul', gL:'កក្កដា',  sem:2,type:'number'},
  {k:'s2_jul_def', lbl:'DEF',   g:'s2_jul', gL:'កក្កដា',  sem:2,type:'number'},
  {k:'s2_aug_abc', lbl:'ABC',   g:'s2_aug', gL:'សីហា',    sem:2,type:'number'},
  {k:'s2_aug_def', lbl:'DEF',   g:'s2_aug', gL:'សីហា',    sem:2,type:'number'},
  {k:'s2_sep_abc', lbl:'ABC',   g:'s2_sep', gL:'កញ្ញា',   sem:2,type:'number'},
  {k:'s2_sep_def', lbl:'DEF',   g:'s2_sep', gL:'កញ្ញា',   sem:2,type:'number'},
];

// ── State ───────────────────────────────────────────────────────
let allData    = [];  // full dataset from Firebase
let filtered   = [];  // after search
let curPage    = 1;
let editRecord = null;

// ── Build table header ──────────────────────────────────────────
function buildHeader(){
  const thead = document.getElementById('thead');
  const fixedCols = COLS.filter(c=>c.fix);
  const varCols   = COLS.filter(c=>!c.fix);

  // Row 1 - group headers
  let r1='<tr class="th-row1">';
  r1+=`<th rowspan="2" class="th-act" style="min-width:90px">Actions</th>`;
  fixedCols.forEach(c=>{
    const w = c.k==='schoolName'?140 : c.k==='teacherName'?120 : 80;
    r1+=`<th rowspan="2" style="min-width:${w}px">${c.lbl}</th>`;
  });

  const seen=new Set();
  varCols.forEach(c=>{
    if(seen.has(c.g))return;
    seen.add(c.g);
    const cnt=varCols.filter(x=>x.g===c.g).length;
    const cls=c.sem===1?'th-s1':'th-s2';
    r1+=`<th colspan="${cnt}" class="${cls}" style="min-width:${cnt*58}px">${c.gL}</th>`;
  });
  r1+='</tr>';

  // Row 2 - sub headers
  let r2='<tr class="th-row2">';
  varCols.forEach(c=>{
    const cls=c.sem===1?'th-s1-sub':'th-s2-sub';
    r2+=`<th class="${cls}" style="min-width:50px">${c.lbl}</th>`;
  });
  r2+='</tr>';

  thead.innerHTML=r1+r2;
}

// ── Render table rows ───────────────────────────────────────────
function renderTable(){
  const q   = document.getElementById('srchBox').value.toLowerCase().trim();
  const rpp = parseInt(document.getElementById('rpp').value)||50;

  filtered = q
    ? allData.filter(r=>
        COLS.slice(0,6).some(c=>String(r[c.k]||'').toLowerCase().includes(q))
      )
    : [...allData];

  document.getElementById('totalBadge').textContent = `${filtered.length} records`;

  const totalPages = Math.max(1,Math.ceil(filtered.length/rpp));
  if(curPage>totalPages) curPage=totalPages;

  const start=(curPage-1)*rpp;
  const slice=filtered.slice(start,start+rpp);

  const tbody=document.getElementById('tbody');

  if(!slice.length){
    tbody.innerHTML=`<tr><td colspan="${COLS.length+1}" style="padding:48px;text-align:center;color:var(--muted)">
      <div style="font-size:2.5rem;opacity:.2;margin-bottom:10px">📭</div>
      <p>មិនមានទិន្នន័យ / No records found</p>
    </td></tr>`;
  } else {
    tbody.innerHTML=slice.map((r,i)=>{
      const cells=COLS.map(c=>{
        const v=r[c.k]??'';
        if(v===''||v==='-'||v===0||v==='0')
          return `<td class="val-zero val-num">-</td>`;
        return `<td class="val-num">${v}</td>`;
      }).join('');
      return `<tr>
        <td>
          <button class="ab ab-edit" onclick="openEdit(${start+i})"><i class="fas fa-pen"></i> Edit</button>
          <button class="ab ab-del"  onclick="deleteRec(${start+i})"><i class="fas fa-trash"></i></button>
        </td>
        ${cells}
      </tr>`;
    }).join('');
  }

  // Pagination
  document.getElementById('pgInfo').textContent =
    `បង្ហាញ ${start+1}–${Math.min(start+rpp,filtered.length)} នៃ ${filtered.length} កំណត់ត្រា`;

  const pgBtns=document.getElementById('pgBtns');
  let btns='';
  btns+=`<button class="pg-btn" onclick="goPage(${curPage-1})" ${curPage===1?'disabled':''}>‹</button>`;
  const range=pageRange(curPage,totalPages);
  range.forEach(p=>{
    if(p==='…') btns+=`<span class="pg-btn" style="cursor:default">…</span>`;
    else btns+=`<button class="pg-btn ${p===curPage?'on':''}" onclick="goPage(${p})">${p}</button>`;
  });
  btns+=`<button class="pg-btn" onclick="goPage(${curPage+1})" ${curPage===totalPages?'disabled':''}>›</button>`;
  pgBtns.innerHTML=btns;
}

function pageRange(cur,total){
  if(total<=7)return Array.from({length:total},(_,i)=>i+1);
  if(cur<=4) return [1,2,3,4,5,'…',total];
  if(cur>=total-3) return [1,'…',total-4,total-3,total-2,total-1,total];
  return [1,'…',cur-1,cur,cur+1,'…',total];
}

function goPage(p){
  const rpp=parseInt(document.getElementById('rpp').value)||50;
  const total=Math.ceil(filtered.length/rpp);
  if(p<1||p>total)return;
  curPage=p;
  renderTable();
}

// ── Edit modal ──────────────────────────────────────────────────
function openEdit(idx){
  editRecord={...filtered[idx]};

  // Build tabs content
  const basicCols = COLS.filter(c=>c.fix);
  const s1Cols    = COLS.filter(c=>c.sem===1);
  const s2Cols    = COLS.filter(c=>c.sem===2);

  function fields(cols){
    return cols.map(c=>`
      <div class="ff">
        <label>${c.lbl} <small style="opacity:.6">[${c.k}]</small></label>
        <input id="f_${c.k}" type="${c.type==='number'?'number':'text'}" value="${editRecord[c.k]??''}">
      </div>`).join('');
  }

  function groupedFields(cols){
    // group by gL
    const groups={};
    cols.forEach(c=>{
      const g=c.gL||c.g||'other';
      if(!groups[g])groups[g]=[];
      groups[g].push(c);
    });
    return Object.entries(groups).map(([g,cs])=>`
      <div class="fsec">
        <div class="fsec-title">${g}</div>
        <div class="fgrid">${fields(cs)}</div>
      </div>`).join('');
  }

  document.getElementById('mBody').innerHTML=`
    <div class="tab-pane on" data-tp="0">
      <div class="fsec">
        <div class="fsec-title">ព័ត៌មានទូទៅ / Basic Information</div>
        <div class="fgrid">${fields(basicCols)}</div>
      </div>
    </div>
    <div class="tab-pane" data-tp="1">${groupedFields(s1Cols)}</div>
    <div class="tab-pane" data-tp="2">${groupedFields(s2Cols)}</div>
  `;

  // reset tabs to first
  switchTab(0);
  document.getElementById('editModal').classList.add('show');
}

function closeModal(){
  document.getElementById('editModal').classList.remove('show');
  editRecord=null;
}

function switchTab(i){
  document.querySelectorAll('.mtab').forEach((t,j)=>t.classList.toggle('on',j===i));
  const mBody=document.getElementById('mBody');
  mBody.querySelectorAll('.tab-pane').forEach(p=>p.classList.remove('on'));
  mBody.querySelectorAll('.tab-pane')[i]?.classList.add('on');
}

async function saveRecord(){
  if(!editRecord)return;
  // collect all field values
  COLS.forEach(c=>{
    const el=document.getElementById('f_'+c.k);
    if(!el)return;
    editRecord[c.k]=c.type==='number'?(parseFloat(el.value)||0):el.value;
  });
  const key=String(editRecord.teacherId).replace(/[.#$/\[\]]/g,'_');
  try{
    await set(ref(db,`teacherData/${key}`),editRecord);
    toast('✓ រក្សាទុករួចរាល់!','ok');
    closeModal();
  }catch(e){
    toast('✗ កំហុស: '+e.message,'err');
  }
}

async function deleteRec(idx){
  const r=filtered[idx];
  if(!confirm(`Delete teacher "${r.teacherName}" (ID: ${r.teacherId})?`))return;
  const key=String(r.teacherId).replace(/[.#$/\[\]]/g,'_');
  try{
    await remove(ref(db,`teacherData/${key}`));
    toast('✓ លុបរួចរាល់!','ok');
  }catch(e){
    toast('✗ កំហុស: '+e.message,'err');
  }
}

// ── Exports ─────────────────────────────────────────────────────
function exportXLSX(){
  const header=COLS.map(c=>c.lbl);
  const rows=filtered.map(r=>COLS.map(c=>r[c.k]??''));
  const ws=XLSX.utils.aoa_to_sheet([header,...rows]);
  // column widths
  ws['!cols']=COLS.map(c=>({wch:c.fix?Math.max(c.lbl.length,14):9}));
  const wb=XLSX.utils.book_new();
  XLSX.utils.book_append_sheet(wb,ws,'TeacherData');
  XLSX.writeFile(wb,'teacher_data.xlsx');
  toast('✓ XLSX downloaded','ok');
}

function exportJSON(){
  const blob=new Blob([JSON.stringify(filtered,null,2)],{type:'application/json'});
  dl(blob,'teacher_data.json');
  toast('✓ JSON downloaded','ok');
}

function exportHTML(){
  const thRow1=()=>{
    let r='<tr>';
    r+=`<th rowspan="2">Actions?</th>`;
    COLS.filter(c=>c.fix).forEach(c=>{r+=`<th rowspan="2">${c.lbl}</th>`});
    const seen=new Set();
    COLS.filter(c=>!c.fix).forEach(c=>{
      if(seen.has(c.g))return;
      seen.add(c.g);
      const cnt=COLS.filter(x=>x.g===c.g).length;
      r+=`<th colspan="${cnt}">${c.gL}</th>`;
    });
    return r+'</tr>';
  };
  const thRow2=()=>{
    let r='<tr>';
    COLS.filter(c=>!c.fix).forEach(c=>{r+=`<th>${c.lbl}</th>`});
    return r+'</tr>';
  };
  const tbRows=filtered.map(r=>{
    const cells=COLS.map(c=>`<td>${r[c.k]??'-'}</td>`).join('');
    return `<tr><td>-</td>${cells}</tr>`;
  }).join('\n');

  const html=`<!DOCTYPE html><html lang="km"><head><meta charset="UTF-8">
<title>Teacher Data Export</title>
<style>
body{font-family:sans-serif;font-size:11px}
table{border-collapse:collapse;width:100%}
th,td{border:1px solid #999;padding:4px 6px;text-align:center;white-space:nowrap}
th{background:#0d2b4e;color:#fff}
tr:nth-child(even) td{background:#f0f4ff}
</style></head><body>
<h2 style="font-size:14px">Teacher Data — Exported ${new Date().toLocaleDateString()}</h2>
<table><thead>${thRow1()}${thRow2()}</thead><tbody>${tbRows}</tbody></table>
</body></html>`;

  dl(new Blob([html],{type:'text/html'}),'teacher_data_export.html');
  toast('✓ HTML downloaded','ok');
}

function exportPDF(){
  const {jsPDF}=window.jspdf;
  const doc=new jsPDF({orientation:'landscape',unit:'mm',format:'a4'});
  const basic=COLS.filter(c=>c.fix);
  const s1=COLS.filter(c=>c.sem===1);
  const s2=COLS.filter(c=>c.sem===2);

  function addTable(title,cols,pageNum){
    if(pageNum>0) doc.addPage();
    doc.setFont('helvetica','bold');
    doc.setFontSize(11);
    doc.setTextColor(13,43,78);
    doc.text(`Teacher Data — ${title}   (${filtered.length} records)`,14,13);
    doc.setFontSize(8);
    doc.setTextColor(100);
    doc.text(`Exported: ${new Date().toLocaleString()}`,14,19);

    const head=[cols.map(c=>c.lbl)];
    const body=filtered.map(r=>cols.map(c=>String(r[c.k]??'-')));

    doc.autoTable({
      head,body,startY:23,
      styles:{fontSize:6.5,cellPadding:1.5,halign:'center'},
      headStyles:{fillColor:[13,43,78],textColor:255,fontStyle:'bold'},
      alternateRowStyles:{fillColor:[240,246,255]},
      margin:{left:14,right:14},
      tableWidth:'auto',
    });
  }

  // Page 1: Basic info
  addTable('Basic Information',basic,0);
  // Page 2: S1 (id + name + s1 cols)
  addTable('Semester 1',[...basic.slice(0,6),...s1],1);
  // Page 3: S2
  addTable('Semester 2',[...basic.slice(0,6),...s2],2);

  doc.save('teacher_data.pdf');
  toast('✓ PDF downloaded (3 pages)','ok');
}

function dl(blob,name){
  const a=document.createElement('a');
  a.href=URL.createObjectURL(blob);
  a.download=name;a.click();
  URL.revokeObjectURL(a.href);
}

function toast(msg,type='ok'){
  const t=document.createElement('div');
  t.className=`toast ${type}`;
  t.innerHTML=`<i class="fas fa-${type==='ok'?'check':'circle-xmark'}"></i> ${msg}`;
  document.body.appendChild(t);
  setTimeout(()=>t.remove(),3500);
}

// ── Wire up UI events ───────────────────────────────────────────
document.getElementById('srchBox').addEventListener('input',()=>{curPage=1;renderTable()});
document.getElementById('rpp').addEventListener('change',()=>{curPage=1;renderTable()});
document.getElementById('btnXLSX') .addEventListener('click',exportXLSX);
document.getElementById('btnJSON') .addEventListener('click',exportJSON);
document.getElementById('btnPDF')  .addEventListener('click',exportPDF);
document.getElementById('btnHTML') .addEventListener('click',exportHTML);
document.getElementById('btnPrint').addEventListener('click',()=>window.print());
document.getElementById('editModal').addEventListener('click',e=>{
  if(e.target===e.currentTarget) closeModal();
});
document.querySelectorAll('.mtab').forEach((t,i)=>{
  t.addEventListener('click',()=>switchTab(i));
});
document.addEventListener('keydown',e=>{if(e.key==='Escape')closeModal()});

// expose to onclick attributes
window.openEdit    = openEdit;
window.deleteRec   = deleteRec;
window.closeModal  = closeModal;
window.saveRecord  = saveRecord;
window.switchTab   = switchTab;
window.goPage      = goPage;

// ── Firebase listener ───────────────────────────────────────────
buildHeader();

onValue(ref(db,'teacherData'),(snap)=>{
  document.getElementById('loading').style.display='none';
  const val=snap.val();
  if(!val){ allData=[];renderTable();return; }
  allData=Object.values(val);
  curPage=1;
  renderTable();
});

</script>
</template>
        </div><!-- /dashboard-body -->
    </div><!-- /dashboard-overlay -->

    <!-- ══════════════ NAVIGATION ══════════════ -->
    <nav class="bg-white shadow-lg fixed w-full z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <div class="flex items-center">
                    <i class="fas fa-graduation-cap text-2xl text-primary mr-2"></i>
                    <span class="text-xl font-bold text-dark">Rauk Primary School</span>
                </div>
                <div class="hidden md:flex items-center space-x-6">
                    <button onclick="scrollToSection('home')" class="nav-link text-dark font-medium">Home</button>
                    <button onclick="scrollToSection('about')" class="nav-link text-dark font-medium">About</button>
                    <button onclick="scrollToSection('programs')" class="nav-link text-dark font-medium">Programs</button>
                    <button onclick="scrollToSection('admissions')" class="nav-link text-dark font-medium">Admissions</button>
                    <button onclick="scrollToSection('contact')" class="nav-link text-dark font-medium">Contact</button>
                    <button onclick="openDashboard()" class="bg-amber-500 hover:bg-amber-600 text-white px-4 py-2 rounded-full font-medium flex items-center gap-2 transition">
                        <i class="fas fa-chart-line text-sm"></i> Dashboard
                    </button>
                    <button class="btn-primary text-white px-4 py-2 rounded-full font-medium">Apply Now</button>
                </div>
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-button" class="text-dark"><i class="fas fa-bars text-xl"></i></button>
                </div>
            </div>
        </div>
        <div id="mobile-menu" class="hidden md:hidden bg-white">
            <div class="px-2 pt-2 pb-3 space-y-1">
                <button onclick="scrollToSection('home')" class="block px-3 py-2 rounded-md text-base font-medium text-dark hover:bg-gray-100 w-full text-left">Home</button>
                <button onclick="scrollToSection('about')" class="block px-3 py-2 rounded-md text-base font-medium text-dark hover:bg-gray-100 w-full text-left">About</button>
                <button onclick="scrollToSection('programs')" class="block px-3 py-2 rounded-md text-base font-medium text-dark hover:bg-gray-100 w-full text-left">Programs</button>
                <button onclick="scrollToSection('admissions')" class="block px-3 py-2 rounded-md text-base font-medium text-dark hover:bg-gray-100 w-full text-left">Admissions</button>
                <button onclick="scrollToSection('contact')" class="block px-3 py-2 rounded-md text-base font-medium text-dark hover:bg-gray-100 w-full text-left">Contact</button>
                <button onclick="openDashboard()" class="block px-3 py-2 rounded-md text-base font-medium text-amber-600 hover:bg-gray-100 w-full text-left">📊 Dashboard</button>
                <button class="btn-primary text-white px-4 py-2 rounded-full font-medium w-full mt-2">Apply Now</button>
            </div>
        </div>
    </nav>

    <!-- ══════════════ HERO ══════════════ -->
    <section id="home" class="hero-bg h-screen flex items-center justify-center">
        <div class="text-center px-4">
            <h1 class="text-4xl md:text-6xl font-bold text-white mb-6 fade-in">Welcome to Rauk Primary School</h1>
            <p class="text-xl md:text-2xl text-gray-200 mb-8 fade-in">Excellence in Education for Future Leaders</p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center fade-in">
                <button onclick="scrollToSection('admissions')" class="btn-primary text-white px-8 py-3 rounded-full font-semibold text-lg">Apply Now</button>
                <button onclick="openDashboard()" class="bg-amber-500 hover:bg-amber-600 text-white px-8 py-3 rounded-full font-semibold text-lg transition flex items-center gap-2 justify-center">
                    <i class="fas fa-chart-line"></i> Open Dashboard
                </button>
                <button onclick="scrollToSection('about')" class="border-2 border-white text-white px-8 py-3 rounded-full font-semibold text-lg hover:bg-white hover:text-dark transition">Learn More</button>
            </div>
        </div>
    </section>

    <!-- ══════════════ ABOUT ══════════════ -->
    <section id="about" class="py-20 bg-light">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-dark mb-4">About Our School</h2>
                <div class="w-20 h-1 bg-secondary mx-auto"></div>
            </div>
            <div class="flex flex-col md:flex-row items-center gap-12">
                <div class="md:w-1/2">
                    <img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='500' height='400' viewBox='0 0 500 400'><rect width='500' height='400' fill='%231e40af'/><circle cx='250' cy='200' r='100' fill='%23f59e0b'/><rect x='150' y='150' width='200' height='100' fill='%23ef4444'/></svg>" alt="School" class="rounded-lg shadow-xl w-full">
                </div>
                <div class="md:w-1/2">
                    <h3 class="text-2xl font-bold text-dark mb-4">Creating Tomorrow's Leaders Today</h3>
                    <p class="text-gray-600 mb-6 leading-relaxed">Rauk Primary School is dedicated to providing quality education that nurtures the intellectual, emotional, and physical development of every student. Our experienced faculty and modern curriculum prepare students for success in a rapidly changing world.</p>
                    <p class="text-gray-600 mb-8 leading-relaxed">Founded with a vision to provide holistic education, we combine traditional academic excellence with innovative teaching methods to ensure each child reaches their full potential.</p>
                    <div class="grid grid-cols-2 gap-4">
                        <div class="flex items-center"><i class="fas fa-check-circle text-secondary text-xl mr-2"></i><span class="text-dark font-medium">Experienced Teachers</span></div>
                        <div class="flex items-center"><i class="fas fa-check-circle text-secondary text-xl mr-2"></i><span class="text-dark font-medium">Modern Facilities</span></div>
                        <div class="flex items-center"><i class="fas fa-check-circle text-secondary text-xl mr-2"></i><span class="text-dark font-medium">Safe Environment</span></div>
                        <div class="flex items-center"><i class="fas fa-check-circle text-secondary text-xl mr-2"></i><span class="text-dark font-medium">Comprehensive Programs</span></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ══════════════ PROGRAMS ══════════════ -->
    <section id="programs" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-dark mb-4">Our Academic Programs</h2>
                <p class="text-gray-600 max-w-2xl mx-auto">We offer a comprehensive curriculum designed to develop critical thinking, creativity, and leadership skills.</p>
                <div class="w-20 h-1 bg-secondary mx-auto mt-4"></div>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="feature-card bg-white p-8 rounded-xl shadow-lg border border-gray-100 transition-all duration-300">
                    <div class="text-secondary text-4xl mb-4"><i class="fas fa-book-open"></i></div>
                    <h3 class="text-xl font-bold text-dark mb-3">Core Curriculum</h3>
                    <p class="text-gray-600 mb-4">Foundation subjects including Mathematics, Science, English, and Social Studies.</p>
                    <ul class="space-y-2">
                        <li class="flex items-center text-sm text-gray-600"><i class="fas fa-circle text-xs text-primary mr-2"></i>Interactive Learning</li>
                        <li class="flex items-center text-sm text-gray-600"><i class="fas fa-circle text-xs text-primary mr-2"></i>Hands-on Activities</li>
                        <li class="flex items-center text-sm text-gray-600"><i class="fas fa-circle text-xs text-primary mr-2"></i>Regular Assessments</li>
                    </ul>
                </div>
                <div class="feature-card bg-white p-8 rounded-xl shadow-lg border border-gray-100 transition-all duration-300">
                    <div class="text-secondary text-4xl mb-4"><i class="fas fa-paint-brush"></i></div>
                    <h3 class="text-xl font-bold text-dark mb-3">Arts &amp; Crafts</h3>
                    <p class="text-gray-600 mb-4">Creative expression through visual arts, music, drama, and creative writing.</p>
                    <ul class="space-y-2">
                        <li class="flex items-center text-sm text-gray-600"><i class="fas fa-circle text-xs text-primary mr-2"></i>Visual Arts</li>
                        <li class="flex items-center text-sm text-gray-600"><i class="fas fa-circle text-xs text-primary mr-2"></i>Music Programs</li>
                        <li class="flex items-center text-sm text-gray-600"><i class="fas fa-circle text-xs text-primary mr-2"></i>Drama Club</li>
                    </ul>
                </div>
                <div class="feature-card bg-white p-8 rounded-xl shadow-lg border border-gray-100 transition-all duration-300">
                    <div class="text-secondary text-4xl mb-4"><i class="fas fa-running"></i></div>
                    <h3 class="text-xl font-bold text-dark mb-3">Physical Education</h3>
                    <p class="text-gray-600 mb-4">Sports activities and fitness programs to promote physical health and teamwork.</p>
                    <ul class="space-y-2">
                        <li class="flex items-center text-sm text-gray-600"><i class="fas fa-circle text-xs text-primary mr-2"></i>Team Sports</li>
                        <li class="flex items-center text-sm text-gray-600"><i class="fas fa-circle text-xs text-primary mr-2"></i>Individual Fitness</li>
                        <li class="flex items-center text-sm text-gray-600"><i class="fas fa-circle text-xs text-primary mr-2"></i>Outdoor Education</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- ══════════════ ADMISSIONS ══════════════ -->
    <section id="admissions" class="py-20 bg-light">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-dark mb-4">Admissions Process</h2>
                <p class="text-gray-600 max-w-2xl mx-auto">We're excited to welcome new students to our school community</p>
                <div class="w-20 h-1 bg-secondary mx-auto mt-4"></div>
            </div>
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div>
                    <h3 class="text-2xl font-bold text-dark mb-6">How to Apply</h3>
                    <div class="space-y-6">
                        <div class="flex"><div class="flex-shrink-0"><div class="flex items-center justify-center h-12 w-12 rounded-full bg-primary text-white font-bold">1</div></div><div class="ml-4"><h4 class="text-lg font-semibold text-dark">Application Form</h4><p class="text-gray-600">Complete our online application form with basic student information.</p></div></div>
                        <div class="flex"><div class="flex-shrink-0"><div class="flex items-center justify-center h-12 w-12 rounded-full bg-primary text-white font-bold">2</div></div><div class="ml-4"><h4 class="text-lg font-semibold text-dark">Document Submission</h4><p class="text-gray-600">Submit required documents including birth certificate and school reports.</p></div></div>
                        <div class="flex"><div class="flex-shrink-0"><div class="flex items-center justify-center h-12 w-12 rounded-full bg-primary text-white font-bold">3</div></div><div class="ml-4"><h4 class="text-lg font-semibold text-dark">Admission Interview</h4><p class="text-gray-600">Short interview with parent and student to assess fit and goals.</p></div></div>
                        <div class="flex"><div class="flex-shrink-0"><div class="flex items-center justify-center h-12 w-12 rounded-full bg-primary text-white font-bold">4</div></div><div class="ml-4"><h4 class="text-lg font-semibold text-dark">Enrollment</h4><p class="text-gray-600">Receive confirmation and complete enrollment procedures.</p></div></div>
                    </div>
                    <button onclick="scrollToSection('contact')" class="mt-8 btn-primary text-white px-8 py-3 rounded-full font-semibold">Contact Us for Details</button>
                </div>
                <div class="bg-white p-8 rounded-xl shadow-lg">
                    <h3 class="text-2xl font-bold text-dark mb-6">Important Dates</h3>
                    <div class="space-y-4">
                        <div class="flex justify-between border-b pb-3"><span class="font-medium text-dark">Application Deadline</span><span class="text-gray-600">June 30, 2026</span></div>
                        <div class="flex justify-between border-b pb-3"><span class="font-medium text-dark">Admission Interviews</span><span class="text-gray-600">July 1–15, 2026</span></div>
                        <div class="flex justify-between border-b pb-3"><span class="font-medium text-dark">Enrollment Period</span><span class="text-gray-600">July 20–30, 2026</span></div>
                        <div class="flex justify-between"><span class="font-medium text-dark">Academic Year Begins</span><span class="text-gray-600">September 1, 2026</span></div>
                    </div>
                    <div class="mt-8 p-6 bg-blue-50 rounded-lg">
                        <h4 class="font-semibold text-dark mb-2">Need Help?</h4>
                        <p class="text-gray-600 text-sm mb-4">Have questions about admissions? Our team is ready to assist you.</p>
                        <button onclick="scrollToSection('contact')" class="text-primary font-medium flex items-center">Contact Admissions Team <i class="fas fa-arrow-right ml-2 text-sm"></i></button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ══════════════ CONTACT ══════════════ -->
    <section id="contact" class="py-20 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-dark mb-4">Get In Touch</h2>
                <p class="text-gray-600 max-w-2xl mx-auto">We'd love to hear from you. Reach out with any questions.</p>
                <div class="w-20 h-1 bg-secondary mx-auto mt-4"></div>
            </div>
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                <div>
                    <form class="space-y-6">
                        <div><label class="block text-gray-700 font-medium mb-2">Full Name</label><input type="text" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary focus:border-transparent"></div>
                        <div><label class="block text-gray-700 font-medium mb-2">Email Address</label><input type="email" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary focus:border-transparent"></div>
                        <div><label class="block text-gray-700 font-medium mb-2">Phone Number</label><input type="tel" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary focus:border-transparent"></div>
                        <div><label class="block text-gray-700 font-medium mb-2">Message</label><textarea rows="5" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary focus:border-transparent"></textarea></div>
                        <button type="submit" class="btn-primary text-white px-8 py-3 rounded-full font-semibold w-full">Send Message</button>
                    </form>
                </div>
                <div class="bg-light p-8 rounded-xl">
                    <h3 class="text-2xl font-bold text-dark mb-6">Contact Information</h3>
                    <div class="space-y-6">
                        <div class="flex"><div class="flex-shrink-0"><div class="flex items-center justify-center h-12 w-12 rounded-full bg-primary text-white"><i class="fas fa-map-marker-alt"></i></div></div><div class="ml-4"><h4 class="text-lg font-semibold text-dark">Our Location</h4><p class="text-gray-600">ស្ពានស្រែង · ភ្នំស្រុក · ព្រះវិហារ</p></div></div>
                        <div class="flex"><div class="flex-shrink-0"><div class="flex items-center justify-center h-12 w-12 rounded-full bg-primary text-white"><i class="fas fa-phone-alt"></i></div></div><div class="ml-4"><h4 class="text-lg font-semibold text-dark">Phone Number</h4><p class="text-gray-600">+855 12 345 678</p></div></div>
                        <div class="flex"><div class="flex-shrink-0"><div class="flex items-center justify-center h-12 w-12 rounded-full bg-primary text-white"><i class="fas fa-envelope"></i></div></div><div class="ml-4"><h4 class="text-lg font-semibold text-dark">Email Address</h4><p class="text-gray-600">info@raukprimary.edu.kh</p></div></div>
                        <div class="flex"><div class="flex-shrink-0"><div class="flex items-center justify-center h-12 w-12 rounded-full bg-primary text-white"><i class="fas fa-clock"></i></div></div><div class="ml-4"><h4 class="text-lg font-semibold text-dark">Working Hours</h4><p class="text-gray-600">Mon–Fri: 7:00 AM – 4:00 PM</p></div></div>
                    </div>
                    <div class="mt-8">
                        <h4 class="text-lg font-semibold text-dark mb-4">Follow Us</h4>
                        <div class="flex space-x-4">
                            <a href="#" class="bg-primary text-white p-3 rounded-full hover:bg-secondary transition"><i class="fab fa-facebook-f"></i></a>
                            <a href="#" class="bg-primary text-white p-3 rounded-full hover:bg-secondary transition"><i class="fab fa-twitter"></i></a>
                            <a href="#" class="bg-primary text-white p-3 rounded-full hover:bg-secondary transition"><i class="fab fa-instagram"></i></a>
                            <a href="#" class="bg-primary text-white p-3 rounded-full hover:bg-secondary transition"><i class="fab fa-youtube"></i></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ══════════════ FOOTER ══════════════ -->
    <footer class="bg-dark text-white py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <div class="flex items-center mb-4"><i class="fas fa-graduation-cap text-2xl text-secondary mr-2"></i><span class="text-xl font-bold">Rauk Primary School</span></div>
                    <p class="text-gray-400 mb-4">Providing quality education to nurture future leaders.</p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-secondary transition"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" class="text-gray-400 hover:text-secondary transition"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="text-gray-400 hover:text-secondary transition"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                <div>
                    <h3 class="text-lg font-semibold mb-4">Quick Links</h3>
                    <ul class="space-y-2">
                        <li><button onclick="scrollToSection('home')" class="text-gray-400 hover:text-secondary transition">Home</button></li>
                        <li><button onclick="scrollToSection('about')" class="text-gray-400 hover:text-secondary transition">About Us</button></li>
                        <li><button onclick="scrollToSection('programs')" class="text-gray-400 hover:text-secondary transition">Programs</button></li>
                        <li><button onclick="scrollToSection('admissions')" class="text-gray-400 hover:text-secondary transition">Admissions</button></li>
                        <li><button onclick="scrollToSection('contact')" class="text-gray-400 hover:text-secondary transition">Contact</button></li>
                        <li><button onclick="openDashboard()" class="text-amber-400 hover:text-secondary transition font-semibold">📊 Dashboard</button></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-semibold mb-4">Programs</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-secondary transition">Early Childhood</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-secondary transition">Elementary</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-secondary transition">Arts &amp; Music</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-secondary transition">Sports Programs</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-semibold mb-4">Newsletter</h3>
                    <p class="text-gray-400 mb-4">Subscribe for updates and news.</p>
                    <div class="flex">
                        <input type="email" placeholder="Your email" class="px-4 py-2 w-full rounded-l-lg text-dark focus:outline-none">
                        <button class="bg-secondary text-dark px-4 py-2 rounded-r-lg font-semibold hover:bg-yellow-500 transition"><i class="fas fa-paper-plane"></i></button>
                    </div>
                </div>
            </div>
            <div class="border-t border-gray-800 mt-12 pt-8 text-center">
                <p class="text-gray-400">© 2026 Rauk Primary School. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById("mobile-menu-button").addEventListener("click", function() {
            document.getElementById("mobile-menu").classList.toggle("hidden");
        });
        function scrollToSection(id) {
            const el = document.getElementById(id);
            if (el) { el.scrollIntoView({ behavior: "smooth" }); document.getElementById("mobile-menu").classList.add("hidden"); }
        }
        function openDashboard() {
            document.getElementById("dashboard-overlay").classList.add("active");
            document.body.style.overflow = "hidden";
        }
        function closeDashboard() {
            document.getElementById("dashboard-overlay").classList.remove("active");
            document.body.style.overflow = "";
        }
        window.addEventListener("scroll", function() {
            const nav = document.querySelector("nav");
            nav.classList.toggle("shadow-lg", window.scrollY > 50);
        });
    </script>


   
</body></html>
