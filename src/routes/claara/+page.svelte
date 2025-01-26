<script>

</script>
        <style>
*{
   margin: 0;
   padding: 0;
   box-sizing: border-box;
   font-family: sans-serif;
}

section{
   width: 100%;
   height: 100vh;
   background-image: url();
   background-size: cover;
   background-position: center;
}

section nav{
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-around;
    box-shadow: 0 0 10px rgb(38, 52, 119);
    background: #fff;
    left: 0;
    z-index: 100;
}

section nav .logo img{
    width: 100px;
    cursor: pointer;
    margin: 8px 0;
}

section nav ul{
    list-style: none;
}

section nav li{
    display: inline-block;
    padding:0 10px;
}

section nav li a{
    text-decoration: none;
    color: #000;
}

section nav li a:hover{
    color: rgb(32, 59, 196);
}

section nav .social_icon i{
    margin: 0 5px;
    font-size:18px;
}

section nav .social_icon i:hover{
    color: rgb(38, 52, 119);
    cursor: pointer;
} 

section .main{
    display: flex;
    align-items: center;
    justify-content: space-around;
    position: relative;
    top: 10%;
}

section .main h1{
    position: relative;
    font-size: 70px;
    top: 20px;
    left:25px;
}

section .main h1 span{
    color: rgb(38, 52, 119);    
}

section .main p{
    width: 650px;
    text-align: justify;
    line-height: 22px;
    position: relative;
    top: 20px;
    left: 25px;
}




.featured_boks{
    width: 100%;
    height: 100vh;
    padding: 70px 0;
}

.featured_boks h1{
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 30px;
    font-size: 60px;
}

.featured_boks .featured_books_box{
    width: 95%;
    height: 60vh;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
    overflow: hidden;
    overflow-x: scroll;
}

.featured_boks .featured_books_box .features-books_card{
    width: 250px;
    height: 500px;
    text-align: center;
    padding: 7px;
    border: 1px solid #919191;
    margin: auto 20px;
}

.featured_boks .featured_books_box .features-books_card:hover{
    box-shadow: 0 0 20px rgb(38, 52, 119);
}

.featured_boks .featured_books_box .features-books_card .featured_books_img img{
    width: 150px;
}

.featured_boks .featured_books_box .features-books_card .featured_books_tag h2{
    margin: 12px;
    
}

.featured_boks .featured_books_box .features-books_card .featured_books_tag .writer{
    color:#919191;
}

.featured_boks .featured_books_box .features-books_card .featured_books_tag .categories{
    color: rgb(38, 52, 119);
    margin-top: 8px;
}

.featured_boks .featured_books_box .features-books_card .featured_books_tag .book_price{
    margin-top: 8px;
    font-weight: bold;
    margin-bottom: 15px;
}

.featured_boks .featured_books_box .features-books_card .featured_books_tag .book_price sub{
    font-weight: 100;
    padding: 0 5px;
}

.featured_boks .featured_books_box .features-books_card .featured_books_tag .f_btn{
    padding: 8px 20px;
    border: 2px solid rgb(38, 52, 119);
    text-decoration: none;
    color:#000;
    border-radius: 10px;
}

::-webkit-scrollbar{
    width: 10px;
    height: 5px;
}

::-webkit-scrollbar-track{
   box-shadow: inset 0 0 8px rgba(0, 0, 0,0.2);
}

::-webkit-scrollbar-thumb{
    background: rgb(38, 52, 119);
    border-radius: 5px;
}


.arrivals{
    width: 100%;
    height: 100vh;
    margin-bottom: 35px;
}

.arrivals h1{
    font-size: 60px;
    text-align: center;
    margin-bottom: 35px;
}

.arrivals .arrivals_box{
    width: 96%;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
    grid-gap: 25px 0;
}

.arrivals .arrivals_box .arrivals-card{
    width: 250px;
    height: 350px;
    text-align: center;
    padding: 5px;
    border: 1px solid #919191;
    margin: auto 20px;
}

.arrivals .arrivals_box .arrivals-card:hover{
    box-shadow: 0 0 5px rgb(38, 52, 119);
}

.arrivals .arrivals_box .arrivals-card .arrivals_image{
    width: 150px;
    height: 220px;
    margin: 0 auto;
    cursor: pointer;
    box-shadow: 0 0 8px rgba(0, 0, 0,0.5);
    overflow: hidden;
}

.arrivals .arrivals_box .arrivals-card .arrivals_image img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
    transition: 0.3s;
}

.arrivals .arrivals_box .arrivals-card:hover .arrivals_image img{
    transform: scale(1.1);
}

.arrivals .arrivals_box .arrivals-card .arrivals_tag p{
    font-family: queen of camelot;
    font-size: 20px;
    margin: 8px 0;
}

.arrivals .arrivals_box .arrivals-card .arrivals_tag .arrivals_icon{
    color: rgb(38, 52, 119);
    margin-bottom: 18px;
}

.arrivals .arrivals_box .arrivals-card .arrivals_tag .arrivals_btn{
    padding: 8px 20px;
    border: 2px solid rgb(38, 52, 119);
    text-decoration: none;
    color: #000;
    border-radius: 10px;
}

.about{
    width: 100%;
    height: auto;
    padding: 20px;
    display: flex;
    align-items: center;
    justify-content: space-around;
    background-color: rgb(38, 52, 119);
}

.about .about_image img{
    width: 600px;
}

.about .about_tag h1{
    font-size: 50px;
    position: relative;
    bottom: 35px;
    color: #fff;
}

.about .about_tag p{
    line-height: 22px;
    width: 650px;
    text-align: justify;
    margin-bottom: 15px;
    color: #fff;
}

.about .about_tag .about_btn{
    padding: 10px 20px;
    background:  #fff;
    color: #000;
    text-decoration: none;
    position: relative;
    top: 50px;
    border-radius: 10px;
}



.location{
    width: 100%;
    height: auto;
    padding: 20px;
    display: flex;
    align-items: center;
    justify-content: space-around;
}

.location .location_image img{
    width: 600px;
}

.location .location_tag h1{
    font-size: 50px;
    position: relative;
    bottom: 35px;
}

.location .location_tag p{
    line-height: 22px;
    width: 650px;
    text-align: justify;
    margin-bottom: 15px;
}

.location .location_tag .location_btn{
    padding: 10px 20px;
    background: rgb(38, 52, 119) ;
    color: #fff;
    text-decoration: none;
    position: relative;
    top: 50px;
    border-radius: 10px;
}


footer{
    width: 100%;
    background: rgb(38, 52, 119);
}

footer .footer_main{
    width: 100%;
    display: flex;
    justify-content: space-around;
}

footer .footer_main .tag{
    margin: 10px 0;
}

footer .footer_main .tag img{
    width: 100px;
    margin-bottom: 10px;
}

footer .footer_main .tag p{
    width: 250px;
    line-height: px;
    text-align: justify;
    color: #fff;
}

footer .footer_main .tag h1{
    font-size: 25px;
    margin: 25px 0;
    color: #fff;
}

footer .footer_main .tag a{
    display: block;
    color: white;
    text-decoration: none;
    margin: 10px 0;
}

footer .footer_main .tag i{
    margin-right: 10px;
}

footer .footer_main .tag .social_link i{
    margin: 0 5px;
}

        </style>

        <section>

            <nav>
               
                <div class="logo">
                <img src="">
                </div>

                <ul>
                  <li><a href=""> Inicio </a></li>
                  <li><a href=""> Destaques </a></li>
                  <li><a href=""> Lançamentos </a></li>
                  <li><a href="#ABOUT"> Sobre a marca </a></li>
                </ul>

                <div class= social_icon>
                    <i class="fa-solid fa-magnifying-glass"></i>
                    <i class="fa-solid fa-cart-shopping"></i>
                </div>
                
            </nav>
            <div class="main">
                  
              <div class="main-tag">
                <h1><b>Seja Bem Vindo à<br><span>Leia Mais</span></b></h1>
                <p>
                  A melhor livraria do país. Aqui você encontra diversos títulos que<br>irão te surpreender, 
                  com preços ótimos e de qualidade altissíma!
                </p>
            </div>
            <div class="main image">
                <img src="">
            </div>
           </div>
            </section>

            <div class="featured_boks">

               <p id="FEATURED"><h1><b>Livros em Destaque</b></h1>

               <div class="featured_books_box">
                  
                <div class="features-books_card">

                  <div class="featured_books_img">
                    <img src="">
                  </div>

                  <div class="featured_books_tag">
                    <h2>Livros Destaque</h2>
                    <p class="writer">Victoria Aveyard</p>
                    <div class="categories">Romance, Ficção Juvenil</div>
                    <p class="book_price">R$30,99<sub><del>R$34,99</del></sub></p>
                    <a href="" class="f_btn">Saiba Mais</a>
                  </div>
                
                </div>
                <div class="features-books_card">

                  <div class="featured_books_img">
                    <img src="">
                  </div>

                  <div class="featured_books_tag">
                    <h2>Livros Destaque</h2>
                    <p class="writer">J.K Rowlling</p>
                    <div class="categories">Aventura, Fantasia</div>
                    <p class="book_price">R$60,99<sub><del>R$69,90</del></sub></p>
                    <a href="" class="f_btn">Saiba Mais</a>
                  </div>
                
                </div>
                <div class="features-books_card">

                  <div class="featured_books_img">
                    <img src="">
                  </div>

                  <div class="featured_books_tag">
                    <h2>Livros Destaque</h2>
                    <p class="writer">Antoine de Saint-Exupéry</p>
                    <div class="categories">Literatura infantil, Fábula</div>
                    <p class="book_price">R$13,50<sub><del>R$15,60</del></sub></p>
                    <a href="" class="f_btn">Saiba Mais</a>
                  </div>
                
                </div>
                <div class="features-books_card">

                  <div class="featured_books_img">
                    <img src="">
                  </div>

                  <div class="featured_books_tag">
                    <h2>Livros Destaque</h2>
                    <p class="writer">Jenna Evans Welch</p>
                    <div class="categories">Ficção</div>
                    <p class="book_price">R$42,67<sub><del>R$46,67</del></sub></p>
                    <a href="" class="f_btn">Saiba Mais</a>
                  </div>
                
                </div>
                <div class="features-books_card">

                  <div class="featured_books_img">
                    <img src="">
                  </div>

                  <div class="featured_books_tag">
                    <h2>Livros Destaque</h2>
                    <p class="writer">Jojo Moyes</p>
                    <div class="categories">Romance de amor, Ficção</div>
                    <p class="book_price">R$43,50<sub><del>R$47,92</del></sub></p>
                    <a href="" class="f_btn">Saiba Mais</a>
                  </div>
                
                </div>
                <div class="features-books_card">

                  <div class="featured_books_img">
                    <img src="">
                  </div>

                  <div class="featured_books_tag">
                    <h2>Livros Destaque</h2>
                    <p class="writer">Rachael Lippincott</p>
                    <div class="categories">Romance, Ficção</div>
                    <p class="book_price">R$29,60<sub><del>R$32,37</del></sub></p>
                    <a href="" class="f_btn">Saiba Mais</a>
                  </div>
                
                </div>
                <div class="features-books_card">

                  <div class="featured_books_img">
                    <img src="">
                  </div>

                  <div class="featured_books_tag">
                    <h2>Livros Destaque</h2>
                    <p class="writer">Colleen Hoover</p>
                    <div class="categories">Romance de amor, Ficção</div>
                    <p class="book_price">R$26,60<sub><del>R$28,79</del></sub></p>
                    <a href="" class="f_btn">Saiba Mais</a>
                  </div>
                
                </div>
                <div class="features-books_card">

                  <div class="featured_books_img">
                    <img src="">
                  </div>

                  <div class="featured_books_tag">
                    <h2>Livros Destaque</h2>
                    <p class="writer">Colleen Hoover</p>
                    <div class="categories">Romance de amor, Ficção</div>
                    <p class="book_price">R$41,99<sub><del>R$46,33</del></sub></p>
                    <a href="" class="f_btn">Saiba Mais</a>
                  </div>
                
                </div>
                <div class="features-books_card">

                  <div class="featured_books_img">
                    <img src="">
                  </div>

                  <div class="featured_books_tag">
                    <h2>Livros Destaque</h2>
                    <p class="writer">Shea Ernshaw</p>
                    <div class="categories"> Ficção, Fantasia sombria</div>
                    <p class="book_price">R$30,99<sub><del>R$34,99</del></sub></p>
                    <a href="" class="f_btn">Saiba Mais</a>
                  </div>
                
                </div>
                <div class="features-books_card">

                  <div class="featured_books_img">
                    <img src="">
                  </div>

                  <div class="featured_books_tag">
                    <h2>Livros Destaque</h2>
                    <p class="writer">J.K Rowlling</p>
                    <div class="categories">Aventura, Fantasia</div>
                    <p class="book_price">R$62,67<sub><del>R$60,00</del></sub></p>
                    <a href="" class="f_btn">Saiba Mais</a>
                  </div>
                
                </div>

              </div>
            
            </div>

            
            <div class="arrivals">
              <p id="RELEASES"><h1><b>Novos Lançamentos</b></h1>

                <div class="arrivals_box">

                  <div class="arrivals-card">
                    <div class="arrivals_image">
                      <img src="">
                    </div>
                    <div class="arrivals_tag">
                      <p>Novos Lançamentos</p>
                      <div class="arrivals_icon">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-regular fa-star-half-stroke"></i>
                      </div>
                      <a href="" class="arrivals_btn">Saiba Mais</a>
                    </div>
                  </div>

                  <div class="arrivals-card">
                    <div class="arrivals_image">
                      <img src="">
                    </div>
                    <div class="arrivals_tag">
                      <p>Novos Lançamentos</p>
                      <div class="arrivals_icon">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-regular fa-star"></i>
                      </div>
                      <a href="" class="arrivals_btn">Saiba Mais</a>
                    </div>
                  </div>

                  <div class="arrivals-card">
                    <div class="arrivals_image">
                      <img src="">
                    </div>
                    <div class="arrivals_tag">
                      <p>Novos Lançamentos</p>
                      <div class="arrivals_icon">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                      </div>
                      <a href="" class="arrivals_btn">Saiba Mais</a>
                    </div>
                  </div>

                  <div class="arrivals-card">
                    <div class="arrivals_image">
                      <img src="">
                    </div>
                    <div class="arrivals_tag">
                      <p>Novos Lançamentos</p>
                      <div class="arrivals_icon">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                      </div>
                      <a href="" class="arrivals_btn">Saiba Mais</a>
                    </div>
                  </div>

                  <div class="arrivals-card">
                    <div class="arrivals_image">
                      <img src="">
                    </div>
                    <div class="arrivals_tag">
                      <p>Novos Lançamentos</p>
                      <div class="arrivals_icon">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-regular fa-star-half-stroke"></i>
                      </div>
                      <a href="" class="arrivals_btn">Saiba Mais</a>
                    </div>
                  </div>

                  <div class="arrivals-card">
                    <div class="arrivals_image">
                      <img src="">
                    </div>
                    <div class="arrivals_tag">
                      <p>Novos Lançamentos</p>
                      <div class="arrivals_icon">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-regular fa-star-half-stroke"></i>
                      </div>
                      <a href="" class="arrivals_btn">Saiba Mais</a>
                    </div>
                  </div>

                  <div class="arrivals-card">
                    <div class="arrivals_image">
                      <img src="">
                    </div>
                    <div class="arrivals_tag">
                      <p>Novos Lançamentos</p>
                      <div class="arrivals_icon">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-regular fa-star-half-stroke"></i>
                      </div>
                      <a href="" class="arrivals_btn">Saiba Mais</a>
                    </div>
                  </div>

                  <div class="arrivals-card">
                    <div class="arrivals_image">
                      <img src="">
                    </div>
                    <div class="arrivals_tag">
                      <p>Novos Lançamentos</p>
                      <div class="arrivals_icon">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-regular fa-star-half-stroke"></i>
                      </div>
                      <a href="" class="arrivals_btn">Saiba Mais</a>
                    </div>
                  </div>

                  <div class="arrivals-card">
                    <div class="arrivals_image">
                      <img src="">
                    </div>
                    <div class="arrivals_tag">
                      <p>Novos Lançamentos</p>
                      <div class="arrivals_icon">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                      </div>
                      <a href="" class="arrivals_btn">Saiba Mais</a>
                    </div>
                  </div>

                  <div class="arrivals-card">
                    <div class="arrivals_image">
                      <img src="">
                    </div>
                    <div class="arrivals_tag">
                      <p>Novos Lançamentos</p>
                      <div class="arrivals_icon">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                      </div>
                      <a href="" class="arrivals_btn">Saiba Mais</a>
                    </div>
                  </div>


                </div>
                <br><br><br>

            </div>
            <p id="ABOUT"></p>
            <div class="about">
              
              <div class="about_image">
                <img src="">
              </div>
              <div class="about_tag">
                <h1><b>Sobre a marca</b></h1>
                <p>
                  Tudo começou em 1989, quando Leila presenteou sua filha com uma pequena livraria no interior de São Paulo. 
                  A primeira loja era pequena, mas o sonho de levar felicidade em forma de livros era gigante. 
                  Em 2010 a Leia Mais aderiu ao franchising e hoje, com mais de 600 lojas espalhadas pelo Brasil,
                  continua com a proposta de levar sorrisos a cada história.
                </p>
                <a href="" class="about_btn">Saiba Mais</a>
              </div>
            </div>
    
           <br><br><br><br><br><br>
            
           
           <div class="location">

              <div class="location_image">
                <img src="">
              </div>
              <div class="location_tag">
                <h1><b>Nos encontre pertinho de você!</b></h1>
                <p>
                  A Leia Mais possui mais de 100 lojas nas regiões centro-oeste, sul, sudeste e nordeste do Brasil.
                  Explore o nosso mapa e descubra qual a Leia Mais mais próxima de você!
                </p>
                <a href="" class="location_btn">Encontre uma Loja</a>
              </div>
            </div>
            

            <br><br><br><br><br><br><br><br>
            <footer>
              <div class="footer_main">

                <div class="tag">
                  <h1><b>Leia Mais</b></h1>
                  <p>
                    O sonho de levar sorrisos <br>a cada história!
                  </p>
                </div>

                <div class="tag">
                  <h1><b>Links</b></h1>
                  <a href="">Inicio</a>
                  <a href="">Destaques</a>
                  <a href="">Lançamentos</a>
                  <a href="">Sobre a marca</a>
                </div>

                <div class="tag">
                  <h1><b>Contatos</b></h1>
                  <a href=""><i class="fa-solid fa-phone">  +55 (18) 4002-8922</i></a>
                  <a href=""><i class="fa-solid fa-phone">  +55 (18) 5478-3214</i></a>
                  <a href=""><i class="fa-solid fa-envelope">  Leiamais@gmail.com</i></a>
                </div>

                <div class="tag">
                  <h1><b>Redes Sociais</b></h1>
                  <div class="social-link">
                    <a href=""><i class="fa-brands fa-facebook-f">  @leiamais</i></a>
                      <a href=""><i class="fa-brands fa-instagram">  @leiamais</i></a>
                        <a href=""><i class="fa-brands fa-x-twitter">  @leiamais</i></a>
                          <a href="w"><i class="fa-brands fa-linkedin-in">  @leiamais</i></a>
                </div>
                </div>
              </div>

            </footer>