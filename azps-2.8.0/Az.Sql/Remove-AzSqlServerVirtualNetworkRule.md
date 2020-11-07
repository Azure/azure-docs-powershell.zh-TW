---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: de7df0147cc28d413444282987f8d5b27f9607a2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792674"
---
# <span data-ttu-id="67185-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="67185-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="67185-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67185-102">SYNOPSIS</span></span>
<span data-ttu-id="67185-103">刪除 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="67185-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="67185-104">句法</span><span class="sxs-lookup"><span data-stu-id="67185-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67185-105">說明</span><span class="sxs-lookup"><span data-stu-id="67185-105">DESCRIPTION</span></span>
<span data-ttu-id="67185-106">這個命令會刪除 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="67185-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="67185-107">示例</span><span class="sxs-lookup"><span data-stu-id="67185-107">EXAMPLES</span></span>

### <span data-ttu-id="67185-108">範例1</span><span class="sxs-lookup"><span data-stu-id="67185-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="67185-109">刪除現有的 Azure SQL Server 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="67185-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="67185-110">參數</span><span class="sxs-lookup"><span data-stu-id="67185-110">PARAMETERS</span></span>

### <span data-ttu-id="67185-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67185-111">-AsJob</span></span>
<span data-ttu-id="67185-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="67185-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67185-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67185-113">-DefaultProfile</span></span>
<span data-ttu-id="67185-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="67185-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67185-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67185-115">-ResourceGroupName</span></span>
<span data-ttu-id="67185-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="67185-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="67185-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="67185-117">-ServerName</span></span>
<span data-ttu-id="67185-118">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="67185-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="67185-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="67185-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="67185-120">Azure Sql Server 虛擬網路規則名稱</span><span class="sxs-lookup"><span data-stu-id="67185-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="67185-121">-確認</span><span class="sxs-lookup"><span data-stu-id="67185-121">-Confirm</span></span>
<span data-ttu-id="67185-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="67185-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67185-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67185-123">-WhatIf</span></span>
<span data-ttu-id="67185-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67185-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67185-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67185-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67185-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67185-126">CommonParameters</span></span>
<span data-ttu-id="67185-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67185-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67185-128">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="67185-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67185-129">輸入</span><span class="sxs-lookup"><span data-stu-id="67185-129">INPUTS</span></span>

### <span data-ttu-id="67185-130">System.object</span><span class="sxs-lookup"><span data-stu-id="67185-130">System.String</span></span>

## <span data-ttu-id="67185-131">輸出</span><span class="sxs-lookup"><span data-stu-id="67185-131">OUTPUTS</span></span>

### <span data-ttu-id="67185-132">AzureSqlServerVirtualNetworkRuleModel 中的 [VirtualNetworkRule]</span><span class="sxs-lookup"><span data-stu-id="67185-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="67185-133">筆記</span><span class="sxs-lookup"><span data-stu-id="67185-133">NOTES</span></span>

## <span data-ttu-id="67185-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="67185-134">RELATED LINKS</span></span>
