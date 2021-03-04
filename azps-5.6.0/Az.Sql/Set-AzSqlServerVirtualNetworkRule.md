---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: b583c8339ebec74fdf8df4116204b7ad5523c258
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913702"
---
# <span data-ttu-id="32a8b-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="32a8b-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="32a8b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="32a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="32a8b-103">修改 Azure SQL Server 虛擬網路規則的組配置。</span><span class="sxs-lookup"><span data-stu-id="32a8b-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="32a8b-104">語法</span><span class="sxs-lookup"><span data-stu-id="32a8b-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32a8b-105">描述</span><span class="sxs-lookup"><span data-stu-id="32a8b-105">DESCRIPTION</span></span>
<span data-ttu-id="32a8b-106">此命令會修改 Azure SQL Server 虛擬網路規則的組配置。</span><span class="sxs-lookup"><span data-stu-id="32a8b-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="32a8b-107">若要控制伺服器中的一組虛擬網路規則，請改為使用 "Add-AzSqlServerVirtualNetworkRule" 和 'Remove-AzSqlServerVirtualNetworkRule'。</span><span class="sxs-lookup"><span data-stu-id="32a8b-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="32a8b-108">例子</span><span class="sxs-lookup"><span data-stu-id="32a8b-108">EXAMPLES</span></span>

### <span data-ttu-id="32a8b-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="32a8b-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="32a8b-110">使用包含新虛擬網路相關資訊的新虛擬網路子網識別碼修改現有的虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="32a8b-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="32a8b-111">參數</span><span class="sxs-lookup"><span data-stu-id="32a8b-111">PARAMETERS</span></span>

### <span data-ttu-id="32a8b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32a8b-112">-AsJob</span></span>
<span data-ttu-id="32a8b-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="32a8b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32a8b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a8b-114">-DefaultProfile</span></span>
<span data-ttu-id="32a8b-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="32a8b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32a8b-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="32a8b-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="32a8b-117">在啟用 vnet 服務端點之前建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="32a8b-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="32a8b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32a8b-118">-ResourceGroupName</span></span>
<span data-ttu-id="32a8b-119">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="32a8b-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="32a8b-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="32a8b-120">-ServerName</span></span>
<span data-ttu-id="32a8b-121">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="32a8b-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="32a8b-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="32a8b-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="32a8b-123">Azure Sql Server 虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="32a8b-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="32a8b-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="32a8b-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="32a8b-125">規則的虛擬網路子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="32a8b-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="32a8b-126">-確認</span><span class="sxs-lookup"><span data-stu-id="32a8b-126">-Confirm</span></span>
<span data-ttu-id="32a8b-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="32a8b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32a8b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32a8b-128">-WhatIf</span></span>
<span data-ttu-id="32a8b-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32a8b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32a8b-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32a8b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32a8b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a8b-131">CommonParameters</span></span>
<span data-ttu-id="32a8b-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="32a8b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a8b-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32a8b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a8b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="32a8b-134">INPUTS</span></span>

### <span data-ttu-id="32a8b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="32a8b-135">System.String</span></span>

## <span data-ttu-id="32a8b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="32a8b-136">OUTPUTS</span></span>

### <span data-ttu-id="32a8b-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="32a8b-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="32a8b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="32a8b-138">NOTES</span></span>

## <span data-ttu-id="32a8b-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="32a8b-139">RELATED LINKS</span></span>
