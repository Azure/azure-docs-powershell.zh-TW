---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: f5f8f00a2ab73485b4da6ad6df17ecf526c360bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136373"
---
# <span data-ttu-id="ffa91-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="ffa91-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="ffa91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ffa91-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa91-103">建立服務實例的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ffa91-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="ffa91-104">句法</span><span class="sxs-lookup"><span data-stu-id="ffa91-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-ExportStorageAccountName <String>] [-EnableSmartProxy] [-ManagedIdentity]
 [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffa91-105">說明</span><span class="sxs-lookup"><span data-stu-id="ffa91-105">DESCRIPTION</span></span>
<span data-ttu-id="ffa91-106">建立或更新服務實例的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ffa91-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="ffa91-107">示例</span><span class="sxs-lookup"><span data-stu-id="ffa91-107">EXAMPLES</span></span>

### <span data-ttu-id="ffa91-108">範例1：在資源群組 MyResourceGroup 中，建立一個名為 MyService 的新 Azure healthcareapis fhir 服務，其中 westus2 優惠輸送量 = 400</span><span class="sxs-lookup"><span data-stu-id="ffa91-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput  400

ResourceGroupName Name Location        Kind   CosmosOfferThroughput
----------------- ----------- -------------------------------
MyResourceGroup   MyService   westus2    fhir-R4   400

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

## <span data-ttu-id="ffa91-109">參數</span><span class="sxs-lookup"><span data-stu-id="ffa91-109">PARAMETERS</span></span>

### <span data-ttu-id="ffa91-110">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="ffa91-110">-AccessPolicyObjectId</span></span>
<span data-ttu-id="ffa91-111">存取原則物件識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="ffa91-111">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="ffa91-112">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="ffa91-112">-AllowCorsCredential</span></span>
<span data-ttu-id="ffa91-113">HealthcareApis Fhir Services AllowCorsCredential。</span><span class="sxs-lookup"><span data-stu-id="ffa91-113">HealthcareApis Fhir Service AllowCorsCredential.</span></span>

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

### <span data-ttu-id="ffa91-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffa91-114">-AsJob</span></span>
<span data-ttu-id="ffa91-115">在背景中執行 Cmdlet 作為作業。</span><span class="sxs-lookup"><span data-stu-id="ffa91-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="ffa91-116">-物件</span><span class="sxs-lookup"><span data-stu-id="ffa91-116">-Audience</span></span>
<span data-ttu-id="ffa91-117">HealthcareApis Fhir Services 物件。</span><span class="sxs-lookup"><span data-stu-id="ffa91-117">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="ffa91-118">-頒發機構</span><span class="sxs-lookup"><span data-stu-id="ffa91-118">-Authority</span></span>
<span data-ttu-id="ffa91-119">HealthcareApis [Fhir 服務授權]。</span><span class="sxs-lookup"><span data-stu-id="ffa91-119">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="ffa91-120">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="ffa91-120">-CorsHeader</span></span>
<span data-ttu-id="ffa91-121">HealthcareApis Fhir 服務的 Cors 標頭清單。</span><span class="sxs-lookup"><span data-stu-id="ffa91-121">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="ffa91-122">指定可在要求期間使用的 HTTP 標頭。</span><span class="sxs-lookup"><span data-stu-id="ffa91-122">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="ffa91-123">針對任何標題使用 \*。</span><span class="sxs-lookup"><span data-stu-id="ffa91-123">Use \* for any header.</span></span>

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

### <span data-ttu-id="ffa91-124">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="ffa91-124">-CorsMaxAge</span></span>
<span data-ttu-id="ffa91-125">HealthcareApis Fhir 服務 Cors 最大使用時間。</span><span class="sxs-lookup"><span data-stu-id="ffa91-125">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="ffa91-126">指定要求中的結果可在數秒內緩存多久。</span><span class="sxs-lookup"><span data-stu-id="ffa91-126">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="ffa91-127">範例：600代表10分鐘。</span><span class="sxs-lookup"><span data-stu-id="ffa91-127">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="ffa91-128">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="ffa91-128">-CorsMethod</span></span>
<span data-ttu-id="ffa91-129">HealthcareApis Fhir 服務的 Cors 方法清單。</span><span class="sxs-lookup"><span data-stu-id="ffa91-129">HealthcareApis Fhir Service List of Cors Method.</span></span>

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

### <span data-ttu-id="ffa91-130">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="ffa91-130">-CorsOrigin</span></span>
<span data-ttu-id="ffa91-131">[Cors 來源] 的 HealthcareApis Fhir 服務清單。</span><span class="sxs-lookup"><span data-stu-id="ffa91-131">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="ffa91-132">指定可存取此 API 的來源網站 Url，或使用 \* 以允許來自任何網站的存取權。</span><span class="sxs-lookup"><span data-stu-id="ffa91-132">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="ffa91-133">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="ffa91-133">-CosmosOfferThroughput</span></span>
<span data-ttu-id="ffa91-134">HealthcareApis Fhir Services CosmosOfferThroughput。</span><span class="sxs-lookup"><span data-stu-id="ffa91-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="ffa91-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa91-135">-DefaultProfile</span></span>
<span data-ttu-id="ffa91-136">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ffa91-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffa91-137">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="ffa91-137">-EnableSmartProxy</span></span>
<span data-ttu-id="ffa91-138">HealthcareApis Fhir Services EnableSmartProxy。</span><span class="sxs-lookup"><span data-stu-id="ffa91-138">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="ffa91-139">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ffa91-139">-ExportStorageAccountName</span></span>
<span data-ttu-id="ffa91-140">HealthcareApis Fhir Service 匯出儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ffa91-140">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="ffa91-141">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="ffa91-141">-FhirVersion</span></span>
<span data-ttu-id="ffa91-142">Fhir 版本。</span><span class="sxs-lookup"><span data-stu-id="ffa91-142">Fhir Version.</span></span>

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

### <span data-ttu-id="ffa91-143">類型</span><span class="sxs-lookup"><span data-stu-id="ffa91-143">-Kind</span></span>
<span data-ttu-id="ffa91-144">HealthcareApis 服務的類型。</span><span class="sxs-lookup"><span data-stu-id="ffa91-144">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="ffa91-145">預設值為 Fhir</span><span class="sxs-lookup"><span data-stu-id="ffa91-145">The default value is Fhir</span></span>

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

### <span data-ttu-id="ffa91-146">-位置</span><span class="sxs-lookup"><span data-stu-id="ffa91-146">-Location</span></span>
<span data-ttu-id="ffa91-147">HealthcareApis 服務位置。</span><span class="sxs-lookup"><span data-stu-id="ffa91-147">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="ffa91-148">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="ffa91-148">-ManagedIdentity</span></span>
<span data-ttu-id="ffa91-149">使用受管理的身分識別？</span><span class="sxs-lookup"><span data-stu-id="ffa91-149">Use Managed Identity?</span></span>

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

### <span data-ttu-id="ffa91-150">-名稱</span><span class="sxs-lookup"><span data-stu-id="ffa91-150">-Name</span></span>
<span data-ttu-id="ffa91-151">HealthcareApis 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="ffa91-151">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="ffa91-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa91-152">-ResourceGroupName</span></span>
<span data-ttu-id="ffa91-153">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ffa91-153">Resource Group Name.</span></span>

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

### <span data-ttu-id="ffa91-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="ffa91-154">-Tag</span></span>
<span data-ttu-id="ffa91-155">HealthcareApis Fhir 服務帳戶標記。</span><span class="sxs-lookup"><span data-stu-id="ffa91-155">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="ffa91-156">-確認</span><span class="sxs-lookup"><span data-stu-id="ffa91-156">-Confirm</span></span>
<span data-ttu-id="ffa91-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ffa91-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa91-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa91-158">-WhatIf</span></span>
<span data-ttu-id="ffa91-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ffa91-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa91-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ffa91-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa91-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa91-161">CommonParameters</span></span>
<span data-ttu-id="ffa91-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ffa91-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa91-163">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ffa91-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa91-164">輸入</span><span class="sxs-lookup"><span data-stu-id="ffa91-164">INPUTS</span></span>

### <span data-ttu-id="ffa91-165">System.object</span><span class="sxs-lookup"><span data-stu-id="ffa91-165">System.String</span></span>

## <span data-ttu-id="ffa91-166">輸出</span><span class="sxs-lookup"><span data-stu-id="ffa91-166">OUTPUTS</span></span>

### <span data-ttu-id="ffa91-167">PSHealthcareApisService 中的 HealthcareApisService。</span><span class="sxs-lookup"><span data-stu-id="ffa91-167">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="ffa91-168">筆記</span><span class="sxs-lookup"><span data-stu-id="ffa91-168">NOTES</span></span>

## <span data-ttu-id="ffa91-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffa91-169">RELATED LINKS</span></span>
