---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 0b76faf383e8cd3c70d6ff1e7e38de367850ac8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905761"
---
# <span data-ttu-id="61b63-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="61b63-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="61b63-102">簡介</span><span class="sxs-lookup"><span data-stu-id="61b63-102">SYNOPSIS</span></span>
<span data-ttu-id="61b63-103">從 SQL Database 伺服器刪除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="61b63-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="61b63-104">語法</span><span class="sxs-lookup"><span data-stu-id="61b63-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61b63-105">描述</span><span class="sxs-lookup"><span data-stu-id="61b63-105">DESCRIPTION</span></span>
<span data-ttu-id="61b63-106">**Remove-AzSqlServerFirewallRule** Cmdlet 會從指定的 Azure SQL Database 伺服器刪除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="61b63-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="61b63-107">例子</span><span class="sxs-lookup"><span data-stu-id="61b63-107">EXAMPLES</span></span>

### <span data-ttu-id="61b63-108">範例 1：刪除規則</span><span class="sxs-lookup"><span data-stu-id="61b63-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="61b63-109">此命令會刪除伺服器上名為 Rule01 的防火牆規則，該防火牆規則名為 Server01。</span><span class="sxs-lookup"><span data-stu-id="61b63-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="61b63-110">參數</span><span class="sxs-lookup"><span data-stu-id="61b63-110">PARAMETERS</span></span>

### <span data-ttu-id="61b63-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61b63-111">-DefaultProfile</span></span>
<span data-ttu-id="61b63-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="61b63-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61b63-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="61b63-113">-FirewallRuleName</span></span>
<span data-ttu-id="61b63-114">指定此 Cmdlet 刪除的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="61b63-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="61b63-115">-強制</span><span class="sxs-lookup"><span data-stu-id="61b63-115">-Force</span></span>
<span data-ttu-id="61b63-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="61b63-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="61b63-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61b63-117">-ResourceGroupName</span></span>
<span data-ttu-id="61b63-118">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="61b63-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="61b63-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="61b63-119">-ServerName</span></span>
<span data-ttu-id="61b63-120">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="61b63-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="61b63-121">-確認</span><span class="sxs-lookup"><span data-stu-id="61b63-121">-Confirm</span></span>
<span data-ttu-id="61b63-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="61b63-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61b63-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61b63-123">-WhatIf</span></span>
<span data-ttu-id="61b63-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61b63-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61b63-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61b63-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61b63-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b63-126">CommonParameters</span></span>
<span data-ttu-id="61b63-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="61b63-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b63-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61b63-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b63-129">輸入</span><span class="sxs-lookup"><span data-stu-id="61b63-129">INPUTS</span></span>

### <span data-ttu-id="61b63-130">System.String</span><span class="sxs-lookup"><span data-stu-id="61b63-130">System.String</span></span>

## <span data-ttu-id="61b63-131">輸出</span><span class="sxs-lookup"><span data-stu-id="61b63-131">OUTPUTS</span></span>

### <span data-ttu-id="61b63-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="61b63-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="61b63-133">筆記</span><span class="sxs-lookup"><span data-stu-id="61b63-133">NOTES</span></span>

## <span data-ttu-id="61b63-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="61b63-134">RELATED LINKS</span></span>

[<span data-ttu-id="61b63-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="61b63-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="61b63-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="61b63-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="61b63-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="61b63-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="61b63-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="61b63-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


