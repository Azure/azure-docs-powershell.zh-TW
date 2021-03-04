---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: fc0a6bc7fa87a78fedd0416ea1578b9404168dce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905745"
---
# <span data-ttu-id="28cbc-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="28cbc-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="28cbc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="28cbc-103">將次要資料庫切換為主要資料庫，以啟動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="28cbc-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="28cbc-104">語法</span><span class="sxs-lookup"><span data-stu-id="28cbc-104">SYNTAX</span></span>

### <span data-ttu-id="28cbc-105">NoOptionsSet (預設) </span><span class="sxs-lookup"><span data-stu-id="28cbc-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28cbc-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="28cbc-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28cbc-107">描述</span><span class="sxs-lookup"><span data-stu-id="28cbc-107">DESCRIPTION</span></span>
<span data-ttu-id="28cbc-108">**Set-AzSqlDatabase Secondarary Cmdlet** 將次要資料庫切換為主要資料庫，以啟動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="28cbc-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="28cbc-109">此 Cmdlet 是設計成一般組配置命令，但目前僅限於啟動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="28cbc-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="28cbc-110">指定 *AllowDataLoss 參數* ，在中斷期間啟動強制容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="28cbc-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="28cbc-111">當您執行規劃的作業時 ，不需要指定此參數，例如復原鑽取。</span><span class="sxs-lookup"><span data-stu-id="28cbc-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="28cbc-112">在後一種情況下，次要資料庫在切換前會先與主要資料庫同步處理。</span><span class="sxs-lookup"><span data-stu-id="28cbc-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="28cbc-113">例子</span><span class="sxs-lookup"><span data-stu-id="28cbc-113">EXAMPLES</span></span>

### <span data-ttu-id="28cbc-114">範例 1：啟動規劃的容錯移轉</span><span class="sxs-lookup"><span data-stu-id="28cbc-114">Example 1: Initiate a planned failover</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="28cbc-115">範例 2：啟動具有潛在資料遺失 (的強制容錯移轉) </span><span class="sxs-lookup"><span data-stu-id="28cbc-115">Example 2: Initiate a forced failover (with potential data loss)</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="28cbc-116">參數</span><span class="sxs-lookup"><span data-stu-id="28cbc-116">PARAMETERS</span></span>

### <span data-ttu-id="28cbc-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="28cbc-117">-AllowDataLoss</span></span>
<span data-ttu-id="28cbc-118">表示此容錯移轉作業允許資料遺失。</span><span class="sxs-lookup"><span data-stu-id="28cbc-118">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="28cbc-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28cbc-119">-AsJob</span></span>
<span data-ttu-id="28cbc-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="28cbc-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28cbc-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="28cbc-121">-DatabaseName</span></span>
<span data-ttu-id="28cbc-122">指定 Azure SQL Database 次要名稱。</span><span class="sxs-lookup"><span data-stu-id="28cbc-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="28cbc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28cbc-123">-DefaultProfile</span></span>
<span data-ttu-id="28cbc-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="28cbc-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28cbc-125">-容錯移轉</span><span class="sxs-lookup"><span data-stu-id="28cbc-125">-Failover</span></span>
<span data-ttu-id="28cbc-126">表示此作業為容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="28cbc-126">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="28cbc-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28cbc-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="28cbc-128">指定指派給合作夥伴 Azure SQL Database 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="28cbc-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="28cbc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28cbc-129">-ResourceGroupName</span></span>
<span data-ttu-id="28cbc-130">指定分派給 Azure SQL Database 次要資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="28cbc-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="28cbc-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28cbc-131">-ServerName</span></span>
<span data-ttu-id="28cbc-132">指定託管 Azure SQL 資料庫次要的 SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="28cbc-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="28cbc-133">-確認</span><span class="sxs-lookup"><span data-stu-id="28cbc-133">-Confirm</span></span>
<span data-ttu-id="28cbc-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="28cbc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28cbc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28cbc-135">-WhatIf</span></span>
<span data-ttu-id="28cbc-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28cbc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28cbc-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28cbc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28cbc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28cbc-138">CommonParameters</span></span>
<span data-ttu-id="28cbc-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28cbc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28cbc-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28cbc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28cbc-141">輸入</span><span class="sxs-lookup"><span data-stu-id="28cbc-141">INPUTS</span></span>

### <span data-ttu-id="28cbc-142">System.String</span><span class="sxs-lookup"><span data-stu-id="28cbc-142">System.String</span></span>

## <span data-ttu-id="28cbc-143">輸出</span><span class="sxs-lookup"><span data-stu-id="28cbc-143">OUTPUTS</span></span>

### <span data-ttu-id="28cbc-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="28cbc-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="28cbc-145">筆記</span><span class="sxs-lookup"><span data-stu-id="28cbc-145">NOTES</span></span>

## <span data-ttu-id="28cbc-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="28cbc-146">RELATED LINKS</span></span>

[<span data-ttu-id="28cbc-147">New-AzSqlDatabase2ary</span><span class="sxs-lookup"><span data-stu-id="28cbc-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="28cbc-148">Remove-AzSqlDatabase二一</span><span class="sxs-lookup"><span data-stu-id="28cbc-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="28cbc-149">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="28cbc-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
