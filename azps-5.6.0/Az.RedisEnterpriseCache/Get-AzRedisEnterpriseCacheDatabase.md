---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9033082093d571fc60cd9b4c495688d11d87aea8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914654"
---
# <span data-ttu-id="ae6ab-101">Get-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="ae6ab-101">Get-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="ae6ab-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ae6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6ab-103">在 RedisEnterprise 集區中，獲得資料庫相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ae6ab-103">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="ae6ab-104">語法</span><span class="sxs-lookup"><span data-stu-id="ae6ab-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ae6ab-105">描述</span><span class="sxs-lookup"><span data-stu-id="ae6ab-105">DESCRIPTION</span></span>
<span data-ttu-id="ae6ab-106">在 RedisEnterprise 集區中，獲得資料庫相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ae6ab-106">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="ae6ab-107">例子</span><span class="sxs-lookup"><span data-stu-id="ae6ab-107">EXAMPLES</span></span>

### <span data-ttu-id="ae6ab-108">範例 1：取得資料庫</span><span class="sxs-lookup"><span data-stu-id="ae6ab-108">Example 1: Get database</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="ae6ab-109">此命令會獲得名為 MyCache 的 Redis Enterprise Cache 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ae6ab-109">This command gets the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="ae6ab-110">參數</span><span class="sxs-lookup"><span data-stu-id="ae6ab-110">PARAMETERS</span></span>

### <span data-ttu-id="ae6ab-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ae6ab-111">-ClusterName</span></span>
<span data-ttu-id="ae6ab-112">RedisEnterprise 組名。</span><span class="sxs-lookup"><span data-stu-id="ae6ab-112">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae6ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6ab-113">-DefaultProfile</span></span>
<span data-ttu-id="ae6ab-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae6ab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae6ab-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae6ab-115">-ResourceGroupName</span></span>
<span data-ttu-id="ae6ab-116">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae6ab-116">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae6ab-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae6ab-117">-SubscriptionId</span></span>
<span data-ttu-id="ae6ab-118">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="ae6ab-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ae6ab-119">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ae6ab-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae6ab-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6ab-120">CommonParameters</span></span>
<span data-ttu-id="ae6ab-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ae6ab-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6ab-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae6ab-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6ab-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ae6ab-123">INPUTS</span></span>

## <span data-ttu-id="ae6ab-124">輸出</span><span class="sxs-lookup"><span data-stu-id="ae6ab-124">OUTPUTS</span></span>

### <span data-ttu-id="ae6ab-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="ae6ab-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="ae6ab-126">筆記</span><span class="sxs-lookup"><span data-stu-id="ae6ab-126">NOTES</span></span>

<span data-ttu-id="ae6ab-127">別名</span><span class="sxs-lookup"><span data-stu-id="ae6ab-127">ALIASES</span></span>

## <span data-ttu-id="ae6ab-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae6ab-128">RELATED LINKS</span></span>

