---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139313"
---
# <span data-ttu-id="56d4e-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="56d4e-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="56d4e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="56d4e-103">移除特定 Api 版本集</span><span class="sxs-lookup"><span data-stu-id="56d4e-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="56d4e-104">句法</span><span class="sxs-lookup"><span data-stu-id="56d4e-104">SYNTAX</span></span>

### <span data-ttu-id="56d4e-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="56d4e-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56d4e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="56d4e-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56d4e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="56d4e-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56d4e-108">說明</span><span class="sxs-lookup"><span data-stu-id="56d4e-108">DESCRIPTION</span></span>

<span data-ttu-id="56d4e-109">AzAzureRmApiManagementApiVersionSet Cmdlet 會移除現有 **的** API 版本集。</span><span class="sxs-lookup"><span data-stu-id="56d4e-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="56d4e-110">示例</span><span class="sxs-lookup"><span data-stu-id="56d4e-110">EXAMPLES</span></span>

### <span data-ttu-id="56d4e-111">範例1：移除 API 版本集</span><span class="sxs-lookup"><span data-stu-id="56d4e-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="56d4e-112">這個命令會以指定的 ApiVersionSetId 移除 API 版本設定。</span><span class="sxs-lookup"><span data-stu-id="56d4e-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="56d4e-113">參數</span><span class="sxs-lookup"><span data-stu-id="56d4e-113">PARAMETERS</span></span>

### <span data-ttu-id="56d4e-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="56d4e-114">-ApiVersionSetId</span></span>
<span data-ttu-id="56d4e-115">API 版本集的識別碼。</span><span class="sxs-lookup"><span data-stu-id="56d4e-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="56d4e-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="56d4e-116">This parameter is required.</span></span>

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

### <span data-ttu-id="56d4e-117">-內容</span><span class="sxs-lookup"><span data-stu-id="56d4e-117">-Context</span></span>
<span data-ttu-id="56d4e-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="56d4e-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="56d4e-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="56d4e-119">This parameter is required.</span></span>

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

### <span data-ttu-id="56d4e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d4e-120">-DefaultProfile</span></span>
<span data-ttu-id="56d4e-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="56d4e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56d4e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56d4e-122">-InputObject</span></span>
<span data-ttu-id="56d4e-123">PsApiManagementApiVersionSet 的實例。</span><span class="sxs-lookup"><span data-stu-id="56d4e-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="56d4e-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="56d4e-124">This parameter is required.</span></span>

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

### <span data-ttu-id="56d4e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56d4e-125">-PassThru</span></span>
<span data-ttu-id="56d4e-126">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="56d4e-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="56d4e-127">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="56d4e-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="56d4e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56d4e-128">-ResourceId</span></span>
<span data-ttu-id="56d4e-129">ApiVersionSet 的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="56d4e-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="56d4e-130">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="56d4e-130">This parameter is required.</span></span>

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

### <span data-ttu-id="56d4e-131">-確認</span><span class="sxs-lookup"><span data-stu-id="56d4e-131">-Confirm</span></span>
<span data-ttu-id="56d4e-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="56d4e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56d4e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d4e-133">-WhatIf</span></span>
<span data-ttu-id="56d4e-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56d4e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56d4e-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56d4e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56d4e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d4e-136">CommonParameters</span></span>
<span data-ttu-id="56d4e-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56d4e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d4e-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="56d4e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d4e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="56d4e-139">INPUTS</span></span>

### <span data-ttu-id="56d4e-140">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="56d4e-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="56d4e-141">ServiceManagement. PsApiManagementApiVersionSet （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="56d4e-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="56d4e-142">System.object</span><span class="sxs-lookup"><span data-stu-id="56d4e-142">System.String</span></span>

## <span data-ttu-id="56d4e-143">輸出</span><span class="sxs-lookup"><span data-stu-id="56d4e-143">OUTPUTS</span></span>

### <span data-ttu-id="56d4e-144">System.object</span><span class="sxs-lookup"><span data-stu-id="56d4e-144">System.Boolean</span></span>

## <span data-ttu-id="56d4e-145">筆記</span><span class="sxs-lookup"><span data-stu-id="56d4e-145">NOTES</span></span>

## <span data-ttu-id="56d4e-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="56d4e-146">RELATED LINKS</span></span>

[<span data-ttu-id="56d4e-147">AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="56d4e-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="56d4e-148">新-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="56d4e-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="56d4e-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="56d4e-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)