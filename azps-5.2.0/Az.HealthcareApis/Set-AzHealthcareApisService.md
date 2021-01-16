---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: c8eb7c58300e3252422d8b599422a3a14eb5c1fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277580"
---
# <span data-ttu-id="9d5e8-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="9d5e8-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="9d5e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5e8-103">更新現有的 healthcareApis fhir 服務。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="9d5e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d5e8-104">SYNTAX</span></span>

### <span data-ttu-id="9d5e8-105">ServiceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9d5e8-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-CosmosKeyVaultKeyUri <String>] [-Authority <String>] [-Audience <String>] [-EnableSmartProxy]
 [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>] [-CorsMethod <String[]>]
 [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential] [-ExportStorageAccountName <String>]
 [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>]
 [-AsJob] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d5e8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d5e8-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d5e8-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d5e8-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d5e8-108">說明</span><span class="sxs-lookup"><span data-stu-id="9d5e8-108">DESCRIPTION</span></span>
<span data-ttu-id="9d5e8-109">更新現有的 healthcareApis fhir 服務。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="9d5e8-110">示例</span><span class="sxs-lookup"><span data-stu-id="9d5e8-110">EXAMPLES</span></span>

### <span data-ttu-id="9d5e8-111">範例1：使用 cosmosdb OfferThroughput = 500 更新資源群組 MyResourceGroup 中名為 MyService 的現有 healthcareapis 服務。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

### <span data-ttu-id="9d5e8-112">範例2：使用 cosmosdb OfferThroughput = 500 和主要保存庫金鑰 uri "HTTPs://"，更新資源群組 MyResourceGroup 中名為 MyService 的現有 healthcareapis 服務 \<my-keyvault> 。 \<my-key></span><span class="sxs-lookup"><span data-stu-id="9d5e8-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>

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

## <span data-ttu-id="9d5e8-113">參數</span><span class="sxs-lookup"><span data-stu-id="9d5e8-113">PARAMETERS</span></span>

### <span data-ttu-id="9d5e8-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="9d5e8-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="9d5e8-115">存取原則物件識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="9d5e8-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="9d5e8-116">-AllowCorsCredential</span></span>
<span data-ttu-id="9d5e8-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="9d5e8-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="9d5e8-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d5e8-118">-AsJob</span></span>
<span data-ttu-id="9d5e8-119">在背景中執行 Cmdlet 作為作業。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="9d5e8-120">-物件</span><span class="sxs-lookup"><span data-stu-id="9d5e8-120">-Audience</span></span>
<span data-ttu-id="9d5e8-121">HealthcareApis FhirService 物件。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="9d5e8-122">-頒發機構</span><span class="sxs-lookup"><span data-stu-id="9d5e8-122">-Authority</span></span>
<span data-ttu-id="9d5e8-123">HealthcareApis [FhirService 機關]。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="9d5e8-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="9d5e8-124">-CorsHeader</span></span>
<span data-ttu-id="9d5e8-125">[Cors] 標題的 HealthcareApis FhirService 清單。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-125">HealthcareApis FhirService List of Cors Headers.</span></span>
<span data-ttu-id="9d5e8-126">指定可在要求期間使用的 HTTP 標頭。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-126">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="9d5e8-127">針對任何標題使用 "\*"。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-127">Use " \* " for any header.</span></span>

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

### <span data-ttu-id="9d5e8-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="9d5e8-128">-CorsMaxAge</span></span>
<span data-ttu-id="9d5e8-129">HealthcareApis FhirService Cors 最大使用時間。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-129">HealthcareApis FhirService Cors Max Age.</span></span>
<span data-ttu-id="9d5e8-130">指定要求中的結果可在數秒內緩存多久。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-130">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="9d5e8-131">範例：600代表10分鐘。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="9d5e8-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="9d5e8-132">-CorsMethod</span></span>
<span data-ttu-id="9d5e8-133">HealthcareApis FhirService 的 Cors 方法清單。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-133">HealthcareApis FhirService List of Cors Methods.</span></span>

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

### <span data-ttu-id="9d5e8-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="9d5e8-134">-CorsOrigin</span></span>
<span data-ttu-id="9d5e8-135">[Cors 來源] 的 HealthcareApis FhirService 清單。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-135">HealthcareApis FhirService List of Cors Origins.</span></span>
<span data-ttu-id="9d5e8-136">指定可存取此 API 的來源網站 Url，或使用 "\*" 允許來自任何網站的存取權。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-136">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

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

### <span data-ttu-id="9d5e8-137">-CosmosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="9d5e8-137">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="9d5e8-138">HealthcareApis Fhir Services CosmosKeyVaultKeyUri。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="9d5e8-139">後備資料庫的客戶管理金鑰的 URI。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-139">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="9d5e8-140">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="9d5e8-140">-CosmosOfferThroughput</span></span>
<span data-ttu-id="9d5e8-141">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="9d5e8-141">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="9d5e8-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d5e8-142">-DefaultProfile</span></span>
<span data-ttu-id="9d5e8-143">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d5e8-144">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="9d5e8-144">-DisableCorsCredential</span></span>
<span data-ttu-id="9d5e8-145">不允許 HealthcareApis FhirService CorsCredentials。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="9d5e8-146">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="9d5e8-146">-DisableManagedIdentity</span></span>
<span data-ttu-id="9d5e8-147">停用受管理的身分識別。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-147">Disable Managed Identity.</span></span>

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

### <span data-ttu-id="9d5e8-148">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="9d5e8-148">-DisableSmartProxy</span></span>
<span data-ttu-id="9d5e8-149">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="9d5e8-149">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="9d5e8-150">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="9d5e8-150">-EnableManagedIdentity</span></span>
<span data-ttu-id="9d5e8-151">啟用受管理的身分識別。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-151">Enable Managed Identity.</span></span>

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

### <span data-ttu-id="9d5e8-152">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="9d5e8-152">-EnableSmartProxy</span></span>
<span data-ttu-id="9d5e8-153">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="9d5e8-153">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="9d5e8-154">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9d5e8-154">-ExportStorageAccountName</span></span>
<span data-ttu-id="9d5e8-155">HealthcareApis Fhir Service 匯出儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-155">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="9d5e8-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d5e8-156">-InputObject</span></span>
<span data-ttu-id="9d5e8-157">從 AzHealthcareApisFhirService HealthcareApis fhir service 輸送管道。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="9d5e8-158">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d5e8-158">-Name</span></span>
<span data-ttu-id="9d5e8-159">HealthcareApis 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-159">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="9d5e8-160">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="9d5e8-160">-PublicNetworkAccess</span></span>
<span data-ttu-id="9d5e8-161">Fhir 服務的網路存取類型。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-161">The network access type for Fhir service.</span></span> <span data-ttu-id="9d5e8-162">通常是 `Enabled` 或 `Disabled` 。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-162">Commonly `Enabled` or `Disabled`.</span></span>

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

### <span data-ttu-id="9d5e8-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d5e8-163">-ResourceGroupName</span></span>
<span data-ttu-id="9d5e8-164">HealthcareApis 服務資源組名。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-164">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="9d5e8-165">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d5e8-165">-ResourceId</span></span>
<span data-ttu-id="9d5e8-166">HealthcareApis Fhir Service ResourceId。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-166">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="9d5e8-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="9d5e8-167">-Tag</span></span>
<span data-ttu-id="9d5e8-168">HealthcareApis Fhir 服務帳戶標記。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-168">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="9d5e8-169">-確認</span><span class="sxs-lookup"><span data-stu-id="9d5e8-169">-Confirm</span></span>
<span data-ttu-id="9d5e8-170">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d5e8-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d5e8-171">-WhatIf</span></span>
<span data-ttu-id="9d5e8-172">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d5e8-173">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d5e8-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5e8-174">CommonParameters</span></span>
<span data-ttu-id="9d5e8-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5e8-176">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5e8-177">輸入</span><span class="sxs-lookup"><span data-stu-id="9d5e8-177">INPUTS</span></span>

### <span data-ttu-id="9d5e8-178">PSHealthcareApisService 中的 HealthcareApis。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="9d5e8-179">System.object</span><span class="sxs-lookup"><span data-stu-id="9d5e8-179">System.String</span></span>

## <span data-ttu-id="9d5e8-180">輸出</span><span class="sxs-lookup"><span data-stu-id="9d5e8-180">OUTPUTS</span></span>

### <span data-ttu-id="9d5e8-181">PSHealthcareApisService 中的 HealthcareApis。</span><span class="sxs-lookup"><span data-stu-id="9d5e8-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="9d5e8-182">筆記</span><span class="sxs-lookup"><span data-stu-id="9d5e8-182">NOTES</span></span>

## <span data-ttu-id="9d5e8-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d5e8-183">RELATED LINKS</span></span>
