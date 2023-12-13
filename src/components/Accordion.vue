<template>
    <div class="tab w-full overflow-hidden">
        <input
            class="absolute opacity-0"
            :id="accNumber"
            type="checkbox"
            name="tabs"
        />
        <label
            class="p-5 leading-normal cursor-pointer font-bold text-gray-purple flex justify-between"
            :for="accNumber"
            ><slot name="header"></slot
        ></label>
        <div
            class="tab-content overflow-hidden text-gray-purple leading-normal"
        >
            <p class="p-5">
                <slot name="body"> </slot>
            </p>
        </div>
    </div>
</template>

<script setup>
const props = defineProps(["accNumber"]);
</script>

<style scoped>
/* Tab content - closed */
.tab-content {
    max-height: 0;
    -webkit-transition: max-height 0.35s;
    -o-transition: max-height 0.35s;
    transition: max-height 0.35s;
}
/* :checked - resize to full height */
.tab input:checked ~ .tab-content {
    max-height: 100vh;
}
/* Label formatting when open */
.tab input:checked + label {
    padding: 1.25rem; /*.p-5*/
    color: hsl(292, 16%, 49%); /*.text-indigo*/
}
/* Icon */
.tab label::after {
    float: right;
    right: 0;
    top: 0;
    display: block;
    width: 1.5em;
    height: 1.5em;
    line-height: 1.5;
    font-size: 1.25rem;
    text-align: center;
    -webkit-transition: all 0.35s;
    -o-transition: all 0.35s;
    transition: all 0.35s;
}
/* Icon formatting - closed */
.tab input[type="checkbox"] + label::after {
    content: url("../assets/images/icon-plus.svg");
}

/* Icon formatting - open */
.tab input[type="checkbox"]:checked + label::after {
    content: url("../assets/images/icon-minus.svg");
}
</style>
