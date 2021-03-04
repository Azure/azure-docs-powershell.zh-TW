---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: c511e605af327f5ac1b913f133cf725baeee894c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906578"
---
# <span data-ttu-id="b528a-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b528a-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="b528a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b528a-102">SYNOPSIS</span></span>
<span data-ttu-id="b528a-103">建立新防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b528a-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b528a-104">語法</span><span class="sxs-lookup"><span data-stu-id="b528a-104">SYNTAX</span></span>

### <span data-ttu-id="b528a-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="b528a-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b528a-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="b528a-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b528a-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b528a-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b528a-108">描述</span><span class="sxs-lookup"><span data-stu-id="b528a-108">DESCRIPTION</span></span>
<span data-ttu-id="b528a-109">建立新防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b528a-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b528a-110">例子</span><span class="sxs-lookup"><span data-stu-id="b528a-110">EXAMPLES</span></span>

### <span data-ttu-id="b528a-111">範例 1：在 MariaDB 下建立防火牆規則</span><span class="sxs-lookup"><span data-stu-id="b528a-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="b528a-112">此命令在 MariaDB 下建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b528a-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="b528a-113">範例 2：使用 -ClientIPAddress 建立新 MariaDB 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b528a-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="b528a-114">此 Cmdlet 會使用 -ClientIPAddress 建立 MariaDB 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b528a-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="b528a-115">範例 3：建立新 MariaDB 防火牆規則以允許所有 IP</span><span class="sxs-lookup"><span data-stu-id="b528a-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="b528a-116">此 Cmdlet 會建立新的 MariaDB 防火牆規則，以允許所有 IP。</span><span class="sxs-lookup"><span data-stu-id="b528a-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="b528a-117">參數</span><span class="sxs-lookup"><span data-stu-id="b528a-117">PARAMETERS</span></span>

### <span data-ttu-id="b528a-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="b528a-118">-AllowAll</span></span>
<span data-ttu-id="b528a-119">展示以允許所有範圍 IP，範圍從 0.0.0.0 到 255.255.255.255。</span><span class="sxs-lookup"><span data-stu-id="b528a-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AllowAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b528a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b528a-120">-AsJob</span></span>
<span data-ttu-id="b528a-121">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="b528a-121">Run the command as a job</span></span>

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

### <span data-ttu-id="b528a-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b528a-122">-ClientIPAddress</span></span>
<span data-ttu-id="b528a-123">用戶端指定的伺服器防火牆規則之單一 IP。</span><span class="sxs-lookup"><span data-stu-id="b528a-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="b528a-124">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="b528a-124">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b528a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b528a-125">-DefaultProfile</span></span>
<span data-ttu-id="b528a-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b528a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b528a-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="b528a-127">-EndIPAddress</span></span>
<span data-ttu-id="b528a-128">伺服器防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b528a-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="b528a-129">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="b528a-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b528a-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="b528a-130">-Name</span></span>
<span data-ttu-id="b528a-131">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b528a-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="b528a-132">如果未指定，則預設為未定義。</span><span class="sxs-lookup"><span data-stu-id="b528a-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="b528a-133">如果 AllowAll 存在，預設名稱為 AllowAll_yyyy-MM-dd_HH-mm-ss。</span><span class="sxs-lookup"><span data-stu-id="b528a-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b528a-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b528a-134">-NoWait</span></span>
<span data-ttu-id="b528a-135">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="b528a-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b528a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b528a-136">-ResourceGroupName</span></span>
<span data-ttu-id="b528a-137">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b528a-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b528a-138">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="b528a-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b528a-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b528a-139">-ServerName</span></span>
<span data-ttu-id="b528a-140">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b528a-140">The name of the server.</span></span>

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

### <span data-ttu-id="b528a-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="b528a-141">-StartIPAddress</span></span>
<span data-ttu-id="b528a-142">伺服器防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b528a-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="b528a-143">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="b528a-143">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b528a-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b528a-144">-SubscriptionId</span></span>
<span data-ttu-id="b528a-145">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b528a-145">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b528a-146">-確認</span><span class="sxs-lookup"><span data-stu-id="b528a-146">-Confirm</span></span>
<span data-ttu-id="b528a-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b528a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b528a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b528a-148">-WhatIf</span></span>
<span data-ttu-id="b528a-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b528a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b528a-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b528a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b528a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b528a-151">CommonParameters</span></span>
<span data-ttu-id="b528a-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b528a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b528a-153">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b528a-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b528a-154">輸入</span><span class="sxs-lookup"><span data-stu-id="b528a-154">INPUTS</span></span>

## <span data-ttu-id="b528a-155">輸出</span><span class="sxs-lookup"><span data-stu-id="b528a-155">OUTPUTS</span></span>

### <span data-ttu-id="b528a-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b528a-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="b528a-157">筆記</span><span class="sxs-lookup"><span data-stu-id="b528a-157">NOTES</span></span>

<span data-ttu-id="b528a-158">別名</span><span class="sxs-lookup"><span data-stu-id="b528a-158">ALIASES</span></span>

## <span data-ttu-id="b528a-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="b528a-159">RELATED LINKS</span></span>

