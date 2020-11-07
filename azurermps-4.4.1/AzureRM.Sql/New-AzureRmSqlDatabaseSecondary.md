---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 226910b81da287c04adb05574b77713e97c6a045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623636"
---
# <span data-ttu-id="952da-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="952da-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="952da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="952da-102">SYNOPSIS</span></span>
<span data-ttu-id="952da-103">建立現有資料庫的次要資料庫並開始資料複製。</span><span class="sxs-lookup"><span data-stu-id="952da-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="952da-104">句法</span><span class="sxs-lookup"><span data-stu-id="952da-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="952da-105">說明</span><span class="sxs-lookup"><span data-stu-id="952da-105">DESCRIPTION</span></span>
<span data-ttu-id="952da-106">**新的-AzureRMSqlDatabaseSecondary** Cmdlet 會在用於設定資料庫異地複製時取代 Start-AzureSqlDatabaseCopy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="952da-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="952da-107">它會將地域複製連結化物件從主要資料庫傳回次要資料庫。</span><span class="sxs-lookup"><span data-stu-id="952da-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="952da-108">示例</span><span class="sxs-lookup"><span data-stu-id="952da-108">EXAMPLES</span></span>

### <span data-ttu-id="952da-109">1：建立作用中 Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="952da-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="952da-110">參數</span><span class="sxs-lookup"><span data-stu-id="952da-110">PARAMETERS</span></span>

### <span data-ttu-id="952da-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="952da-111">-AllowConnections</span></span>
<span data-ttu-id="952da-112">指定副 Azure SQL 資料庫的閱讀意圖。</span><span class="sxs-lookup"><span data-stu-id="952da-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="952da-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="952da-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="952da-114">不</span><span class="sxs-lookup"><span data-stu-id="952da-114">No</span></span>
- <span data-ttu-id="952da-115">同時</span><span class="sxs-lookup"><span data-stu-id="952da-115">All</span></span>

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

### <span data-ttu-id="952da-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="952da-116">-DatabaseName</span></span>
<span data-ttu-id="952da-117">指定要作為主要的資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="952da-117">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="952da-118">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="952da-118">-PartnerResourceGroupName</span></span>
<span data-ttu-id="952da-119">指定此 Cmdlet 指派副資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="952da-119">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="952da-120">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="952da-120">-PartnerServerName</span></span>
<span data-ttu-id="952da-121">指定要作為副的 Azure SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="952da-121">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="952da-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="952da-122">-ResourceGroupName</span></span>
<span data-ttu-id="952da-123">指定此 Cmdlet 指派主要資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="952da-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="952da-124">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="952da-124">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="952da-125">指定要放入次要資料庫的彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="952da-125">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="952da-126">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="952da-126">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="952da-127">指定要指派給次要資料庫的服務目標名稱。</span><span class="sxs-lookup"><span data-stu-id="952da-127">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="952da-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="952da-128">-ServerName</span></span>
<span data-ttu-id="952da-129">指定主要 SQL 資料庫之 SQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="952da-129">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="952da-130">-標記</span><span class="sxs-lookup"><span data-stu-id="952da-130">-Tags</span></span>
<span data-ttu-id="952da-131">指定雜湊資料表形式的鍵值對，以與 SQL 資料庫複製連結建立關聯。</span><span class="sxs-lookup"><span data-stu-id="952da-131">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="952da-132">例如：</span><span class="sxs-lookup"><span data-stu-id="952da-132">For example:</span></span>

<span data-ttu-id="952da-133">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="952da-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="952da-134">-確認</span><span class="sxs-lookup"><span data-stu-id="952da-134">-Confirm</span></span>
<span data-ttu-id="952da-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="952da-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="952da-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="952da-136">-WhatIf</span></span>
<span data-ttu-id="952da-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="952da-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="952da-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="952da-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="952da-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="952da-139">-DefaultProfile</span></span>
<span data-ttu-id="952da-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="952da-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="952da-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="952da-141">CommonParameters</span></span>
<span data-ttu-id="952da-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="952da-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="952da-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="952da-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="952da-144">輸入</span><span class="sxs-lookup"><span data-stu-id="952da-144">INPUTS</span></span>

## <span data-ttu-id="952da-145">輸出</span><span class="sxs-lookup"><span data-stu-id="952da-145">OUTPUTS</span></span>

### <span data-ttu-id="952da-146">AzureReplicationLinkModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="952da-146">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="952da-147">這個 Cmdlet 會傳回 **ReplicationLink** 物件。</span><span class="sxs-lookup"><span data-stu-id="952da-147">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="952da-148">筆記</span><span class="sxs-lookup"><span data-stu-id="952da-148">NOTES</span></span>

## <span data-ttu-id="952da-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="952da-149">RELATED LINKS</span></span>

[<span data-ttu-id="952da-150">移除-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="952da-150">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="952da-151">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="952da-151">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="952da-152">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="952da-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
