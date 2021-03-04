---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
ms.openlocfilehash: 24e6d0f96114f6843b5af48fafe6d58cc7b49126
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912550"
---
# <span data-ttu-id="eaacf-101">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eaacf-101">Get-AzSqlDatabase</span></span>

## <span data-ttu-id="eaacf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eaacf-102">SYNOPSIS</span></span>
<span data-ttu-id="eaacf-103">獲得一或多個資料庫。</span><span class="sxs-lookup"><span data-stu-id="eaacf-103">Gets one or more databases.</span></span>

## <span data-ttu-id="eaacf-104">語法</span><span class="sxs-lookup"><span data-stu-id="eaacf-104">SYNTAX</span></span>

```
Get-AzSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaacf-105">描述</span><span class="sxs-lookup"><span data-stu-id="eaacf-105">DESCRIPTION</span></span>
<span data-ttu-id="eaacf-106">**Get-AzSqlDatabase** Cmdlet 會從 Azure SQL Database Server 取得一或多個 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="eaacf-106">The **Get-AzSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="eaacf-107">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eaacf-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="eaacf-108">例子</span><span class="sxs-lookup"><span data-stu-id="eaacf-108">EXAMPLES</span></span>

### <span data-ttu-id="eaacf-109">範例 1：在伺服器上取得所有資料庫</span><span class="sxs-lookup"><span data-stu-id="eaacf-109">Example 1: Get all databases on a server</span></span>
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

<span data-ttu-id="eaacf-110">此命令會在伺服器上名為 server01 的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="eaacf-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="eaacf-111">範例 2：在伺服器上按名稱取得資料庫</span><span class="sxs-lookup"><span data-stu-id="eaacf-111">Example 2: Get a database by name on a server</span></span>
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

<span data-ttu-id="eaacf-112">此命令會從伺服器名稱為 Server01 的資料庫命名為 Database02。</span><span class="sxs-lookup"><span data-stu-id="eaacf-112">This command gets a database named Database02 from a server named Server01.</span></span>

### <span data-ttu-id="eaacf-113">範例 3：使用篩選在伺服器上取得所有資料庫</span><span class="sxs-lookup"><span data-stu-id="eaacf-113">Example 3: Get all databases on a server using filtering</span></span>
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

<span data-ttu-id="eaacf-114">此命令會在伺服器上以「資料庫」做為開始，而伺服器名稱為 server01 的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="eaacf-114">This command gets all databases on the server named server01 that start with "database".</span></span>

## <span data-ttu-id="eaacf-115">參數</span><span class="sxs-lookup"><span data-stu-id="eaacf-115">PARAMETERS</span></span>

### <span data-ttu-id="eaacf-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eaacf-116">-DatabaseName</span></span>
<span data-ttu-id="eaacf-117">指定要取取的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="eaacf-117">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaacf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaacf-118">-DefaultProfile</span></span>
<span data-ttu-id="eaacf-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="eaacf-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eaacf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaacf-120">-ResourceGroupName</span></span>
<span data-ttu-id="eaacf-121">指定指派資料庫伺服器之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eaacf-121">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="eaacf-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eaacf-122">-ServerName</span></span>
<span data-ttu-id="eaacf-123">指定指派資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="eaacf-123">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="eaacf-124">-確認</span><span class="sxs-lookup"><span data-stu-id="eaacf-124">-Confirm</span></span>
<span data-ttu-id="eaacf-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eaacf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaacf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaacf-126">-WhatIf</span></span>
<span data-ttu-id="eaacf-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eaacf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaacf-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eaacf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaacf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaacf-129">CommonParameters</span></span>
<span data-ttu-id="eaacf-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eaacf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaacf-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eaacf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaacf-132">輸入</span><span class="sxs-lookup"><span data-stu-id="eaacf-132">INPUTS</span></span>

### <span data-ttu-id="eaacf-133">System.String</span><span class="sxs-lookup"><span data-stu-id="eaacf-133">System.String</span></span>

## <span data-ttu-id="eaacf-134">輸出</span><span class="sxs-lookup"><span data-stu-id="eaacf-134">OUTPUTS</span></span>

### <span data-ttu-id="eaacf-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="eaacf-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="eaacf-136">筆記</span><span class="sxs-lookup"><span data-stu-id="eaacf-136">NOTES</span></span>

## <span data-ttu-id="eaacf-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="eaacf-137">RELATED LINKS</span></span>

[<span data-ttu-id="eaacf-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eaacf-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="eaacf-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eaacf-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="eaacf-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eaacf-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="eaacf-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eaacf-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="eaacf-142">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eaacf-142">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)


