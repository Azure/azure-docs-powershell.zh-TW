---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: 1705b053939d8c5b67666d550c6c8340e892ae45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910958"
---
# <span data-ttu-id="ea8c9-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ea8c9-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="ea8c9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ea8c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8c9-103">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="ea8c9-104">語法</span><span class="sxs-lookup"><span data-stu-id="ea8c9-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea8c9-105">描述</span><span class="sxs-lookup"><span data-stu-id="ea8c9-105">DESCRIPTION</span></span>
<span data-ttu-id="ea8c9-106">建立或更新現有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="ea8c9-107">例子</span><span class="sxs-lookup"><span data-stu-id="ea8c9-107">EXAMPLES</span></span>

### <span data-ttu-id="ea8c9-108">範例 1：建立新的 PostgreSql 伺服器虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="ea8c9-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="ea8c9-109">這些 Cmdlet 會建立 PostgreSql 伺服器虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="ea8c9-110">參數</span><span class="sxs-lookup"><span data-stu-id="ea8c9-110">PARAMETERS</span></span>

### <span data-ttu-id="ea8c9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea8c9-111">-AsJob</span></span>
<span data-ttu-id="ea8c9-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="ea8c9-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ea8c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea8c9-113">-DefaultProfile</span></span>
<span data-ttu-id="ea8c9-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea8c9-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ea8c9-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="ea8c9-116">在啟用 vnet 服務端點之前建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="ea8c9-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea8c9-117">-Name</span></span>
<span data-ttu-id="ea8c9-118">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="ea8c9-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ea8c9-119">-NoWait</span></span>
<span data-ttu-id="ea8c9-120">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="ea8c9-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ea8c9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea8c9-121">-PassThru</span></span>
<span data-ttu-id="ea8c9-122">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="ea8c9-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ea8c9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea8c9-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea8c9-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-124">The name of the resource group.</span></span>
<span data-ttu-id="ea8c9-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ea8c9-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ea8c9-126">-ServerName</span></span>
<span data-ttu-id="ea8c9-127">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-127">The name of the server.</span></span>

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

### <span data-ttu-id="ea8c9-128">-子網Id</span><span class="sxs-lookup"><span data-stu-id="ea8c9-128">-SubnetId</span></span>
<span data-ttu-id="ea8c9-129">虛擬網路子網的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="ea8c9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea8c9-130">-SubscriptionId</span></span>
<span data-ttu-id="ea8c9-131">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ea8c9-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ea8c9-132">-Confirm</span></span>
<span data-ttu-id="ea8c9-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea8c9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea8c9-134">-WhatIf</span></span>
<span data-ttu-id="ea8c9-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea8c9-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea8c9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8c9-137">CommonParameters</span></span>
<span data-ttu-id="ea8c9-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ea8c9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8c9-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea8c9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8c9-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ea8c9-140">INPUTS</span></span>

## <span data-ttu-id="ea8c9-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ea8c9-141">OUTPUTS</span></span>

### <span data-ttu-id="ea8c9-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ea8c9-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="ea8c9-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ea8c9-143">NOTES</span></span>

<span data-ttu-id="ea8c9-144">別名</span><span class="sxs-lookup"><span data-stu-id="ea8c9-144">ALIASES</span></span>

## <span data-ttu-id="ea8c9-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea8c9-145">RELATED LINKS</span></span>

