---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 8f505496bc94d7cd0fc4ca69e6a81324a82871d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914942"
---
# <span data-ttu-id="9f809-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9f809-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="9f809-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9f809-102">SYNOPSIS</span></span>
<span data-ttu-id="9f809-103">移除特定的 Api 版本集</span><span class="sxs-lookup"><span data-stu-id="9f809-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="9f809-104">語法</span><span class="sxs-lookup"><span data-stu-id="9f809-104">SYNTAX</span></span>

### <span data-ttu-id="9f809-105">展開Parameter (預設) </span><span class="sxs-lookup"><span data-stu-id="9f809-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f809-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9f809-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f809-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f809-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f809-108">描述</span><span class="sxs-lookup"><span data-stu-id="9f809-108">DESCRIPTION</span></span>

<span data-ttu-id="9f809-109">**Remove-AzAzureRmApiManagementApiVersionSet** Cmdlet 會移除現有的 API 版本集。</span><span class="sxs-lookup"><span data-stu-id="9f809-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="9f809-110">例子</span><span class="sxs-lookup"><span data-stu-id="9f809-110">EXAMPLES</span></span>

### <span data-ttu-id="9f809-111">範例 1：移除 API 版本集</span><span class="sxs-lookup"><span data-stu-id="9f809-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="9f809-112">此命令會移除具有指定 ApiVersionSetId 的 API 版本集。</span><span class="sxs-lookup"><span data-stu-id="9f809-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="9f809-113">參數</span><span class="sxs-lookup"><span data-stu-id="9f809-113">PARAMETERS</span></span>

### <span data-ttu-id="9f809-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="9f809-114">-ApiVersionSetId</span></span>
<span data-ttu-id="9f809-115">API 版本集的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9f809-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="9f809-116">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="9f809-116">This parameter is required.</span></span>

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

### <span data-ttu-id="9f809-117">-內容</span><span class="sxs-lookup"><span data-stu-id="9f809-117">-Context</span></span>
<span data-ttu-id="9f809-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="9f809-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9f809-119">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="9f809-119">This parameter is required.</span></span>

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

### <span data-ttu-id="9f809-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f809-120">-DefaultProfile</span></span>
<span data-ttu-id="9f809-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f809-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f809-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f809-122">-InputObject</span></span>
<span data-ttu-id="9f809-123">PsApiManagementApiVersionSet 實例。</span><span class="sxs-lookup"><span data-stu-id="9f809-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="9f809-124">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="9f809-124">This parameter is required.</span></span>

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

### <span data-ttu-id="9f809-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f809-125">-PassThru</span></span>
<span data-ttu-id="9f809-126">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="9f809-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="9f809-127">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="9f809-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="9f809-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f809-128">-ResourceId</span></span>
<span data-ttu-id="9f809-129">ApiVersionSet 的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="9f809-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="9f809-130">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="9f809-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f809-131">-確認</span><span class="sxs-lookup"><span data-stu-id="9f809-131">-Confirm</span></span>
<span data-ttu-id="9f809-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9f809-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f809-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f809-133">-WhatIf</span></span>
<span data-ttu-id="9f809-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9f809-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f809-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9f809-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f809-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f809-136">CommonParameters</span></span>
<span data-ttu-id="9f809-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9f809-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f809-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f809-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f809-139">輸入</span><span class="sxs-lookup"><span data-stu-id="9f809-139">INPUTS</span></span>

### <span data-ttu-id="9f809-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="9f809-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9f809-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9f809-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="9f809-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9f809-142">System.String</span></span>

## <span data-ttu-id="9f809-143">輸出</span><span class="sxs-lookup"><span data-stu-id="9f809-143">OUTPUTS</span></span>

### <span data-ttu-id="9f809-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f809-144">System.Boolean</span></span>

## <span data-ttu-id="9f809-145">筆記</span><span class="sxs-lookup"><span data-stu-id="9f809-145">NOTES</span></span>

## <span data-ttu-id="9f809-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f809-146">RELATED LINKS</span></span>

[<span data-ttu-id="9f809-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9f809-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="9f809-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9f809-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="9f809-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9f809-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)