---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 9673df14bdd0f5b7d0e946170a155231e8c4e751
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287788"
---
# <span data-ttu-id="789df-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="789df-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="789df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="789df-102">SYNOPSIS</span></span>
<span data-ttu-id="789df-103">移除特定的 API 發行</span><span class="sxs-lookup"><span data-stu-id="789df-103">Removes a particular API Release</span></span>

## <span data-ttu-id="789df-104">句法</span><span class="sxs-lookup"><span data-stu-id="789df-104">SYNTAX</span></span>

### <span data-ttu-id="789df-105">ByApiReleaseId (預設) </span><span class="sxs-lookup"><span data-stu-id="789df-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="789df-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="789df-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="789df-107">說明</span><span class="sxs-lookup"><span data-stu-id="789df-107">DESCRIPTION</span></span>

<span data-ttu-id="789df-108">**AzAzureRmApiManagementApiRelease** Cmdlet 會移除現有的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="789df-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="789df-109">示例</span><span class="sxs-lookup"><span data-stu-id="789df-109">EXAMPLES</span></span>

### <span data-ttu-id="789df-110">範例1：移除 API 發行</span><span class="sxs-lookup"><span data-stu-id="789df-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="789df-111">這個命令會以指定的 ApiId 和 ReleaseId 移除 API 發行。</span><span class="sxs-lookup"><span data-stu-id="789df-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="789df-112">參數</span><span class="sxs-lookup"><span data-stu-id="789df-112">PARAMETERS</span></span>

### <span data-ttu-id="789df-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="789df-113">-ApiId</span></span>
<span data-ttu-id="789df-114">API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="789df-114">Identifier of the API.</span></span>
<span data-ttu-id="789df-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="789df-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="789df-116">-內容</span><span class="sxs-lookup"><span data-stu-id="789df-116">-Context</span></span>
<span data-ttu-id="789df-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="789df-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="789df-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="789df-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="789df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="789df-119">-DefaultProfile</span></span>
<span data-ttu-id="789df-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="789df-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="789df-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="789df-121">-InputObject</span></span>
<span data-ttu-id="789df-122">PsApiManagementApiRelease 的實例。</span><span class="sxs-lookup"><span data-stu-id="789df-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="789df-123">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="789df-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="789df-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="789df-124">-PassThru</span></span>
<span data-ttu-id="789df-125">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="789df-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="789df-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="789df-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="789df-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="789df-127">-ReleaseId</span></span>
<span data-ttu-id="789df-128">API 發行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="789df-128">Identifier of the API Release.</span></span>
<span data-ttu-id="789df-129">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="789df-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="789df-130">-確認</span><span class="sxs-lookup"><span data-stu-id="789df-130">-Confirm</span></span>
<span data-ttu-id="789df-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="789df-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="789df-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="789df-132">-WhatIf</span></span>
<span data-ttu-id="789df-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="789df-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="789df-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="789df-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="789df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789df-135">CommonParameters</span></span>
<span data-ttu-id="789df-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="789df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789df-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="789df-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789df-138">輸入</span><span class="sxs-lookup"><span data-stu-id="789df-138">INPUTS</span></span>

### <span data-ttu-id="789df-139">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="789df-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="789df-140">ServiceManagement. PsApiManagementApiRelease （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="789df-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="789df-141">System.object</span><span class="sxs-lookup"><span data-stu-id="789df-141">System.String</span></span>

## <span data-ttu-id="789df-142">輸出</span><span class="sxs-lookup"><span data-stu-id="789df-142">OUTPUTS</span></span>

### <span data-ttu-id="789df-143">System.object</span><span class="sxs-lookup"><span data-stu-id="789df-143">System.Boolean</span></span>

## <span data-ttu-id="789df-144">筆記</span><span class="sxs-lookup"><span data-stu-id="789df-144">NOTES</span></span>

## <span data-ttu-id="789df-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="789df-145">RELATED LINKS</span></span>

[<span data-ttu-id="789df-146">AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="789df-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="789df-147">新-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="789df-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="789df-148">更新-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="789df-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)