---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 83a68863b3dce71a091dc5de11377bade7bdc638
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273124"
---
# <span data-ttu-id="cf020-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cf020-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="cf020-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf020-102">SYNOPSIS</span></span>
<span data-ttu-id="cf020-103">從 SQL 資料庫伺服器刪除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="cf020-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="cf020-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf020-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf020-105">說明</span><span class="sxs-lookup"><span data-stu-id="cf020-105">DESCRIPTION</span></span>
<span data-ttu-id="cf020-106">**AzSqlServerFirewallRule** Cmdlet 會從指定的 Azure SQL Database 伺服器刪除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="cf020-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="cf020-107">示例</span><span class="sxs-lookup"><span data-stu-id="cf020-107">EXAMPLES</span></span>

### <span data-ttu-id="cf020-108">範例1：刪除規則</span><span class="sxs-lookup"><span data-stu-id="cf020-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="cf020-109">這個命令會刪除名為 Server01 的伺服器上名為 Rule01 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="cf020-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="cf020-110">參數</span><span class="sxs-lookup"><span data-stu-id="cf020-110">PARAMETERS</span></span>

### <span data-ttu-id="cf020-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf020-111">-DefaultProfile</span></span>
<span data-ttu-id="cf020-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cf020-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf020-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="cf020-113">-FirewallRuleName</span></span>
<span data-ttu-id="cf020-114">指定此 Cmdlet 刪除的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="cf020-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="cf020-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cf020-115">-Force</span></span>
<span data-ttu-id="cf020-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="cf020-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf020-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf020-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf020-118">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf020-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="cf020-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cf020-119">-ServerName</span></span>
<span data-ttu-id="cf020-120">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf020-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="cf020-121">-確認</span><span class="sxs-lookup"><span data-stu-id="cf020-121">-Confirm</span></span>
<span data-ttu-id="cf020-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf020-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf020-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf020-123">-WhatIf</span></span>
<span data-ttu-id="cf020-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf020-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf020-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf020-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf020-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf020-126">CommonParameters</span></span>
<span data-ttu-id="cf020-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf020-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf020-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cf020-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf020-129">輸入</span><span class="sxs-lookup"><span data-stu-id="cf020-129">INPUTS</span></span>

### <span data-ttu-id="cf020-130">System.object</span><span class="sxs-lookup"><span data-stu-id="cf020-130">System.String</span></span>

## <span data-ttu-id="cf020-131">輸出</span><span class="sxs-lookup"><span data-stu-id="cf020-131">OUTPUTS</span></span>

### <span data-ttu-id="cf020-132">AzureSqlServerFirewallRuleModel 中的 [FirewallRule]</span><span class="sxs-lookup"><span data-stu-id="cf020-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="cf020-133">筆記</span><span class="sxs-lookup"><span data-stu-id="cf020-133">NOTES</span></span>

## <span data-ttu-id="cf020-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf020-134">RELATED LINKS</span></span>

[<span data-ttu-id="cf020-135">AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cf020-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="cf020-136">新-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cf020-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="cf020-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cf020-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="cf020-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="cf020-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


