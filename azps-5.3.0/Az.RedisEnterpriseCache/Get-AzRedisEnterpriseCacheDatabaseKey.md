---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: e602cb4fc86ede6a4e1f7cc894c1825fd1d560fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435587"
---
# <span data-ttu-id="64348-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="64348-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="64348-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64348-102">SYNOPSIS</span></span>
<span data-ttu-id="64348-103">檢索 RedisEnterprise 資料庫的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="64348-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="64348-104">句法</span><span class="sxs-lookup"><span data-stu-id="64348-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64348-105">說明</span><span class="sxs-lookup"><span data-stu-id="64348-105">DESCRIPTION</span></span>
<span data-ttu-id="64348-106">檢索 RedisEnterprise 資料庫的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="64348-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="64348-107">示例</span><span class="sxs-lookup"><span data-stu-id="64348-107">EXAMPLES</span></span>

### <span data-ttu-id="64348-108">範例1：取得資料庫便捷鍵</span><span class="sxs-lookup"><span data-stu-id="64348-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="64348-109">這個命令會取得用來驗證連線至 Redis Enterprise Cache （名為 MyCache）資料庫之連線的機密便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="64348-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="64348-110">參數</span><span class="sxs-lookup"><span data-stu-id="64348-110">PARAMETERS</span></span>

### <span data-ttu-id="64348-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="64348-111">-ClusterName</span></span>
<span data-ttu-id="64348-112">RedisEnterprise 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="64348-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="64348-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64348-113">-DefaultProfile</span></span>
<span data-ttu-id="64348-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="64348-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64348-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64348-115">-ResourceGroupName</span></span>
<span data-ttu-id="64348-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="64348-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="64348-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64348-117">-SubscriptionId</span></span>
<span data-ttu-id="64348-118">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="64348-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="64348-119">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="64348-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="64348-120">-確認</span><span class="sxs-lookup"><span data-stu-id="64348-120">-Confirm</span></span>
<span data-ttu-id="64348-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="64348-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64348-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64348-122">-WhatIf</span></span>
<span data-ttu-id="64348-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64348-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64348-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64348-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64348-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64348-125">CommonParameters</span></span>
<span data-ttu-id="64348-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64348-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64348-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="64348-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64348-128">輸入</span><span class="sxs-lookup"><span data-stu-id="64348-128">INPUTS</span></span>

## <span data-ttu-id="64348-129">輸出</span><span class="sxs-lookup"><span data-stu-id="64348-129">OUTPUTS</span></span>

### <span data-ttu-id="64348-130">IAccessKeys （RedisEnterpriseCache）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="64348-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="64348-131">筆記</span><span class="sxs-lookup"><span data-stu-id="64348-131">NOTES</span></span>

<span data-ttu-id="64348-132">別名</span><span class="sxs-lookup"><span data-stu-id="64348-132">ALIASES</span></span>

## <span data-ttu-id="64348-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="64348-133">RELATED LINKS</span></span>

