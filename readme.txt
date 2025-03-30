1. First we are going to make the logo of our homepage for that we will use a section tag with id "header" and inside that we will use an anchor tag and inside it in the img tag we will give our logo.
<section id="header">
        <a href="#"><img src="img/logo.png" class="logo" alt=""></a>
    </section>

2. Now for the navbar we will create a div and inside that we will create an unordered list with an id "navbar" and paste the various pages.
<div>
            <ul id="navbar">
                <li><a href="index.html">Home</a></li>
                <li><a href="shop.html">Shop</a></li>
                <li><a href="blog.html">Blog</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="contact.html">Contact</a></li>
                <li><a href="cart.html"><i class="fa-light fa-bag-shopping"></i></a></li>
            </ul>
        </div>

We also have to import font-awesome cdn- <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.15.4/css/all.css"/>

3. Now i have copied some inbuild css.

4. Now some css for header-
#header{
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px 80px;
    background: rgb(246, 240, 240);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.06);
}

5. Now to style navbar-
#navbar{
    display: flex;
    align-items: center;
    justify-content: center;
}

#navbar li{
    list-style: none;
    padding: 0 20px;
}

#navbar li a{
    text-decoration: none;
    font-size: 16px;
    font-weight: 600;
    color: #1a1a11;
}

#navbar li a:hover{
    color: #088178;
}

6. Now I want to highlight my home page to show i am currently in homepage. So i will give a class active like this-<li><a class="active" href="index.html">Home</a></li>
and to style it this will be the css-
#navbar li a:hover,
#navbar li a.active{
    color: #088178;
}

7. Now I want to set underline for the pages in navbar when i hover on that-
#navbar li a.active::after,  -->this is pseudo class
#navbar li a:hover::after{
  content: "";
  width: 30%;
  height: 2px;
  background: #088178;
  position: absolute;
  bottom: -4px;
  left: 20px;
}

also i have to set position:relative in #navbar li as because it is the parent element.

---------------------------------------------------------------------The Navbar is finished-------------------------------------------------------------------------------------------------

1. Now for the image in homepage we will give a section tag with id hero and paste some text like this-
<section id="hero">
        <h4>Trade-in-Offer</h4>
        <h2>Super value deals</h2>
        <h2>On all products</h2>
        <p>Save more with coupons & up to 70% off!</p>
        <button>Shop Now</button>
    </section>
2. Now the css for the image-
#hero{
  background-image: url("img/hero4.png");
  height: 90vh;
  width: 100%;
  background-size: cover;
  background-position: top 25% right 0;
  padding: 0 80px;
  display: flex;
  flex-direction: column;  -->this is because the flex direction normally is row wise
  align-items: flex-start;
  justify-content: center;
}

3. Now we have to style the text and the button -
#hero h4{
  padding-bottom: 15px;
}

#hero h1{
  color: #088178;
}

#hero button{
  background-image: url("img/button.png");
  background-color: transparent;
  color: #088178;
  border: 0;
  padding: 14px 80px 14px 65px;
  background-repeat: no-repeat;
  cursor: pointer;
  font-weight: 700;
  font-size: 15px;
}

4. Also we will see that the shadow-box is not showing under the navbar so we have to give a z-index in the header like this-
#header{
    z-index: 999;
    position: sticky;
    top: 0;
    left: 0;
}

-------------------------------------------------------------------------The Hero section is finished---------------------------------------------------------------------------------------

1. To add features first we will add a section tag with id feature and inside it a div tag with cla fe-box and inside we paste the image and the text-
<section id="feature">
        <div class="fe-box">
            <img src="img/features/f1.png" alt="">
            <h6>Free Shipping</h6>
        </div>
    </section>

2. Now to add padding between hero and feature we will give class to section tag as .section-p1 which has padding of 40px 80px.

3. Now we will add a box around the first box-
#feature .fe-box{
  width: 180px;
  text-align: center;
  padding: 25px 15px;
  box-shadow: 20px 20px 34px rgba(0, 0, 0, 0.03);
  border: 1px solid #cce7d0;
  border-radius: 4px;
  margin: 15px 0;
}

4. Now tro hover around the box the css will be-
#feature .fe-box:hover{
  box-shadow: 10px 10px 54px rgba(70, 62, 221, 0.1);
}

5. For the image insisde the box-{
#feature .fe-box img{
  width: 100%;
  margin-bottom: 10px;
}

6.The text inside the box-
#feature .fe-box h6{
  display: inline-block;
  padding: 9px 8px 6px 8px;
  line-height: 1;
  border-radius: 4px;
  color: #088178;
  background-color: #fddde4;
}

7. Now we will repeat it for 5 more boxes and to provide different colors we will use n-th child like this-
#feature .fe-box:nth-child(2) h6{
  background-color: #cdebbc;
}

#feature .fe-box:nth-child(3) h6{
  background-color: #d1e8f2;
}

#feature .fe-box:nth-child(4) h6{
  background-color: #cdd4f8;
}

#feature .fe-box:nth-child(5) h6{
  background-color: #f6dbf6;
}

#feature .fe-box:nth-child(6) h6{
  background-color: #fff2e5;
}
--------------------------------------------------------------------------------------End of feature----------------------------------------------------------------------------------------

1. Now for the product first-
<section id="product1" class="section-p1">
        <h2>Featured products</h2>
        <p>Summer Collection New Modern Design</p>
        <div class="pro-container">
            <div class="pro">
                <img src="img/products/f1.jpg" alt="">
                <div class="des">
                    <span>adidas</span>
                    <h5>Cartoon Astronaut T-Shirts</h5>
                    <div class="star">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <h4>$78</h4>
                </div>
                <a href="#"><i class="fal fa-shopping-cart"></i></a>
            </div>
        </div>
    </section>
This is for one product

2.Now we have to style it-
#product1{
  text-align: center;
} -->This will center the text  of h2 and p tag

#product1 .pro-container{
  display: flex;
  justify-content: space-between;
  padding-top: 20px;
  flex-wrap:wrap;
}  -->When we will add multiple product inside the div class="pro-container" we have to allign them in same row so we need it 

#product1 .pro{
  width: 23%;
  min-width: 250px;
  padding: 10px 12px;
  border: 1px solid #cce7d0;
  border-radius: 25px;
  cursor: pointer;
  box-shadow: 20px 20px 30px rgba(0, 0, 0, 0.02);
  margin: 15px 0;
  transition: 0.2s ease;
  position: relative; -->for the cart logo to be visible inside the box we need to set position relative because it is its parent class
}

#product1 .pro:hover{
  box-shadow: 20px 20px 30px rgba(0, 0, 0, 0.06);
}

#product1 .pro img{
  width: 100%;
  border-radius: 20px;
}

#product1 .pro .des{
  text-align: start;
  padding: 10px 0;
}

#product1 .pro .des span{
  color: #606063;
  font-size: 12px;
}

#product1 .pro .des h5{
  padding-top: 7px;
  color: #1a1a11;
  font-size: 14px;
}

#product1 .pro .des i{
  font-size: 12px;
  color: rgb(243, 181, 25);
}

#product1 .pro .des h4{
  padding-top: 7px;
  font-size: 15px;
  font-weight: 700;
  color: #088178;
}

#product1 .pro .cart{
  width: 40px;
  height: 40px;
  line-height: 40px;
  border-radius: 50px;
  background-color: #e8f6ea;
  font-weight: 500;
  color: #088178;
  border: 1px solid #cce7d0;
  position: absolute;
  bottom: 20px;
  right: 10px;
}

3. Now we will change the images.
----------------------------------------------------------------------------------------End of feature--------------------------------------------------------------------------------------

1. For Banner first we will create a section with idd banner and class section-m1 and add text and button like this-
<section id="banner" class="section-m1">
        <h4>Repair Services</h4>
        <h2>Up to <span>70% Off</span> - All T-Shirts & Accessories</h2>
        <button class="normal">Explore More</button>
    </section>

2. Now Css for banner-
#banner{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-image: url("img/banner/b2.jpg");
  width: 100%;
  height: 40vh;
  background-size: cover;
  background-position: center;
}

#banner h2{
  color: #fff;
  padding: 10px 0;
}

#banner h4{
  color: #fff;
}

#banner h2 span{
  color: #ef3636;
}

3. Now we will create an universal button class normal and add css like this-
button.normal{
  font-size: 14px;
  font-weight: 600;
  padding: 15px 30px;
  color: black;
  background-color: white;
  border-radius: 4px;
  cursor: pointer;
  border: none;
  outline: none;
  transition: 0.2s;
}

Now we will add hover effect-
#banner button:hover{
  background: #088178;
  color: white;
}

Now we will create a section with new arrival same as product section.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
1. Now to create two small banners-
<section id="sm-banner" class="section-p1">
        <div class="banner-box">
            <h4>Crazy deals</h4>
            <h2>Buy 1 get 1 Free</h2>
            <span>The best classic dress is on sale at cara</span>
            <button class="white">Learn More</button>
        </div>
        <div class="banner-box banner-box2">  ->we are creating second class just to change the background image
            <h4>Spring/Summer</h4>
            <h2>Upcoming Season</h2>
            <span>The best classic dress is on sale at cara</span>
            <button class="white">Collection</button>
        </div>
    </section>

2. Now the css-
#sm-banner{
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

#sm-banner .banner-box{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  background-image: url("img/banner/b17.jpg");
  min-width: 580px;
  height: 50vh;
  background-size: cover;
  background-position: center;
  padding: 30px;
}

#sm-banner .banner-box2{
  background-image: url("img/banner/b10.jpg");
}

#sm-banner h4{
  color: #fff;
  font-size: 20px;
  font-weight: 300;
}

#sm-banner h2{
  color: #fff;
  font-size: 28px;
  font-weight: 800;
}

#sm-banner span{
  color: #fff;
  font-size: 14px;
  font-weight: 500;
  padding-bottom: 15px;
}

#sm-banner .banner-box:hover button{
  background: #088178;
  border: 1px solid #088178;
}

Also to change the button we will use the universal button css along with class white and the css will be-
button.white{
  font-size: 13px;
  font-weight: 600;
  padding: 11px 18px;
  color: #fff;
  background-color: transparent;
  cursor: pointer;
  border: 1px solid #fff;
  outline: none;
  transition: 0.2s;
}

3. Now we will create three more small banners-
<section id="banner3">
        <div class="banner-box">
            <h2>SEASONAL SALE</h2>
            <h3>Winter Collection -50% OFF</h3>
        </div>
        <div class="banner-box banner-box2">
            <h2>NEW FOOTWARE COLLECTION</h2>
            <h3>Spring/Summer 2023</h3>
        </div>
        <div class="banner-box banner-box3">
            <h2>T-Shirts</h2>
            <h3>New Trendy Prints</h3>
        </div>
    </section>

And the css-
#banner3{
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  padding: 0 50px;
}

#banner3 .banner-box{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  background-image: url("img/banner/b7.jpg");
  min-width: 30%;
  height: 30vh;
  background-size: cover;
  background-position: center;
  padding: 20px;
  margin-bottom: 20px;
}

#banner3 .banner-box2{
  background-image: url("img/banner/b4.jpg");
}

#banner3 .banner-box3{
  background-image: url("img/banner/b18.jpg");
}

#banner3 h2{
  color: #fff;
  font-weight: 900;
  font-size: 22px;
}

#banner3 h3{
  color: #ec554e;
  font-weight: 800;
  font-size: 15px;
}

-------------------------------------------------------------------------------End of Banner---------------------------------------------------------------------------------------------

1. Now we will create the newsletter section-
<section id="newsletter" class="section-p1 section-m1">
        <div class="newstext">
            <h4>Sign up for newsletters</h4>
            <p>Get E-mail updates about our latest shop and <span>special offers.</span></p>
        </div>
        <div class="form">
            <input type="text" placeholder="Your email address">
            <button class="normal">Sign up</button>
        </div>
    </section>

2. And the css-
#newsletter{
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  align-items: center;
  background-image: url("img/banner/b14.png");
  background-repeat: no-repeat;
  background-position: 20% 30%;
  background-color: #041e42;
}

#newsletter h4{
  font-size: 22px;
  font-weight: 700;
  color: #fff;
}

#newsletter p{
  font-size: 14px;
  font-weight: 600;
  color: #818ea0;
}

#newsletter p span{
  color: #ffbd27;
}

#newsletter .form{
  display: flex;
  width: 40%;
}

#newsletter input{
  height: 3.125rem;
  padding: 0 1.25em;
  font-size: 14px;
  width: 100%;
  border: 1px solid transparent;
  border-radius: 4px;
  outline: none;
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}

#newsletter button{
  background-color: #088178;
  color: #fff;
  white-space: nowrap;
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}

--------------------------------------------------------------------------------------End of Newletter section------------------------------------------------------------------------------

1. NOw we will add the footer section-
<footer class="section-p1">
        <div class="col">
            <img class="logo" src="img/logo.png" alt="">
            <h4>Contact</h4>
            <p><strong>Address: </strong>562 Wellington Road, Street 32, San Francisco</p>
            <p><strong>Phone: </strong>+01 2222 365 /(+91) 01 2345 6789</p>
            <p><strong>Hours: </strong>10:00 - 18:00, Mon - Sat</p>
            <div class="follow">
                <h4>Follow us</h4>
                <div class="icon">
                    <i class="fab fa-facebook-f"></i>
                    <i class="fab fa-twitter"></i>
                    <i class="fab fa-instagram"></i>
                    <i class="fab fa-pinterest-p"></i>
                    <i class="fab fa-youtube"></i>
                </div>
            </div>
        </div>

        <div class="col">
            <h4>About</h4>
            <a href="#">About Us</a>
            <a href="#">Delivery Information</a>
            <a href="#">Privacy Policy</a>
            <a href="#">Terms & Conditions</a>
            <a href="#">Contact Us</a>
        </div>

        <div class="col">
            <h4>My Account</h4>
            <a href="#">Sign In</a>
            <a href="#">View Cart</a>
            <a href="#">My Wishlist</a>
            <a href="#">Track My Order</a>
            <a href="#">Help</a>
        </div>

        <div class="col install">
            <h4>Install App</h4>
            <p>From App Store or Google Play</p>
            <div class="row">
                <img src="img/pay/app.jpg" alt="">
                <img src="img/pay/play.jpg" alt="">
            </div>
            <p>Secured Payment Gateway</p>
            <img src="img/pay/pay.png" alt="">
        </div>

        <div class="copywright">
            <p>© 2021, Tech2 etc - HTML CSS Ecommerce Template</p>
        </div>
    </footer>

2. And the css-
footer{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

footer .col{
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin-bottom: 20px;
}

footer .logo{
  margin-bottom: 30px;
}

footer h4{
  font-size: 14px;
  padding-bottom: 20px;
}

footer p{
  font-size: 13px;
  margin: 0 0 8px 0;
}

footer a{
  font-size: 13px;
  text-decoration: none;
  color: #222;
  margin-bottom: 10px;
}

footer .follow{
  margin-top: 20px;
}

footer .follow i{
  color: #465b52;
  padding-right: 4px;
  cursor: pointer;
}

footer .install .row img{
  border: 1px solid #088178;
  border-radius: 6px;
}

footer .install img{
  margin: 10px 0 15px 0;
}

footer .follow i:hover,
footer a:hover{
  color: #088178;
}

footer .copywright{
  width: 100%;
  text-align: center;
}
-----------------------------------------------------------------------------End of Footer Section-----------------------------------------------------------------------------------------

1. Now to add media querie we first select the device as ipad and set the min-width-{
@media (max-width: 799px)

2. To show the navbar as sliding we have to do the css like this-
#navbar {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    position: fixed;
    top: 0;
    right: -300px;
    height: 100vh;
    width: 300px;
    background-color: #E3E6F3;
    box-shadow: 0 40px 60px rgba(0, 0, 0, 0.1);
    padding: 80px 0 0 10px;
    transition: 0.3s;
  }

  #navbar.active{
    right: 0px;  -->this will be when the sliding happen
  }

  #navbar li{
    margin-bottom: 25px;
  }

we will add a mobile id in html-
<div id="mobile">
            <a href="cart.html"><i class="far fa-shopping-bag"></i></a>
            <i id="bar" class="fas fa-outdent"></i>
        </div>

  #mobile{
    display: flex;
    align-items: center;
  }

  #mobile i{
    color: #1a1a1a;
    font-size: 24px;
    padding-left: 20px;
  }
 we will add a close id after shopping bag section-
<a href="#" id="close"><i class="far fa-times"></i></a>

  #close{
    display: initial;
    position: absolute;
    top: 30px;
    left: 30px;
    color: #222;
    font-size: 24px;
  }

we will add a class lg-bag in shopping bag-

  #lg-bag{
    display: none;
  }

the rest of the css-
#hero{
    height: 70vh;
    padding: 0 80px;
    background-position: top 30% right 30%;
  }

  #feature{
    justify-content: center;
  }

  #feature .fe-box{
    margin: 15px 15px;
  }

  #product1 .pro-container{
    justify-content: center;
  }

  #product1 .pro{
    margin: 15px;
  }

  #banner{
    height: 20vh;
  }

  #sm-banner .banner-box{
    min-width: 100%;
  }

  #banner3{
    padding: 0 40px;
  }

  #banner3 .banner-box{
    width: 28%;
  }

  #newsletter .form{
    width: 70%;
  }
}

Now we have to add javascript for the navbar open and close in responsive design-
const bar = document.getElementById('bar');
const close = document.getElementById('close');
const nav = document.getElementById('navbar');

if(bar){
    bar.addEventListener('click', () => {
        nav.classList.add('active');
    })
}

if(close){
    close.addEventListener('click', () => {
        nav.classList.remove('active');
    })
}

Now we add css for different device-
@media (max-width: 477px) {
  .section-p1{
    padding: 20px;
  }

  #header{
    padding: 10px 30px;
  }
  h1{
    font-size: 38px;
  }
  h2{
    font-size: 32px;
  }
  #hero{
    padding: 0 20px;
    background-position: 55%;
  }
  #feature{
    justify-content: space-between;
  }
  #feature .fe-box{
    width: 155px;
    margin: 0 0 15px 0;
  }
  #product1 .pro{
    width: 100%;
  }
  #banner{
    height: 40vh;
  }
  #sm-banner .banner-box{
    height: 40vh;
  }
  #sm-banner .banner-box2{
    margin-top: 20px;
  }
  #banner3{
    padding: 0 20px;
  }
  #banner3 .banner-box{
    width: 100%;
  }
  #newsletter{
    padding: 40px 20px;
  }
  #newsletter .form{
    width: 100%;
  }

}
-------------------------------------------------------------------------------End of Home Page---------------------------------------------------------------------------------------------

1. First we wil create an new file name as shop.html and we copy everything from index.html to shop.html.
2. Then we remove the feature, banner, sm-banner, banner3 section.
3. Now we have to highlight the shop section in navbar so we simply put the active class in header section from home to shop like this-
<li><a href="index.html">Home</a></li>
                <li><a class="active" href="shop.html">Shop</a></li>
                <li><a href="blog.html">Blog</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="contact.html">Contact</a></li>
                <li id="lg-bag"><a href="cart.html"><i class="far fa-shopping-bag"></i></a></li>
                <a href="#" id="close"><i class="far fa-times"></i></a>

4. Now we will change the id hero to page-header and give the following text-
<section id="page-header">
        <h2>#Stay Home</h2>
        <p>Save more with coupons & up to 70% off!</p>
    </section>
5. Now we add css-
#page-header{
  background-image: url("img/banner/b1.jpg");
  width: 100%;
  height: 40vh;
  background-size: cover;
  display: flex;
  justify-content: center;
  text-align: center;
  flex-direction: column;
  padding: 14px;
}

#page-header h2,
#page-header p{
  color: #fff;
}
6. Now we open the product1 id section and we remove the first heading and paragraph. This one-
<h2>Featured products</h2>
        <p>Summer Collection New Modern Design</p>
Now we remove the last closing div and last closing section tag and also  remove the next starting section and div tag. this one-
</div>
    </section>
<section id="product1" class="section-p1">
        <h2>New Arrivals</h2>
        <p>Summer Collection New Modern Design</p>
        <div class="pro-container">
This will merge all the products.

7. Now we will add the numbers and arrow to go to different pages-
<section id="pagination" class="section-p1">
        <a href="#">1</a>
        <a href="#">2</a>
        <a href="#"><i class="fal fa-long-arrow-alt-right"></i></a>
    </section>
8. Now we add css for the numbers-
#pagination{
  text-align: center;
}

#pagination a{
  text-decoration: none;
  background-color: #088178;
  padding: 15px 20px;
  border-radius: 4px;
  color: #fff;
  font-weight: 600;
}

#pagination a i{
  font-size: 16px;
  font-weight: 600;
}

9.  Now we will create another file name as sproduct.html and copy everyhting from shop.html to sproduct.html.
10. Then we will only keep header, newsletter and footer.
11. Then-
<section id="prodetails" class="section-p1">
        <div class="single-pro-image">
            <img src="img/products/f1.jpg" width="100%" id="MainImg" alt="">

            <div class="small-img-group">
                <div class="small-img-col">
                    <img src="img/products/f1.jpg" width="100%" class="small-img" alt="">
                </div>
                <div class="small-img-col">
                    <img src="img/products/f2.jpg" width="100%" class="small-img" alt="">
                </div>
                <div class="small-img-col">
                    <img src="img/products/f3.jpg" width="100%" class="small-img" alt="">
                </div>
                <div class="small-img-col">
                    <img src="img/products/f4.jpg" width="100%" class="small-img" alt="">
                </div>
            </div>
        </div>
        <div></div>
    </section>

12. Now the css-
#prodetails .single-pro-image{
  width: 40%;
  margin-right: 50px;
}

.small-img-group{
  display: flex;
  justify-content: space-between;
}

.small-img-col{
  flex-basis: 24%;
  cursor: pointer;
}

13. Now in the second div we will do something like this-
 
<div class="single-pro-details">
            <h6>Home/ T-Shirts</h6>
            <h4>Men's Fashion T shirt</h4>
            <h2>$139.00</h2>
            <select>
                <option>Select Size</option>
                <option>Small</option>
                <option>Medium</option>
                <option>Large</option>
                <option>XL</option>
                <option>XXL</option>
                <option>XXXL</option>
                <input type="number" value="1">
                <button class="normal">Add to Cart</button>
                <h4>Product Details</h4>
                <span>The Gildan Ultra Cotton T-shirt is made from a substantial 6.0 oz. per sq. yd. fabric constructed
                    from
                    100% cotton, this classic fit preshrunk jersey knit provides unmatched comfort with each wear.
                    Featuring
                    a taped neck and shoulder, and a seamless double-needle collar, and available in a range of colors,
                    it
                    offers it all in the ultimate head-turning package.</span>
            </select>
        </div>

Now the css-
#prodetails .single-pro-details{
  width: 50%;
  padding-top: 30px;
}

#prodetails .single-pro-details h4{
  padding: 40px 0 20px 0;
}

#prodetails .single-pro-details h2{
  font-size: 26px;
}

#prodetails .single-pro-details select{
  display: block;
  padding: 5px 10px;
  margin-bottom: 10px;
}

#prodetails .single-pro-details input{
  width: 50px;
  height: 47px;
  padding-left: 10px;
  font-size: 16px;
  margin-right: 10px;
}

#prodetails .single-pro-details input:focus{
  outline: none;
}


#prodetails .single-pro-details button{
  background: #088178;
  color: #fff;
}

#prodetails .single-pro-details span{
  line-height: 25px;
}