function palavra() {
    const p = document.querySelector('p#resposta')
    let aldo = document.querySelector('#aldo').value
    let jucimara = document.querySelector('#jucimara').value

    if (aldo.length > jucimara.length) {
        p.innerHTML = 'A'
    } else if (aldo.length < jucimara.length) {
        p.innerHTML = 'B'
    } else {
        p.innerHTML = '*'
    }
}
// Alternar claro/escuro
const checkbox = document.getElementById('checkbox');
 
function introAboutLogoTransition() {
  $("#about-quad").css("top", "70%");
  $("#about-quad").css("opacity", "1");
}

function checkDarkMode(){
  if (localStorage.getItem("tourism_website_darkmode") !== null && localStorage.getItem("tourism_website_darkmode") === "true") {
    document.body.classList.add('dark');
    checkbox.checked = true;
  }
};
checkDarkMode();

checkbox.addEventListener('change', () => {
  document.body.classList.toggle('dark');
  document.body.classList.contains('dark') ?
    localStorage.setItem("tourism_website_darkmode", true) :
    localStorage.setItem("tourism_website_darkmode", false);
});

// botão de rolagem
 
let mybutton = document.getElementById("upbtn");
 
window.onscroll = function() {scrollFunction()};

function scrollFunction() {
  if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
    mybutton.style.display = "block";
  } else {
    mybutton.style.display = "none";
  }
}
function topFunction() {
  document.body.scrollTop = 0;
  document.documentElement.scrollTop = 0
}

