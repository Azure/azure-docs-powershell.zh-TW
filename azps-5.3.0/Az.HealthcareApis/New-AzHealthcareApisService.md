---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: 33f1af70b0fef7e89ccb584ed3b69f32e2810690
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98289107"
---
# <span data-ttu-id="cb520-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="cb520-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="cb520-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb520-102">SYNOPSIS</span></span>
<span data-ttu-id="cb520-103">建立服務實例的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="cb520-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="cb520-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb520-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb520-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb520-105">DESCRIPTION</span></span>
<span data-ttu-id="cb520-106">建立或更新服務實例的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="cb520-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="cb520-107">示例</span><span class="sxs-lookup"><span data-stu-id="cb520-107">EXAMPLES</span></span>

### <span data-ttu-id="cb520-108">範例1：在資源群組 MyResourceGroup 中，建立一個名為 MyService 的新 Azure healthcareapis fhir 服務，其中 westus2 優惠輸送量 = 400</span><span class="sxs-lookup"><span data-stu-id="cb520-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
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

### <span data-ttu-id="cb520-109">範例2：在位置 westus2 的資源群組 MyResourceGroup 中，建立名為 MyService 的新 Azure healthcareapis fhir 服務，並提供 cosmosdb 提供輸送量 = 400 和主要保存庫金鑰 uri "HTTPs:// \<my-keyvault> . vault.azure.net/keys/ \<my-key> "</span><span class="sxs-lookup"><span data-stu-id="cb520-109">Example 2 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>
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

## <span data-ttu-id="cb520-110">參數</span><span class="sxs-lookup"><span data-stu-id="cb520-110">PARAMETERS</span></span>

### <span data-ttu-id="cb520-111">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="cb520-111">-AccessPolicyObjectId</span></span>
<span data-ttu-id="cb520-112">存取原則物件識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="cb520-112">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="cb520-113">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="cb520-113">-AllowCorsCredential</span></span>
<span data-ttu-id="cb520-114">HealthcareApis Fhir Services AllowCorsCredentials。</span><span class="sxs-lookup"><span data-stu-id="cb520-114">HealthcareApis Fhir Service AllowCorsCredentials.</span></span>

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

### <span data-ttu-id="cb520-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb520-115">-AsJob</span></span>
<span data-ttu-id="cb520-116">在背景中執行 Cmdlet 作為作業。</span><span class="sxs-lookup"><span data-stu-id="cb520-116">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="cb520-117">-物件</span><span class="sxs-lookup"><span data-stu-id="cb520-117">-Audience</span></span>
<span data-ttu-id="cb520-118">HealthcareApis Fhir Services 物件。</span><span class="sxs-lookup"><span data-stu-id="cb520-118">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="cb520-119">-頒發機構</span><span class="sxs-lookup"><span data-stu-id="cb520-119">-Authority</span></span>
<span data-ttu-id="cb520-120">HealthcareApis [Fhir 服務授權]。</span><span class="sxs-lookup"><span data-stu-id="cb520-120">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="cb520-121">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="cb520-121">-CorsHeader</span></span>
<span data-ttu-id="cb520-122">HealthcareApis Fhir 服務的 Cors 標頭清單。</span><span class="sxs-lookup"><span data-stu-id="cb520-122">HealthcareApis Fhir Service List of Cors Header.</span></span>
<span data-ttu-id="cb520-123">指定可在要求期間使用的 HTTP 標頭。</span><span class="sxs-lookup"><span data-stu-id="cb520-123">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="cb520-124">針對任何標題使用 "\*"。</span><span class="sxs-lookup"><span data-stu-id="cb520-124">Use " \* " for any header.</span></span>

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

### <span data-ttu-id="cb520-125">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="cb520-125">-CorsMaxAge</span></span>
<span data-ttu-id="cb520-126">HealthcareApis Fhir 服務 Cors 最大使用時間。</span><span class="sxs-lookup"><span data-stu-id="cb520-126">HealthcareApis Fhir Service Cors Max Age.</span></span>
<span data-ttu-id="cb520-127">指定要求中的結果可在數秒內緩存多久。</span><span class="sxs-lookup"><span data-stu-id="cb520-127">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="cb520-128">範例：600代表10分鐘。</span><span class="sxs-lookup"><span data-stu-id="cb520-128">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="cb520-129">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="cb520-129">-CorsMethod</span></span>
<span data-ttu-id="cb520-130">HealthcareApis Fhir 服務的 Cors 方法清單。</span><span class="sxs-lookup"><span data-stu-id="cb520-130">HealthcareApis Fhir Service List of Cors Method.</span></span>

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

### <span data-ttu-id="cb520-131">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="cb520-131">-CorsOrigin</span></span>
<span data-ttu-id="cb520-132">[Cors 來源] 的 HealthcareApis Fhir 服務清單。</span><span class="sxs-lookup"><span data-stu-id="cb520-132">HealthcareApis Fhir Service List of Cors Origin.</span></span>
<span data-ttu-id="cb520-133">指定可存取此 API 的來源網站 Url，或使用 "\*" 允許來自任何網站的存取權。</span><span class="sxs-lookup"><span data-stu-id="cb520-133">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

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

### <span data-ttu-id="cb520-134">-CosmosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="cb520-134">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="cb520-135">HealthcareApis Fhir Services CosmosKeyVaultKeyUri。</span><span class="sxs-lookup"><span data-stu-id="cb520-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="cb520-136">後備資料庫的客戶管理金鑰的 URI。</span><span class="sxs-lookup"><span data-stu-id="cb520-136">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="cb520-137">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="cb520-137">-CosmosOfferThroughput</span></span>
<span data-ttu-id="cb520-138">HealthcareApis Fhir Services CosmosOfferThroughput。</span><span class="sxs-lookup"><span data-stu-id="cb520-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="cb520-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb520-139">-DefaultProfile</span></span>
<span data-ttu-id="cb520-140">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb520-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb520-141">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="cb520-141">-EnableSmartProxy</span></span>
<span data-ttu-id="cb520-142">HealthcareApis Fhir Services EnableSmartProxy。</span><span class="sxs-lookup"><span data-stu-id="cb520-142">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="cb520-143">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cb520-143">-ExportStorageAccountName</span></span>
<span data-ttu-id="cb520-144">HealthcareApis Fhir Service 匯出儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="cb520-144">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="cb520-145">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="cb520-145">-FhirVersion</span></span>
<span data-ttu-id="cb520-146">Fhir 版本。</span><span class="sxs-lookup"><span data-stu-id="cb520-146">Fhir Version.</span></span>

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

### <span data-ttu-id="cb520-147">類型</span><span class="sxs-lookup"><span data-stu-id="cb520-147">-Kind</span></span>
<span data-ttu-id="cb520-148">HealthcareApis 服務的類型。</span><span class="sxs-lookup"><span data-stu-id="cb520-148">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="cb520-149">預設值為 Fhir</span><span class="sxs-lookup"><span data-stu-id="cb520-149">The default value is Fhir</span></span>

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

### <span data-ttu-id="cb520-150">-位置</span><span class="sxs-lookup"><span data-stu-id="cb520-150">-Location</span></span>
<span data-ttu-id="cb520-151">HealthcareApis 服務位置。</span><span class="sxs-lookup"><span data-stu-id="cb520-151">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="cb520-152">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="cb520-152">-ManagedIdentity</span></span>
<span data-ttu-id="cb520-153">使用受管理的身分識別？</span><span class="sxs-lookup"><span data-stu-id="cb520-153">Use Managed Identity?</span></span>

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

### <span data-ttu-id="cb520-154">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb520-154">-Name</span></span>
<span data-ttu-id="cb520-155">HealthcareApis 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="cb520-155">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="cb520-156">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="cb520-156">-PublicNetworkAccess</span></span>
<span data-ttu-id="cb520-157">Fhir 服務的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="cb520-157">The network access type for Fhir service.</span></span> <span data-ttu-id="cb520-158">通常是 `Enabled` 或 `Disabled` 。</span><span class="sxs-lookup"><span data-stu-id="cb520-158">Commonly `Enabled` or `Disabled`.</span></span>

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

### <span data-ttu-id="cb520-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb520-159">-ResourceGroupName</span></span>
<span data-ttu-id="cb520-160">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="cb520-160">Resource Group Name.</span></span>

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

### <span data-ttu-id="cb520-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="cb520-161">-Tag</span></span>
<span data-ttu-id="cb520-162">HealthcareApis Fhir 服務帳戶標記。</span><span class="sxs-lookup"><span data-stu-id="cb520-162">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="cb520-163">-確認</span><span class="sxs-lookup"><span data-stu-id="cb520-163">-Confirm</span></span>
<span data-ttu-id="cb520-164">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb520-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb520-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb520-165">-WhatIf</span></span>
<span data-ttu-id="cb520-166">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb520-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb520-167">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb520-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb520-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb520-168">CommonParameters</span></span>
<span data-ttu-id="cb520-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb520-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb520-170">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb520-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb520-171">輸入</span><span class="sxs-lookup"><span data-stu-id="cb520-171">INPUTS</span></span>

### <span data-ttu-id="cb520-172">System.object</span><span class="sxs-lookup"><span data-stu-id="cb520-172">System.String</span></span>

## <span data-ttu-id="cb520-173">輸出</span><span class="sxs-lookup"><span data-stu-id="cb520-173">OUTPUTS</span></span>

### <span data-ttu-id="cb520-174">PSHealthcareApisService 中的 HealthcareApis。</span><span class="sxs-lookup"><span data-stu-id="cb520-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="cb520-175">筆記</span><span class="sxs-lookup"><span data-stu-id="cb520-175">NOTES</span></span>

## <span data-ttu-id="cb520-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb520-176">RELATED LINKS</span></span>
