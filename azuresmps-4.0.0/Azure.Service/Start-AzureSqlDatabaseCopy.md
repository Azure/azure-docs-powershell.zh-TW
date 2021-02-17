---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413059"
---
# <span data-ttu-id="f109d-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f109d-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="f109d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f109d-102">SYNOPSIS</span></span>
<span data-ttu-id="f109d-103">啟動 Azure SQL 資料庫的複製作業。</span><span class="sxs-lookup"><span data-stu-id="f109d-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="f109d-104">語法</span><span class="sxs-lookup"><span data-stu-id="f109d-104">SYNTAX</span></span>

### <span data-ttu-id="f109d-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f109d-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f109d-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="f109d-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f109d-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f109d-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f109d-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="f109d-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f109d-109">描述</span><span class="sxs-lookup"><span data-stu-id="f109d-109">DESCRIPTION</span></span>
<span data-ttu-id="f109d-110">**Start-AzureSqlDatabaseCopy** Cmdlet 會啟動一次複製作業或特定 Azure SQL Database 的連續複製作業。</span><span class="sxs-lookup"><span data-stu-id="f109d-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="f109d-111">此 Cmdlet 並非專案。</span><span class="sxs-lookup"><span data-stu-id="f109d-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="f109d-112">原始資料庫是源資料庫。</span><span class="sxs-lookup"><span data-stu-id="f109d-112">The original database is the source database.</span></span>
<span data-ttu-id="f109d-113">此副本是次要或目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="f109d-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="f109d-114">對於連續的複製，來源和目標資料庫不能位於同一個伺服器上，而主託管來源和目標資料庫的伺服器必須是相同訂閱的一部分。</span><span class="sxs-lookup"><span data-stu-id="f109d-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="f109d-115">如果您未指定 *ContinuousCopy* 參數，此 Cmdlet 會建立源資料庫的一次副本。</span><span class="sxs-lookup"><span data-stu-id="f109d-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="f109d-116">收到回應時，作業可能仍在進行中。</span><span class="sxs-lookup"><span data-stu-id="f109d-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="f109d-117">您可以使用 Cmdlet 或 Cmdlet Get-AzureSqlDatabaseCopy或Get-AzureSqlDatabaseOperation作業。</span><span class="sxs-lookup"><span data-stu-id="f109d-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="f109d-118">如果您指定 *ContinuousCopy，* 此 Cmdlet 會建立源資料庫的連續副本。</span><span class="sxs-lookup"><span data-stu-id="f109d-118">If you specify *ContinuousCopy*, this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="f109d-119">收到回應時，作業將會進行中。</span><span class="sxs-lookup"><span data-stu-id="f109d-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="f109d-120">您可以使用 **Get-AzuresqlDatabaseCopy** 或 **Get-AzureSqlDatabaseOperation 監控作業**。</span><span class="sxs-lookup"><span data-stu-id="f109d-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="f109d-121">您可以將連續的複製建立為線上或離線資料庫。</span><span class="sxs-lookup"><span data-stu-id="f109d-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="f109d-122">線上連續副本可用來設定 Azure SQL database Geo-Replication活動資料庫 https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ 。</span><span class="sxs-lookup"><span data-stu-id="f109d-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="f109d-123">離線連續副本可用來設定 Azure SQL database Geo-Replication標準資料夾 https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ 。</span><span class="sxs-lookup"><span data-stu-id="f109d-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="f109d-124">例子</span><span class="sxs-lookup"><span data-stu-id="f109d-124">EXAMPLES</span></span>

### <span data-ttu-id="f109d-125">範例 1：排程連續資料庫副本</span><span class="sxs-lookup"><span data-stu-id="f109d-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="f109d-126">此命令會在伺服器上排程名為 lpqd0zbr8y 的 Orders 資料庫的連續副本。</span><span class="sxs-lookup"><span data-stu-id="f109d-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="f109d-127">該命令會在伺服器上建立名為 bk0b8kf658 的目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="f109d-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="f109d-128">範例 2：在同一個伺服器上建立一次副本</span><span class="sxs-lookup"><span data-stu-id="f109d-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="f109d-129">此命令會在伺服器上名為 lpqd0zbr8y 的 Orders 建立一次資料庫的一次副本。</span><span class="sxs-lookup"><span data-stu-id="f109d-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="f109d-130">該命令會在同一個伺服器上建立名為 OrdersCopy 的複製。</span><span class="sxs-lookup"><span data-stu-id="f109d-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="f109d-131">範例 3：排程連續離線資料庫副本</span><span class="sxs-lookup"><span data-stu-id="f109d-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="f109d-132">此命令會在伺服器上排程名為 lpqd0zbr8y 的 Orders 資料庫的連續副本。</span><span class="sxs-lookup"><span data-stu-id="f109d-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="f109d-133">此命令會在伺服器上建立一個名為 bk0b8kf658 的離線目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="f109d-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="f109d-134">參數</span><span class="sxs-lookup"><span data-stu-id="f109d-134">PARAMETERS</span></span>

### <span data-ttu-id="f109d-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="f109d-135">-ContinuousCopy</span></span>
<span data-ttu-id="f109d-136">表示資料庫複本為複本資料庫 (複本) 。</span><span class="sxs-lookup"><span data-stu-id="f109d-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="f109d-137">同一伺服器不支援連續複製。</span><span class="sxs-lookup"><span data-stu-id="f109d-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="f109d-138">如果未指定此參數，則執行一次複製。</span><span class="sxs-lookup"><span data-stu-id="f109d-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="f109d-139">對於一次複製，來源和合作夥伴資料庫必須位於同一個伺服器上。</span><span class="sxs-lookup"><span data-stu-id="f109d-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f109d-140">-資料庫</span><span class="sxs-lookup"><span data-stu-id="f109d-140">-Database</span></span>
<span data-ttu-id="f109d-141">指定代表來源 Azure SQL Database 的物件。</span><span class="sxs-lookup"><span data-stu-id="f109d-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="f109d-142">此參數接受管線輸入。</span><span class="sxs-lookup"><span data-stu-id="f109d-142">This parameter accepts pipeline input.</span></span>

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f109d-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f109d-143">-DatabaseName</span></span>
<span data-ttu-id="f109d-144">指定源資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f109d-144">Specifies the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f109d-145">-強制</span><span class="sxs-lookup"><span data-stu-id="f109d-145">-Force</span></span>
<span data-ttu-id="f109d-146">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f109d-146">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f109d-147">-Offline2010</span><span class="sxs-lookup"><span data-stu-id="f109d-147">-OfflineSecondary</span></span>
<span data-ttu-id="f109d-148">指定連續的複製為被動副本，而不是使用中複製。</span><span class="sxs-lookup"><span data-stu-id="f109d-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="f109d-149">如果源資料庫是 Standard edition 資料庫，則此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="f109d-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="f109d-150">如果指定此參數，則必須同時指定 *ContinuousCopy。*</span><span class="sxs-lookup"><span data-stu-id="f109d-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f109d-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="f109d-151">-PartnerDatabase</span></span>
<span data-ttu-id="f109d-152">指定目標資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f109d-152">Specifies name of the target database.</span></span>
<span data-ttu-id="f109d-153">如果您指定 *ContinuousCopy* 參數 *，PartnerDatabase* 的值必須與源資料庫的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="f109d-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="f109d-154">如果您未指定 *ContinuousCopy，* 則必須指定目標資料庫的名稱，此名稱可能會與源資料庫名稱不同。</span><span class="sxs-lookup"><span data-stu-id="f109d-154">If you do not specify *ContinuousCopy*, you must specify a name for the target database, which can be different from the source database name.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f109d-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="f109d-155">-PartnerServer</span></span>
<span data-ttu-id="f109d-156">指定主託管目標資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f109d-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="f109d-157">此伺服器必須與源資料庫伺服器在同一個 Azure 訂閱中。</span><span class="sxs-lookup"><span data-stu-id="f109d-157">This server must be in the same Azure subscription as the source database server.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f109d-158">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f109d-158">-Profile</span></span>
<span data-ttu-id="f109d-159">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f109d-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f109d-160">如果您未指定設定檔，此 Cmdlet 會從本地預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f109d-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f109d-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f109d-161">-ServerName</span></span>
<span data-ttu-id="f109d-162">指定源資料庫所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f109d-162">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f109d-163">-確認</span><span class="sxs-lookup"><span data-stu-id="f109d-163">-Confirm</span></span>
<span data-ttu-id="f109d-164">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f109d-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f109d-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f109d-165">-WhatIf</span></span>
<span data-ttu-id="f109d-166">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f109d-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f109d-167">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f109d-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f109d-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f109d-168">CommonParameters</span></span>
<span data-ttu-id="f109d-169">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f109d-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f109d-170">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f109d-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f109d-171">輸入</span><span class="sxs-lookup"><span data-stu-id="f109d-171">INPUTS</span></span>

### <span data-ttu-id="f109d-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="f109d-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="f109d-173">輸出</span><span class="sxs-lookup"><span data-stu-id="f109d-173">OUTPUTS</span></span>

### <span data-ttu-id="f109d-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f109d-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="f109d-175">筆記</span><span class="sxs-lookup"><span data-stu-id="f109d-175">NOTES</span></span>
* <span data-ttu-id="f109d-176">驗證：此 Cmdlet 需要憑證式驗證。</span><span class="sxs-lookup"><span data-stu-id="f109d-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="f109d-177">有關如何使用憑證式驗證來設定目前訂閱的範例，請參閱 New-AzureSqlDatabaseServerContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f109d-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="f109d-178">監控：若要檢查伺服器上一或多個連續的複製關係狀態，請使用 **Get-AzureSqlDatabaseCopy** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f109d-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="f109d-179">若要驗證連續複製關係的來源和目標作業狀態，請使用 **Get-AzureSqlDatabaseOperation** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f109d-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="f109d-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="f109d-180">RELATED LINKS</span></span>

[<span data-ttu-id="f109d-181">Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="f109d-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="f109d-182">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="f109d-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="f109d-183">啟動資料庫複製</span><span class="sxs-lookup"><span data-stu-id="f109d-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[<span data-ttu-id="f109d-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f109d-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="f109d-185">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f109d-185">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


