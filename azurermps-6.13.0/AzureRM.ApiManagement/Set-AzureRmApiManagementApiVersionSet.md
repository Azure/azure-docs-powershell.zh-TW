---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 5d9bc89eb2d4188b7b2903bee7a8b0a44bec1216
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450339"
---
# <span data-ttu-id="74269-101">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="74269-101">Set-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="74269-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74269-102">SYNOPSIS</span></span>
<span data-ttu-id="74269-103">更新 API 管理內容中設定的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="74269-103">Updates an API Version Set in the API Management Context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74269-104">句法</span><span class="sxs-lookup"><span data-stu-id="74269-104">SYNTAX</span></span>

### <span data-ttu-id="74269-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="74269-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-Name <String>] [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74269-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="74269-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74269-107">說明</span><span class="sxs-lookup"><span data-stu-id="74269-107">DESCRIPTION</span></span>

<span data-ttu-id="74269-108">**AzureRmApiManagementApiVersionSet** Cmdlet 會修改 Azure API 管理 API 版本設定。</span><span class="sxs-lookup"><span data-stu-id="74269-108">The **Set-AzureRmApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="74269-109">示例</span><span class="sxs-lookup"><span data-stu-id="74269-109">EXAMPLES</span></span>

### <span data-ttu-id="74269-110">範例1</span><span class="sxs-lookup"><span data-stu-id="74269-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="74269-111">這個命令會更新現有的 API 版本集與版本設定配置 `Header` 和標頭參數 `api-version` 。</span><span class="sxs-lookup"><span data-stu-id="74269-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="74269-112">參數</span><span class="sxs-lookup"><span data-stu-id="74269-112">PARAMETERS</span></span>

### <span data-ttu-id="74269-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="74269-113">-ApiVersionSetId</span></span>
<span data-ttu-id="74269-114">新 API 版本集的識別碼。</span><span class="sxs-lookup"><span data-stu-id="74269-114">Identifier for new API Version Set.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74269-115">-內容</span><span class="sxs-lookup"><span data-stu-id="74269-115">-Context</span></span>
<span data-ttu-id="74269-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="74269-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="74269-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="74269-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74269-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74269-118">-DefaultProfile</span></span>
<span data-ttu-id="74269-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74269-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74269-120">-描述</span><span class="sxs-lookup"><span data-stu-id="74269-120">-Description</span></span>
<span data-ttu-id="74269-121">Api 版本集的描述。</span><span class="sxs-lookup"><span data-stu-id="74269-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="74269-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="74269-122">-HeaderName</span></span>
<span data-ttu-id="74269-123">將包含版本設定資訊的標頭值。</span><span class="sxs-lookup"><span data-stu-id="74269-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="74269-124">如果您已選取 [版本配置] 標題，則必須指定此值。</span><span class="sxs-lookup"><span data-stu-id="74269-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="74269-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74269-125">-InputObject</span></span>
<span data-ttu-id="74269-126">PsApiManagementApiVersionSet 的實例。</span><span class="sxs-lookup"><span data-stu-id="74269-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="74269-127">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="74269-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74269-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="74269-128">-Name</span></span>
<span data-ttu-id="74269-129">ApiVersion 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="74269-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="74269-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="74269-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="74269-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74269-131">-PassThru</span></span>
<span data-ttu-id="74269-132">如果已指定，則會將代表已修改之 apiVersionSet 的 PsApiManagementApiVersionSet 類型的 ServiceManagement 類型 ApiManagement 寫入輸出。</span><span class="sxs-lookup"><span data-stu-id="74269-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="74269-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="74269-133">-QueryName</span></span>
<span data-ttu-id="74269-134">會包含版本設定資訊的查詢值。</span><span class="sxs-lookup"><span data-stu-id="74269-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="74269-135">如果是 [選取版本配置] 查詢，則必須指定此值。</span><span class="sxs-lookup"><span data-stu-id="74269-135">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="74269-136">-配置</span><span class="sxs-lookup"><span data-stu-id="74269-136">-Scheme</span></span>
<span data-ttu-id="74269-137">針對 Api 版本設定選取的版本設定配置。</span><span class="sxs-lookup"><span data-stu-id="74269-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="74269-138">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="74269-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74269-139">-確認</span><span class="sxs-lookup"><span data-stu-id="74269-139">-Confirm</span></span>
<span data-ttu-id="74269-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74269-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74269-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74269-141">-WhatIf</span></span>
<span data-ttu-id="74269-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74269-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74269-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74269-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74269-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74269-144">CommonParameters</span></span>
<span data-ttu-id="74269-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74269-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74269-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74269-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74269-147">輸入</span><span class="sxs-lookup"><span data-stu-id="74269-147">INPUTS</span></span>

### <span data-ttu-id="74269-148">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="74269-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="74269-149">ServiceManagement. PsApiManagementApiVersionSet （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="74269-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="74269-150">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="74269-150">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="74269-151">System.object</span><span class="sxs-lookup"><span data-stu-id="74269-151">System.String</span></span>

### <span data-ttu-id="74269-152">ServiceManagement. PsApiManagementVersioningScheme （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="74269-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="74269-153">輸出</span><span class="sxs-lookup"><span data-stu-id="74269-153">OUTPUTS</span></span>

### <span data-ttu-id="74269-154">ServiceManagement. PsApiManagementApiVersionSet （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="74269-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="74269-155">筆記</span><span class="sxs-lookup"><span data-stu-id="74269-155">NOTES</span></span>

## <span data-ttu-id="74269-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="74269-156">RELATED LINKS</span></span>

[<span data-ttu-id="74269-157">AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="74269-157">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="74269-158">新-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="74269-158">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="74269-159">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="74269-159">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
