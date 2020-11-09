---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 4dea3f8bf91bb4b9c0478c281e6ca9366c49744c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285895"
---
# <span data-ttu-id="77079-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="77079-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="77079-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77079-102">SYNOPSIS</span></span>
<span data-ttu-id="77079-103">修改 Azure SQL 資料庫伺服器中的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="77079-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="77079-104">句法</span><span class="sxs-lookup"><span data-stu-id="77079-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77079-105">說明</span><span class="sxs-lookup"><span data-stu-id="77079-105">DESCRIPTION</span></span>
<span data-ttu-id="77079-106">**AzSqlServerFirewallRule** Cmdlet 會修改 Azure SQL 資料庫伺服器中的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="77079-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="77079-107">示例</span><span class="sxs-lookup"><span data-stu-id="77079-107">EXAMPLES</span></span>

### <span data-ttu-id="77079-108">範例1：修改防火牆規則</span><span class="sxs-lookup"><span data-stu-id="77079-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="77079-109">這個命令會修改名為 Server01 的伺服器上名為 Rule01 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="77079-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="77079-110">此命令會修改開始和結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="77079-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="77079-111">參數</span><span class="sxs-lookup"><span data-stu-id="77079-111">PARAMETERS</span></span>

### <span data-ttu-id="77079-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77079-112">-DefaultProfile</span></span>
<span data-ttu-id="77079-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="77079-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77079-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="77079-114">-EndIpAddress</span></span>
<span data-ttu-id="77079-115">指定此規則 IP 位址範圍的結束值。</span><span class="sxs-lookup"><span data-stu-id="77079-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="77079-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="77079-116">-FirewallRuleName</span></span>
<span data-ttu-id="77079-117">指定此 Cmdlet 修改的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="77079-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="77079-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77079-118">-ResourceGroupName</span></span>
<span data-ttu-id="77079-119">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="77079-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="77079-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="77079-120">-ServerName</span></span>
<span data-ttu-id="77079-121">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="77079-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="77079-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="77079-122">-StartIpAddress</span></span>
<span data-ttu-id="77079-123">指定防火牆規則 IP 位址範圍的起始值。</span><span class="sxs-lookup"><span data-stu-id="77079-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="77079-124">-確認</span><span class="sxs-lookup"><span data-stu-id="77079-124">-Confirm</span></span>
<span data-ttu-id="77079-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="77079-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77079-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77079-126">-WhatIf</span></span>
<span data-ttu-id="77079-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="77079-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77079-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77079-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77079-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77079-129">CommonParameters</span></span>
<span data-ttu-id="77079-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77079-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77079-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="77079-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77079-132">輸入</span><span class="sxs-lookup"><span data-stu-id="77079-132">INPUTS</span></span>

### <span data-ttu-id="77079-133">System.object</span><span class="sxs-lookup"><span data-stu-id="77079-133">System.String</span></span>

## <span data-ttu-id="77079-134">輸出</span><span class="sxs-lookup"><span data-stu-id="77079-134">OUTPUTS</span></span>

### <span data-ttu-id="77079-135">AzureSqlServerFirewallRuleModel 中的 [FirewallRule]</span><span class="sxs-lookup"><span data-stu-id="77079-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="77079-136">筆記</span><span class="sxs-lookup"><span data-stu-id="77079-136">NOTES</span></span>

## <span data-ttu-id="77079-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="77079-137">RELATED LINKS</span></span>

[<span data-ttu-id="77079-138">AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="77079-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="77079-139">新-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="77079-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="77079-140">移除-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="77079-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="77079-141">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="77079-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


