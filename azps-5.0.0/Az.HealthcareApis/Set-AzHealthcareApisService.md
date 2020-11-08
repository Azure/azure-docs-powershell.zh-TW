---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: a944982688dac8f9a28c10b3d26e71a8331451ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138820"
---
# <span data-ttu-id="f79c6-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="f79c6-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="f79c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f79c6-102">SYNOPSIS</span></span>
<span data-ttu-id="f79c6-103">更新現有的 healthcareApis fhir 服務。</span><span class="sxs-lookup"><span data-stu-id="f79c6-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="f79c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="f79c6-104">SYNTAX</span></span>

### <span data-ttu-id="f79c6-105">ServiceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f79c6-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f79c6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f79c6-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-Authority <String>] [-Audience <String>]
 [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>]
 [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential]
 [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity]
 [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f79c6-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f79c6-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f79c6-108">說明</span><span class="sxs-lookup"><span data-stu-id="f79c6-108">DESCRIPTION</span></span>
<span data-ttu-id="f79c6-109">更新現有的 healthcareApis fhir 服務。</span><span class="sxs-lookup"><span data-stu-id="f79c6-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="f79c6-110">示例</span><span class="sxs-lookup"><span data-stu-id="f79c6-110">EXAMPLES</span></span>

### <span data-ttu-id="f79c6-111">範例1：使用 cosmosdb OfferThroughput = 500 更新資源群組 MyResourceGroup 中名為 MyService 的現有 healthcareapis 服務。</span><span class="sxs-lookup"><span data-stu-id="f79c6-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> Set-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 500
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

### <span data-ttu-id="f79c6-112">範例2：使用 cosmosdb OfferThroughput = 500 更新資源群組 MyResourceGroup 中名為 MyService 的現有 healthcareapis 服務。</span><span class="sxs-lookup"><span data-stu-id="f79c6-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 500
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

## <span data-ttu-id="f79c6-113">參數</span><span class="sxs-lookup"><span data-stu-id="f79c6-113">PARAMETERS</span></span>

### <span data-ttu-id="f79c6-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="f79c6-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="f79c6-115">存取原則物件識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="f79c6-115">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="f79c6-116">-AllowCorsCredential</span></span>
<span data-ttu-id="f79c6-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="f79c6-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f79c6-118">-AsJob</span></span>
<span data-ttu-id="f79c6-119">在背景中執行 Cmdlet 作為作業。</span><span class="sxs-lookup"><span data-stu-id="f79c6-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="f79c6-120">-物件</span><span class="sxs-lookup"><span data-stu-id="f79c6-120">-Audience</span></span>
<span data-ttu-id="f79c6-121">HealthcareApis FhirService 物件。</span><span class="sxs-lookup"><span data-stu-id="f79c6-121">HealthcareApis FhirService Audience.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-122">-頒發機構</span><span class="sxs-lookup"><span data-stu-id="f79c6-122">-Authority</span></span>
<span data-ttu-id="f79c6-123">HealthcareApis [FhirService 機關]。</span><span class="sxs-lookup"><span data-stu-id="f79c6-123">HealthcareApis FhirService Authority.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="f79c6-124">-CorsHeader</span></span>
<span data-ttu-id="f79c6-125">HealthcareApis Fhir 服務的 Cors 標頭清單。</span><span class="sxs-lookup"><span data-stu-id="f79c6-125">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="f79c6-126">指定可在要求期間使用的 HTTP 標頭。</span><span class="sxs-lookup"><span data-stu-id="f79c6-126">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="f79c6-127">針對任何標題使用 \*。</span><span class="sxs-lookup"><span data-stu-id="f79c6-127">Use \* for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="f79c6-128">-CorsMaxAge</span></span>
<span data-ttu-id="f79c6-129">HealthcareApis Fhir 服務 Cors 最大使用時間。</span><span class="sxs-lookup"><span data-stu-id="f79c6-129">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="f79c6-130">指定要求中的結果可在數秒內緩存多久。</span><span class="sxs-lookup"><span data-stu-id="f79c6-130">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="f79c6-131">範例：600代表10分鐘。</span><span class="sxs-lookup"><span data-stu-id="f79c6-131">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="f79c6-132">-CorsMethod</span></span>
<span data-ttu-id="f79c6-133">HealthcareApis FhirService 的 Cors 方法清單。</span><span class="sxs-lookup"><span data-stu-id="f79c6-133">HealthcareApis FhirService List of Cors Methods.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="f79c6-134">-CorsOrigin</span></span>
<span data-ttu-id="f79c6-135">[Cors 來源] 的 HealthcareApis FhirService 清單。</span><span class="sxs-lookup"><span data-stu-id="f79c6-135">HealthcareApis FhirService List of Cors Origins.</span></span> <span data-ttu-id="f79c6-136">[Cors 來源] 的 HealthcareApis Fhir 服務清單。</span><span class="sxs-lookup"><span data-stu-id="f79c6-136">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="f79c6-137">指定可存取此 API 的來源網站 Url，或使用 \* 以允許來自任何網站的存取權。</span><span class="sxs-lookup"><span data-stu-id="f79c6-137">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-138">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="f79c6-138">-CosmosOfferThroughput</span></span>
<span data-ttu-id="f79c6-139">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="f79c6-139">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f79c6-140">-DefaultProfile</span></span>
<span data-ttu-id="f79c6-141">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f79c6-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f79c6-142">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="f79c6-142">-DisableCorsCredential</span></span>
<span data-ttu-id="f79c6-143">不允許 HealthcareApis FhirService CorsCredentials。</span><span class="sxs-lookup"><span data-stu-id="f79c6-143">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-144">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="f79c6-144">-DisableManagedIdentity</span></span>
<span data-ttu-id="f79c6-145">停用受管理的身分識別。</span><span class="sxs-lookup"><span data-stu-id="f79c6-145">Disable Managed Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-146">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="f79c6-146">-DisableSmartProxy</span></span>
<span data-ttu-id="f79c6-147">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="f79c6-147">HealthcareApis FhirService DisableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-148">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="f79c6-148">-EnableManagedIdentity</span></span>
<span data-ttu-id="f79c6-149">啟用受管理的身分識別。</span><span class="sxs-lookup"><span data-stu-id="f79c6-149">Enable Managed Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-150">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="f79c6-150">-EnableSmartProxy</span></span>
<span data-ttu-id="f79c6-151">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="f79c6-151">HealthcareApis FhirService EnableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-152">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f79c6-152">-ExportStorageAccountName</span></span>
<span data-ttu-id="f79c6-153">HealthcareApis Fhir Service 匯出儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f79c6-153">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f79c6-154">-InputObject</span></span>
<span data-ttu-id="f79c6-155">從 AzHealthcareApisFhirService HealthcareApis fhir service 輸送管道。</span><span class="sxs-lookup"><span data-stu-id="f79c6-155">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-156">-名稱</span><span class="sxs-lookup"><span data-stu-id="f79c6-156">-Name</span></span>
<span data-ttu-id="f79c6-157">HealthcareApis 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="f79c6-157">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="f79c6-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f79c6-158">-ResourceGroupName</span></span>
<span data-ttu-id="f79c6-159">HealthcareApis 服務資源組名。</span><span class="sxs-lookup"><span data-stu-id="f79c6-159">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="f79c6-160">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f79c6-160">-ResourceId</span></span>
<span data-ttu-id="f79c6-161">HealthcareApis Fhir Service ResourceId。</span><span class="sxs-lookup"><span data-stu-id="f79c6-161">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="f79c6-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="f79c6-162">-Tag</span></span>
<span data-ttu-id="f79c6-163">HealthcareApis Fhir 服務帳戶標記。</span><span class="sxs-lookup"><span data-stu-id="f79c6-163">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-164">-確認</span><span class="sxs-lookup"><span data-stu-id="f79c6-164">-Confirm</span></span>
<span data-ttu-id="f79c6-165">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f79c6-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f79c6-166">-WhatIf</span></span>
<span data-ttu-id="f79c6-167">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f79c6-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f79c6-168">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f79c6-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79c6-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f79c6-169">CommonParameters</span></span>
<span data-ttu-id="f79c6-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f79c6-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f79c6-171">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f79c6-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f79c6-172">輸入</span><span class="sxs-lookup"><span data-stu-id="f79c6-172">INPUTS</span></span>

### <span data-ttu-id="f79c6-173">System.object</span><span class="sxs-lookup"><span data-stu-id="f79c6-173">System.String</span></span>

### <span data-ttu-id="f79c6-174">PSHealthcareApisService 中的 HealthcareApisService。</span><span class="sxs-lookup"><span data-stu-id="f79c6-174">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="f79c6-175">輸出</span><span class="sxs-lookup"><span data-stu-id="f79c6-175">OUTPUTS</span></span>

### <span data-ttu-id="f79c6-176">PSHealthcareApisService 中的 HealthcareApisService。</span><span class="sxs-lookup"><span data-stu-id="f79c6-176">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="f79c6-177">筆記</span><span class="sxs-lookup"><span data-stu-id="f79c6-177">NOTES</span></span>

## <span data-ttu-id="f79c6-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="f79c6-178">RELATED LINKS</span></span>
