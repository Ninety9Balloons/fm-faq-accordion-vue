<template>
    <main class="bg-white rounded-xl p-6">
        <div class="flex">
            <img class="w-6 mr-10" src="../assets/images/icon-star.svg" />
            <h1 class="text-dark-purple font-bold text-3xl">FAQs</h1>
        </div>
        <Accordion accNumber="tab-multi-one">
            <template #header
                >What is Frontend Mentor, and how will it help me?</template
            >
            <template #body>
                Frontend Mentor offers realistic coding challenges to help
                developers improve their frontend coding skills with projects in
                HTML, CSS, and JavaScript. It's suitable for all levels and
                ideal for portfolio building.</template
            >
        </Accordion>

        <Accordion accNumber="tab-multi-two" class="border-t">
            <template #header>Is Frontend Mentor free?</template>
            <template #body>
                Yes, Frontend Mentor offers both free and premium coding
                challenges, with the free option providing access to a range of
                projects suitable for all skill levels.</template
            >
        </Accordion>

        <Accordion accNumber="tab-multi-three" class="border-t">
            <template #header
                >Can I use Frontend Mentor projects in my portfolio?</template
            >
            <template #body>
                Yes, you can use projects completed on Frontend Mentor in your
                portfolio. It's an excellent way to showcase your skills to
                potential employers!</template
            >
        </Accordion>

        <Accordion accNumber="tab-multi-four" class="border-t">
            <template #header
                >How can I get help if I'm stuck on a Frontend Mentor
                challenge?</template
            >
            <template #body>
                The best place to get help is inside Frontend Mentor's Discord
                community. There's a help channel where you can ask questions
                and seek support from other community members.</template
            >
        </Accordion>
    </main>
</template>

<script setup>
import Accordion from "./Accordion.vue";
</script>
