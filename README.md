# Personal Portfolio

A personal portfolio website built with Spring Boot and Thymeleaf, containerized with Docker and deployed through a CI/CD pipeline.

**Live site:** https://kim-portfolio.onrender.com

## About

A simple, fast portfolio that introduces who I am, the projects I've built, and my background — designed to be easy for recruiters to evaluate quickly. Server-side rendered with Thymeleaf and served by a Spring Boot backend.

## Tech Stack

- **Backend:** Java 21, Spring Boot
- **Templating:** Thymeleaf
- **Styling:** Plain CSS (custom design tokens)
- **Build:** Maven
- **Containerization:** Docker (multi-stage build)
- **Deployment:** Render (auto-deploy on push)

## Project Structure

```
.
├── src/main/java/com/eunbi/portfolio/
│   ├── PortfolioApplication.java     # Spring Boot entry point
│   └── HomeController.java           # Serves the home page
├── src/main/resources/
│   ├── templates/
│   │   └── index.html                # Page (Thymeleaf)
│   └── static/
│       ├── css/style.css             # Styles
│       └── resume.pdf                # Downloadable résumé
├── Dockerfile                        # Multi-stage build for deployment
└── pom.xml                           # Dependencies
```

## Running Locally

Requires Java 21.

```bash
git clone https://github.com/kimberly-smart/kim-portfolio.git
cd kim-portfolio
./mvnw spring-boot:run
```

Then open http://localhost:8080

## Running with Docker

```bash
docker build -t portfolio .
docker run -p 8080:8080 portfolio
```

## Deployment

Hosted on Render as a Docker web service. Pushing to the `main` branch automatically triggers a rebuild and redeploy.

## Contact

- **Email:** kimeunb1822@gmail.com
- **LinkedIn:** https://linkedin.com/in/kimeunb
- **GitHub:** https://github.com/kimberly-smart
