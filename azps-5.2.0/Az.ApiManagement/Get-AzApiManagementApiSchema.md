---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 837494b8f042d3ea788eda69d47845b02859c805
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278163"
---
# <span data-ttu-id="658be-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="658be-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="658be-102">摘要</span><span class="sxs-lookup"><span data-stu-id="658be-102">SYNOPSIS</span></span>
<span data-ttu-id="658be-103">取得 API 架構的詳細資料</span><span class="sxs-lookup"><span data-stu-id="658be-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="658be-104">句法</span><span class="sxs-lookup"><span data-stu-id="658be-104">SYNTAX</span></span>

### <span data-ttu-id="658be-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="658be-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="658be-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="658be-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="658be-107">說明</span><span class="sxs-lookup"><span data-stu-id="658be-107">DESCRIPTION</span></span>
<span data-ttu-id="658be-108">**AzApiManagementApiSchema** Cmdlet 會取得 API 架構的詳細資料</span><span class="sxs-lookup"><span data-stu-id="658be-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="658be-109">示例</span><span class="sxs-lookup"><span data-stu-id="658be-109">EXAMPLES</span></span>

### <span data-ttu-id="658be-110">範例1：取得 Api 所有 Api 架構的詳細資料</span><span class="sxs-lookup"><span data-stu-id="658be-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
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

<span data-ttu-id="658be-111">這個命令會取得與 Api 相關的所有 API 架構 `swagger-petstore-extensive` ，以用於特定的 ApiManagement 內容。</span><span class="sxs-lookup"><span data-stu-id="658be-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="658be-112">範例2：取得與 Api 相關聯的特定架構</span><span class="sxs-lookup"><span data-stu-id="658be-112">Example 2: Get the specific schema associated with an Api</span></span>
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

<span data-ttu-id="658be-113">這個命令會取得 `5cc9cf67e6ed3b1154e638bd` 與 api 相關的 api 架構 `swagger-petstore-extensive` ，以用於特定的 ApiManagement 內容。</span><span class="sxs-lookup"><span data-stu-id="658be-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="658be-114">參數</span><span class="sxs-lookup"><span data-stu-id="658be-114">PARAMETERS</span></span>

### <span data-ttu-id="658be-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="658be-115">-ApiId</span></span>
<span data-ttu-id="658be-116">要尋找的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="658be-116">API identifier to look for.</span></span>
<span data-ttu-id="658be-117">如果已指定，將會嘗試透過識別碼取得 API。</span><span class="sxs-lookup"><span data-stu-id="658be-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="658be-118">-內容</span><span class="sxs-lookup"><span data-stu-id="658be-118">-Context</span></span>
<span data-ttu-id="658be-119">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="658be-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="658be-120">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="658be-120">This parameter is required.</span></span>

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

### <span data-ttu-id="658be-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="658be-121">-DefaultProfile</span></span>
<span data-ttu-id="658be-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="658be-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="658be-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="658be-123">-ResourceId</span></span>
<span data-ttu-id="658be-124">Api 架構的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="658be-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="658be-125">如果已指定，將會嘗試依據識別碼尋找 api 架構。</span><span class="sxs-lookup"><span data-stu-id="658be-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="658be-126">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="658be-126">This parameter is required.</span></span>

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

### <span data-ttu-id="658be-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="658be-127">-SchemaId</span></span>
<span data-ttu-id="658be-128">架構的識別碼。</span><span class="sxs-lookup"><span data-stu-id="658be-128">The identifier of the Schema.</span></span>

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

### <span data-ttu-id="658be-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="658be-129">CommonParameters</span></span>
<span data-ttu-id="658be-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="658be-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="658be-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="658be-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="658be-132">輸入</span><span class="sxs-lookup"><span data-stu-id="658be-132">INPUTS</span></span>

### <span data-ttu-id="658be-133">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="658be-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="658be-134">System.object</span><span class="sxs-lookup"><span data-stu-id="658be-134">System.String</span></span>

## <span data-ttu-id="658be-135">輸出</span><span class="sxs-lookup"><span data-stu-id="658be-135">OUTPUTS</span></span>

### <span data-ttu-id="658be-136">ServiceManagement. PsApiManagementApiSchema （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="658be-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="658be-137">筆記</span><span class="sxs-lookup"><span data-stu-id="658be-137">NOTES</span></span>

## <span data-ttu-id="658be-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="658be-138">RELATED LINKS</span></span>

[<span data-ttu-id="658be-139">新-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="658be-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="658be-140">移除-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="658be-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="658be-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="658be-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)