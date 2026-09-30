<script setup>

    import MainNavigation from './components/MainNavigation.vue';
    import SiteFooter from './components/SiteFooter.vue';
    import SiteContent from './components/SiteContent.vue';
    import InputField from './components/InputField.vue';
import { reactive } from 'vue';

    // function logMessage(name) {
    //     console.log('Input field changed!', name);
    // }

    function submitForm()
    {
        console.log(`form submitted`, formData)
        console.log(`form submitted`, JSON.stringify(formData))
    }

    const formData = reactive({
        email:'',
        firstname:'',
        lastname:''
    });
</script>

<template>
    <header>
        <MainNavigation />
        <!-- <MainNavigation /> -->
    </header>

    <main>
        <SiteContent />
        <!-- email input -->
        <InputField 
        v-model="formData.email"
        id="e-mail"
        type="email"
        placeholder="enter your email"
        label="email adress"
        />

         <!-- firstname input -->
          <InputField 
        v-model="formData.firstname"
        id="firstname"
        type="text"
        placeholder="enter your firstname"
        label="firstname"
        />

        <!-- lastname input -->
          <InputField 
        v-model="formData.lastname"
        id="lastname"
        type="text"
        placeholder="enter your lastname"
        label="lastname"
        />

        <button @click="submitForm">Submit</button>
    </main>


    <footer>
        <!-- sitefooter komponens használata -->
        <SiteFooter />
    </footer>

</template>

<style scoped>
</style>
