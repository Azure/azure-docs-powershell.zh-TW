---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 57e1aa691ffaca498e925488fb90fb8b828ff9f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903790"
---
# <span data-ttu-id="b9431-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b9431-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="b9431-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b9431-102">SYNOPSIS</span></span>
<span data-ttu-id="b9431-103">獲得資源提供者。</span><span class="sxs-lookup"><span data-stu-id="b9431-103">Gets a resource provider.</span></span>

## <span data-ttu-id="b9431-104">語法</span><span class="sxs-lookup"><span data-stu-id="b9431-104">SYNTAX</span></span>

### <span data-ttu-id="b9431-105">清單可用 (預設) </span><span class="sxs-lookup"><span data-stu-id="b9431-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9431-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="b9431-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9431-107">描述</span><span class="sxs-lookup"><span data-stu-id="b9431-107">DESCRIPTION</span></span>
<span data-ttu-id="b9431-108">**Get-AzResourceProvider Cmdlet** 會取得 Azure 資源提供者。</span><span class="sxs-lookup"><span data-stu-id="b9431-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="b9431-109">例子</span><span class="sxs-lookup"><span data-stu-id="b9431-109">EXAMPLES</span></span>

### <span data-ttu-id="b9431-110">範例 1：取得以目前訂閱註冊的所有資源提供者</span><span class="sxs-lookup"><span data-stu-id="b9431-110">Example 1: Get all resource providers registered with the current subscription</span></span>

```powershell
PS C:\>Get-AzResourceProvider

ProviderNamespace : Microsoft.AppConfiguration
RegistrationState : Registered
ResourceTypes     : {configurationStores, configurationStores/eventGridFilters, checkNameAvailability, locations…}
Locations         : {West Central US, Central US, West US, East US…}

ProviderNamespace : Microsoft.KeyVault
RegistrationState : Registered
ResourceTypes     : {vaults, vaults/secrets, vaults/accessPolicies, operations…}
Locations         : {North Central US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {virtualNetworks, publicIPAddresses, networkInterfaces, privateEndpoints…}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets, virtualMachines, virtualMachines/extensions, virtualMachineScaleSets…}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Security
RegistrationState : Registered
ResourceTypes     : {operations, securityStatuses, tasks, regulatoryComplianceStandards…}
Locations         : {Central US, East US, West Europe, West Central US…}

ProviderNamespace : Microsoft.ResourceHealth
RegistrationState : Registered
ResourceTypes     : {availabilityStatuses, childAvailabilityStatuses, childResources, events…}
Locations         : {Australia Southeast}

ProviderNamespace : Microsoft.PolicyInsights
RegistrationState : Registered
ResourceTypes     : {policyEvents, policyStates, operations, asyncOperationResults…}
Locations         : {}

ProviderNamespace : Microsoft.Storage
RegistrationState : Registered
ResourceTypes     : {storageAccounts, operations, locations/asyncoperations, storageAccounts/listAccountSas…}
Locations         : {East US, East US 2, West US, West Europe…}

ProviderNamespace : Microsoft.Web
RegistrationState : Registered
ResourceTypes     : {publishingUsers, ishostnameavailable, validate, isusernameavailable…}
Locations         : {Central US, North Europe, West Europe, Southeast Asia…}

ProviderNamespace : Sendgrid.Email
RegistrationState : Registered
ResourceTypes     : {accounts, operations}
Locations         : {Australia East, Australia Southeast, Brazil South, Canada Central…}

ProviderNamespace : Microsoft.Authorization
RegistrationState : Registered
ResourceTypes     : {roleAssignments, roleDefinitions, classicAdministrators, permissions…}
Locations         : {}
...
```

<span data-ttu-id="b9431-111">此命令會從訂閱中獲得所有資源提供者。</span><span class="sxs-lookup"><span data-stu-id="b9431-111">This command gets all the resource providers from the subscription.</span></span>

### <span data-ttu-id="b9431-112">範例 2：從特定 ProviderNamespace 取得所有資源提供者詳細資料</span><span class="sxs-lookup"><span data-stu-id="b9431-112">Example 2: Get all resource provider details from the given ProviderNamespace</span></span>

```powershell
PS C:\>Get-AzResourceProvider -ProviderNamespace Microsoft.Compute
ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/networkInterfaces}
Locations         : {East US, East US 2, West US, Central US…}
...
```

<span data-ttu-id="b9431-113">此命令會獲得 "Microsoft.Compute" 下的所有資源提供者。</span><span class="sxs-lookup"><span data-stu-id="b9431-113">This command Gets all the resource providers under "Microsoft.Compute".</span></span>

### <span data-ttu-id="b9431-114">範例 3：從特定 ProviderNamespace 陣列取得所有資源提供者詳細資料</span><span class="sxs-lookup"><span data-stu-id="b9431-114">Example 3: Get all resource provider details from the given ProviderNamespace array</span></span>

```powershell
PS C:\>Get-AzResourceProvider -ProviderNamespace Microsoft.Compute,Microsoft.Network
ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/extensions}
Locations         : {East US, East US 2, West US, Central US…}
...

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {virtualNetworks}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {publicIPAddresses}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {networkInterfaces}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {privateEndpoints}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {privateEndpointRedirectMaps}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {loadBalancers}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {networkSecurityGroups}
Locations         : {West US, East US, North Europe, West Europe…}
...
```

<span data-ttu-id="b9431-115">此命令會獲得 "Microsoft.Compute" 和 "Microsoft.Network" 下的所有資源提供者。</span><span class="sxs-lookup"><span data-stu-id="b9431-115">This command Gets all the resource providers under "Microsoft.Compute" and "Microsoft.Network".</span></span>

## <span data-ttu-id="b9431-116">參數</span><span class="sxs-lookup"><span data-stu-id="b9431-116">PARAMETERS</span></span>

### <span data-ttu-id="b9431-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b9431-117">-ApiVersion</span></span>
<span data-ttu-id="b9431-118">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b9431-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b9431-119">您可以指定與預設版本不同的版本。</span><span class="sxs-lookup"><span data-stu-id="b9431-119">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9431-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9431-120">-DefaultProfile</span></span>
<span data-ttu-id="b9431-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b9431-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9431-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="b9431-122">-ListAvailable</span></span>
<span data-ttu-id="b9431-123">表示此作業會獲得所有可用的資源提供者。</span><span class="sxs-lookup"><span data-stu-id="b9431-123">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9431-124">-位置</span><span class="sxs-lookup"><span data-stu-id="b9431-124">-Location</span></span>
<span data-ttu-id="b9431-125">指定資源提供者的位置。</span><span class="sxs-lookup"><span data-stu-id="b9431-125">Specifies the location of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9431-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="b9431-126">-Pre</span></span>
<span data-ttu-id="b9431-127">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b9431-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9431-128">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="b9431-128">-ProviderNamespace</span></span>
<span data-ttu-id="b9431-129">指定資源提供者的命名空間。</span><span class="sxs-lookup"><span data-stu-id="b9431-129">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9431-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9431-130">CommonParameters</span></span>
<span data-ttu-id="b9431-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b9431-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9431-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9431-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9431-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b9431-133">INPUTS</span></span>

### <span data-ttu-id="b9431-134">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b9431-134">System.String[]</span></span>

## <span data-ttu-id="b9431-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b9431-135">OUTPUTS</span></span>

### <span data-ttu-id="b9431-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b9431-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="b9431-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b9431-137">NOTES</span></span>

## <span data-ttu-id="b9431-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9431-138">RELATED LINKS</span></span>

[<span data-ttu-id="b9431-139">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b9431-139">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="b9431-140">取消註冊-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b9431-140">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


