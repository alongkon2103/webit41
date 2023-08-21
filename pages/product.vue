<template>
      <Head>
    <Title>Alongkon | Product</Title>
  </Head>
  <div v-if="pending">
    Loading ...
  </div>
  <div v-else>
    <div class="container d-flex justify-content-center">
    <form class="w-50 my-5 ">
        <div class="input-group flex-nowrap w-100">
  <input type="text" class="form-control shadow-none" placeholder="Search" aria-label="Username" aria-describedby="addon-wrapping">
  <button type="submit" class="btn btn-success"><i class="bi bi-search"></i></button>
</div>  

</form>
</div>
        <div class="container">
        <div class="grid mb-5">
            <div class="content"  v-for="products in datas">
            <div class="item w-100 h-100 rounded-1" style="border: 0.1px solid black;">
                      <div class="content p-3 " style="height: 90%;">
                        	<img class="priceimg w-50" :src=products.image alt="">
                        <h6 class="text-center mt-3">{{ products.title }}</h6>
                       
                      </div>
                      <p class="mx-2">Studios : {{ products.studios }} </p>
                    </div>
                </div>
        </div>
        </div>
    </div>
   

</template>

<script setup>
const { pending, data: datas } = await useFetch('http://localhost:8081/products')
  console.log(datas)
</script>

<style scope>
.grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    column-gap: 16px;
    row-gap: 30px;
}

.item:hover {
    box-shadow: -2px 5px 32px -11px rgba(0, 0, 0, 0.86);
}

.item {
    transition: 0.2s;
}
.priceimg{
    display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
}

</style>
