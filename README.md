<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Resume</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            padding: 20px;
            line-height: 1.6;
            background-color: rgb(246, 247, 247);
        }
        .container {
            max-width: 800px;
            margin: auto;
            padding: 20px;
            background: rgb(252, 252, 252);
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1, h2, h3 {
            text-align: center;
        }
        #skills ul, #education ul, #achievements ul, #links ul {
            list-style: none;
            padding: 0;
        }
        #skills li, #education li, #achievements li, #links li {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
            transition: transform 0.3s;
        }
        #skills li i, #links li a {
            margin-right: 10px;
            color: #0b0b0b;
        }
        #skills li:hover, #links li:hover {
            transform: scale(1.05);
        }
        #projects {
            margin-top: 20px;
        }
        .card {
            background: #444444;
            color: rgb(255, 251, 251);
            padding: 20px;
            margin-bottom: 10px;
            border-radius: 5px;
            cursor: pointer;
            transition: transform 0.3s, background-color 0.3s;
        }
        .card:hover {
            background-color: #444444;
            transform: scale(1.05);
        }
        .description {
            display: none;
            margin-top: 10px;
            font-size: 0.9em;
            opacity: 0;
            transition: opacity 0.5s ease;
        }
        .description.show {
            display: block;
            opacity: 1;
        }
        nav {
            line-height: 5px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            border: 1px solid rgb(8, 8, 8);
            padding: 8px;
            text-align: left;
        }
        th {
            background-color: rgb(250, 250, 250);
        }
        #links {
            font-size: 18px;
        }
        #links ul {
            list-style-type: none;
            padding: 0;
        }
        #links ul li {
            margin-bottom: 10px;
        }
        #links ul li a {
            text-decoration: none;
            color: #171616;
            margin-right: 10px;
        }
        #links ul li a i {
            font-size: 24px;
        }
        #achievements {
            margin-top: 20px;
        }
        #achievements ul {
            list-style-type: none;
            padding-left: 0;
        }
        #achievements li {
            position: relative;
            padding-left: 20px;
            margin-bottom: 10px;
            line-height: 1.5;
        }
        /* Animated bullet points */
        #achievements li::before {
            content: '\2022';
            color: #0a0a0a;
            font-size: 24px;
            position: absolute;
            left: -20px;
            animation: bullet-animation 1s ease-out infinite alternate;
        }
        @keyframes bullet-animation {
            0% {
                transform: translateY(0);
            }
            100% {
                transform: translateY(-3px);
            }
        }
    </style>
    <script>
        function toggleDescription(element) {
            const description = element.querySelector('.description');
            description.classList.toggle('show');
        }
    </script>
</head>
<body>
    <div class="container">
        <nav class="navigation">
            <h1 style="font-size: xx-large;">Surabhi M.P</h1>
            <h2 style="font-size: medium;">Electronics and Communication Engineer</h2>
        </nav>

        <section id="summary">
            <h3>Summary</h3>
            <p>Electronics and Communication Engineer with a strong background in VLSI, Digital Electronics, and data structures and algorithms. Experienced in projects like FireFighting Robot, Spam Mail Detector, and Solar-powered Water Body Cleaner Bot. Proven track record in C++, HTML, CSS, and Arduino. Skilled in Cadence, Matlab, and Eagle software.</p>
        </section>

        <section id="education">
            <h2>Education</h2>
            <table>
                <tr>
                    <th>Institution</th>
                    <th>Degree/Standard</th>
                    <th>Grade</th>
                    <th>Duration</th>
                </tr>
                <tr>
                    <td>Sri Jayachamarajendra College of Engineering</td>
                    <td>Bachelor of Engineering in Electronics and Communication</td>
                    <td>8.74 CGPA</td>
                    <td>Dec 2020 – Jun 2024</td>
                </tr>
                <tr>
                    <td>Vidya Bharati PU College, Shimogga</td>
                    <td>12th Standard</td>
                    <td>93.83%</td>
                    <td>April 2019 – March 2020</td>
                </tr>
                <tr>
                    <td>SVHS, Shimogga</td>
                    <td>10th Standard</td>
                    <td>92.64%</td>
                    <td>April 2017 – March 2018</td>
                </tr>
            </table>
        </section>

        <section id="achievements">
            <h3>Achievements</h3>
            <ul>
                <li>Attended the IEEE IoT Workshop (April 2022)</li>
                <li>Completed the NASSCOM Internship in Digital Engineering with a Gold Certificate (Sept 2023)</li>
                <li>Selected for top 15 in college level project competition</li>
                <li>District level discus and shotput throw player (school level)</li>
                <li>Shabdh Cultural Club Volunteer (June 2023)</li>
                <li>E-Certificate and Technical Paper Published (solar powered GPS-guided water body cleaning Bot) in JXU Volume 18, Issue 6, 2024</li>
            </ul>
        </section>

        <section id="skills">
            <h3>Skills</h3>
            <ul>
                <li><i class="fas fa-code"></i> Programming: C++</li>
                <li><i class="fas fa-microchip"></i> Hardware: Soldering, Etching, PCB Design</li>
                <li><i class="fas fa-tools"></i> Design Tools: Proteus, Eagle</li>
                <li><i class="fas fa-laptop-code"></i> Development Tools: Arduino IDE, Cadence Virtuoso</li>
                <li><i class="fas fa-globe"></i> Web Development: HTML, CSS, JavaScript, SQL</li>
                <li><i class="fas fa-microchip"></i> Areas of Interest: VLSI, Digital Electronics, Control Systems, OOP, Data Structures</li>
            </ul>
        </section>

        <section id="projects">
            <h3>Projects</h3>
            <div class="card" onclick="toggleDescription(this)">
                <h4>Fire Fighting Robot</h4>
                <p class="description">A firefighting robot using Arduino Uno, motor driver, DC motor, gas sensor, and temperature sensor to autonomously navigate and extinguish fires.</p>
            </div>
            <div class="card" onclick="toggleDescription(this)">
                <h4>Solar-powered GPS-guided water body cleaning bot</h4>
                <p class="description">An eco-friendly, solar-powered water body cleaner using Arduino Uno, GPS navigation, and DC motors for autonomous operation.</p>
            </div>
            <div class="card" onclick="toggleDescription(this)">
                <h4>Low-Power High-Speed Sense Amplifier Based Flipflop</h4>
                <p class="description">A high-speed, low-power circuit designed using Cadence software, used in modern digital applications like memory and microprocessors.</p>
            </div>
            <div class="card" onclick="toggleDescription(this)">
                <h4>Drowsiness detector</h4>
                <p class="description">A drowsiness detector using OpenCV and Python, integrating dlib for facial landmark detection to monitor eye closure and head movements.</p>
            </div>
            <div class="card" onclick="toggleDescription(this)">
                <h4>Recipe generator</h4>
                <p class="description">A web app built with HTML, CSS, and JavaScript, where users input ingredients, and the app
