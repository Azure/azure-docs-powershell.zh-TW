---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/new-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: 3d28515ede93abf2ebb5be8bad2e961f2e22b572
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914642"
---
# <span data-ttu-id="879e7-101">New-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="879e7-101">New-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="879e7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="879e7-102">SYNOPSIS</span></span>
<span data-ttu-id="879e7-103">重新產生 RedisEnterprise 資料庫的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="879e7-103">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="879e7-104">語法</span><span class="sxs-lookup"><span data-stu-id="879e7-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 -KeyType <AccessKeyType> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="879e7-105">描述</span><span class="sxs-lookup"><span data-stu-id="879e7-105">DESCRIPTION</span></span>
<span data-ttu-id="879e7-106">重新產生 RedisEnterprise 資料庫的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="879e7-106">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="879e7-107">例子</span><span class="sxs-lookup"><span data-stu-id="879e7-107">EXAMPLES</span></span>

### <span data-ttu-id="879e7-108">範例 1：重新產生主便捷鍵</span><span class="sxs-lookup"><span data-stu-id="879e7-108">Example 1: Regenerate primary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Primary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
new-primary-key                              secondary-key

```

<span data-ttu-id="879e7-109">此命令會重新產生用於驗證 Redis Enterprise Cache 資料庫之 MyCache 之資料庫之連結的主機密便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="879e7-109">This command regenerates the primary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="879e7-110">範例 2：重新產生次要便捷鍵</span><span class="sxs-lookup"><span data-stu-id="879e7-110">Example 2: Regenerate secondary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Secondary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  new-secondary-key

```

<span data-ttu-id="879e7-111">此命令會重新產生次要的機密便捷鍵，用於驗證 Redis Enterprise Cache 資料庫的 MyCache。</span><span class="sxs-lookup"><span data-stu-id="879e7-111">This command regenerates the secondary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="879e7-112">參數</span><span class="sxs-lookup"><span data-stu-id="879e7-112">PARAMETERS</span></span>

### <span data-ttu-id="879e7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="879e7-113">-AsJob</span></span>
<span data-ttu-id="879e7-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="879e7-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="879e7-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="879e7-115">-ClusterName</span></span>
<span data-ttu-id="879e7-116">RedisEnterprise 組名。</span><span class="sxs-lookup"><span data-stu-id="879e7-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="879e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="879e7-117">-DefaultProfile</span></span>
<span data-ttu-id="879e7-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="879e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="879e7-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="879e7-119">-KeyType</span></span>
<span data-ttu-id="879e7-120">要重新產生哪個便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="879e7-120">Which access key to regenerate.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.AccessKeyType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="879e7-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="879e7-121">-NoWait</span></span>
<span data-ttu-id="879e7-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="879e7-122">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="879e7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="879e7-123">-ResourceGroupName</span></span>
<span data-ttu-id="879e7-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="879e7-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="879e7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="879e7-125">-SubscriptionId</span></span>
<span data-ttu-id="879e7-126">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="879e7-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="879e7-127">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="879e7-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="879e7-128">-確認</span><span class="sxs-lookup"><span data-stu-id="879e7-128">-Confirm</span></span>
<span data-ttu-id="879e7-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="879e7-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="879e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="879e7-130">-WhatIf</span></span>
<span data-ttu-id="879e7-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="879e7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="879e7-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="879e7-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="879e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="879e7-133">CommonParameters</span></span>
<span data-ttu-id="879e7-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="879e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="879e7-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="879e7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="879e7-136">輸入</span><span class="sxs-lookup"><span data-stu-id="879e7-136">INPUTS</span></span>

## <span data-ttu-id="879e7-137">輸出</span><span class="sxs-lookup"><span data-stu-id="879e7-137">OUTPUTS</span></span>

### <span data-ttu-id="879e7-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="879e7-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="879e7-139">筆記</span><span class="sxs-lookup"><span data-stu-id="879e7-139">NOTES</span></span>

<span data-ttu-id="879e7-140">別名</span><span class="sxs-lookup"><span data-stu-id="879e7-140">ALIASES</span></span>

## <span data-ttu-id="879e7-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="879e7-141">RELATED LINKS</span></span>

