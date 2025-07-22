<script>
import Header from "$lib/components/Header.svelte";
import Footer from "$lib/components/Footer.svelte";
</script>

<meta charset="UTF-8" />
<title>GonePass – Password Manager</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<style>
    :root {
        --primary: #14b8a6;
        --primary-dark: #0f766e;
        --accent: #6366f1;
        --accent-dark: #4338ca;
        --gray-light: #f8fafc;
        --gray-border: #e2e8f0;
        --gray-muted: #64748b;
        --text-main: #1e293b;
        --white: #ffffff;
    }

    body {
        font-family: 'Segoe UI', sans-serif;
        background-color: var(--gray-light);
        color: var(--text-main);
        margin: 0;
    }

    .section1 {
        text-align: center;
        padding: 4rem 1rem 2rem;
        background-color: var(--white);
    }

    .section1 h1 {
        font-size: 2.5rem;
        color: var(--text-main);
    }

    .section1 p {
        font-size: 1.2rem;
        max-width: 600px;
        margin: 1rem auto;
        color: var(--gray-muted);
    }

    .button-group {
        margin-top: 2rem;
    }

    button {
        padding: 0.75rem 1.5rem;
        font-size: 1rem;
        margin: 0 0.5rem;
        border: none;
        border-radius: 8px;
        cursor: pointer;
        transition: 0.3s;
    }

    .btn-primary {
        background-color: var(--primary);
        color: white;
    }

    .btn-primary:hover {
        background-color: var(--primary-dark);
    }

    .btn-secondary {
        background-color: var(--accent);
        color: white;
    }
    .btn-primary a,
    .btn-secondary a {
        text-decoration: none;
        color: inherit;
    }

    .btn-secondary:hover {
        background-color: var(--accent-dark);
    }

    .section2 {
        max-width: 1100px;
        margin: 4rem auto;
        padding: 0 1rem;
    }

    .section2 h2 {
        text-align: center;
        font-size: 2rem;
        margin-bottom: 2rem;
    }

    .features {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 2rem;
    }

    .feature {
        background-color: var(--white);
        padding: 1.5rem;
        border-radius: 12px;
        box-shadow: 0 2px 8px rgba(0,0,0,0.04);
        width: 300px;
        transition: 0.2s;
    }

    .feature:hover {
        transform: translateY(-5px);
        box-shadow: 0 4px 12px rgba(0,0,0,0.08);
    }

    .feature h3 {
        color: var(--primary);
        margin-bottom: 0.5rem;
    }

    .feature p {
        color: var(--gray-muted);
        font-size: 0.95rem;
    }

    @media (max-width: 768px) {
        .features {
            flex-direction: column;
            align-items: center;
        }
    }
</style>

<body>
<Header/>

<section class="section1">
    <h1>Protect What Matters Most</h1>
    <p>GonePass is your secure and reliable password manager. Store, generate and access all your credentials in one safe place – wherever you are.</p>
    <div class="button-group">
        <button class="btn-primary"><a href="/login">Get Started Now !</a></button>
        <button class="btn-secondary"><a href="/register">Sign Up</a></button>
    </div>
</section>

<section class="section2">
    <h2>Why Use a GonePass ?</h2>
    <div class="features">
        <div class="feature">
            <h3>Convenience</h3>
            <p>Stop remembering dozens of passwords. With GonePass, everything is saved securely and accessible instantly.</p>
        </div>
        <div class="feature">
            <h3>Security First</h3>
            <p>We use end-to-end encryption, strong hashing, and secure storage protocols to protect your data.</p>
        </div>
        <div class="feature">
            <h3>Time Saving</h3>
            <p>Autofill your passwords and credentials instantly on all your devices. Focus on what matters.</p>
        </div>
    </div>
</section>

<section class="section2">
    <h2>Key Features</h2>
    <div class="features">
        <div class="feature">
            <h3>Secure Password Generator</h3>
            <p>Create strong, random passwords instantly. Customize length, symbols, and complexity.</p>
        </div>
        <div class="feature">
            <h3>Two-Factor Authentication</h3>
            <p>Protect your vault with 2FA (email, OTP, or TOTP) for an extra layer of security.</p>
        </div>
        <div class="feature">
            <h3>Robust Backend Security</h3>
            <p>Built with secure coding standards, encrypted storage, and regular vulnerability audits.</p>
        </div>
    </div>
</section>

</body>
<Footer/>

