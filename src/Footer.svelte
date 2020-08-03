<script>
    import NavLinks from './NavLinks.svelte';
    import SocialLink from './SocialLink.svelte';
    import Icon from 'fa-svelte';
    import { faLinkedinIn, faInstagram, faTwitter } from '@fortawesome/free-brands-svg-icons';
</script>

<style>
.container {
    background-color: #F5F5F5;
    padding: 3rem 3.2rem 6.4rem;
    color: #545759;
}

.container li, .socialLinks a {
    color: #1c1c1c;
}

.contact {
    margin-top: 6rem;
}

.contact > *:not(:last-child), .mailUpdates {
    margin-bottom: 2rem;
}

.socialLinks {
    margin: 3rem 0;
}

.socialLinks > *:not(:last-child) {
    margin-right: 1.5rem;
}

.mailUpdates a {
    border-bottom: 1px solid #545759;
    font-weight: bold;
}
</style>

<footer class="container">
    <div class="wrapper">
        <NavLinks />
        <div class="contact">
            <p>hello@commercebear.com</p>
            <p>Canada +1 647 479 6243</p>
            <p>USA +1 929 232 2327</p>
        </div>
        <div class="socialLinks">
            <SocialLink iconName={faLinkedinIn} />
            <SocialLink iconName={faInstagram} />
            <SocialLink iconName={faTwitter} />
        </div>
        <p class="mailUpdates">
            <a
                href="https://mailchi.mp/commercebear/updates"
                target="_blank"
                rel="noopener noreferrer"
                aria-label="This is an external link (opens in a new tab)"
            >
                Click here 
            </a>{" "}
            to join our growing industry following and stay up to date with all
            things CommerceBear.
        </p>
        <p>© 2020 CommerceBear. All Rights Reserved</p>
    </div>
</footer>