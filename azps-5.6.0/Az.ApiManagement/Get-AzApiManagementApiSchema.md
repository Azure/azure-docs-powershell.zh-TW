---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 3af651595ba51f7e5443a9f6447d07848470dc90
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904161"
---
# <span data-ttu-id="7867b-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7867b-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="7867b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7867b-102">SYNOPSIS</span></span>
<span data-ttu-id="7867b-103">取得 API 架構的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="7867b-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="7867b-104">語法</span><span class="sxs-lookup"><span data-stu-id="7867b-104">SYNTAX</span></span>

### <span data-ttu-id="7867b-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7867b-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7867b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7867b-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7867b-107">描述</span><span class="sxs-lookup"><span data-stu-id="7867b-107">DESCRIPTION</span></span>
<span data-ttu-id="7867b-108">**Get-AzApiManagementApiSchema Cmdlet** 會取得 API 架構的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="7867b-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="7867b-109">例子</span><span class="sxs-lookup"><span data-stu-id="7867b-109">EXAMPLES</span></span>

### <span data-ttu-id="7867b-110">範例 1：取得 Api 的所有 Api 架構詳細資料</span><span class="sxs-lookup"><span data-stu-id="7867b-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId wsdlapitest

SchemaId           : 2a03e1b4-1826-4e59-b372-4711f575db28
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <s:schema elementFormDefault="qualified"....

SchemaId           : b6e5497d-f65a-4851-9f5b-b5684cdae688
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <?xml version=""1.0"" encoding=""UTF-8""....
```

<span data-ttu-id="7867b-111">此命令會針對特定 ApiManagement 上下文，獲得與 Api `swagger-petstore-extensive` 相關聯的所有 API 架構。</span><span class="sxs-lookup"><span data-stu-id="7867b-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="7867b-112">範例 2：取得與 Api 相關聯的特定架構</span><span class="sxs-lookup"><span data-stu-id="7867b-112">Example 2: Get the specific schema associated with an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaId 5cc9cf67e6ed3b1154e638bd

SchemaId           : 5cc9cf67e6ed3b1154e638bd
Api Id             : swagger-petstore-extensive
Schema ContentType : swaggerdefinition
Schema Document    : {
                       "definitions": {
                         "pet": {
                        ....
```

<span data-ttu-id="7867b-113">此命令會針對特定 `5cc9cf67e6ed3b1154e638bd` ApiManagement 上下文，獲得與 `swagger-petstore-extensive` Api 相關聯的 API 架構。</span><span class="sxs-lookup"><span data-stu-id="7867b-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="7867b-114">參數</span><span class="sxs-lookup"><span data-stu-id="7867b-114">PARAMETERS</span></span>

### <span data-ttu-id="7867b-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7867b-115">-ApiId</span></span>
<span data-ttu-id="7867b-116">要尋找的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="7867b-116">API identifier to look for.</span></span>
<span data-ttu-id="7867b-117">如果指定，會嘗試使用識別碼取得 API。</span><span class="sxs-lookup"><span data-stu-id="7867b-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7867b-118">-內容</span><span class="sxs-lookup"><span data-stu-id="7867b-118">-Context</span></span>
<span data-ttu-id="7867b-119">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="7867b-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7867b-120">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="7867b-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7867b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7867b-121">-DefaultProfile</span></span>
<span data-ttu-id="7867b-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7867b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7867b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7867b-123">-ResourceId</span></span>
<span data-ttu-id="7867b-124">Api 架構的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7867b-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="7867b-125">如果指定，會嘗試根據識別碼尋找 api 架構。</span><span class="sxs-lookup"><span data-stu-id="7867b-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="7867b-126">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="7867b-126">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7867b-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="7867b-127">-SchemaId</span></span>
<span data-ttu-id="7867b-128">架構的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7867b-128">The identifier of the Schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7867b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7867b-129">CommonParameters</span></span>
<span data-ttu-id="7867b-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7867b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7867b-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7867b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7867b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7867b-132">INPUTS</span></span>

### <span data-ttu-id="7867b-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="7867b-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7867b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7867b-134">System.String</span></span>

## <span data-ttu-id="7867b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7867b-135">OUTPUTS</span></span>

### <span data-ttu-id="7867b-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7867b-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="7867b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7867b-137">NOTES</span></span>

## <span data-ttu-id="7867b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7867b-138">RELATED LINKS</span></span>

[<span data-ttu-id="7867b-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7867b-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="7867b-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7867b-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="7867b-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7867b-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)