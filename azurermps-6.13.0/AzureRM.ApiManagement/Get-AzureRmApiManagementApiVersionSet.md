---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 60a811aaa097ccc95f8dd57fa105ba4b1388b060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450356"
---
# <span data-ttu-id="6136a-101">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6136a-101">Get-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="6136a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6136a-102">SYNOPSIS</span></span>
<span data-ttu-id="6136a-103">取得 API 版本集合的詳細資料</span><span class="sxs-lookup"><span data-stu-id="6136a-103">Get the details of the API Version Sets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6136a-104">句法</span><span class="sxs-lookup"><span data-stu-id="6136a-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6136a-105">說明</span><span class="sxs-lookup"><span data-stu-id="6136a-105">DESCRIPTION</span></span>
<span data-ttu-id="6136a-106">**AzureRmApiManagementApiVersionSet** Cmdlet 會取得 api 管理內容中所設定 Api 版本集合的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6136a-106">The **Get-AzureRmApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="6136a-107">示例</span><span class="sxs-lookup"><span data-stu-id="6136a-107">EXAMPLES</span></span>

### <span data-ttu-id="6136a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6136a-108">Example 1</span></span>

### <span data-ttu-id="6136a-109">範例1：取得所有 API 版本集合</span><span class="sxs-lookup"><span data-stu-id="6136a-109">Example 1: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext

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

<span data-ttu-id="6136a-110">這個命令會取得指定內容的所有 API 版本集合。</span><span class="sxs-lookup"><span data-stu-id="6136a-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="6136a-111">範例2：取得由識別碼設定的 API 版本</span><span class="sxs-lookup"><span data-stu-id="6136a-111">Example 2: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

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

<span data-ttu-id="6136a-112">這個命令會以指定的識別碼來取得 API 版本設定。</span><span class="sxs-lookup"><span data-stu-id="6136a-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="6136a-113">參數</span><span class="sxs-lookup"><span data-stu-id="6136a-113">PARAMETERS</span></span>

### <span data-ttu-id="6136a-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="6136a-114">-ApiVersionSetId</span></span>
<span data-ttu-id="6136a-115">要尋找的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="6136a-115">API identifier to look for.</span></span>
<span data-ttu-id="6136a-116">如果已指定，將會嘗試透過識別碼取得 API。</span><span class="sxs-lookup"><span data-stu-id="6136a-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="6136a-117">-內容</span><span class="sxs-lookup"><span data-stu-id="6136a-117">-Context</span></span>
<span data-ttu-id="6136a-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="6136a-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6136a-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="6136a-119">This parameter is required.</span></span>

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

### <span data-ttu-id="6136a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6136a-120">-DefaultProfile</span></span>
<span data-ttu-id="6136a-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6136a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6136a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6136a-122">CommonParameters</span></span>
<span data-ttu-id="6136a-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6136a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6136a-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6136a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6136a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="6136a-125">INPUTS</span></span>

### <span data-ttu-id="6136a-126">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="6136a-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6136a-127">System.object</span><span class="sxs-lookup"><span data-stu-id="6136a-127">System.String</span></span>

## <span data-ttu-id="6136a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="6136a-128">OUTPUTS</span></span>

### <span data-ttu-id="6136a-129">ServiceManagement. PsApiManagementApiVersionSet （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="6136a-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="6136a-130">筆記</span><span class="sxs-lookup"><span data-stu-id="6136a-130">NOTES</span></span>

## <span data-ttu-id="6136a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="6136a-131">RELATED LINKS</span></span>

[<span data-ttu-id="6136a-132">新-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6136a-132">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="6136a-133">移除-AzureRmApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="6136a-133">Remove-AzureRmApiManagementApiSet</span></span>](./Remove-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="6136a-134">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6136a-134">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiSet.md)
