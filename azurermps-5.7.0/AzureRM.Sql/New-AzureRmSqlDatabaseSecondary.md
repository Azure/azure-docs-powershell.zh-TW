---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: b23128d2ef55e971f20569e251601b410b218ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444235"
---
# <span data-ttu-id="de208-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="de208-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="de208-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de208-102">SYNOPSIS</span></span>
<span data-ttu-id="de208-103">建立現有資料庫的次要資料庫並開始資料複製。</span><span class="sxs-lookup"><span data-stu-id="de208-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de208-104">句法</span><span class="sxs-lookup"><span data-stu-id="de208-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de208-105">說明</span><span class="sxs-lookup"><span data-stu-id="de208-105">DESCRIPTION</span></span>
<span data-ttu-id="de208-106">**新的-AzureRMSqlDatabaseSecondary** Cmdlet 會在用於設定資料庫異地複製時取代 Start-AzureSqlDatabaseCopy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de208-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="de208-107">它會將地域複製連結化物件從主要資料庫傳回次要資料庫。</span><span class="sxs-lookup"><span data-stu-id="de208-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="de208-108">示例</span><span class="sxs-lookup"><span data-stu-id="de208-108">EXAMPLES</span></span>

### <span data-ttu-id="de208-109">1：建立作用中 Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="de208-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="de208-110">參數</span><span class="sxs-lookup"><span data-stu-id="de208-110">PARAMETERS</span></span>

### <span data-ttu-id="de208-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="de208-111">-AllowConnections</span></span>
<span data-ttu-id="de208-112">指定副 Azure SQL 資料庫的閱讀意圖。</span><span class="sxs-lookup"><span data-stu-id="de208-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="de208-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="de208-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="de208-114">不</span><span class="sxs-lookup"><span data-stu-id="de208-114">No</span></span>
- <span data-ttu-id="de208-115">同時</span><span class="sxs-lookup"><span data-stu-id="de208-115">All</span></span>

```yaml
Type: AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de208-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de208-116">-AsJob</span></span>
<span data-ttu-id="de208-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="de208-117">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de208-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="de208-118">-DatabaseName</span></span>
<span data-ttu-id="de208-119">指定要作為主要的資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="de208-119">Specifies the name of the database to act as primary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de208-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de208-120">-DefaultProfile</span></span>
<span data-ttu-id="de208-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="de208-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de208-122">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de208-122">-PartnerResourceGroupName</span></span>
<span data-ttu-id="de208-123">指定此 Cmdlet 指派副資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="de208-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de208-124">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="de208-124">-PartnerServerName</span></span>
<span data-ttu-id="de208-125">指定要作為副的 Azure SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="de208-125">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de208-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de208-126">-ResourceGroupName</span></span>
<span data-ttu-id="de208-127">指定此 Cmdlet 指派主要資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="de208-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de208-128">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="de208-128">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="de208-129">指定要放入次要資料庫的彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="de208-129">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de208-130">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="de208-130">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="de208-131">指定要指派給次要資料庫的服務目標名稱。</span><span class="sxs-lookup"><span data-stu-id="de208-131">Specifies the name of the service objective to assign to the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de208-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="de208-132">-ServerName</span></span>
<span data-ttu-id="de208-133">指定主要 SQL 資料庫之 SQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="de208-133">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de208-134">-標記</span><span class="sxs-lookup"><span data-stu-id="de208-134">-Tags</span></span>
<span data-ttu-id="de208-135">指定雜湊資料表形式的鍵值對，以與 SQL 資料庫複製連結建立關聯。</span><span class="sxs-lookup"><span data-stu-id="de208-135">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="de208-136">例如：</span><span class="sxs-lookup"><span data-stu-id="de208-136">For example:</span></span>

<span data-ttu-id="de208-137">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="de208-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de208-138">-確認</span><span class="sxs-lookup"><span data-stu-id="de208-138">-Confirm</span></span>
<span data-ttu-id="de208-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="de208-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de208-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de208-140">-WhatIf</span></span>
<span data-ttu-id="de208-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de208-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de208-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de208-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de208-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de208-143">CommonParameters</span></span>
<span data-ttu-id="de208-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de208-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de208-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="de208-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de208-146">輸入</span><span class="sxs-lookup"><span data-stu-id="de208-146">INPUTS</span></span>

### <span data-ttu-id="de208-147">所有</span><span class="sxs-lookup"><span data-stu-id="de208-147">None</span></span>
<span data-ttu-id="de208-148">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="de208-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de208-149">輸出</span><span class="sxs-lookup"><span data-stu-id="de208-149">OUTPUTS</span></span>

### <span data-ttu-id="de208-150">AzureReplicationLinkModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="de208-150">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="de208-151">這個 Cmdlet 會傳回 **ReplicationLink** 物件。</span><span class="sxs-lookup"><span data-stu-id="de208-151">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="de208-152">筆記</span><span class="sxs-lookup"><span data-stu-id="de208-152">NOTES</span></span>

## <span data-ttu-id="de208-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="de208-153">RELATED LINKS</span></span>

[<span data-ttu-id="de208-154">移除-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="de208-154">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="de208-155">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="de208-155">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="de208-156">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="de208-156">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
