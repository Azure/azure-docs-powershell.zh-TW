---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: ff635c55600c6528ecad537b74a843e2d1da830e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914653"
---
# <span data-ttu-id="9eb10-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="9eb10-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="9eb10-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9eb10-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb10-103">取得 RedisEnterprise 資料庫的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="9eb10-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="9eb10-104">語法</span><span class="sxs-lookup"><span data-stu-id="9eb10-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9eb10-105">描述</span><span class="sxs-lookup"><span data-stu-id="9eb10-105">DESCRIPTION</span></span>
<span data-ttu-id="9eb10-106">取得 RedisEnterprise 資料庫的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="9eb10-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="9eb10-107">例子</span><span class="sxs-lookup"><span data-stu-id="9eb10-107">EXAMPLES</span></span>

### <span data-ttu-id="9eb10-108">範例 1：取得資料庫便捷鍵</span><span class="sxs-lookup"><span data-stu-id="9eb10-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="9eb10-109">此命令會取得用於驗證 Redis Enterprise Cache 資料庫之 MyCache 之資料庫的驗證便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="9eb10-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="9eb10-110">參數</span><span class="sxs-lookup"><span data-stu-id="9eb10-110">PARAMETERS</span></span>

### <span data-ttu-id="9eb10-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9eb10-111">-ClusterName</span></span>
<span data-ttu-id="9eb10-112">RedisEnterprise 組名。</span><span class="sxs-lookup"><span data-stu-id="9eb10-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="9eb10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb10-113">-DefaultProfile</span></span>
<span data-ttu-id="9eb10-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9eb10-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eb10-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eb10-115">-ResourceGroupName</span></span>
<span data-ttu-id="9eb10-116">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9eb10-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="9eb10-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9eb10-117">-SubscriptionId</span></span>
<span data-ttu-id="9eb10-118">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="9eb10-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9eb10-119">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="9eb10-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9eb10-120">-確認</span><span class="sxs-lookup"><span data-stu-id="9eb10-120">-Confirm</span></span>
<span data-ttu-id="9eb10-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9eb10-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eb10-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eb10-122">-WhatIf</span></span>
<span data-ttu-id="9eb10-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9eb10-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eb10-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9eb10-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eb10-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb10-125">CommonParameters</span></span>
<span data-ttu-id="9eb10-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9eb10-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb10-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9eb10-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb10-128">輸入</span><span class="sxs-lookup"><span data-stu-id="9eb10-128">INPUTS</span></span>

## <span data-ttu-id="9eb10-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9eb10-129">OUTPUTS</span></span>

### <span data-ttu-id="9eb10-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="9eb10-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="9eb10-131">筆記</span><span class="sxs-lookup"><span data-stu-id="9eb10-131">NOTES</span></span>

<span data-ttu-id="9eb10-132">別名</span><span class="sxs-lookup"><span data-stu-id="9eb10-132">ALIASES</span></span>

## <span data-ttu-id="9eb10-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="9eb10-133">RELATED LINKS</span></span>

