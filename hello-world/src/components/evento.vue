<template>

    <!-- single Event -->
          <div class="event">
            <div class="card event-card">
              <a href={{general_url}} target="_blank" rel="noopener noreferrer">
              <img :src="imgPost()" class="card-img-top car-img" alt="">
              </a>
              <!-- card body -->
              <div class="description">
                <div class="event-info d-flex justify-content-between">
                  <!-- first flex child -->
                  <div class="event-text text-uppercase" id="evento">
                    <h6 class="font-weight-bold">{{title}}</h6>
                    <h6>{{title2}}</h6> 
                  </div>
                  <!-- second flex child -->
                  <a href={{tickets_url}} target="_blank" rel="noopener noreferrer">

                  <h5 class="event-value align-self-center py-2 px-3">
                    <span class="event-price">{{prize}}</span>
                  </h5>
                  
                </a>
                </div>
              </div>
              <!-- end of card -->
              <div class="location" >
                <p><span></span>{{date}}</p>
                <a href={{location_url}} target="_blank" rel="noopener noreferrer"><span></span>{{location_name}}<img src="../assets/maps.png"></a>
              </div>
            </div>
          </div>
          <!--end of single Event -->
</template>


<script >

export default {
    props: {
        title: String, 
        title2: String, 
        photo: Image, 
        general_url: URL, 
        tickets_url: URL, 
        prize: String, 
        date: String, 
        location_name: String, 
        location_url: URL
        },
        methods:{
            imgPost(){
                console.log ("PASAAAAA");
                return "../assets/Puro_Latino.jpeg";
            }
        }
}
</script>


<style >
@import url('https://fonts.googleapis.com/css?family=Roboto:400,700');

:root{
  --mainOrange:rgba(241, 99, 64, 0.7);
  --transparentOrange:rgba(241, 99, 64, 0.7);
  --mainWhite:#FFFFFF;
  --mainGrey:#9c9c9c;
  --mainBlack:#000000;
  --mainGrey:rgb(216, 214, 214);
  --mainYellow:#e3b505;
}

.description{
    width: 348px;
    height: 94.4px;
    background: var(--mainWhite);
}

.location{
    width: 348px;
    height: 89px;
}

    /* Events */
.event{
  background: var(--mainGrey);
}
.event-card{
  border-radius: 0!important;
}
.event-img{
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}
.event-value{
  background: var(--mainOrange);
  color: var(--mainWhite);
  clip-path: polygon(15% 0,85% 0,100% 100%,0 100%);
  transition: all 1s linear;
}
.event-value:hover{
  clip-path: polygon(0% 0,100% 0,100% 100%,0 100%);
}  

</style>