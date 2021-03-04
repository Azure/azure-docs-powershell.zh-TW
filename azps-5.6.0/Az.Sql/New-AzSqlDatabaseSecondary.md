---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 983291eda139793b2cc5d0fe5cd213b5d8cd69a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909429"
---
# <span data-ttu-id="52051-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="52051-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="52051-102">簡介</span><span class="sxs-lookup"><span data-stu-id="52051-102">SYNOPSIS</span></span>
<span data-ttu-id="52051-103">為現有的資料庫建立次要資料庫，並開始資料複製。</span><span class="sxs-lookup"><span data-stu-id="52051-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="52051-104">語法</span><span class="sxs-lookup"><span data-stu-id="52051-104">SYNTAX</span></span>

### <span data-ttu-id="52051-105">DtuBasedDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="52051-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52051-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="52051-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52051-107">描述</span><span class="sxs-lookup"><span data-stu-id="52051-107">DESCRIPTION</span></span>
<span data-ttu-id="52051-108">**New-AzSqlDatabase二維元** Cmdlet 會取代 Start-AzSqlDatabaseCopy Cmdlet，用於設定資料庫的異地複製。</span><span class="sxs-lookup"><span data-stu-id="52051-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="52051-109">它會從主要資料庫到次要資料庫，會返回異地複製連結化物件。</span><span class="sxs-lookup"><span data-stu-id="52051-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="52051-110">例子</span><span class="sxs-lookup"><span data-stu-id="52051-110">EXAMPLES</span></span>

### <span data-ttu-id="52051-111">範例 1：建立使用中Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="52051-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="52051-112">範例 2：建立 active Geo-Replication，並指定合作夥伴資料庫名稱與源資料庫名稱不同</span><span class="sxs-lookup"><span data-stu-id="52051-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="52051-113">參數</span><span class="sxs-lookup"><span data-stu-id="52051-113">PARAMETERS</span></span>

### <span data-ttu-id="52051-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="52051-114">-AllowConnections</span></span>
<span data-ttu-id="52051-115">指定次要 Azure SQL Database 的讀取意圖。</span><span class="sxs-lookup"><span data-stu-id="52051-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="52051-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="52051-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="52051-117">不</span><span class="sxs-lookup"><span data-stu-id="52051-117">No</span></span>
- <span data-ttu-id="52051-118">所有</span><span class="sxs-lookup"><span data-stu-id="52051-118">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Replication.Model.AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52051-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52051-119">-AsJob</span></span>
<span data-ttu-id="52051-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="52051-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52051-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="52051-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="52051-122">用來儲存 SQL Database 備份的備份儲存空間。</span><span class="sxs-lookup"><span data-stu-id="52051-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="52051-123">選項包括：本地、區域及地理位置。</span><span class="sxs-lookup"><span data-stu-id="52051-123">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52051-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="52051-124">-DatabaseName</span></span>
<span data-ttu-id="52051-125">指定做為主要資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="52051-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="52051-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52051-126">-DefaultProfile</span></span>
<span data-ttu-id="52051-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="52051-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52051-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="52051-128">-LicenseType</span></span>
<span data-ttu-id="52051-129">Azure Sql 資料庫授權類型。</span><span class="sxs-lookup"><span data-stu-id="52051-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="52051-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="52051-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="52051-131">要建立之次要資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="52051-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="52051-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52051-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="52051-133">指定此 Cmdlet 指派次要資料庫的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="52051-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="52051-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="52051-134">-PartnerServerName</span></span>
<span data-ttu-id="52051-135">指定做為次要的 Azure SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="52051-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="52051-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52051-136">-ResourceGroupName</span></span>
<span data-ttu-id="52051-137">指定此 Cmdlet 指派主資料庫的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="52051-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="52051-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="52051-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="52051-139">第二代 Azure Sql Database 的計算產生。</span><span class="sxs-lookup"><span data-stu-id="52051-139">The compute generation of the Azure Sql Database secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52051-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="52051-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="52051-141">指定要放入次要資料庫的集中資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="52051-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52051-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="52051-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="52051-143">指定要指派給次要資料庫的服務目標名稱。</span><span class="sxs-lookup"><span data-stu-id="52051-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52051-144">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="52051-144">-SecondaryType</span></span>
<span data-ttu-id="52051-145">資料庫的次要類型如果為次要類型。</span><span class="sxs-lookup"><span data-stu-id="52051-145">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="52051-146">有效的值為地理位置和命名。</span><span class="sxs-lookup"><span data-stu-id="52051-146">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52051-147">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="52051-147">-SecondaryVCore</span></span>
<span data-ttu-id="52051-148">次要 Azure Sql Database 的 Vcore 數位。</span><span class="sxs-lookup"><span data-stu-id="52051-148">The Vcore numbers of the Azure Sql Database secondary.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52051-149">-ServerName</span><span class="sxs-lookup"><span data-stu-id="52051-149">-ServerName</span></span>
<span data-ttu-id="52051-150">指定主 SQL 資料庫的 SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="52051-150">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="52051-151">-標記</span><span class="sxs-lookup"><span data-stu-id="52051-151">-Tags</span></span>
<span data-ttu-id="52051-152">以雜湊表的形式指定要與 SQL Database 複製連結建立關聯的索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="52051-152">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="52051-153">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="52051-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52051-154">-確認</span><span class="sxs-lookup"><span data-stu-id="52051-154">-Confirm</span></span>
<span data-ttu-id="52051-155">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="52051-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52051-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52051-156">-WhatIf</span></span>
<span data-ttu-id="52051-157">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52051-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52051-158">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52051-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52051-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52051-159">CommonParameters</span></span>
<span data-ttu-id="52051-160">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="52051-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52051-161">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52051-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52051-162">輸入</span><span class="sxs-lookup"><span data-stu-id="52051-162">INPUTS</span></span>

### <span data-ttu-id="52051-163">System.String</span><span class="sxs-lookup"><span data-stu-id="52051-163">System.String</span></span>

## <span data-ttu-id="52051-164">輸出</span><span class="sxs-lookup"><span data-stu-id="52051-164">OUTPUTS</span></span>

### <span data-ttu-id="52051-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="52051-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="52051-166">筆記</span><span class="sxs-lookup"><span data-stu-id="52051-166">NOTES</span></span>

## <span data-ttu-id="52051-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="52051-167">RELATED LINKS</span></span>

[<span data-ttu-id="52051-168">Remove-AzSqlDatabase二一</span><span class="sxs-lookup"><span data-stu-id="52051-168">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="52051-169">Set-AzSqlDatabase二一</span><span class="sxs-lookup"><span data-stu-id="52051-169">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="52051-170">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="52051-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
