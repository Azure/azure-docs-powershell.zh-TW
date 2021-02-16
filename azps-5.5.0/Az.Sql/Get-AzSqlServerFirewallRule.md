---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: c2157521614375bbdeb06aac9a62320ec1e08c70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139767"
---
# <span data-ttu-id="f755b-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f755b-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="f755b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f755b-102">SYNOPSIS</span></span>
<span data-ttu-id="f755b-103">取得 SQL 資料庫伺服器的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="f755b-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="f755b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f755b-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f755b-105">說明</span><span class="sxs-lookup"><span data-stu-id="f755b-105">DESCRIPTION</span></span>
<span data-ttu-id="f755b-106">**AzSqlServerFirewallRule** Cmdlet 會取得 Azure SQL 資料庫伺服器的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="f755b-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="f755b-107">如果您指定防火牆規則的名稱，此 Cmdlet 會取得該特定防火牆規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f755b-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="f755b-108">示例</span><span class="sxs-lookup"><span data-stu-id="f755b-108">EXAMPLES</span></span>

### <span data-ttu-id="f755b-109">範例1：取得伺服器的所有規則</span><span class="sxs-lookup"><span data-stu-id="f755b-109">Example 1: Get all rules for a server</span></span>
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

<span data-ttu-id="f755b-110">這個命令會取得伺服器名為 Server01 的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="f755b-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="f755b-111">範例2：使用篩選取得伺服器的所有規則</span><span class="sxs-lookup"><span data-stu-id="f755b-111">Example 2: Get all rules for a server using filtering</span></span>
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

<span data-ttu-id="f755b-112">這個命令會取得名為 Server01 且以 "Rule" 為開頭的伺服器所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="f755b-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="f755b-113">參數</span><span class="sxs-lookup"><span data-stu-id="f755b-113">PARAMETERS</span></span>

### <span data-ttu-id="f755b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f755b-114">-DefaultProfile</span></span>
<span data-ttu-id="f755b-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f755b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f755b-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="f755b-116">-FirewallRuleName</span></span>
<span data-ttu-id="f755b-117">指定防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f755b-117">Specifies the name of the firewall rule.</span></span>

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

### <span data-ttu-id="f755b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f755b-118">-ResourceGroupName</span></span>
<span data-ttu-id="f755b-119">指定指派 SQL Server 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f755b-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="f755b-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f755b-120">-ServerName</span></span>
<span data-ttu-id="f755b-121">指定 SQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f755b-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="f755b-122">-確認</span><span class="sxs-lookup"><span data-stu-id="f755b-122">-Confirm</span></span>
<span data-ttu-id="f755b-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f755b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f755b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f755b-124">-WhatIf</span></span>
<span data-ttu-id="f755b-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f755b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f755b-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f755b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f755b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f755b-127">CommonParameters</span></span>
<span data-ttu-id="f755b-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f755b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f755b-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f755b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f755b-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f755b-130">INPUTS</span></span>

### <span data-ttu-id="f755b-131">System.object</span><span class="sxs-lookup"><span data-stu-id="f755b-131">System.String</span></span>

## <span data-ttu-id="f755b-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f755b-132">OUTPUTS</span></span>

### <span data-ttu-id="f755b-133">AzureSqlServerFirewallRuleModel 中的 [FirewallRule]</span><span class="sxs-lookup"><span data-stu-id="f755b-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="f755b-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f755b-134">NOTES</span></span>

## <span data-ttu-id="f755b-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f755b-135">RELATED LINKS</span></span>

[<span data-ttu-id="f755b-136">新-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f755b-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f755b-137">移除-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f755b-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f755b-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f755b-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f755b-139">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="f755b-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


