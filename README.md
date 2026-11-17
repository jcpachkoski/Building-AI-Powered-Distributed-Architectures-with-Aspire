## .NET Aspire and GenAI Develop Distributed Architectures 2025
https://www.udemy.com/course/net-aspire-and-genai-develop-distributed-architectures/?couponCode=LAUNCH_ASPIRE

Develop AI-Powered Distributed Architectures using .NET Aspire and GenAI to develop EShop Catalog and Basket microservices integrate with Backing services including PostgreSQL, Redis, RabbitMQ, Keycloak, Ollama and Semantic Kernel to Create Intelligent E-Shop Solutions.

![big_picture](https://github.com/user-attachments/assets/7933c4ac-ae45-4a89-907e-0c0545a5fbfd)

This is the EShop Aplication running, performing a **Semantic Search**:
![06eShopLite-SearchSemantic](https://github.com/user-attachments/assets/31353be8-5419-4161-bbac-c0ed5cf42899)

## Local Docker connectivity

The AppHost, Basket, and WebApp launch profiles set `DOTNET_SYSTEM_NET_DISABLEIPV6=1` to avoid Redis connection timeouts when `localhost` selects IPv6 but Docker publishes the service on IPv4 loopback. This affects all .NET networking in those local processes; TLS and Aspire-assigned ports remain enabled. Production configuration is unchanged. Stop and restart AppHost and its project resources after changing launch profiles.

If Docker's IPv6 loopback connectivity is working, remove this setting from both profiles in each project's `Properties\launchSettings.json` to restore dual-stack networking.
