---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 22b74b3dcd76577d7c864a3779d12c8474c431a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446632"
---
# <span data-ttu-id="5b493-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5b493-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="5b493-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b493-102">SYNOPSIS</span></span>
<span data-ttu-id="5b493-103">建立資料庫或彈性資料庫。</span><span class="sxs-lookup"><span data-stu-id="5b493-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b493-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b493-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b493-105">說明</span><span class="sxs-lookup"><span data-stu-id="5b493-105">DESCRIPTION</span></span>
<span data-ttu-id="5b493-106">**新的-AzureRmSqlDatabase** Cmdlet 會建立 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="5b493-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="5b493-107">您也可以將 *ElasticPoolName* 參數設定為現有彈性池，以建立彈性資料庫。</span><span class="sxs-lookup"><span data-stu-id="5b493-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="5b493-108">示例</span><span class="sxs-lookup"><span data-stu-id="5b493-108">EXAMPLES</span></span>

### <span data-ttu-id="5b493-109">範例1：在指定的伺服器上建立資料庫</span><span class="sxs-lookup"><span data-stu-id="5b493-109">Example 1: Create a database on a specified server</span></span>
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
Tags                          :
```

<span data-ttu-id="5b493-110">這個命令會在伺服器 Server01 上建立名為 Database01 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="5b493-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="5b493-111">範例2：在指定的伺服器上建立彈性資料庫</span><span class="sxs-lookup"><span data-stu-id="5b493-111">Example 2: Create an elastic database on a specified server</span></span>
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
Tags                          :
```

<span data-ttu-id="5b493-112">這個命令會在伺服器 Server01 上名為 ElasticPool01 的彈性池中建立名為 Database01 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="5b493-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="5b493-113">參數</span><span class="sxs-lookup"><span data-stu-id="5b493-113">PARAMETERS</span></span>

### <span data-ttu-id="5b493-114">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="5b493-114">-CatalogCollation</span></span>
<span data-ttu-id="5b493-115">指定 SQL 資料庫編目排序規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b493-115">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="5b493-116">-CollationName</span><span class="sxs-lookup"><span data-stu-id="5b493-116">-CollationName</span></span>
<span data-ttu-id="5b493-117">指定 SQL 資料庫排序規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b493-117">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="5b493-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5b493-118">-DatabaseName</span></span>
<span data-ttu-id="5b493-119">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b493-119">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="5b493-120">-Edition</span><span class="sxs-lookup"><span data-stu-id="5b493-120">-Edition</span></span>
<span data-ttu-id="5b493-121">指定要指派給資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="5b493-121">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="5b493-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5b493-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5b493-123">設置</span><span class="sxs-lookup"><span data-stu-id="5b493-123">Default</span></span>
- <span data-ttu-id="5b493-124">所有</span><span class="sxs-lookup"><span data-stu-id="5b493-124">None</span></span>
- <span data-ttu-id="5b493-125">佳</span><span class="sxs-lookup"><span data-stu-id="5b493-125">Premium</span></span>
- <span data-ttu-id="5b493-126">空白</span><span class="sxs-lookup"><span data-stu-id="5b493-126">Basic</span></span>
- <span data-ttu-id="5b493-127">標準</span><span class="sxs-lookup"><span data-stu-id="5b493-127">Standard</span></span>
- <span data-ttu-id="5b493-128">倉庫</span><span class="sxs-lookup"><span data-stu-id="5b493-128">DataWarehouse</span></span>
- <span data-ttu-id="5b493-129">空閒</span><span class="sxs-lookup"><span data-stu-id="5b493-129">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b493-130">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5b493-130">-ElasticPoolName</span></span>
<span data-ttu-id="5b493-131">指定要放入資料庫之彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b493-131">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="5b493-132">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="5b493-132">-MaxSizeBytes</span></span>
<span data-ttu-id="5b493-133">指定資料庫的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5b493-133">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="5b493-134">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="5b493-134">-ReadScale</span></span>
<span data-ttu-id="5b493-135">要指派給 Azure SQL 資料庫的 [讀取比例] 選項。 (啟用/停用) </span><span class="sxs-lookup"><span data-stu-id="5b493-135">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="5b493-136">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="5b493-136">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="5b493-137">指定要指派給資料庫之服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b493-137">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="5b493-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b493-138">-ResourceGroupName</span></span>
<span data-ttu-id="5b493-139">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b493-139">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5b493-140">-SampleName</span><span class="sxs-lookup"><span data-stu-id="5b493-140">-SampleName</span></span>
<span data-ttu-id="5b493-141">建立此資料庫時要套用之範例架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b493-141">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="5b493-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5b493-142">-ServerName</span></span>
<span data-ttu-id="5b493-143">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="5b493-143">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5b493-144">-標記</span><span class="sxs-lookup"><span data-stu-id="5b493-144">-Tags</span></span>
<span data-ttu-id="5b493-145">以這個 Cmdlet 所關聯的雜湊資料表形式，指定鍵值對的字典。</span><span class="sxs-lookup"><span data-stu-id="5b493-145">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="5b493-146">例如：</span><span class="sxs-lookup"><span data-stu-id="5b493-146">For example:</span></span>

<span data-ttu-id="5b493-147">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5b493-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5b493-148">-確認</span><span class="sxs-lookup"><span data-stu-id="5b493-148">-Confirm</span></span>
<span data-ttu-id="5b493-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5b493-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b493-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b493-150">-WhatIf</span></span>
<span data-ttu-id="5b493-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5b493-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b493-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b493-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b493-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b493-153">-DefaultProfile</span></span>
<span data-ttu-id="5b493-154">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b493-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b493-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b493-155">CommonParameters</span></span>
<span data-ttu-id="5b493-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b493-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b493-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5b493-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b493-158">輸入</span><span class="sxs-lookup"><span data-stu-id="5b493-158">INPUTS</span></span>

## <span data-ttu-id="5b493-159">輸出</span><span class="sxs-lookup"><span data-stu-id="5b493-159">OUTPUTS</span></span>

### <span data-ttu-id="5b493-160">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="5b493-160">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5b493-161">筆記</span><span class="sxs-lookup"><span data-stu-id="5b493-161">NOTES</span></span>

## <span data-ttu-id="5b493-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b493-162">RELATED LINKS</span></span>

[<span data-ttu-id="5b493-163">AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5b493-163">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="5b493-164">新-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5b493-164">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="5b493-165">新-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="5b493-165">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="5b493-166">移除-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5b493-166">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="5b493-167">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5b493-167">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="5b493-168">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5b493-168">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="5b493-169">暫停-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5b493-169">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="5b493-170">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="5b493-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
