---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 7019fc7345b4296d9c35f11c6acec5bf5a42d966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454520"
---
# <span data-ttu-id="cfd5d-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cfd5d-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="cfd5d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cfd5d-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd5d-103">建立在目前時間使用快照的 SQL 資料庫複本。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfd5d-104">句法</span><span class="sxs-lookup"><span data-stu-id="cfd5d-104">SYNTAX</span></span>

### <span data-ttu-id="cfd5d-105">DtuBasedDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="cfd5d-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cfd5d-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="cfd5d-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-Tags <Hashtable>] [-CopyResourceGroupName <String>]
 [-CopyServerName <String>] -CopyDatabaseName <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfd5d-107">說明</span><span class="sxs-lookup"><span data-stu-id="cfd5d-107">DESCRIPTION</span></span>
<span data-ttu-id="cfd5d-108">**新的-AzureRmSqlDatabaseCopy** Cmdlet 會建立 Azure SQL Database 的複本，此資料庫會在目前時間使用資料的快照。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-108">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="cfd5d-109">使用這個 Cmdlet （而不是 Start-AzureSqlDatabaseCopy Cmdlet）來建立一次性的資料庫複本。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-109">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="cfd5d-110">這個 Cmdlet 會傳回復本的 **資料庫** 物件。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-110">This cmdlet returns the **Database** object of the copy.</span></span>
<span data-ttu-id="cfd5d-111">注意：請使用 New-AzureRmSqlDatabaseSecondary Cmdlet 來設定資料庫的異地複製。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-111">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>
<span data-ttu-id="cfd5d-112">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cfd5d-113">示例</span><span class="sxs-lookup"><span data-stu-id="cfd5d-113">EXAMPLES</span></span>

## <span data-ttu-id="cfd5d-114">參數</span><span class="sxs-lookup"><span data-stu-id="cfd5d-114">PARAMETERS</span></span>

### <span data-ttu-id="cfd5d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfd5d-115">-AsJob</span></span>
<span data-ttu-id="cfd5d-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cfd5d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfd5d-117">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="cfd5d-117">-ComputeGeneration</span></span>
<span data-ttu-id="cfd5d-118">要指派給新複本的計算產生。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-118">The compute generation to assign to the new copy.</span></span>

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

### <span data-ttu-id="cfd5d-119">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="cfd5d-119">-CopyDatabaseName</span></span>
<span data-ttu-id="cfd5d-120">指定 SQL 資料庫複本的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-120">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="cfd5d-121">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfd5d-121">-CopyResourceGroupName</span></span>
<span data-ttu-id="cfd5d-122">指定要在其中指派複本的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-122">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="cfd5d-123">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="cfd5d-123">-CopyServerName</span></span>
<span data-ttu-id="cfd5d-124">指定主持複本的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-124">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="cfd5d-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cfd5d-125">-DatabaseName</span></span>
<span data-ttu-id="cfd5d-126">指定要複製的 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-126">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="cfd5d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfd5d-127">-DefaultProfile</span></span>
<span data-ttu-id="cfd5d-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cfd5d-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfd5d-129">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="cfd5d-129">-ElasticPoolName</span></span>
<span data-ttu-id="cfd5d-130">指定要在其中指派複本的彈性池名稱。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-130">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="cfd5d-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="cfd5d-131">-LicenseType</span></span>
<span data-ttu-id="cfd5d-132">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-132">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="cfd5d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfd5d-133">-ResourceGroupName</span></span>
<span data-ttu-id="cfd5d-134">指定包含要複製之資料庫的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-134">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="cfd5d-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cfd5d-135">-ServerName</span></span>
<span data-ttu-id="cfd5d-136">指定包含要複製之資料庫的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-136">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="cfd5d-137">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="cfd5d-137">-ServiceObjectiveName</span></span>
<span data-ttu-id="cfd5d-138">指定要指派給複本之服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-138">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="cfd5d-139">-標記</span><span class="sxs-lookup"><span data-stu-id="cfd5d-139">-Tags</span></span>
<span data-ttu-id="cfd5d-140">指定雜湊資料表形式的鍵值對，以與 Azure SQL 資料庫複本建立關聯。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-140">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="cfd5d-141">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="cfd5d-141">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cfd5d-142">-VCore</span><span class="sxs-lookup"><span data-stu-id="cfd5d-142">-VCore</span></span>
<span data-ttu-id="cfd5d-143">Azure Sql 資料庫複本的 Vcore 號碼。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-143">The Vcore numbers of the Azure Sql Database copy.</span></span>

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

### <span data-ttu-id="cfd5d-144">-確認</span><span class="sxs-lookup"><span data-stu-id="cfd5d-144">-Confirm</span></span>
<span data-ttu-id="cfd5d-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfd5d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfd5d-146">-WhatIf</span></span>
<span data-ttu-id="cfd5d-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfd5d-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfd5d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd5d-149">CommonParameters</span></span>
<span data-ttu-id="cfd5d-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd5d-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd5d-152">輸入</span><span class="sxs-lookup"><span data-stu-id="cfd5d-152">INPUTS</span></span>

### <span data-ttu-id="cfd5d-153">System.object</span><span class="sxs-lookup"><span data-stu-id="cfd5d-153">System.String</span></span>

## <span data-ttu-id="cfd5d-154">輸出</span><span class="sxs-lookup"><span data-stu-id="cfd5d-154">OUTPUTS</span></span>

### <span data-ttu-id="cfd5d-155">AzureSqlDatabaseCopyModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="cfd5d-155">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>

## <span data-ttu-id="cfd5d-156">筆記</span><span class="sxs-lookup"><span data-stu-id="cfd5d-156">NOTES</span></span>

## <span data-ttu-id="cfd5d-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="cfd5d-157">RELATED LINKS</span></span>

[<span data-ttu-id="cfd5d-158">新-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="cfd5d-158">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="cfd5d-159">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="cfd5d-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
