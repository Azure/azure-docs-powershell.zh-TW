---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: fee978a1500c0fc472ec8015a3e8dbbbdc8015bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276488"
---
# <span data-ttu-id="06499-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="06499-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="06499-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06499-102">SYNOPSIS</span></span>
<span data-ttu-id="06499-103">取得快取的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="06499-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="06499-104">句法</span><span class="sxs-lookup"><span data-stu-id="06499-104">SYNTAX</span></span>

### <span data-ttu-id="06499-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="06499-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06499-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06499-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06499-107">說明</span><span class="sxs-lookup"><span data-stu-id="06499-107">DESCRIPTION</span></span>
<span data-ttu-id="06499-108">取得 Api 管理服務中設定的快取詳細資料。</span><span class="sxs-lookup"><span data-stu-id="06499-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="06499-109">示例</span><span class="sxs-lookup"><span data-stu-id="06499-109">EXAMPLES</span></span>

### <span data-ttu-id="06499-110">範例1：取得所有緩存</span><span class="sxs-lookup"><span data-stu-id="06499-110">Example 1: Get all Caches</span></span>
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

<span data-ttu-id="06499-111">取得 Api 管理服務中設定的所有快取記憶體清單。</span><span class="sxs-lookup"><span data-stu-id="06499-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="06499-112">範例2：取得由識別碼 westus 指定的快取</span><span class="sxs-lookup"><span data-stu-id="06499-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
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

<span data-ttu-id="06499-113">取得為 westus 設定的指定快取詳細資料</span><span class="sxs-lookup"><span data-stu-id="06499-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="06499-114">參數</span><span class="sxs-lookup"><span data-stu-id="06499-114">PARAMETERS</span></span>

### <span data-ttu-id="06499-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="06499-115">-CacheId</span></span>
<span data-ttu-id="06499-116">快取的識別碼。</span><span class="sxs-lookup"><span data-stu-id="06499-116">Identifier of a cache.</span></span>
<span data-ttu-id="06499-117">如果已指定，將會嘗試透過識別碼尋找快取。</span><span class="sxs-lookup"><span data-stu-id="06499-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="06499-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="06499-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="06499-119">-內容</span><span class="sxs-lookup"><span data-stu-id="06499-119">-Context</span></span>
<span data-ttu-id="06499-120">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="06499-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="06499-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="06499-121">This parameter is required.</span></span>

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

### <span data-ttu-id="06499-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06499-122">-DefaultProfile</span></span>
<span data-ttu-id="06499-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="06499-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06499-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06499-124">-ResourceId</span></span>
<span data-ttu-id="06499-125">快取的 [Arm 資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="06499-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="06499-126">如果已指定，將會嘗試透過識別碼尋找快取。</span><span class="sxs-lookup"><span data-stu-id="06499-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="06499-127">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="06499-127">This parameter is required.</span></span>

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

### <span data-ttu-id="06499-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06499-128">CommonParameters</span></span>
<span data-ttu-id="06499-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06499-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06499-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="06499-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06499-131">輸入</span><span class="sxs-lookup"><span data-stu-id="06499-131">INPUTS</span></span>

### <span data-ttu-id="06499-132">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="06499-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="06499-133">System.object</span><span class="sxs-lookup"><span data-stu-id="06499-133">System.String</span></span>

## <span data-ttu-id="06499-134">輸出</span><span class="sxs-lookup"><span data-stu-id="06499-134">OUTPUTS</span></span>

### <span data-ttu-id="06499-135">ServiceManagement. PsApiManagementCache （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="06499-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="06499-136">筆記</span><span class="sxs-lookup"><span data-stu-id="06499-136">NOTES</span></span>

## <span data-ttu-id="06499-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="06499-137">RELATED LINKS</span></span>

[<span data-ttu-id="06499-138">新-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="06499-138">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="06499-139">移除-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="06499-139">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="06499-140">更新-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="06499-140">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
