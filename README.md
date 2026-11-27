# Appointments API (InnoAppointmentsApi)

Appointments API is a backend service for clinic appointments. The solution follows the same layout as the other platform APIs. Domain endpoints are not implemented yet.

The executable project is `AppointmentsApi/AppointmentsApi.Api`. Target framework: **.NET 10**.

---

## Prerequisites

Before building and running this project locally, ensure you have the following installed:

* [.NET SDK](https://dotnet.microsoft.com/download) (version 10.0 or later)
* [Git](https://git-scm.com/downloads)
* An IDE such as [Visual Studio 2022](https://visualstudio.microsoft.com/), [Visual Studio Code](https://code.visualstudio.com/), or [JetBrains Rider](https://www.jetbrains.com/rider/)

---

## Local Setup & Run

1. **Clone the repository**
```bash
git clone https://github.com/EvgeniyaInternship/InnoAppointmentsApi.git
cd InnoAppointmentsApi/AppointmentsApi

```


2. **Restore dependencies**
```bash
dotnet restore

```


3. **Build the project**
```bash
dotnet build

```


4. **Run the API**
Run the API project directly using the `.NET CLI`:
```bash
dotnet run --project AppointmentsApi.Api --launch-profile http

```


5. **Verify the service**
Once started, the service will be accessible locally at:
```text
https://localhost:7096
http://localhost:5096

```

The `https` profile also listens on `https://localhost:7096`.
