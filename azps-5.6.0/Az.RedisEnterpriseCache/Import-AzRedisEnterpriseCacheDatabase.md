---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/import-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: b7258c552d14a9c7cdeafae5c23908321b0705c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914649"
---
# <span data-ttu-id="9d5e5-101">Import-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="9d5e5-101">Import-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="9d5e5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9d5e5-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5e5-103">將資料庫檔案導入目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="9d5e5-103">Imports a database file to target database.</span></span>

## <span data-ttu-id="9d5e5-104">語法</span><span class="sxs-lookup"><span data-stu-id="9d5e5-104">SYNTAX</span></span>

```
Import-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9d5e5-105">描述</span><span class="sxs-lookup"><span data-stu-id="9d5e5-105">DESCRIPTION</span></span>
<span data-ttu-id="9d5e5-106">將資料庫檔案導入目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="9d5e5-106">Imports a database file to target database.</span></span>

## <span data-ttu-id="9d5e5-107">例子</span><span class="sxs-lookup"><span data-stu-id="9d5e5-107">EXAMPLES</span></span>

### <span data-ttu-id="9d5e5-108">範例 1：匯出資料庫</span><span class="sxs-lookup"><span data-stu-id="9d5e5-108">Example 1: Import database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/myfilename?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="9d5e5-109">此命令會將資料庫檔案導入名為 MyCache 的 Redis Enterprise Cache 資料庫。</span><span class="sxs-lookup"><span data-stu-id="9d5e5-109">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="9d5e5-110">範例 2：使用範例檔案名 (資料庫) </span><span class="sxs-lookup"><span data-stu-id="9d5e5-110">Example 2: Import database (using example filename)</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/bk20201130-223654-1-db-1_of_1-2-0-16383.rdb.gz?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="9d5e5-111">此命令會將資料庫檔案導入名為 MyCache 的 Redis Enterprise Cache 資料庫。</span><span class="sxs-lookup"><span data-stu-id="9d5e5-111">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="9d5e5-112">參數</span><span class="sxs-lookup"><span data-stu-id="9d5e5-112">PARAMETERS</span></span>

### <span data-ttu-id="9d5e5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d5e5-113">-AsJob</span></span>
<span data-ttu-id="9d5e5-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="9d5e5-114">Run the command as a job</span></span>

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

### <span data-ttu-id="9d5e5-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9d5e5-115">-ClusterName</span></span>
<span data-ttu-id="9d5e5-116">RedisEnterprise 組名。</span><span class="sxs-lookup"><span data-stu-id="9d5e5-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="9d5e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d5e5-117">-DefaultProfile</span></span>
<span data-ttu-id="9d5e5-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d5e5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d5e5-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9d5e5-119">-NoWait</span></span>
<span data-ttu-id="9d5e5-120">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="9d5e5-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9d5e5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d5e5-121">-PassThru</span></span>
<span data-ttu-id="9d5e5-122">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="9d5e5-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9d5e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d5e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="9d5e5-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d5e5-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="9d5e5-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="9d5e5-125">-SasUri</span></span>
<span data-ttu-id="9d5e5-126">目標 Blob 的 SAS Uri，用於從</span><span class="sxs-lookup"><span data-stu-id="9d5e5-126">SAS Uri for the target blob to import from</span></span>

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

### <span data-ttu-id="9d5e5-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9d5e5-127">-SubscriptionId</span></span>
<span data-ttu-id="9d5e5-128">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="9d5e5-128">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9d5e5-129">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="9d5e5-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9d5e5-130">-確認</span><span class="sxs-lookup"><span data-stu-id="9d5e5-130">-Confirm</span></span>
<span data-ttu-id="9d5e5-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9d5e5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d5e5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d5e5-132">-WhatIf</span></span>
<span data-ttu-id="9d5e5-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d5e5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d5e5-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d5e5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d5e5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5e5-135">CommonParameters</span></span>
<span data-ttu-id="9d5e5-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9d5e5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5e5-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d5e5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5e5-138">輸入</span><span class="sxs-lookup"><span data-stu-id="9d5e5-138">INPUTS</span></span>

## <span data-ttu-id="9d5e5-139">輸出</span><span class="sxs-lookup"><span data-stu-id="9d5e5-139">OUTPUTS</span></span>

### <span data-ttu-id="9d5e5-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9d5e5-140">System.Boolean</span></span>

## <span data-ttu-id="9d5e5-141">筆記</span><span class="sxs-lookup"><span data-stu-id="9d5e5-141">NOTES</span></span>

<span data-ttu-id="9d5e5-142">別名</span><span class="sxs-lookup"><span data-stu-id="9d5e5-142">ALIASES</span></span>

## <span data-ttu-id="9d5e5-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d5e5-143">RELATED LINKS</span></span>

