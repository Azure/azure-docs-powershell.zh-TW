---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: ff474116854838c40a4862cf93f4d017ccdf4527
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614850"
---
# <span data-ttu-id="e7007-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e7007-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="e7007-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7007-102">SYNOPSIS</span></span>
<span data-ttu-id="e7007-103">建立資料庫或彈性資料庫。</span><span class="sxs-lookup"><span data-stu-id="e7007-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="e7007-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7007-104">SYNTAX</span></span>

### <span data-ttu-id="e7007-105">DtuBasedDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="e7007-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7007-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="e7007-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7007-107">說明</span><span class="sxs-lookup"><span data-stu-id="e7007-107">DESCRIPTION</span></span>
<span data-ttu-id="e7007-108">**新的-AzSqlDatabase** Cmdlet 會建立 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e7007-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="e7007-109">您也可以將 *ElasticPoolName* 參數設定為現有彈性池，以建立彈性資料庫。</span><span class="sxs-lookup"><span data-stu-id="e7007-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="e7007-110">示例</span><span class="sxs-lookup"><span data-stu-id="e7007-110">EXAMPLES</span></span>

### <span data-ttu-id="e7007-111">範例1：在指定的伺服器上建立資料庫</span><span class="sxs-lookup"><span data-stu-id="e7007-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="e7007-112">這個命令會在伺服器 Server01 上建立名為 Database01 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="e7007-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="e7007-113">範例2：在指定的伺服器上建立彈性資料庫</span><span class="sxs-lookup"><span data-stu-id="e7007-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="e7007-114">這個命令會在伺服器 Server01 上名為 ElasticPool01 的彈性池中建立名為 Database02 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="e7007-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="e7007-115">範例3：在指定的伺服器上建立 Vcore 資料庫</span><span class="sxs-lookup"><span data-stu-id="e7007-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

<span data-ttu-id="e7007-116">這個命令會在伺服器 Server01 上建立名為 Database03 的 Vcore 資料庫。</span><span class="sxs-lookup"><span data-stu-id="e7007-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="e7007-117">參數</span><span class="sxs-lookup"><span data-stu-id="e7007-117">PARAMETERS</span></span>

### <span data-ttu-id="e7007-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7007-118">-AsJob</span></span>
<span data-ttu-id="e7007-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e7007-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7007-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="e7007-120">-CatalogCollation</span></span>
<span data-ttu-id="e7007-121">指定 SQL 資料庫編目排序規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7007-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="e7007-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="e7007-122">-CollationName</span></span>
<span data-ttu-id="e7007-123">指定 SQL 資料庫排序規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7007-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="e7007-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="e7007-124">-ComputeGeneration</span></span>
<span data-ttu-id="e7007-125">要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="e7007-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="e7007-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7007-126">-DatabaseName</span></span>
<span data-ttu-id="e7007-127">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7007-127">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7007-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7007-128">-DefaultProfile</span></span>
<span data-ttu-id="e7007-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e7007-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7007-130">-Edition</span><span class="sxs-lookup"><span data-stu-id="e7007-130">-Edition</span></span>
<span data-ttu-id="e7007-131">指定要指派給資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="e7007-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="e7007-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e7007-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7007-133">所有</span><span class="sxs-lookup"><span data-stu-id="e7007-133">None</span></span>
- <span data-ttu-id="e7007-134">空白</span><span class="sxs-lookup"><span data-stu-id="e7007-134">Basic</span></span>
- <span data-ttu-id="e7007-135">標準</span><span class="sxs-lookup"><span data-stu-id="e7007-135">Standard</span></span>
- <span data-ttu-id="e7007-136">佳</span><span class="sxs-lookup"><span data-stu-id="e7007-136">Premium</span></span>
- <span data-ttu-id="e7007-137">倉庫</span><span class="sxs-lookup"><span data-stu-id="e7007-137">DataWarehouse</span></span>
- <span data-ttu-id="e7007-138">空閒</span><span class="sxs-lookup"><span data-stu-id="e7007-138">Free</span></span>
- <span data-ttu-id="e7007-139">伸縮</span><span class="sxs-lookup"><span data-stu-id="e7007-139">Stretch</span></span>
- <span data-ttu-id="e7007-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="e7007-140">GeneralPurpose</span></span>
- <span data-ttu-id="e7007-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="e7007-141">BusinessCritical</span></span>

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

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7007-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e7007-142">-ElasticPoolName</span></span>
<span data-ttu-id="e7007-143">指定要放入資料庫之彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7007-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="e7007-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e7007-144">-LicenseType</span></span>
<span data-ttu-id="e7007-145">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="e7007-145">The license type for the Azure Sql database.</span></span> <span data-ttu-id="e7007-146">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="e7007-146">Possible values are:</span></span>
- <span data-ttu-id="e7007-147">BasePrice-Azure 混合式福利 () AHB 現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="e7007-147">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="e7007-148">現有 SQL Server 授權擁有者的資料庫價格將會打折。</span><span class="sxs-lookup"><span data-stu-id="e7007-148">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="e7007-149">LicenseIncluded-Azure 混合式福利 () AHB 不會套用現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="e7007-149">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="e7007-150">資料庫價格將包含新的 SQL Server 授權成本。</span><span class="sxs-lookup"><span data-stu-id="e7007-150">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="e7007-151">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="e7007-151">-MaxSizeBytes</span></span>
<span data-ttu-id="e7007-152">指定資料庫的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e7007-152">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7007-153">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="e7007-153">-ReadScale</span></span>
<span data-ttu-id="e7007-154">要指派給 Azure SQL 資料庫的 [讀取比例] 選項。 (啟用/停用) </span><span class="sxs-lookup"><span data-stu-id="e7007-154">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7007-155">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e7007-155">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="e7007-156">指定要指派給資料庫之服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7007-156">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="e7007-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7007-157">-ResourceGroupName</span></span>
<span data-ttu-id="e7007-158">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7007-158">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e7007-159">-SampleName</span><span class="sxs-lookup"><span data-stu-id="e7007-159">-SampleName</span></span>
<span data-ttu-id="e7007-160">建立此資料庫時要套用之範例架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7007-160">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7007-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e7007-161">-ServerName</span></span>
<span data-ttu-id="e7007-162">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="e7007-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="e7007-163">-標記</span><span class="sxs-lookup"><span data-stu-id="e7007-163">-Tags</span></span>
<span data-ttu-id="e7007-164">以這個 Cmdlet 所關聯的雜湊資料表形式，指定鍵值對的字典。</span><span class="sxs-lookup"><span data-stu-id="e7007-164">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="e7007-165">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e7007-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e7007-166">-VCore</span><span class="sxs-lookup"><span data-stu-id="e7007-166">-VCore</span></span>
<span data-ttu-id="e7007-167">Azure Sql 資料庫的 Vcore 號碼</span><span class="sxs-lookup"><span data-stu-id="e7007-167">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="e7007-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="e7007-168">-ZoneRedundant</span></span>
<span data-ttu-id="e7007-169">要與 Azure Sql 資料庫建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="e7007-169">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="e7007-170">-確認</span><span class="sxs-lookup"><span data-stu-id="e7007-170">-Confirm</span></span>
<span data-ttu-id="e7007-171">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e7007-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7007-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7007-172">-WhatIf</span></span>
<span data-ttu-id="e7007-173">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e7007-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7007-174">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7007-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7007-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7007-175">CommonParameters</span></span>
<span data-ttu-id="e7007-176">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7007-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7007-177">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e7007-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7007-178">輸入</span><span class="sxs-lookup"><span data-stu-id="e7007-178">INPUTS</span></span>

### <span data-ttu-id="e7007-179">System.object</span><span class="sxs-lookup"><span data-stu-id="e7007-179">System.String</span></span>

## <span data-ttu-id="e7007-180">輸出</span><span class="sxs-lookup"><span data-stu-id="e7007-180">OUTPUTS</span></span>

### <span data-ttu-id="e7007-181">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="e7007-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="e7007-182">筆記</span><span class="sxs-lookup"><span data-stu-id="e7007-182">NOTES</span></span>

## <span data-ttu-id="e7007-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7007-183">RELATED LINKS</span></span>

[<span data-ttu-id="e7007-184">AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e7007-184">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="e7007-185">新-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e7007-185">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="e7007-186">新-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e7007-186">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="e7007-187">移除-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e7007-187">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="e7007-188">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e7007-188">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="e7007-189">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e7007-189">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="e7007-190">暫停-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e7007-190">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="e7007-191">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="e7007-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

