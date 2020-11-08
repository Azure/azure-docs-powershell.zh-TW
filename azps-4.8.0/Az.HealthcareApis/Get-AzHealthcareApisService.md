---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: d1a6edc3365631f93d2bc3b7a0e153ec360c2611
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129320"
---
# <span data-ttu-id="3f4aa-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="3f4aa-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="3f4aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f4aa-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4aa-103">取得服務實例的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3f4aa-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="3f4aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f4aa-104">SYNTAX</span></span>

### <span data-ttu-id="3f4aa-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3f4aa-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f4aa-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f4aa-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f4aa-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f4aa-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f4aa-108">說明</span><span class="sxs-lookup"><span data-stu-id="3f4aa-108">DESCRIPTION</span></span>
<span data-ttu-id="3f4aa-109">取得在指定的訂閱或資源群組內建立的現有 healthcareApis fhir 服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="3f4aa-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="3f4aa-110">示例</span><span class="sxs-lookup"><span data-stu-id="3f4aa-110">EXAMPLES</span></span>

### <span data-ttu-id="3f4aa-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3f4aa-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -Name "MyService" -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="3f4aa-112">範例2</span><span class="sxs-lookup"><span data-stu-id="3f4aa-112">Example 2</span></span>

<span data-ttu-id="3f4aa-113">取得所提供資源群組中所有 HealthcareApis 服務的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3f4aa-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="3f4aa-114">範例3</span><span class="sxs-lookup"><span data-stu-id="3f4aa-114">Example 3</span></span>

<span data-ttu-id="3f4aa-115">取得指定訂閱中所有 HealthcareApis 服務的中繼資料</span><span class="sxs-lookup"><span data-stu-id="3f4aa-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="3f4aa-116">參數</span><span class="sxs-lookup"><span data-stu-id="3f4aa-116">PARAMETERS</span></span>

### <span data-ttu-id="3f4aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4aa-117">-DefaultProfile</span></span>
<span data-ttu-id="3f4aa-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f4aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f4aa-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="3f4aa-119">-Name</span></span>
<span data-ttu-id="3f4aa-120">HealthcareApis 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="3f4aa-120">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f4aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="3f4aa-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3f4aa-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4aa-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f4aa-123">-ResourceId</span></span>
<span data-ttu-id="3f4aa-124">資源識別碼名稱。</span><span class="sxs-lookup"><span data-stu-id="3f4aa-124">Resource Id Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4aa-125">CommonParameters</span></span>
<span data-ttu-id="3f4aa-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f4aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4aa-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3f4aa-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4aa-128">輸入</span><span class="sxs-lookup"><span data-stu-id="3f4aa-128">INPUTS</span></span>

### <span data-ttu-id="3f4aa-129">System.object</span><span class="sxs-lookup"><span data-stu-id="3f4aa-129">System.String</span></span>

## <span data-ttu-id="3f4aa-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3f4aa-130">OUTPUTS</span></span>

### <span data-ttu-id="3f4aa-131">PSHealthcareApisService 中的 HealthcareApisService。</span><span class="sxs-lookup"><span data-stu-id="3f4aa-131">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="3f4aa-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3f4aa-132">NOTES</span></span>

## <span data-ttu-id="3f4aa-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f4aa-133">RELATED LINKS</span></span>
