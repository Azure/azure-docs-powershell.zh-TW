---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: cfbbfd9472d18d75dea3da68cb4d2e06cf54c9a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906565"
---
# <span data-ttu-id="c320b-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c320b-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="c320b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c320b-102">SYNOPSIS</span></span>
<span data-ttu-id="c320b-103">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="c320b-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="c320b-104">語法</span><span class="sxs-lookup"><span data-stu-id="c320b-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c320b-105">描述</span><span class="sxs-lookup"><span data-stu-id="c320b-105">DESCRIPTION</span></span>
<span data-ttu-id="c320b-106">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="c320b-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="c320b-107">例子</span><span class="sxs-lookup"><span data-stu-id="c320b-107">EXAMPLES</span></span>

### <span data-ttu-id="c320b-108">範例 1：為 MariaDB 建立虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="c320b-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="c320b-109">此命令會為 MariaDB 建立虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="c320b-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="c320b-110">參數</span><span class="sxs-lookup"><span data-stu-id="c320b-110">PARAMETERS</span></span>

### <span data-ttu-id="c320b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c320b-111">-AsJob</span></span>
<span data-ttu-id="c320b-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="c320b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c320b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c320b-113">-DefaultProfile</span></span>
<span data-ttu-id="c320b-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c320b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c320b-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c320b-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="c320b-116">在啟用 vnet 服務端點之前建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="c320b-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="c320b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c320b-117">-Name</span></span>
<span data-ttu-id="c320b-118">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c320b-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="c320b-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c320b-119">-NoWait</span></span>
<span data-ttu-id="c320b-120">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="c320b-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c320b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c320b-121">-PassThru</span></span>
<span data-ttu-id="c320b-122">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="c320b-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c320b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c320b-123">-ResourceGroupName</span></span>
<span data-ttu-id="c320b-124">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c320b-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c320b-125">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="c320b-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c320b-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c320b-126">-ServerName</span></span>
<span data-ttu-id="c320b-127">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c320b-127">The name of the server.</span></span>

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

### <span data-ttu-id="c320b-128">-子網Id</span><span class="sxs-lookup"><span data-stu-id="c320b-128">-SubnetId</span></span>
<span data-ttu-id="c320b-129">虛擬網路子網的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c320b-129">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c320b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c320b-130">-SubscriptionId</span></span>
<span data-ttu-id="c320b-131">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="c320b-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="c320b-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c320b-132">-Confirm</span></span>
<span data-ttu-id="c320b-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c320b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c320b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c320b-134">-WhatIf</span></span>
<span data-ttu-id="c320b-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c320b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c320b-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c320b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c320b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c320b-137">CommonParameters</span></span>
<span data-ttu-id="c320b-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c320b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c320b-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c320b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c320b-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c320b-140">INPUTS</span></span>

## <span data-ttu-id="c320b-141">輸出</span><span class="sxs-lookup"><span data-stu-id="c320b-141">OUTPUTS</span></span>

### <span data-ttu-id="c320b-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c320b-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="c320b-143">筆記</span><span class="sxs-lookup"><span data-stu-id="c320b-143">NOTES</span></span>

<span data-ttu-id="c320b-144">別名</span><span class="sxs-lookup"><span data-stu-id="c320b-144">ALIASES</span></span>

## <span data-ttu-id="c320b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c320b-145">RELATED LINKS</span></span>

