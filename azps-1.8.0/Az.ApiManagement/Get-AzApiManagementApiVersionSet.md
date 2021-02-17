---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 5b7c06e9ed75cf973a3b9e375ff888477b9a96d7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400972"
---
# <span data-ttu-id="1c9a9-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1c9a9-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1c9a9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1c9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9a9-103">取得 API 版本集的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="1c9a9-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="1c9a9-104">語法</span><span class="sxs-lookup"><span data-stu-id="1c9a9-104">SYNTAX</span></span>

```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c9a9-105">描述</span><span class="sxs-lookup"><span data-stu-id="1c9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="1c9a9-106">**Get-AzApiManagementApiVersionSet** Cmdlet 會取得 API 管理環境中所設定 API 版本集的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-106">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="1c9a9-107">例子</span><span class="sxs-lookup"><span data-stu-id="1c9a9-107">EXAMPLES</span></span>

### <span data-ttu-id="1c9a9-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="1c9a9-108">Example 1</span></span>

### <span data-ttu-id="1c9a9-109">範例 1：取得所有 API 版本集</span><span class="sxs-lookup"><span data-stu-id="1c9a9-109">Example 1: Get all API Version Sets</span></span>
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

<span data-ttu-id="1c9a9-110">此命令會針對指定的上下文獲得所有 API 版本集。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="1c9a9-111">範例 2：取得 API 版本設定</span><span class="sxs-lookup"><span data-stu-id="1c9a9-111">Example 2: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="1c9a9-112">此命令會獲得具有指定識別碼的 API 版本集。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="1c9a9-113">參數</span><span class="sxs-lookup"><span data-stu-id="1c9a9-113">PARAMETERS</span></span>

### <span data-ttu-id="1c9a9-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="1c9a9-114">-ApiVersionSetId</span></span>
<span data-ttu-id="1c9a9-115">要尋找的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-115">API identifier to look for.</span></span>
<span data-ttu-id="1c9a9-116">如果指定，會嘗試使用識別碼取得 API。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="1c9a9-117">-內容</span><span class="sxs-lookup"><span data-stu-id="1c9a9-117">-Context</span></span>
<span data-ttu-id="1c9a9-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1c9a9-119">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9a9-120">-DefaultProfile</span></span>
<span data-ttu-id="1c9a9-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c9a9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9a9-122">CommonParameters</span></span>
<span data-ttu-id="1c9a9-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9a9-124">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1c9a9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9a9-125">輸入</span><span class="sxs-lookup"><span data-stu-id="1c9a9-125">INPUTS</span></span>

### <span data-ttu-id="1c9a9-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="1c9a9-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1c9a9-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1c9a9-127">System.String</span></span>

## <span data-ttu-id="1c9a9-128">輸出</span><span class="sxs-lookup"><span data-stu-id="1c9a9-128">OUTPUTS</span></span>

### <span data-ttu-id="1c9a9-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1c9a9-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1c9a9-130">筆記</span><span class="sxs-lookup"><span data-stu-id="1c9a9-130">NOTES</span></span>

## <span data-ttu-id="1c9a9-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c9a9-131">RELATED LINKS</span></span>

[<span data-ttu-id="1c9a9-132">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1c9a9-132">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="1c9a9-133">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="1c9a9-133">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="1c9a9-134">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1c9a9-134">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
