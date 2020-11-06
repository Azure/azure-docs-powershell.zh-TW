---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: d2af2095198cf0a1102e3422716013f2f2e02fc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448188"
---
# <span data-ttu-id="91caf-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="91caf-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="91caf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91caf-102">SYNOPSIS</span></span>
<span data-ttu-id="91caf-103">建立現有資料庫的次要資料庫並開始資料複製。</span><span class="sxs-lookup"><span data-stu-id="91caf-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91caf-104">句法</span><span class="sxs-lookup"><span data-stu-id="91caf-104">SYNTAX</span></span>

### <span data-ttu-id="91caf-105">DtuBasedDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="91caf-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-LicenseType <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91caf-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="91caf-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91caf-107">說明</span><span class="sxs-lookup"><span data-stu-id="91caf-107">DESCRIPTION</span></span>
<span data-ttu-id="91caf-108">**新的-AzureRMSqlDatabaseSecondary** Cmdlet 會在用於設定資料庫異地複製時取代 Start-AzureSqlDatabaseCopy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91caf-108">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="91caf-109">它會將地域複製連結化物件從主要資料庫傳回次要資料庫。</span><span class="sxs-lookup"><span data-stu-id="91caf-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="91caf-110">示例</span><span class="sxs-lookup"><span data-stu-id="91caf-110">EXAMPLES</span></span>

### <span data-ttu-id="91caf-111">1：建立作用中 Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="91caf-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="91caf-112">參數</span><span class="sxs-lookup"><span data-stu-id="91caf-112">PARAMETERS</span></span>

### <span data-ttu-id="91caf-113">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="91caf-113">-AllowConnections</span></span>
<span data-ttu-id="91caf-114">指定副 Azure SQL 資料庫的閱讀意圖。</span><span class="sxs-lookup"><span data-stu-id="91caf-114">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="91caf-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="91caf-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91caf-116">不</span><span class="sxs-lookup"><span data-stu-id="91caf-116">No</span></span>
- <span data-ttu-id="91caf-117">同時</span><span class="sxs-lookup"><span data-stu-id="91caf-117">All</span></span>

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

### <span data-ttu-id="91caf-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91caf-118">-AsJob</span></span>
<span data-ttu-id="91caf-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="91caf-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91caf-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="91caf-120">-DatabaseName</span></span>
<span data-ttu-id="91caf-121">指定要作為主要的資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="91caf-121">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="91caf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91caf-122">-DefaultProfile</span></span>
<span data-ttu-id="91caf-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="91caf-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91caf-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="91caf-124">-LicenseType</span></span>
<span data-ttu-id="91caf-125">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="91caf-125">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="91caf-126">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91caf-126">-PartnerResourceGroupName</span></span>
<span data-ttu-id="91caf-127">指定此 Cmdlet 指派副資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="91caf-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="91caf-128">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="91caf-128">-PartnerServerName</span></span>
<span data-ttu-id="91caf-129">指定要作為副的 Azure SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="91caf-129">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="91caf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91caf-130">-ResourceGroupName</span></span>
<span data-ttu-id="91caf-131">指定此 Cmdlet 指派主要資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="91caf-131">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="91caf-132">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="91caf-132">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="91caf-133">Azure Sql 資料庫副的計算產生方式。</span><span class="sxs-lookup"><span data-stu-id="91caf-133">The compute generation of teh Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="91caf-134">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="91caf-134">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="91caf-135">指定要放入次要資料庫的彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="91caf-135">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="91caf-136">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="91caf-136">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="91caf-137">指定要指派給次要資料庫的服務目標名稱。</span><span class="sxs-lookup"><span data-stu-id="91caf-137">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="91caf-138">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="91caf-138">-SecondaryVCore</span></span>
<span data-ttu-id="91caf-139">Azure Sql 資料庫副的 Vcore 號碼。</span><span class="sxs-lookup"><span data-stu-id="91caf-139">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="91caf-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="91caf-140">-ServerName</span></span>
<span data-ttu-id="91caf-141">指定主要 SQL 資料庫之 SQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="91caf-141">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="91caf-142">-標記</span><span class="sxs-lookup"><span data-stu-id="91caf-142">-Tags</span></span>
<span data-ttu-id="91caf-143">指定雜湊資料表形式的鍵值對，以與 SQL 資料庫複製連結建立關聯。</span><span class="sxs-lookup"><span data-stu-id="91caf-143">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="91caf-144">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="91caf-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="91caf-145">-確認</span><span class="sxs-lookup"><span data-stu-id="91caf-145">-Confirm</span></span>
<span data-ttu-id="91caf-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="91caf-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91caf-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91caf-147">-WhatIf</span></span>
<span data-ttu-id="91caf-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="91caf-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91caf-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91caf-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91caf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91caf-150">CommonParameters</span></span>
<span data-ttu-id="91caf-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91caf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91caf-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91caf-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91caf-153">輸入</span><span class="sxs-lookup"><span data-stu-id="91caf-153">INPUTS</span></span>

### <span data-ttu-id="91caf-154">System.object</span><span class="sxs-lookup"><span data-stu-id="91caf-154">System.String</span></span>

## <span data-ttu-id="91caf-155">輸出</span><span class="sxs-lookup"><span data-stu-id="91caf-155">OUTPUTS</span></span>

### <span data-ttu-id="91caf-156">AzureReplicationLinkModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="91caf-156">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="91caf-157">筆記</span><span class="sxs-lookup"><span data-stu-id="91caf-157">NOTES</span></span>

## <span data-ttu-id="91caf-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="91caf-158">RELATED LINKS</span></span>

[<span data-ttu-id="91caf-159">移除-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="91caf-159">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="91caf-160">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="91caf-160">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="91caf-161">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="91caf-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
