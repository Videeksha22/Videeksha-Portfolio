/*==========================toggle icon navbar=========================*/
let menuIcon = document.querySelector('#menu-icon');
let navbar = document.querySelector('.navbar');

menuIcon.onclick = () => {
  navbar.classList.toggle('active');
  menuIcon.classList.toggle('fa-bars');
  menuIcon.classList.toggle('fa-xmark'); // changes bars to X
};

/*==========================scroll section active link=========================*/
let sections = document.querySelectorAll('section');
let navLinks = document.querySelectorAll('header nav a');

window.onscroll = () => {
  let top = window.scrollY;

  sections.forEach(sec => {
    let offset = sec.offsetTop - 150;
    let height = sec.offsetHeight;
    let id = sec.getAttribute('id');

    if (top >= offset && top < offset + height) {
      navLinks.forEach(links => {
        links.classList.remove('active');
        document.querySelector('header nav a[href*=' + id + ']').classList.add('active');
      });
    }
  });

  /*==========================sticky navbar=========================*/
  let header = document.querySelector('header');
  header.classList.toggle('sticky', window.scrollY > 100);

  /*==========================remove toggle icon and navbar=========================*/
  menuIcon.classList.remove('fa-xmark');
  menuIcon.classList.add('fa-bars');   // ✅ make sure hamburger returns
  navbar.classList.remove('active');
};

/*==========================scroll reveal=========================*/
ScrollReveal({
  distance: '80px',
  duration: 2000,
  delay: 200,
});
ScrollReveal().reveal('.home-content, .heading', { origin: 'top' });
ScrollReveal().reveal('.home-img, .techstack-container, .projects-box, .contact form', { origin: 'bottom' });
ScrollReveal().reveal('.home-content h1, .about-img', { origin: 'left' });
ScrollReveal().reveal('.home-content p, .about-content', { origin: 'right' });

/*==========================typed js=========================*/
const typed = new Typed('.multiple-text', {
  strings: ['CSE Student', 'Full-Stack Developer', 'Aspiring Software Engineer', 'Problem Solver'],
  typeSpeed: 40,
  backSpeed: 20,
  backDelay: 900,
  loop: true,
});

/*==========================email js=========================*/
// Contact form handling with EmailJS
document.getElementById("contact-form").addEventListener("submit", function(event) {
  event.preventDefault(); // prevent default form submission

  emailjs.send("service_fltpxse", "template_difbnym", {
    from_name: document.getElementById("name").value,
    from_email: document.getElementById("email").value,
    message: document.getElementById("message").value,
  })
  .then(function() {
  let msg = document.getElementById("form-message");
  msg.innerText = "✅ Message sent successfully!";
  msg.style.color = "var(--main-color)";

  document.getElementById("contact-form").reset();

  // Optional: auto-hide after 3s
  setTimeout(() => {
    msg.innerText = "";
  }, 3000);
})
.catch(function() {
  let msg = document.getElementById("form-message");
  msg.innerText = "❌ Failed to send message.";
  msg.style.color = "var(--error-color)";
});
});
