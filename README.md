Terraform module for creating Azure Web App service with Free Azure Service Plan.

## Description

This Terraform module creates an Azure Web App service with a Free tier App Service Plan. It provides a simple way to deploy web applications to Azure with minimal configuration.

## Requirements

| Name      | Version  |
| --------- | -------- |
| terraform | >= 1.0.0 |
| azurerm   | >= 3.0.0 |

## Providers

| Name    | Version  |
| ------- | -------- |
| azurerm | >= 3.0.0 |

## Inputs

| Name                | Description                                          | Type     | Default | Required |
| ------------------- | ---------------------------------------------------- | -------- | ------- | :------: |
| app_name            | The name of the Web App                              | `string` | n/a     |   yes    |
| location            | The Azure region where the resources will be created | `string` | n/a     |   yes    |
| resource_group_name | The name of the resource group                       | `string` | n/a     |   yes    |

## Outputs

| Name                      | Description                          |
| ------------------------- | ------------------------------------ |
| service_plan_name         | Represents service plan name         |
| service_plan_id           | Represents service plan id           |
| web_app_name              | Represents web app name              |
| web_app_id                | Represents web app id                |
| web_app_default_host_name | Represents web app default host name |

## Usage

```hcl
module "web_app" {
  source  = "Dragan2402/terraform-azurerm-web-app"
  version = "1.0.0"

  app_name            = "my-web-app"
  location            = "eastus"
  resource_group_name = "my-resource-group"
}
```

## License

MIT Licensed. See LICENSE for full details.

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Authors

Maintained by Dragan Mirkovic

## Additional Information

- [Azure Web App Documentation](https://docs.microsoft.com/en-us/azure/app-service/)
- [Terraform Azure Provider Documentation](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs)
