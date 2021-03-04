---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 3576cfb8185898ea7bb0fa2052a18b651d1d5cc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914665"
---
# <span data-ttu-id="30bc7-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="30bc7-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="30bc7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="30bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="30bc7-103">從目標資料庫匯出資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="30bc7-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="30bc7-104">語法</span><span class="sxs-lookup"><span data-stu-id="30bc7-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="30bc7-105">描述</span><span class="sxs-lookup"><span data-stu-id="30bc7-105">DESCRIPTION</span></span>
<span data-ttu-id="30bc7-106">從目標資料庫匯出資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="30bc7-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="30bc7-107">例子</span><span class="sxs-lookup"><span data-stu-id="30bc7-107">EXAMPLES</span></span>

### <span data-ttu-id="30bc7-108">範例 1：匯出資料庫</span><span class="sxs-lookup"><span data-stu-id="30bc7-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="30bc7-109">此命令會匯出名為 MyCache 的 Redis Enterprise Cache 資料庫至資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="30bc7-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="30bc7-110">參數</span><span class="sxs-lookup"><span data-stu-id="30bc7-110">PARAMETERS</span></span>

### <span data-ttu-id="30bc7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30bc7-111">-AsJob</span></span>
<span data-ttu-id="30bc7-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="30bc7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="30bc7-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="30bc7-113">-ClusterName</span></span>
<span data-ttu-id="30bc7-114">RedisEnterprise 組名。</span><span class="sxs-lookup"><span data-stu-id="30bc7-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="30bc7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30bc7-115">-DefaultProfile</span></span>
<span data-ttu-id="30bc7-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="30bc7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30bc7-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="30bc7-117">-NoWait</span></span>
<span data-ttu-id="30bc7-118">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="30bc7-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="30bc7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30bc7-119">-PassThru</span></span>
<span data-ttu-id="30bc7-120">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="30bc7-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="30bc7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30bc7-121">-ResourceGroupName</span></span>
<span data-ttu-id="30bc7-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="30bc7-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="30bc7-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="30bc7-123">-SasUri</span></span>
<span data-ttu-id="30bc7-124">要匯出的目標目錄的 SAS Uri</span><span class="sxs-lookup"><span data-stu-id="30bc7-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="30bc7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30bc7-125">-SubscriptionId</span></span>
<span data-ttu-id="30bc7-126">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="30bc7-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="30bc7-127">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="30bc7-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="30bc7-128">-確認</span><span class="sxs-lookup"><span data-stu-id="30bc7-128">-Confirm</span></span>
<span data-ttu-id="30bc7-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="30bc7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30bc7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30bc7-130">-WhatIf</span></span>
<span data-ttu-id="30bc7-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30bc7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30bc7-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30bc7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30bc7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30bc7-133">CommonParameters</span></span>
<span data-ttu-id="30bc7-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="30bc7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30bc7-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30bc7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30bc7-136">輸入</span><span class="sxs-lookup"><span data-stu-id="30bc7-136">INPUTS</span></span>

## <span data-ttu-id="30bc7-137">輸出</span><span class="sxs-lookup"><span data-stu-id="30bc7-137">OUTPUTS</span></span>

### <span data-ttu-id="30bc7-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="30bc7-138">System.Boolean</span></span>

## <span data-ttu-id="30bc7-139">筆記</span><span class="sxs-lookup"><span data-stu-id="30bc7-139">NOTES</span></span>

<span data-ttu-id="30bc7-140">別名</span><span class="sxs-lookup"><span data-stu-id="30bc7-140">ALIASES</span></span>

## <span data-ttu-id="30bc7-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="30bc7-141">RELATED LINKS</span></span>

