---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 77a89dec96e0e9b7ca7bd003f8368274edf6acdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140090"
---
# <span data-ttu-id="e8a87-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e8a87-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="e8a87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8a87-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a87-103">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="e8a87-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="e8a87-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8a87-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e8a87-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8a87-105">DESCRIPTION</span></span>
<span data-ttu-id="e8a87-106">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="e8a87-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="e8a87-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8a87-107">EXAMPLES</span></span>

### <span data-ttu-id="e8a87-108">範例1：建立 MariaDB 的虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="e8a87-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="e8a87-109">這個命令會建立 MariaDB 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="e8a87-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="e8a87-110">參數</span><span class="sxs-lookup"><span data-stu-id="e8a87-110">PARAMETERS</span></span>

### <span data-ttu-id="e8a87-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8a87-111">-AsJob</span></span>
<span data-ttu-id="e8a87-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="e8a87-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e8a87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a87-113">-DefaultProfile</span></span>
<span data-ttu-id="e8a87-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8a87-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8a87-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8a87-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="e8a87-116">在虛擬網路啟用 vnet 服務端點之前，請先建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="e8a87-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="e8a87-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8a87-117">-Name</span></span>
<span data-ttu-id="e8a87-118">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8a87-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="e8a87-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e8a87-119">-NoWait</span></span>
<span data-ttu-id="e8a87-120">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="e8a87-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e8a87-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8a87-121">-PassThru</span></span>
<span data-ttu-id="e8a87-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="e8a87-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e8a87-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8a87-123">-ResourceGroupName</span></span>
<span data-ttu-id="e8a87-124">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8a87-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e8a87-125">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="e8a87-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e8a87-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e8a87-126">-ServerName</span></span>
<span data-ttu-id="e8a87-127">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8a87-127">The name of the server.</span></span>

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

### <span data-ttu-id="e8a87-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e8a87-128">-SubnetId</span></span>
<span data-ttu-id="e8a87-129">虛擬網路子網的 ARM 資源 id。</span><span class="sxs-lookup"><span data-stu-id="e8a87-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="e8a87-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8a87-130">-SubscriptionId</span></span>
<span data-ttu-id="e8a87-131">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="e8a87-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e8a87-132">-確認</span><span class="sxs-lookup"><span data-stu-id="e8a87-132">-Confirm</span></span>
<span data-ttu-id="e8a87-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8a87-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8a87-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8a87-134">-WhatIf</span></span>
<span data-ttu-id="e8a87-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8a87-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8a87-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8a87-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8a87-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a87-137">CommonParameters</span></span>
<span data-ttu-id="e8a87-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8a87-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a87-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8a87-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a87-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e8a87-140">INPUTS</span></span>

## <span data-ttu-id="e8a87-141">輸出</span><span class="sxs-lookup"><span data-stu-id="e8a87-141">OUTPUTS</span></span>

### <span data-ttu-id="e8a87-142">IVirtualNetworkRule （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="e8a87-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="e8a87-143">筆記</span><span class="sxs-lookup"><span data-stu-id="e8a87-143">NOTES</span></span>

<span data-ttu-id="e8a87-144">別名</span><span class="sxs-lookup"><span data-stu-id="e8a87-144">ALIASES</span></span>

## <span data-ttu-id="e8a87-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8a87-145">RELATED LINKS</span></span>

