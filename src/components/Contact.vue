<script setup>
import { reactive, ref, toRef } from 'vue';
import { useVuelidate } from '@vuelidate/core';
import { required, email, minLength, maxLength } from '@vuelidate/validators';

const setupValidation = () => {
    const form = reactive({
        name: "",
        email: "",
        message: "",
    });

    const rules = {
        name: { required },
        email: { required, email },
        message: { required, minLength: minLength(3), maxLength: maxLength(500) },
    }

    const vv = useVuelidate(rules, {
        name: toRef(form, "name"),
        email: toRef(form, "email"),
        message: toRef(form, "message")
    });

    return { form, vv };
};

const state = ref(setupValidation());

const onSubmit = () => {
    state.value.vv.$touch();

    if (state.value.vv.$invalid) return;

    alert("Form submitted");

    // Reset validation and form data
    state.value = setupValidation();
}

</script>

<template>
    <section class="contact" id="contact">
        <h2>Contact</h2>
        <p class="contact-bio">Have a question or want to work together? Leave your details and I will get back to you as
            soon as
            possible.</p>
        <form class="contact-form" @submit.prevent="onSubmit" novalidate>
            <input type="text" name="name" v-model="state.form.name" placeholder="Your name"
                :class="{ 'invalid': state.vv.name.$error }">
            <input type="email" name="email" v-model="state.form.email" placeholder="Email"
                :class="{ 'invalid': state.vv.email.$error }">
            <textarea name="message" v-model="state.form.message" placeholder="Message"
                :class="{ 'invalid': state.vv.message.$error }"></textarea>
            <div class="form-handling">
                <div class="errors">
                    <p class="name error" v-if="state.vv.name.$error">Please enter your name.</p>
                    <p class="email error" v-if="state.vv.email.$error">Please enter a valid email.</p>
                    <p class="message error" v-if="state.vv.message.$error">Message should be between 10 and 500 characters.
                    </p>
                </div>
                <button class="submit-btn" type="submit">SUBMIT</button>
            </div>
        </form>
    </section>
</template>

<style scoped>
.contact {
    justify-content: flex-start;
}

.form-handling {
    display: flex;
    justify-content: space-between;
    width: 100%;
}

.error {
    font-weight: 500;
}

.contact-form {
    width: 600px;
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    gap: 0.75em;
}

input,
textarea {
    width: 100%;
    padding: 0.5em 1em;
    resize: none;
    outline: none;
    background-color: rgba(40, 40, 40, 0.95);
    color: inherit;
    border: none;
    font-family: inherit;
    font-size: 1.1em;
}

textarea {
    height: 200px;
}

.contact-bio {
    width: 600px;
    font-size: 1.1em;
    margin: 1.5em 0em 1.5em 0em;
}

.submit-btn {
    background: none;
    color: inherit;
    font-size: 1em;
    padding: 0.5em 1.5em;
    transition: box-shadow .15s ease-in-out;
    font-weight: 500;
    box-shadow: inset 0 -5px 0 -1px #ff4d5a;
    border: none;
    cursor: pointer;
    align-self: flex-start;
}

.submit-btn:hover {
    box-shadow: inset 0 -100px 0 -1px #ff4d5a;
}


.invalid {
    border-left: 2px solid #ff4d5a;
}

@media (max-width: 650px) {

    .error {
        line-height: 1.8;
        font-size: 10px;
        font-weight: 500;
    }

    .contact {
        min-height: fit-content;
        padding-bottom: 2em;
    }

    .contact-bio,
    .contact-form {
        width: 300px;
        font-size: 15px;
    }

    .contact-form {
        gap: 1em;
    }

    .contact-bio {
        margin: 1.5em 0 1.5em 0;
    }
}
</style>
