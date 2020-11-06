---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
ms.openlocfilehash: 2b8db6f5d550c91f806595c80be4beb300a95273
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613944"
---
# <span data-ttu-id="f6608-101">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f6608-101">Remove-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="f6608-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6608-102">SYNOPSIS</span></span>
<span data-ttu-id="f6608-103">已移除特定的 API 修訂版本</span><span class="sxs-lookup"><span data-stu-id="f6608-103">Removed a particular API Revision</span></span>

## <span data-ttu-id="f6608-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6608-104">SYNTAX</span></span>

### <span data-ttu-id="f6608-105">ByApiId (預設) </span><span class="sxs-lookup"><span data-stu-id="f6608-105">ByApiId (Default)</span></span>
```
Remove-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6608-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f6608-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6608-107">說明</span><span class="sxs-lookup"><span data-stu-id="f6608-107">DESCRIPTION</span></span>
<span data-ttu-id="f6608-108">Cmdlet **移除-AzApiManagementApiRevision** 會移除特定的 API 修訂版本。</span><span class="sxs-lookup"><span data-stu-id="f6608-108">The cmdlet **Remove-AzApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="f6608-109">示例</span><span class="sxs-lookup"><span data-stu-id="f6608-109">EXAMPLES</span></span>

### <span data-ttu-id="f6608-110">範例1：移除 API 修訂</span><span class="sxs-lookup"><span data-stu-id="f6608-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="f6608-111">這個命令會 `2` `echo-api` 從 api 管理服務移除 api 的修訂版本。</span><span class="sxs-lookup"><span data-stu-id="f6608-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="f6608-112">參數</span><span class="sxs-lookup"><span data-stu-id="f6608-112">PARAMETERS</span></span>

### <span data-ttu-id="f6608-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f6608-113">-ApiId</span></span>
<span data-ttu-id="f6608-114">API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6608-114">Identifier of the API.</span></span>
<span data-ttu-id="f6608-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f6608-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6608-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f6608-116">-ApiRevision</span></span>
<span data-ttu-id="f6608-117">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6608-117">Identifier of the API Revision.</span></span> <span data-ttu-id="f6608-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f6608-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6608-119">-內容</span><span class="sxs-lookup"><span data-stu-id="f6608-119">-Context</span></span>
<span data-ttu-id="f6608-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="f6608-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f6608-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f6608-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6608-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6608-122">-DefaultProfile</span></span>
<span data-ttu-id="f6608-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6608-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6608-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6608-124">-InputObject</span></span>
<span data-ttu-id="f6608-125">PsApiManagementApiRelease 的實例。</span><span class="sxs-lookup"><span data-stu-id="f6608-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="f6608-126">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f6608-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6608-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6608-127">-PassThru</span></span>
<span data-ttu-id="f6608-128">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="f6608-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="f6608-129">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f6608-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="f6608-130">-確認</span><span class="sxs-lookup"><span data-stu-id="f6608-130">-Confirm</span></span>
<span data-ttu-id="f6608-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f6608-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6608-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6608-132">-WhatIf</span></span>
<span data-ttu-id="f6608-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6608-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6608-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6608-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6608-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6608-135">CommonParameters</span></span>
<span data-ttu-id="f6608-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6608-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6608-137">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f6608-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6608-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f6608-138">INPUTS</span></span>

### <span data-ttu-id="f6608-139">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f6608-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f6608-140">System.object</span><span class="sxs-lookup"><span data-stu-id="f6608-140">System.String</span></span>

### <span data-ttu-id="f6608-141">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f6608-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="f6608-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f6608-142">OUTPUTS</span></span>

### <span data-ttu-id="f6608-143">System.object</span><span class="sxs-lookup"><span data-stu-id="f6608-143">System.Boolean</span></span>

## <span data-ttu-id="f6608-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f6608-144">NOTES</span></span>

## <span data-ttu-id="f6608-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6608-145">RELATED LINKS</span></span>

[<span data-ttu-id="f6608-146">AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f6608-146">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="f6608-147">新-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f6608-147">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="f6608-148">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="f6608-148">Set-AzApiManagementApiRevision</span></span>](./Set-AzApiManagementApiRevision.md)