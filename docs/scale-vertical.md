This topic describes how to scale the .NET Core sample app.

## Overview

Factors such as user load, or the number and nature of tasks performed by a
{{ product_short }} app, can change the disk space and memory the app uses. For
many apps, increasing the available disk space or memory can improve overall
performance. Similarly, running additional instances of an app can allow the app
to handle increases in user load and concurrent requests.

Use the `cf scale` command to scale the .NET sample app in the following ways:

- **Horizontal scaling**: Create or destroy instances of the app. Adding more
instances allows your app to handle increased traffic and demand.
- **Vertical scaling**: Change the disk space limit or memory limit that
{{ product_short }} applies to all instances of the app. Adding more disk or
memory resources can improve the overall performance of your app.

## Scale up the .NET Core sample app vertically

You can scale up an app vertically by changing the disk space limit and the
memory limit.

### Scale up disk

To scale up the .NET Core sample app disk, run the following command:

``` shell
cf scale dotnet-core-sample-app -k 1G
```

After you run the above command, {{ product_short }} increases the disk space of
all instances of your app to 1&nbsp;GB.

### Scale up memory

To scale up the .NET Core sample app memory, run the following command:

``` shell
cf scale dotnet-sample-app -m 1G
```

After you run the above command, {{ product_short }} increases the memory limit of
all instances of your app to 1&nbsp;GB.

## Scale down the .NET Core sample app vertically

You can scale an app down vertically by decreasing the disk space limit and the
memory limit.

### Scale down disk

To scale down the .NET Core sample app disk, run the following command:

``` shell
cf scale dotnet-core-sample-app -k 512M
```

After you run the above command, {{ product_short }} decreases the disk space of
all instances of your app to 512&nbsp;MB.

### Scale down memory

To scale down the .NET Core sample app memory, run the following command:

``` shell
cf scale dotnet-core-sample-app -m 512M
```

After you run the above command, {{ product_short }} decreases the memory limit of
all instances of your app to 512&nbsp;MB.