<script setup>

</script>

<template>
    <section class="contact" id="contact">
        <h2>Contact</h2>
        <p class="contact-bio">Have a question or want to work together? Leave your details and I will get back to you as
            soon as
            possible.</p>
        <form class="contact-form" action="">
            <input type="text" name="name" placeholder="Your name">
            <input type="email" name="email" placeholder="Email">
            <textarea name="message" placeholder="Message"></textarea>
            <button class="submit-btn" type="submit">SUBMIT</button>
        </form>
    </section>
</template>

<style scoped>
.contact {
    justify-content: flex-start;
}

.contact-form {
    width: 500px;
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    gap: 0.5em;
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
    width: 500px;
    font-size: 1.1em;
    margin: 1em 0em 2em 0em;
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
}

.submit-btn:hover {
    box-shadow: inset 0 -100px 0 -1px #ff4d5a;
}

@media (max-width: 650px) {

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
