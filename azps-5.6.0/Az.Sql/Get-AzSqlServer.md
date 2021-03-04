---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: 26a1e7dab44f71aa14990fe4e46a2f79a24e9067
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914269"
---
# <span data-ttu-id="05a5e-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="05a5e-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="05a5e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="05a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="05a5e-103">會返回 SQL Database 伺服器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="05a5e-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="05a5e-104">語法</span><span class="sxs-lookup"><span data-stu-id="05a5e-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05a5e-105">描述</span><span class="sxs-lookup"><span data-stu-id="05a5e-105">DESCRIPTION</span></span>
<span data-ttu-id="05a5e-106">**Get-AzSqlServer** Cmdlet 會返回一或多個 Azure SQL 資料庫伺服器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="05a5e-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="05a5e-107">指定伺服器名稱，只查看該伺服器的資訊。</span><span class="sxs-lookup"><span data-stu-id="05a5e-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="05a5e-108">例子</span><span class="sxs-lookup"><span data-stu-id="05a5e-108">EXAMPLES</span></span>

### <span data-ttu-id="05a5e-109">範例 1：取得指派給資源群組之 SQL Server 的所有實例</span><span class="sxs-lookup"><span data-stu-id="05a5e-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
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

<span data-ttu-id="05a5e-110">此命令會獲得指派給資源群組 ResourceGroup01 的所有 Azure SQL 資料庫伺服器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="05a5e-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="05a5e-111">範例 2：取得 Azure SQL Database 伺服器相關資訊</span><span class="sxs-lookup"><span data-stu-id="05a5e-111">Example 2: Get information about an Azure SQL Database server</span></span>
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

<span data-ttu-id="05a5e-112">此命令會獲得名稱為 Server01 的 Azure SQL Database 伺服器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="05a5e-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="05a5e-113">範例 3：取得訂閱中 SQL Server 的所有實例</span><span class="sxs-lookup"><span data-stu-id="05a5e-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
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

<span data-ttu-id="05a5e-114">此命令會獲得目前訂閱中所有 Azure SQL Database 伺服器的資訊。</span><span class="sxs-lookup"><span data-stu-id="05a5e-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="05a5e-115">範例 4：使用篩選將 SQL Server 的所有實例指派給資源群組</span><span class="sxs-lookup"><span data-stu-id="05a5e-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
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

<span data-ttu-id="05a5e-116">此命令會獲得指派給以「伺服器」為起始資源群組 ResourceGroup01 之所有 Azure SQL 資料庫伺服器的資訊。</span><span class="sxs-lookup"><span data-stu-id="05a5e-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="05a5e-117">參數</span><span class="sxs-lookup"><span data-stu-id="05a5e-117">PARAMETERS</span></span>

### <span data-ttu-id="05a5e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a5e-118">-DefaultProfile</span></span>
<span data-ttu-id="05a5e-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="05a5e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05a5e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05a5e-120">-ResourceGroupName</span></span>
<span data-ttu-id="05a5e-121">指定指派伺服器之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="05a5e-121">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a5e-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="05a5e-122">-ServerName</span></span>
<span data-ttu-id="05a5e-123">指定此 Cmdlet 所獲得伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="05a5e-123">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05a5e-124">-確認</span><span class="sxs-lookup"><span data-stu-id="05a5e-124">-Confirm</span></span>
<span data-ttu-id="05a5e-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="05a5e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05a5e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05a5e-126">-WhatIf</span></span>
<span data-ttu-id="05a5e-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="05a5e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05a5e-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05a5e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05a5e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a5e-129">CommonParameters</span></span>
<span data-ttu-id="05a5e-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="05a5e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a5e-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05a5e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a5e-132">輸入</span><span class="sxs-lookup"><span data-stu-id="05a5e-132">INPUTS</span></span>

### <span data-ttu-id="05a5e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="05a5e-133">System.String</span></span>

## <span data-ttu-id="05a5e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="05a5e-134">OUTPUTS</span></span>

### <span data-ttu-id="05a5e-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="05a5e-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="05a5e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="05a5e-136">NOTES</span></span>

## <span data-ttu-id="05a5e-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="05a5e-137">RELATED LINKS</span></span>

[<span data-ttu-id="05a5e-138">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="05a5e-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="05a5e-139">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="05a5e-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="05a5e-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="05a5e-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="05a5e-141">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="05a5e-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


