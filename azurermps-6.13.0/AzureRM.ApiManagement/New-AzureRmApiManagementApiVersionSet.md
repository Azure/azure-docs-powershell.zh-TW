---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: e10b91994bdb7351a7154d04cb7de3231ed87a5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447528"
---
# <span data-ttu-id="e3528-101">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e3528-101">New-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="e3528-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3528-102">SYNOPSIS</span></span>
<span data-ttu-id="e3528-103">建立 API 版本集合。</span><span class="sxs-lookup"><span data-stu-id="e3528-103">Creates an API Version Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3528-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3528-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -Name <String> -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3528-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3528-105">DESCRIPTION</span></span>
<span data-ttu-id="e3528-106">**新的-AzureRmApiManagementApiVersionSet** Cmdlet 會在 Azure API 管理內容中建立 API 版本設定實體。</span><span class="sxs-lookup"><span data-stu-id="e3528-106">The **New-AzureRmApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="e3528-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3528-107">EXAMPLES</span></span>

### <span data-ttu-id="e3528-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e3528-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

ApiVersionSetId   : ea9a87cd-a699-4a75-bf7d-909846b91268
Description       : version by xmsversion
VersionQueryName  :
VersionHeaderName : x-ms-version
DisplayName       : newversion
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/ea9a87cd-a699-4a75-bf7d-909846b91268
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="e3528-109">這個命令會建立 API 版本設定的版本配置 `Query` 和查詢參數 `api-version` 。</span><span class="sxs-lookup"><span data-stu-id="e3528-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="e3528-110">參數</span><span class="sxs-lookup"><span data-stu-id="e3528-110">PARAMETERS</span></span>

### <span data-ttu-id="e3528-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="e3528-111">-ApiVersionSetId</span></span>
<span data-ttu-id="e3528-112">新 API 版本集的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3528-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="e3528-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="e3528-113">This parameter is optional.</span></span>
<span data-ttu-id="e3528-114">如果未指定，將會產生識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3528-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="e3528-115">-內容</span><span class="sxs-lookup"><span data-stu-id="e3528-115">-Context</span></span>
<span data-ttu-id="e3528-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="e3528-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e3528-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e3528-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3528-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3528-118">-DefaultProfile</span></span>
<span data-ttu-id="e3528-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3528-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3528-120">-描述</span><span class="sxs-lookup"><span data-stu-id="e3528-120">-Description</span></span>
<span data-ttu-id="e3528-121">Api 版本集的描述。</span><span class="sxs-lookup"><span data-stu-id="e3528-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="e3528-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="e3528-122">-HeaderName</span></span>
<span data-ttu-id="e3528-123">將包含版本設定資訊的標頭值。</span><span class="sxs-lookup"><span data-stu-id="e3528-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="e3528-124">如果您已選取 [版本配置] 標題，則必須指定此值。</span><span class="sxs-lookup"><span data-stu-id="e3528-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="e3528-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3528-125">-Name</span></span>
<span data-ttu-id="e3528-126">ApiVersion 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3528-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="e3528-127">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e3528-127">This parameter is required.</span></span>

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

### <span data-ttu-id="e3528-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="e3528-128">-QueryName</span></span>
<span data-ttu-id="e3528-129">會包含版本設定資訊的查詢值。</span><span class="sxs-lookup"><span data-stu-id="e3528-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="e3528-130">如果是 [選取版本配置] 查詢，則必須指定此值。</span><span class="sxs-lookup"><span data-stu-id="e3528-130">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="e3528-131">-配置</span><span class="sxs-lookup"><span data-stu-id="e3528-131">-Scheme</span></span>
<span data-ttu-id="e3528-132">針對 Api 版本設定選取的版本設定配置。</span><span class="sxs-lookup"><span data-stu-id="e3528-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="e3528-133">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e3528-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3528-134">-確認</span><span class="sxs-lookup"><span data-stu-id="e3528-134">-Confirm</span></span>
<span data-ttu-id="e3528-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3528-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3528-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3528-136">-WhatIf</span></span>
<span data-ttu-id="e3528-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3528-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3528-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3528-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3528-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3528-139">CommonParameters</span></span>
<span data-ttu-id="e3528-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3528-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3528-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3528-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3528-142">輸入</span><span class="sxs-lookup"><span data-stu-id="e3528-142">INPUTS</span></span>

### <span data-ttu-id="e3528-143">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e3528-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="e3528-144">參數：內容 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e3528-144">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="e3528-145">System.object</span><span class="sxs-lookup"><span data-stu-id="e3528-145">System.String</span></span>

### <span data-ttu-id="e3528-146">ServiceManagement. PsApiManagementVersioningScheme （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e3528-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="e3528-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e3528-147">OUTPUTS</span></span>

### <span data-ttu-id="e3528-148">ServiceManagement. PsApiManagementApiVersionSet （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e3528-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="e3528-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e3528-149">NOTES</span></span>

## <span data-ttu-id="e3528-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3528-150">RELATED LINKS</span></span>

[<span data-ttu-id="e3528-151">AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e3528-151">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="e3528-152">移除-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e3528-152">Remove-AzureRmApiManagementApiVersionSet</span></span>](./Remove-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="e3528-153">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e3528-153">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
