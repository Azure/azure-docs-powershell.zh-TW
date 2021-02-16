---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: ab5985a7302834f4f7184a43ac2f5ebf795a3d83
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139995"
---
# <span data-ttu-id="3275f-101">New-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="3275f-101">New-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="3275f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3275f-102">SYNOPSIS</span></span>
<span data-ttu-id="3275f-103">再生 RedisEnterprise 資料庫的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="3275f-103">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="3275f-104">句法</span><span class="sxs-lookup"><span data-stu-id="3275f-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 -KeyType <AccessKeyType> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3275f-105">說明</span><span class="sxs-lookup"><span data-stu-id="3275f-105">DESCRIPTION</span></span>
<span data-ttu-id="3275f-106">再生 RedisEnterprise 資料庫的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="3275f-106">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="3275f-107">示例</span><span class="sxs-lookup"><span data-stu-id="3275f-107">EXAMPLES</span></span>

### <span data-ttu-id="3275f-108">範例1：重新產生主要便捷鍵</span><span class="sxs-lookup"><span data-stu-id="3275f-108">Example 1: Regenerate primary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Primary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
new-primary-key                              secondary-key

```

<span data-ttu-id="3275f-109">這個命令會重新產生主要的機密存取金鑰，以用於驗證連線至 Redis Enterprise Cache （名為 MyCache）資料庫的連線。</span><span class="sxs-lookup"><span data-stu-id="3275f-109">This command regenerates the primary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="3275f-110">範例2：重新產生副便捷鍵</span><span class="sxs-lookup"><span data-stu-id="3275f-110">Example 2: Regenerate secondary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Secondary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  new-secondary-key

```

<span data-ttu-id="3275f-111">這個命令會重新產生次要機密存取金鑰，以用於驗證名為 MyCache 之 Redis Enterprise Cache 之資料庫的連線。</span><span class="sxs-lookup"><span data-stu-id="3275f-111">This command regenerates the secondary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="3275f-112">參數</span><span class="sxs-lookup"><span data-stu-id="3275f-112">PARAMETERS</span></span>

### <span data-ttu-id="3275f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3275f-113">-AsJob</span></span>
<span data-ttu-id="3275f-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="3275f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3275f-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3275f-115">-ClusterName</span></span>
<span data-ttu-id="3275f-116">RedisEnterprise 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="3275f-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="3275f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3275f-117">-DefaultProfile</span></span>
<span data-ttu-id="3275f-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3275f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3275f-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3275f-119">-KeyType</span></span>
<span data-ttu-id="3275f-120">要重新產生的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="3275f-120">Which access key to regenerate.</span></span>

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

### <span data-ttu-id="3275f-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3275f-121">-NoWait</span></span>
<span data-ttu-id="3275f-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="3275f-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3275f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3275f-123">-ResourceGroupName</span></span>
<span data-ttu-id="3275f-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3275f-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="3275f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3275f-125">-SubscriptionId</span></span>
<span data-ttu-id="3275f-126">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="3275f-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3275f-127">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="3275f-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3275f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="3275f-128">-Confirm</span></span>
<span data-ttu-id="3275f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3275f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3275f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3275f-130">-WhatIf</span></span>
<span data-ttu-id="3275f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3275f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3275f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3275f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3275f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3275f-133">CommonParameters</span></span>
<span data-ttu-id="3275f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3275f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3275f-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3275f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3275f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="3275f-136">INPUTS</span></span>

## <span data-ttu-id="3275f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="3275f-137">OUTPUTS</span></span>

### <span data-ttu-id="3275f-138">IAccessKeys （RedisEnterpriseCache）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="3275f-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="3275f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="3275f-139">NOTES</span></span>

<span data-ttu-id="3275f-140">別名</span><span class="sxs-lookup"><span data-stu-id="3275f-140">ALIASES</span></span>

## <span data-ttu-id="3275f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="3275f-141">RELATED LINKS</span></span>

