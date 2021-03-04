---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 4f6f7f1cf2223d4ef139d60e710f4a861149a3ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917509"
---
# <span data-ttu-id="fadf3-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fadf3-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="fadf3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fadf3-102">SYNOPSIS</span></span>
<span data-ttu-id="fadf3-103">從全域或 API 層級範圍移除診斷實體。</span><span class="sxs-lookup"><span data-stu-id="fadf3-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="fadf3-104">語法</span><span class="sxs-lookup"><span data-stu-id="fadf3-104">SYNTAX</span></span>

### <span data-ttu-id="fadf3-105">ByResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fadf3-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fadf3-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="fadf3-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fadf3-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fadf3-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fadf3-108">描述</span><span class="sxs-lookup"><span data-stu-id="fadf3-108">DESCRIPTION</span></span>
<span data-ttu-id="fadf3-109">Cmdlet **Remove-AzApiManagementDiagnostic** 會從全域範圍或範圍移除 `DiagnosticId` 指定的診斷 `ApiId` 實體</span><span class="sxs-lookup"><span data-stu-id="fadf3-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="fadf3-110">例子</span><span class="sxs-lookup"><span data-stu-id="fadf3-110">EXAMPLES</span></span>

### <span data-ttu-id="fadf3-111">範例 1：移除診斷實體</span><span class="sxs-lookup"><span data-stu-id="fadf3-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="fadf3-112">此範例會從 `applicationinsights` Api 管理服務移除診斷。</span><span class="sxs-lookup"><span data-stu-id="fadf3-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="fadf3-113">參數</span><span class="sxs-lookup"><span data-stu-id="fadf3-113">PARAMETERS</span></span>

### <span data-ttu-id="fadf3-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fadf3-114">-ApiId</span></span>
<span data-ttu-id="fadf3-115">API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fadf3-115">Identifier of the API.</span></span>
<span data-ttu-id="fadf3-116">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="fadf3-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fadf3-117">-內容</span><span class="sxs-lookup"><span data-stu-id="fadf3-117">-Context</span></span>
<span data-ttu-id="fadf3-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="fadf3-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fadf3-119">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="fadf3-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fadf3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fadf3-120">-DefaultProfile</span></span>
<span data-ttu-id="fadf3-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fadf3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fadf3-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="fadf3-122">-DiagnosticId</span></span>
<span data-ttu-id="fadf3-123">現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fadf3-123">Identifier of existing product.</span></span>
<span data-ttu-id="fadf3-124">如果指定，會返回產品範圍策略。</span><span class="sxs-lookup"><span data-stu-id="fadf3-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="fadf3-125">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="fadf3-125">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fadf3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fadf3-126">-InputObject</span></span>
<span data-ttu-id="fadf3-127">PsApiManagementDiagnostic 的實例。</span><span class="sxs-lookup"><span data-stu-id="fadf3-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="fadf3-128">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="fadf3-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fadf3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fadf3-129">-PassThru</span></span>
<span data-ttu-id="fadf3-130">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="fadf3-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="fadf3-131">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="fadf3-131">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fadf3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fadf3-132">-ResourceId</span></span>
<span data-ttu-id="fadf3-133">診斷的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="fadf3-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="fadf3-134">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="fadf3-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fadf3-135">-確認</span><span class="sxs-lookup"><span data-stu-id="fadf3-135">-Confirm</span></span>
<span data-ttu-id="fadf3-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fadf3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fadf3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fadf3-137">-WhatIf</span></span>
<span data-ttu-id="fadf3-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fadf3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fadf3-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fadf3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fadf3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fadf3-140">CommonParameters</span></span>
<span data-ttu-id="fadf3-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fadf3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fadf3-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fadf3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fadf3-143">輸入</span><span class="sxs-lookup"><span data-stu-id="fadf3-143">INPUTS</span></span>

### <span data-ttu-id="fadf3-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="fadf3-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fadf3-145">System.String</span><span class="sxs-lookup"><span data-stu-id="fadf3-145">System.String</span></span>

### <span data-ttu-id="fadf3-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fadf3-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fadf3-147">輸出</span><span class="sxs-lookup"><span data-stu-id="fadf3-147">OUTPUTS</span></span>

### <span data-ttu-id="fadf3-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fadf3-148">System.Boolean</span></span>

## <span data-ttu-id="fadf3-149">筆記</span><span class="sxs-lookup"><span data-stu-id="fadf3-149">NOTES</span></span>

## <span data-ttu-id="fadf3-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="fadf3-150">RELATED LINKS</span></span>

[<span data-ttu-id="fadf3-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fadf3-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="fadf3-152">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fadf3-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="fadf3-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fadf3-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)