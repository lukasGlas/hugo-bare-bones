

## Installation

    npm install cypress --save-dev


npx cypress open

https://docs.cypress.io/guides/getting-started/opening-the-app


name: Cypress Tests

on: push

jobs:
  cypress-run:
    runs-on: ubuntu-22.04
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      # Install npm dependencies, cache them correctly
      # and run all Cypress tests
      - name: Cypress run
        uses: cypress-io/github-action@v6
        with:
          build: npm run build
          start: npm start

