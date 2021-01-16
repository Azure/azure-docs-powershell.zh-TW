---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284391"
---
# <span data-ttu-id="da2c3-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da2c3-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="da2c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="da2c3-103">建立新的防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="da2c3-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="da2c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="da2c3-104">SYNTAX</span></span>

### <span data-ttu-id="da2c3-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="da2c3-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da2c3-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="da2c3-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="da2c3-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="da2c3-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da2c3-108">說明</span><span class="sxs-lookup"><span data-stu-id="da2c3-108">DESCRIPTION</span></span>
<span data-ttu-id="da2c3-109">建立新的防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="da2c3-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="da2c3-110">示例</span><span class="sxs-lookup"><span data-stu-id="da2c3-110">EXAMPLES</span></span>

### <span data-ttu-id="da2c3-111">範例1：在 MariaDB 下建立防火牆規則</span><span class="sxs-lookup"><span data-stu-id="da2c3-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="da2c3-112">這個命令會在 MariaDB 下建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="da2c3-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="da2c3-113">範例2：使用-ClientIPAddress 建立新的 MariaDB 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="da2c3-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="da2c3-114">這個 Cmdlet 會使用-ClientIPAddress 建立 MariaDB 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="da2c3-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="da2c3-115">範例3：建立新的 MariaDB 防火牆規則，以允許所有 Ip</span><span class="sxs-lookup"><span data-stu-id="da2c3-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="da2c3-116">這個 Cmdlet 會建立新的 MariaDB 防火牆規則，以允許所有的 Ip。</span><span class="sxs-lookup"><span data-stu-id="da2c3-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="da2c3-117">參數</span><span class="sxs-lookup"><span data-stu-id="da2c3-117">PARAMETERS</span></span>

### <span data-ttu-id="da2c3-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="da2c3-118">-AllowAll</span></span>
<span data-ttu-id="da2c3-119">[提供] 可允許所有範圍的 Ip （從0.0.0.0 到255.255.255.255）。</span><span class="sxs-lookup"><span data-stu-id="da2c3-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="da2c3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da2c3-120">-AsJob</span></span>
<span data-ttu-id="da2c3-121">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="da2c3-121">Run the command as a job</span></span>

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

### <span data-ttu-id="da2c3-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="da2c3-122">-ClientIPAddress</span></span>
<span data-ttu-id="da2c3-123">用戶端指定的伺服器防火牆規則單一 IP。</span><span class="sxs-lookup"><span data-stu-id="da2c3-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="da2c3-124">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="da2c3-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="da2c3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da2c3-125">-DefaultProfile</span></span>
<span data-ttu-id="da2c3-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="da2c3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da2c3-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="da2c3-127">-EndIPAddress</span></span>
<span data-ttu-id="da2c3-128">伺服器防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="da2c3-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="da2c3-129">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="da2c3-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="da2c3-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="da2c3-130">-Name</span></span>
<span data-ttu-id="da2c3-131">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="da2c3-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="da2c3-132">如果未指定，則預設值為未定義。</span><span class="sxs-lookup"><span data-stu-id="da2c3-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="da2c3-133">如果 AllowAll 存在，預設名稱是 AllowAll_yyyy MM dd_HH-ss。</span><span class="sxs-lookup"><span data-stu-id="da2c3-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="da2c3-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="da2c3-134">-NoWait</span></span>
<span data-ttu-id="da2c3-135">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="da2c3-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="da2c3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da2c3-136">-ResourceGroupName</span></span>
<span data-ttu-id="da2c3-137">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="da2c3-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="da2c3-138">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="da2c3-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="da2c3-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="da2c3-139">-ServerName</span></span>
<span data-ttu-id="da2c3-140">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="da2c3-140">The name of the server.</span></span>

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

### <span data-ttu-id="da2c3-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="da2c3-141">-StartIPAddress</span></span>
<span data-ttu-id="da2c3-142">伺服器防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="da2c3-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="da2c3-143">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="da2c3-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="da2c3-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da2c3-144">-SubscriptionId</span></span>
<span data-ttu-id="da2c3-145">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="da2c3-145">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="da2c3-146">-確認</span><span class="sxs-lookup"><span data-stu-id="da2c3-146">-Confirm</span></span>
<span data-ttu-id="da2c3-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="da2c3-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da2c3-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da2c3-148">-WhatIf</span></span>
<span data-ttu-id="da2c3-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="da2c3-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da2c3-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="da2c3-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da2c3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da2c3-151">CommonParameters</span></span>
<span data-ttu-id="da2c3-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da2c3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da2c3-153">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="da2c3-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da2c3-154">輸入</span><span class="sxs-lookup"><span data-stu-id="da2c3-154">INPUTS</span></span>

## <span data-ttu-id="da2c3-155">輸出</span><span class="sxs-lookup"><span data-stu-id="da2c3-155">OUTPUTS</span></span>

### <span data-ttu-id="da2c3-156">IFirewallRule （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="da2c3-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="da2c3-157">筆記</span><span class="sxs-lookup"><span data-stu-id="da2c3-157">NOTES</span></span>

<span data-ttu-id="da2c3-158">別名</span><span class="sxs-lookup"><span data-stu-id="da2c3-158">ALIASES</span></span>

## <span data-ttu-id="da2c3-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="da2c3-159">RELATED LINKS</span></span>

