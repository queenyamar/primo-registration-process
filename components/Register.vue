<template>
    <div class="register">
        <div class="container">
            <b-row>
                <b-col md="6">
                    <div class="register__content">
                        <h2 class="register__title">Let's create your<br />Primo account</h2>
                        <b-img :src="require(`~/assets/images/graphics/register.png`)" fluid></b-img>
                    </div>
                </b-col>
                <b-col md="6">
                    <div class="register__form">
                        <b-form @submit="onSubmit">
                            <b-row>
                                <b-col lg="6">
                                    <div class="form-group">
                                        <label class="form-label">First Name</label>
                                        <b-form-input
                                            v-model="form.firstName"
                                            type="text"
                                            placeholder="Enter first name"
                                            required
                                        ></b-form-input>
                                    </div>
                                </b-col>
                                <b-col lg="6">
                                    <div class="form-group">
                                        <label class="form-label">Last Name</label>
                                        <b-form-input
                                            v-model="form.lastName"
                                            type="text"
                                            placeholder="Enter last name"
                                            required
                                        ></b-form-input>
                                    </div>
                                </b-col>
                            </b-row>
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
                                <label class="form-label">Workplace name</label>
                                <b-form-input
                                    v-model="form.workplace"
                                    type="text"
                                    placeholder="Enter workplace"
                                    required
                                ></b-form-input>
                            </div>
                            <div class="form-group">
                                <label class="form-label">What region are you in?</label>
                                <b-form-select
                                    v-model="form.region"
                                    :options="regions"
                                    required
                                ></b-form-select>
                            </div>
                            <div class="text-right">
                                <b-link href="/organization-info" class="btn btn-green">Next</b-link>
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
                    firstName: '',
                    lastName: '',
                    email: '',
                    workplace: '',
                    region: ''
                },
                regions: [{ text: 'Select', value: '' }, 'Hong Kong', 'China', 'Japan', 'Korea'],
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