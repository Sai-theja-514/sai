# portfolio
<!DOCTYPE html>
<html>
<head>
  <title>Personal Portfolio</title>
  <link rel="stylesheet" type="text/css" href="Style.css">
</head>
<body>
  <a href=https://www.linkedin.com/in/saitheja-gunna-80a535313 target="_blank" class="linkedin-icon">
    <img src="F:\saitheja Portfolio\Logo-Linkedin.jpg.crdownload" alt="LinkedIn">
  </a>
</body>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#Certifications">Certifications</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section id="about">
    <div class="container">
      <div class="flex-container">
        <img src="C:\Users\lenovo\Downloads\6208258120245952305.jpg" alt="Profile Picture" id="profile-picture">
        <div>
          <h1>About Me</h1>
          <p>I am a passionate web developer with expertise in HTML, CSS, and JavaScript. I love creating modern and responsive websites that provide a great user experience.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="projects">
    <div class="container">
      <h1>My Projects</h1>
      <div class="project">
        <h3> Project </h3>
        <p>The Simple Calculator is a web-based application designed to perform basic arithmetic operations efficiently. The project showcases a clean and user-friendly interface, making it a practical tool for everyday calculations.</p>
      </div>
    </div>
  </section>
  <section id="certifications">
    <div class="container">
      <h1>Certifications</h1>
      <div class="certification">
        <h3>AWS Data Engineering Virtual Training</h3>
        <p>Completed through AWS Academy in collaboration with Edu Skills and AICTE. Gained expertise in AWS cloud services, data engineering concepts, and hands-on experience with real-world projects.</p>
      </div>
      <div class="certification">
        <h3>Java Programming on HackerRank</h3>
        <p>Enhanced my Java programming skills by solving complex challenges on HackerRank, including data structures, algorithms, and object-oriented programming.</p>
      </div>
      <div class="certification">
        <h3>Mastering Figma on Guvi</h3>
        <p>Completed a course on mastering Figma through Guvi, acquiring proficiency in creating user interfaces, wireframes, and prototypes for web and mobile applications.</p>
      </div>
    </div>
  </section>

  <section id="contact">
    <div class="container">
      <h1>Contact Me</h1>
      <form id="contactForm">
        <input type="text" id="name" placeholder="Name">
        <input type="email" id="email" placeholder="Email">
        <textarea id="message" placeholder="Message"></textarea>
        <button type="submit">Send Message</button>
      </form>
    </div>
  </section>

  <footer>
    <p>&copy; 2024 Sai Theja</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
* {     
    box-sizing: border-box;   
}      
body {     
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;     
    margin: 0;     
    padding: 0;     
    background-color: #f8f8f8;     
    color: #333;   
}  
#profile-picture {
    display: block;
    margin: 20px auto;
    border: 3px solid #333;
} 
.linkedin-icon {
    position: fixed; 
    top: 20px; 
    right: 50px;
    z-index: 1000; 
}

.linkedin-icon img {
    width: 40px;
    height: 40px;
    transition: opacity 0.3s ease;
}

.linkedin-icon img:hover {
    opacity: 0.7;
}
header {     
    background-color: #333;     
    padding: 20px;   
}
.flex-container {
    display: flex;
    align-items: center;
}

#profile-picture {
    width: 150px; 
    height: auto;
    margin-right: 20px; 
    border-radius: 50%; 
    border: 3px solid #333;
}

.flex-container div {
    flex: 1; 
}     
nav ul {     
    list-style-type: none;     
    margin: 0;     
    padding: 0;   
}      
nav ul li {     
    display: inline;     
    margin-right: 20px;   
}      
nav ul li a {     
    text-decoration: none;     
    color: #fff;     
    font-weight: bold;     
    transition: color 0.3s ease;   
}      
nav ul li a:hover {     
    color: #ddd;   
}      
.container {     
    max-width: 800px;     
    margin: 0 auto;     
    padding: 40px;     
    background-color: #fff;     
    border-radius: 5px;     
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);   
}      
h1 {     
    font-size: 36px;     
    margin-bottom: 20px;     
    color: #333;   
}      
p {     
    font-size: 18px;     
    line-height: 1.5;     
    margin-bottom: 20px;     
    color: #555;   
}      
.project {     
    margin-bottom: 20px;  
}      
.project h3 {     
    font-size: 24px;     
    margin-bottom: 10px;     
    color: #333;   
}      
form input,   
form textarea {     
    width: 100%;     
    padding: 10px;     
    margin-bottom: 20px;     
    border: 1px solid #ccc;     
    border-radius: 5px;   
}      
form button {     
    padding: 10px 20px;     
    background-color: #333;     
    color: #fff;     
    border: none;     
    border-radius: 5px;     
    cursor: pointer;     
    transition: background-color 0.3s ease; 
}      
form button:hover {     
    background-color: #555;   
}      
footer {     
    background-color: #070606;     
    color: #fff;     
    padding: 10px;     
    text-align: center;   
} 
// Handle image upload and display
document.getElementById('imageUpload').addEventListener('change', function(event) {
    const reader = new FileReader();
    reader.onload = function(){
        const img = document.getElementById('profile-picture');
        img.src = reader.result;
        img.style.display = 'block';
    }
    reader.readAsDataURL(event.target.files[0]);
});

// Handle form submission
document.getElementById('contactForm').addEventListener('submit', function(event) {
    event.preventDefault(); // Prevent form from submitting the traditional way

    const name = document.getElementById('name').value;
    const email = document.getElementById('email').value;
    const message = document.getElementById('message').value;

    if (name && email && message) {
        alert('Thank you, ' + name + '! Your message has been sent.');
        // Here you can add code to actually send the form data to your email or server
        document.getElementById('contactForm').reset(); // Reset the form after submission
    } else {
        alert('Please fill in all fields.');
    }
});
