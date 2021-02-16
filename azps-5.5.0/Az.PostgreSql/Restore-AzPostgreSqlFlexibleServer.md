---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restore-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: e8554f0ac88cf3d69e36282b7e310cc92b41d6db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128558"
---
# <span data-ttu-id="96aba-101">Restore-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="96aba-101">Restore-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="96aba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96aba-102">SYNOPSIS</span></span>
<span data-ttu-id="96aba-103">從現有的備份還原 PostgreSQL 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="96aba-103">Restore a PostgreSQL flexible server from an existing backup</span></span>

## <span data-ttu-id="96aba-104">句法</span><span class="sxs-lookup"><span data-stu-id="96aba-104">SYNTAX</span></span>

```
Restore-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> -SourceServerName <String>
 -Location <String> -RestorePointInTime <DateTime> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96aba-105">說明</span><span class="sxs-lookup"><span data-stu-id="96aba-105">DESCRIPTION</span></span>
<span data-ttu-id="96aba-106">從現有的備份還原伺服器</span><span class="sxs-lookup"><span data-stu-id="96aba-106">Restore a server from an existing backup</span></span>

## <span data-ttu-id="96aba-107">示例</span><span class="sxs-lookup"><span data-stu-id="96aba-107">EXAMPLES</span></span>

### <span data-ttu-id="96aba-108">範例1：使用 PointInTime Restore 還原 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="96aba-108">Example 1: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Restore-AzPostgreSqlFlexibleServer -Name pg-restore -ResourceGroupName PowershellPostgreSqlTest -SourceServerName postgresql-test -Location eastus -RestorePointInTime $restorePointInTime 

Name       Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier       
----       -------- ------------------ ------- ----------------------- -------          -------       
pg-restore eastus   postgresql_test         12     131072              Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="96aba-109">這些 Cmdlet 會使用 PointInTime 還原來還原 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="96aba-109">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="96aba-110">參數</span><span class="sxs-lookup"><span data-stu-id="96aba-110">PARAMETERS</span></span>

### <span data-ttu-id="96aba-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96aba-111">-AsJob</span></span>
<span data-ttu-id="96aba-112">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="96aba-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="96aba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96aba-113">-DefaultProfile</span></span>
<span data-ttu-id="96aba-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96aba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96aba-115">-位置</span><span class="sxs-lookup"><span data-stu-id="96aba-115">-Location</span></span>
<span data-ttu-id="96aba-116">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="96aba-116">The location the resource resides in.</span></span>

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

### <span data-ttu-id="96aba-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="96aba-117">-Name</span></span>
<span data-ttu-id="96aba-118">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="96aba-118">The name of the server.</span></span>

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

### <span data-ttu-id="96aba-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="96aba-119">-NoWait</span></span>
<span data-ttu-id="96aba-120">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="96aba-120">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="96aba-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96aba-121">-ResourceGroupName</span></span>
<span data-ttu-id="96aba-122">包含資源之資源群組的名稱，您可以從 Azure 資源管理員 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="96aba-122">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="96aba-123">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="96aba-123">-RestorePointInTime</span></span>
<span data-ttu-id="96aba-124">從 (ISO8601 格式中還原的時間點) （例如2017年、2004年，26T02：10： 00 + 08：00）。</span><span class="sxs-lookup"><span data-stu-id="96aba-124">The point in time to restore from (ISO8601 format), e.g., 2017-04-26T02:10:00+08:00.</span></span>

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

### <span data-ttu-id="96aba-125">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="96aba-125">-SourceServerName</span></span>
<span data-ttu-id="96aba-126">來源伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="96aba-126">The name of the source server.</span></span>

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

### <span data-ttu-id="96aba-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96aba-127">-SubscriptionId</span></span>
<span data-ttu-id="96aba-128">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="96aba-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="96aba-129">-確認</span><span class="sxs-lookup"><span data-stu-id="96aba-129">-Confirm</span></span>
<span data-ttu-id="96aba-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="96aba-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96aba-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96aba-131">-WhatIf</span></span>
<span data-ttu-id="96aba-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96aba-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96aba-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96aba-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96aba-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96aba-134">CommonParameters</span></span>
<span data-ttu-id="96aba-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96aba-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96aba-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="96aba-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96aba-137">輸入</span><span class="sxs-lookup"><span data-stu-id="96aba-137">INPUTS</span></span>

## <span data-ttu-id="96aba-138">輸出</span><span class="sxs-lookup"><span data-stu-id="96aba-138">OUTPUTS</span></span>

### <span data-ttu-id="96aba-139">IServerAutoGenerated （PostgreSql）。 Api20200214Preview。</span><span class="sxs-lookup"><span data-stu-id="96aba-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="96aba-140">筆記</span><span class="sxs-lookup"><span data-stu-id="96aba-140">NOTES</span></span>

<span data-ttu-id="96aba-141">別名</span><span class="sxs-lookup"><span data-stu-id="96aba-141">ALIASES</span></span>

## <span data-ttu-id="96aba-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="96aba-142">RELATED LINKS</span></span>

