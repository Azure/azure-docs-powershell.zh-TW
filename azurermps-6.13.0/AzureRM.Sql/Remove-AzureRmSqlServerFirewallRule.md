---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 3e0f7e021f6ddf2f9b18873dda4f9d482a4db1da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626038"
---
# <span data-ttu-id="e889a-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e889a-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="e889a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e889a-102">SYNOPSIS</span></span>
<span data-ttu-id="e889a-103">從 SQL 資料庫伺服器刪除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="e889a-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e889a-104">句法</span><span class="sxs-lookup"><span data-stu-id="e889a-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e889a-105">說明</span><span class="sxs-lookup"><span data-stu-id="e889a-105">DESCRIPTION</span></span>
<span data-ttu-id="e889a-106">**AzureRmSqlServerFirewallRule** Cmdlet 會從指定的 Azure SQL Database 伺服器刪除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="e889a-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="e889a-107">示例</span><span class="sxs-lookup"><span data-stu-id="e889a-107">EXAMPLES</span></span>

### <span data-ttu-id="e889a-108">範例1：刪除規則</span><span class="sxs-lookup"><span data-stu-id="e889a-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="e889a-109">這個命令會刪除名為 Server01 的伺服器上名為 Rule01 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="e889a-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="e889a-110">參數</span><span class="sxs-lookup"><span data-stu-id="e889a-110">PARAMETERS</span></span>

### <span data-ttu-id="e889a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e889a-111">-DefaultProfile</span></span>
<span data-ttu-id="e889a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e889a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e889a-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="e889a-113">-FirewallRuleName</span></span>
<span data-ttu-id="e889a-114">指定此 Cmdlet 刪除的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="e889a-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e889a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e889a-115">-Force</span></span>
<span data-ttu-id="e889a-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e889a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e889a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e889a-117">-ResourceGroupName</span></span>
<span data-ttu-id="e889a-118">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e889a-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e889a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e889a-119">-ServerName</span></span>
<span data-ttu-id="e889a-120">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e889a-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e889a-121">-確認</span><span class="sxs-lookup"><span data-stu-id="e889a-121">-Confirm</span></span>
<span data-ttu-id="e889a-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e889a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e889a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e889a-123">-WhatIf</span></span>
<span data-ttu-id="e889a-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e889a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e889a-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e889a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e889a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e889a-126">CommonParameters</span></span>
<span data-ttu-id="e889a-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e889a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e889a-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e889a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e889a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e889a-129">INPUTS</span></span>

### <span data-ttu-id="e889a-130">System.object</span><span class="sxs-lookup"><span data-stu-id="e889a-130">System.String</span></span>

## <span data-ttu-id="e889a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e889a-131">OUTPUTS</span></span>

### <span data-ttu-id="e889a-132">AzureSqlServerFirewallRuleModel 中的 [FirewallRule]</span><span class="sxs-lookup"><span data-stu-id="e889a-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="e889a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e889a-133">NOTES</span></span>

## <span data-ttu-id="e889a-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e889a-134">RELATED LINKS</span></span>

[<span data-ttu-id="e889a-135">AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e889a-135">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="e889a-136">新-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e889a-136">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="e889a-137">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e889a-137">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="e889a-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="e889a-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


