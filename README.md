# Qtill

Helping students and educators.

## Architecture

The frontend is React / TBD, responsible for the user interface.
The backend uses FastAPI with postgress, to expose a Rest API for various resources (like courses, candidates, and applications).
User authentication will be handled with OIDC.

### Diagram

```mermaid
graph TD;
    A[Frontend - React / TBD] -->|HTTP Request| B[FastAPI];

    subgraph FastAPI [Backend]
        B1[Rest API Endpoints - Courses, Universities, Applications];
        B2[Database Layer - PostgreSQL];
        B3[Authentication - OIDC & OAuth2 ];

        B --> B1;
        B1 --> B2;
        B1 --> B3;
    end
```
