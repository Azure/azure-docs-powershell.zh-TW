---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: be18436936a7329de0b43701311a899713311ad9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916607"
---
# <span data-ttu-id="98c2f-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="98c2f-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="98c2f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="98c2f-103">取得 API 版本集的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="98c2f-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="98c2f-104">語法</span><span class="sxs-lookup"><span data-stu-id="98c2f-104">SYNTAX</span></span>

### <span data-ttu-id="98c2f-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="98c2f-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98c2f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98c2f-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98c2f-107">描述</span><span class="sxs-lookup"><span data-stu-id="98c2f-107">DESCRIPTION</span></span>
<span data-ttu-id="98c2f-108">**Get-AzApiManagementApiVersionSet** Cmdlet 會取得 API 管理環境中所設定 API 版本集的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="98c2f-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="98c2f-109">例子</span><span class="sxs-lookup"><span data-stu-id="98c2f-109">EXAMPLES</span></span>

### <span data-ttu-id="98c2f-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="98c2f-110">Example 1</span></span>

### <span data-ttu-id="98c2f-111">範例 2：取得所有 API 版本集</span><span class="sxs-lookup"><span data-stu-id="98c2f-111">Example 2: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext

ApiVersionSetId   : a93316c8-8b88-46cc-8260-380789a5d598
Description       :
VersionQueryName  :
VersionHeaderName :
DisplayName       : Echo API
VersioningScheme  : Segment
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/a916c8-8b88-46cc-8260-380789a5d598
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso

ApiVersionSetId   : 4cbdfa34-25f3-4a93-a9b6-76b6eade7562
Description       :
VersionQueryName  : api-version
VersionHeaderName :
DisplayName       : getproduct old
VersioningScheme  : Query
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/4cbdfa34-25f3-4a93-a9b6-76b6eade7562
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="98c2f-112">此命令會針對指定的上下文獲得所有 API 版本集。</span><span class="sxs-lookup"><span data-stu-id="98c2f-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="98c2f-113">範例 3：取得 API 版本設定</span><span class="sxs-lookup"><span data-stu-id="98c2f-113">Example 3: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="98c2f-114">此命令會獲得具有指定識別碼的 API 版本集。</span><span class="sxs-lookup"><span data-stu-id="98c2f-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="98c2f-115">參數</span><span class="sxs-lookup"><span data-stu-id="98c2f-115">PARAMETERS</span></span>

### <span data-ttu-id="98c2f-116">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="98c2f-116">-ApiVersionSetId</span></span>
<span data-ttu-id="98c2f-117">要尋找的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="98c2f-117">API identifier to look for.</span></span>
<span data-ttu-id="98c2f-118">如果指定，會嘗試使用識別碼取得 API。</span><span class="sxs-lookup"><span data-stu-id="98c2f-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="98c2f-119">-內容</span><span class="sxs-lookup"><span data-stu-id="98c2f-119">-Context</span></span>
<span data-ttu-id="98c2f-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="98c2f-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="98c2f-121">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="98c2f-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98c2f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c2f-122">-DefaultProfile</span></span>
<span data-ttu-id="98c2f-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="98c2f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98c2f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98c2f-124">-ResourceId</span></span>
<span data-ttu-id="98c2f-125">ApiVersionSet 的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="98c2f-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="98c2f-126">如果指定，會嘗試根據識別碼尋找 apiVersionSet。</span><span class="sxs-lookup"><span data-stu-id="98c2f-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="98c2f-127">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="98c2f-127">This parameter is required.</span></span>

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

### <span data-ttu-id="98c2f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c2f-128">CommonParameters</span></span>
<span data-ttu-id="98c2f-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98c2f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c2f-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98c2f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c2f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="98c2f-131">INPUTS</span></span>

### <span data-ttu-id="98c2f-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="98c2f-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="98c2f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="98c2f-133">System.String</span></span>

## <span data-ttu-id="98c2f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="98c2f-134">OUTPUTS</span></span>

### <span data-ttu-id="98c2f-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="98c2f-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="98c2f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="98c2f-136">NOTES</span></span>

## <span data-ttu-id="98c2f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="98c2f-137">RELATED LINKS</span></span>

[<span data-ttu-id="98c2f-138">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="98c2f-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="98c2f-139">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="98c2f-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="98c2f-140">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="98c2f-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
