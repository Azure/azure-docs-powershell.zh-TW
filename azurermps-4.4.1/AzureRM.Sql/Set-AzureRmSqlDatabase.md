---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: 3d36c94ebcc1b733559f9fb4075fb20e4ec67144
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624123"
---
# <span data-ttu-id="098d6-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="098d6-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="098d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="098d6-102">SYNOPSIS</span></span>
<span data-ttu-id="098d6-103">為資料庫設定屬性，或將現有資料庫移至彈性池中。</span><span class="sxs-lookup"><span data-stu-id="098d6-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="098d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="098d6-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="098d6-105">說明</span><span class="sxs-lookup"><span data-stu-id="098d6-105">DESCRIPTION</span></span>
<span data-ttu-id="098d6-106">**AzureRmSqlDatabase** Cmdlet 會設定 Azure SQL 資料庫的屬性。</span><span class="sxs-lookup"><span data-stu-id="098d6-106">The **Set-AzureRmSqlDatabase** cmdlet sets properties for an Azure SQL database.</span></span>
<span data-ttu-id="098d6-107">此外，您也可以指定 *ElasticPoolName* 參數，將資料庫移至彈性池。</span><span class="sxs-lookup"><span data-stu-id="098d6-107">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span>
<span data-ttu-id="098d6-108">如果資料庫已在彈性池中，您可以使用 *RequestedServiceObjectiveName* 參數來指派效能等級。</span><span class="sxs-lookup"><span data-stu-id="098d6-108">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to assign a performance level.</span></span>

## <span data-ttu-id="098d6-109">示例</span><span class="sxs-lookup"><span data-stu-id="098d6-109">EXAMPLES</span></span>

### <span data-ttu-id="098d6-110">範例1：將資料庫更新為標準的 S2 資料庫</span><span class="sxs-lookup"><span data-stu-id="098d6-110">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
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
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="098d6-111">這個命令會將一個名為 Database01 的資料庫，更新為伺服器上名為 Server01 的標準 S2 資料庫。</span><span class="sxs-lookup"><span data-stu-id="098d6-111">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="098d6-112">範例2：將資料庫新增至彈性池</span><span class="sxs-lookup"><span data-stu-id="098d6-112">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
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
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="098d6-113">這個命令會將一個名為 Database01 的資料庫，新增到名為 Server01 的伺服器上名為 ElasticPool01 的彈性池。</span><span class="sxs-lookup"><span data-stu-id="098d6-113">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

## <span data-ttu-id="098d6-114">參數</span><span class="sxs-lookup"><span data-stu-id="098d6-114">PARAMETERS</span></span>

### <span data-ttu-id="098d6-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="098d6-115">-DatabaseName</span></span>
<span data-ttu-id="098d6-116">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="098d6-116">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="098d6-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="098d6-117">-Edition</span></span>
<span data-ttu-id="098d6-118">指定資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="098d6-118">Specifies the edition for the database.</span></span>
<span data-ttu-id="098d6-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="098d6-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="098d6-120">所有</span><span class="sxs-lookup"><span data-stu-id="098d6-120">None</span></span>
- <span data-ttu-id="098d6-121">佳</span><span class="sxs-lookup"><span data-stu-id="098d6-121">Premium</span></span>
- <span data-ttu-id="098d6-122">空白</span><span class="sxs-lookup"><span data-stu-id="098d6-122">Basic</span></span>
- <span data-ttu-id="098d6-123">標準</span><span class="sxs-lookup"><span data-stu-id="098d6-123">Standard</span></span>
- <span data-ttu-id="098d6-124">倉庫</span><span class="sxs-lookup"><span data-stu-id="098d6-124">DataWarehouse</span></span>
- <span data-ttu-id="098d6-125">空閒</span><span class="sxs-lookup"><span data-stu-id="098d6-125">Free</span></span>

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

### <span data-ttu-id="098d6-126">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="098d6-126">-ElasticPoolName</span></span>
<span data-ttu-id="098d6-127">指定要在其中移動資料庫的彈性池名稱。</span><span class="sxs-lookup"><span data-stu-id="098d6-127">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="098d6-128">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="098d6-128">-MaxSizeBytes</span></span>
<span data-ttu-id="098d6-129">指定資料庫的新的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="098d6-129">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="098d6-130">您可以指定此參數或 *MaxSizeGB* 。</span><span class="sxs-lookup"><span data-stu-id="098d6-130">You can specify either this parameter or *MaxSizeGB*.</span></span>
<span data-ttu-id="098d6-131">請參閱每個版本的 *MaxSizeGB* 參數（針對可接受的值）。</span><span class="sxs-lookup"><span data-stu-id="098d6-131">See the *MaxSizeGB* parameter for acceptable values per edition.</span></span>

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

### <span data-ttu-id="098d6-132">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="098d6-132">-ReadScale</span></span>
<span data-ttu-id="098d6-133">要指派給 Azure SQL 資料庫的 [讀取比例] 選項。 (啟用/停用) </span><span class="sxs-lookup"><span data-stu-id="098d6-133">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="098d6-134">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="098d6-134">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="098d6-135">指定要指派給資料庫之服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="098d6-135">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="098d6-136">如需服務目標的相關資訊，請參閱 Microsoft 開發人員網路文件庫中的 [AZURE SQL 資料庫服務層級和效能層級](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="098d6-136">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="098d6-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="098d6-137">-ResourceGroupName</span></span>
<span data-ttu-id="098d6-138">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="098d6-138">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="098d6-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="098d6-139">-ServerName</span></span>
<span data-ttu-id="098d6-140">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="098d6-140">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="098d6-141">-標記</span><span class="sxs-lookup"><span data-stu-id="098d6-141">-Tags</span></span>
<span data-ttu-id="098d6-142">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="098d6-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="098d6-143">例如：</span><span class="sxs-lookup"><span data-stu-id="098d6-143">For example:</span></span>

<span data-ttu-id="098d6-144">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="098d6-144">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="098d6-145">-確認</span><span class="sxs-lookup"><span data-stu-id="098d6-145">-Confirm</span></span>
<span data-ttu-id="098d6-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="098d6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="098d6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="098d6-147">-WhatIf</span></span>
<span data-ttu-id="098d6-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="098d6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="098d6-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="098d6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="098d6-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098d6-150">-DefaultProfile</span></span>
<span data-ttu-id="098d6-151">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="098d6-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="098d6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098d6-152">CommonParameters</span></span>
<span data-ttu-id="098d6-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="098d6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098d6-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="098d6-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098d6-155">輸入</span><span class="sxs-lookup"><span data-stu-id="098d6-155">INPUTS</span></span>

## <span data-ttu-id="098d6-156">輸出</span><span class="sxs-lookup"><span data-stu-id="098d6-156">OUTPUTS</span></span>

### <span data-ttu-id="098d6-157">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="098d6-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="098d6-158">筆記</span><span class="sxs-lookup"><span data-stu-id="098d6-158">NOTES</span></span>

## <span data-ttu-id="098d6-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="098d6-159">RELATED LINKS</span></span>

[<span data-ttu-id="098d6-160">AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="098d6-160">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="098d6-161">新-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="098d6-161">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="098d6-162">移除-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="098d6-162">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="098d6-163">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="098d6-163">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="098d6-164">暫停-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="098d6-164">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="098d6-165">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="098d6-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
