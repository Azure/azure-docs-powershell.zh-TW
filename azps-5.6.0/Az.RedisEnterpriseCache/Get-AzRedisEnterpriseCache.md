---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: fd127005107586e31798d215d7f54888b26705c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914662"
---
# <span data-ttu-id="f077e-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="f077e-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="f077e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f077e-102">SYNOPSIS</span></span>
<span data-ttu-id="f077e-103">獲得 RedisEnterprise 集區及其關聯資料庫的資訊</span><span class="sxs-lookup"><span data-stu-id="f077e-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="f077e-104">語法</span><span class="sxs-lookup"><span data-stu-id="f077e-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f077e-105">描述</span><span class="sxs-lookup"><span data-stu-id="f077e-105">DESCRIPTION</span></span>
<span data-ttu-id="f077e-106">獲得 RedisEnterprise 集區及其關聯資料庫的資訊</span><span class="sxs-lookup"><span data-stu-id="f077e-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="f077e-107">例子</span><span class="sxs-lookup"><span data-stu-id="f077e-107">EXAMPLES</span></span>

### <span data-ttu-id="f077e-108">範例 1：取得 Redis Enterprise Cache by name</span><span class="sxs-lookup"><span data-stu-id="f077e-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="f077e-109">此命令會獲得名為 MyCache 的 Redis Enterprise Cache。</span><span class="sxs-lookup"><span data-stu-id="f077e-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="f077e-110">範例 2：在資源群組中取得每個 Redis Enterprise Cache</span><span class="sxs-lookup"><span data-stu-id="f077e-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="f077e-111">此命令會獲得指定資源群組中每個 Redis Enterprise Cache。</span><span class="sxs-lookup"><span data-stu-id="f077e-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="f077e-112">參數</span><span class="sxs-lookup"><span data-stu-id="f077e-112">PARAMETERS</span></span>

### <span data-ttu-id="f077e-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f077e-113">-ClusterName</span></span>
<span data-ttu-id="f077e-114">RedisEnterprise 組名。</span><span class="sxs-lookup"><span data-stu-id="f077e-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="f077e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f077e-115">-DefaultProfile</span></span>
<span data-ttu-id="f077e-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f077e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f077e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f077e-117">-ResourceGroupName</span></span>
<span data-ttu-id="f077e-118">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f077e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="f077e-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f077e-119">-SubscriptionId</span></span>
<span data-ttu-id="f077e-120">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f077e-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f077e-121">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f077e-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f077e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f077e-122">CommonParameters</span></span>
<span data-ttu-id="f077e-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f077e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f077e-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f077e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f077e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f077e-125">INPUTS</span></span>

## <span data-ttu-id="f077e-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f077e-126">OUTPUTS</span></span>

### <span data-ttu-id="f077e-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="f077e-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="f077e-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f077e-128">NOTES</span></span>

<span data-ttu-id="f077e-129">別名</span><span class="sxs-lookup"><span data-stu-id="f077e-129">ALIASES</span></span>

## <span data-ttu-id="f077e-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="f077e-130">RELATED LINKS</span></span>

