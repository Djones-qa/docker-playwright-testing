# Docker Playwright Testing

![CI](https://github.com/Djones-qa/docker-playwright-testing/actions/workflows/docker-tests.yml/badge.svg)

Playwright E2E tests running inside Docker containers with GitHub Actions CI.

## Architecture
`
GitHub Push
    ↓
GitHub Actions triggers
    ↓
Docker image built
    ↓
Playwright tests run inside container
    ↓
Results exported from container
    ↓
Report uploaded as artifact
`

## Tech Stack
- Playwright
- TypeScript
- Docker
- Docker Compose
- GitHub Actions CI

## Files
- Dockerfile — Container definition
- docker-compose.yml — Multi-container setup
- tests/ — Playwright test specs
- .github/workflows/ — CI pipeline

## Run Locally (requires Docker)
`ash
docker build -t playwright-tests .
docker run --rm playwright-tests
`

## Run in CI
Tests run automatically on every push via GitHub Actions.

## Test Coverage
- Login page loads correctly
- Valid credentials login successfully
- Invalid username shows error
- Invalid password shows error
- Logout works correctly

## Author
Darrius Jones - github.com/Djones-qa