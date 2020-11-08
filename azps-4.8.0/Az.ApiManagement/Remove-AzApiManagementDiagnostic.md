---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 488f4082007c96a111483d7efac6a8b9a74dba8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970001"
---
# <span data-ttu-id="103ef-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="103ef-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="103ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="103ef-102">SYNOPSIS</span></span>
<span data-ttu-id="103ef-103">從全域或 API 層級範圍中移除診斷實體。</span><span class="sxs-lookup"><span data-stu-id="103ef-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="103ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="103ef-104">SYNTAX</span></span>

### <span data-ttu-id="103ef-105">ByResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="103ef-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="103ef-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="103ef-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="103ef-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="103ef-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="103ef-108">說明</span><span class="sxs-lookup"><span data-stu-id="103ef-108">DESCRIPTION</span></span>
<span data-ttu-id="103ef-109">Cmdlet **移除-AzApiManagementDiagnostic** 會 `DiagnosticId` 從全域範圍或範圍中移除指定的診斷實體 `ApiId`</span><span class="sxs-lookup"><span data-stu-id="103ef-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="103ef-110">示例</span><span class="sxs-lookup"><span data-stu-id="103ef-110">EXAMPLES</span></span>

### <span data-ttu-id="103ef-111">範例1：移除診斷實體</span><span class="sxs-lookup"><span data-stu-id="103ef-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="103ef-112">這個範例會 `applicationinsights` 從 Api 管理服務移除診斷程式。</span><span class="sxs-lookup"><span data-stu-id="103ef-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="103ef-113">參數</span><span class="sxs-lookup"><span data-stu-id="103ef-113">PARAMETERS</span></span>

### <span data-ttu-id="103ef-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="103ef-114">-ApiId</span></span>
<span data-ttu-id="103ef-115">API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="103ef-115">Identifier of the API.</span></span>
<span data-ttu-id="103ef-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="103ef-116">This parameter is required.</span></span>

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

### <span data-ttu-id="103ef-117">-內容</span><span class="sxs-lookup"><span data-stu-id="103ef-117">-Context</span></span>
<span data-ttu-id="103ef-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="103ef-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="103ef-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="103ef-119">This parameter is required.</span></span>

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

### <span data-ttu-id="103ef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="103ef-120">-DefaultProfile</span></span>
<span data-ttu-id="103ef-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="103ef-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="103ef-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="103ef-122">-DiagnosticId</span></span>
<span data-ttu-id="103ef-123">現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="103ef-123">Identifier of existing product.</span></span>
<span data-ttu-id="103ef-124">如果已指定，將會傳回產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="103ef-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="103ef-125">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="103ef-125">This parameters is optional.</span></span>

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

### <span data-ttu-id="103ef-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="103ef-126">-InputObject</span></span>
<span data-ttu-id="103ef-127">PsApiManagementDiagnostic 的實例。</span><span class="sxs-lookup"><span data-stu-id="103ef-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="103ef-128">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="103ef-128">This parameter is required.</span></span>

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

### <span data-ttu-id="103ef-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="103ef-129">-PassThru</span></span>
<span data-ttu-id="103ef-130">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="103ef-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="103ef-131">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="103ef-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="103ef-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="103ef-132">-ResourceId</span></span>
<span data-ttu-id="103ef-133">診斷的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="103ef-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="103ef-134">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="103ef-134">This parameter is required.</span></span>

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

### <span data-ttu-id="103ef-135">-確認</span><span class="sxs-lookup"><span data-stu-id="103ef-135">-Confirm</span></span>
<span data-ttu-id="103ef-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="103ef-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="103ef-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="103ef-137">-WhatIf</span></span>
<span data-ttu-id="103ef-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="103ef-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="103ef-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="103ef-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="103ef-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="103ef-140">CommonParameters</span></span>
<span data-ttu-id="103ef-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="103ef-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="103ef-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="103ef-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="103ef-143">輸入</span><span class="sxs-lookup"><span data-stu-id="103ef-143">INPUTS</span></span>

### <span data-ttu-id="103ef-144">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="103ef-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="103ef-145">System.object</span><span class="sxs-lookup"><span data-stu-id="103ef-145">System.String</span></span>

### <span data-ttu-id="103ef-146">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="103ef-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="103ef-147">輸出</span><span class="sxs-lookup"><span data-stu-id="103ef-147">OUTPUTS</span></span>

### <span data-ttu-id="103ef-148">System.object</span><span class="sxs-lookup"><span data-stu-id="103ef-148">System.Boolean</span></span>

## <span data-ttu-id="103ef-149">筆記</span><span class="sxs-lookup"><span data-stu-id="103ef-149">NOTES</span></span>

## <span data-ttu-id="103ef-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="103ef-150">RELATED LINKS</span></span>

[<span data-ttu-id="103ef-151">AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="103ef-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="103ef-152">新-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="103ef-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="103ef-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="103ef-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)