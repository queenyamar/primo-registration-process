<template>
    <div class="welcome">
        <div class="container">
            <b-row>
                <b-col md="6">
                    <div class="welcome__content">
                        <h2 class="welcome__title">Welcome!</h2>
                        <b-img :src="require(`~/assets/images/graphics/welcome.png`)" fluid></b-img>
                    </div>
                </b-col>
                <b-col md="6">
                    <div class="welcome__form">
                        <b-form @submit="onSubmit">
                            <div class="form-group">
                                <label class="form-label">Email</label>
                                <b-form-input
                                    v-model="form.email"
                                    type="email"
                                    placeholder="Enter email"
                                    required
                                ></b-form-input>
                            </div>
                            <div class="form-group">
                                <label class="form-label">Password</label>
                                <b-form-input
                                    v-model="form.password"
                                    type="password"
                                    placeholder="Enter password"
                                    required
                                ></b-form-input>
                            </div>
                            <div class="form-group d-md-flex justify-content-md-between align-items-md-center">
                                <b-form-checkbox
                                    v-model="status"
                                    value="signed_in"
                                    unchecked-value="signed_out"
                                    class="welcome__checkbox-label"
                                >
                                    Keep me signed in
                                </b-form-checkbox>
                                <a class="text-blue welcome__forgot" href="#">Forgot password?</a>
                            </div>
                            <b-button class="btn-green" block>Login</b-button>
                        </b-form>
                        <p class="welcome__divider">OR</p>
                        <b-button class="btn-outline-white" block>
                            <b-img :src="require(`~/assets/images/icons/google-icon.svg`)" fluid></b-img>
                            <span class="ml-3">Sign in with Google</span>
                        </b-button>
                        <p class="mb-0 welcome__sign-up">New here? <span><a class="text-blue" href="/register">Sign up</a></span></p>
                    </div>
                </b-col>
            </b-row>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                form: {
                    email: '',
                    password: '',
                    status: 'signed_out'
                },
                show: true
            }
        },
        methods: {
            onSubmit(event) {
                event.preventDefault()
                alert(JSON.stringify(this.form))
            },
        }
    }
</script>