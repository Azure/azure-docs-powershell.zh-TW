---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: e99c060cc7446cbecc46040ec4a498cf9f545e7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917217"
---
# <span data-ttu-id="5c285-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="5c285-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="5c285-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5c285-102">SYNOPSIS</span></span>
<span data-ttu-id="5c285-103">建立服務實例的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5c285-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="5c285-104">語法</span><span class="sxs-lookup"><span data-stu-id="5c285-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c285-105">描述</span><span class="sxs-lookup"><span data-stu-id="5c285-105">DESCRIPTION</span></span>
<span data-ttu-id="5c285-106">建立或更新服務實例的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5c285-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="5c285-107">例子</span><span class="sxs-lookup"><span data-stu-id="5c285-107">EXAMPLES</span></span>

### <span data-ttu-id="5c285-108">範例 1：在位於 westus2 位置的資源群組 MyResourceGroup 中，建立名為 MyService 的新 Azure healthcareapis fhir 服務，其提供輸送量 = 400</span><span class="sxs-lookup"><span data-stu-id="5c285-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : 
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

### <span data-ttu-id="5c285-109">範例 2：在位於 westus2 位置的資源群組 MyResourceGroup 中，建立名為 MyService 的新 Azure healthcareapis fhir 服務，其提供輸送量 = 400 且金鑰庫金鑰 uri "HTTPs:// \<my-keyvault> \<my-key> .vault.azure.net/keys/"</span><span class="sxs-lookup"><span data-stu-id="5c285-109">Example 2 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : https://<my-keyvault>.vault.azure.net/keys/<my-key>
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

## <span data-ttu-id="5c285-110">參數</span><span class="sxs-lookup"><span data-stu-id="5c285-110">PARAMETERS</span></span>

### <span data-ttu-id="5c285-111">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="5c285-111">-AccessPolicyObjectId</span></span>
<span data-ttu-id="5c285-112">Access Policy Object ID 清單。</span><span class="sxs-lookup"><span data-stu-id="5c285-112">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c285-113">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="5c285-113">-AllowCorsCredential</span></span>
<span data-ttu-id="5c285-114">HealthcareApis Fhir Service AllowCorsCredentials.</span><span class="sxs-lookup"><span data-stu-id="5c285-114">HealthcareApis Fhir Service AllowCorsCredentials.</span></span>

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

### <span data-ttu-id="5c285-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c285-115">-AsJob</span></span>
<span data-ttu-id="5c285-116">在背景中以工作執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c285-116">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="5c285-117">-物件</span><span class="sxs-lookup"><span data-stu-id="5c285-117">-Audience</span></span>
<span data-ttu-id="5c285-118">醫療保健發票服務物件。</span><span class="sxs-lookup"><span data-stu-id="5c285-118">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="5c285-119">-授權</span><span class="sxs-lookup"><span data-stu-id="5c285-119">-Authority</span></span>
<span data-ttu-id="5c285-120">醫療保健Apis Fhir Service Authority.</span><span class="sxs-lookup"><span data-stu-id="5c285-120">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="5c285-121">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="5c285-121">-CorsHeader</span></span>
<span data-ttu-id="5c285-122">HealthcareApis Fhir Service List of Cors Header.</span><span class="sxs-lookup"><span data-stu-id="5c285-122">HealthcareApis Fhir Service List of Cors Header.</span></span>
<span data-ttu-id="5c285-123">指定可在要求期間使用的 HTTP 標頭。</span><span class="sxs-lookup"><span data-stu-id="5c285-123">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="5c285-124">將 " \* " 用於任何頁眉。</span><span class="sxs-lookup"><span data-stu-id="5c285-124">Use " \* " for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c285-125">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="5c285-125">-CorsMaxAge</span></span>
<span data-ttu-id="5c285-126">HealthcareApis Fhir Service Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="5c285-126">HealthcareApis Fhir Service Cors Max Age.</span></span>
<span data-ttu-id="5c285-127">指定要求的結果可以以秒數進行緩存多久。</span><span class="sxs-lookup"><span data-stu-id="5c285-127">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="5c285-128">範例：600 表示 10 分鐘。</span><span class="sxs-lookup"><span data-stu-id="5c285-128">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c285-129">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="5c285-129">-CorsMethod</span></span>
<span data-ttu-id="5c285-130">Cors Method 的 HealthcareApis Fhir Service List.</span><span class="sxs-lookup"><span data-stu-id="5c285-130">HealthcareApis Fhir Service List of Cors Method.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c285-131">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="5c285-131">-CorsOrigin</span></span>
<span data-ttu-id="5c285-132">HealthcareApis Fhir Service List of Cors Origin.</span><span class="sxs-lookup"><span data-stu-id="5c285-132">HealthcareApis Fhir Service List of Cors Origin.</span></span>
<span data-ttu-id="5c285-133">指定可存取此 API 的來源網站的 URL，或使用 " \* " 允許從任何網站存取。</span><span class="sxs-lookup"><span data-stu-id="5c285-133">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c285-134">-外星KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="5c285-134">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="5c285-135">HealthcareApis Fhir ServiceAultsKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="5c285-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="5c285-136">支援資料庫之客戶管理金鑰的 URI。</span><span class="sxs-lookup"><span data-stu-id="5c285-136">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="5c285-137">-一些高能專案</span><span class="sxs-lookup"><span data-stu-id="5c285-137">-CosmosOfferThroughput</span></span>
<span data-ttu-id="5c285-138">HealthcareApis Fhir Service一些OfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="5c285-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c285-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c285-139">-DefaultProfile</span></span>
<span data-ttu-id="5c285-140">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c285-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c285-141">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="5c285-141">-EnableSmartProxy</span></span>
<span data-ttu-id="5c285-142">HealthcareApis Fhir Service EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="5c285-142">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="5c285-143">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5c285-143">-ExportStorageAccountName</span></span>
<span data-ttu-id="5c285-144">HealthcareApis Fhir Service 匯出儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5c285-144">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="5c285-145">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="5c285-145">-FhirVersion</span></span>
<span data-ttu-id="5c285-146">Fhir 版本。</span><span class="sxs-lookup"><span data-stu-id="5c285-146">Fhir Version.</span></span>

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

### <span data-ttu-id="5c285-147">-Kind</span><span class="sxs-lookup"><span data-stu-id="5c285-147">-Kind</span></span>
<span data-ttu-id="5c285-148">一種醫療保健發票服務。</span><span class="sxs-lookup"><span data-stu-id="5c285-148">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="5c285-149">預設值為 Fhir</span><span class="sxs-lookup"><span data-stu-id="5c285-149">The default value is Fhir</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c285-150">-位置</span><span class="sxs-lookup"><span data-stu-id="5c285-150">-Location</span></span>
<span data-ttu-id="5c285-151">醫療保健發票服務位置。</span><span class="sxs-lookup"><span data-stu-id="5c285-151">HealthcareApis Service Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c285-152">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="5c285-152">-ManagedIdentity</span></span>
<span data-ttu-id="5c285-153">使用受管理的身分識別？</span><span class="sxs-lookup"><span data-stu-id="5c285-153">Use Managed Identity?</span></span>

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

### <span data-ttu-id="5c285-154">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c285-154">-Name</span></span>
<span data-ttu-id="5c285-155">醫療保健發票服務名稱。</span><span class="sxs-lookup"><span data-stu-id="5c285-155">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c285-156">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="5c285-156">-PublicNetworkAccess</span></span>
<span data-ttu-id="5c285-157">Fhir 服務的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="5c285-157">The network access type for Fhir service.</span></span> <span data-ttu-id="5c285-158">一般 `Enabled` 或 `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="5c285-158">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c285-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c285-159">-ResourceGroupName</span></span>
<span data-ttu-id="5c285-160">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5c285-160">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c285-161">-標記</span><span class="sxs-lookup"><span data-stu-id="5c285-161">-Tag</span></span>
<span data-ttu-id="5c285-162">HealthcareApis Fhir Service 帳戶標記。</span><span class="sxs-lookup"><span data-stu-id="5c285-162">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c285-163">-確認</span><span class="sxs-lookup"><span data-stu-id="5c285-163">-Confirm</span></span>
<span data-ttu-id="5c285-164">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5c285-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c285-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c285-165">-WhatIf</span></span>
<span data-ttu-id="5c285-166">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c285-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c285-167">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c285-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c285-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c285-168">CommonParameters</span></span>
<span data-ttu-id="5c285-169">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5c285-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c285-170">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c285-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c285-171">輸入</span><span class="sxs-lookup"><span data-stu-id="5c285-171">INPUTS</span></span>

### <span data-ttu-id="5c285-172">System.String</span><span class="sxs-lookup"><span data-stu-id="5c285-172">System.String</span></span>

## <span data-ttu-id="5c285-173">輸出</span><span class="sxs-lookup"><span data-stu-id="5c285-173">OUTPUTS</span></span>

### <span data-ttu-id="5c285-174">Microsoft.Azure.Commands.HealthcareApis.models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="5c285-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="5c285-175">筆記</span><span class="sxs-lookup"><span data-stu-id="5c285-175">NOTES</span></span>

## <span data-ttu-id="5c285-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c285-176">RELATED LINKS</span></span>
