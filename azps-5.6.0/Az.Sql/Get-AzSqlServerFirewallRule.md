---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: 21c942a9a67fd263dd251fd66224858292759096
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913717"
---
# <span data-ttu-id="5ab33-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5ab33-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="5ab33-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5ab33-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab33-103">獲得 SQL Database 伺服器的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="5ab33-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="5ab33-104">語法</span><span class="sxs-lookup"><span data-stu-id="5ab33-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ab33-105">描述</span><span class="sxs-lookup"><span data-stu-id="5ab33-105">DESCRIPTION</span></span>
<span data-ttu-id="5ab33-106">**Get-AzSqlServerFirewallRule** Cmdlet 會取得 Azure SQL Database 伺服器的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="5ab33-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="5ab33-107">如果您指定防火牆規則的名稱，此 Cmdlet 會獲得該特定防火牆規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="5ab33-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="5ab33-108">例子</span><span class="sxs-lookup"><span data-stu-id="5ab33-108">EXAMPLES</span></span>

### <span data-ttu-id="5ab33-109">範例 1：取得伺服器的所有規則</span><span class="sxs-lookup"><span data-stu-id="5ab33-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="5ab33-110">此命令會獲得伺服器名稱為 Server01 的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="5ab33-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="5ab33-111">範例 2：使用篩選取得伺服器的所有規則</span><span class="sxs-lookup"><span data-stu-id="5ab33-111">Example 2: Get all rules for a server using filtering</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule*"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : Rule01

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule02
```

<span data-ttu-id="5ab33-112">此命令會獲得伺服器名稱為「規則」的所有防火牆規則。伺服器名稱為「規則」。</span><span class="sxs-lookup"><span data-stu-id="5ab33-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="5ab33-113">參數</span><span class="sxs-lookup"><span data-stu-id="5ab33-113">PARAMETERS</span></span>

### <span data-ttu-id="5ab33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab33-114">-DefaultProfile</span></span>
<span data-ttu-id="5ab33-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="5ab33-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ab33-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="5ab33-116">-FirewallRuleName</span></span>
<span data-ttu-id="5ab33-117">指定防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ab33-117">Specifies the name of the firewall rule.</span></span>

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

### <span data-ttu-id="5ab33-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab33-118">-ResourceGroupName</span></span>
<span data-ttu-id="5ab33-119">指定指派給 SQL Server 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="5ab33-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="5ab33-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5ab33-120">-ServerName</span></span>
<span data-ttu-id="5ab33-121">指定 SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ab33-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="5ab33-122">-確認</span><span class="sxs-lookup"><span data-stu-id="5ab33-122">-Confirm</span></span>
<span data-ttu-id="5ab33-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5ab33-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab33-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab33-124">-WhatIf</span></span>
<span data-ttu-id="5ab33-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ab33-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ab33-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ab33-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab33-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab33-127">CommonParameters</span></span>
<span data-ttu-id="5ab33-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5ab33-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab33-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ab33-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab33-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5ab33-130">INPUTS</span></span>

### <span data-ttu-id="5ab33-131">System.String</span><span class="sxs-lookup"><span data-stu-id="5ab33-131">System.String</span></span>

## <span data-ttu-id="5ab33-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5ab33-132">OUTPUTS</span></span>

### <span data-ttu-id="5ab33-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="5ab33-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="5ab33-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5ab33-134">NOTES</span></span>

## <span data-ttu-id="5ab33-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ab33-135">RELATED LINKS</span></span>

[<span data-ttu-id="5ab33-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5ab33-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5ab33-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5ab33-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5ab33-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5ab33-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="5ab33-139">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="5ab33-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


