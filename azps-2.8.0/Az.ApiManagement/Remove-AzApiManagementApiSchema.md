---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
ms.openlocfilehash: 4fa05a0c3568d8d787a7b269cd0f26c0adc82d0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613942"
---
# <span data-ttu-id="a31b6-101">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="a31b6-101">Remove-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="a31b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a31b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a31b6-103">從 API 移除 API 架構。</span><span class="sxs-lookup"><span data-stu-id="a31b6-103">Removes the API Schema from the API.</span></span>

## <span data-ttu-id="a31b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="a31b6-104">SYNTAX</span></span>

### <span data-ttu-id="a31b6-105">ByApiSchemaId (預設) </span><span class="sxs-lookup"><span data-stu-id="a31b6-105">ByApiSchemaId (Default)</span></span>
```
Remove-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a31b6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a31b6-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a31b6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a31b6-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementApiSchema -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a31b6-108">說明</span><span class="sxs-lookup"><span data-stu-id="a31b6-108">DESCRIPTION</span></span>
<span data-ttu-id="a31b6-109">從 Api **移除** 的 Cmdlet AzApiManagementSchema。</span><span class="sxs-lookup"><span data-stu-id="a31b6-109">The cmdlet **Remove-AzApiManagementSchema** from the Api.</span></span>

## <span data-ttu-id="a31b6-110">示例</span><span class="sxs-lookup"><span data-stu-id="a31b6-110">EXAMPLES</span></span>

### <span data-ttu-id="a31b6-111">範例1：從 API 移除 Api 架構</span><span class="sxs-lookup"><span data-stu-id="a31b6-111">Example 1 : Removes the Api Schema from the API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiSchema -Context $apimContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="a31b6-112">`2`如果沒有參照，腳本會從 Api 移除架構 `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="a31b6-112">The script removes the Schema `2` from the Api `echo-api` if it is not referenced.</span></span>

## <span data-ttu-id="a31b6-113">參數</span><span class="sxs-lookup"><span data-stu-id="a31b6-113">PARAMETERS</span></span>

### <span data-ttu-id="a31b6-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a31b6-114">-ApiId</span></span>
<span data-ttu-id="a31b6-115">API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a31b6-115">Identifier of the API.</span></span>
<span data-ttu-id="a31b6-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a31b6-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31b6-117">-內容</span><span class="sxs-lookup"><span data-stu-id="a31b6-117">-Context</span></span>
<span data-ttu-id="a31b6-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="a31b6-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a31b6-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a31b6-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a31b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a31b6-120">-DefaultProfile</span></span>
<span data-ttu-id="a31b6-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a31b6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a31b6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a31b6-122">-InputObject</span></span>
<span data-ttu-id="a31b6-123">PsApiManagementApiSchema 的實例。</span><span class="sxs-lookup"><span data-stu-id="a31b6-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="a31b6-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a31b6-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a31b6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a31b6-125">-PassThru</span></span>
<span data-ttu-id="a31b6-126">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="a31b6-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="a31b6-127">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a31b6-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="a31b6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a31b6-128">-ResourceId</span></span>
<span data-ttu-id="a31b6-129">ApiSchema 的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="a31b6-129">Arm ResourceId of ApiSchema.</span></span> <span data-ttu-id="a31b6-130">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a31b6-130">This parameter is required.</span></span>

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

### <span data-ttu-id="a31b6-131">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="a31b6-131">-SchemaId</span></span>
<span data-ttu-id="a31b6-132">API 架構的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a31b6-132">Identifier of the API Schema.</span></span>
<span data-ttu-id="a31b6-133">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a31b6-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31b6-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a31b6-134">-Confirm</span></span>
<span data-ttu-id="a31b6-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a31b6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a31b6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a31b6-136">-WhatIf</span></span>
<span data-ttu-id="a31b6-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a31b6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a31b6-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a31b6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a31b6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31b6-139">CommonParameters</span></span>
<span data-ttu-id="a31b6-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a31b6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31b6-141">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a31b6-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31b6-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a31b6-142">INPUTS</span></span>

### <span data-ttu-id="a31b6-143">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a31b6-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a31b6-144">ServiceManagement. PsApiManagementApiSchema （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a31b6-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="a31b6-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a31b6-145">System.String</span></span>

## <span data-ttu-id="a31b6-146">輸出</span><span class="sxs-lookup"><span data-stu-id="a31b6-146">OUTPUTS</span></span>

### <span data-ttu-id="a31b6-147">System.object</span><span class="sxs-lookup"><span data-stu-id="a31b6-147">System.Boolean</span></span>

## <span data-ttu-id="a31b6-148">筆記</span><span class="sxs-lookup"><span data-stu-id="a31b6-148">NOTES</span></span>

## <span data-ttu-id="a31b6-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="a31b6-149">RELATED LINKS</span></span>

[<span data-ttu-id="a31b6-150">AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="a31b6-150">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="a31b6-151">新-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="a31b6-151">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="a31b6-152">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="a31b6-152">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
