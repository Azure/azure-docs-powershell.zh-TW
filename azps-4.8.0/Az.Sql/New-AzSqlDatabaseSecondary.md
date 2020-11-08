---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 0b0934ffe9a5721ff08438ca7a24d97e2b4a34cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970095"
---
# <span data-ttu-id="db0ce-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="db0ce-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="db0ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db0ce-102">SYNOPSIS</span></span>
<span data-ttu-id="db0ce-103">建立現有資料庫的次要資料庫並開始資料複製。</span><span class="sxs-lookup"><span data-stu-id="db0ce-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="db0ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="db0ce-104">SYNTAX</span></span>

### <span data-ttu-id="db0ce-105">DtuBasedDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="db0ce-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db0ce-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="db0ce-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db0ce-107">說明</span><span class="sxs-lookup"><span data-stu-id="db0ce-107">DESCRIPTION</span></span>
<span data-ttu-id="db0ce-108">**新的-AzSqlDatabaseSecondary** Cmdlet 會在用於設定資料庫異地複製時取代 Start-AzSqlDatabaseCopy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db0ce-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="db0ce-109">它會將地域複製連結化物件從主要資料庫傳回次要資料庫。</span><span class="sxs-lookup"><span data-stu-id="db0ce-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="db0ce-110">示例</span><span class="sxs-lookup"><span data-stu-id="db0ce-110">EXAMPLES</span></span>

### <span data-ttu-id="db0ce-111">範例1：建立作用中 Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="db0ce-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="db0ce-112">範例2：建立作用中 Geo-Replication，並指定合作夥伴資料庫名稱與源資料庫名稱不同</span><span class="sxs-lookup"><span data-stu-id="db0ce-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="db0ce-113">參數</span><span class="sxs-lookup"><span data-stu-id="db0ce-113">PARAMETERS</span></span>

### <span data-ttu-id="db0ce-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="db0ce-114">-AllowConnections</span></span>
<span data-ttu-id="db0ce-115">指定副 Azure SQL 資料庫的閱讀意圖。</span><span class="sxs-lookup"><span data-stu-id="db0ce-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="db0ce-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="db0ce-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db0ce-117">不</span><span class="sxs-lookup"><span data-stu-id="db0ce-117">No</span></span>
- <span data-ttu-id="db0ce-118">同時</span><span class="sxs-lookup"><span data-stu-id="db0ce-118">All</span></span>

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

### <span data-ttu-id="db0ce-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db0ce-119">-AsJob</span></span>
<span data-ttu-id="db0ce-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="db0ce-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db0ce-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="db0ce-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="db0ce-122">儲存 SQL 資料庫備份所用的備份儲存空間冗余。</span><span class="sxs-lookup"><span data-stu-id="db0ce-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="db0ce-123">選項包括： Local、Zone 和 Geo。</span><span class="sxs-lookup"><span data-stu-id="db0ce-123">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="db0ce-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="db0ce-124">-DatabaseName</span></span>
<span data-ttu-id="db0ce-125">指定要作為主要的資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="db0ce-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="db0ce-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db0ce-126">-DefaultProfile</span></span>
<span data-ttu-id="db0ce-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="db0ce-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db0ce-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="db0ce-128">-LicenseType</span></span>
<span data-ttu-id="db0ce-129">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="db0ce-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="db0ce-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="db0ce-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="db0ce-131">要建立之次要資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="db0ce-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="db0ce-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db0ce-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="db0ce-133">指定此 Cmdlet 指派副資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="db0ce-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="db0ce-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="db0ce-134">-PartnerServerName</span></span>
<span data-ttu-id="db0ce-135">指定要作為副的 Azure SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="db0ce-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="db0ce-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db0ce-136">-ResourceGroupName</span></span>
<span data-ttu-id="db0ce-137">指定此 Cmdlet 指派主要資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="db0ce-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="db0ce-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="db0ce-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="db0ce-139">Azure Sql 資料庫副的計算產生方式。</span><span class="sxs-lookup"><span data-stu-id="db0ce-139">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="db0ce-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="db0ce-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="db0ce-141">指定要放入次要資料庫的彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="db0ce-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="db0ce-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="db0ce-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="db0ce-143">指定要指派給次要資料庫的服務目標名稱。</span><span class="sxs-lookup"><span data-stu-id="db0ce-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="db0ce-144">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="db0ce-144">-SecondaryVCore</span></span>
<span data-ttu-id="db0ce-145">Azure Sql 資料庫副的 Vcore 號碼。</span><span class="sxs-lookup"><span data-stu-id="db0ce-145">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="db0ce-146">-ServerName</span><span class="sxs-lookup"><span data-stu-id="db0ce-146">-ServerName</span></span>
<span data-ttu-id="db0ce-147">指定主要 SQL 資料庫之 SQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="db0ce-147">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="db0ce-148">-標記</span><span class="sxs-lookup"><span data-stu-id="db0ce-148">-Tags</span></span>
<span data-ttu-id="db0ce-149">指定雜湊資料表形式的鍵值對，以與 SQL 資料庫複製連結建立關聯。</span><span class="sxs-lookup"><span data-stu-id="db0ce-149">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="db0ce-150">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="db0ce-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="db0ce-151">-確認</span><span class="sxs-lookup"><span data-stu-id="db0ce-151">-Confirm</span></span>
<span data-ttu-id="db0ce-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="db0ce-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db0ce-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db0ce-153">-WhatIf</span></span>
<span data-ttu-id="db0ce-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="db0ce-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db0ce-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db0ce-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db0ce-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db0ce-156">CommonParameters</span></span>
<span data-ttu-id="db0ce-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db0ce-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db0ce-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="db0ce-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db0ce-159">輸入</span><span class="sxs-lookup"><span data-stu-id="db0ce-159">INPUTS</span></span>

### <span data-ttu-id="db0ce-160">System.object</span><span class="sxs-lookup"><span data-stu-id="db0ce-160">System.String</span></span>

## <span data-ttu-id="db0ce-161">輸出</span><span class="sxs-lookup"><span data-stu-id="db0ce-161">OUTPUTS</span></span>

### <span data-ttu-id="db0ce-162">AzureReplicationLinkModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="db0ce-162">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="db0ce-163">筆記</span><span class="sxs-lookup"><span data-stu-id="db0ce-163">NOTES</span></span>

## <span data-ttu-id="db0ce-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="db0ce-164">RELATED LINKS</span></span>

[<span data-ttu-id="db0ce-165">移除-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="db0ce-165">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="db0ce-166">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="db0ce-166">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="db0ce-167">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="db0ce-167">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
