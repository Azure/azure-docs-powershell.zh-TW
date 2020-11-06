---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 71256ab72d8c5c6042aa6c17b184066f96b3a813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444147"
---
# <span data-ttu-id="78368-101">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="78368-101">Remove-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="78368-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78368-102">SYNOPSIS</span></span>
<span data-ttu-id="78368-103">移除特定的 API 發行</span><span class="sxs-lookup"><span data-stu-id="78368-103">Removes a particular API Release</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78368-104">句法</span><span class="sxs-lookup"><span data-stu-id="78368-104">SYNTAX</span></span>

### <span data-ttu-id="78368-105">ByApiReleaseId (預設) </span><span class="sxs-lookup"><span data-stu-id="78368-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78368-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="78368-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78368-107">說明</span><span class="sxs-lookup"><span data-stu-id="78368-107">DESCRIPTION</span></span>

<span data-ttu-id="78368-108">**AzureRmApiManagementApiRelease** Cmdlet 會移除現有的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="78368-108">The **Remove-AzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="78368-109">示例</span><span class="sxs-lookup"><span data-stu-id="78368-109">EXAMPLES</span></span>

### <span data-ttu-id="78368-110">範例1：移除 API 發行</span><span class="sxs-lookup"><span data-stu-id="78368-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="78368-111">這個命令會以指定的 ApiId 和 ReleaseId 移除 API 發行。</span><span class="sxs-lookup"><span data-stu-id="78368-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="78368-112">參數</span><span class="sxs-lookup"><span data-stu-id="78368-112">PARAMETERS</span></span>

### <span data-ttu-id="78368-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="78368-113">-ApiId</span></span>
<span data-ttu-id="78368-114">API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="78368-114">Identifier of the API.</span></span>
<span data-ttu-id="78368-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="78368-115">This parameter is required.</span></span>

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

### <span data-ttu-id="78368-116">-內容</span><span class="sxs-lookup"><span data-stu-id="78368-116">-Context</span></span>
<span data-ttu-id="78368-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="78368-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="78368-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="78368-118">This parameter is required.</span></span>

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

### <span data-ttu-id="78368-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78368-119">-DefaultProfile</span></span>
<span data-ttu-id="78368-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78368-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78368-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78368-121">-InputObject</span></span>
<span data-ttu-id="78368-122">PsApiManagementApiRelease 的實例。</span><span class="sxs-lookup"><span data-stu-id="78368-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="78368-123">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="78368-123">This parameter is required.</span></span>

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

### <span data-ttu-id="78368-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78368-124">-PassThru</span></span>
<span data-ttu-id="78368-125">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="78368-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="78368-126">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="78368-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="78368-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="78368-127">-ReleaseId</span></span>
<span data-ttu-id="78368-128">API 發行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="78368-128">Identifier of the API Release.</span></span>
<span data-ttu-id="78368-129">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="78368-129">This parameter is required.</span></span>

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

### <span data-ttu-id="78368-130">-確認</span><span class="sxs-lookup"><span data-stu-id="78368-130">-Confirm</span></span>
<span data-ttu-id="78368-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="78368-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78368-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78368-132">-WhatIf</span></span>
<span data-ttu-id="78368-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="78368-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78368-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78368-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78368-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78368-135">CommonParameters</span></span>
<span data-ttu-id="78368-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78368-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78368-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78368-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78368-138">輸入</span><span class="sxs-lookup"><span data-stu-id="78368-138">INPUTS</span></span>

### <span data-ttu-id="78368-139">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="78368-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="78368-140">ServiceManagement. PsApiManagementApiRelease （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="78368-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>
<span data-ttu-id="78368-141">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="78368-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="78368-142">System.object</span><span class="sxs-lookup"><span data-stu-id="78368-142">System.String</span></span>

## <span data-ttu-id="78368-143">輸出</span><span class="sxs-lookup"><span data-stu-id="78368-143">OUTPUTS</span></span>

### <span data-ttu-id="78368-144">System.object</span><span class="sxs-lookup"><span data-stu-id="78368-144">System.Boolean</span></span>

## <span data-ttu-id="78368-145">筆記</span><span class="sxs-lookup"><span data-stu-id="78368-145">NOTES</span></span>

## <span data-ttu-id="78368-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="78368-146">RELATED LINKS</span></span>

[<span data-ttu-id="78368-147">AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="78368-147">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="78368-148">新-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="78368-148">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="78368-149">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="78368-149">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
