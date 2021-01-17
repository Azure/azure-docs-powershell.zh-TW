---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: d713675e3e73f32a4579d801a4dc1577cebd4cf0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434981"
---
# <span data-ttu-id="c025d-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c025d-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="c025d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c025d-102">SYNOPSIS</span></span>
<span data-ttu-id="c025d-103">將次要資料庫切換為主要資料庫，以便啟動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="c025d-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="c025d-104">句法</span><span class="sxs-lookup"><span data-stu-id="c025d-104">SYNTAX</span></span>

### <span data-ttu-id="c025d-105">NoOptionsSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c025d-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c025d-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="c025d-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c025d-107">說明</span><span class="sxs-lookup"><span data-stu-id="c025d-107">DESCRIPTION</span></span>
<span data-ttu-id="c025d-108">**AzSqlDatabaseSecondary** Cmdlet 會將次要資料庫切換為主要資料庫，以便啟動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="c025d-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="c025d-109">這個 Cmdlet 是設計為一般配置命令，但目前僅限於啟動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="c025d-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="c025d-110">指定 *AllowDataLoss* 參數，以在中斷期間啟動強制容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="c025d-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="c025d-111">您不需要在執行計畫作業時（例如復原鑽孔）來指定此參數。</span><span class="sxs-lookup"><span data-stu-id="c025d-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="c025d-112">在後一種情況下，次要資料庫會在切換前與主要資料庫同步處理。</span><span class="sxs-lookup"><span data-stu-id="c025d-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="c025d-113">示例</span><span class="sxs-lookup"><span data-stu-id="c025d-113">EXAMPLES</span></span>

### <span data-ttu-id="c025d-114">範例1：啟動計畫的容錯移轉</span><span class="sxs-lookup"><span data-stu-id="c025d-114">Example 1: Initiate a planned failover</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="c025d-115">範例2：啟動強制性容錯移轉 (可能造成資料遺失) </span><span class="sxs-lookup"><span data-stu-id="c025d-115">Example 2: Initiate a forced failover (with potential data loss)</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="c025d-116">參數</span><span class="sxs-lookup"><span data-stu-id="c025d-116">PARAMETERS</span></span>

### <span data-ttu-id="c025d-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="c025d-117">-AllowDataLoss</span></span>
<span data-ttu-id="c025d-118">表示此容錯移轉作業允許資料遺失。</span><span class="sxs-lookup"><span data-stu-id="c025d-118">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c025d-119">-AsJob</span></span>
<span data-ttu-id="c025d-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c025d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c025d-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c025d-121">-DatabaseName</span></span>
<span data-ttu-id="c025d-122">指定 Azure SQL 資料庫副的名稱。</span><span class="sxs-lookup"><span data-stu-id="c025d-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c025d-123">-DefaultProfile</span></span>
<span data-ttu-id="c025d-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c025d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-125">-容錯移轉</span><span class="sxs-lookup"><span data-stu-id="c025d-125">-Failover</span></span>
<span data-ttu-id="c025d-126">表示此操作為容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="c025d-126">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c025d-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c025d-128">指定合作夥伴 Azure SQL 資料庫所指派的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c025d-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c025d-129">-ResourceGroupName</span></span>
<span data-ttu-id="c025d-130">指定 Azure SQL 資料庫副指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c025d-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c025d-131">-ServerName</span></span>
<span data-ttu-id="c025d-132">指定託管 Azure SQL 資料庫副的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c025d-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-133">-確認</span><span class="sxs-lookup"><span data-stu-id="c025d-133">-Confirm</span></span>
<span data-ttu-id="c025d-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c025d-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c025d-135">-WhatIf</span></span>
<span data-ttu-id="c025d-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c025d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c025d-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c025d-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c025d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c025d-138">CommonParameters</span></span>
<span data-ttu-id="c025d-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c025d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c025d-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c025d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c025d-141">輸入</span><span class="sxs-lookup"><span data-stu-id="c025d-141">INPUTS</span></span>

### <span data-ttu-id="c025d-142">System.object</span><span class="sxs-lookup"><span data-stu-id="c025d-142">System.String</span></span>

## <span data-ttu-id="c025d-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c025d-143">OUTPUTS</span></span>

### <span data-ttu-id="c025d-144">AzureReplicationLinkModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="c025d-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="c025d-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c025d-145">NOTES</span></span>

## <span data-ttu-id="c025d-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="c025d-146">RELATED LINKS</span></span>

[<span data-ttu-id="c025d-147">新-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c025d-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="c025d-148">移除-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c025d-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="c025d-149">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="c025d-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
