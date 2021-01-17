---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 0e007634659d842b0c59712a2ee191a79e1aeb58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447483"
---
# <span data-ttu-id="c6077-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c6077-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="c6077-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6077-102">SYNOPSIS</span></span>
<span data-ttu-id="c6077-103">建立 API 版本集合。</span><span class="sxs-lookup"><span data-stu-id="c6077-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="c6077-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6077-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6077-105">說明</span><span class="sxs-lookup"><span data-stu-id="c6077-105">DESCRIPTION</span></span>
<span data-ttu-id="c6077-106">**新的-AzApiManagementApiVersionSet** Cmdlet 會在 Azure API 管理內容中建立 API 版本設定實體。</span><span class="sxs-lookup"><span data-stu-id="c6077-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="c6077-107">示例</span><span class="sxs-lookup"><span data-stu-id="c6077-107">EXAMPLES</span></span>

### <span data-ttu-id="c6077-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c6077-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

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

<span data-ttu-id="c6077-109">這個命令會建立 API 版本設定的版本配置 `Query` 和查詢參數 `api-version` 。</span><span class="sxs-lookup"><span data-stu-id="c6077-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="c6077-110">參數</span><span class="sxs-lookup"><span data-stu-id="c6077-110">PARAMETERS</span></span>

### <span data-ttu-id="c6077-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="c6077-111">-ApiVersionSetId</span></span>
<span data-ttu-id="c6077-112">新 API 版本集的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6077-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="c6077-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="c6077-113">This parameter is optional.</span></span>
<span data-ttu-id="c6077-114">如果未指定，將會產生識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6077-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="c6077-115">-內容</span><span class="sxs-lookup"><span data-stu-id="c6077-115">-Context</span></span>
<span data-ttu-id="c6077-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="c6077-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c6077-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="c6077-117">This parameter is required.</span></span>

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

### <span data-ttu-id="c6077-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6077-118">-DefaultProfile</span></span>
<span data-ttu-id="c6077-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6077-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6077-120">-描述</span><span class="sxs-lookup"><span data-stu-id="c6077-120">-Description</span></span>
<span data-ttu-id="c6077-121">Api 版本集的描述。</span><span class="sxs-lookup"><span data-stu-id="c6077-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="c6077-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="c6077-122">-HeaderName</span></span>
<span data-ttu-id="c6077-123">將包含版本設定資訊的標頭值。</span><span class="sxs-lookup"><span data-stu-id="c6077-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="c6077-124">如果選擇 [版本配置] 標題，則必須指定此值。</span><span class="sxs-lookup"><span data-stu-id="c6077-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="c6077-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6077-125">-Name</span></span>
<span data-ttu-id="c6077-126">ApiVersion 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6077-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="c6077-127">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="c6077-127">This parameter is required.</span></span>

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

### <span data-ttu-id="c6077-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="c6077-128">-QueryName</span></span>
<span data-ttu-id="c6077-129">會包含版本設定資訊的查詢值。</span><span class="sxs-lookup"><span data-stu-id="c6077-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="c6077-130">如果選擇 [版本設定模式] 查詢，則必須指定此值。</span><span class="sxs-lookup"><span data-stu-id="c6077-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="c6077-131">-配置</span><span class="sxs-lookup"><span data-stu-id="c6077-131">-Scheme</span></span>
<span data-ttu-id="c6077-132">針對 Api 版本設定選取的版本設定配置。</span><span class="sxs-lookup"><span data-stu-id="c6077-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="c6077-133">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="c6077-133">This parameter is required.</span></span>

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

### <span data-ttu-id="c6077-134">-確認</span><span class="sxs-lookup"><span data-stu-id="c6077-134">-Confirm</span></span>
<span data-ttu-id="c6077-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c6077-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6077-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6077-136">-WhatIf</span></span>
<span data-ttu-id="c6077-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6077-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6077-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6077-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6077-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6077-139">CommonParameters</span></span>
<span data-ttu-id="c6077-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6077-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6077-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c6077-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6077-142">輸入</span><span class="sxs-lookup"><span data-stu-id="c6077-142">INPUTS</span></span>

### <span data-ttu-id="c6077-143">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="c6077-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c6077-144">System.object</span><span class="sxs-lookup"><span data-stu-id="c6077-144">System.String</span></span>

### <span data-ttu-id="c6077-145">ServiceManagement. PsApiManagementVersioningScheme （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="c6077-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="c6077-146">輸出</span><span class="sxs-lookup"><span data-stu-id="c6077-146">OUTPUTS</span></span>

### <span data-ttu-id="c6077-147">ServiceManagement. PsApiManagementApiVersionSet （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="c6077-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="c6077-148">筆記</span><span class="sxs-lookup"><span data-stu-id="c6077-148">NOTES</span></span>

## <span data-ttu-id="c6077-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6077-149">RELATED LINKS</span></span>

[<span data-ttu-id="c6077-150">AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c6077-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="c6077-151">移除-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c6077-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="c6077-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c6077-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)