---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
ms.openlocfilehash: bcaa1c5d57fea979e227fa8890cac6ac0b3f8a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792385"
---
# <span data-ttu-id="2c2a2-101">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2c2a2-101">Get-AzSqlDatabase</span></span>

## <span data-ttu-id="2c2a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="2c2a2-103">取得一或多個資料庫。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-103">Gets one or more databases.</span></span>

## <span data-ttu-id="2c2a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c2a2-104">SYNTAX</span></span>

```
Get-AzSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c2a2-105">說明</span><span class="sxs-lookup"><span data-stu-id="2c2a2-105">DESCRIPTION</span></span>
<span data-ttu-id="2c2a2-106">**AzSqlDatabase** Cmdlet 會從 Azure Sql Database Server 取得一個或多個 azure sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-106">The **Get-AzSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="2c2a2-107">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2c2a2-108">示例</span><span class="sxs-lookup"><span data-stu-id="2c2a2-108">EXAMPLES</span></span>

### <span data-ttu-id="2c2a2-109">範例1：取得伺服器上的所有資料庫</span><span class="sxs-lookup"><span data-stu-id="2c2a2-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : master
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
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

<span data-ttu-id="2c2a2-110">這個命令會取得伺服器上名為 server01 的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="2c2a2-111">範例2：在伺服器上依名稱取得資料庫</span><span class="sxs-lookup"><span data-stu-id="2c2a2-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
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

<span data-ttu-id="2c2a2-112">這個命令會從名為 Server01 的伺服器中取得名為 Database02 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-112">This command gets a database named Database02 from a server named Server01.</span></span>

### <span data-ttu-id="2c2a2-113">範例3：使用篩選取得伺服器上的所有資料庫</span><span class="sxs-lookup"><span data-stu-id="2c2a2-113">Example 3: Get all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database*"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
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

<span data-ttu-id="2c2a2-114">這個命令會取得伺服器上名為 server01 的所有資料庫，其開頭為「database」。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-114">This command gets all databases on the server named server01 that start with "database".</span></span>

## <span data-ttu-id="2c2a2-115">參數</span><span class="sxs-lookup"><span data-stu-id="2c2a2-115">PARAMETERS</span></span>

### <span data-ttu-id="2c2a2-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2c2a2-116">-DatabaseName</span></span>
<span data-ttu-id="2c2a2-117">指定要檢索之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-117">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="2c2a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c2a2-118">-DefaultProfile</span></span>
<span data-ttu-id="2c2a2-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2c2a2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c2a2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c2a2-120">-ResourceGroupName</span></span>
<span data-ttu-id="2c2a2-121">指定指派資料庫伺服器的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-121">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="2c2a2-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2c2a2-122">-ServerName</span></span>
<span data-ttu-id="2c2a2-123">指定指派給資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-123">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="2c2a2-124">-確認</span><span class="sxs-lookup"><span data-stu-id="2c2a2-124">-Confirm</span></span>
<span data-ttu-id="2c2a2-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c2a2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c2a2-126">-WhatIf</span></span>
<span data-ttu-id="2c2a2-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c2a2-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c2a2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c2a2-129">CommonParameters</span></span>
<span data-ttu-id="2c2a2-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c2a2-131">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c2a2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2c2a2-132">INPUTS</span></span>

### <span data-ttu-id="2c2a2-133">System.object</span><span class="sxs-lookup"><span data-stu-id="2c2a2-133">System.String</span></span>

## <span data-ttu-id="2c2a2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2c2a2-134">OUTPUTS</span></span>

### <span data-ttu-id="2c2a2-135">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="2c2a2-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2c2a2-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2c2a2-136">NOTES</span></span>

## <span data-ttu-id="2c2a2-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c2a2-137">RELATED LINKS</span></span>

[<span data-ttu-id="2c2a2-138">新-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2c2a2-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="2c2a2-139">移除-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2c2a2-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="2c2a2-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2c2a2-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="2c2a2-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2c2a2-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="2c2a2-142">暫停-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2c2a2-142">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)


