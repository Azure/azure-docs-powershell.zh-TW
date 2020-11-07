---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: fb8769dcd8f989ad0715a799ce397eb0fe594126
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792484"
---
# <span data-ttu-id="ef7b6-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ef7b6-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="ef7b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef7b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7b6-103">傳回 SQL 資料庫伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ef7b6-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="ef7b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef7b6-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef7b6-105">說明</span><span class="sxs-lookup"><span data-stu-id="ef7b6-105">DESCRIPTION</span></span>
<span data-ttu-id="ef7b6-106">**AzSqlServer** Cmdlet 會傳回一或多個 Azure SQL 資料庫伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ef7b6-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="ef7b6-107">指定伺服器的名稱，只查看該伺服器的資訊。</span><span class="sxs-lookup"><span data-stu-id="ef7b6-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="ef7b6-108">示例</span><span class="sxs-lookup"><span data-stu-id="ef7b6-108">EXAMPLES</span></span>

### <span data-ttu-id="ef7b6-109">範例1：取得指派給資源群組的所有 SQL Server 實例</span><span class="sxs-lookup"><span data-stu-id="ef7b6-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="ef7b6-110">這個命令會取得指派給資源群組 ResourceGroup01 的所有 Azure SQL 資料庫伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ef7b6-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="ef7b6-111">範例2：取得 Azure SQL 資料庫伺服器的相關資訊</span><span class="sxs-lookup"><span data-stu-id="ef7b6-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="ef7b6-112">這個命令會取得名為 Server01 的 Azure SQL Database 伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ef7b6-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="ef7b6-113">範例3：在訂閱中取得 SQL Server 的所有實例</span><span class="sxs-lookup"><span data-stu-id="ef7b6-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server03.database.windows.net
```

<span data-ttu-id="ef7b6-114">這個命令會取得目前訂閱中所有 Azure SQL Database 伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ef7b6-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="ef7b6-115">範例4：使用篩選來取得指派給資源群組的所有 SQL Server 實例</span><span class="sxs-lookup"><span data-stu-id="ef7b6-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "server*"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="ef7b6-116">這個命令會取得指派給以「server」開頭之資源群組 ResourceGroup01 的所有 Azure SQL 資料庫伺服器資訊。</span><span class="sxs-lookup"><span data-stu-id="ef7b6-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="ef7b6-117">參數</span><span class="sxs-lookup"><span data-stu-id="ef7b6-117">PARAMETERS</span></span>

### <span data-ttu-id="ef7b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7b6-118">-DefaultProfile</span></span>
<span data-ttu-id="ef7b6-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ef7b6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef7b6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef7b6-120">-ResourceGroupName</span></span>
<span data-ttu-id="ef7b6-121">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef7b6-121">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ef7b6-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ef7b6-122">-ServerName</span></span>
<span data-ttu-id="ef7b6-123">指定此 Cmdlet 取得的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ef7b6-123">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ef7b6-124">-確認</span><span class="sxs-lookup"><span data-stu-id="ef7b6-124">-Confirm</span></span>
<span data-ttu-id="ef7b6-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef7b6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef7b6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef7b6-126">-WhatIf</span></span>
<span data-ttu-id="ef7b6-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef7b6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef7b6-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef7b6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef7b6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7b6-129">CommonParameters</span></span>
<span data-ttu-id="ef7b6-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef7b6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7b6-131">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ef7b6-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7b6-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ef7b6-132">INPUTS</span></span>

### <span data-ttu-id="ef7b6-133">System.object</span><span class="sxs-lookup"><span data-stu-id="ef7b6-133">System.String</span></span>

## <span data-ttu-id="ef7b6-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ef7b6-134">OUTPUTS</span></span>

### <span data-ttu-id="ef7b6-135">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="ef7b6-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="ef7b6-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ef7b6-136">NOTES</span></span>

## <span data-ttu-id="ef7b6-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef7b6-137">RELATED LINKS</span></span>

[<span data-ttu-id="ef7b6-138">新-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ef7b6-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="ef7b6-139">移除-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ef7b6-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="ef7b6-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ef7b6-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="ef7b6-141">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ef7b6-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


