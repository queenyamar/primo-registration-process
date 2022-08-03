<template>
    <div class="hero-banner">
        <b-container>
            <b-row>
                <b-col lg="6">
                    <h1 class="hero-banner__title">Bring more leads for your business</h1>
                    <p class="hero-banner__description">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eu quam nec lacus eleifend ultrices quis ac purus. In sit amet mollis lacus. Sed eget ipsum sit amet mauris dapibus pellentesque.</p>
                    <div class="hero-banner__form">
                        <b-input-group>
                            <b-form-input class="hero-banner__input" placeholder="Enter your email"></b-form-input>
                            <b-input-group-append>
                                <b-button @click="showModal()" class="btn-hero">Get started</b-button>
                            </b-input-group-append>
                        </b-input-group>
                    </div>
                </b-col>
            </b-row>
        </b-container>
        <b-modal modal-class="verify-modal" ref="verifyModal" :hide-header="true" :hide-footer="true" centered>
            <div class="verify-modal__header">
                <div class="verify-modal__icon">
                    <span class="material-icons email-icon">
                        email
                    </span>
                </div>
                <h6 class="verify-modal__title">Verify email</h6>
            </div>
            <div class="verify-modal__content">
                <p class="mb-0">Verification email sent to</p>
                <p class="verify-modal__email">loremipsum@gmail.com</p>
                <b-link href="/welcome" class="btn btn-green">Verify</b-link>
            </div>
            <div class="verify-modal__footer">
                <p class="text-center verify-modal__contact">Didn’t see an email? Check spam folder or resend email.
                    <span><a href="#" class="text-blue">Contact us for any questions.</a></span></p>
            </div>
        </b-modal>
    </div>
</template>

<script>
    export default {
        methods: {
            showModal() {
                this.$refs['verifyModal'].show()
            },
            hideModal() {
                this.$refs['verifyModal'].hide()
            },
        },
    }
</script>