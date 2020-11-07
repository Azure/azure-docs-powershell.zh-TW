---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967291"
---
# <span data-ttu-id="6fbc6-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6fbc6-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="6fbc6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6fbc6-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbc6-103">啟動 Azure SQL 資料庫的複製作業。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="6fbc6-104">句法</span><span class="sxs-lookup"><span data-stu-id="6fbc6-104">SYNTAX</span></span>

### <span data-ttu-id="6fbc6-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6fbc6-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbc6-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="6fbc6-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbc6-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6fbc6-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbc6-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="6fbc6-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fbc6-109">說明</span><span class="sxs-lookup"><span data-stu-id="6fbc6-109">DESCRIPTION</span></span>
<span data-ttu-id="6fbc6-110">**AzureSqlDatabaseCopy** Cmdlet 會啟動一次性複製作業或特定 Azure SQL 資料庫的連續複製作業。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="6fbc6-111">這個 Cmdlet 不是事務性的。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="6fbc6-112">原始資料庫是源資料庫。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-112">The original database is the source database.</span></span>
<span data-ttu-id="6fbc6-113">複本是次要或目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="6fbc6-114">針對連續複本，來源和目標資料庫不能位於同一個伺服器上，而且主持來源和目標資料庫的伺服器必須屬於相同的訂閱。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="6fbc6-115">如果您沒有指定 *ContinuousCopy* 參數，這個 Cmdlet 會建立來源資料庫的一次性複本。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="6fbc6-116">收到回應時，仍可進行該作業。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="6fbc6-117">您可以使用 Get-AzureSqlDatabaseCopy 或 Get-AzureSqlDatabaseOperation Cmdlet 來監視作業。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="6fbc6-118">如果您指定 *ContinuousCopy* ，這個 Cmdlet 會建立源資料庫的連續複本。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-118">If you specify *ContinuousCopy* , this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="6fbc6-119">收到回應時，作業將會進行中。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="6fbc6-120">您可以使用 **AzureSqlDatabaseCopy** 或 **AzureSqlDatabaseOperation** 來監視作業。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="6fbc6-121">您可以建立連續複本做為線上或離線資料庫。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="6fbc6-122">線上連續複本是用來設定 Azure SQL Database 的作用中 Geo-Replication https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ 。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="6fbc6-123">離線連續副本是用來設定 Azure SQL Database 的標準 Geo-Replication https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ 。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="6fbc6-124">示例</span><span class="sxs-lookup"><span data-stu-id="6fbc6-124">EXAMPLES</span></span>

### <span data-ttu-id="6fbc6-125">範例1：排程連續資料庫複製</span><span class="sxs-lookup"><span data-stu-id="6fbc6-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="6fbc6-126">這個命令會在名為 lpqd0zbr8y 的伺服器上，排程一個名為 [訂單] 的資料庫連續複本。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="6fbc6-127">該命令會在伺服器上建立名為 bk0b8kf658 的目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="6fbc6-128">範例2：在同一個伺服器上建立一次性複本</span><span class="sxs-lookup"><span data-stu-id="6fbc6-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="6fbc6-129">這個命令會在名為 lpqd0zbr8y 的伺服器上，建立名為「訂單」的單一時間複本。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="6fbc6-130">該命令會在同一台伺服器上建立名為 OrdersCopy 的複本。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="6fbc6-131">範例3：排程連續離線資料庫複本</span><span class="sxs-lookup"><span data-stu-id="6fbc6-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="6fbc6-132">這個命令會在名為 lpqd0zbr8y 的伺服器上，排程一個名為 [訂單] 的資料庫連續複本。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="6fbc6-133">這個命令會在伺服器上建立名為 bk0b8kf658 的離線目標資料庫。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="6fbc6-134">參數</span><span class="sxs-lookup"><span data-stu-id="6fbc6-134">PARAMETERS</span></span>

### <span data-ttu-id="6fbc6-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="6fbc6-135">-ContinuousCopy</span></span>
<span data-ttu-id="6fbc6-136">表示資料庫複本將是複本資料庫 (的連續複本) 。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="6fbc6-137">在同一個伺服器中不支援連續複製。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="6fbc6-138">如果未指定此參數，則會執行一次性複本。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="6fbc6-139">若是一次性複本，來源與夥伴資料庫必須在同一個伺服器上。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

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

### <span data-ttu-id="6fbc6-140">-資料庫</span><span class="sxs-lookup"><span data-stu-id="6fbc6-140">-Database</span></span>
<span data-ttu-id="6fbc6-141">指定代表來源 Azure SQL 資料庫的物件。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="6fbc6-142">這個參數接受管線輸入。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-142">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="6fbc6-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6fbc6-143">-DatabaseName</span></span>
<span data-ttu-id="6fbc6-144">指定源資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-144">Specifies the name of the source database.</span></span>

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

### <span data-ttu-id="6fbc6-145">-Force</span><span class="sxs-lookup"><span data-stu-id="6fbc6-145">-Force</span></span>
<span data-ttu-id="6fbc6-146">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-146">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6fbc6-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="6fbc6-147">-OfflineSecondary</span></span>
<span data-ttu-id="6fbc6-148">指定連續複製是一個被動複本，而不是使用中的複本。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="6fbc6-149">如果源資料庫是標準版本的資料庫，則需要此參數。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="6fbc6-150">如果指定此參數，則也必須指定 *ContinuousCopy* 。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

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

### <span data-ttu-id="6fbc6-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="6fbc6-151">-PartnerDatabase</span></span>
<span data-ttu-id="6fbc6-152">指定目標資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-152">Specifies name of the target database.</span></span>
<span data-ttu-id="6fbc6-153">如果您指定 *ContinuousCopy* 參數， *PartnerDatabase* 的值必須與源資料庫的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="6fbc6-154">如果您沒有指定 *ContinuousCopy* ，您必須指定目標資料庫的名稱，這可能與源資料庫名稱不同。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-154">If you do not specify *ContinuousCopy* , you must specify a name for the target database, which can be different from the source database name.</span></span>

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

### <span data-ttu-id="6fbc6-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="6fbc6-155">-PartnerServer</span></span>
<span data-ttu-id="6fbc6-156">指定主持目標資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="6fbc6-157">此伺服器必須與源資料庫伺服器位於相同的 Azure 訂閱中。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-157">This server must be in the same Azure subscription as the source database server.</span></span>

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

### <span data-ttu-id="6fbc6-158">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6fbc6-158">-Profile</span></span>
<span data-ttu-id="6fbc6-159">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6fbc6-160">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6fbc6-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6fbc6-161">-ServerName</span></span>
<span data-ttu-id="6fbc6-162">指定源資料庫所在之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-162">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="6fbc6-163">-確認</span><span class="sxs-lookup"><span data-stu-id="6fbc6-163">-Confirm</span></span>
<span data-ttu-id="6fbc6-164">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fbc6-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fbc6-165">-WhatIf</span></span>
<span data-ttu-id="6fbc6-166">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fbc6-167">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fbc6-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbc6-168">CommonParameters</span></span>
<span data-ttu-id="6fbc6-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbc6-170">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbc6-171">輸入</span><span class="sxs-lookup"><span data-stu-id="6fbc6-171">INPUTS</span></span>

### <span data-ttu-id="6fbc6-172">SqlDatabase.. Database （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="6fbc6-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="6fbc6-173">輸出</span><span class="sxs-lookup"><span data-stu-id="6fbc6-173">OUTPUTS</span></span>

### <span data-ttu-id="6fbc6-174">WindowsAzure. SqlDatabase. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6fbc6-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="6fbc6-175">筆記</span><span class="sxs-lookup"><span data-stu-id="6fbc6-175">NOTES</span></span>
* <span data-ttu-id="6fbc6-176">驗證：此 Cmdlet 需要以憑證為基礎的驗證。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="6fbc6-177">如需如何使用以憑證為基礎的驗證來設定目前訂閱的範例，請參閱 New-AzureSqlDatabaseServerContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="6fbc6-178">監視：若要檢查伺服器上作用中的一或多個連續複本關聯的狀態，請使用 **AzureSqlDatabaseCopy** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="6fbc6-179">若要確認連續複製關聯之來源和目標上的作業狀態，請使用 **AzureSqlDatabaseOperation** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fbc6-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="6fbc6-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="6fbc6-180">RELATED LINKS</span></span>

[<span data-ttu-id="6fbc6-181">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="6fbc6-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="6fbc6-182">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="6fbc6-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="6fbc6-183">開始資料庫複製</span><span class="sxs-lookup"><span data-stu-id="6fbc6-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[<span data-ttu-id="6fbc6-184">Azure SQL 資料庫 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6fbc6-184">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="6fbc6-185">AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6fbc6-185">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="6fbc6-186">停止 AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6fbc6-186">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


