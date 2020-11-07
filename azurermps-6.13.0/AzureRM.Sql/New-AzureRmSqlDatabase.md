---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 7eaa753b973b887cbbddc132b998d05f3e374e3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625551"
---
# <span data-ttu-id="97e92-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="97e92-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="97e92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97e92-102">SYNOPSIS</span></span>
<span data-ttu-id="97e92-103">建立資料庫或彈性資料庫。</span><span class="sxs-lookup"><span data-stu-id="97e92-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97e92-104">句法</span><span class="sxs-lookup"><span data-stu-id="97e92-104">SYNTAX</span></span>

### <span data-ttu-id="97e92-105">DtuBasedDatabase (預設) </span><span class="sxs-lookup"><span data-stu-id="97e92-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e92-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="97e92-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97e92-107">說明</span><span class="sxs-lookup"><span data-stu-id="97e92-107">DESCRIPTION</span></span>
<span data-ttu-id="97e92-108">**新的-AzureRmSqlDatabase** Cmdlet 會建立 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="97e92-108">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="97e92-109">您也可以將 *ElasticPoolName* 參數設定為現有彈性池，以建立彈性資料庫。</span><span class="sxs-lookup"><span data-stu-id="97e92-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="97e92-110">示例</span><span class="sxs-lookup"><span data-stu-id="97e92-110">EXAMPLES</span></span>

### <span data-ttu-id="97e92-111">範例1：在指定的伺服器上建立資料庫</span><span class="sxs-lookup"><span data-stu-id="97e92-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="97e92-112">這個命令會在伺服器 Server01 上建立名為 Database01 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="97e92-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="97e92-113">範例2：在指定的伺服器上建立彈性資料庫</span><span class="sxs-lookup"><span data-stu-id="97e92-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="97e92-114">這個命令會在伺服器 Server01 上名為 ElasticPool01 的彈性池中建立名為 Database02 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="97e92-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="97e92-115">範例3：在指定的伺服器上建立 Vcore 資料庫</span><span class="sxs-lookup"><span data-stu-id="97e92-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
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

<span data-ttu-id="97e92-116">這個命令會在伺服器 Server01 上建立名為 Database03 的 Vcore 資料庫。</span><span class="sxs-lookup"><span data-stu-id="97e92-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="97e92-117">參數</span><span class="sxs-lookup"><span data-stu-id="97e92-117">PARAMETERS</span></span>

### <span data-ttu-id="97e92-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97e92-118">-AsJob</span></span>
<span data-ttu-id="97e92-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="97e92-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97e92-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="97e92-120">-CatalogCollation</span></span>
<span data-ttu-id="97e92-121">指定 SQL 資料庫編目排序規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="97e92-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="97e92-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="97e92-122">-CollationName</span></span>
<span data-ttu-id="97e92-123">指定 SQL 資料庫排序規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="97e92-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="97e92-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="97e92-124">-ComputeGeneration</span></span>
<span data-ttu-id="97e92-125">要指派的計算產生。</span><span class="sxs-lookup"><span data-stu-id="97e92-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="97e92-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="97e92-126">-DatabaseName</span></span>
<span data-ttu-id="97e92-127">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="97e92-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="97e92-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e92-128">-DefaultProfile</span></span>
<span data-ttu-id="97e92-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="97e92-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97e92-130">-Edition</span><span class="sxs-lookup"><span data-stu-id="97e92-130">-Edition</span></span>
<span data-ttu-id="97e92-131">指定要指派給資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="97e92-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="97e92-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="97e92-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97e92-133">所有</span><span class="sxs-lookup"><span data-stu-id="97e92-133">None</span></span>
- <span data-ttu-id="97e92-134">空白</span><span class="sxs-lookup"><span data-stu-id="97e92-134">Basic</span></span>
- <span data-ttu-id="97e92-135">標準</span><span class="sxs-lookup"><span data-stu-id="97e92-135">Standard</span></span>
- <span data-ttu-id="97e92-136">佳</span><span class="sxs-lookup"><span data-stu-id="97e92-136">Premium</span></span>
- <span data-ttu-id="97e92-137">倉庫</span><span class="sxs-lookup"><span data-stu-id="97e92-137">DataWarehouse</span></span>
- <span data-ttu-id="97e92-138">空閒</span><span class="sxs-lookup"><span data-stu-id="97e92-138">Free</span></span>
- <span data-ttu-id="97e92-139">伸縮</span><span class="sxs-lookup"><span data-stu-id="97e92-139">Stretch</span></span>
- <span data-ttu-id="97e92-140">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="97e92-140">GeneralPurpose</span></span>
- <span data-ttu-id="97e92-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="97e92-141">BusinessCritical</span></span>

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

### <span data-ttu-id="97e92-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="97e92-142">-ElasticPoolName</span></span>
<span data-ttu-id="97e92-143">指定要放入資料庫之彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="97e92-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="97e92-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="97e92-144">-LicenseType</span></span>
<span data-ttu-id="97e92-145">Azure Sql 資料庫的授權類型。</span><span class="sxs-lookup"><span data-stu-id="97e92-145">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="97e92-146">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="97e92-146">-MaxSizeBytes</span></span>
<span data-ttu-id="97e92-147">指定資料庫的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="97e92-147">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="97e92-148">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="97e92-148">-ReadScale</span></span>
<span data-ttu-id="97e92-149">要指派給 Azure SQL 資料庫的 [讀取比例] 選項。 (啟用/停用) </span><span class="sxs-lookup"><span data-stu-id="97e92-149">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="97e92-150">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="97e92-150">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="97e92-151">指定要指派給資料庫之服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="97e92-151">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="97e92-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97e92-152">-ResourceGroupName</span></span>
<span data-ttu-id="97e92-153">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="97e92-153">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="97e92-154">-SampleName</span><span class="sxs-lookup"><span data-stu-id="97e92-154">-SampleName</span></span>
<span data-ttu-id="97e92-155">建立此資料庫時要套用之範例架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="97e92-155">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="97e92-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="97e92-156">-ServerName</span></span>
<span data-ttu-id="97e92-157">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="97e92-157">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="97e92-158">-標記</span><span class="sxs-lookup"><span data-stu-id="97e92-158">-Tags</span></span>
<span data-ttu-id="97e92-159">以這個 Cmdlet 所關聯的雜湊資料表形式，指定鍵值對的字典。</span><span class="sxs-lookup"><span data-stu-id="97e92-159">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="97e92-160">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="97e92-160">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="97e92-161">-VCore</span><span class="sxs-lookup"><span data-stu-id="97e92-161">-VCore</span></span>
<span data-ttu-id="97e92-162">Azure Sql 資料庫的 Vcore 號碼</span><span class="sxs-lookup"><span data-stu-id="97e92-162">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="97e92-163">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="97e92-163">-ZoneRedundant</span></span>
<span data-ttu-id="97e92-164">要與 Azure Sql 資料庫建立關聯的區域冗余</span><span class="sxs-lookup"><span data-stu-id="97e92-164">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="97e92-165">-確認</span><span class="sxs-lookup"><span data-stu-id="97e92-165">-Confirm</span></span>
<span data-ttu-id="97e92-166">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="97e92-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97e92-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97e92-167">-WhatIf</span></span>
<span data-ttu-id="97e92-168">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="97e92-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97e92-169">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97e92-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97e92-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e92-170">CommonParameters</span></span>
<span data-ttu-id="97e92-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97e92-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e92-172">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97e92-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e92-173">輸入</span><span class="sxs-lookup"><span data-stu-id="97e92-173">INPUTS</span></span>

### <span data-ttu-id="97e92-174">System.object</span><span class="sxs-lookup"><span data-stu-id="97e92-174">System.String</span></span>

## <span data-ttu-id="97e92-175">輸出</span><span class="sxs-lookup"><span data-stu-id="97e92-175">OUTPUTS</span></span>

### <span data-ttu-id="97e92-176">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="97e92-176">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="97e92-177">筆記</span><span class="sxs-lookup"><span data-stu-id="97e92-177">NOTES</span></span>

## <span data-ttu-id="97e92-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="97e92-178">RELATED LINKS</span></span>

[<span data-ttu-id="97e92-179">AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="97e92-179">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="97e92-180">新-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="97e92-180">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="97e92-181">新-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="97e92-181">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="97e92-182">移除-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="97e92-182">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="97e92-183">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="97e92-183">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="97e92-184">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="97e92-184">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="97e92-185">暫停-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="97e92-185">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="97e92-186">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="97e92-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

