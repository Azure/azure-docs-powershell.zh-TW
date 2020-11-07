---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 1ed31d2fedc44900d08a4108ea53220a29228a7c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792721"
---
# <span data-ttu-id="6c38d-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6c38d-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="6c38d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c38d-102">SYNOPSIS</span></span>
<span data-ttu-id="6c38d-103">建立現有資料庫的次要資料庫並開始資料複製。</span><span class="sxs-lookup"><span data-stu-id="6c38d-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="6c38d-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c38d-104">SYNTAX</span></span>

### <span data-ttu-id="6c38d-105">DtuBasedDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="6c38d-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-LicenseType <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c38d-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="6c38d-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c38d-107">說明</span><span class="sxs-lookup"><span data-stu-id="6c38d-107">DESCRIPTION</span></span>
<span data-ttu-id="6c38d-108">**新的-AzSqlDatabaseSecondary** Cmdlet 會在用於設定資料庫異地複製時取代 Start-AzSqlDatabaseCopy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c38d-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="6c38d-109">它會將地域複製連結化物件從主要資料庫傳回次要資料庫。</span><span class="sxs-lookup"><span data-stu-id="6c38d-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="6c38d-110">示例</span><span class="sxs-lookup"><span data-stu-id="6c38d-110">EXAMPLES</span></span>

### <span data-ttu-id="6c38d-111">1：建立作用中 Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="6c38d-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="6c38d-112">參數</span><span class="sxs-lookup"><span data-stu-id="6c38d-112">PARAMETERS</span></span>

### <span data-ttu-id="6c38d-113">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="6c38d-113">-AllowConnections</span></span>
<span data-ttu-id="6c38d-114">指定副 Azure SQL 資料庫的閱讀意圖。</span><span class="sxs-lookup"><span data-stu-id="6c38d-114">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="6c38d-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6c38d-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6c38d-116">不</span><span class="sxs-lookup"><span data-stu-id="6c38d-116">No</span></span>
- <span data-ttu-id="6c38d-117">同時</span><span class="sxs-lookup"><span data-stu-id="6c38d-117">All</span></span>

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

### <span data-ttu-id="6c38d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c38d-118">-AsJob</span></span>
<span data-ttu-id="6c38d-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6c38d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c38d-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6c38d-120">-DatabaseName</span></span>
<span data-ttu-id="6c38d-121">指定要作為主要的資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c38d-121">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="6c38d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c38d-122">-DefaultProfile</span></span>
<span data-ttu-id="6c38d-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6c38d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c38d-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6c38d-124">-LicenseType</span></span>
<span data-ttu-id="6c38d-125">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="6c38d-125">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="6c38d-126">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c38d-126">-PartnerResourceGroupName</span></span>
<span data-ttu-id="6c38d-127">指定此 Cmdlet 指派副資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c38d-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="6c38d-128">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="6c38d-128">-PartnerServerName</span></span>
<span data-ttu-id="6c38d-129">指定要作為副的 Azure SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c38d-129">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="6c38d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c38d-130">-ResourceGroupName</span></span>
<span data-ttu-id="6c38d-131">指定此 Cmdlet 指派主要資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c38d-131">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="6c38d-132">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="6c38d-132">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="6c38d-133">Azure Sql 資料庫副的計算產生方式。</span><span class="sxs-lookup"><span data-stu-id="6c38d-133">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="6c38d-134">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6c38d-134">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="6c38d-135">指定要放入次要資料庫的彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c38d-135">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="6c38d-136">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="6c38d-136">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="6c38d-137">指定要指派給次要資料庫的服務目標名稱。</span><span class="sxs-lookup"><span data-stu-id="6c38d-137">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="6c38d-138">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="6c38d-138">-SecondaryVCore</span></span>
<span data-ttu-id="6c38d-139">Azure Sql 資料庫副的 Vcore 號碼。</span><span class="sxs-lookup"><span data-stu-id="6c38d-139">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="6c38d-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6c38d-140">-ServerName</span></span>
<span data-ttu-id="6c38d-141">指定主要 SQL 資料庫之 SQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c38d-141">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="6c38d-142">-標記</span><span class="sxs-lookup"><span data-stu-id="6c38d-142">-Tags</span></span>
<span data-ttu-id="6c38d-143">指定雜湊資料表形式的鍵值對，以與 SQL 資料庫複製連結建立關聯。</span><span class="sxs-lookup"><span data-stu-id="6c38d-143">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="6c38d-144">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6c38d-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6c38d-145">-確認</span><span class="sxs-lookup"><span data-stu-id="6c38d-145">-Confirm</span></span>
<span data-ttu-id="6c38d-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c38d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c38d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c38d-147">-WhatIf</span></span>
<span data-ttu-id="6c38d-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c38d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c38d-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c38d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c38d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c38d-150">CommonParameters</span></span>
<span data-ttu-id="6c38d-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c38d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c38d-152">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6c38d-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c38d-153">輸入</span><span class="sxs-lookup"><span data-stu-id="6c38d-153">INPUTS</span></span>

### <span data-ttu-id="6c38d-154">System.object</span><span class="sxs-lookup"><span data-stu-id="6c38d-154">System.String</span></span>

## <span data-ttu-id="6c38d-155">輸出</span><span class="sxs-lookup"><span data-stu-id="6c38d-155">OUTPUTS</span></span>

### <span data-ttu-id="6c38d-156">AzureReplicationLinkModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="6c38d-156">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="6c38d-157">筆記</span><span class="sxs-lookup"><span data-stu-id="6c38d-157">NOTES</span></span>

## <span data-ttu-id="6c38d-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c38d-158">RELATED LINKS</span></span>

[<span data-ttu-id="6c38d-159">移除-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6c38d-159">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="6c38d-160">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6c38d-160">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="6c38d-161">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="6c38d-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
