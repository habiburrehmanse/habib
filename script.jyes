document.addEventListener("DOMContentLoaded", function () {
  const links = document.querySelectorAll(".nav-link");

  links.forEach(link => {
    link.addEventListener("click", function (e) {
      e.preventDefault();
      const targetId = this.getAttribute("href");
      document.querySelector(targetId).scrollIntoView({
        behavior: "smooth",
        block: "start"
      });
    });
  });
});
window.addEventListener("scroll", function () {
  let scrollPos = window.scrollY + 100; // Adjust offset for better detection
  let links = document.querySelectorAll(".nav-link");

  links.forEach(link => {
    let section = document.querySelector(link.getAttribute("href"));
    if (section.offsetTop <= scrollPos && section.offsetTop + section.offsetHeight > scrollPos) {
      links.forEach(l => l.classList.remove("active"));
      link.classList.add("active");
    }
  });
});
window.addEventListener("scroll", function () {
  const navbar = document.querySelector(".navbar");
  if (window.scrollY > 50) {
    navbar.classList.add("scrolled");
  } else {
    navbar.classList.remove("scrolled");
  }
});

document.addEventListener("DOMContentLoaded", function () {
  let navbarHeight = document.querySelector(".navbar").offsetHeight;
  document.querySelectorAll(".nav-link").forEach(link => {
    link.addEventListener("click", function (event) {
      event.preventDefault();
      let targetId = this.getAttribute("href").substring(1);
      let targetElement = document.getElementById(targetId);
      if (targetElement) {
        window.scrollTo({
          top: targetElement.offsetTop - navbarHeight,
          behavior: "smooth"
        });
      }
    });
  });
});
