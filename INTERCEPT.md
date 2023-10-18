# Cypress guide

### Mock with fixed response:
```
cy.intercept(
    'POST',
    '/some/route', 
    `
    {"mockKey": "mockValue"}
    `
);
```

### Simulate network error for a particular request

```
req.destroy() - destroy the request and respond with a network error
```

```
cy.intercept(
    'POST',
    '/some/route', 
    (req) => {
        req.destroy();
    }
);
```

Reference: 
https://docs.cypress.io/api/commands/intercept
