############### Titan APIs ####################

//Listing page

->Watches with respect to watchCollections or watchType
* https://titan-a1eo.onrender.com/watches?watchType=3
* https://titan-a1eo.onrender.com/watches?collectionId=4


->Filter based on watch brand and collection selected (GET)
* https://titan-a1eo.onrender.com/collectionFilter/2?brandId=5

->Filter based on watch price and collection selected(GET)
* https://titan-a1eo.onrender.com/collectionFilter/2?lprice=20000&hprice=30000

->Filter based on watch brand and watch type(GET)
* https://titan-a1eo.onrender.com/watchTypeFilter/1?brandId=5

->Filter based on watch price and watch type(GET)
* https://titan-a1eo.onrender.com/watchTypeFilter/1?lprice=8000&hprice=30000

->Sorting based on the price
* https://titan-a1eo.onrender.com/collectionFilter/2?sort=1



//Details page

->To show the details of selected watch(GET)
* https://titan-a1eo.onrender.com/details?watchId=20


//cart page
->To show the items added to cart (POST)
* https://titan-a1eo.onrender.com/cart
body:
 { 
    "id":[ 11,34,23,9 ] 
    }

->To place the order (POST)
* https://titan-a1eo.onrender.com/placeOrder
body { 
    "orderId": 3, 
    "name": "Amit", 
    "email": "amit@gmail.com", 
    "address": "Hom 35", 
    "phone": 8934645457, 
    "cost": 833, 
    "cartItem": [ 11,34,23 ] 
}

//Orders

->List of orders (GET)
* https://titan-a1eo.onrender.com/orders

-> List of orders wrt to email (GET)
* https://titan-a1eo.onrender.com/orders?email=vik@gmail.com

->Update payment details (PUT)
* https://titan-a1eo.onrender.com/updateOrder/2
body{
    "status":"Delivered",
    "bank_details":"HDFC Bank",
    "date":"15-11-2022" 
}

->Delete order (DELETE)
* https://titan-a1eo.onrender.com/deleteOrder/6372a91f116bbb14cd7bd024





################ Login App APIs ###################

>to show the users(GET)
* https://userlogin-h5v5.onrender.com/api/auth/users

>Register the user (POST)
* https://userlogin-h5v5.onrender.com/api/auth/register
body{
    "name":"Vinayak2",
    "email":"vik2@gmail.com",
    "password":"123",
    "phone":123456789
}

>Login (POST)
* https://userlogin-h5v5.onrender.com/api/auth/login
body{
    "email":"vik2@gmail.com",
    "password":"123"
}

>User Information (GET)
* https://userlogin-h5v5.onrender.com/api/auth/userInfo
Header{
    x-access-token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjYzN2RmMTg2ZmM3Y2JjZDVmYTQ2NmY2MiIsImlhdCI6MTY2OTIwMDQ3MCwiZXhwIjoxNjY5Mjg2ODcwfQ.HbsSHwYe3ZGlD09ly7Wk2TSSjS9V4ow1uF_uZXSjRzQ
}