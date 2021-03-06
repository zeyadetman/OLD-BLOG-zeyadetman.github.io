---
layout: default
title: Projects
permalink: /projects/
---
<link rel="stylesheet" href="/css/languages.css">
<link rel="stylesheet" href="/css/projects.css">
<script async defer src="https://buttons.github.io/buttons.js"></script>

<h1>Codes & Projects
<a class="github-button" href="https://github.com/zeyadetman" data-size="small" data-show-count="true" aria-label="Follow @zeyadetman on GitHub">Follow @zeyadetman</a></h1>


<div class="projects-content">
    <div class="projects-intro">
    <img src="https://github.com/zeyadetman/zeyadetman-old-blog/blob/master/images/logo.png?raw=true" style="width:30%;" class="sitelogo img-fluid">
    <p>My Hobby is coding, creating open-source projects, I can code in many languages, the main goal is to build good things. If you want to create a project with me, <a href="mailto:zeyadetman@gmail.com">Send Mail...</a> </p>
    </div>
    <div class="latest">
    <h3>Latest Repos</h3>    
        <div class="projects" id="latest-projects">
        </div>
    </div>
</div>

<div class="all-projects">
    <div class="frontend projectssection"  id="frontendprojects">
        <h3 class="projects-title">Front-End Development <a href="{{page.url}}#frontendprojects"><i class="fas fa-link"></i></a></h3>
        <div class="cards" id="frontendCards">
        </div>
    </div>
    <div class="softwaredev projectssection"  id="softwareprojects">
        <h3 class="projects-title">Software Development <a href="{{page.url}}#softwareprojects"><i class="fas fa-link"></i></a></h3>
        <div class="cards" id="softwaredevCards">
        </div>
    </div>
<div>

<script>

const url = 'https://api.github.com/users/zeyadetman/repos?sort=created';
fetch(url,{method:'GET'}).then((res)=>res.json())
    .then((res)=>{
        let data = res.filter(repo=>(repo.fork == false))
        data = data.filter((repo,indx,data)=>indx<6)
        data.forEach((repo) => {
            let lang = repo.language;
            let desc = repo.description;
            if(desc == null)
                desc = 'description not found'
            if(lang == "C++")
                lang = 'cpp';
            else if(lang == "C#")
                lang = 'csharp';
            lang = lang.toLowerCase();
            document.getElementById('latest-projects').innerHTML+=`
            <div class="project">
                <a href="${repo.html_url}" class="project-name">${repo.name}</a>
                <span class="${lang}">${lang}</span>
                <p class="project-description">${desc}</p>
            </div>
            `;
        });
    })
    .catch(()=>console.log('err'));


const webimgs = `/images/projects/web/`;
const softwareimgs = `/images/projects/software/`;

var frontendProjects = [
    {
        title:'Moviesta',
        description:'🎞️ The king of Movies',
        imgurl:`${webimgs}moviesta.png`,
        sourcecodeurl:'https://github.com/zeyadetman/Moviesta',
        site:'https://zeyadetman.github.io/Moviesta/'
    },
    {
        title:'Which movie should watch?',
        description:'🎥 Compare between two movies to choose your next movie',
        imgurl:`${webimgs}wmsw.png`,
        sourcecodeurl:'https://github.com/zeyadetman/which-movie-should-watch',
        site:'https://zeyadetman.github.io/which-movie-should-watch/'
    },
    {
        title:'The Chaos Game',
        description:'A method of creating a fractal, using a polygon and an initial point selected at random inside it.',
        imgurl:`${webimgs}chaos.png`,
        sourcecodeurl:'https://github.com/zeyadetman/chaos',
        site:'https://zeyadetman.github.io/chaos/'
    },
    {
        title:'Clock',
        description:'simple clock',
        imgurl:`${webimgs}clock.png`,
        sourcecodeurl:'https://github.com/zeyadetman/Clock',
        site:'https://zeyadetman.github.io/Clock/'
    },
    {
        title:'Calculator',
        description:'Calculator.',
        imgurl:`${webimgs}calculator.png`,
        sourcecodeurl:'https://github.com/zeyadetman/Calculator',
        site:'https://zeyadetman.github.io/Calculator/'
    },
    {
        title:'Eclipse',
        description:'Eclipse',
        imgurl:`${webimgs}eclipse.png`,
        sourcecodeurl:'https://github.com/zeyadetman/Eclipse',
        site:'https://zeyadetman.github.io/Eclipse/'
    },
    {
        title:'KeyNumbers',
        description:'The ASCII of Keyboard buttons',
        imgurl:`${webimgs}keys.png`,
        sourcecodeurl:'https://github.com/zeyadetman/KeyNumbers',
        site:'https://zeyadetman.github.io/KeyNumbers/'
    },
    {
        title:'Piano',
        description:'Simple piano',
        imgurl:`${webimgs}piano.png`,
        sourcecodeurl:'https://github.com/zeyadetman/Piano',
        site:'https://zeyadetman.github.io/Piano/'
    },
    {
        title:'TICTACTOE',
        description:'TICTACTOE',
        imgurl:`${webimgs}tictactoe.png`,
        sourcecodeurl:'https://github.com/zeyadetman/TICTACTOE',
        site:'https://zeyadetman.github.io/TICTACTOE/'
    },
    {
        title:'pixelartmaker',
        description:'Pixel Art Maker',
        imgurl:`${webimgs}pixelartmaker.png`,
        sourcecodeurl:'https://github.com/zeyadetman/pixelartmaker',
        site:'https://zeyadetman.github.io/pixelartmaker/'
    },
    {
        title:'Wikipedia',
        description:'Fast Browsing for Wikipedia.',
        imgurl:`${webimgs}wikipedia.png`,
        sourcecodeurl:'https://github.com/zeyadetman/Wikipedia',
        site:'https://zeyadetman.github.io/Wikipedia/'
    },
    {
        title:'Pomodoro',
        description:'Pomodoro Clock Advanced Front End Development Projects freecodecamp',
        imgurl:`${webimgs}pomodoro.png`,
        sourcecodeurl:'https://github.com/zeyadetman/PomodoroClock',
        site:'https://zeyadetman.github.io/PomodoroClock/'
    },
    {
        title:'TerminalPortfolio',
        description:'ZeeTerminal (Personal Site)',
        imgurl:`${webimgs}terminal.png`,
        sourcecodeurl:'https://github.com/zeyadetman/TerminalPortfolio',
        site:'https://zeyadetman.github.io/TerminalPortfolio/'
    },
    {
        title:'WeatherApp',
        description:'Want to find the weather right now? try this ',
        imgurl:`${webimgs}weather.png`,
        sourcecodeurl:'https://github.com/zeyadetman/WeatherApp',
        site:'https://zeyadetman.github.io/WeatherApp/'
    },
    {
        title:'counteributors.github.io',
        description:`Want to create a big project? Here You'll find contributors.`,
        imgurl:`${webimgs}counteributors.png`,
        sourcecodeurl:'https://github.com/counteributors/counteributors.github.io',
        site:'https://counteributors.github.io'
    },
    {
        title:'MoviesQuotes',
        description:`Want to read movies quotes? here you'll find what you want!`,
        imgurl:`${webimgs}quote.png`,
        sourcecodeurl:'https://github.com/zeyadetman/MoviesQuotes',
        site:'https://zeyadetman.github.io/MoviesQuotes/'
    },
    {
        title:'Logo-Game',
        description:`guess this logo.`,
        imgurl:`${webimgs}logogame.png`,
        sourcecodeurl:'https://github.com/zeyadetman/Logo-Game',
        site:'https://zeyadetman.github.io/Logo-Game/'
    }

]

var softwareProjects = [
    {
        title:'Targmly',
        lang:'python',
        description:"Translate to arabic wherever you're. just copy the word!",
        imgurl:`${softwareimgs}screenshot1.jpg`,
        sourcecodeurl:'https://github.com/zeyadetman/Targmly',
        site:'https://github.com/zeyadetman/Targmly'
    },
    {
        title:'TinyLanguageCompiler',
        lang:'csharp',
        description:"Compiler for Tiny programming language",
        imgurl:`${softwareimgs}tiny.jpg`,
        sourcecodeurl:'https://github.com/zeyadetman/TinyLanguageCompiler',
        site:'https://github.com/zeyadetman/TinyLanguageCompiler'
    },
    {
        title:'DownloadInstagramAccountPhotos',
        lang:'python',
        description:"Download all the photos of Public Instagram Account",
        imgurl:`${softwareimgs}insta.jpg`,
        sourcecodeurl:'https://github.com/zeyadetman/DownloadInstagramAccountPhotos',
        site:'https://github.com/zeyadetman/DownloadInstagramAccountPhotos'
    },
    {
        title:'Image-TextSteganography',
        lang:'csharp',
        description:"An image steganography by converting the image into text of pixels and use the LSB to hide the ciphered text that encrypted by The Caesar cipher Algorithm (Cryptography). The project decrypt the image by loading it, converting the pixels’ digits and break the LSB.",
        imgurl:`${softwareimgs}steg.jpg`,
        sourcecodeurl:'https://github.com/zeyadetman/Image-TextSteganography',
        site:'https://github.com/zeyadetman/Image-TextSteganography'
    },
    {
        title:'RemoveDuplicateFiles',
        lang:'python',
        description:"Remove Duplicated files",
        imgurl:`${softwareimgs}screenshot1.jpg`,
        sourcecodeurl:'https://github.com/zeyadetman/RemoveDuplicateFiles',
        site:'https://github.com/zeyadetman/RemoveDuplicateFiles'
    }

]

document.addEventListener("DOMContentLoaded", ()=>{
    frontendProjects.forEach((project)=>{
        document.getElementById('frontendCards').innerHTML +=
        `<div class="card">
            <div class="imgcont">        
                <img src="${project.imgurl}" class="card-img img-fluid">
            </div>
                <h6 class="card-title">${project.title}</h6>
                <p class="card-desc">${project.description}</p>
                <ul class="card-links">
                    <li class="card-link card-source-code"><a href="${project.sourcecodeurl}">Code</a></li>
                    <li class="card-link card-site"><a href="${project.site}">Site</a></li>
                </ul>
        </div>`});

    softwareProjects.forEach((project)=>{
        document.getElementById('softwaredevCards').innerHTML += 
        `<div class="card">
            <div class="imgcont">        
                <img src="${project.imgurl}" class="card-img img-fluid">
            </div>
                <h6 class="card-title">${project.title}</h6>
                <p class="card-desc">${project.description}</p>
                <ul class="card-links">
                    <li class="card-link card-source-code"><a href="${project.sourcecodeurl}">Code</a></li>
                </ul>
        </div>`});
});

</script>