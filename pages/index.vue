<template>
<div class="content bg-blue-200">
    
    <h1 class="text-center font-extrabold text-5xl mt-8 bg-blue-200">Shopping Product List</h1>

    <nav class="text-center font-bold text-xl mt-8 ">
        <a>

            <select name="Category" id="shoes" class="bg-blue-200">
                <option value="shoes">Select watches</option>
                <option value="shoes">Formal watches</option>
                <option value="shoes">Casual watches</option>
                <option value="shoes">Nike watches</option>
                <option value="shoes">Puma Sports watches</option>
                <option value="shoes">Leather Belt watches</option>
                <option value="shoes">Diesel watches</option>
            </select><br>
        </a>
    </nav>
    <div>
        <table class="mt-6">
            <tr class="border-2 rounded-md border-black">
                <td class="text-center p-2">
                    <div>
                        <img src="assets/Diesel.jpg" alt="showimage" class="px-64  items-center ">
                        <h3 class="font-bold text-xl">Diesel</h3>
                        <p><b>This is  Diesel Brand</b></p>
                        <h5><b>Rs 10,000/- only</b></h5>

                        <i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><br>
                        <!-- <button class="buy-1 border-2 px-2  border-black rounded-md">Buy Now</button> -->
                    </div>
                </td>
                <td class="p-2">
                    <div class="content text-center ">
                        <img src="assets/watch2.jpg" alt="showimage" class="px-64 items-center ">
                        <h3 class="font-bold text-xl">Casio</h3>
                        <p><b>This is Casio Brand</b></p>
                        <h5><b>Rs 11,200/- only</b></h5>
                        <i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><br>
                        <!-- <button class="buy-2 border-2 px-2  border-black rounded-md">Buy Now</button> -->
                    </div>
                </td>
            </tr>
            <tr class="border-2 rounded-md border-black">
                <td class="p-2">
                    <div class="content text-center">
                        <img src="assets/Brown watches.jfif" alt="showimage" class="px-64  items-center">
                        <h3 class="font-bold text-xl">Rolex</h3>
                        <p><b>This is Rolex Brand</b></p>
                        <h5><b>Rs 11,500/- only</b></h5>
                        <i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><br>
                        <!-- <button class="buy-3 border-2 px-2  border-black rounded-md">Buy Now</button> -->
                    </div>
                </td>
                <td class="p-2">
                    <div class="content text-center">
                        <img src="assets/watch.jpg" alt="showimage" class="px-64  items-center">
                        <h3 class="font-bold text-xl">Matrix</h3>
                        <p><b>This is Matrix Brand</b></p>
                        <h5><b>Rs 13,200/- only</b></h5>
                        <i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><br>
                        <!-- <button class="buy-4 border-2 px-2  border-black rounded-md">Buy Now</button> -->
                    </div>
                </td>
            </tr>
        </table>
    </div>

</div>
<!-- 1st from statrs -->
<div>
    <title>
        Productlist Project
    </title>
    <h1 class="text-center font-bold text-5xl mt-4 bg-blue-200">Form To Add Products</h1>
    <hr class="mt-5 border-1 border-black">
    <div class="sm  border-4 bg-blue-300 mr-60 ml-60 p-6 border-solid border-black rounded-md mt-6 ">
        <form action="" name="myForm" onsubmit="return validateForm()" method="post">
            <div class="justify-between p-1 sm">
                <label class="font-semibold text-xl mr-16" for="pname">Product Name</label>
                <input class="ml-16 border-2 px-32" type="text" v-model="formdata.pname" name="pname" id="pname" @change="validationName" required>
            </div>
            <div class="p-1">
                <label class="font-semibold text-xl mr-16" for="price">Product Price</label>
                <input class="ml-16  border-2 px-32 " type="number" v-model="formdata.price" name="price" id="price" @change="validationPrice" required>
            </div>
            <div class="p-1">
                <label class="font-semibold text-xl mr-16" for="category">Product Category</label>
                <input class="ml-8 border-2 px-32" type="text" v-model="formdata.category" name="category" id="category" @change="validationCategory" required>
            </div>
            <div class="p-1">
                <label class="font-semibold text-xl mr-16" for="color">Product color</label>
                <input class="ml-16 border-2 px-32" type="text" v-model="formdata.color" name="color" id="color" @change="validationColor" required>
            </div>
            <div class="p-1  mt-6">
                <button class="ml-16 border-2 font-bold mr-16 rounded-md hover:bg-green-800  bg-orange-800 text-blue-500 hover:bg-black  text-white p-2 text-center shadow-lg shadow-black" type="submit" @click="addpro">Add Product</button>
                <button class="ml-16 border-2 font-bold mr-16 rounded-md bg-neutral-900 hover:bg-orange-500 text-blue-500 hover:bg-red-500  text-white p-2 text-center shadow-lg shadow-yellow-900" type="reset">Reset</button>
            </div>
        </form>
        <table border="2" class="border-2  bg-gray-100 mr-60 ml-32 p-6 border-solid border-black rounded-md mt-8 ">
            <tr>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product ID</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Name </td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Price</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Category</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Color</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Delete</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Edit Data</td>
            </tr>
            <tr v-for="(item,i) in myarr" :key="item">
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{item.id = i + 1}}</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{item.pname}}</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{item.price}}</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{item.category}}</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{item.color}}</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8"><button class=" border-2 font-bold rounded-md bg-green-500 hover:bg-black  text-white p-2 text-center" @click="deletepro(i)">Delete</button></td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8"><button class=" border-2 font-bold rounded-md bg-green-500 hover:bg-black  text-white p-2 text-center" @click="editpro(i)">Edit</button></td>
            </tr>
        </table>

        <div>
            <label class="font-bold text-xl mr-16" for="searchpro">Search Product</label>
            <input @keyup="userFindByAddress(userAddress)" v-model="this.userAddress" class="ml-2 mt-8 border-2 px-32" type="text" name="searchpro" id="searchpro">
            <!-- <button class=" border-2 font-bold rounded-md bg-red-300 text-blue-500 hover:bg-black  text-white p-2 text-center" type="search" @click="this.userFindByAddress(userAddress)">Search</button> -->
        </div>
        <hr class="border-1 border-black">
        <!-- 2nd table  -->
        <table border="2" class="border-2  bg-gray-100 mr-60 ml-32 p-6 border-solid border-black rounded-md mt-8 ">
            <tr>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product ID</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Name </td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Price</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Category</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Color</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Delete</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Edit Data</td>
            </tr>
            <tr v-for="(prod,i) in userFound" :key="prod">
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{prod.id = i + 1}}</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{prod.pname}}</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{prod.price}}</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{prod.category}}</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{prod.color}}</td>
            </tr>
        </table>

    </div>
</div>
<!-- 1st from end -->
<!-- 2ndfrom starts  -->
<div>

    <!-- <div class="border-solid border-2 border-black drop-shadow-md bg-gradient-to-r from-cyan-300 to-blue-200 ">
        <form action="" method="post">
            <h1 style="color: black" class="font-bold text-3xl p-1 bg-cyan-300 text-center">Shopping Product List</h1>
            <table class="ml-96">
                <tr class="text-center">
                    <td><label>Product Name :</label></td>
                    <td><input type="text" v-model="formdata.pname" class="bg-white border border-slate-300 rounded-md py-2 pl-9 pr-3 m-5" @change="validationName" required></td>
                </tr>
                <tr>
                    <td><label>Product Price :</label></td>
                    <td><input type="number" v-model="formdata.price" class="bg-white border border-slate-300 rounded-md py-2 pl-9 pr-3 m-5" @change="validationPrice" required></td>
                </tr>
                <tr>
                    <td><label>Product Category:</label></td>
                    <td><input type="text" v-model="formdata.category" class="bg-white border border-slate-300 rounded-md py-2 pl-9 pr-3 m-5" @change="validationCategory" required></td>
                </tr>
                <tr>
                    <td><label>Product Color :</label></td>
                    <td><input type="text" v-model="formdata.color" class="bg-white border border-slate-300 rounded-md py-2 pl-9 pr-3 m-5" @change="validationColor" required></td>
                </tr>
                <tr>
                    <td>
                        <button type="button" class="mb-5 border-solid font-extrabold rounded border-2 border-black p-3 bg-gray-300 bg-hover-black" @click="login">
                            Submit
                        </button>
                    </td>
                </tr>
            </table>
        </form>
    </div> -->

    <!-- <div>
        <h1 class="font-semibold text-center text-3xl p-2 bg-blue-300"><b>My Cart</b></h1>
    </div> -->
    <div>
        <table class="border-2  bg-gray-100 mr-60 ml-60 p-6 border-solid border-black rounded-md mt-4">
            <!-- <tr>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">ID</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Image</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Name</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Price</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Category</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Color</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Delete</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Edit Data</td>
            </tr> -->
            <tr v-for="(item,i) in myarr" :key="item">
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{item.id = i + 1}}</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8"><img src="assets/wooden color.jfif" alt="image"></td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{item.pname}}</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{item.price}}</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{item.category}}</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8">{{item.color}}</td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8"><button class=" border-2 font-bold rounded-md bg-red-300 text-blue-500 hover:bg-black  text-white p-2 text-center" @click="deleteIndex(i)">Delete</button></td>
                <td class="border-2  bg-gray-100 p-2 border-solid border-black rounded-md mt-8"><button class=" border-2 font-bold rounded-md bg-green-500 text-blue-500 hover:bg-black  text-white p-2 text-center" @click="editIndex(i)">Edit</button></td>
            </tr>
        </table>
    </div>

    <table class="border-2  bg-gray-100 mr-60 ml-60 p-6 border-solid border-black rounded-md mt-4 ">
        <!-- <tr>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">ID</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Image</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Name</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Price</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Category</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Product Color</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Delete</td>
            <td class="border-2  bg-blue-100 p-2 border-solid border-black rounded-md mt-8 font-bold">Edit Data</td>
        </tr> -->
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
    name: "product-data",
    data() {
        return {
            isEdit: false,
            indexEdit: -1,
            userAddress: "",
            myarr: [],
            formdata: {
                id: 0,
                pname: "",
                price: "",
                category: "",
                color: "",
            }
        }
    },
    methods: {
        addpro(event) {
            event.preventDefault();
            //validation name
            if (!isNaN(this.formdata.pname) || this.formdata.pname == null || this.formdata.pname == "") {
                alert("Please Enter Name");
                // console.log("Please Enter Name");
                this.resetForm();
            } else {
                console.log(this.formdata.pname);
                // alert("Name is valid");
            }
            // //vali price
            if (isNaN(this.formdata.price) || this.formdata.price == "") {
                // if( !isNaN(this.formdata.price) || !this.formdata.price==null || !this.formdata.price==""  ){
                // || this.formdata.price==""
                alert("Please Enter price");
                // console.log("Please Enter price");
                this.resetForm();
            } else {
                console.log(this.formdata.price);
                alert("price is valid");
            }
            //vali cate
            if (!isNaN(this.formdata.category) || this.formdata.category == null || this.formdata.category == "") {
                alert("Please Enter category");
                // console.log("Please Enter category");
                this.resetForm();
            } else {
                console.log(this.formdata.category);
                // alert("categoy is valid");
            }
            //vali color
            if (!isNaN(this.formdata.color) || this.formdata.color == null || this.formdata.color == "") {
                alert("Please Enter color");
                // console.log("Please Enter color");
                this.resetForm();
            } else {
                console.log(this.formdata.color);
                // alert("Name is color");
            }
            //other if else condition
            if (this.isEdit == true) {
                this.myarr[this.indexEdit] = this.formdata;
                this.isEdit = false;
                this.indexEdit = -1;
            } else {
                this.myarr.push(this.formdata);
            }
            this.formdata = {
                id: 0,
                pname: "",
                price: "",
                category: "",
                color: "",
            }
            console.log("Formdata is :", this.myarr);
        },
        deletepro(index) {
            this.myarr.splice(index, 1);
        },
        editpro(index) {
            this.formdata.pname = this.myarr[index].pname;
            this.formdata.price = this.myarr[index].price;
            this.formdata.category = this.myarr[index].category;
            this.formdata.color = this.myarr[index].color;
            this.isEdit = true;
            this.indexEdit = index;
        },
        userpro(userName) {
            console.log(userName);
            this.userFound = this.myarr.filter((e) => {
                if (e.pname == userName) {
                    // this.userFound.push(e);
                    console.log(e);
                    return e;
                    // alert("user Found" + e.firstName+ ""+e.lastName);
                }
            });
            // console.log(find1);
            console.log(this.userFound);
        },
        userFindByAddress(userAddress) {
            // console.log(userAddress);
            this.userFound = this.myarr.filter((e) => {
                // if (e.pname == userAddress)
                this.pname1 = userAddress.toLocaleLowerCase();
                this.pname2 = e.pname.toLocaleLowerCase();
                this.price1 = userAddress.toString();
                this.price2 = e.price.toString();
                this.category1 = userAddress.toLocaleLowerCase();
                this.category2 = e.category.toLocaleLowerCase();
                this.color1 = userAddress.toLocaleLowerCase();
                this.color2 = e.color.toLocaleLowerCase();
                if (this.pname2.startsWith(this.pname1) || this.price2.startsWith(this.price1) || this.category2.startsWith(this.category1) || this.color2.startsWith(this.color1)) {
                    console.log(e);
                    return e;
                }
            });
            console.log(this.userFound);
        },
        createNewCard() {
            this.myarr.push(this.formdata);
        },
        login(event) {
            event.preventDefault();
            //validation
            if (!isNaN(this.formdata.pname) || this.formdata.pname == null || this.formdata.pname == "") {
                alert("Please Enter Name");
                // console.log("Please Enter Name");
                this.resetForm();
            } else {
                console.log(this.formdata.pname);
                // alert("Name is valid");
            }
            //vali price
            if (isNaN(this.formdata.price) || this.formdata.price == "") {
                // if( !isNaN(this.formdata.price) || !this.formdata.price==null || !this.formdata.price==""  ){
                // || this.formdata.price==""
                alert("Please Enter price");
                // console.log("Please Enter price");
                this.resetForm();
            } else {
                console.log(this.formdata.price);
                alert("price is valid");
            }
            //vali cate
            if (!isNaN(this.formdata.category) || this.formdata.category == null || this.formdata.category == "") {
                alert("Please Enter category");
                // console.log("Please Enter category");
                this.resetForm();
            } else {
                console.log(this.formdata.category);
                // alert("categoy is valid");
            }
            //vali color
            if (!isNaN(this.formdata.color) || this.formdata.color == null || this.formdata.color == "") {
                alert("Please Enter color");
                // console.log("Please Enter color");
                this.resetForm();
            } else {
                console.log(this.formdata.color);
                // alert("Name is color");
            }
            if (this.isEdit == true) {
                this.myarr[this.indexEdit] = this.formdata;
                this.isEdit = false;
                this.indexEdit = -1;
            } else {
                this.myarr.push(this.formdata);
            }
            this.formdata = {
                id: 0,
                pname: "",
                price: "",
                category: "",
                color: "",
                image: "",
            }
            console.log("Formdata is :", this.myarr);
        },
        deleteIndex(index) {
            this.myarr.splice(index, 1);
        },
        editIndex(index) {
            this.formdata.pname = this.myarr[index].pname;
            this.formdata.price = this.myarr[index].price;
            this.formdata.category = this.myarr[index].category;
            this.formdata.color = this.myarr[index].color;
            this.formdata.image = this.myarr[index].image;
            this.isEdit = true;
            this.indexEdit = index;
        },
    }
}
</script>
