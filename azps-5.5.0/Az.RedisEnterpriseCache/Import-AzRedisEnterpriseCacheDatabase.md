---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/import-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 6ab4babd894a3c639db6e41e6088653604072c7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140002"
---
# <span data-ttu-id="de082-101">Import-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="de082-101">Import-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="de082-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de082-102">SYNOPSIS</span></span>
<span data-ttu-id="de082-103">將資料庫檔案匯入至目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="de082-103">Imports a database file to target database.</span></span>

## <span data-ttu-id="de082-104">句法</span><span class="sxs-lookup"><span data-stu-id="de082-104">SYNTAX</span></span>

```
Import-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="de082-105">說明</span><span class="sxs-lookup"><span data-stu-id="de082-105">DESCRIPTION</span></span>
<span data-ttu-id="de082-106">將資料庫檔案匯入至目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="de082-106">Imports a database file to target database.</span></span>

## <span data-ttu-id="de082-107">示例</span><span class="sxs-lookup"><span data-stu-id="de082-107">EXAMPLES</span></span>

### <span data-ttu-id="de082-108">範例1：匯入資料庫</span><span class="sxs-lookup"><span data-stu-id="de082-108">Example 1: Import database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/myfilename?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="de082-109">這個命令會將資料庫檔案匯入到名為 MyCache 的 Redis Enterprise Cache 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="de082-109">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="de082-110">範例2：使用範例檔案名) 匯入資料庫 (</span><span class="sxs-lookup"><span data-stu-id="de082-110">Example 2: Import database (using example filename)</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/bk20201130-223654-1-db-1_of_1-2-0-16383.rdb.gz?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="de082-111">這個命令會將資料庫檔案匯入到名為 MyCache 的 Redis Enterprise Cache 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="de082-111">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="de082-112">參數</span><span class="sxs-lookup"><span data-stu-id="de082-112">PARAMETERS</span></span>

### <span data-ttu-id="de082-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de082-113">-AsJob</span></span>
<span data-ttu-id="de082-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="de082-114">Run the command as a job</span></span>

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

### <span data-ttu-id="de082-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="de082-115">-ClusterName</span></span>
<span data-ttu-id="de082-116">RedisEnterprise 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="de082-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="de082-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de082-117">-DefaultProfile</span></span>
<span data-ttu-id="de082-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="de082-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de082-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="de082-119">-NoWait</span></span>
<span data-ttu-id="de082-120">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="de082-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="de082-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de082-121">-PassThru</span></span>
<span data-ttu-id="de082-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="de082-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="de082-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de082-123">-ResourceGroupName</span></span>
<span data-ttu-id="de082-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="de082-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="de082-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="de082-125">-SasUri</span></span>
<span data-ttu-id="de082-126">要從中匯入之目標 blob 的 SAS Uri</span><span class="sxs-lookup"><span data-stu-id="de082-126">SAS Uri for the target blob to import from</span></span>

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

### <span data-ttu-id="de082-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de082-127">-SubscriptionId</span></span>
<span data-ttu-id="de082-128">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="de082-128">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="de082-129">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="de082-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="de082-130">-確認</span><span class="sxs-lookup"><span data-stu-id="de082-130">-Confirm</span></span>
<span data-ttu-id="de082-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="de082-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de082-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de082-132">-WhatIf</span></span>
<span data-ttu-id="de082-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de082-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de082-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de082-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de082-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de082-135">CommonParameters</span></span>
<span data-ttu-id="de082-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de082-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de082-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="de082-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de082-138">輸入</span><span class="sxs-lookup"><span data-stu-id="de082-138">INPUTS</span></span>

## <span data-ttu-id="de082-139">輸出</span><span class="sxs-lookup"><span data-stu-id="de082-139">OUTPUTS</span></span>

### <span data-ttu-id="de082-140">System.object</span><span class="sxs-lookup"><span data-stu-id="de082-140">System.Boolean</span></span>

## <span data-ttu-id="de082-141">筆記</span><span class="sxs-lookup"><span data-stu-id="de082-141">NOTES</span></span>

<span data-ttu-id="de082-142">別名</span><span class="sxs-lookup"><span data-stu-id="de082-142">ALIASES</span></span>

## <span data-ttu-id="de082-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="de082-143">RELATED LINKS</span></span>

