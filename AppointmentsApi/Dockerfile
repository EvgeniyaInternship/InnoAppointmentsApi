FROM mcr.microsoft.com/dotnet/sdk:10.0 AS build
WORKDIR /src
COPY AppointmentsApi.Domain/AppointmentsApi.Domain.csproj AppointmentsApi.Domain/
COPY AppointmentsApi.Application/AppointmentsApi.Application.csproj AppointmentsApi.Application/
COPY AppointmentsApi.Infrastructure/AppointmentsApi.Infrastructure.csproj AppointmentsApi.Infrastructure/
COPY AppointmentsApi.Api/AppointmentsApi.Api.csproj AppointmentsApi.Api/
RUN dotnet restore AppointmentsApi.Api/AppointmentsApi.Api.csproj
COPY . .
RUN dotnet publish AppointmentsApi.Api/AppointmentsApi.Api.csproj -c Release -o /app/publish /p:UseAppHost=false

FROM mcr.microsoft.com/dotnet/aspnet:10.0 AS runtime
WORKDIR /app
COPY --from=build /app/publish .
ENV ASPNETCORE_URLS=http://+:5096
EXPOSE 5096
ENTRYPOINT ["dotnet", "AppointmentsApi.Api.dll"]
