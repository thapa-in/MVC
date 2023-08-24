
Help of Unity we can achive Dependency in our Web Api Project.

We can achive DI in MVC application by install two Nuget package in our MVC5 application.
1. **Unity v5.11.1**
2. **Unity.Mvc5v1.4.0**

Then we can get **UnityConfig.cs** in "**App_Start**" folder

Declare Repository in there UnityConfig.cs 
```
container.RegisterType<IJsonResponse, JsonResponse>();
```
