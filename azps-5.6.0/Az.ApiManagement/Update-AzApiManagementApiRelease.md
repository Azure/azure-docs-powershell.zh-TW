---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 16c73a389e6602999272255534312928fc4a13f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908657"
---
# <span data-ttu-id="414df-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="414df-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="414df-102">簡介</span><span class="sxs-lookup"><span data-stu-id="414df-102">SYNOPSIS</span></span>
<span data-ttu-id="414df-103">更新特定的 Api 版本。</span><span class="sxs-lookup"><span data-stu-id="414df-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="414df-104">語法</span><span class="sxs-lookup"><span data-stu-id="414df-104">SYNTAX</span></span>

### <span data-ttu-id="414df-105">展開Parameter (預設) </span><span class="sxs-lookup"><span data-stu-id="414df-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="414df-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="414df-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="414df-107">描述</span><span class="sxs-lookup"><span data-stu-id="414df-107">DESCRIPTION</span></span>
<span data-ttu-id="414df-108">**Update-AzApiManagementApiRelease** Cmdlet 會修改 Azure API 管理 API 版本。</span><span class="sxs-lookup"><span data-stu-id="414df-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="414df-109">例子</span><span class="sxs-lookup"><span data-stu-id="414df-109">EXAMPLES</span></span>

### <span data-ttu-id="414df-110">範例 1：更新 API 修訂的 API 版本</span><span class="sxs-lookup"><span data-stu-id="414df-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="414df-111">此命令會以 `echo-api-release` 新的附注更新 API 的 API `echo-api` 版本。</span><span class="sxs-lookup"><span data-stu-id="414df-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="414df-112">參數</span><span class="sxs-lookup"><span data-stu-id="414df-112">PARAMETERS</span></span>

### <span data-ttu-id="414df-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="414df-113">-ApiId</span></span>
<span data-ttu-id="414df-114">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="414df-114">Identifier of existing API.</span></span>
<span data-ttu-id="414df-115">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="414df-115">This parameter is required.</span></span>

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

### <span data-ttu-id="414df-116">-內容</span><span class="sxs-lookup"><span data-stu-id="414df-116">-Context</span></span>
<span data-ttu-id="414df-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="414df-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="414df-118">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="414df-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="414df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="414df-119">-DefaultProfile</span></span>
<span data-ttu-id="414df-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="414df-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="414df-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="414df-121">-InputObject</span></span>
<span data-ttu-id="414df-122">類型為 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiRelease 的實例。</span><span class="sxs-lookup"><span data-stu-id="414df-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="414df-123">-注意</span><span class="sxs-lookup"><span data-stu-id="414df-123">-Note</span></span>
<span data-ttu-id="414df-124">Api 版本資訊。</span><span class="sxs-lookup"><span data-stu-id="414df-124">Api Release Notes.</span></span>
<span data-ttu-id="414df-125">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="414df-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="414df-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="414df-126">-PassThru</span></span>
<span data-ttu-id="414df-127">如果指定的話，代表已設定 API 發行之 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease 類型的實例。</span><span class="sxs-lookup"><span data-stu-id="414df-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="414df-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="414df-128">-ReleaseId</span></span>
<span data-ttu-id="414df-129">Api 修訂版本識別碼。</span><span class="sxs-lookup"><span data-stu-id="414df-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="414df-130">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="414df-130">This parameter is required.</span></span>

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

### <span data-ttu-id="414df-131">-確認</span><span class="sxs-lookup"><span data-stu-id="414df-131">-Confirm</span></span>
<span data-ttu-id="414df-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="414df-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="414df-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="414df-133">-WhatIf</span></span>
<span data-ttu-id="414df-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="414df-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="414df-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="414df-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="414df-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="414df-136">CommonParameters</span></span>
<span data-ttu-id="414df-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="414df-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="414df-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="414df-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="414df-139">輸入</span><span class="sxs-lookup"><span data-stu-id="414df-139">INPUTS</span></span>

### <span data-ttu-id="414df-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="414df-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="414df-141">System.String</span><span class="sxs-lookup"><span data-stu-id="414df-141">System.String</span></span>

### <span data-ttu-id="414df-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="414df-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="414df-143">輸出</span><span class="sxs-lookup"><span data-stu-id="414df-143">OUTPUTS</span></span>

### <span data-ttu-id="414df-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="414df-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="414df-145">筆記</span><span class="sxs-lookup"><span data-stu-id="414df-145">NOTES</span></span>

## <span data-ttu-id="414df-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="414df-146">RELATED LINKS</span></span>

[<span data-ttu-id="414df-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="414df-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="414df-148">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="414df-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
