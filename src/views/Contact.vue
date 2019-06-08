<template>
    <div class="contact page">
        <div class="contact-title">
            <h2>Let's rock it together !</h2>
            <p>
                Contact me if you want me to make your projects real.
            </p>
        </div>
        <div class="socials">
            <div class="icon">
                <a href="mailto:martin.prejean@hetic.net" title="Send me an email !">
                    <img src="@/assets/mail.svg" alt="email icon">
                </a>
            </div>
            <div class="icon">
                <a href="https://www.facebook.com/martin.macabies?ref=bookmarks" target="_blank" title="Contact me via Facebook">
                    <img src="@/assets/facebook.svg" alt="email icon">
                </a>
            </div>
            <div class="icon">
                <a href="https://www.linkedin.com/in/martinprejean" target="_blank" title="Contact me via Linkedin">
                    <img src="@/assets/linkedin.svg" alt="email icon">
                </a>
            </div>
            <div class="icon">
                <a href="https://www.instagram.com/mmacabies/?hl=fr" target="_blank" title="Contact me via Instagram">
                    <img src="@/assets/instagram.svg" alt="email icon">
                </a>
            </div>
        </div>
    </div>
</template>

<style>

.contact
{
    width: 100vw;
    height: 80vh;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}

.contact-title
{
    font-size: 3rem;
    text-align: center;
}

.contact-title p
{
    font-size: 1rem;
    padding: 1rem;
    text-align: center;
}

.socials
{
    display: flex;
}
.icon
{
    border-radius: 50%;
    margin: 2rem;
}

.icon img
{
    width: 24px;
    height: 24px;
    display: flex;
    justify-content: center;

} 

@media screen and (max-width: 1024px) 
{
    .contact
    {
        height: 100%;
    }
}
</style>