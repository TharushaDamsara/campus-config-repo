# campus-config-repo

Centralized, Git-backed configuration source for the CampusFlow [campus-config-server](https://github.com/TharushaDamsara/campus-config-server).
Each file corresponds to a `spring.application.name` served by the Config Server; `application.yml`
holds configuration shared by all services.

**Student:** Tharusha Damsara (241711004)
**GCP Project ID:** campusflow-eca-2026

## Technology Stack

- YAML (Spring Cloud Config format)

## Setup / Getting Started

No build steps — this repo is cloned directly by the Config Server. Point the Config Server at it via:

```yaml
spring:
  cloud:
    config:
      server:
        git:
          uri: https://github.com/TharushaDamsara/campus-config-repo
          default-label: main
```

Sensitive values (DB passwords, JWT secrets) are supplied via environment variables at runtime and
are **not** stored in this repo; the values shown here are local-development fallbacks only.
# campus-config-server
# campus-config-server
# campus-config-server
