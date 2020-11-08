---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 55321b384a24e18a962b99cc40161eabbeb00160
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136626"
---
# <span data-ttu-id="7cc5e-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7cc5e-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="7cc5e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7cc5e-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc5e-103">修改 Azure SQL Server 虛擬網路規則的設定。</span><span class="sxs-lookup"><span data-stu-id="7cc5e-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="7cc5e-104">句法</span><span class="sxs-lookup"><span data-stu-id="7cc5e-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cc5e-105">說明</span><span class="sxs-lookup"><span data-stu-id="7cc5e-105">DESCRIPTION</span></span>
<span data-ttu-id="7cc5e-106">這個命令會修改 Azure SQL Server 虛擬網路規則的設定。</span><span class="sxs-lookup"><span data-stu-id="7cc5e-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="7cc5e-107">若要控制伺服器中的一組虛擬網路規則，請改用 [Add-AzSqlServerVirtualNetworkRule] 和 [Remove-AzSqlServerVirtualNetworkRule]。</span><span class="sxs-lookup"><span data-stu-id="7cc5e-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="7cc5e-108">示例</span><span class="sxs-lookup"><span data-stu-id="7cc5e-108">EXAMPLES</span></span>

### <span data-ttu-id="7cc5e-109">範例1</span><span class="sxs-lookup"><span data-stu-id="7cc5e-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="7cc5e-110">使用新的虛擬網路子網 id （包含新虛擬網路的相關資訊）來修改現有的虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="7cc5e-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="7cc5e-111">參數</span><span class="sxs-lookup"><span data-stu-id="7cc5e-111">PARAMETERS</span></span>

### <span data-ttu-id="7cc5e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cc5e-112">-AsJob</span></span>
<span data-ttu-id="7cc5e-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7cc5e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7cc5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc5e-114">-DefaultProfile</span></span>
<span data-ttu-id="7cc5e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7cc5e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cc5e-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cc5e-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="7cc5e-117">在虛擬網路啟用 vnet 服務端點之前，請先建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="7cc5e-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="7cc5e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cc5e-118">-ResourceGroupName</span></span>
<span data-ttu-id="7cc5e-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cc5e-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="7cc5e-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7cc5e-120">-ServerName</span></span>
<span data-ttu-id="7cc5e-121">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="7cc5e-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="7cc5e-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="7cc5e-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="7cc5e-123">Azure Sql Server 虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="7cc5e-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="7cc5e-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="7cc5e-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="7cc5e-125">規則的虛擬網路子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="7cc5e-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="7cc5e-126">-確認</span><span class="sxs-lookup"><span data-stu-id="7cc5e-126">-Confirm</span></span>
<span data-ttu-id="7cc5e-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7cc5e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cc5e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cc5e-128">-WhatIf</span></span>
<span data-ttu-id="7cc5e-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7cc5e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cc5e-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7cc5e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cc5e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc5e-131">CommonParameters</span></span>
<span data-ttu-id="7cc5e-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7cc5e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc5e-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7cc5e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc5e-134">輸入</span><span class="sxs-lookup"><span data-stu-id="7cc5e-134">INPUTS</span></span>

### <span data-ttu-id="7cc5e-135">System.object</span><span class="sxs-lookup"><span data-stu-id="7cc5e-135">System.String</span></span>

## <span data-ttu-id="7cc5e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="7cc5e-136">OUTPUTS</span></span>

### <span data-ttu-id="7cc5e-137">AzureSqlServerVirtualNetworkRuleModel 中的 [VirtualNetworkRule]</span><span class="sxs-lookup"><span data-stu-id="7cc5e-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="7cc5e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="7cc5e-138">NOTES</span></span>

## <span data-ttu-id="7cc5e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="7cc5e-139">RELATED LINKS</span></span>