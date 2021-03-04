---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: 6fb1e00f74bcd170d8117e4e37655da6c275a62f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911117"
---
# <span data-ttu-id="4e407-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="4e407-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="4e407-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4e407-102">SYNOPSIS</span></span>
<span data-ttu-id="4e407-103">取得 HPC 快 (目標) 。</span><span class="sxs-lookup"><span data-stu-id="4e407-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="4e407-104">語法</span><span class="sxs-lookup"><span data-stu-id="4e407-104">SYNTAX</span></span>

### <span data-ttu-id="4e407-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4e407-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e407-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e407-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e407-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e407-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e407-108">描述</span><span class="sxs-lookup"><span data-stu-id="4e407-108">DESCRIPTION</span></span>
<span data-ttu-id="4e407-109">**Get-AzHpcCacheStorageTarget** Cmdlet 會取得 (快) 的儲存目標。</span><span class="sxs-lookup"><span data-stu-id="4e407-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="4e407-110">例子</span><span class="sxs-lookup"><span data-stu-id="4e407-110">EXAMPLES</span></span>

### <span data-ttu-id="4e407-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="4e407-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="4e407-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="4e407-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="4e407-113">參數</span><span class="sxs-lookup"><span data-stu-id="4e407-113">PARAMETERS</span></span>

### <span data-ttu-id="4e407-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="4e407-114">-CacheId</span></span>
<span data-ttu-id="4e407-115">Cache 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4e407-115">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e407-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="4e407-116">-CacheName</span></span>
<span data-ttu-id="4e407-117">緩存名稱。</span><span class="sxs-lookup"><span data-stu-id="4e407-117">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e407-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="4e407-118">-CacheObject</span></span>
<span data-ttu-id="4e407-119">要啟動的緩存物件。</span><span class="sxs-lookup"><span data-stu-id="4e407-119">The cache object to start.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e407-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e407-120">-DefaultProfile</span></span>
<span data-ttu-id="4e407-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e407-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e407-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e407-122">-Name</span></span>
<span data-ttu-id="4e407-123">儲存目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e407-123">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: StorageTargetName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e407-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e407-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e407-125">其中的資源群組緩存名稱。</span><span class="sxs-lookup"><span data-stu-id="4e407-125">Name of resource group cache is in.</span></span>


```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e407-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e407-126">CommonParameters</span></span>
<span data-ttu-id="4e407-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4e407-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e407-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e407-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e407-129">輸入</span><span class="sxs-lookup"><span data-stu-id="4e407-129">INPUTS</span></span>

### <span data-ttu-id="4e407-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4e407-130">System.String</span></span>

## <span data-ttu-id="4e407-131">輸出</span><span class="sxs-lookup"><span data-stu-id="4e407-131">OUTPUTS</span></span>

### <span data-ttu-id="4e407-132">Microsoft.Azure.PowerShell.Cmdlets.HPCache.models.PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="4e407-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="4e407-133">筆記</span><span class="sxs-lookup"><span data-stu-id="4e407-133">NOTES</span></span>

## <span data-ttu-id="4e407-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e407-134">RELATED LINKS</span></span>
