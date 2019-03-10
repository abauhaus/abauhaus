
<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8' />
    <title></title>
    <meta name='viewport' content='initial-scale=1,maximum-scale=1,user-scalable=no' />
    <script src='https://api.tiles.mapbox.com/mapbox-gl-js/v0.44.1/mapbox-gl.js'></script>
    <link href='https://api.tiles.mapbox.com/mapbox-gl-js/v0.44.1/mapbox-gl.css' rel='stylesheet' />
    <style>
        body { margin:0; padding:0; }
        #map { position:absolute; top:0; bottom:0; width:100%; }
    </style>
</head>
<body>

<style>
#map {
    position: fixed;
    width:50%;
}
#features {
    width: 50%;
    margin-left: 50%;
    font-family: Tw Cen MT;
    overflow-y: scroll;
    background-color: #fafafa;
}
section {
    padding:  25px 50px;
    line-height: 25px;
    border-bottom: 1px solid #ddd;
    opacity: 0.25;
    font-size: 20px;
}
section.active {
    opacity: 1;
}
section:last-child {
    border-bottom: none;
    margin-bottom: 1000px;
}
</style>

<div id='map'></div>
<div id='features'>
    <section id='welcome' class='active'>
        <h3> Analisa Bauhaus: Resumap</h3>
        <p>Welcome to my resumap! In addition to my standard resume, I created this resume-map to give you a better idea of who I am and where I come from. <br><br> Scroll through to see how I got to where I am today. <br><br></p>
    </section>
    <section id='section1' class='active'>
        <h3>The Beginning</h3>
        <p> I was born and raised in San Carlos, California by an educator and a tech company executive. I was brought up with values of inclusion, academic excellence and doing good for people and the planet.
    </section>
    <section id='section2'>
        <h3>High School: 2010 - 2014</h3>
        <p> From 2010 to 2014 I attended Sequoia High School in Redwood City, California where I swam for both a club swim team and the high school team, as well as played water polo for the school. I was a member of the California Scholarship Federation and an All-American Athlete for both swimming and water polo.</p>
    </section>
    <section id='section3'>
        <h3>College: 2014 - 2018</h3>
        <p>In August of 2014 I moved across 3,000 miles from home to Carlisle, PA to continue my education at Dickinson College, my first choice school! In my second semester at Dickinson I was invited to join Kappa Alpha Theta, a Women’s Fraternity with values of intellectual curiosity, leadership potential, commitment to service, and personal excellence. During my sophomore year, I joined and then was made co-president of the Red Devil Swim Club, Dickinson’s club swim team. I also served as the club’s Sports Club Council Representative. <br><br>
    </section>
    <section id='section4'>
        <h3>Summer Abroad: 2016</h3>
        <p>  I spent the first part of the summer before junior year in Málaga, Spain as part of Dickinson’s Summer Study Abroad in Spain program where I practiced Spanish daily and developed a deep love for Málaga and Spanish culture. 
    </section>
    <section id='section5'>
        <h3>Summer: 2016</h3>
        <p>After returning home to California from Málaga, I interned for Environmental Entrepreneurs (E2) in San Francisco. At E2 I helped in advocating for California environmental policy through data input, policy briefs and meeting with California state senators in support of CA Senate Bill 32, which expands on the 2006 Assembly Bill 32 to reduce greenhouse gas emissions. In September, 2016 the bill passed!</p>
    </section>
    <section id='section6'>
        <h3>Semester Abroad: 2017</h3>
        <p>6. Malaga Spain — In Spring 2017, I was able to return to Málaga for a semester abroad. I spent 5 months living with a Spanish host family and attending classes at the Universidad de Málaga. By the end of my stay in Spain, my Spanish fluency had improved immensely along with my understanding of Spanish culture.</p>
    </section>
    <section id='section7'>
        <h3>Summer: 2017</h3>
        <p>In the summer before my senior year at Dickinson, I was able to have two different internships. The first was with the Pennsylvania Behavioral Health and Aging Coalition (PBHAC) where I was a Communications Intern. At PBHAC I managed their social media presence, event marketing and coordination and attended trainings to develop better healthcare for older Pennsylvanians.</p>
    </section>
    <section id='section8'>
        <h3>Summer: 2017</h3>
        <p>The second internship I had in the summer of 2017 was with Court Appointed Special Advocates (CASA) located in the courthouse in Carlisle. There, I managed various case files and attended court hearing where CASA and Children and Youth Services were involved while also learning first-hand the challenges children in our communities face every day.</p>
    </section>
    <section id='section9'>
        <h3>Graduation: 2018</h3>
        <p>In May 2018, I graduated from Dickinson College in Carlisle, PA with a Bachelor of the Arts degree in Sociology and Spanish Language and Literature!</p>
    </section>
    <section id='section10'>
        <h3>Today</h3>
        <p>I am currently doing a year of national service through the AmeriCorps VISTA program. AmeriCorps VISTA is a national poverty alleviation program that sends volunteers into professional settings to work on projects targeting issues of poverty. I am serving as a Marketing and Communications Associate at the Community Action Association of Pennsylvania working on a set of marketing resources designed to help the public and Pennsylvania's Community Action Agencies talk about issues of poverty in a concise, compelling way.</p>
    </section>
</div>
<script>
mapboxgl.accessToken = 'pk.eyJ1IjoiYWJhdWhhdXMiLCJhIjoiY2p0MXJyd3R5MDhveTN5b3ZyZmFzdWszeiJ9.NLffD7i0q01lyzedbhEATg';
var map = new mapboxgl.Map({
    container: 'map',
    style: 'mapbox://styles/mapbox/outdoors-v10',
        bearing: -0,
        center: [-108.866174, 49.272291],
        zoom: 2,
        speed: 0.8,
        pitch: 0
});
var chapters = {
    'welcome': {
        bearing: -0,
        center: [-108.866174, 49.272291],
        zoom: 2,
        speed: 0.8,
        pitch: 0
    },
    'section1': {
        bearing: 0,
        center: [-122.261800, 37.504900],
        zoom: 13.00,
        pitch: 0
    },
    'section2': {
        center: [-122.236630, 37.484400],
        bearing: 0,
        zoom: 16,
        speed: 0.6,
        pitch: 0
    },
    'section3': {
        bearing: 0,
        center: [-77.196480, 40.202644],
        zoom: 16,
        speed: 0.6,
        pitch: 0.00
    },
    'section4': {
        bearing: 0,
        center: [-4.412525, 36.720476],
        zoom: 10,
        speed: 0.6,
        pitch: 0
    },
    'section5': {
        bearing: 0,
        center: [-122.402524, 37.789760],
        zoom: 16,
        pitch: 0,
        speed: 0.6
    },
    'section6': {
        bearing: 0,
        center: [-4.417654, 36.727547],
        zoom: 16,
        pitch: 0,
        speed: 0.6
    },
    'section7': {
        bearing: 0,
        center: [-76.856344, 40.316054],
        zoom: 16,
        speed: 0.6,
        pitch: 0
    },
    'section8': {
        bearing: 0,
        center: [-77.189775, 40.201830],
        zoom: 16,
        speed: 0.6,
        pitch: 0
     },
    'section9': {
        bearing: 0,
        center: [-77.196480, 40.202644],
        zoom: 16,
        speed: 0.6,
        pitch: 0
    },
    'section10': {
        bearing: 0,
        center: [-76.839820, 40.236482],
        zoom: 16,
        speed: 0.6,
        pitch: 0 
};
// On every scroll event, check which element is on screen
window.onscroll = function() {
    var chapterNames = Object.keys(chapters);
    for (var i = 0; i < chapterNames.length; i++) {
        var chapterName = chapterNames[i];
        if (isElementOnScreen(chapterName)) {
            setActiveChapter(chapterName);
            break;
        }
    }
};
var activeChapterName = 'baker';
function setActiveChapter(chapterName) {
    if (chapterName === activeChapterName) return;
    map.flyTo(chapters[chapterName]);
    document.getElementById(chapterName).setAttribute('class', 'active');
    document.getElementById(activeChapterName).setAttribute('class', '');
    activeChapterName = chapterName;
}
function isElementOnScreen(id) {
    var element = document.getElementById(id);
    var bounds = element.getBoundingClientRect();
    return bounds.top < window.innerHeight && bounds.bottom > 0;
}
</script>
</body>
</html>
