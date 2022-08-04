<template>
<div class="content bg-blue-200">
        <h1 class="text-center font-extrabold text-5xl mt-8 bg-blue-200">Shopping Product List</h1>

    <nav class="text-center font-bold text-xl mt-8 border-2 rounded-md border-black">
        <a>
            <select name="Category" id="watches" class="bg-blue-200">
                <option value="watch">Select Watches</option>
                <option value="watch">Titan</option>
                <option value="watch">Puma</option>
                <option value="watch">Ladies Wear</option>
                <option value="watch">G-Shock</option>
                <option value="watch">Rolex</option>
            </select>
            <select name="Category" id="mobile" class="bg-blue-200">
                <option value="mobile">Select Mobiles</option>
                <option value="mobile">Apple Iphone</option>
                <option value="mobile">Oneplus</option>
                <option value="mobile">Oppo</option>
                <option value="mobile">Vivo</option>
                <option value="mobile">Redmi</option>
                <option value="mobile">Samsung</option>
            </select>
            <select name="Category" id="earphone" class="bg-blue-200">
                <option value="earphone">Select Earphone</option>
                <option value="earphone">Apple Airpods</option>
                <option value="earphone">Oneplus Buds</option>
                <option value="earphone">Oppo Earphone</option>
                <option value="earphone">Vivo Earphones</option>
                <option value="earphone">Redmi Earphone</option>
                <option value="earphone">Samsung Earphones</option>
            </select>
            <select name="Category" id="shoes" class="bg-blue-200">
                <option value="shoes">Select Shoes</option>
                <option value="shoes">Formal Shoes</option>
                <option value="shoes">Casual Shoes</option>
                <option value="shoes">Nike Air</option>
                <option value="shoes">Puma Sports</option>
                <option value="shoes">Red Chief Leather</option>
                <option value="shoes">Loafers</option>
            </select><br>
            <div class="inline-flex p-4 mt-4">
                <div class="mr-8 border-2 px-2 border-black rounded-md"><a href="productlist2">Add Products</a></div>
                <div class="ml-8 border-2 px-2 border-black rounded-md"><a href="productform">filter</a></div>
            </div>
        </a>
    </nav>
    <div>
        <table class="mt-6">
            <tr class="border-2 rounded-md border-black">
                <td class="text-center p-2">
                    <div>
                        <img src="assets/watch.jpg" alt="showimage" class="px-64  items-center ">
                        <h3 class="font-bold text-xl">Watches</h3>
                        <p><b>This is black edition watches </b></p>
                        <h5><b>Rs 10,000/- only</b></h5>

                        <i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><br>
                        <button class="buy-1 border-2 px-2  border-black rounded-md">Buy Now</button>
                    </div>
                </td>
                <td class="p-2">
                    <div class="content text-center ">
                        <img src="assets/watch2.jpg" alt="showimage" class="px-64 items-center ">
                        <h3 class="font-bold text-xl">Watches</h3>
                        <p><b>This is simple watches </b></p>
                        <h5><b>Rs 11,200/- only</b></h5>
                        <i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><br>
                        <button class="buy-2 border-2 px-2  border-black rounded-md">Buy Now</button>
                    </div>
                </td>
            </tr>
            <tr class="border-2 rounded-md border-black">
                <td class="p-2">
                    <div class="content text-center">
                        <img src="assets/wooden color.jfif" alt="showimage" class="px-64  items-center">
                        <h3 class="font-bold text-xl">Watches</h3>
                        <p><b>This is wooden colour</b></p>
                        <h5><b>Rs 11,500/- only</b></h5>
                        <i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><br>
                        <button class="buy-3 border-2 px-2  border-black rounded-md">Buy Now</button>
                    </div>
                </td>
                <td class="p-2">
                    <div class="content text-center">
                        <img src="assets/Brown watches.jfif" alt="showimage" class="px-64  items-center">
                        <h3 class="font-bold text-xl">Watches</h3>
                        <p><b>This Brown Edition</b></p>
                        <h5><b>Rs 13,200/- only</b></h5>
                        <i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><i class="fa fa-star checked"></i><br>
                        <button class="buy-4 border-2 px-2  border-black rounded-md">Buy Now</button>
                    </div>
                </td>
            </tr>
        </table>
    </div>

</div>
</template>

