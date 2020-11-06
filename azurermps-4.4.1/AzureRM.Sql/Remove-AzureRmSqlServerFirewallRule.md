---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 1f7f039bb0bba1338fdcc4d5ceb3a403822fba71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446619"
---
# <span data-ttu-id="9861d-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9861d-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="9861d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9861d-102">SYNOPSIS</span></span>
<span data-ttu-id="9861d-103">從 SQL 資料庫伺服器刪除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="9861d-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9861d-104">句法</span><span class="sxs-lookup"><span data-stu-id="9861d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9861d-105">說明</span><span class="sxs-lookup"><span data-stu-id="9861d-105">DESCRIPTION</span></span>
<span data-ttu-id="9861d-106">**AzureRmSqlServerFirewallRule** Cmdlet 會從指定的 Azure SQL Database 伺服器刪除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="9861d-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="9861d-107">示例</span><span class="sxs-lookup"><span data-stu-id="9861d-107">EXAMPLES</span></span>

### <span data-ttu-id="9861d-108">範例1：刪除規則</span><span class="sxs-lookup"><span data-stu-id="9861d-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "RresourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="9861d-109">這個命令會刪除名為 Server01 的伺服器上名為 Rule01 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="9861d-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="9861d-110">參數</span><span class="sxs-lookup"><span data-stu-id="9861d-110">PARAMETERS</span></span>

### <span data-ttu-id="9861d-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="9861d-111">-FirewallRuleName</span></span>
<span data-ttu-id="9861d-112">指定此 Cmdlet 刪除的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="9861d-112">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="9861d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9861d-113">-Force</span></span>
<span data-ttu-id="9861d-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="9861d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9861d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9861d-115">-ResourceGroupName</span></span>
<span data-ttu-id="9861d-116">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9861d-116">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9861d-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9861d-117">-ServerName</span></span>
<span data-ttu-id="9861d-118">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9861d-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="9861d-119">-確認</span><span class="sxs-lookup"><span data-stu-id="9861d-119">-Confirm</span></span>
<span data-ttu-id="9861d-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9861d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9861d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9861d-121">-WhatIf</span></span>
<span data-ttu-id="9861d-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9861d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9861d-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9861d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9861d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9861d-124">-DefaultProfile</span></span>
<span data-ttu-id="9861d-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9861d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9861d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9861d-126">CommonParameters</span></span>
<span data-ttu-id="9861d-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9861d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9861d-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9861d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9861d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="9861d-129">INPUTS</span></span>

### <span data-ttu-id="9861d-130">AzureSqlServerFirewallRuleModel 中的 [FirewallRule]</span><span class="sxs-lookup"><span data-stu-id="9861d-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="9861d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9861d-131">OUTPUTS</span></span>

## <span data-ttu-id="9861d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="9861d-132">NOTES</span></span>

## <span data-ttu-id="9861d-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="9861d-133">RELATED LINKS</span></span>

[<span data-ttu-id="9861d-134">AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9861d-134">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="9861d-135">新-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9861d-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="9861d-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9861d-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="9861d-137">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="9861d-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


