---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: e6b9122481e5e506fc02a13a61b7ebeb71372e96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138894"
---
# <span data-ttu-id="c27da-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c27da-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="c27da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c27da-102">SYNOPSIS</span></span>
<span data-ttu-id="c27da-103">取得 API 版本集合的詳細資料</span><span class="sxs-lookup"><span data-stu-id="c27da-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="c27da-104">句法</span><span class="sxs-lookup"><span data-stu-id="c27da-104">SYNTAX</span></span>

### <span data-ttu-id="c27da-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c27da-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c27da-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c27da-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c27da-107">說明</span><span class="sxs-lookup"><span data-stu-id="c27da-107">DESCRIPTION</span></span>
<span data-ttu-id="c27da-108">**AzApiManagementApiVersionSet** Cmdlet 會取得 api 管理內容中所設定 Api 版本集合的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c27da-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="c27da-109">示例</span><span class="sxs-lookup"><span data-stu-id="c27da-109">EXAMPLES</span></span>

### <span data-ttu-id="c27da-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c27da-110">Example 1</span></span>

### <span data-ttu-id="c27da-111">範例2：取得所有 API 版本集合</span><span class="sxs-lookup"><span data-stu-id="c27da-111">Example 2: Get all API Version Sets</span></span>
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

<span data-ttu-id="c27da-112">這個命令會取得指定內容的所有 API 版本集合。</span><span class="sxs-lookup"><span data-stu-id="c27da-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="c27da-113">範例3：取得由識別碼設定的 API 版本</span><span class="sxs-lookup"><span data-stu-id="c27da-113">Example 3: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="c27da-114">這個命令會以指定的識別碼來取得 API 版本設定。</span><span class="sxs-lookup"><span data-stu-id="c27da-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="c27da-115">參數</span><span class="sxs-lookup"><span data-stu-id="c27da-115">PARAMETERS</span></span>

### <span data-ttu-id="c27da-116">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="c27da-116">-ApiVersionSetId</span></span>
<span data-ttu-id="c27da-117">要尋找的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="c27da-117">API identifier to look for.</span></span>
<span data-ttu-id="c27da-118">如果已指定，將會嘗試透過識別碼取得 API。</span><span class="sxs-lookup"><span data-stu-id="c27da-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="c27da-119">-內容</span><span class="sxs-lookup"><span data-stu-id="c27da-119">-Context</span></span>
<span data-ttu-id="c27da-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="c27da-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c27da-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="c27da-121">This parameter is required.</span></span>

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

### <span data-ttu-id="c27da-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c27da-122">-DefaultProfile</span></span>
<span data-ttu-id="c27da-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c27da-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c27da-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c27da-124">-ResourceId</span></span>
<span data-ttu-id="c27da-125">ApiVersionSet 的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c27da-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="c27da-126">如果已指定，將會嘗試依據識別碼尋找 apiVersionSet。</span><span class="sxs-lookup"><span data-stu-id="c27da-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="c27da-127">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="c27da-127">This parameter is required.</span></span>

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

### <span data-ttu-id="c27da-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c27da-128">CommonParameters</span></span>
<span data-ttu-id="c27da-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c27da-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c27da-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c27da-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c27da-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c27da-131">INPUTS</span></span>

### <span data-ttu-id="c27da-132">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="c27da-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c27da-133">System.object</span><span class="sxs-lookup"><span data-stu-id="c27da-133">System.String</span></span>

## <span data-ttu-id="c27da-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c27da-134">OUTPUTS</span></span>

### <span data-ttu-id="c27da-135">ServiceManagement. PsApiManagementApiVersionSet （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="c27da-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="c27da-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c27da-136">NOTES</span></span>

## <span data-ttu-id="c27da-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c27da-137">RELATED LINKS</span></span>

[<span data-ttu-id="c27da-138">新-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c27da-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="c27da-139">移除-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="c27da-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="c27da-140">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c27da-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
