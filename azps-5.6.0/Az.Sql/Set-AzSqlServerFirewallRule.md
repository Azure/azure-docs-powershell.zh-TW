---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 2365cb4f6dedeb0620a2bdb1c1549eb0cd25d0c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912309"
---
# <span data-ttu-id="86b22-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="86b22-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="86b22-102">簡介</span><span class="sxs-lookup"><span data-stu-id="86b22-102">SYNOPSIS</span></span>
<span data-ttu-id="86b22-103">修改 Azure SQL Database Server 中的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="86b22-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="86b22-104">語法</span><span class="sxs-lookup"><span data-stu-id="86b22-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86b22-105">描述</span><span class="sxs-lookup"><span data-stu-id="86b22-105">DESCRIPTION</span></span>
<span data-ttu-id="86b22-106">**Set-AzSqlServerFirewallRule** Cmdlet 會修改 Azure SQL Database 伺服器中的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="86b22-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="86b22-107">例子</span><span class="sxs-lookup"><span data-stu-id="86b22-107">EXAMPLES</span></span>

### <span data-ttu-id="86b22-108">範例 1：修改防火牆規則</span><span class="sxs-lookup"><span data-stu-id="86b22-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="86b22-109">此命令會修改伺服器上名為 Rule01 的防火牆規則，該規則名為 Server01。</span><span class="sxs-lookup"><span data-stu-id="86b22-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="86b22-110">該命令會修改開始與結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="86b22-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="86b22-111">參數</span><span class="sxs-lookup"><span data-stu-id="86b22-111">PARAMETERS</span></span>

### <span data-ttu-id="86b22-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86b22-112">-DefaultProfile</span></span>
<span data-ttu-id="86b22-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="86b22-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86b22-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="86b22-114">-EndIpAddress</span></span>
<span data-ttu-id="86b22-115">指定此規則的 IP 位址範圍的結束值。</span><span class="sxs-lookup"><span data-stu-id="86b22-115">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86b22-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="86b22-116">-FirewallRuleName</span></span>
<span data-ttu-id="86b22-117">指定此 Cmdlet 修改的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="86b22-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="86b22-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86b22-118">-ResourceGroupName</span></span>
<span data-ttu-id="86b22-119">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="86b22-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="86b22-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="86b22-120">-ServerName</span></span>
<span data-ttu-id="86b22-121">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="86b22-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="86b22-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="86b22-122">-StartIpAddress</span></span>
<span data-ttu-id="86b22-123">指定防火牆規則的 IP 位址範圍的起始值。</span><span class="sxs-lookup"><span data-stu-id="86b22-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86b22-124">-確認</span><span class="sxs-lookup"><span data-stu-id="86b22-124">-Confirm</span></span>
<span data-ttu-id="86b22-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="86b22-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86b22-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86b22-126">-WhatIf</span></span>
<span data-ttu-id="86b22-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="86b22-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86b22-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="86b22-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86b22-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86b22-129">CommonParameters</span></span>
<span data-ttu-id="86b22-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="86b22-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86b22-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86b22-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86b22-132">輸入</span><span class="sxs-lookup"><span data-stu-id="86b22-132">INPUTS</span></span>

### <span data-ttu-id="86b22-133">System.String</span><span class="sxs-lookup"><span data-stu-id="86b22-133">System.String</span></span>

## <span data-ttu-id="86b22-134">輸出</span><span class="sxs-lookup"><span data-stu-id="86b22-134">OUTPUTS</span></span>

### <span data-ttu-id="86b22-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="86b22-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="86b22-136">筆記</span><span class="sxs-lookup"><span data-stu-id="86b22-136">NOTES</span></span>

## <span data-ttu-id="86b22-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="86b22-137">RELATED LINKS</span></span>

[<span data-ttu-id="86b22-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="86b22-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="86b22-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="86b22-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="86b22-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="86b22-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="86b22-141">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="86b22-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


