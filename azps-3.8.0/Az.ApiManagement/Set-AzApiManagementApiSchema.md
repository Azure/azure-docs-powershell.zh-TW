---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
ms.openlocfilehash: 23881baf47536db4fa694cf2165b8550b7f8cd62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959805"
---
# <span data-ttu-id="525fe-101">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="525fe-101">Set-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="525fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="525fe-102">SYNOPSIS</span></span>
<span data-ttu-id="525fe-103">修改 API 架構</span><span class="sxs-lookup"><span data-stu-id="525fe-103">Modifies an API Schema</span></span>

## <span data-ttu-id="525fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="525fe-104">SYNTAX</span></span>

### <span data-ttu-id="525fe-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="525fe-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-SchemaDocumentContentType <String>] [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="525fe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="525fe-106">ByInputObject</span></span>
```
Set-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="525fe-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="525fe-107">ByResourceId</span></span>
```
Set-AzApiManagementApiSchema -ResourceId <String> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="525fe-108">說明</span><span class="sxs-lookup"><span data-stu-id="525fe-108">DESCRIPTION</span></span>
<span data-ttu-id="525fe-109">**AzApiManagementApiSchema** Cmdlet 會修改 Azure API 管理 API 架構。</span><span class="sxs-lookup"><span data-stu-id="525fe-109">The **Set-AzApiManagementApiSchema** cmdlet modifies an Azure API Management API Schema.</span></span>

## <span data-ttu-id="525fe-110">示例</span><span class="sxs-lookup"><span data-stu-id="525fe-110">EXAMPLES</span></span>

### <span data-ttu-id="525fe-111">範例1：修改 API 架構</span><span class="sxs-lookup"><span data-stu-id="525fe-111">Example 1 : Modifies an API Schema</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiSchema -Context $ApiMgmtContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="525fe-112">此範例會更新 Api 架構</span><span class="sxs-lookup"><span data-stu-id="525fe-112">The example updates the Api Schema</span></span>

## <span data-ttu-id="525fe-113">參數</span><span class="sxs-lookup"><span data-stu-id="525fe-113">PARAMETERS</span></span>

### <span data-ttu-id="525fe-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="525fe-114">-ApiId</span></span>
<span data-ttu-id="525fe-115">現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="525fe-115">Identifier of existing API.</span></span>
<span data-ttu-id="525fe-116">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="525fe-116">This parameter is required.</span></span>

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

### <span data-ttu-id="525fe-117">-內容</span><span class="sxs-lookup"><span data-stu-id="525fe-117">-Context</span></span>
<span data-ttu-id="525fe-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="525fe-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="525fe-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="525fe-119">This parameter is required.</span></span>

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

### <span data-ttu-id="525fe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="525fe-120">-DefaultProfile</span></span>
<span data-ttu-id="525fe-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="525fe-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="525fe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="525fe-122">-InputObject</span></span>
<span data-ttu-id="525fe-123">PsApiManagementApiSchema 的實例。</span><span class="sxs-lookup"><span data-stu-id="525fe-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="525fe-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="525fe-124">This parameter is required.</span></span>

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

### <span data-ttu-id="525fe-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="525fe-125">-PassThru</span></span>
<span data-ttu-id="525fe-126">如果已指定，則 ServiceManagement 代表 set API 的 PsApiManagementApi 類型的 ApiManagement 的實例。</span><span class="sxs-lookup"><span data-stu-id="525fe-126">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="525fe-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="525fe-127">-ResourceId</span></span>
<span data-ttu-id="525fe-128">[Arm] 診斷程式或 Api 架構的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="525fe-128">Arm ResourceId of Diagnostic or Api Schema.</span></span> <span data-ttu-id="525fe-129">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="525fe-129">This parameter is required.</span></span>

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

### <span data-ttu-id="525fe-130">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="525fe-130">-SchemaDocument</span></span>
<span data-ttu-id="525fe-131">以字串形式給 Api 架構檔。</span><span class="sxs-lookup"><span data-stu-id="525fe-131">Api schema document as a string.</span></span> <span data-ttu-id="525fe-132">此參數是-未指定-SchemaDocumentFile。</span><span class="sxs-lookup"><span data-stu-id="525fe-132">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="525fe-133">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="525fe-133">-SchemaDocumentContentType</span></span>
<span data-ttu-id="525fe-134">Api 架構的 ContentType。</span><span class="sxs-lookup"><span data-stu-id="525fe-134">ContentType of the api Schema.</span></span> <span data-ttu-id="525fe-135">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="525fe-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="525fe-136">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="525fe-136">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="525fe-137">Api 架構檔路徑。</span><span class="sxs-lookup"><span data-stu-id="525fe-137">Api schema document file path.</span></span> <span data-ttu-id="525fe-138">此參數是-未指定-SchemaDocument。</span><span class="sxs-lookup"><span data-stu-id="525fe-138">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="525fe-139">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="525fe-139">-SchemaId</span></span>
<span data-ttu-id="525fe-140">現有架構的識別碼。</span><span class="sxs-lookup"><span data-stu-id="525fe-140">Identifier of existing Schema.</span></span>
<span data-ttu-id="525fe-141">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="525fe-141">This parameter is required.</span></span>

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

### <span data-ttu-id="525fe-142">-確認</span><span class="sxs-lookup"><span data-stu-id="525fe-142">-Confirm</span></span>
<span data-ttu-id="525fe-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="525fe-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="525fe-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="525fe-144">-WhatIf</span></span>
<span data-ttu-id="525fe-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="525fe-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="525fe-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="525fe-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="525fe-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="525fe-147">CommonParameters</span></span>
<span data-ttu-id="525fe-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="525fe-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="525fe-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="525fe-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="525fe-150">輸入</span><span class="sxs-lookup"><span data-stu-id="525fe-150">INPUTS</span></span>

### <span data-ttu-id="525fe-151">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="525fe-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="525fe-152">System.object</span><span class="sxs-lookup"><span data-stu-id="525fe-152">System.String</span></span>

### <span data-ttu-id="525fe-153">ServiceManagement. PsApiManagementApiSchema （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="525fe-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="525fe-154">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="525fe-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="525fe-155">輸出</span><span class="sxs-lookup"><span data-stu-id="525fe-155">OUTPUTS</span></span>

### <span data-ttu-id="525fe-156">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="525fe-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="525fe-157">筆記</span><span class="sxs-lookup"><span data-stu-id="525fe-157">NOTES</span></span>

## <span data-ttu-id="525fe-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="525fe-158">RELATED LINKS</span></span>

[<span data-ttu-id="525fe-159">AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="525fe-159">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="525fe-160">新-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="525fe-160">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="525fe-161">移除-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="525fe-161">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

