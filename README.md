# EX01 Developing a Simple Webserver
## Date:27-03-2024

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
</head>
<body>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container-fluid">
          <a class="navbar-brand" href="#">Home</a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#">Ahout</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">Queries</a>
              </li>
              <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                  Dropdown
                </a>
                <ul class="dropdown-menu">
                  <li><a class="dropdown-item" href="#">Action</a></li>
                  <li><a class="dropdown-item" href="#">Another action</a></li>
                  <li><hr class="dropdown-divider"></li>
                  <li><a class="dropdown-item" href="#">Something else here</a></li>
                </ul>
              </li>
              <li class="nav-item">
                <a class="nav-link disabled" aria-disabled="true">Contact</a>
              </li>
            </ul>
            <form class="d-flex" role="search">
              <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
              <button class="btn btn-outline-success" type="submit">Search</button>
            </form>
          </div>
        </div>
      </nav>

    <div id="carouselExampleIndicators" class="carousel slide">
        <div class="carousel-indicators">
          <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
          <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
          <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="maxresdefault.jpg" class="d-block w-100" alt="...">
  
          </div>
          <div class="carousel-item">
            <img src="Present-time-is-the-opportunity-for-India-to-start-undoing-its-Tibet-mistake.jpg" class="d-block w-100" alt="...">
          </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div><br>
    <div class="card-group">
        <div class="card">
          <img src="bribery1.avif" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">Bribery in Parliament</h5>
            <p class="card-text">The 1998 judgment came on a plea by former Prime Minister PV Narasimha Rao, who was among the Congress leaders accused of bribing certain MPs to vote against a no-confidence motion moved against Rao's government in 1993.</p>
            <p class="card-text"><small class="text-body-secondary">Last updated 3 mins ago</small></p>
            <a href="https://www.barandbench.com/news/bribery-parliament-what1998-supreme-court-judgment-pv-narasimha-rao-case-say"class="btn btn-success">Go somewhere</a>
          </div>
        </div>
        <div class="card">
          <img src="sbi.webp" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">ADR says it will oppose SBI plea on electoral bonds</h5>
            <p class="card-text">The Supreme Court on February 15 annulled the electoral bonds scheme for political funding. File. As the State Bank of India moved the Supreme Court seeking time till June 30 to comply with a direction to make public details of electoral bonds purchased since April 2019, the Association for Democratic Reforms (ADR), chief petitioner in the electoral bonds case, said it was considering all legal options, including opposing the SBI plea in court.</p>
            <p class="card-text"><small class="text-body-secondary">Last updated 3 mins ago</small></p>
            <a href="https://www.thehindu.com/news/national/sbi-moves-supreme-court-seeking-extension-of-time-to-disclose-details-of-electoral-bonds/article67914093.ece"class="btn btn-primary">Go somewhere</a>
          </div>
        </div>
        <div class="card">
          <img src="Official_Photograph_of_Prime_Minister_Narendra_Modi_Portrait.png" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">PM Modi visit LIVE Updates</h5>
            <p class="card-text">PM Modi visit LIVE Updates: Prime Minister Narendra Modi on Tuesday will be in Telangana and Odisha to inaugurate and lay foundation stone of a slew of development projects worth over ₹26,400 crore. Today, he will inaugurate and lay the foundation for development projects worth more than ₹6,800 crore, related to multiple key sectors such as road, rail, petroleum and natural gas, followed by a public address in Telangana's Sangareddy.</p>
            <p class="card-text"><small class="text-body-secondary">Last updated 3 mins ago</small></p>
            <a href="https://www.hindustantimes.com/india-news/pm-narendra-modi-visit-live-updates-march-5-telangana-odisha-sangareddy-chandikhole-rs-26-400-crore-worth-projects-101709598756459.html" class="btn btn-primary">Go somewhere</a>
          </div>
        </div>
      </div>
      <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
    
</body>
</html>
```

## OUTPUT:
![alt text](output.png)
![alt text](output2.png)

## RESULT:
The program for implementing simple webserver is executed successfully.
