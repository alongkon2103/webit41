<template>
      <Head>
    <Title>Alongkon | About</Title>
  </Head>
    <h1 class="text-center">About me</h1>
    <div class="container d-flex justify-content-center ">
    <div class="card mb-3" style="max-width: 100%;">
  <div class="row g-0">
    <div class="col-md-4">
      <img :src="picture" class="img-fluid rounded-start" alt="..." :width="size">
    </div>
    <div class="col-md-8 d-flex">
      <div class="card-body d-flex">
        <div class="container w-100">
        <h5 class="card-title">{{ getfullname() }}</h5>

<p class="card-text my-0"> Nickname : {{ nickname }}</p>
        <p class="card-text my-0">Age: {{ age }}</p>
        <p class="card-text my-0">Address : {{ address }}</p>
        <p v-if="hobby.length === 0 ">ไม่มีงานอดิเรก</p>
        <div class="container d-flex rounded-2 m-2 p-2" style="background-color: #efefefef;" v-else>
            <div class="container" >
        <p class="card-text my-0">Hobbys : </p>
            <ul >
                <li v-for="hobbys in hobby">{{ hobbys }}</li>
            </ul>
        </div>
        <div class="container">
            <p class="card-text my-0">Generals : </p>
            <ul>
                <li v-for="(generals ,object) in general" :key="key"> {{ object }} : {{  generals }} </li>
            </ul>
        </div>
        </div>
            <button type="button" class="btn btn-primary mx-2" @click="showdata()">Click to see</button>
            <button type="button" class="btn btn-success mx-2" @click="plus(10)">Increment</button>
            <button type="button" class="btn btn-danger mx-2" @click="del(3)">Decrement</button>
        </div>


      <div class="container">

      </div>
    </div>
    </div>
    
  </div>
</div>
</div>
</template>

<script>

    export default{
        data(){
            return{
                firstName : 'Alongkon',
                lastName : 'Chanthiang',
                age : 8,
                address : 'Chonburi',
                picture : 'https://scontent.fbkk5-5.fna.fbcdn.net/v/t39.30808-6/336772762_734323044994253_2968445902711011451_n.jpg?stp=cp6_dst-jpg&_nc_cat=100&ccb=1-7&_nc_sid=8bfeb9&_nc_eui2=AeGu0aEAF8ZzqmwBk05fGanRq9wGi0Kk2Sar3AaLQqTZJgWBErq3apsxUgDBDYDPe3px0FH2lArFfj15wXeVH8g9&_nc_ohc=UPQWhn8RAdoAX9j503u&_nc_ht=scontent.fbkk5-5.fna&oh=00_AfB15siLjOIVK6vaOQTElGgNnJwldzMi2eGKlUtE0YsbEA&oe=64E30E30',
                size : 1000,
                hobby: ["codeing",'Playgame','Sleep'],
                general: {Gender:'Male',Weight:120,Height: 178,Status : false},
                nickname : ''
            }
        },
        methods: {
            getfullname(){
                return `${this.firstName} ${this.lastName} `
            },
            showdata(){
                alert(this.firstName)
            },
            plus(value){
                this.age += value
            },
            del(value){
                this.age -= value
            },
            setNickname(event){
                this.nickname=event.target.value
            },
            submitform(){
                alert("Save success")
            }
        }
    }
</script>