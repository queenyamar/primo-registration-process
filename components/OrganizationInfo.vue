<template>
    <div class="organization">
        <div class="container">
            <b-row>
                <b-col md="6">
                    <div class="organization__content">
                        <h2 class="organization__title">Tell us a little bit<br />about you</h2>
                        <b-img :src="require(`~/assets/images/graphics/organization.png`)" fluid></b-img>
                    </div>
                </b-col>
                <b-col md="6">
                    <div class="organization__form">
                        <b-form @submit="onSubmit">
                            <div class="form-group">
                                <label class="form-label">What industry is your business in?</label>
                                <b-form-input
                                    v-model="form.industry"
                                    type="text"
                                    placeholder="Enter industry of your business"
                                    required
                                ></b-form-input>
                            </div>
                            <div class="form-group">
                                <label class="form-label">What size is your team?</label>
                                <b-form-input
                                    v-model="form.size"
                                    type="text"
                                    placeholder="Enter size of team"
                                    required
                                ></b-form-input>
                            </div>
                            <div class="form-group">
                                <label class="form-label">Please selet your app tools to connect<br />
                                    <span><small>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</small></span>
                                </label>
                                <div class="organization__tools">
                                    <b-button class="btn-form">Google workspace</b-button>
                                    <b-button class="btn-form">Slack</b-button>
                                    <b-button class="btn-form">Asana</b-button>
                                    <b-button class="btn-form">Microsoft Office</b-button>
                                </div>
                            </div>
                            <div class="text-center text-lg-right mt-4">
                                <b-button class="btn-outline-green mb-2 mb-lg-0">Back</b-button>
                                <b-button class="btn-green">Start exploring Primo</b-button>
                            </div>
                        </b-form>
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
                    industry: '',
                    team: '',
                },
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