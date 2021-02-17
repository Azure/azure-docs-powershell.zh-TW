---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 301de93ba72aff800a963034df422b6a4e4061f9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400870"
---
# <span data-ttu-id="47ac2-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="47ac2-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="47ac2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="47ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="47ac2-103">移除特定的 API 發行</span><span class="sxs-lookup"><span data-stu-id="47ac2-103">Removes a particular API Release</span></span>

## <span data-ttu-id="47ac2-104">語法</span><span class="sxs-lookup"><span data-stu-id="47ac2-104">SYNTAX</span></span>

### <span data-ttu-id="47ac2-105">ByApiReleaseId (預設) </span><span class="sxs-lookup"><span data-stu-id="47ac2-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ac2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="47ac2-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47ac2-107">描述</span><span class="sxs-lookup"><span data-stu-id="47ac2-107">DESCRIPTION</span></span>

<span data-ttu-id="47ac2-108">**Remove-AzAzureRmApiManagementApiRelease** Cmdlet 會移除現有的 API 發行。</span><span class="sxs-lookup"><span data-stu-id="47ac2-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="47ac2-109">例子</span><span class="sxs-lookup"><span data-stu-id="47ac2-109">EXAMPLES</span></span>

### <span data-ttu-id="47ac2-110">範例 1：移除 API 發行</span><span class="sxs-lookup"><span data-stu-id="47ac2-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="47ac2-111">此命令會移除具有指定 ApiId 和 ReleaseId 的 API 發行。</span><span class="sxs-lookup"><span data-stu-id="47ac2-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="47ac2-112">參數</span><span class="sxs-lookup"><span data-stu-id="47ac2-112">PARAMETERS</span></span>

### <span data-ttu-id="47ac2-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="47ac2-113">-ApiId</span></span>
<span data-ttu-id="47ac2-114">API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="47ac2-114">Identifier of the API.</span></span>
<span data-ttu-id="47ac2-115">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="47ac2-115">This parameter is required.</span></span>

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

### <span data-ttu-id="47ac2-116">-內容</span><span class="sxs-lookup"><span data-stu-id="47ac2-116">-Context</span></span>
<span data-ttu-id="47ac2-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="47ac2-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="47ac2-118">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="47ac2-118">This parameter is required.</span></span>

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

### <span data-ttu-id="47ac2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ac2-119">-DefaultProfile</span></span>
<span data-ttu-id="47ac2-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="47ac2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47ac2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47ac2-121">-InputObject</span></span>
<span data-ttu-id="47ac2-122">PsApiManagementApiRelease 實例。</span><span class="sxs-lookup"><span data-stu-id="47ac2-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="47ac2-123">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="47ac2-123">This parameter is required.</span></span>

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

### <span data-ttu-id="47ac2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47ac2-124">-PassThru</span></span>
<span data-ttu-id="47ac2-125">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="47ac2-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="47ac2-126">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="47ac2-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="47ac2-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="47ac2-127">-ReleaseId</span></span>
<span data-ttu-id="47ac2-128">API 發行識別碼。</span><span class="sxs-lookup"><span data-stu-id="47ac2-128">Identifier of the API Release.</span></span>
<span data-ttu-id="47ac2-129">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="47ac2-129">This parameter is required.</span></span>

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

### <span data-ttu-id="47ac2-130">-確認</span><span class="sxs-lookup"><span data-stu-id="47ac2-130">-Confirm</span></span>
<span data-ttu-id="47ac2-131">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="47ac2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47ac2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ac2-132">-WhatIf</span></span>
<span data-ttu-id="47ac2-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47ac2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47ac2-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47ac2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47ac2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ac2-135">CommonParameters</span></span>
<span data-ttu-id="47ac2-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="47ac2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ac2-137">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="47ac2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ac2-138">輸入</span><span class="sxs-lookup"><span data-stu-id="47ac2-138">INPUTS</span></span>

### <span data-ttu-id="47ac2-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="47ac2-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47ac2-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="47ac2-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="47ac2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="47ac2-141">System.String</span></span>

## <span data-ttu-id="47ac2-142">輸出</span><span class="sxs-lookup"><span data-stu-id="47ac2-142">OUTPUTS</span></span>

### <span data-ttu-id="47ac2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="47ac2-143">System.Boolean</span></span>

## <span data-ttu-id="47ac2-144">筆記</span><span class="sxs-lookup"><span data-stu-id="47ac2-144">NOTES</span></span>

## <span data-ttu-id="47ac2-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="47ac2-145">RELATED LINKS</span></span>

[<span data-ttu-id="47ac2-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="47ac2-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="47ac2-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="47ac2-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="47ac2-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="47ac2-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)