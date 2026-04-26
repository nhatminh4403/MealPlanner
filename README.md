# 🍽️ Meal Planner Application (Fullstack)

*English below*

## 🇻🇳 Giới thiệu (Tiếng Việt)

Đây là hệ thống **Meal Planner** fullstack bao gồm:

* 🔧 Backend API: xây dựng bằng **ABP Framework**
* 🌐 Frontend: xây dựng bằng **Next.js**

### 🔗 GitHub Repositories

* Backend API: [https://github.com/nhatminh4403/MealPlannerAPI.BE](https://github.com/nhatminh4403/MealPlannerAPI.BE)
* Frontend: [https://github.com/nhatminh4403/MealPlanner.FE](https://github.com/nhatminh4403/MealPlanner.FE)

---

## 🏗️ Kiến trúc hệ thống

### Backend (MealPlannerAPI)

Dự án sử dụng kiến trúc **Layered Monolith (ABP Framework v10)**.

### 📂 Backend Projects (Chi tiết)

#### Core Layers

* `MealPlannerAPI.Domain` → Business logic, entities, domain services
* `MealPlannerAPI.Domain.Shared` → Constants, enums, shared models

#### Application Layers

* `MealPlannerAPI.Application` → Use cases, application services
* `MealPlannerAPI.Application.Contracts` → Interfaces/contracts

#### Infrastructure Layers

* `MealPlannerAPI.EntityFrameworkCore` → DbContext, repository

#### API Layer

* `MealPlannerAPI.HttpApi` → Controllers
* `MealPlannerAPI.HttpApi.Client` → API client proxy
* `MealPlannerAPI.HttpApi.Host` → Main host application

#### Tools

* `MealPlannerAPI.DbMigrator` → Migration & seed data

#### Test Projects

* `MealPlannerAPI.Application.Tests`
* `MealPlannerAPI.Domain.Tests`
* `MealPlannerAPI.EntityFrameworkCore.Tests`

---

### Frontend (MealPlanner.FE)

* Sử dụng **Next.js (App Router)**
* Tối ưu font với `next/font`
* Chạy tại: [http://localhost:3000](http://localhost:3000)

---

## ⚙️ Yêu cầu môi trường

### Backend:

* .NET 10.0+ SDK
* Node.js v18 hoặc v20

### Frontend:

* Node.js (v18+)

---

## 🚀 Hướng dẫn chạy dự án

### 1. Clone source code

```bash
git clone https://github.com/nhatminh4403/MealPlannerAPI.BE
git clone https://github.com/nhatminh4403/MealPlanner.FE
```

### 2. Setup Backend

```bash
cd MealPlannerAPI.BE
abp install-libs
```

```bash
dotnet run --project src/MealPlannerAPI.DbMigrator
```

```bash
dotnet run --project src/MealPlannerAPI.HttpApi.Host
```

### 3. Setup Frontend

```bash
cd MealPlanner.FE
npm install
npm run dev
```

---

## 🔐 Production

```bash
dotnet dev-certs https -v -ep openiddict.pfx -p your-password
```

---

# 🍽️ Meal Planner Application (Fullstack)

## 🇺🇸 Overview (English)

This is a **fullstack Meal Planner system** consisting of:

* 🔧 Backend API: built with **ABP Framework**
* 🌐 Frontend: built with **Next.js**

### 🔗 GitHub Repositories

* Backend API: [https://github.com/nhatminh4403/MealPlannerAPI.BE](https://github.com/nhatminh4403/MealPlannerAPI.BE)
* Frontend: [https://github.com/nhatminh4403/MealPlanner.FE](https://github.com/nhatminh4403/MealPlanner.FE)

---

## 🏗️ Architecture

### Backend (MealPlannerAPI)

Uses **ABP Framework v10 layered architecture**.

### 📂 Backend Projects (Detailed)

#### Core Layers

* `MealPlannerAPI.Domain` → Core business logic
* `MealPlannerAPI.Domain.Shared` → Shared resources

#### Application Layers

* `MealPlannerAPI.Application` → Application services
* `MealPlannerAPI.Application.Contracts` → Interfaces

#### Infrastructure Layers

* `MealPlannerAPI.EntityFrameworkCore` → EF Core config
* `MealPlannerAPI.EntityFrameworkCore.DbMigrations` → Migrations

#### API Layer

* `MealPlannerAPI.HttpApi` → Controllers
* `MealPlannerAPI.HttpApi.Client` → Client proxies
* `MealPlannerAPI.HttpApi.Host` → Main host

#### Tools

* `MealPlannerAPI.DbMigrator` → Migration tool

#### Test Projects

* `Application.Tests`
* `Domain.Tests`
* `EntityFrameworkCore.Tests`

---

### Frontend (MealPlanner.FE)

* Built with Next.js
* Runs at [http://localhost:3000](http://localhost:3000)

---

## 🚀 Getting Started

```bash
git clone https://github.com/nhatminh4403/MealPlannerAPI.BE
git clone https://github.com/nhatminh4403/MealPlanner.FE
```

---

## 📦 Deployment

* Backend: ASP.NET Core deployment (preferably **Microsoft Azure** or **AWS** if you have knowledge of deploying to)
* Frontend: Vercel recommended
