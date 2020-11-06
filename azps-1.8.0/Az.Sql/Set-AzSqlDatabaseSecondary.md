---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 598266c17bde6cb9e05efa6b917341975f0a3153
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614727"
---
# <span data-ttu-id="81820-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="81820-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="81820-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81820-102">SYNOPSIS</span></span>
<span data-ttu-id="81820-103">將次要資料庫切換為主要資料庫，以便啟動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="81820-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="81820-104">句法</span><span class="sxs-lookup"><span data-stu-id="81820-104">SYNTAX</span></span>

### <span data-ttu-id="81820-105">NoOptionsSet (預設) </span><span class="sxs-lookup"><span data-stu-id="81820-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81820-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="81820-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81820-107">說明</span><span class="sxs-lookup"><span data-stu-id="81820-107">DESCRIPTION</span></span>
<span data-ttu-id="81820-108">**AzSqlDatabaseSecondary** Cmdlet 會將次要資料庫切換為主要資料庫，以便啟動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="81820-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="81820-109">這個 Cmdlet 是設計為一般配置命令，但目前僅限於啟動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="81820-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="81820-110">指定 *AllowDataLoss* 參數，以在中斷期間啟動強制容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="81820-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="81820-111">您不需要在執行計畫作業時（例如復原鑽孔）來指定此參數。</span><span class="sxs-lookup"><span data-stu-id="81820-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="81820-112">在後一種情況下，次要資料庫會在切換前與主要資料庫同步處理。</span><span class="sxs-lookup"><span data-stu-id="81820-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="81820-113">示例</span><span class="sxs-lookup"><span data-stu-id="81820-113">EXAMPLES</span></span>

## <span data-ttu-id="81820-114">參數</span><span class="sxs-lookup"><span data-stu-id="81820-114">PARAMETERS</span></span>

### <span data-ttu-id="81820-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="81820-115">-AllowDataLoss</span></span>
<span data-ttu-id="81820-116">表示此容錯移轉作業允許資料遺失。</span><span class="sxs-lookup"><span data-stu-id="81820-116">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="81820-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81820-117">-AsJob</span></span>
<span data-ttu-id="81820-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81820-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81820-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="81820-119">-DatabaseName</span></span>
<span data-ttu-id="81820-120">指定 Azure SQL 資料庫副的名稱。</span><span class="sxs-lookup"><span data-stu-id="81820-120">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="81820-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81820-121">-DefaultProfile</span></span>
<span data-ttu-id="81820-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="81820-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81820-123">-容錯移轉</span><span class="sxs-lookup"><span data-stu-id="81820-123">-Failover</span></span>
<span data-ttu-id="81820-124">表示此操作為容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="81820-124">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="81820-125">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81820-125">-PartnerResourceGroupName</span></span>
<span data-ttu-id="81820-126">指定合作夥伴 Azure SQL 資料庫所指派的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="81820-126">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="81820-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81820-127">-ResourceGroupName</span></span>
<span data-ttu-id="81820-128">指定 Azure SQL 資料庫副指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="81820-128">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="81820-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="81820-129">-ServerName</span></span>
<span data-ttu-id="81820-130">指定託管 Azure SQL 資料庫副的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="81820-130">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="81820-131">-確認</span><span class="sxs-lookup"><span data-stu-id="81820-131">-Confirm</span></span>
<span data-ttu-id="81820-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81820-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81820-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81820-133">-WhatIf</span></span>
<span data-ttu-id="81820-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81820-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81820-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81820-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81820-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81820-136">CommonParameters</span></span>
<span data-ttu-id="81820-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81820-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81820-138">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="81820-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81820-139">輸入</span><span class="sxs-lookup"><span data-stu-id="81820-139">INPUTS</span></span>

### <span data-ttu-id="81820-140">System.object</span><span class="sxs-lookup"><span data-stu-id="81820-140">System.String</span></span>

## <span data-ttu-id="81820-141">輸出</span><span class="sxs-lookup"><span data-stu-id="81820-141">OUTPUTS</span></span>

### <span data-ttu-id="81820-142">AzureReplicationLinkModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="81820-142">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="81820-143">筆記</span><span class="sxs-lookup"><span data-stu-id="81820-143">NOTES</span></span>

## <span data-ttu-id="81820-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="81820-144">RELATED LINKS</span></span>

[<span data-ttu-id="81820-145">新-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="81820-145">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="81820-146">移除-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="81820-146">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="81820-147">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="81820-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
