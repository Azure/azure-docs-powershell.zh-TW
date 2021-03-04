---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: 53a164b2cd3421898974f7f5f1c2fd2b7ed51c21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903382"
---
# <span data-ttu-id="27d3c-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="27d3c-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="27d3c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="27d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="27d3c-103">取得快緩存的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="27d3c-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="27d3c-104">語法</span><span class="sxs-lookup"><span data-stu-id="27d3c-104">SYNTAX</span></span>

### <span data-ttu-id="27d3c-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="27d3c-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27d3c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27d3c-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27d3c-107">描述</span><span class="sxs-lookup"><span data-stu-id="27d3c-107">DESCRIPTION</span></span>
<span data-ttu-id="27d3c-108">取得 Api 管理服務中已配置的快處理詳細資料。</span><span class="sxs-lookup"><span data-stu-id="27d3c-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="27d3c-109">例子</span><span class="sxs-lookup"><span data-stu-id="27d3c-109">EXAMPLES</span></span>

### <span data-ttu-id="27d3c-110">範例 1：取得所有快點</span><span class="sxs-lookup"><span data-stu-id="27d3c-110">Example 1: Get all Caches</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-West-US
ServiceName       : contoso
```

<span data-ttu-id="27d3c-111">在 Api 管理服務中，獲得所有已配置的緩存清單。</span><span class="sxs-lookup"><span data-stu-id="27d3c-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="27d3c-112">範例 2：取得識別碼 westus 指定的快</span><span class="sxs-lookup"><span data-stu-id="27d3c-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext -cacheId westus
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="27d3c-113">取得為 westus 所配置的指定快快詳細資料</span><span class="sxs-lookup"><span data-stu-id="27d3c-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="27d3c-114">參數</span><span class="sxs-lookup"><span data-stu-id="27d3c-114">PARAMETERS</span></span>

### <span data-ttu-id="27d3c-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="27d3c-115">-CacheId</span></span>
<span data-ttu-id="27d3c-116">緩存的識別碼。</span><span class="sxs-lookup"><span data-stu-id="27d3c-116">Identifier of a cache.</span></span>
<span data-ttu-id="27d3c-117">如果指定，會嘗試根據識別碼尋找緩存。</span><span class="sxs-lookup"><span data-stu-id="27d3c-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="27d3c-118">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="27d3c-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="27d3c-119">-內容</span><span class="sxs-lookup"><span data-stu-id="27d3c-119">-Context</span></span>
<span data-ttu-id="27d3c-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="27d3c-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="27d3c-121">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="27d3c-121">This parameter is required.</span></span>

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

### <span data-ttu-id="27d3c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d3c-122">-DefaultProfile</span></span>
<span data-ttu-id="27d3c-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="27d3c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27d3c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27d3c-124">-ResourceId</span></span>
<span data-ttu-id="27d3c-125">緩存的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="27d3c-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="27d3c-126">如果指定，會嘗試根據識別碼尋找緩存。</span><span class="sxs-lookup"><span data-stu-id="27d3c-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="27d3c-127">此參數為必填專案。</span><span class="sxs-lookup"><span data-stu-id="27d3c-127">This parameter is required.</span></span>

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

### <span data-ttu-id="27d3c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27d3c-128">CommonParameters</span></span>
<span data-ttu-id="27d3c-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="27d3c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27d3c-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27d3c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27d3c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="27d3c-131">INPUTS</span></span>

### <span data-ttu-id="27d3c-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="27d3c-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="27d3c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="27d3c-133">System.String</span></span>

## <span data-ttu-id="27d3c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="27d3c-134">OUTPUTS</span></span>

### <span data-ttu-id="27d3c-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="27d3c-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="27d3c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="27d3c-136">NOTES</span></span>

## <span data-ttu-id="27d3c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="27d3c-137">RELATED LINKS</span></span>

[<span data-ttu-id="27d3c-138">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="27d3c-138">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="27d3c-139">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="27d3c-139">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="27d3c-140">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="27d3c-140">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
