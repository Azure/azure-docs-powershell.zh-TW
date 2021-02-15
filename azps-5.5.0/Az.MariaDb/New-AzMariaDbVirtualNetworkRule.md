---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 77a89dec96e0e9b7ca7bd003f8368274edf6acdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131578"
---
# <span data-ttu-id="a0970-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a0970-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="a0970-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0970-102">SYNOPSIS</span></span>
<span data-ttu-id="a0970-103">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a0970-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="a0970-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0970-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a0970-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0970-105">DESCRIPTION</span></span>
<span data-ttu-id="a0970-106">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a0970-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="a0970-107">示例</span><span class="sxs-lookup"><span data-stu-id="a0970-107">EXAMPLES</span></span>

### <span data-ttu-id="a0970-108">範例1：建立 MariaDB 的虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="a0970-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="a0970-109">這個命令會建立 MariaDB 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a0970-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="a0970-110">參數</span><span class="sxs-lookup"><span data-stu-id="a0970-110">PARAMETERS</span></span>

### <span data-ttu-id="a0970-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0970-111">-AsJob</span></span>
<span data-ttu-id="a0970-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="a0970-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a0970-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0970-113">-DefaultProfile</span></span>
<span data-ttu-id="a0970-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0970-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0970-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0970-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="a0970-116">在虛擬網路啟用 vnet 服務端點之前，請先建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="a0970-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="a0970-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0970-117">-Name</span></span>
<span data-ttu-id="a0970-118">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0970-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="a0970-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a0970-119">-NoWait</span></span>
<span data-ttu-id="a0970-120">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="a0970-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a0970-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0970-121">-PassThru</span></span>
<span data-ttu-id="a0970-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="a0970-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a0970-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0970-123">-ResourceGroupName</span></span>
<span data-ttu-id="a0970-124">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0970-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a0970-125">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="a0970-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a0970-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a0970-126">-ServerName</span></span>
<span data-ttu-id="a0970-127">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0970-127">The name of the server.</span></span>

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

### <span data-ttu-id="a0970-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a0970-128">-SubnetId</span></span>
<span data-ttu-id="a0970-129">虛擬網路子網的 ARM 資源 id。</span><span class="sxs-lookup"><span data-stu-id="a0970-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="a0970-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0970-130">-SubscriptionId</span></span>
<span data-ttu-id="a0970-131">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="a0970-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a0970-132">-確認</span><span class="sxs-lookup"><span data-stu-id="a0970-132">-Confirm</span></span>
<span data-ttu-id="a0970-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0970-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0970-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0970-134">-WhatIf</span></span>
<span data-ttu-id="a0970-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0970-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0970-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0970-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0970-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0970-137">CommonParameters</span></span>
<span data-ttu-id="a0970-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0970-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0970-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0970-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0970-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a0970-140">INPUTS</span></span>

## <span data-ttu-id="a0970-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a0970-141">OUTPUTS</span></span>

### <span data-ttu-id="a0970-142">IVirtualNetworkRule （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="a0970-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="a0970-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a0970-143">NOTES</span></span>

<span data-ttu-id="a0970-144">別名</span><span class="sxs-lookup"><span data-stu-id="a0970-144">ALIASES</span></span>

## <span data-ttu-id="a0970-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0970-145">RELATED LINKS</span></span>

