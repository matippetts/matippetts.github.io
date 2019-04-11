---
title: Learning Goals
author: Mark Tippetts
published: true
---
Methodologies:
{% for methodology in site.methodologies %}
- {{ methodology.name }}
{% endfor %}
- BDD
- UI automation
  - headless browser
  - GUI testing
- Page scraping
- Release cycle
- Configuration-as-code

Architectures:
{% for architecture in site.architectures %}
- {{ architecture.name }}
{% endfor %}
- JAMstack
- Headless CMS
  - Git-based
  - API-based
- REST API
- CQRS (with GraphQL)
- PWA (Progressive Web App)
- SPA
- MVC routing

Languages:
{% for language in site.languages %}
- {{ language.name }}
{% endfor %}
- Java 8
- Java 11
- Groovy
- JavaScript

Libraries:
{% for library in site.libraries %}
- {{ library.name }}
{% endfor %}
- JavaFX
- TestFX & FXtest
- GMF
- Spock
- Geb

Platforms:
{% for platform in site.platforms %}
- {{ platform.name }}
{% endfor %}
- Electron
- Servlet engine
  - Tomcat
  - Jetty
- Eclipse 3 RCP
- Eclipse 4 RCP
- Freeplane (addons & plugins)

Tools:
{% for tool in site.tools %}
- {{ tool.name }}
{% endfor %}
- Eclipse
- Atom
  - VS Code
- Git
- Gradle
- Maven
- NPM

Protocols:
{% for protocol in site.protocols %}
- {{ protocol.name }}
{% endfor %}
- DNS
- SMTP
- HTTP 1.1
- HTTP/2
- POP3
- IMAP
- WebDAV
- SSH
