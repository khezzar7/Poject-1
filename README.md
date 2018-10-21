# Poject-1

//Ciblage du DOM
const imgSmall = document.getElementById('imgSmall').children;
const imgBig = document.getElementById('imgBig').children;

function addEvents(){
for(let i = 0; i < imgSmall.length; i ++){
  imgSmall[i].addEventListener('mouseover', e=>{
    displayImgBig(e.target.src);
  })
  imgSmall[i].addEventListener('mouseout', e=>{
    reset();
  })
}
}


function displayImgBig(imageSrc){
  for (let i = 0; i < imgBig.length; i++) {
    if(imageSrc == imgBig[i].src){
      imgBig[i].style.display='inline';
    }else {
      imgBig[i].style.display='none';
    }
  }
}
function reset(){
  for(let i = 0; i< imgBig.length; i++){
    imgBig[i].style.display='none';
  }
}
function init(){
addEvents();
}
//Initialisation
init();
