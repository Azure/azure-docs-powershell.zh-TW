---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 99956b752b71309278af4c1f9b43b8efa9015f21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435589"
---
# <span data-ttu-id="e5f32-101">Get-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="e5f32-101">Get-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="e5f32-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5f32-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f32-103">取得 RedisEnterprise 群集中資料庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e5f32-103">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="e5f32-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5f32-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e5f32-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5f32-105">DESCRIPTION</span></span>
<span data-ttu-id="e5f32-106">取得 RedisEnterprise 群集中資料庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e5f32-106">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="e5f32-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5f32-107">EXAMPLES</span></span>

### <span data-ttu-id="e5f32-108">範例1：取得資料庫</span><span class="sxs-lookup"><span data-stu-id="e5f32-108">Example 1: Get database</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="e5f32-109">這個命令會取得名為 MyCache 之 Redis Enterprise Cache 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="e5f32-109">This command gets the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="e5f32-110">參數</span><span class="sxs-lookup"><span data-stu-id="e5f32-110">PARAMETERS</span></span>

### <span data-ttu-id="e5f32-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e5f32-111">-ClusterName</span></span>
<span data-ttu-id="e5f32-112">RedisEnterprise 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5f32-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="e5f32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f32-113">-DefaultProfile</span></span>
<span data-ttu-id="e5f32-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5f32-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5f32-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5f32-115">-ResourceGroupName</span></span>
<span data-ttu-id="e5f32-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5f32-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="e5f32-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5f32-117">-SubscriptionId</span></span>
<span data-ttu-id="e5f32-118">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e5f32-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e5f32-119">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e5f32-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e5f32-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f32-120">CommonParameters</span></span>
<span data-ttu-id="e5f32-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5f32-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f32-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e5f32-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f32-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e5f32-123">INPUTS</span></span>

## <span data-ttu-id="e5f32-124">輸出</span><span class="sxs-lookup"><span data-stu-id="e5f32-124">OUTPUTS</span></span>

### <span data-ttu-id="e5f32-125">IDatabase （RedisEnterpriseCache）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="e5f32-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="e5f32-126">筆記</span><span class="sxs-lookup"><span data-stu-id="e5f32-126">NOTES</span></span>

<span data-ttu-id="e5f32-127">別名</span><span class="sxs-lookup"><span data-stu-id="e5f32-127">ALIASES</span></span>

## <span data-ttu-id="e5f32-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5f32-128">RELATED LINKS</span></span>

