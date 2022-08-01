<template>
<main class="flex justify-center w-full h-screen">
    <div>
        <form action="" class="bg-gray-100 border-blue-400 rounded-lg border-2 px-12">
            <table>
                <h2 class="text-teal-900 text-xl font-bold pt-6">Product Information</h2>
                <hr />
                <br />
                <label class="pt-10 py-10 " for="pname">Product name:</label><br />
                <input type="text" v-model="user.pname" id="pname" name="pname"  /><br /><br />
                <label for="ppri">product price:</label><br />
                <input type="number" v-model="user.ppri" id="ppri" name="ppri"  /><br /><br />
                <label for="category"> product category: </label><br />
                <input type="text" v-model="user.category" id="category" name="category" placeholder="Enter your address" />
                <br /><br />
                <label for="color">product color: </label><br />
                <input type="text" v-model="user.color" id="color" name="color"  />
                <br /><br />
                <div>
                    <button class="py-1 px-5 mr-5 bg-cyan-500 hover:bg-cyan-500 shadow-lg shadow-cyan-500/50 text-white font-bold text-center rounded-md mb-3" type="submit" @click="proli" id="btnsub"> Add to Cart </button>
                    <button class="py-1 px-5 bg-cyan-500 hover:bg-cyan-500 shadow-lg shadow-cyan-500/50 text-white font-bold text-center rounded-md mb-3" type="reset"> Reset </button>
                </div>
            </table>
        </form>
        <br>
        <table class="list">
            <tr>
                <!-- <th class="px-4 border-black rounded-lg border-2">id</th> -->
                <th class="px-4 border-blue-400 rounded-lg border-4">Product ID</th>
                <th class="px-4 border-blue-400 rounded-lg border-4">Product Name </th>
                <th class="px-4 border-blue-400 rounded-lg border-4">Product Price</th>
                <th class="px-4 border-blue-400 rounded-lg border-4">Product Category</th>
                <th class="px-4 border-blue-400 rounded-lg border-4">Product Color</th>
                <th class="px-4 border-blue-400 rounded-lg border-4">Action</th>
            </tr>
            <tr v-for="(item,index) in users" v-bind:index="index" :key="item">
                <!-- <td class="px-4 border-black rounded-lg border-2">{{item.id=i+1}}</td> -->
                <td class="px-4 border-blue-400 rounded-lg border-4">{{item.id=i+1}}</td>
                <td class="px-4 border-blue-400 rounded-lg border-4">{{item.pname}}</td>
                <td class="px-4 border-blue-400 rounded-lg border-4">{{item.price}}</td>
                <td class="px-4 border-blue-400 rounded-lg border-4">{{item.category}}}</td>
                <td class="px-4 border-blue-400 rounded-lg border-4">{{item.color}}</td>
                <td class="px-4 border-blue-400 rounded-lg border-4">{{item.Action}}
                    <button class="mx-3 rounded-lg bg-red-600 hover:bg-red-700 text-white w-20" @click="userDelete(index)">
                        Delete
                    </button>
                    <button class="mx-3 rounded-lg bg-green-600 hover:bg-green-600 text-white w-20" @click="onEdit(index)">
                        Edit
                    </button>
                </td>
            </tr>
        </table>
    </div>
</main>
</template>
<script>
export default {
    name:"product-data",
    data() {
        return {
            isEdit:false,
            indexEdit:-1,
            users: [],
            user: {
                 id: 0,
                pname: "",
                price : "",
                category : "",
                color : "",
            },
        };
    },
    methods: {
        proli(event) {
            event.preventDefault();
            document.getElementById("btnsub").innerHTML='Submit'
            if(this.isEdit==true){
                this.users[this.indexEdit]=this.user;
                this.isEdit=false;
                this.indexEdit=-1;
                alert('Successfully Updated')
            }
            else{
                 this.users.push(this.user);
                 alert('Data Added')
            }
           this.user = {
                id: 0,
                pname: "",
                price : "",
                category : "",
                color : "",
            };
        },
        onReset(event) {
            event.preventDefault();
            this.form. id = "";
            this.form.pname = "";
            this.form.price = "";
            this.form.category = "";
            this.form.color=""
        },
        userDelete(index) {
            this.users.splice(index, 1)
        },
        onEdit(index){
          document.getElementById("btnsub").innerHTML='Update'
            this.user.pname=this.users[index].pname;
            this.user.price=this.users[index].price;
            this.user.category=this.users[index].category;
            this.user.color=this.users[index].color;
            // this.user.number=this.users[index].number;
            this.isEdit=true;
            this.indexEdit=index;
        }
    }
}
</script>