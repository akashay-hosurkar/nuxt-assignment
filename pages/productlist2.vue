<template>
<div>
    
    <div class="border-solid border-2 border-black drop-shadow-md bg-gradient-to-r from-cyan-300 to-blue-200 ">
        <form >
            <h1 style="color: black" class="font-bold text-3xl p-2">Shopping Product List</h1>
            <table >
                <tr class="text-center">
                    <td><label>Product Name :</label></td>
                    <td><input type="text" v-model="prodata.pname" class="bg-white border border-slate-300 rounded-md py-2 pl-9 pr-3 m-5"></td>
                </tr>
                <tr>
                    <td><label>Product Price :</label></td>
                    <td><input type="number" v-model="prodata.price" class="bg-white border border-slate-300 rounded-md py-2 pl-9 pr-3 m-5"></td>
                </tr>
                <tr>
                    <td><label>Product Category:</label></td>
                    <td><input type="text" v-model="prodata.category" class="bg-white border border-slate-300 rounded-md py-2 pl-9 pr-3 m-5"></td>
                </tr>
                <tr>
                    <td><label>Product Color :</label></td>
                    <td><input type="text" v-model="prodata.color" class="bg-white border border-slate-300 rounded-md py-2 pl-9 pr-3 m-5"></td>
                </tr>
                <tr>
                    <td>
                        <button type="button" class=" mb-10 border-solid font-extrabold rounded border-2 border-black p-3 bg-gray-300 bg-hover-black" @click="login" id="btnsub">
                            Submit
                        </button>
                    </td>
                </tr>
            </table>
        </form>
    </div>
    <!--<div class="bg-gray-300 col-span-2 flex" v-for="(prod) in myarr" :key="prod">   
        <div class="m-10 h-52 w-52 border-4 border-black" >
            <img src="assets/show1.jfif" class="h-45 w-45">
            product Name: <b>{{this.formdata.pname}}</b>
            Product price: <b>{{this.formdata.price}}</b>
            Product Category <b>{{this.formdata.category}}</b>
            Product Color <b>{{this.formdata.category}}</b>
         </div>
        <div class="m-10 h-52 w-52 border-4 border-black" >
            <img src="assets/show2.jfif" class="h-45 w-45"> 
            product Name: <b>{{formdata.pname}}</b>
            Product price: <b>{{formdata.price}}</b>
            Product Category <b>{{formdata.category}}</b>
            Product Color <b>{{formdata.category}}</b>
        </div>
        <div class="m-10 h-52 w-52 border-4 border-black" >
            <img src="assets/shoe3.jfif" class="h-45 w-45">
            product Name: <b>{{formdata.pname}}</b>
            Product price: <b>{{formdata.price}}</b>
            Product Category <b>{{formdata.category}}</b>
            Product Color <b>{{formdata.category}}</b>
        </div> -->
    <table class="border-2  bg-gray-100 mr-60 ml-60 p-6 border-solid border-black rounded-md mt-4 ">
        <tr>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">ID</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Image</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Name</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Price</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Category</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Color</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Delete</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Edit Data</td>
        </tr>
        <tr v-for="(item,index) in proarr" :key="item">
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8">{{item.id = index + 1}}</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8"><img src="assets/sneaker.jpg" alt="image"></td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8">{{item.pname}}</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8">{{item.price}}</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8">{{item.category}}</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8">{{item.color}}</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8"><button class=" border-2 font-bold rounded-md bg-red-300 text-blue-500 hover:bg-black  text-white p-2 text-center"  @click="deleteIndex(index)">Delete</button></td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8"><button class=" border-2 font-bold rounded-md bg-green-500 text-blue-500 hover:bg-black  text-white p-2 text-center"  @click="editIndex(index)">Edit</button></td>
        </tr>
    </table>
</div>
</template>

<script>
export default {
    name: 'formdataproduct',
    data() {
        return {
            isEdit: false,
            indexEdit: -1,
            userAddress : "",
            proarr: [],
            prodata: {
                pname: "",
                price: "",
                category: "",
                color: "",
                image : "",
            },
        };
    },
    methods: {
        createNewCard() {
            this.proarr.push(this.prodata);
        },
        login(event) {
            event.preventDefault();
            document.getElementById("btnsub").innerHTML='Submit'
            if (this.isEdit == true) {
                this.proarr[this.indexEdit] = this.prodata;
                this.isEdit = false;
                this.indexEdit = -1;
                alert('Successfully Updated')
            } else {
                this.proarr.push(this.prodata);
                 alert('Data Added')
            }
            this.prodata = {
                id: 0,
                pname: "",
                price: "",
                category: "",
                color: "",
                image : "",
            }
            console.log("prodata is :", this.proarr);
        },
        deleteIndex(index) {
            this.proarr.splice(index, 1);
        },
        editIndex(index) {
            document.getElementById("btnsub").innerHTML='Update'
            this.prodata.pname = this.proarr[index].pname;
            this.prodata.price = this.proarr[index].price;
            this.prodata.category = this.proarr[index].category;
            this.prodata.color = this.proarr[index].color;
            this.prodata.image = this.proarr[index].image;
            this.isEdit = true;
            this.indexEdit = index;
        },
    }
}
</script>