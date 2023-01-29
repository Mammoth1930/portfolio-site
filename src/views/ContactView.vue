<template>
    <section id="contact">
        <article>
            <h3>Want to see more?</h3>
            <p>Please feel free to reach out to me via email or social media.</p>
            <div class="social-container">
                <a class="social-btn" href="mailto: mamoth1930@gmail.com" target="_blank" rel="noopener noreferrer"><img src="@/assets/img/email.png"/>mamoth1930@gmail.com</a>
                <a class="social-btn" href="https://www.linkedin.com/in/riley-farrell-420240201/" target="_blank" rel="noopener noreferrer"><img src="@/assets/img/linkedIn.png"/>Riley Farrell</a>
                <a class="social-btn" href="https://github.com/Mammoth1930" target="_blank" rel="noopener noreferrer"><img src="@/assets/img/github.png"/>Mammoth1930</a>
            </div>
            <div class="social-container-icon">
                <a class="social-btn-icon" href="mailto: mamoth1930@gmail.com" target="_blank" rel="noopener noreferrer"><img src="@/assets/img/email.png"/></a>
                <a class="social-btn-icon" href="https://www.linkedin.com/in/riley-farrell-420240201/" target="_blank" rel="noopener noreferrer"><img src="@/assets/img/linkedIn.png"/></a>
                <a class="social-btn-icon" href="https://github.com/Mammoth1930" target="_blank" rel="noopener noreferrer"><img src="@/assets/img/github.png"/></a>
            </div> 
        </article>
    </section>
  </template>

<style>
article h3 {
    margin-left: 100px;
    margin-top: 30px;
}

.social-container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin: 50px 100px 0px 100px;
    padding-bottom: 50px;
}

.social-container-icon {
    display: none;
}

.social-btn {
    display: flex;
    align-items: center;
    font-size: 1.5em;
    width: 350px;
    padding: 10px 20px;
    margin: 0px 30px;
    background-color: var(--accent-color);
    border-radius: 1ch;
    color: var(--text-primary-color);
    text-decoration: none;
}

.social-btn:hover {
    transform: scale(1.1);
    box-shadow: 2px 5px 5px var(--accent-bright);
    text-decoration: none;
}

.social-btn img {
    width: 30px;
    margin-right: 15px;
}

/* Laptop size */
@media screen and (max-width: 1200px) {
    article p, .social-container, #carousel-main, #thumbnails {
        margin: 30px 50px 0px 50px;
    }

    article h3, article h2 {
        margin-left: 50px;
        margin-top: 30px;
    }

    .social-btn {
        font-size: 1em;
        margin: 0px 5px;
    }
}

/* Tablet size */
@media screen and (max-width: 740px) {
    .social-container {
        flex-direction: column;
        padding-bottom: 0px;
        margin: 50px 0px 0px 0px;
    }

    .social-btn {
        margin-bottom: 25px;
        margin-left: 0px;
        margin-right: 0px;
        width: 300px;
    }
}

@media screen and (max-width: 360px) {
    .social-btn {
        width: 230px;
    }
}

@media screen and (max-width: 285px) {
    .social-container {
        display: none;
    }

    .social-container-icon {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        margin: 50px 100px 0px 100px;
        padding-bottom: 50px;
    }

    .social-btn-icon {
        margin-bottom: 20px;
    }

    .social-btn-icon:hover {
        transform: scale(1.1);
    }

    .social-btn-icon img {
        width: 80px;
    }
}
</style>