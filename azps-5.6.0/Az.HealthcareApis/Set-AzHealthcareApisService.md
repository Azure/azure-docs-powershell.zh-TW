---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: 2ff0f9f03524368e01b6edbcad5b8db8fef4fb21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917213"
---
# <span data-ttu-id="3b40d-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="3b40d-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="3b40d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3b40d-102">SYNOPSIS</span></span>
<span data-ttu-id="3b40d-103">更新現有的醫療保健發票服務。</span><span class="sxs-lookup"><span data-stu-id="3b40d-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="3b40d-104">語法</span><span class="sxs-lookup"><span data-stu-id="3b40d-104">SYNTAX</span></span>

### <span data-ttu-id="3b40d-105">ServiceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3b40d-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-CosmosKeyVaultKeyUri <String>] [-Authority <String>] [-Audience <String>] [-EnableSmartProxy]
 [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>] [-CorsMethod <String[]>]
 [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential] [-ExportStorageAccountName <String>]
 [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>]
 [-AsJob] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b40d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b40d-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b40d-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b40d-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b40d-108">描述</span><span class="sxs-lookup"><span data-stu-id="3b40d-108">DESCRIPTION</span></span>
<span data-ttu-id="3b40d-109">更新現有的醫療保健發票服務。</span><span class="sxs-lookup"><span data-stu-id="3b40d-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="3b40d-110">例子</span><span class="sxs-lookup"><span data-stu-id="3b40d-110">EXAMPLES</span></span>

### <span data-ttu-id="3b40d-111">範例 1：使用db OfferThroughput = 500 更新資源群組 MyResourceGroup 中名為 MyService 的現有醫療保健apis 服務。</span><span class="sxs-lookup"><span data-stu-id="3b40d-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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
CosmosKeyVaultKeyUri    : 
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

### <span data-ttu-id="3b40d-112">範例 2：更新資源群組 MyResourceGroup 中名為 MyService 的現有醫療保健 apis 服務，其為HTTPs:// \<my-keyvault> \<my-key> .vault.azure.net/keys/"</span><span class="sxs-lookup"><span data-stu-id="3b40d-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosKeyVaultKeyUri    : https://<my-keyvault>.vault.azure.net/keys/<my-key>
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

## <span data-ttu-id="3b40d-113">參數</span><span class="sxs-lookup"><span data-stu-id="3b40d-113">PARAMETERS</span></span>

### <span data-ttu-id="3b40d-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="3b40d-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="3b40d-115">Access Policy Object ID 清單。</span><span class="sxs-lookup"><span data-stu-id="3b40d-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="3b40d-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="3b40d-116">-AllowCorsCredential</span></span>
<span data-ttu-id="3b40d-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="3b40d-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="3b40d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b40d-118">-AsJob</span></span>
<span data-ttu-id="3b40d-119">在背景中以工作執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b40d-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="3b40d-120">-物件</span><span class="sxs-lookup"><span data-stu-id="3b40d-120">-Audience</span></span>
<span data-ttu-id="3b40d-121">醫療保健 Apis FhirService 物件。</span><span class="sxs-lookup"><span data-stu-id="3b40d-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="3b40d-122">-授權</span><span class="sxs-lookup"><span data-stu-id="3b40d-122">-Authority</span></span>
<span data-ttu-id="3b40d-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="3b40d-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="3b40d-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="3b40d-124">-CorsHeader</span></span>
<span data-ttu-id="3b40d-125">HealthcareApis FhirService List of Cors Headers.</span><span class="sxs-lookup"><span data-stu-id="3b40d-125">HealthcareApis FhirService List of Cors Headers.</span></span>
<span data-ttu-id="3b40d-126">指定可在要求期間使用的 HTTP 標頭。</span><span class="sxs-lookup"><span data-stu-id="3b40d-126">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="3b40d-127">將 " \* " 用於任何頁眉。</span><span class="sxs-lookup"><span data-stu-id="3b40d-127">Use " \* " for any header.</span></span>

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

### <span data-ttu-id="3b40d-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="3b40d-128">-CorsMaxAge</span></span>
<span data-ttu-id="3b40d-129">HealthcareApis FhirService Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="3b40d-129">HealthcareApis FhirService Cors Max Age.</span></span>
<span data-ttu-id="3b40d-130">指定要求的結果可以以秒數進行緩存多久。</span><span class="sxs-lookup"><span data-stu-id="3b40d-130">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="3b40d-131">範例：600 表示 10 分鐘。</span><span class="sxs-lookup"><span data-stu-id="3b40d-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="3b40d-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="3b40d-132">-CorsMethod</span></span>
<span data-ttu-id="3b40d-133">HealthcareApis FhirService List of Cors Methods.</span><span class="sxs-lookup"><span data-stu-id="3b40d-133">HealthcareApis FhirService List of Cors Methods.</span></span>

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

### <span data-ttu-id="3b40d-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="3b40d-134">-CorsOrigin</span></span>
<span data-ttu-id="3b40d-135">HealthcareApis FhirService List of Cors Origins.</span><span class="sxs-lookup"><span data-stu-id="3b40d-135">HealthcareApis FhirService List of Cors Origins.</span></span>
<span data-ttu-id="3b40d-136">指定可存取此 API 的來源網站的 URL，或使用 " \* " 允許從任何網站存取。</span><span class="sxs-lookup"><span data-stu-id="3b40d-136">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

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

### <span data-ttu-id="3b40d-137">-外星KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="3b40d-137">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="3b40d-138">HealthcareApis Fhir ServiceAultsKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="3b40d-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="3b40d-139">支援資料庫之客戶管理金鑰的 URI。</span><span class="sxs-lookup"><span data-stu-id="3b40d-139">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="3b40d-140">-一些高能專案</span><span class="sxs-lookup"><span data-stu-id="3b40d-140">-CosmosOfferThroughput</span></span>
<span data-ttu-id="3b40d-141">HealthcareApis FhirServiceServiceServiceOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="3b40d-141">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="3b40d-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b40d-142">-DefaultProfile</span></span>
<span data-ttu-id="3b40d-143">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b40d-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b40d-144">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="3b40d-144">-DisableCorsCredential</span></span>
<span data-ttu-id="3b40d-145">HealthcareApis FhirService CorsCredentials Not alloweds.</span><span class="sxs-lookup"><span data-stu-id="3b40d-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="3b40d-146">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="3b40d-146">-DisableManagedIdentity</span></span>
<span data-ttu-id="3b40d-147">停用受管理身分識別。</span><span class="sxs-lookup"><span data-stu-id="3b40d-147">Disable Managed Identity.</span></span>

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

### <span data-ttu-id="3b40d-148">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="3b40d-148">-DisableSmartProxy</span></span>
<span data-ttu-id="3b40d-149">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="3b40d-149">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="3b40d-150">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="3b40d-150">-EnableManagedIdentity</span></span>
<span data-ttu-id="3b40d-151">啟用受管理身分識別。</span><span class="sxs-lookup"><span data-stu-id="3b40d-151">Enable Managed Identity.</span></span>

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

### <span data-ttu-id="3b40d-152">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="3b40d-152">-EnableSmartProxy</span></span>
<span data-ttu-id="3b40d-153">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="3b40d-153">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="3b40d-154">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3b40d-154">-ExportStorageAccountName</span></span>
<span data-ttu-id="3b40d-155">HealthcareApis Fhir Service 匯出儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3b40d-155">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="3b40d-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b40d-156">-InputObject</span></span>
<span data-ttu-id="3b40d-157">來自 Get-AzHealthcareApisFhirService 的 HealthcareApis fhirService 服務。</span><span class="sxs-lookup"><span data-stu-id="3b40d-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="3b40d-158">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b40d-158">-Name</span></span>
<span data-ttu-id="3b40d-159">醫療保健發票服務名稱。</span><span class="sxs-lookup"><span data-stu-id="3b40d-159">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="3b40d-160">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="3b40d-160">-PublicNetworkAccess</span></span>
<span data-ttu-id="3b40d-161">Fhir 服務的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="3b40d-161">The network access type for Fhir service.</span></span> <span data-ttu-id="3b40d-162">一般 `Enabled` 或 `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="3b40d-162">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b40d-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b40d-163">-ResourceGroupName</span></span>
<span data-ttu-id="3b40d-164">醫療保健發票服務資源組名。</span><span class="sxs-lookup"><span data-stu-id="3b40d-164">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="3b40d-165">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b40d-165">-ResourceId</span></span>
<span data-ttu-id="3b40d-166">HealthcareApis Fhir Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="3b40d-166">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="3b40d-167">-標記</span><span class="sxs-lookup"><span data-stu-id="3b40d-167">-Tag</span></span>
<span data-ttu-id="3b40d-168">HealthcareApis Fhir Service 帳戶標記。</span><span class="sxs-lookup"><span data-stu-id="3b40d-168">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="3b40d-169">-確認</span><span class="sxs-lookup"><span data-stu-id="3b40d-169">-Confirm</span></span>
<span data-ttu-id="3b40d-170">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3b40d-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b40d-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b40d-171">-WhatIf</span></span>
<span data-ttu-id="3b40d-172">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3b40d-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b40d-173">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b40d-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b40d-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b40d-174">CommonParameters</span></span>
<span data-ttu-id="3b40d-175">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3b40d-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b40d-176">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b40d-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b40d-177">輸入</span><span class="sxs-lookup"><span data-stu-id="3b40d-177">INPUTS</span></span>

### <span data-ttu-id="3b40d-178">Microsoft.Azure.Commands.HealthcareApis.models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="3b40d-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="3b40d-179">System.String</span><span class="sxs-lookup"><span data-stu-id="3b40d-179">System.String</span></span>

## <span data-ttu-id="3b40d-180">輸出</span><span class="sxs-lookup"><span data-stu-id="3b40d-180">OUTPUTS</span></span>

### <span data-ttu-id="3b40d-181">Microsoft.Azure.Commands.HealthcareApis.models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="3b40d-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="3b40d-182">筆記</span><span class="sxs-lookup"><span data-stu-id="3b40d-182">NOTES</span></span>

## <span data-ttu-id="3b40d-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b40d-183">RELATED LINKS</span></span>
