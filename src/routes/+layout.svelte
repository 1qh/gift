<script lang="ts">
    import '$/app.postcss'
    import { arrow, autoUpdate, computePosition, flip, offset, shift } from '@floating-ui/dom'
    import { AppShell, LightSwitch, storePopup } from '@skeletonlabs/skeleton'

    storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow })
</script>

<AppShell>
    <div
        class="bg-cover bg-top bg-no-repeat lg:bg-[image:url('/src/assets/bg_desktop.svg')] bg-[image:url('/src/assets/bg_mobile.svg')] h-full">
        <LightSwitch class="opacity-5" />
        <div class="flex items-center justify-center">
            <img src={'/src/assets/logo1.svg'} alt="" width="110" class="mx-2" />
            <img src={'/src/assets/logo2.svg'} alt="" width="60" class="mx-2" />
            <img src={'/src/assets/logo3.svg'} alt="" width="80" class="mx-2" />
        </div>
        <div class="container flex items-center justify-center h-full mx-auto">
            <div class="flex flex-col items-center space-y-10 text-center">
                <slot />
            </div>
        </div>
    </div>
</AppShell>
