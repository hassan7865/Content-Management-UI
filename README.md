# Content-Management-UI

Angular UI for a courier / shipment content-management system. Works with [Content-Management-API](https://github.com/hassan7865/Content-Management-API).

## Overview

Role-based Angular app with three areas:

- **Public** — home, about, services, login
- **Admin** — dashboard, users/couriers, customers
- **Customer** — dashboard and shipment upload

Uses route guards per area and talks to the ASP.NET Core CMS API.

## Stack

- Angular 16 (NgModules)
- Angular Material / CDK, PrimeNG
- DataTables (`angular-datatables`)
- SheetJS (`xlsx`) for spreadsheet import/export
- TypeScript, RxJS

## Structure

```
src/app/
  public/       # Marketing + login
  Admin/        # Admin layout and feature modules
  Customers/    # Customer layout, upload flows
  Services/     # HTTP / domain services
  Guard/        # admin / customer / public guards
src/environment.ts
```

## Getting started

```bash
npm install
npm start
# or: ng serve
```

Build:

```bash
npm run build
```

Set `BASEURL` in `src/environment.ts` to your CMS API (default: `http://localhost:7040/api`).

## Notes

- Admin and customer routes require a valid session from the API.
- Keep API keys and production URLs out of committed config when possible.
