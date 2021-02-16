---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: a6fe478aa8221060974f54e75b63a64edf0beae4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141902"
---
# <span data-ttu-id="376b9-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="376b9-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="376b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="376b9-102">SYNOPSIS</span></span>
<span data-ttu-id="376b9-103">取得 RedisEnterprise 群集及其關聯資料庫的相關資訊</span><span class="sxs-lookup"><span data-stu-id="376b9-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="376b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="376b9-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="376b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="376b9-105">DESCRIPTION</span></span>
<span data-ttu-id="376b9-106">取得 RedisEnterprise 群集及其關聯資料庫的相關資訊</span><span class="sxs-lookup"><span data-stu-id="376b9-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="376b9-107">示例</span><span class="sxs-lookup"><span data-stu-id="376b9-107">EXAMPLES</span></span>

### <span data-ttu-id="376b9-108">範例1：透過名稱取得 Redis Enterprise Cache</span><span class="sxs-lookup"><span data-stu-id="376b9-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="376b9-109">這個命令會取得名為 MyCache 的 Redis 企業版快取。</span><span class="sxs-lookup"><span data-stu-id="376b9-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="376b9-110">範例2：在資源群組中取得每個 Redis Enterprise Cache</span><span class="sxs-lookup"><span data-stu-id="376b9-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="376b9-111">這個命令會在指定的資源群組中取得每個 Redis 企業版快取。</span><span class="sxs-lookup"><span data-stu-id="376b9-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="376b9-112">參數</span><span class="sxs-lookup"><span data-stu-id="376b9-112">PARAMETERS</span></span>

### <span data-ttu-id="376b9-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="376b9-113">-ClusterName</span></span>
<span data-ttu-id="376b9-114">RedisEnterprise 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="376b9-114">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="376b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376b9-115">-DefaultProfile</span></span>
<span data-ttu-id="376b9-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="376b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="376b9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="376b9-117">-ResourceGroupName</span></span>
<span data-ttu-id="376b9-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="376b9-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="376b9-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="376b9-119">-SubscriptionId</span></span>
<span data-ttu-id="376b9-120">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="376b9-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="376b9-121">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="376b9-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="376b9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376b9-122">CommonParameters</span></span>
<span data-ttu-id="376b9-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="376b9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376b9-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="376b9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376b9-125">輸入</span><span class="sxs-lookup"><span data-stu-id="376b9-125">INPUTS</span></span>

## <span data-ttu-id="376b9-126">輸出</span><span class="sxs-lookup"><span data-stu-id="376b9-126">OUTPUTS</span></span>

### <span data-ttu-id="376b9-127">ICluster （RedisEnterpriseCache）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="376b9-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="376b9-128">筆記</span><span class="sxs-lookup"><span data-stu-id="376b9-128">NOTES</span></span>

<span data-ttu-id="376b9-129">別名</span><span class="sxs-lookup"><span data-stu-id="376b9-129">ALIASES</span></span>

## <span data-ttu-id="376b9-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="376b9-130">RELATED LINKS</span></span>

