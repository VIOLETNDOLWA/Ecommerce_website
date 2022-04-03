 Plans to create Ecommerce website with vanilla javascript

1. Create Folder Structure
  1. create root folder as Fully Ecommerce website
  2. add frontend and backend folder
  3. create src folder in frontend folder
  4. create index.html
  5. rum npm init or npm init --yes to install package.json in frontend folder
  6. run npm install -D live-server to install live server
  7. add start command as live-server src --verbose
  8. run npm start

2. Design website
    1. create style.css
    2. link style.css to index.html
    3. create div,grid-ontainer
    4. create header,main and footer
    5. style html, body
    6. style grid-container, header,main and footer

3. Create statics Home Screen 
   1. create ul.products
   2. create li
   3. create div.product
   4. add .product-image, .product-name, .product-price, .product-brand
   5. style ul.products and internal divs
   6. duplicate 2 times to show 3 products

 4. Render dynamic Home screen
    1. create dat.js
    2. export an array of 6 products
    3. create screen/HomeScreen.js
    4. export home screen as an object with render() method
    5. implement render()
    6. import data.js
    7. return products mapped to lis inside an ul
    8. create app.js
    9. link it to index.html as module
    10. set main id to main_container
    11. create router() function
    12. set main_container innerHTML to HomeScreen.render()
    13. set load event of window to router() function

5. Build Url router
    1. create routes as route:screen object for home screen
    2. create utils.js
    3. export parseRequestURL()
    4. set url as hash address split by slash
    5. return resources, id and verb of url
    6. update router()
    7. set request as parseRequestURL()
    8. build parseurland compare with routes
    9. if route exist render it, else rendor Error404
    10. create screens/Error404.js and rendor error message

6. Create Node.js server
    1. run npm init or npm init --yes in root  Fully ecomerce website folder  
    2. run npm install express to install express
    3. create server.js
    4. add start command as node backend/server.js
    5. require express
    6. move data.js from frontend to backend
    7. create route for /api/products
    8. return products in data.js
    run npm start

7. load products from backend
   1. edit HomeScreen.js
    2. make render async
    3. fetch products from '/api/products' in render()
    4. make router() async and call await HomeScreen.render()
   5. use cors on backend :install using npm istall cors

8. Add webpack
  1. cd frontend
  2. npm install -D webpack webpack-cli webpack-dev-server
  3. npm uninstall live-server
  4. "start": "webpack-dev-server --node development --watch-content-base --open"
  5. move idex.html, style.css and images to frontend folder
  6. rename app.js to index.js
  7. update index.html
  8. add <script src="main.js"></script>
  9. npm start
  10. npm install axios
  11. change fetch to axios in HomeScreen   


    


