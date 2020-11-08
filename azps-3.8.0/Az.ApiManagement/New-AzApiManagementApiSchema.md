---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: ad931b574af8445947e9f3f4df12c35c2baa1bf7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958205"
---
# <span data-ttu-id="b1df6-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="b1df6-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="b1df6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1df6-102">SYNOPSIS</span></span>
<span data-ttu-id="b1df6-103">在 ApiManagement 服務中建立新的 API 架構</span><span class="sxs-lookup"><span data-stu-id="b1df6-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="b1df6-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1df6-104">SYNTAX</span></span>

### <span data-ttu-id="b1df6-105">SchemaDocumentInline (預設) </span><span class="sxs-lookup"><span data-stu-id="b1df6-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1df6-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="b1df6-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1df6-107">說明</span><span class="sxs-lookup"><span data-stu-id="b1df6-107">DESCRIPTION</span></span>
<span data-ttu-id="b1df6-108">建立 API 的新 API 架構。</span><span class="sxs-lookup"><span data-stu-id="b1df6-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="b1df6-109">示例</span><span class="sxs-lookup"><span data-stu-id="b1df6-109">EXAMPLES</span></span>

### <span data-ttu-id="b1df6-110">範例1：建立新的 [Swagger] 架構以 Petstore 大量 API</span><span class="sxs-lookup"><span data-stu-id="b1df6-110">Example 1 : Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="b1df6-111">Cmdlet **New-AzApiManagementApiSchema** 會建立或更新 aPI 的架構 `swagger-petstore-extensive` 。</span><span class="sxs-lookup"><span data-stu-id="b1df6-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="b1df6-112">參數</span><span class="sxs-lookup"><span data-stu-id="b1df6-112">PARAMETERS</span></span>

### <span data-ttu-id="b1df6-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b1df6-113">-ApiId</span></span>
<span data-ttu-id="b1df6-114">Api 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1df6-114">Identifier of api.</span></span> <span data-ttu-id="b1df6-115">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="b1df6-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-116">-內容</span><span class="sxs-lookup"><span data-stu-id="b1df6-116">-Context</span></span>
<span data-ttu-id="b1df6-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="b1df6-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b1df6-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="b1df6-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1df6-119">-DefaultProfile</span></span>
<span data-ttu-id="b1df6-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1df6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1df6-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="b1df6-121">-SchemaDocument</span></span>
<span data-ttu-id="b1df6-122">以字串形式給 Api 架構檔。</span><span class="sxs-lookup"><span data-stu-id="b1df6-122">Api schema document as a string.</span></span> <span data-ttu-id="b1df6-123">此參數是-未指定-SchemaDocumentFile。</span><span class="sxs-lookup"><span data-stu-id="b1df6-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentInline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="b1df6-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="b1df6-125">Api 架構的 ContentType。</span><span class="sxs-lookup"><span data-stu-id="b1df6-125">ContentType of the api Schema.</span></span> <span data-ttu-id="b1df6-126">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="b1df6-126">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="b1df6-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="b1df6-128">Api 架構檔路徑。</span><span class="sxs-lookup"><span data-stu-id="b1df6-128">Api schema document file path.</span></span> <span data-ttu-id="b1df6-129">此參數是-未指定-SchemaDocument。</span><span class="sxs-lookup"><span data-stu-id="b1df6-129">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="b1df6-130">-SchemaId</span></span>
<span data-ttu-id="b1df6-131">新架構的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1df6-131">Identifier of new schema.</span></span>
<span data-ttu-id="b1df6-132">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="b1df6-132">This parameter is optional.</span></span>
<span data-ttu-id="b1df6-133">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="b1df6-133">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-134">-確認</span><span class="sxs-lookup"><span data-stu-id="b1df6-134">-Confirm</span></span>
<span data-ttu-id="b1df6-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1df6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1df6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1df6-136">-WhatIf</span></span>
<span data-ttu-id="b1df6-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1df6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1df6-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1df6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1df6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1df6-139">CommonParameters</span></span>
<span data-ttu-id="b1df6-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1df6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1df6-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1df6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1df6-142">輸入</span><span class="sxs-lookup"><span data-stu-id="b1df6-142">INPUTS</span></span>

### <span data-ttu-id="b1df6-143">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b1df6-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b1df6-144">System.object</span><span class="sxs-lookup"><span data-stu-id="b1df6-144">System.String</span></span>

## <span data-ttu-id="b1df6-145">輸出</span><span class="sxs-lookup"><span data-stu-id="b1df6-145">OUTPUTS</span></span>

### <span data-ttu-id="b1df6-146">ServiceManagement. PsApiManagementApiSchema （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b1df6-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="b1df6-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b1df6-147">NOTES</span></span>

## <span data-ttu-id="b1df6-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1df6-148">RELATED LINKS</span></span>

[<span data-ttu-id="b1df6-149">AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="b1df6-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="b1df6-150">移除-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="b1df6-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="b1df6-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="b1df6-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)