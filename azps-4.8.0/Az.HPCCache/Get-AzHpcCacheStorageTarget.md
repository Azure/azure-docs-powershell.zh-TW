---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971069"
---
# <span data-ttu-id="3a3a6-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="3a3a6-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="3a3a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="3a3a6-103">取得 HPC 快取儲存空間目標 (s）) 。</span><span class="sxs-lookup"><span data-stu-id="3a3a6-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="3a3a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a3a6-104">SYNTAX</span></span>

### <span data-ttu-id="3a3a6-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3a3a6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a3a6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a3a6-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a3a6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a3a6-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a3a6-108">說明</span><span class="sxs-lookup"><span data-stu-id="3a3a6-108">DESCRIPTION</span></span>
<span data-ttu-id="3a3a6-109">AzHpcCacheStorageTarget Cmdlet 會取得在 **快取** 上存在的存儲目標 (s) 。</span><span class="sxs-lookup"><span data-stu-id="3a3a6-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="3a3a6-110">示例</span><span class="sxs-lookup"><span data-stu-id="3a3a6-110">EXAMPLES</span></span>

### <span data-ttu-id="3a3a6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3a3a6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="3a3a6-112">範例2</span><span class="sxs-lookup"><span data-stu-id="3a3a6-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="3a3a6-113">參數</span><span class="sxs-lookup"><span data-stu-id="3a3a6-113">PARAMETERS</span></span>

### <span data-ttu-id="3a3a6-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="3a3a6-114">-CacheId</span></span>
<span data-ttu-id="3a3a6-115">快取的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3a3a6-115">The resource id of the Cache</span></span>

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

### <span data-ttu-id="3a3a6-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="3a3a6-116">-CacheName</span></span>
<span data-ttu-id="3a3a6-117">快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3a6-117">Name of cache.</span></span>

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

### <span data-ttu-id="3a3a6-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="3a3a6-118">-CacheObject</span></span>
<span data-ttu-id="3a3a6-119">要開始的快取物件。</span><span class="sxs-lookup"><span data-stu-id="3a3a6-119">The cache object to start.</span></span>

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

### <span data-ttu-id="3a3a6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a3a6-120">-DefaultProfile</span></span>
<span data-ttu-id="3a3a6-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a3a6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a3a6-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a3a6-122">-Name</span></span>
<span data-ttu-id="3a3a6-123">儲存目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3a6-123">Name of storage target.</span></span>

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

### <span data-ttu-id="3a3a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a3a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="3a3a6-125">資源群組快取的名稱是。</span><span class="sxs-lookup"><span data-stu-id="3a3a6-125">Name of resource group cache is in.</span></span>


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

### <span data-ttu-id="3a3a6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a3a6-126">CommonParameters</span></span>
<span data-ttu-id="3a3a6-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a3a6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a3a6-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3a3a6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a3a6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3a3a6-129">INPUTS</span></span>

### <span data-ttu-id="3a3a6-130">System.object</span><span class="sxs-lookup"><span data-stu-id="3a3a6-130">System.String</span></span>

## <span data-ttu-id="3a3a6-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3a3a6-131">OUTPUTS</span></span>

### <span data-ttu-id="3a3a6-132">PSHpcStorageTarget （HPCCache）的</span><span class="sxs-lookup"><span data-stu-id="3a3a6-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="3a3a6-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3a3a6-133">NOTES</span></span>

## <span data-ttu-id="3a3a6-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a3a6-134">RELATED LINKS</span></span>