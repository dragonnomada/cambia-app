<template>
    <div class="login">
        <div class="signin-logo">
            <div class="signin-logo-circulos">
                <div class="signin-logo-curculo-menor"></div>
            </div>
            <img alt="" class="signin-logo-corazones"
                src="https://static.overlay-tech.com/assets/9430a984-8453-48e7-b0ce-91f4a217605e.svg" />
        </div>
        <div class="signin-form">
            <Field name="email" placeholder="Escribe tu correo" />
            <Field name="password" placeholder="Escribe tu contraseña"
                icon="https://static.overlay-tech.com/assets/f781ad01-cb2a-4871-be6a-a048caffe55e.svg" is-password />
            <div class="remeber-forgot">
                <div class="check-remember">
                    <img alt="" class="check-remember-icon"
                        src="https://static.overlay-tech.com/assets/f6e4fea5-1adb-47af-91c9-20bfaa180759.svg" />
                    <p class="check-remember-text">
                        Recordar contraseña
                    </p>
                </div>
                <p class="link-forgot">Olvidé mi contraseña</p>
            </div>
        </div>
        <div class="signin-buttons">
            <div class="signin-main-button">
                <div class="button-login">
                    <p class="button-login-text">Iniciar Sesión</p>
                    <!-- <img alt="" class="button-login-text"
                        src="https://static.overlay-tech.com/assets/969b44c2-0c5c-4313-b66a-5221ac306b24.png" /> -->
                </div>
                <div class="registro">
                    <p class="registro-existe">¿Tienes cuenta?</p>
                    <p class="registro-nuevo">Registarme</p>
                </div>
            </div>
            <div class="signin-other-buttons">
                <div class="button-twitter">
                    <p class="button-twitter-text">
                        Continuar con Twitter
                    </p>
                    <div class="flex-wrapper-one">
                        <img alt="" class="button-twitter-icon"
                            src="https://static.overlay-tech.com/assets/a05b920a-e0a4-41d8-bdaf-5c792f1346f8.svg" />
                    </div>
                </div>
                <div class="button-twitter">
                    <p class="button-gmail-text">
                        Continuar con Gmail
                    </p>
                    <div class="flex-wrapper-three">
                        <img alt="" class="button-gmail-icon"
                            src="https://static.overlay-tech.com/assets/0b0b64a5-0147-434d-8055-db52d0881bac.svg" />
                    </div>
                </div>
                <div class="button-twitter">
                    <p class="button-apple-text">
                        Continuar con Apple
                    </p>
                    <div class="flex-wrapper-two">
                        <img alt="" class="button-apple-icon"
                            src="https://static.overlay-tech.com/assets/f71ecb0f-0638-4a9f-b20f-f8bb6fd0741f.svg" />
                    </div>
                </div>
                <div class="button-facebook">
                    <p class="button-gmail-text">
                        Continuar con Facebook
                    </p>
                    <div class="flex-wrapper-four">
                        <img alt="" class="button-facebook-icon"
                            src="https://static.overlay-tech.com/assets/cd00e447-0c1f-4fe9-be1b-daac592439e8.svg" />
                    </div>
                </div>
            </div>
        </div>
        <img alt="" class="logo-citibanamex"
            src="https://static.overlay-tech.com/assets/d9d0049e-a1d2-4ff1-858d-e73f87c03852.svg" />
    </div>
</template>

<script>
import Field from './controls/Field.vue';
export default {
    name: "Login",
    components: { Field }
};
</script>

<style lang="scss" scoped>
.login {
    flex-grow: 1;
    position: relative;
    background-color: rgba(255, 255, 255, 1);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.signin-logo {
    position: relative;
}

.signin-logo-circulos {
    background-color: rgba(229, 228, 228, 0.45);
    border-radius: 50%;
    padding: 19px 19.28px 19.28px 19px;
    position: relative;
}

.signin-logo-curculo-menor {
    width: 136.72px;
    height: 136.72px;
    background-color: rgba(26, 26, 172, 0.15);
    border-radius: 50%;
}

.signin-logo-corazones {
    width: 123.35px;
    height: 77.93px;
    position: absolute;
    left: 25px;
    top: 48px;
}

.signin-form {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.remeber-forgot {
    margin-left: 37px;
    display: flex;
    align-items: center;
}

.check-remember {
    margin-right: 34px;
    display: flex;
    align-items: center;
}

.check-remember-icon {
    align-self: center;
}

.check-remember-text {
    font-family: "Roboto";
    font-size: 12px;
    font-weight: 500;
    line-height: normal;
    color: rgba(74, 74, 74, 0.75);
    padding-left: 12px;
}

.link-forgot {
    font-family: "Roboto";
    font-size: 12px;
    font-weight: 600;
    line-height: normal;
    color: rgba(63, 63, 184, 1);
}

.signin-buttons {

    padding-bottom: 72px;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.signin-main-button {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.button-login {
    width: 100%;
    background-color: rgba(63, 63, 184, 1);
    margin-bottom: 8px;
    padding: 12px;
    box-shadow: 5px 4px 4px 0 rgba(0, 0, 0, 0.25);
    display: flex;
    justify-content: center;
    align-items: center;
}

.button-login-text {
    font-family: "Roboto";
    font-size: 14px;
    font-weight: 500;
    color: white;
    text-transform: uppercase;
}

.registro {
    display: flex;
    align-items: flex-start;
    padding-bottom: 24px;
}

.registro-existe {
    height: 11px;
    width: 88px;
    font-family: "Roboto";
    font-size: 12px;
    font-weight: 500;
    line-height: normal;
    color: rgba(74, 74, 74, 0.75);
    display: flex;
    margin-right: 20px;
}

.registro-nuevo {
    height: 11px;
    width: 70px;
    font-family: "Roboto";
    font-size: 12px;
    font-weight: 600;
    line-height: normal;
    color: rgba(63, 63, 184, 1);
    display: flex;
}

.signin-other-buttons {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.button-twitter {
    margin-bottom: 13px;
    padding: 0 7px 0 0;
    position: relative;
}

.button-twitter-text {
    height: 17px;
    width: 142px;
    font-family: "Roboto";
    font-size: 12px;
    font-weight: 500;
    line-height: normal;
    color: rgba(74, 74, 74, 0.75);
    display: flex;
    text-shadow: 3px 3px 3px rgba(234, 234, 234, 0.25);
    position: absolute;
    right: 0;
    bottom: 3px;
}

.flex-wrapper-one {
    background-color: rgba(125, 125, 253, 0.15);
    border-radius: 15px;
    padding: 6px 153px 5px 17px;
    box-shadow: 3px 3px 3px 0 rgba(234, 234, 234, 0.25),
        0 4px 4px 0 rgba(0, 0, 0, 0.25);
    position: relative;
}

.button-twitter-icon {
    width: 100%;
    height: 100%;
}

.button-gmail-text {
    height: 17px;
    width: 142px;
    font-family: "Roboto";
    font-size: 12px;
    font-weight: 500;
    line-height: normal;
    color: rgba(74, 74, 74, 0.75);
    display: flex;
    text-shadow: 3px 3px 3px rgba(234, 234, 234, 0.25);
    position: absolute;
    right: 0;
    top: 8px;
}

.flex-wrapper-three {
    background-color: rgba(125, 125, 253, 0.15);
    border-radius: 15px;
    padding: 6px 154px 6.08px 16px;
    box-shadow: 3px 3px 3px 0 rgba(234, 234, 234, 0.25),
        0 4px 4px 0 rgba(0, 0, 0, 0.25);
    position: relative;
}

.button-gmail-icon {
    width: 20px;
    height: 15.92px;
}

.button-apple-text {
    height: 17px;
    width: 142px;
    font-family: "Roboto";
    font-size: 12px;
    font-weight: 500;
    line-height: normal;
    color: rgba(74, 74, 74, 0.75);
    display: flex;
    text-shadow: 3px 3px 3px rgba(234, 234, 234, 0.25);
    position: absolute;
    right: 0;
    top: 7px;
}

.flex-wrapper-two {
    background-color: rgba(125, 125, 253, 0.15);
    border-radius: 15px;
    padding: 2px 155.73px 6.5px 18px;
    box-shadow: 3px 3px 3px 0 rgba(234, 234, 234, 0.25),
        0 4px 4px 0 rgba(0, 0, 0, 0.25);
    position: relative;
}

.button-apple-icon {
    width: 16.27px;
    height: 19.5px;
}

.button-facebook {
    padding: 0 4px 0 0;
    position: relative;
}

.flex-wrapper-four {
    background-color: rgba(125, 125, 253, 0.15);
    border-radius: 15px;
    padding: 4px 157px 4px 13px;
    box-shadow: 3px 3px 3px 0 rgba(234, 234, 234, 0.25),
        0 4px 4px 0 rgba(0, 0, 0, 0.25);
    position: relative;
}

.button-facebook-icon {
    width: 20px;
    height: 20px;
}

.logo-citibanamex {
    width: 142px;
    height: 22px;
}
</style>