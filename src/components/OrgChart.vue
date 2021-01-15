<template>
    <div id="tree" ref="tree"></div>
</template>

<script>

    import OrgChart from '@balkangraph/orgchart.js'

    export default {

        name: 'tree',
        data() {
            return {
                /*
                nodes: [
                    { id: 1, name: "Denny Curtis", title: "CEO", img: "https://cdn.balkan.app/shared/2.jpg" },
                    { id: 2, pid: 1, name: "Ashley Barnett", title: "Sales Manager", img: "https://cdn.balkan.app/shared/3.jpg" },
                    { id: 3, pid: 1, name: "Caden Ellison", title: "Dev Manager", img: "https://cdn.balkan.app/shared/4.jpg" },
                    { id: 4, pid: 2, name: "Elliot Patel", title: "Sales", img: "https://cdn.balkan.app/shared/5.jpg" },
                    { id: 5, pid: 2, name: "Lynn Hussain", title: "Sales", img: "https://cdn.balkan.app/shared/6.jpg" },
                    { id: 6, pid: 3, name: "Tanner May", title: "Developer", img: "https://cdn.balkan.app/shared/7.jpg" },
                    { id: 7, pid: 3, name: "Fran Parsons", title: "Developer", img: "https://cdn.balkan.app/shared/8.jpg" }
                ]
                */
                    nodes: [
                    { id: 1, name: "Africa", title: "AFRICOM", img: "africa.png" },
                    { id: 2, pid: 1, name: "Cameroon", title: "Country", img: "cameroon.png" },
                    { id: 3, pid: 1, name: "Nigeria", title: "Country", img: "nigeria.png" },
                    { id: 4, pid: 3, name: "Malheureux Crétins", title: "Group", img: "fist.jpg" },
                    { id: 5, pid: 4, name: "Petite Mosquee de Dougdje", title: "Mosque", img: "mosque.jpg" },
                    { id: 6, pid: 4, name: "Ashigashiya Mosque", title: "Group", img: "mosque.jpg" },
                    { id: 7, pid: 4, name: "Fakikwe Fakikiwe Sama", title: "Group", img: "mosque.jpg" },
                    { id: 8, pid: 5, name: "Brian Major", title: "Member", img: "https://cdn.balkan.app/shared/5.jpg" },
                    { id: 9, pid: 6, name: "Brian Major", title: "Member", img: "https://cdn.balkan.app/shared/5.jpg" },
                    { id: 10, pid: 7, name: "Brian Major", title: "Member", img: "https://cdn.balkan.app/shared/5.jpg" },
                    { id: 11, pid: 5, name: "Aaron Julian", title: "Member", img: "https://cdn.balkan.app/shared/6.jpg" },
                    { id: 12, pid: 6, name: "Aaron Julian", title: "Member", img: "https://cdn.balkan.app/shared/6.jpg" },
                    { id: 13, pid: 7, name: "Aaron Julian", title: "Member", img: "https://cdn.balkan.app/shared/6.jpg" },
                    { id: 14, pid: 5, name: "Michael Towles", title: "Member", img: "https://cdn.balkan.app/shared/7.jpg" },
                    { id: 15, pid: 6, name: "Michael Towles", title: "Member", img: "https://cdn.balkan.app/shared/7.jpg" },
                    { id: 16, pid: 7, name: "Michael Towles", title: "Member", img: "https://cdn.balkan.app/shared/7.jpg" }
                ]                           
            }
        },

        methods: {
            oc: function(domEl, x) {

                this.chart = new OrgChart(domEl, {
                nodes: x,
                nodeBinding: {
                    field_0: "name",
                    field_1: "title",
                    img_0: "img"
                }
                });

            }
        },

        mounted(){
        this.oc(this.$refs.tree, this.nodes)
        }
    }
</script>

<style scoped>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    } 
    #tree {
        width: 100%;
        height: 100%;
    }                   
</style>