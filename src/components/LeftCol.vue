<template>
    <div class="left-col user-info">
        <!-- <div class="user-thumb">
            <img src="http://www.2-10.com/wp-content/uploads/2015/10/user1-300x300.jpg" alt="">
        </div> -->
        <br>
        <div class="form-field" v-if="edit == 'name'">
            <input type="text" name="" id="" v-model="personObj.name" @keyup.enter="edit = null">
        </div>
        <h1 v-else class="name" @dblclick="edit = 'name'">{{ personObj.name }}</h1>
        <h3 class="position">{{ personObj.position }}</h3>
        <br>
        <div class="skills">
            <h3 class="title"><i class="fa fa-fw fa-lightbulb-o"></i> Skills</h3>
            <ul id="v-for-object" class="">
                <li v-for="(skill, index) in personObj.skills" :key='index'>
                    <i class="fa fa-fw fa-dot-circle-o"></i> {{ skill }}
                    <template v-if="index != (personObj.skills.length - 1)">,</template>
                </li>
            </ul>
        </div>

        <br>
        <div class="version-control-tools">
            <h3 class="title"><i class="fa fa-code-fork"></i> Version Control Tool(s)</h3>
            <p><i class="fa fa-dot-circle-o"></i> {{ personObj.versioningTools }}</p>
        </div>

        <br>
        <div class="version-control-System">
            <h3 class="title"><i class="fa fa-star"></i> Version Control System(s)</h3>
            <ul id="v-for-object" class="demo">
                <li v-for="(skill, index) in personObj.versioningSystems" :key='index'>
                    <i class="fa fa-fw fa-dot-circle-o"></i> {{ skill }}
                    <template v-if="index != (personObj.versioningSystems.length - 1)">,</template>
                </li>
            </ul>
        </div>

        <br>
        <div class="contact">
            <h3 class="title"><i class="fa fa-fw fa-user"></i> Contact Me</h3>
            <ul>
                <li><i class="fa fa-fw fa-phone"></i> {{ personObj.phone }}</li>
                <li><i class="fa fa-fw fa-envelope"></i> {{ personObj.email }}</li>
                <li><i class="fa fa-fw fa-github"></i> {{ personObj.github }}</li>
                <!-- <li><i class="fa fa-fw fa-twitter"></i> {{ personObj.twitter }}</li> -->
                <li><i class="fa fa-fw fa-map"></i> {{ personObj.address }}</li>
            </ul>
        </div>

        <br>
        <div class="hobbies">
            <h3 class="title"><i class="fa fa-fw fa-user"></i> Hobbies</h3>
            <ul>
                <li v-for="(hobby, index) in personObj.hobbies" :key='index'>
                    <i class="fa fa-fw fa-angle-right"></i> {{ hobby }}
                    <template v-if="index != (personObj.hobbies.length - 1)">,</template>
                </li>

            </ul>
        </div>
    </div>

</template>

<script>
export default {
    name: 'LeftCol',
    props: ['person'],
    methods: {
        updateVal(){
            alert()
        }
    },
    data() {
        return {
            edit: false,
			personObj: {}
        }
    },
	mounted() {
		this.personObj = this.person
	}
}
</script>
