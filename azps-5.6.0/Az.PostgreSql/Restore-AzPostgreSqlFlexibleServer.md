---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/restore-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 503d20a8473c83a9b2ca7ca1ec19deab6db7103c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902322"
---
# <span data-ttu-id="557eb-101">Restore-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="557eb-101">Restore-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="557eb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="557eb-102">SYNOPSIS</span></span>
<span data-ttu-id="557eb-103">從現有的備份還原 PostgreSQL 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="557eb-103">Restore a PostgreSQL flexible server from an existing backup</span></span>

## <span data-ttu-id="557eb-104">語法</span><span class="sxs-lookup"><span data-stu-id="557eb-104">SYNTAX</span></span>

```
Restore-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> -SourceServerName <String>
 -Location <String> -RestorePointInTime <DateTime> [-SubscriptionId <String>] [-Zone <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="557eb-105">描述</span><span class="sxs-lookup"><span data-stu-id="557eb-105">DESCRIPTION</span></span>
<span data-ttu-id="557eb-106">從現有的備份還原伺服器</span><span class="sxs-lookup"><span data-stu-id="557eb-106">Restore a server from an existing backup</span></span>

## <span data-ttu-id="557eb-107">例子</span><span class="sxs-lookup"><span data-stu-id="557eb-107">EXAMPLES</span></span>

### <span data-ttu-id="557eb-108">範例 1：使用 PointInTime 還原還原 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="557eb-108">Example 1: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Restore-AzPostgreSqlFlexibleServer -Name pg-restore -ResourceGroupName PowershellPostgreSqlTest -SourceServerName postgresql-test -Location eastus -RestorePointInTime $restorePointInTime 

Name       Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier       
----       -------- ------------------ ------- ----------------------- -------          -------       
pg-restore eastus   postgresql_test         12     131072              Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="557eb-109">這些 Cmdlet 會使用 PointInTime 還原還原 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="557eb-109">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="557eb-110">參數</span><span class="sxs-lookup"><span data-stu-id="557eb-110">PARAMETERS</span></span>

### <span data-ttu-id="557eb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="557eb-111">-AsJob</span></span>
<span data-ttu-id="557eb-112">以工作執行命令。</span><span class="sxs-lookup"><span data-stu-id="557eb-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="557eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="557eb-113">-DefaultProfile</span></span>
<span data-ttu-id="557eb-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="557eb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="557eb-115">-位置</span><span class="sxs-lookup"><span data-stu-id="557eb-115">-Location</span></span>
<span data-ttu-id="557eb-116">資源所在位置。</span><span class="sxs-lookup"><span data-stu-id="557eb-116">The location the resource resides in.</span></span>

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

### <span data-ttu-id="557eb-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="557eb-117">-Name</span></span>
<span data-ttu-id="557eb-118">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="557eb-118">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="557eb-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="557eb-119">-NoWait</span></span>
<span data-ttu-id="557eb-120">非同步執行命令。</span><span class="sxs-lookup"><span data-stu-id="557eb-120">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="557eb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="557eb-121">-ResourceGroupName</span></span>
<span data-ttu-id="557eb-122">包含資源的資源組名，您可從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="557eb-122">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="557eb-123">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="557eb-123">-RestorePointInTime</span></span>
<span data-ttu-id="557eb-124">從 (ISO8601 格式) 還原的時間點，例如 2017-04-26T02：10：00+08：00。</span><span class="sxs-lookup"><span data-stu-id="557eb-124">The point in time to restore from (ISO8601 format), e.g., 2017-04-26T02:10:00+08:00.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="557eb-125">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="557eb-125">-SourceServerName</span></span>
<span data-ttu-id="557eb-126">來源伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="557eb-126">The name of the source server.</span></span>

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

### <span data-ttu-id="557eb-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="557eb-127">-SubscriptionId</span></span>
<span data-ttu-id="557eb-128">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="557eb-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="557eb-129">-區域</span><span class="sxs-lookup"><span data-stu-id="557eb-129">-Zone</span></span>
<span data-ttu-id="557eb-130">資源要置入的可用性區域。</span><span class="sxs-lookup"><span data-stu-id="557eb-130">Availability zone into which to provision the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="557eb-131">-確認</span><span class="sxs-lookup"><span data-stu-id="557eb-131">-Confirm</span></span>
<span data-ttu-id="557eb-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="557eb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="557eb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="557eb-133">-WhatIf</span></span>
<span data-ttu-id="557eb-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="557eb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="557eb-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="557eb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="557eb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="557eb-136">CommonParameters</span></span>
<span data-ttu-id="557eb-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="557eb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="557eb-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="557eb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="557eb-139">輸入</span><span class="sxs-lookup"><span data-stu-id="557eb-139">INPUTS</span></span>

## <span data-ttu-id="557eb-140">輸出</span><span class="sxs-lookup"><span data-stu-id="557eb-140">OUTPUTS</span></span>

### <span data-ttu-id="557eb-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="557eb-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="557eb-142">筆記</span><span class="sxs-lookup"><span data-stu-id="557eb-142">NOTES</span></span>

<span data-ttu-id="557eb-143">別名</span><span class="sxs-lookup"><span data-stu-id="557eb-143">ALIASES</span></span>

## <span data-ttu-id="557eb-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="557eb-144">RELATED LINKS</span></span>

