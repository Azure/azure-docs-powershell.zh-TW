---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: c6766e27c40f52b9d146590e91f6ecc73d5f32f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913174"
---
# <span data-ttu-id="b0794-101">New-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b0794-101">New-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="b0794-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b0794-102">SYNOPSIS</span></span>
<span data-ttu-id="b0794-103">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b0794-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="b0794-104">語法</span><span class="sxs-lookup"><span data-stu-id="b0794-104">SYNTAX</span></span>

```
New-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b0794-105">描述</span><span class="sxs-lookup"><span data-stu-id="b0794-105">DESCRIPTION</span></span>
<span data-ttu-id="b0794-106">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b0794-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="b0794-107">例子</span><span class="sxs-lookup"><span data-stu-id="b0794-107">EXAMPLES</span></span>

### <span data-ttu-id="b0794-108">範例 1：建立新 MySql 伺服器虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="b0794-108">Example 1: Create a new MySql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> New-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="b0794-109">這些 Cmdlet 會建立 MySql 伺服器虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b0794-109">These cmdlets create a MySql server Virtual Network Rule.</span></span>

## <span data-ttu-id="b0794-110">參數</span><span class="sxs-lookup"><span data-stu-id="b0794-110">PARAMETERS</span></span>

### <span data-ttu-id="b0794-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0794-111">-AsJob</span></span>
<span data-ttu-id="b0794-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="b0794-112">Run the command as a job</span></span>

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

### <span data-ttu-id="b0794-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0794-113">-DefaultProfile</span></span>
<span data-ttu-id="b0794-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0794-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0794-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0794-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="b0794-116">在啟用 vnet 服務端點之前建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b0794-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="b0794-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0794-117">-Name</span></span>
<span data-ttu-id="b0794-118">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0794-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="b0794-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b0794-119">-NoWait</span></span>
<span data-ttu-id="b0794-120">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="b0794-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b0794-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0794-121">-PassThru</span></span>
<span data-ttu-id="b0794-122">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="b0794-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b0794-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0794-123">-ResourceGroupName</span></span>
<span data-ttu-id="b0794-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0794-124">The name of the resource group.</span></span>
<span data-ttu-id="b0794-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b0794-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b0794-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b0794-126">-ServerName</span></span>
<span data-ttu-id="b0794-127">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b0794-127">The name of the server.</span></span>

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

### <span data-ttu-id="b0794-128">-子網Id</span><span class="sxs-lookup"><span data-stu-id="b0794-128">-SubnetId</span></span>
<span data-ttu-id="b0794-129">虛擬網路子網的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0794-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="b0794-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0794-130">-SubscriptionId</span></span>
<span data-ttu-id="b0794-131">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0794-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b0794-132">-確認</span><span class="sxs-lookup"><span data-stu-id="b0794-132">-Confirm</span></span>
<span data-ttu-id="b0794-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b0794-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0794-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0794-134">-WhatIf</span></span>
<span data-ttu-id="b0794-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b0794-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0794-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0794-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0794-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0794-137">CommonParameters</span></span>
<span data-ttu-id="b0794-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b0794-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0794-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0794-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0794-140">輸入</span><span class="sxs-lookup"><span data-stu-id="b0794-140">INPUTS</span></span>

## <span data-ttu-id="b0794-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b0794-141">OUTPUTS</span></span>

### <span data-ttu-id="b0794-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b0794-142">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="b0794-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b0794-143">NOTES</span></span>

<span data-ttu-id="b0794-144">別名</span><span class="sxs-lookup"><span data-stu-id="b0794-144">ALIASES</span></span>

## <span data-ttu-id="b0794-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0794-145">RELATED LINKS</span></span>

