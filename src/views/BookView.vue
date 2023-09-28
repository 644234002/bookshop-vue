<template>
    <div>
        <h1>GGEZ BOOK</h1>
        <button @click="showMsg">Sweet Alert</button>
    </div>
</template>

<script setup>
import axios from "axios"
import {ref,onMounted} from 'vue'
import Swal from 'Sweetalert2'

const apiUrl=import.meta.env.VITE_API_URL+'/books'
const token="eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InVzZXIxOSIsInBhc3N3b3JkIjoiJDJhJDEwJDhXYmJsMXFEclQweDhvcUguMXNNM3VYYXFwbGpwQ2NrdTdrLlE4R0l1cEovZVcxT1dhcEQyIiwiaWF0IjoxNjk1ODczMDYzfQ.5Ao9YOQnpYq139pfHxreD-ZOaKcmKYKoNgA1UmXzdjU"
const books=ref([])

function showMsg(){
    Swal.fire({
//   position: 'top-end',
  icon: 'success',
  title: 'New book has been saved',
  showConfirmButton: false,
  timer: 1500
})
}

onMounted(async () => {
    //Get books
    // const response=await axios.get(apiUrl,{headers:{Authorization: 'bearer ' + token}})
    // books.value=response.data.data
    // console.log(books.value)

    /*
    const book=ref({
    title: "Data MiningX010X",
    isbn: "1234567890",
    pageCount: 304,
    publishedDate: new Date(),
    thumbnailUrl: "https://raw.githubusercontent.com/kesinee-bo/sp01/master/Books/unavailable.jpg",
    shortDescription: "Great Book...Highly recommended. -- Choice Magazine",
    author: "64",
    category: "Machine Learning",
    price: 100
    })

    const {data,error}=await axios.post(apiUrl, book.value, {headers:{Authorization: 'bearer ' + token}})
    
    if(error==null){
        console.log(data);
    }*/
})

</script>

<style scoped>

</style>