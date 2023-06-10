# <!DOCTYPE html>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<link rel="icon" href="Console.png">
<link href="https://fonts.googleapis.com/css2?family=Open+Sans&display=swap" rel="stylesheet">
<style>
    * {
        box-sizing: border-box;
        padding: 0;
        margin: 0;
    }
    
    a {
        color: #001C55;
    }
    
    body {
        background-color: #ffffff;
        font-family: "Open Sans", sans-serif;
    }
    
    .navbar {
        padding-bottom: 10px;
        overflow: hidden;
        background-color: #ffffff;
    }
    
    .main-nav {
        list-style-type: none;
        display: none;
    }
    
    .nav-links,
    .logo {
        text-decoration: none;
        color: rgb(0, 28, 85, 1.0);
        font-family: "Open Sans", sans-serif;
        text-align: center;
        -webkit-font-smoothing: antialiased;
        text-decoration: none;
        font-size: 4.0vw;
        font-weight: 500;
        font-stretch: 130%;
        line-height: normal;
        display: inline-block;
        padding: 38px
    }
    
    .nav-links:hover {
        font-weight: 800;
    }
    
    .main-nav li {
        text-align: center;
        margin-top: -15px;
    }
    
    .logo {
        display: inline-block;
        padding: 17px 10px;
        font-size: 22px;
    }
    
    .navbar-toggle {
        position: absolute;
        top: 30px;
        right: 45px;
        cursor: pointer;
        color: #001C55;
        font-size: 24px;
    }
    
    .active {
        display: block;
    }
    
    #current {
        display: block;
        font-weight: 650;
    }
    
    .image {
        width: 100%;
        text-align: center;
        margin-top: -50px;
    }
    
    .subimage p {
        text-align: center;
        margin-left: auto;
        margin-right: auto;
    }
    
    .bio {
        width: 100%;
        float: left;
        padding-right: 40px;
        padding-left: 40px;
    }
    
    @media screen and (min-width: 1500px) {
        .nav-links {
            font-size: 0.95vw;
        }
        .image {
            width: 40%;
            float: left;
            margin-top: 0px;
        }
        .bio {
            width: 60%;
            float: left;
            padding-right: 120px;
            padding-left: 40px;
        }
        .subimage {
            float: right;
        }
    }
    
    @media screen and (min-width: 800px) {
        .image {
            width: 40%;
            float: left;
            margin-top: 0px;
        }
        .bio {
            width: 60%;
            float: left;
            padding-right: 120px;
            padding-left: 40px;
        }
        .subimage {
            float: right;
        }
        .navbar {
            display: flex;
            justify-content: space-between;
            padding-bottom: 0;
            height: 70px;
            align-items: center;
        }
        .main-nav {
            display: flex;
            margin-right: 30px;
            flex-direction: row;
            justify-content: flex-end;
        }
        .main-nav li {
            margin: 0;
        }
        .nav-links {
            margin-left: 0px;
            margin-right: 0px;
            padding: 17px 18px;
            font-size: 1.0vw;
        }
        .logo {
            margin-top: 0;
        }
        .navbar-toggle {
            display: none;
        }
        .nav-links:hover {
            background-color: rgb(166, 225, 250);
        }
        .navbar {
            position: fixed;
            right: 10px;
            width: 95%;
        }
    }
    
    h1 {
        color: #001C55;
    }
    
    .tooltip {
        position: relative;
        display: inline-block;
    }
    
    .tooltip .tooltiptext {
        visibility: hidden;
        width: 85px;
        background-color: #333333;
        color: #fff;
        text-align: center;
        border-radius: 6px;
        padding: 5px 0;
        font-family: "Open Sans", sans-serif;
        font-size: 0.8em;
        /* Position the tooltip */
        position: absolute;
        z-index: 2;
        bottom: 100%;
        left: 100%;
        margin-left: -64px;
        margin-bottom: 3px;
    }
    
    .tooltip:hover .tooltiptext {
        visibility: visible;
    }
    
    .modal {
        position: fixed;
        /* Stay in place */
        z-index: 3;
        /* Sit on top */
        padding-top: 20px;
        /* Location of the box */
        padding-bottom: 20px;
        left: 0;
        top: 0;
        width: 100%;
        /* Full width */
        height: 100%;
        /* Full height */
        overflow: auto;
        /* Enable scroll if needed */
        background-color: rgb(0, 0, 0);
        /* Fallback color */
        background-color: rgba(0, 0, 0, 0.4);
        /* Black w/ opacity */
    }
    
    .modal-content {
        background-color: #fefefe;
        margin: auto;
        padding: 20px;
        width: 80%;
    }
    
    .close {
        color: #a6b8dd;
        float: right;
        font-size: 28px;
        font-weight: bold;
        margin-top: -15px;
    }
    
    .close:hover,
    .close:focus {
        color: #001C55;
        text-decoration: none;
        cursor: pointer;
    }
</style>

<head>
    <title>Yefim Shneyderman</title>
</head>

<body>
    <div style="z-index: 1; position:fixed; background-color: #ffffff; width:100%; height:85px;">
        <div style="margin-top: 10px; margin-left: 30px; margin-right: 25px;">
            <nav class="navbar">
                <span class="navbar-toggle" id="js-navbar-toggle">
            <i class="fa fa-bars"></i>
        </span>
                <a href="#" class="logo">Yefim Shneyderman</a>
                <ul class="main-nav" id="js-menu">
                    <li>
                        <a href="#" class="nav-links" id="current">Home</a>
                    </li>
                    <li>
                        <a href="#Education" class="nav-links">Education</a>
                    </li>
                    <li>
                        <a href="#Skills" class="nav-links">Skills</a>
                    </li>
                    <li>
                        <a href="#Projects" class="nav-links">Projects</a>
                    </li>
                    <li>
                        <a href="#Experience" class="nav-links">Experience</a>
                    </li>
                    <li>
                        <a href="https://github.com/yshneyderman/yshneyderman.github.io/raw/master/Yefim%20Shneyderman%20Resume.pdf" class="nav-links" style="background-color: rgb(166,225,250,0.5);"><i class="fa fa-download"></i>&nbsp;&nbsp;Resume</a>
                    </li>
                </ul>
            </nav>
        </div>
    </div>
    <div style="text-align:center">
        <div style="display:inline-block; padding-top: 100px; margin-right: 40px; margin-left: 40px;">
            <div class="image" style="display:inline-block;">
                <div class="subimage">
                    <img src="profileoffice.png" width="300px" style="margin-left: auto; margin-right: auto; display: block; margin-top:100px;">
                    <p style="text-align:center;padding-top:20px; font-size:0.95em;color:#001C55; padding-right: 70px; padding-left: 70px; max-width:500px">Photo of me at the Nasdaq office, taken September 2022</p>
                </div>
            </div>
            <div class="bio" style="display:inline-block; margin-top:20px; font-size:1.2em;color:#001C55; max-width:900px; text-align: left;">
                <h1 style="font-size:2.3em; text-align: center; min-width: 330px">Yefim Shneyderman</h1><br>
                <p style="margin-bottom:12px; min-width: 450px">I'm a software developer at Nasdaq and a student at the University of Massachusetts Amherst pursuing my master's degree in Computer Science.</p>
                <p style="margin-bottom:12px; min-width: 450px">As a student I am very passionate about learning and love using technology to solve problems around me.</p>
                <p style="margin-bottom:12px; min-width: 450px">I'm very interested in learning about and working on software engineering/development, artificial intelligence/machine learning, sustainability, finance, and graphic design. I am seeking projects to help gain some more useful skills
                    and contribute to the world.</p>
                <p style="margin-bottom:12px; min-width: 450px">In my free time I like coding, hiking, painting, listening to music, reading, swimming, badminton, and watching my favorite movies/tv shows.</p>
                <div style="text-align:center; margin-top:25px;">
                    <div id="movies" style="z-index: 0;text-align:center; display: inline-block;position:relative; width:230px; height: 50px; background-color:#CCF0FF;padding:10px;cursor: pointer;" onmouseover="shadow('movies')" onmouseout="unshadow('movies')" onclick="window.open('movies.html','_blank')">
                        <p style="font-size:0.9em;color:#001C55;font-weight:600">Favorite Movies / TV</p><br>
                    </div>
                </div>

            </div>
        </div>
    </div>
    </div>
    </div>

    <div id="Contact" style="width:100%; text-align:center; float:left; padding-top:75px; margin-top:-30px; margin-bottom:0px;min-width:600px">
        <h1 style="font-size:2.3em; text-align: center">Contact Me</h1><br>
        <p style="font-size:1.1em; margin-bottom:15px;">Feel free to send a message on LinkedIn...<br> or send me an email at yshneyderman@umass.edu.</p>
        <div class="tooltip">
            <div style="z-index: 0;text-align:center; display: inline-block;position:relative; width:50px; height: 50px; padding:10px;cursor: pointer; font-size: 50px; margin-right:10px;" onmouseover="shadow('giticon')" onmouseout="unshadow('giticon')" onclick="window.open('https://github.com/yshneyderman','_blank')">
                <i id="giticon" class="fa fa-github" style="color:#001C55; border-radius: 100px; width:50px"></i>
            </div>
            <span class="tooltiptext" style="margin-bottom:-15px">GitHub</span>
        </div>
        <div class="tooltip">
            <div style="z-index: 0;text-align:center; display: inline-block;position:relative; width:50px; height: 50px; padding:10px;cursor: pointer; font-size: 50px;margin-right:10px;" onmouseover="shadow('linkedinicon')" onmouseout="unshadow('linkedinicon')" onclick="window.open('https://www.linkedin.com/in/yshneyderman/','_blank')">
                <i id="linkedinicon" class="fa fa-linkedin-square" style="color:#001C55; width:50px; border-radius:12px;"> </i>
            </div>
            <span class="tooltiptext" style="margin-bottom:-15px">LinkedIn</span>
        </div>
        <div class="tooltip">
            <div style="z-index: 0;text-align:center; display: inline-block;position:relative; width:50px; height: 50px; padding:10px;cursor: pointer; font-size: 50px;margin-right:10px;" onmouseover="shadow('emailicon')" onmouseout="unshadow('emailicon')" onclick="window.open('mailto:yshneyderman@umass.edu')">
                <i id="emailicon" class="fa fa-envelope" style="color:#001C55;cursor:pointer; width:60px; border-radius: 8px;"></i>
            </div>
            <span class="tooltiptext" style="margin-bottom:-15px;">Email</span>
        </div>

    </div>

    <div id="Education" style="width:100%; text-align:center; padding-top:75px; margin-top:-30px; margin-bottom:-70px;min-width:600px;">
        <h1 style="font-size:2.3em; text-align: center">Education</h1><br>
        <div style="display: inline-block; width: 100%; margin-left:5px">
            <div id="UMass2" style="max-width:1400px;z-index: 0; text-align:left; display: inline-block;position:relative; width:90%; height: 180px; margin-left:10px; margin-right:10px;background-color:rgb(166,225,250);padding: 30px;min-width:600px">
                <img src="https://img.icons8.com/windows/64/000000/university.png" width="30px" style="float:left" />
                <p style="width:90%; float:left;font-size:1.4em;margin-left:4px;color:#001C55;font-weight:600">University of Massachusetts Amherst</p><br>
                <p style="width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:600">Master of Science</p><br>
                <p style="width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:600">Computer Science</p><br>
                <p style="width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:100">Awards: Bay State Scholars Scholarship
                    &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;</p><br>
            </div>
            <div id="UMassClick2" style="max-width:1400px;min-width:600px;z-index: 0; text-align:left; display: inline-block;position:relative; width:90%; height: 45px; margin-left:10px; margin-right:10px;background-color:#CCF0FF; margin-bottom:0px; padding-bottom:15px; padding-left: 20px; padding-right:20px; padding-top: 10px; cursor: pointer;"
                onclick="expand('masters')" onmouseover="shadow('UMassClick2')" onmouseout="unshadow('UMassClick2')">
                <p style="width:50%; float:left; font-size:1.0em;margin-left:4px;color:#001C55;font-weight:600">Coursework</p>
                <div id="caretmasters"><i class="fa fa-caret-down" aria-hidden="true"></i></div>
            </div>
            <div id="Courses" style="max-width:1400px;display: inline-block; z-index: 0; text-align:center; position:relative; width:90%; margin-left:10px; margin-right:10px;padding-bottom:15px; padding-left: 20px; padding-right:20px; padding-top: 10px; margin-bottom:20px;">
                <div class="coursemasters" style="display:none; z-index: 0; text-align:left; margin-bottom: 10px; position:relative; width:100%; background-color:#e4f7ff; padding-bottom:15px; padding-left: 20px; padding-right:20px; padding-top: 10px; cursor: pointer;">
                    <p style="font-size:0.9em;color:#001C55;font-weight:400">
                        <b>CS515: </b>Algorithms for Data Science,
                        <b>CS574: </b>Intelligent Visual Computing: A Neural Network Approach,
                        <b>CS590J: </b>Cyber Effects: Reverse Engineering, Exploit Analysis, and Capability Development,
                        <b>CS563: </b>Internet Law and Policy,
                        <b>CS682: </b>Neural Networks: A Modern Introduction,
                        <b>SCH-MGMT 644: </b>Economic Analysis for managers,
                        <b>CS560: </b>Introduction to Network and Computer Security
                </div>
            </div>
        </div>
        <br>
        <div style="display: inline-block; margin-left:5px">
            <div id="UMass" style="max-width:1400px;z-index: 0; text-align:left; display: inline-block;position:relative; width:90%; height: 245px; margin-left:10px; margin-right:10px;background-color:rgb(166,225,250);padding: 30px;min-width:600px">
                <img src="https://img.icons8.com/windows/64/000000/university.png" width="30px" style="float:left" />
                <p style="width:90%; float:left;font-size:1.4em;margin-left:4px;color:#001C55;font-weight:600">University of Massachusetts Amherst</p><br>
                <p style="width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:600">Bachelor of Science</p><br>
                <p style="width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:600">Double Major in Computer Science & Mathematics (Computing)</p><br>
                <p style="width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:100">Awards: Dean's List, Cum Laude, John and Abigail Adams Scholarship</p><br>
                <p style="width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:100">Activities and Societies: UMass Cybersecurity Club, UMass Design Club, UMass Association for Computing Machinery</p><br>
            </div>
            <div id="UMassClick" style="max-width:1400px;min-width:600px;z-index: 0; text-align:left; display: inline-block;position:relative; width:90%; height: 45px; margin-left:10px; margin-right:10px;background-color:#CCF0FF; margin-bottom:0px; padding-bottom:15px; padding-left: 20px; padding-right:20px; padding-top: 10px; cursor: pointer;"
                onclick="expand('bachelors')" onmouseover="shadow('UMassClick')" onmouseout="unshadow('UMassClick')">
                <p style="width:50%; float:left; font-size:1.0em;margin-left:4px;color:#001C55;font-weight:600">Coursework</p>
                <div id="caretbachelors"><i class="fa fa-caret-down" aria-hidden="true"></i></div>
            </div>
            <div id="Courses" style="max-width:1400px;display: inline-block; z-index: 0; text-align:center; position:relative; width:90%; margin-left:10px; margin-right:10px;padding-bottom:15px; padding-left: 20px; padding-right:20px; padding-top: 10px; margin-bottom:20px;">
                <div class="coursebachelors" style="display:none; z-index: 0; text-align:left; margin-bottom: 10px; position:relative; width:100%; background-color:#e4f7ff; padding-bottom:15px; padding-left: 20px; padding-right:20px; padding-top: 10px; cursor: pointer;">
                    <p style="font-size:0.9em;color:#001C55;font-weight:600">Computer Science / Math:
                        <p style="font-size:0.9em;color:#001C55;font-weight:400">
                            Calculus (I, II, III), Physics (I, II), Problem Solving with Computers, Data Structures, Computation, Programming Methodology, Computer Systems Principles, Reasoning Under Uncertainty, Algorithms, Artificial Intelligence, Web Development, Machine Learning,
                            Operating Systems, Linear Algebra, Statistics (I, II), Differential Equations, Abstract Algebra I, Networks and Security, Applications of Natural Language Processing, Scientific Computing, Combinatorics and Graph Theory
                </div>
                <div class="coursebachelors" style="z-index: 0; text-align:left; display: none ;position:relative; width:100%; background-color:#e4f7ff; padding-bottom:15px; padding-left: 20px; padding-right:20px; padding-top: 10px; cursor: pointer;">
                    <p style="font-size:0.9em;color:#001C55;font-weight:600">Other:
                        <p style="font-size:0.9em;color:#001C55;font-weight:400">
                            European History, U.S. History, French, English/Writing, Comparative Literature (International Short Story), Comparative Literature (Dystopian), Microeconomics, Environmental Science</p>
                </div>
            </div>
        </div>
    </div>

    <div id="Skills" style="width:100%; text-align:center; float:left; padding-top:75px; min-width:600px;">
        <h1 style="font-size:2.3em; text-align: center">Skills</h1><br>
        <div style="display:inline-block; max-width:1400px;">
            <div style="text-align:left; float:left; width:50%; padding-right: 20px; padding-left:60px;">
                <p style="font-size:1.2em;color:#001C55;font-weight:600">Computer Science</p>
                <div style="padding-left:30px; padding-top:5px;font-size:1.0em;color:#001C55;">
                    <p>
                        <ul style="padding-bottom:10px;"><b>Languages:</b> Java, Python, Go, JavaScript, C/C++, MATLAB, Assembly
                        </ul>
                    </p>
                    <p>
                        <ul style="padding-bottom:10px;"><b>Skills:</b> 
                            Algorithms,
                            Data Structures, 
                            Unit Testing, 
                            Image Processing, 
                            Machine Learning, 
                            Data Visualization, 
                            Computational Complexity, 
                            Networking,
                            Artificial Intelligence, 
                            Neural Networks, 
                            GUIs, 
                            Threads/Processes, 
                            Linux,
                            Web Development, 
                            Object Oriented Programming, 
                            Operating Systems,
                            Cloud,
                            Blockchain,
                            CI/CD,
                            Infrastructure as Code,
                            Architecture,
                            Documentation
                        </ul>
                    </p>
                    <p>
                        <ul style="padding-bottom:10px;"><b>Technologies:</b> 
                            HTML, 
                            CSS, 
                            jQuery, 
                            Node.js, 
                            Express.js,
                            Matplotlib, 
                            scikit-learn, 
                            Pandas, 
                            Pytorch, 
                            NumPy, 
                            MongoDB, 
                            Mongoose, 
                            Mustache, 
                            Express, 
                            PostgreSQL, 
                            SQL,
                            Spring Boot, 
                            Flask,
                            React, 
                            Docker, 
                            Kubernetes, 
                            Google Cloud, 
                            BigQuery, 
                            Bitcoin,
                            Solana,
                            Corvil,
                            Helm,
                            Kubernetes,
                            Grafana,
                            Loki,
                            Prometheus,
                            AWS,
                            Terraform
                        </ul>
                    </p>
                    <p>
                        <ul style="padding-bottom:10px;"><b>Tools:</b> 
                            ThoughtSpot, 
                            DataStudio, 
                            Looker,
                            Confluence, 
                            JIRA,
                            git,
                            GitLab,
                            K9s,
                            Lens,
                            VSCode,
                            Eclipse,
                            Pycharm,
                            IntelliJ
                        </ul>
                    </p>
                </div>
            </div>
            <div style="text-align:left; float:right; width:50%; padding-right: 60px; padding-left:20px;">
                <p style="font-size:1.2em;color:#001C55;font-weight:600">Videography and Design</p>
                <div style="padding-left:30px; padding-top:5px;font-size:1.0em;color:#001C55;">
                    <p>
                        <p>
                            <ul style="padding-bottom:10px;">I have 7 years of experience in Videography and Graphic Design through self learning and my volunteering at North Andover CAM.</ul>
                        </p>
                        <p>
                            <p>
                                <ul style="padding-bottom:10px;">Alongside my skills with camcorders, GoPro, DSLR cameras, lighting, directing, technical directing, audio, script writing, and storyboarding, I also have experience with: </ul>
                            </p>
                            <p>
                                <p>
                                    <ul style="padding-bottom:10px;"><b>Advanced: </b>Premiere Pro, Final Cut Pro X (Video Editing), Photoshop (Graphic Design), Illustrator (Graphic Design), Microsoft Office Suite</ul>
                                </p>
                                <p>
                                    <ul style="padding-bottom:10px;"><b>Intermediate:</b> After Effects (Visual Effects and Animation), Lightroom (Photography), InDesign (Page Design), XD (UX/UI Design), Audition (Audio)</ul>
                                </p>
                </div>
            </div>
        </div>
    </div>
    <br>
    <div id="Projects" style="text-align:center; float:left; padding-top:75px; width:100%; min-width:600px;">
        <h1 style="font-size:2.3em; text-align: center;">Projects</h1><br>
        <h1 style="font-size:1.1em; text-align: center; font-weight:400; margin-top:-10px; margin-bottom:10px">Click on a project for more information</h1><br>

        <div style="display: inline-block;  max-width:1600px; padding-left:50px; padding-right:50px;">
            <div id="490A" style="z-index: 0;text-align:left; display: inline-block;position:relative; width:515px; height: 215px; margin-left:8px; margin-right:8px; background-color:rgb(166,225,250);padding:20px;  margin-bottom: 20px; padding: 30px; cursor: pointer;"
                onmouseover="shadow('490A')" onmouseout="unshadow('490A')" onclick="modal('490AModal')">
                <img src="icons8-repository-96.png" width="31px" style="float:left;padding:5px;">
                <p style="float:left;font-size:1.4em;margin-left:4px;color:#001C55;font-weight:600">CS490A Project</p><br>
                <p style="float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:400">Final project to perform sentiment analysis of financial tweets to predict change in stock price.</p><br>
                <p style="float:left;margin-top: 10px; font-size:1.0em;color:#808080;font-weight:400">Updated on Dec 2020</p><br>
                <div style="float:right;position:absolute;bottom:10px;right:17px">
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/python.png" width="35px" /><span class="tooltiptext">Python</span></div>
                </div>
            </div>

            <div id="490AModal" class="modal">
                <div class="modal-content" style="height:535px; text-align:center; width:950px">
                    <span class="close" id="490AModalClose">&times;</span>
                    <p style="font-size:1.4em;color:#001C55;font-weight:600">CS490A Project</p>
                    <div style="margin-bottom:30px;float:left; width:50%; text-align: center; padding:10px; margin-top: 80px; background-color:#CCF0FF;">
                        <img src="Images/490A.png" width="400px" style="margin-top:20px;border-radius:0px; border-style:solid; border-color:#001C55;">
                        <p style="margin-top: 10px; font-size:0.9em;color:#001C55;font-weight:400; text-align: center; margin-bottom:20px;">Candlestick chart of AAPL stock.</p>
                    </div>
                    <div style="float:right; width:50%; text-align:left; padding:10px; margin-top:45px; padding-left:20px">
                        <p style="float:left;margin-top: 10px; font-size:0.9em;color:#001C55;font-weight:400; text-align: left">
                            Final project for Natural Language Processing class where I worked on a team of 3 to predict daily changes in stock prices using sentiment-labeled Twitter data from the corresponding time period. <br><br> We scraped 26,321 tweets,
                            each of which referenced one of 6 different companies (AAPL, AMD, ARW, CHGG, UIS, XBIT), and performed sentiment analysis on them using VADER. We then fed the VADER sentiment scores, along with other tweet metadata such as number
                            of comments, number of retweets, and number of likes, into various machine learning models that attempted to (1) classify the direction of stock price change (up or down) and (2) predict the amount of change. Overall, we found
                            no statistically significant indication that our model was successful at predicting either metric, but have identified many important bottlenecks to tackle in future research.
                            <br><br>
                        </p>
                        <div style="text-align:center">
                            <button id="yshneydermanGithub" style="background-color:#CCF0FF; border:none; width:180px; color:#001C55; padding:10px; cursor: pointer;" onmouseover="shadow('yshneydermanGithub')" onmouseout="unshadow('yshneydermanGithub')" onclick=" window.open('https://github.com/jamesqo/stock-market-prediction','_blank')">
                    <i class="fa fa-fw fa-github" style="color:#001C55"></i>
                GitHub Repository
                </button>
                        </div>
                    </div>
                </div>
            </div>

            <div id="yshneyderman" style="z-index: 0;text-align:left; display: inline-block;position:relative; width:515px; height: 215px; margin-left:8px; margin-right:8px; background-color:rgb(166,225,250);padding:20px;  margin-bottom: 20px; padding: 30px; cursor: pointer;"
                onmouseover="shadow('yshneyderman')" onmouseout="unshadow('yshneyderman')" onclick="modal('yshneydermanModal')">
                <img src="icons8-repository-96.png" width="31px" style="float:left;padding:5px;">
                <p style="float:left;font-size:1.4em;margin-left:4px;color:#001C55;font-weight:600">yshneyderman.github.io</p><br>
                <p style="float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:400">A personal website template available to modify and use for your own. Based on Saad Pasta, Ashutosh Hathidara, Bootstrap Portfolio designs.</p><br>
                <p style="float:left;margin-top: 10px; font-size:1.0em;color:#808080;font-weight:400">Updated on Aug 2020</p><br>
                <div style="float:right;position:absolute;bottom:10px;right:17px">
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/javascript.png" width="35px" /><span class="tooltiptext">JavaScript</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/html-5.png" width="35px" /><span class="tooltiptext">HTML</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/css3.png" width="35px" /><span class="tooltiptext">CSS</span></div>
                </div>
            </div>

            <div id="yshneydermanModal" class="modal">
                <div class="modal-content" style="height:535px; text-align:center; width:950px">
                    <span class="close" id="yshneydermanModalClose">&times;</span>
                    <p style="font-size:1.4em;color:#001C55;font-weight:600">yshneyderman.github.io</p>
                    <div style="margin-bottom:30px;float:left; width:50%; text-align: center; padding:10px; margin-top: 80px; background-color:#CCF0FF;">
                        <img src="Images/Yshneyderman.png" width="400px" style="margin-top:20px;border-radius:0px; border-style:solid; border-color:#001C55;">
                        <p style="margin-top: 10px; font-size:0.9em;color:#001C55;font-weight:400; text-align: center; margin-bottom:20px;">Old Website view and layout.</p>
                    </div>
                    <div style="float:right; width:50%; text-align:left; padding:10px; margin-top:45px; padding-left:20px">
                        <p style="float:left;margin-top: 10px; font-size:0.9em;color:#001C55;font-weight:400; text-align: left">
                            A personal website template available to modify and use for your own. Based on Saad Pasta, Ashutosh Hathidara, Bootstrap Portfolio designs, but all in single page HTML/CSS.<br><br> Started working on personal website in March 2019
                            to keep track of educational and professional interests and showcase skills for potential employers. I've been adding to it anytime new experiences, skills, or classes come up that I believe would be useful to my profile as an
                            applicant to academic programs or work opportunities.<br><br> Added personal and fun information over time. Feel free to copy and change for your own purposes!<br><br> Link to the GitHub repository:<br><br>
                        </p>
                        <div style="text-align:center">
                            <button id="yshneydermanGithub" style="background-color:#CCF0FF; border:none; width:180px; color:#001C55; padding:10px; cursor: pointer;" onmouseover="shadow('yshneydermanGithub')" onmouseout="unshadow('yshneydermanGithub')" onclick=" window.open('https://github.com/yshneyderman/yshneyderman.github.io','_blank')">
                    <i class="fa fa-fw fa-github" style="color:#001C55"></i>
                GitHub Repository
                </button>
                        </div>
                    </div>
                </div>
            </div>

            <div id="30days" style="z-index: 0;text-align:left; display: inline-block;position:relative; width:515px; height: 215px; margin-left:8px; margin-right:8px;background-color:rgb(166,225,250);padding:20px;  margin-bottom: 20px; padding: 30px; cursor: pointer;"
                onmouseover="shadow('30days')" onmouseout="unshadow('30days')" onclick="modal('30daysModal')">
                <img src="icons8-repository-96.png" width="31px" style="float:left;padding:5px;">
                <p style="float:left;font-size:1.4em;margin-left:4px;color:#001C55;font-weight:600">30DaysCoding.com</p><br>
                <p style="float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:400">Website to teach coding practices and interview preparation. Wrote guides and documents.</p><br>
                <p style="float:left;margin-top: 10px; font-size:1.0em;color:#808080;font-weight:400">Updated May 2020</p><br>
                <div style="float:right;position:absolute;bottom:10px;right:17px">
                    <div class="tooltip"><img src="https://img.icons8.com/fluent/48/000000/microsoft-word-2019.png" width="35px" /><span class="tooltiptext">Word</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/office/80/000000/pdf.png" width="35px" /><span class="tooltiptext">PDF</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/javascript.png" width="35px" /><span class="tooltiptext">JavaScript</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/html-5.png" width="35px" /><span class="tooltiptext">HTML</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/css3.png" width="35px" /><span class="tooltiptext">CSS</span></div>
                </div>
            </div>

            <div id="30daysModal" class="modal">
                <div class="modal-content" style="height:580px; text-align:center; width:950px">
                    <span class="close" id="30daysModalClose">&times;</span>
                    <p style="font-size:1.4em;color:#001C55;font-weight:600">30dayscoding.com</p>
                    <div style="float:left; width:50%; text-align: center; padding:10px; margin-top: 60px; background-color:#CCF0FF;">
                        <img src="Images/30days1.png" width="200px" style="margin-top:50px; border-radius:0px; border-style:solid; border-color:#001C55;display:inline-block">
                        <img src="Images/30days2.png" width="200px" style="border-radius:0px; border-style:solid; border-color:#001C55;display:inline-block">
                        <img src="Images/30days3.png" width="200px" style="border-radius:0px; border-style:solid; border-color:#001C55;display:inline-block">
                        <img src="Images/30days4.png" width="200px" style="border-radius:0px; border-style:solid; border-color:#001C55; display:inline-block">
                        <p style="margin-top: 10px; font-size:0.9em;color:#001C55;font-weight:400; text-align: center; margin-bottom: 50px">Screenshots of website and interview guide.</p>
                    </div>
                    <div style="float:right; width:50%; text-align:left; padding:10px; margin-top:10px;">
                        <p style="padding-left:20px;float:left;margin-top: 10px; font-size:0.9em;color:#001C55;font-weight:400; text-align: left">
                            An educational website I worked on with a good friend and fellow UMass Amherst CS major <a href="https://github.com/aryansingh12">Aryan Singh</a>. We both agreed that it was unfair for modern resources to help teach people to improve
                            their skills were behind paywalls and only available to people who were members of certain clubs/universities so we sought to create a repository of all of our experience with CS interviews. We had both passed interviews in FAANG
                            companies and reached out to other friends who had similar experience to put together free links, documents, and resources to help teach these concepts.<br><br> We started working in early 2020 and published the site when COVID-19
                            was declared as a pandemic and everyone was at home - the perfect time to pick up/refresh these skills.<br><br> The initial LinkedIn posts recieved thousands of views and at some points the website had a few hundred users. The
                            site was also featured in newsletters by the CICS department in emails recommending resources for career development. There are still current plans to add more free content such as resume parsers, more tips for acing an interview,
                            and documents written by Aryan and I to discuss programming concepts like Arrays, Linked Lists, etc. with helpful graphics.<br>
                        </p>
                    </div>
                </div>
            </div>

        <div id="CS326" style="z-index: 0;text-align:left; display: inline-block;position:relative; width:515px; height: 215px; margin-left:8px; margin-right:8px;background-color:rgb(166,225,250);padding:20px;  margin-bottom: 20px; padding: 30px; cursor: pointer;" onmouseover="shadow('CS326')" onmouseout="unshadow('CS326')" onclick="modal('CS326Modal')">
            <img src="icons8-repository-96.png" width="31px" style="float:left;padding:5px;">
            <p style="float:left;font-size:1.4em;margin-left:4px;color:#001C55;font-weight:600">CS326 Projects</p><br>
            <p style="float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:400">Small Web Development projects from textbook and one team-based large Full Stack App project at the end.</p><br>
            <p style="float:left;margin-top: 10px; font-size:1.0em;color:#808080;font-weight:400">Updated Dec 2019</p><br>
            <div style="float:right;position:absolute;bottom:10px;right:17px">
            <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/nodejs.png" width="35px"/><span class="tooltiptext">NodeJS</span></div>
            <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/mongodb.png" width="35px"/><span class="tooltiptext">MongoDB</span></div>
            <div class="tooltip"><img src="https://static.thenounproject.com/png/117898-200.png" style="transform: rotate(-90deg)" width="35px"/><span class="tooltiptext">Mustache</span></div>
            <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/javascript.png" width="35px"/><span class="tooltiptext">JavaScript</span></div>
            <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/html-5.png" width="35px"/><span class="tooltiptext">HTML</span></div>
            <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/css3.png" width="35px"/><span class="tooltiptext">CSS</span></div>
            
            </div>
        </div>

        <div id="CS326Modal" class="modal">
            <div class="modal-content" style="height:535px; text-align:center; width:950px">
            <span class="close" id="CS326ModalClose">&times;</span>
            <p style="font-size:1.4em;color:#001C55;font-weight:600">CS326</p>
                <div style="float:left; width:50%; text-align: center; padding:10px; margin-top: 60px; background-color:#CCF0FF;">
                <img src="Images/TuneRater.png" width="400px" style="margin-top:50px; border-radius:0px; border-style:solid; border-color:#001C55;display:inline-block">
                <p style="margin-top: 10px; font-size:0.9em;color:#001C55;font-weight:400; text-align: center; margin-bottom: 50px">TuneRater final project screenshot.</p> 
                </div>
                <div style="float:right; width:50%; text-align:left; padding:10px; margin-top:10px;">
                <p style="padding-left:20px;float:left;margin-top: 10px; font-size:0.9em;color:#001C55;font-weight:400; text-align: left">
                    A 300 level class covering Web Development which began with a basic introduction to HTML/CSS and proceeded to teach about fundamental web technologies, industry trends, and important full stack concepts. Class featured weekly mini-projects as well as a final group project of our choosing.<br>
                    <br><b>TuneRater</b><br> Class formed teams of four and brainstormed a full stack application to develop that met the requirements of implementing certain web technologies and skills we learned through the year. The team worked in a Scrum/agile-like
                            development flow with weekly standup meetings to work towards our goal of creating and presenting a fully functioning web app. The team came up with "TuneRater" - a site for aspiring musicians to create and share their music with
                            a more art based community that could listen and critique their skills as an artist. We felt the need for this website in a world where Spotify and YouTube often did not provide the feedback an artist wants. The project uses Data
                            Storage of music files, info, and account info on MongoDB, and a Node.js server to interact with (rating, comenting, and sending this info to the database)<br>
                        </p>
                    </div>
                </div>
            </div>

            <div id="Nacam" style="z-index: 0;text-align:left; display: inline-block;position:relative; width:515px; height: 215px; margin-left:8px; margin-right:8px;background-color:rgb(166,225,250);padding:20px;  margin-bottom: 20px; padding: 30px; cursor: pointer;"
                onmouseover="shadow('Nacam')" onmouseout="unshadow('Nacam')" onclick="modal('NacamModal')">
                <img src="icons8-repository-96.png" width="31px" style="float:left;padding:5px;">
                <p style="float:left;font-size:1.4em;margin-left:4px;color:#001C55;font-weight:600">North Andover CAM</p><br>
                <p style="float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:400">Volunteer Projects for North Andover Community Access and Media.</p><br>
                <p style="float:left;margin-top: 10px; font-size:1.0em;color:#808080;font-weight:400">Updated Apr 2020</p><br>
                <div style="float:right;position:absolute;bottom:10px;right:17px">
                    <div class="tooltip"><img src="https://img.icons8.com/fluent/48/000000/adobe-creative-cloud.png" width="35px" /><span class="tooltiptext">Creative Cloud</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/adobe-photoshop.png" width="35px" /><span class="tooltiptext">Photoshop</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/adobe-illustrator.png" width="35px" /><span class="tooltiptext">Illustrator</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/adobe-premiere-pro.png" width="35px" /><span class="tooltiptext">Premiere Pro</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/adobe-audition.png" width="35px" /><span class="tooltiptext">Audition</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/adobe-after-effects.png" width="35px" /><span class="tooltiptext">After Effects</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/final-cut-pro-x.png" width="35px" /><span class="tooltiptext">Final Cut Pro</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/adobe-lightroom.png" width="35px" /><span class="tooltiptext">Lightroom</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/adobe-xd.png" width="35px" /><span class="tooltiptext">XD</span></div>
                    <div class="tooltip"><img src="https://vignette.wikia.nocookie.net/logopedia/images/1/1e/Adobe_Media_Encoder_%282012-2013%29.png/revision/latest/scale-to-width-down/340?cb=20160228175700" width="27px" style="margin-bottom:3px" /><span class="tooltiptext">Media Encoder</span></div>
                    <div class="tooltip"><img src="https://img.icons8.com/color/48/000000/adobe-indesign.png" width="35px" /><span class="tooltiptext">InDesign</span></div>
                </div>
            </div>

            <div id="NacamModal" class="modal">
                <div class="modal-content" style="height:850px; text-align:center; width:950px">
                    <span class="close" id="NacamModalClose">&times;</span>
                    <p style="font-size:1.4em;color:#001C55;font-weight:600">NACAM</p>
                    <div style="float:left; width:50%; text-align: center; padding:10px; margin-top: 60px; background-color:#CCF0FF;">
                        <img src="Images/NACAMYefim.png" width="400px" style="margin-top:50px; border-radius:0px; border-style:solid; border-color:#001C55;display:inline-block">
                        <p style="margin-top: 10px; font-size:0.9em;color:#001C55;font-weight:400; text-align: center; margin-bottom: 50px">Picture of me directing a football game.</p>
                    </div>
                    <div style="float:right; width:50%; text-align:left; padding:10px; margin-top:10px;">
                        <p style="padding-left:20px;float:left;margin-top: 10px; font-size:0.9em;color:#001C55;font-weight:400; text-align: left">
                            <a href="https://northandovercam.org/">NACAM Website</a><br>
                            <a href="https://www.youtube.com/channel/UC13W-m9GqbT1miA6x_5oaaw">NACAM YouTube</a><br><br> The North Andover Community Access and Media is an organization that produces community access programming on the Public, Education, and
                            Government access channels in North Andover. The organization's members are able to use studio equipment for productions to be featured on the channels as well as have access to trainings and assist in real productions that the
                            studio helps out with around town such as sporting events, concerts, town meeting, festivals, etc.<br><br> I joined NACAM in October 2013 and in my time in High School I accumulated the most volunteer hours over any other member
                            and spent a lot of time learning software and techniques listed in my skills section. As a member I volunteered at a lot of NACAM productions in a variety of roles such as cameraman, director, technical director, audio, equipment
                            setup, floor director, lighting, editor, etc. I worked with employees at NACAM to film community events linked below:<br><br>
                            <a href="https://www.youtube.com/watch?v=rZrBxhH-jTo">8568F VEX Robotics Worlds Reveal 2017</a><br>
                            <a href="https://www.youtube.com/watch?v=KHIBS7pYK-k">Mr. North Andover 2017</a><br>
                            <a href="https://www.youtube.com/watch?v=fYVrW_1jExI">Spring Concert 2016</a><br>
                            <a href="https://www.youtube.com/watch?v=w2XbsMBFklc">Spring Concert 2015</a><br>
                            <a href="https://www.youtube.com/watch?v=4a-HMKvGnJE">Winter Concert 2016</a><br>
                            <a href="https://www.youtube.com/watch?v=-iRlHl_BANo">All Town Band Festival 2016</a><br>
                            <a href="https://www.youtube.com/watch?v=BrskaRoJR6A">North Andover Football Games</a><br>
                            <a href="https://www.youtube.com/watch?v=nfJPpJNsgRs">North Andover Town Meeting 2017</a><br>
                            <a href="https://www.youtube.com/watch?v=Y0CYsUPCaAc">North Andover Santa Parade 2019</a><br>
                            <a href="https://www.youtube.com/watch?v=-BgGIh3Zzyc">Santa Call In Show</a><br>
                            <a href="https://www.youtube.com/watch?v=062_H5Gi2XI">The North Andover Journal</a><br><br> These links represent a small amount of the work that is available on YouTube. I volunteered at a variety of these sorts of events as well
                            as helping out with Youth Programs and other smaller projects around the town.<br>
                        </p>
                    </div>
                </div>
            </div>
        </div>

    </div>
    <br>
    <div id="Experience" style="width:100%; text-align:center; float:left; padding-top:75px; min-width:630px;">
        <div style="display: inline-block;  max-width:1600px;">
            <h1 style="font-size:2.3em; text-align: center">Experience</h1><br>
            <div style="padding-left:20px; padding-right:20px;">
                <div id="Nasdaq0" style="max-width:1400px; z-index: 0; text-align:left; display: inline-block;position:relative; width:90%; margin-left:8px; margin-right:8px; margin-bottom: 30px; background-color:rgb(166,225,250);padding: 30px;">
                    <img src="https://pbs.twimg.com/profile_images/1128741286461227014/Yzrhjz0n_400x400.png" width="35px" style="float:left" />
                    <p style="width:70%; float:left;font-size:1.4em;color:#001C55;font-weight:600; padding-top:4px; margin-left:12px">Software Developer</p><br>
                    <p style="width:90%;float:left;margin-top: 15px; font-size:1.0em;color:#001C55;font-weight:600;">Nasdaq</p><br>
                    <p style="width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:600">Jul 2021 - Present </p><br>
                    <p style="min-width: 460px; width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:100">
                        Created data ingestion pipeline for Nasdaq performance data into GCP and analyzed and reported trends.<br> Updated and maintained message decoders and developed scripts to automate the process for future markets and updates<br> 
                        Mentored intern projects in Digital Assets and Record Linkage.</p><br>
                </div>
                <div id="Nasdaq1" style="max-width:1400px; z-index: 0; text-align:left; display: inline-block;position:relative; width:90%; margin-left:8px; margin-right:8px; margin-bottom: 30px; background-color:rgb(166,225,250);padding: 30px;">
                    <img src="https://pbs.twimg.com/profile_images/1128741286461227014/Yzrhjz0n_400x400.png" width="35px" style="float:left" />
                    <p style="width:70%; float:left;font-size:1.4em;color:#001C55;font-weight:600; padding-top:4px; margin-left:12px">Full Stack Software Engineering Intern</p><br>
                    <p style="width:90%;float:left;margin-top: 15px; font-size:1.0em;color:#001C55;font-weight:600;">Nasdaq - Internship</p><br>
                    <p style="width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:600">Jun 2020 - Aug 2020 • 3 mos </p><br>
                    <p style="min-width: 460px; width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:100">
                        Created Secure Multiparty Compute / Homomorphic Encryption proof of concept project with team at Nasdaq Boston Innovation Lab.<br> Learned to use and work with React.js, PostgreSQL, Java Spring Boot, Kubernetes, Docker, Flask.<br> Presented
                        the project to Nasdaq Executives for evaluation on business promise and profitability for multiple use cases.</p><br>
                </div>
                <div id="Indigo" style="max-width:1400px; z-index: 0; text-align:left; display: inline-block;position:relative; width:90%; margin-left:8px; margin-right:8px; margin-bottom: 30px; background-color:rgb(166,225,250);padding: 30px;">
                    <img src="https://yt3.ggpht.com/ytc/AAUvwnhFG95NUq1eDbyu9cvGcVN7843W794jkfqqmkBMEA=s900-c-k-c0x00ffffff-no-rj" width="35px" style="float:left" />
                    <p style="width:70%; float:left;font-size:1.4em;margin-left:4px;color:#001C55;font-weight:600; padding-top:4px; margin-left:12px">Independent Contractor / Laboratories & Facilities Intern</p><br>
                    <p style="width:90%;float:left;margin-top: 15px; font-size:1.0em;color:#001C55;font-weight:600;">Indigo Ag. - Internship</p><br>
                    <p style="width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:600">Jun 2018 - Jun 2021 • 3 yrs </p><br>
                    <p style="min-width: 460px;width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:100">
                        Collaborated with environmental health and safety consultants, and managers to create educational multimedia content for Indigo’s online safety training site. Launched the platform to track user progress and ensure OSHA compliance.<br>                Used technology skills to work on projects regarding office security, training employees, asset tracking, seating, etc.<br> Created pages, filters, maps, graphics, and SOP’s for a variety of tools used by the team including JIRA, OfficeSpace,
                        Simpplr, SharePoint, and assisted in regular Lab & Facilities duties.</p><br>
                </div>
                <div id="NACAM" style="max-width:1400px; z-index: 0; text-align:left; display: inline-block;position:relative; width:90%; margin-left:8px; margin-right:8px; margin-bottom: 30px; background-color:rgb(166,225,250);padding: 30px;">
                    <img src="data:image/png;base64,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"
                        width="35px" style="float:left" />
                    <p style="width:70%; float:left;font-size:1.4em;margin-left:4px;color:#001C55;font-weight:600; padding-top:4px; margin-left:12px">Volunteer / Youth Representative</p><br>
                    <p style="width:90%;float:left;margin-top: 15px; font-size:1.0em;color:#001C55;font-weight:600;">North Andover Community Access and Media - Volunteer</p><br>
                    <p style="width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:600">Oct 2013 - May 2020 • 7 yrs </p><br>
                    <p style="min-width: 460px;width:90%;float:left;margin-top: 10px; font-size:1.0em;color:#001C55;font-weight:100">
                        Led and assisted in community film events and projects at the tv station.<br> Received training and experience working with professional video-editing/related software and equipment.<br> Elected Youth Representative to work with staff
                        to develop programs for youth members</p><br>
                </div>
            </div>
        </div>
    </div>
</body>

<script>
    let mainNav = document.getElementById("js-menu");
    let navBarToggle = document.getElementById("js-navbar-toggle");

    navBarToggle.addEventListener("click", function() {
        mainNav.classList.toggle("active");
    });
</script>

<script>
    function shadow(id) {
        let div = document.getElementById(id);
        div.style.boxShadow = "0 4px 9px 0 rgba(0, 0, 0, 0.2)";
    }

    function unshadow(id) {
        let div = document.getElementById(id);
        div.style.boxShadow = "";
    }

    function expand(id) {
        let div = document.getElementById("caret" + id);
        let elements = document.getElementsByClassName("course" + id);
        if (div.innerHTML === '<i class="fa fa-caret-down" aria-hidden="true"></i>') {
            div.innerHTML = '<i class="fa fa-caret-up" aria-hidden="true"></i>';
            for (var i = 0; i < elements.length; i++) {
                elements[i].style.display = "inline-block";
            }
        } else {
            div.innerHTML = '<i class="fa fa-caret-down" aria-hidden="true"></i>';
            for (var i = 0; i < elements.length; i++) {
                elements[i].style.display = "none";
            }
        }
    }
</script>
<script>
    let list = document.getElementsByClassName("modal")
    for (let i = 0; i < list.length; i++) {
        list[i].style.display = "none";
    }

    function modal(id) {
        console.log(id);
        var modal = document.getElementById(id);
        console.log(modal);
        // Get the button that opens the modal
        var btn = document.getElementById(id + "Button");

        // Get the <span> element that closes the modal
        var span = document.getElementById(id + "Close");
        console.log(span);

        // When the user clicks on <span> (x), close the modal
        span.onclick = function() {
            modal.style.display = "none";
        }

        // When the user clicks the button, open the modal 
        modal.style.display = "block";

        // When the user clicks anywhere outside of the modal, close it
        window.onclick = function(event) {
            if (event.target == modal) {
                modal.style.display = "none";
            }
        }
    }
</script>


</html>-tech
