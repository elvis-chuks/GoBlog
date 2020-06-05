<template>
    <div>
        <Nav/>
        <main>
            <div class="top">
                <button @click="newPost()" id="myBtn">
                    Create New Post
                </button>
            </div>

            <div class="article">
                <h1 class="title">Getting Started with Golang</h1>
                <p class="post-details">First of all, I hate Lorem ipsum, second of all, 
                this is a blog post about building a blog using Golang and Vue JS. VueJS would power the front end,
                while Golang would power the backend.
                Get Started using Golang and secure the bag so that the bag can secure you.</p>
                <hr>
            </div>
            <div class="article">
                <div class="article-top">
                    <h1 class="title">Getting Started with Golang</h1>
                    <div class="actions">
                        <img src="../assets/edit.svg" class="edit" />
                        <img src="../assets/delete.svg" class="delete" />
                    </div>
                </div>
                <p class="post-details">First of all, I hate Lorem ipsum, second of all, 
                this is a blog post about building a blog using Golang and Vue JS. VueJS would power the front end,
                while Golang would power the backend.
                Get Started using Golang and secure the bag so that the bag can secure you.</p>
                <hr>
            </div>
            <div class="article">
                <h1 class="title">Getting Started with Golang</h1>
                <p class="post-details">First of all, I hate Lorem ipsum, second of all, 
                this is a blog post about building a blog using Golang and Vue JS. VueJS would power the front end,
                while Golang would power the backend.
                Get Started using Golang and secure the bag so that the bag can secure you.</p>
                <hr>
            </div>
            <div class="article">
                <div class="article-top">
                    <h1 class="title">Getting Started with Golang</h1>
                    <div class="actions">
                        <img src="../assets/edit.svg" class="edit" />
                        <img src="../assets/delete.svg" class="delete" />
                    </div>
                </div>
                <p class="post-details">First of all, I hate Lorem ipsum, second of all, 
                this is a blog post about building a blog using Golang and Vue JS. VueJS would power the front end,
                while Golang would power the backend.
                Get Started using Golang and secure the bag so that the bag can secure you.</p>
                <hr>
            </div>
        </main>

        <div id="myModal" class="modal">

        <!-- Modal content -->
        <div class="modal-content">
            <span class="close" @click="closeModal()">&times;</span>
            <div class="modal-header">
                
                <h2>New Post</h2>
            </div>
            <div class="modal-body">
                <div class="form">
                    <div class="form-group">
                        <input type="text" placeholder="Title" name="post-title" class="form-control">
                    </div>
                    <div class="form-group text">
                        <textarea name="post-content" id="post-content" cols="30" rows="10" class="form-control" placeholder="Post Description"></textarea>
                    </div>
                    <div class="bottom">
                        <div class="side"></div>
                        <div class="side">
                            <button>Post</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        

        </div>
    </div>
</template>

<script>
import Nav from '@/components/nav.vue'
export default {
    name : "Posts",
    components:{
        Nav
    },
    methods:{
        newPost(){
            var modal = document.getElementById("myModal");
            modal.style.display = "block";
        },
        closeModal(){
            var modal = document.getElementById("myModal");
            modal.style.display = "none";
        }
    },
}
</script>

<style scoped>
main{
    padding-top:80px;
    width:90%;
    margin:auto;
    /* background:red; */
}
.top button{
    padding:10px;
    background:none;
    border:1px solid #3A2E2E;
    width:184px;
    color: #3A2E2E;
    font-size:13px;
    cursor: pointer;
    border-radius: 3px;
}
.article{
    margin-top:50px;
}
.article-top{
    display:flex;
    width:100%;
}
.article-top .title{
    flex:4;
}
.article-top .actions{
    flex:1;
}
.article-top .actions{
    display:flex;
    justify-content: flex-end;
}
.article-top .actions img{
    cursor: pointer;
}

.edit{
    margin-right:30px;
    margin-top:2px;
}
.article .title{
    font-size:18px;
}
.article p {
    margin-top:20px;
    font-size:13px;
    color:#938B8B;
}
.article hr{
    margin-top:30px;
    background: #ECECEC;
    border:none;
    height:1px;
}

.form-group{
    width:100%;
}
.form-control{
    width:100%;
    padding:9px;
    border-radius: 2px;
    border:1px solid grey;
}
textarea{
    border-radius: 5px;
}
.text{
    margin-top:20px;
}
.bottom{
    display:flex;
    margin-bottom:30px;
}
.side{
    flex:1;
}
.side button{
  margin-top:40px;
  color:white;
  background:#332A2A;
  border-radius: 3px;
  font-size:12px;
  cursor: pointer;
  width:100%;
  border:none;
  padding:9px;
}

/* The Modal (background) */
.modal {
  display: none; /* Hidden by default */
  position: fixed; /*Stay in place*/
  z-index: 1; /* Sit on top */
  left: 0;
  top: 0;
  width: 100%; /* Full width */
  height: 100%; /* Full height */
  overflow: auto; /* Enable scroll if needed */
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
  transition: 2s;
  padding-top:100px;
}


/* The Close Button */
.close {
  color: #aaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
  margin-right: 20px;
  margin-top: 10px;
}

.close:hover,
.close:focus {
  color: black;
  text-decoration: none;
  cursor: pointer;
}


/* Modal Header */
.modal-header {
  padding: 50px 25px;
  color: black;
}

/* Modal Body */
.modal-body {padding: 0px 25px;}

/* Modal Content */
.modal-content {
  position: relative;
  background-color: #fefefe;
  margin: auto;
  padding: 0;
  border: 1px solid #888;
  width: 40%;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2),0 6px 20px 0 rgba(0,0,0,0.19);
  animation-name: animatetop;
  animation-duration: 0.4s
}

/* Add Animation */
@keyframes animatetop {
  from {top: -300px; opacity: 0}
  to {top: 0; opacity: 1}
}

@media(max-width:800px){
    .modal-content {
        width:95%;
    }
}
</style>