<template>
    <h1>Forms</h1>

    <div>
        <pre>
            {{ JSON.stringify(formValues, null, 2) }}
        </pre>
    </div>

    <form @submit="handleSubmit">
        <div>
            <label for="name">Name</label>
            <input id="name" type="text" v-model.trim.lazy="formValues.name">
        </div>

        <div>
            <label for="profile">Profile Summary</label>
            <textarea id="profile" v-model="formValues.profile"></textarea>
        </div>

        <div>
            <label for="country">Country</label>
            <select id="country" v-model="formValues.country">
                <option>Please Select Country</option>
                <option value="ind">India</option>
                <option value="us">USA</option>
                <option value="aus">AUS</option>
            </select>
        </div>

        <div>
            <label for="job-location">Job Location</label>
            <select id="job-location" multiple v-model="formValues.jobLocation">
                <option value="ind">India</option>
                <option value="us">USA</option>
                <option value="aus">AUS</option>
            </select>
        </div>

        <div>
            <input type="checkbox" id="remote-work" v-model="formValues.remoteWork">
            <label for="remote-work">Open to Remote Work ?</label>
        </div>

        <div>
            <input type="checkbox" id="relocate" v-model="formValues.relocate" true-value="yes" false-value="no">
            <label for="relocate">Open to Relocate ?</label>
        </div>


        <div>
            <label>Skill Set</label>

            <input type="checkbox" value="html" id="html" v-model="formValues.skills">
            <label for="html">HTML</label>

            <input type="checkbox" value="css" id="css" v-model="formValues.skills">
            <label for="css">CSS</label>

            <input type="checkbox" value="javascript" id="javascript" v-model="formValues.skills">
            <label for="javascript">JavaScript</label>
        </div>

        <div>
            <label>Years of Experience</label>

            <input type="radio" value="0-2" id="0-2" v-model="formValues.yoe">
            <label for="0-2">0-2</label>

            <input type="radio" value="2-4" id="2-4" v-model="formValues.yoe">
            <label for="2-4">2-4</label>

            <input type="radio" value="4-6" id="4-6" v-model="formValues.yoe">
            <label for="4-6">4-6</label>
        </div>

        <div>
            <label for="age">Age</label>
            <input 
                id="age"
                type="number"
                v-model.number="formValues.age"
            />
        </div>

        <div>
            <button>Submit form</button>
        </div>
    </form>

    <hr />

</template>

<script>

export default {
    name: 'FormsVue',
    data() {
        return {
            formValues: {
                name: '',
                profile: '',
                country: 'ind',
                jobLocation: [],
                remoteWork: false,
                relocate: 'no',
                skills: [],
                yoe: '',
                age: null,
            }
        }
    },
    methods: {
        handleSubmit(event) {
            event.preventDefault();
            console.log('Form Values', this.formValues);
        }
    }
}
</script>

<style>
label {
    font-weight: bold;
    display: flex;
    margin-bottom: 5px;
}

input+label {
    font-weight: bold;
    display: inline-flex;
    margin-right: 20px;
}

input[type='text'],
textarea,
select {
    display: block;
    width: 400px;
    padding: 6px 12px;
    font-size: 14px;
    line-height: 1.42857143;
    color: #555;
    background-color: #fff;
    background-image: none;
    border: 1px solid #ccc;
    border-radius: 4px;
}
</style>
