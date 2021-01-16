---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 1e50bba7c00c94daac983511f6fcea0ed1319759
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435593"
---
# <span data-ttu-id="1b5d2-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="1b5d2-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="1b5d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="1b5d2-103">從目標資料庫匯出資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="1b5d2-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="1b5d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b5d2-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1b5d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="1b5d2-105">DESCRIPTION</span></span>
<span data-ttu-id="1b5d2-106">從目標資料庫匯出資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="1b5d2-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="1b5d2-107">示例</span><span class="sxs-lookup"><span data-stu-id="1b5d2-107">EXAMPLES</span></span>

### <span data-ttu-id="1b5d2-108">範例1：匯出資料庫</span><span class="sxs-lookup"><span data-stu-id="1b5d2-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="1b5d2-109">這個命令會將名為 MyCache 的 Redis Enterprise Cache 資料庫匯出至資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="1b5d2-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="1b5d2-110">參數</span><span class="sxs-lookup"><span data-stu-id="1b5d2-110">PARAMETERS</span></span>

### <span data-ttu-id="1b5d2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b5d2-111">-AsJob</span></span>
<span data-ttu-id="1b5d2-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="1b5d2-112">Run the command as a job</span></span>

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

### <span data-ttu-id="1b5d2-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1b5d2-113">-ClusterName</span></span>
<span data-ttu-id="1b5d2-114">RedisEnterprise 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b5d2-114">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="1b5d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b5d2-115">-DefaultProfile</span></span>
<span data-ttu-id="1b5d2-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b5d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b5d2-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1b5d2-117">-NoWait</span></span>
<span data-ttu-id="1b5d2-118">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="1b5d2-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1b5d2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b5d2-119">-PassThru</span></span>
<span data-ttu-id="1b5d2-120">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="1b5d2-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1b5d2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b5d2-121">-ResourceGroupName</span></span>
<span data-ttu-id="1b5d2-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b5d2-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="1b5d2-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="1b5d2-123">-SasUri</span></span>
<span data-ttu-id="1b5d2-124">要匯出到的目標目錄的 SAS Uri</span><span class="sxs-lookup"><span data-stu-id="1b5d2-124">SAS Uri for the target directory to export to</span></span>

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

### <span data-ttu-id="1b5d2-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b5d2-125">-SubscriptionId</span></span>
<span data-ttu-id="1b5d2-126">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="1b5d2-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1b5d2-127">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="1b5d2-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1b5d2-128">-確認</span><span class="sxs-lookup"><span data-stu-id="1b5d2-128">-Confirm</span></span>
<span data-ttu-id="1b5d2-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1b5d2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b5d2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b5d2-130">-WhatIf</span></span>
<span data-ttu-id="1b5d2-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1b5d2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b5d2-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1b5d2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b5d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b5d2-133">CommonParameters</span></span>
<span data-ttu-id="1b5d2-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b5d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b5d2-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1b5d2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b5d2-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1b5d2-136">INPUTS</span></span>

## <span data-ttu-id="1b5d2-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1b5d2-137">OUTPUTS</span></span>

### <span data-ttu-id="1b5d2-138">System.object</span><span class="sxs-lookup"><span data-stu-id="1b5d2-138">System.Boolean</span></span>

## <span data-ttu-id="1b5d2-139">筆記</span><span class="sxs-lookup"><span data-stu-id="1b5d2-139">NOTES</span></span>

<span data-ttu-id="1b5d2-140">別名</span><span class="sxs-lookup"><span data-stu-id="1b5d2-140">ALIASES</span></span>

## <span data-ttu-id="1b5d2-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b5d2-141">RELATED LINKS</span></span>

