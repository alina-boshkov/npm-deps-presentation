# npm-deps-presentation
README.md
Here is a ready-to-use README.md file for your presentation. You can copy and paste this content directly into a file named README.md in your GitHub repository.

Advanced Dependency Management: An Interactive Guide
This is an interactive presentation designed to educate frontend development teams on advanced dependency management concepts and best practices. It covers the inner workings of npm, historical incidents that highlight ecosystem fragility, and actionable steps to build more resilient projects.

How to View the Presentation
This is a single-page web application (index.html). You can view it in two ways:

Online: [https://alina-boshkov.github.io/npm-deps-presentation/]

Locally: Simply download or clone this repository and open the index.html file in your web browser.

Key Topics
The Mechanics of npm install: A deep dive into how npm resolves and manages dependencies.

Historical Incidents: Case studies on major events like the left-pad, event-stream, and stylus incidents.

Best Practices: Actionable advice for securing our dependency ecosystem.

Interactive Features
This presentation includes speaker notes on each slide to assist with delivery. Click the "Show Speaker Notes" button on any slide to reveal detailed talking points.

Technology Stack
HTML: For the page structure.

Tailwind CSS: For styling and a fully responsive layout.

JavaScript: For all interactive functionality, including slide navigation and the speaker notes toggle.

More notes: 
Incident stories: 
The left-pad Incident (2016)
In 2016, a developer unpublished a small, 11-line utility package from the npm registry as a form of protest. This simple package was a transitive dependency for thousands of projects, including major frameworks, causing builds around the world to fail. The incident highlighted the fragility of a software supply chain built on many small, interconnected packages and demonstrated how a single point of failure can have a global impact.

The event-stream Attack (2018)
A malicious actor used a social engineering attack to gain control of a popular, but unmaintained, package. They then added a backdoor to a sub-dependency, which was specifically designed to target and steal cryptocurrency from the Copay Bitcoin wallet. This sophisticated supply chain attack went undetected for months and showed that even trusted packages can be compromised, emphasizing the need for developers to be vigilant about their dependencies.

The stylus Incident (2025)
The stylus CSS preprocessor package was removed from the npm registry by the security team. This was not because the package itself contained malicious code, but because a contributor was linked to other malicious packages. The removal broke builds for major frameworks that relied on it, revealing a new layer of supply chain risk where a package's stability can be tied to the reputation and actions of its maintainers, regardless of its own code integrity.

Best practives: 

Run npm audit: This is a crucial first step for routinely checking your dependencies for known security vulnerabilities.

Lockfiles are Non-Negotiable: Committing package-lock.json ensures that every developer and every deployment uses the exact same versions of all packages, preventing inconsistencies and surprise bugs.

Perform Dependency Audits: This goes beyond npm audit to suggest using tools to check for outdated or unmaintained packages, helping you proactively manage your dependency health.

Mind Your Binaries: The presentation highlights the risk of postinstall scripts, which can run arbitrary code on your machine. This practice reminds the team to be aware of what packages might be executing during installation.

Credits
Created by Alina Boshkov for Lemonade.