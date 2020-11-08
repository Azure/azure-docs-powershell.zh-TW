---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 3b660f5db14e1197c1e262a10f8225e4e9a82b81
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969618"
---
# <span data-ttu-id="37315-101">New-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="37315-101">New-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="37315-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37315-102">SYNOPSIS</span></span>
<span data-ttu-id="37315-103">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="37315-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="37315-104">句法</span><span class="sxs-lookup"><span data-stu-id="37315-104">SYNTAX</span></span>

```
New-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37315-105">說明</span><span class="sxs-lookup"><span data-stu-id="37315-105">DESCRIPTION</span></span>
<span data-ttu-id="37315-106">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="37315-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="37315-107">示例</span><span class="sxs-lookup"><span data-stu-id="37315-107">EXAMPLES</span></span>

### <span data-ttu-id="37315-108">範例1：建立新的 MySql 伺服器虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="37315-108">Example 1: Create a new MySql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> New-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="37315-109">這些 Cmdlet 會建立 MySql 伺服器虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="37315-109">These cmdlets create a MySql server Virtual Network Rule.</span></span>

## <span data-ttu-id="37315-110">參數</span><span class="sxs-lookup"><span data-stu-id="37315-110">PARAMETERS</span></span>

### <span data-ttu-id="37315-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37315-111">-AsJob</span></span>
<span data-ttu-id="37315-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="37315-112">Run the command as a job</span></span>

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

### <span data-ttu-id="37315-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37315-113">-DefaultProfile</span></span>
<span data-ttu-id="37315-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37315-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37315-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="37315-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="37315-116">在虛擬網路啟用 vnet 服務端點之前，請先建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="37315-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="37315-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="37315-117">-Name</span></span>
<span data-ttu-id="37315-118">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="37315-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37315-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="37315-119">-NoWait</span></span>
<span data-ttu-id="37315-120">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="37315-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="37315-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37315-121">-PassThru</span></span>
<span data-ttu-id="37315-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="37315-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="37315-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37315-123">-ResourceGroupName</span></span>
<span data-ttu-id="37315-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="37315-124">The name of the resource group.</span></span>
<span data-ttu-id="37315-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="37315-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="37315-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="37315-126">-ServerName</span></span>
<span data-ttu-id="37315-127">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="37315-127">The name of the server.</span></span>

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

### <span data-ttu-id="37315-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="37315-128">-SubnetId</span></span>
<span data-ttu-id="37315-129">虛擬網路子網的 ARM 資源 id。</span><span class="sxs-lookup"><span data-stu-id="37315-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="37315-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37315-130">-SubscriptionId</span></span>
<span data-ttu-id="37315-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="37315-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37315-132">-確認</span><span class="sxs-lookup"><span data-stu-id="37315-132">-Confirm</span></span>
<span data-ttu-id="37315-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="37315-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37315-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37315-134">-WhatIf</span></span>
<span data-ttu-id="37315-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37315-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37315-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37315-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37315-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37315-137">CommonParameters</span></span>
<span data-ttu-id="37315-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37315-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37315-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="37315-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37315-140">輸入</span><span class="sxs-lookup"><span data-stu-id="37315-140">INPUTS</span></span>

## <span data-ttu-id="37315-141">輸出</span><span class="sxs-lookup"><span data-stu-id="37315-141">OUTPUTS</span></span>

### <span data-ttu-id="37315-142">IVirtualNetworkRule 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="37315-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="37315-143">筆記</span><span class="sxs-lookup"><span data-stu-id="37315-143">NOTES</span></span>

<span data-ttu-id="37315-144">別名</span><span class="sxs-lookup"><span data-stu-id="37315-144">ALIASES</span></span>

## <span data-ttu-id="37315-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="37315-145">RELATED LINKS</span></span>
