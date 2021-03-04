---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: 7ac8d0b243f70d9e0f02c620febc7062f0c2e3ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904549"
---
# <span data-ttu-id="96d84-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="96d84-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="96d84-102">簡介</span><span class="sxs-lookup"><span data-stu-id="96d84-102">SYNOPSIS</span></span>
<span data-ttu-id="96d84-103">在 ApiManagement 服務中建立新 API 架構</span><span class="sxs-lookup"><span data-stu-id="96d84-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="96d84-104">語法</span><span class="sxs-lookup"><span data-stu-id="96d84-104">SYNTAX</span></span>

### <span data-ttu-id="96d84-105">SchemaDocumentInline (預設) </span><span class="sxs-lookup"><span data-stu-id="96d84-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96d84-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="96d84-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96d84-107">描述</span><span class="sxs-lookup"><span data-stu-id="96d84-107">DESCRIPTION</span></span>
<span data-ttu-id="96d84-108">建立 API 的新 API 架構。</span><span class="sxs-lookup"><span data-stu-id="96d84-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="96d84-109">例子</span><span class="sxs-lookup"><span data-stu-id="96d84-109">EXAMPLES</span></span>

### <span data-ttu-id="96d84-110">範例 1：為 Swagger Petstore Extensive API 建立新架構</span><span class="sxs-lookup"><span data-stu-id="96d84-110">Example 1: Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="96d84-111">Cmdlet **New-AzApiManagementApiSchema** 會建立或更新 `swagger-petstore-extensive` aPI 的架構。</span><span class="sxs-lookup"><span data-stu-id="96d84-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="96d84-112">參數</span><span class="sxs-lookup"><span data-stu-id="96d84-112">PARAMETERS</span></span>

### <span data-ttu-id="96d84-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="96d84-113">-ApiId</span></span>
<span data-ttu-id="96d84-114">api 識別碼。</span><span class="sxs-lookup"><span data-stu-id="96d84-114">Identifier of api.</span></span> <span data-ttu-id="96d84-115">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="96d84-115">This parameter is required.</span></span>

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

### <span data-ttu-id="96d84-116">-內容</span><span class="sxs-lookup"><span data-stu-id="96d84-116">-Context</span></span>
<span data-ttu-id="96d84-117">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="96d84-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="96d84-118">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="96d84-118">This parameter is required.</span></span>

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

### <span data-ttu-id="96d84-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96d84-119">-DefaultProfile</span></span>
<span data-ttu-id="96d84-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="96d84-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96d84-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="96d84-121">-SchemaDocument</span></span>
<span data-ttu-id="96d84-122">Api 架構檔做為字串。</span><span class="sxs-lookup"><span data-stu-id="96d84-122">Api schema document as a string.</span></span> <span data-ttu-id="96d84-123">此參數為必填專案，未指定 -SchemaDocumentFile。</span><span class="sxs-lookup"><span data-stu-id="96d84-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

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

### <span data-ttu-id="96d84-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="96d84-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="96d84-125">Api 架構的 ContentType。</span><span class="sxs-lookup"><span data-stu-id="96d84-125">ContentType of the api Schema.</span></span> <span data-ttu-id="96d84-126">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="96d84-126">This parameter is required.</span></span>

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

### <span data-ttu-id="96d84-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="96d84-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="96d84-128">Api 架構檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="96d84-128">Api schema document file path.</span></span> <span data-ttu-id="96d84-129">此參數為必填專案，未指定 -SchemaDocument。</span><span class="sxs-lookup"><span data-stu-id="96d84-129">This parameter is required is -SchemaDocument is not specified.</span></span>

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

### <span data-ttu-id="96d84-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="96d84-130">-SchemaId</span></span>
<span data-ttu-id="96d84-131">新架構的識別碼。</span><span class="sxs-lookup"><span data-stu-id="96d84-131">Identifier of new schema.</span></span>
<span data-ttu-id="96d84-132">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="96d84-132">This parameter is optional.</span></span>
<span data-ttu-id="96d84-133">如果未指定，將會產生。</span><span class="sxs-lookup"><span data-stu-id="96d84-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="96d84-134">-確認</span><span class="sxs-lookup"><span data-stu-id="96d84-134">-Confirm</span></span>
<span data-ttu-id="96d84-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="96d84-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96d84-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96d84-136">-WhatIf</span></span>
<span data-ttu-id="96d84-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96d84-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96d84-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96d84-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96d84-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d84-139">CommonParameters</span></span>
<span data-ttu-id="96d84-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="96d84-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d84-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96d84-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d84-142">輸入</span><span class="sxs-lookup"><span data-stu-id="96d84-142">INPUTS</span></span>

### <span data-ttu-id="96d84-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="96d84-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="96d84-144">System.String</span><span class="sxs-lookup"><span data-stu-id="96d84-144">System.String</span></span>

## <span data-ttu-id="96d84-145">輸出</span><span class="sxs-lookup"><span data-stu-id="96d84-145">OUTPUTS</span></span>

### <span data-ttu-id="96d84-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="96d84-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="96d84-147">筆記</span><span class="sxs-lookup"><span data-stu-id="96d84-147">NOTES</span></span>

## <span data-ttu-id="96d84-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="96d84-148">RELATED LINKS</span></span>

[<span data-ttu-id="96d84-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="96d84-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="96d84-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="96d84-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="96d84-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="96d84-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
