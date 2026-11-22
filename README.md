# Employee Dashboard API

A 10,000-record local REST API designed for a React/TanStack virtualization assignment.

## Run

```bash
npm install
npm start
```

API base URL:

`http://localhost:3001`

Main endpoint:

`GET http://localhost:3001/employees`

## Useful json-server queries

Pagination:
`/employees?_page=1&_per_page=50`

Sort:
`/employees?_sort=name`
`/employees?_sort=-salary`

Filter:
`/employees?department=Engineering`
`/employees?status=Active`

Multiple filters:
`/employees?department=Engineering&status=Active`

Search-like filtering can be implemented in the React app after fetching a page, or you can extend the API layer with your own query strategy.

## Assignment goal

Build a production-style Employee Operations Dashboard that can comfortably render thousands of rows without DOM performance problems.

Recommended stack:
- React + TypeScript
- TanStack Query
- TanStack Table
- TanStack Virtual OR react-window
- CSS/Tailwind of your choice

Do not simply render all 10,000 rows into the DOM. The main challenge is virtualization.
