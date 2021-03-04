---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: e06447fc72dc8dc3bc09768360039a561b1b862a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913178"
---
# <span data-ttu-id="1cc19-101">New-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1cc19-101">New-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="1cc19-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1cc19-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc19-103">為 MySQL 彈性伺服器建立新的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="1cc19-103">Creates a new firewall rule for MySQL flexible server</span></span>

## <span data-ttu-id="1cc19-104">語法</span><span class="sxs-lookup"><span data-stu-id="1cc19-104">SYNTAX</span></span>

### <span data-ttu-id="1cc19-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="1cc19-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1cc19-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="1cc19-106">AllowAll</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1cc19-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="1cc19-107">ClientIPAddress</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1cc19-108">描述</span><span class="sxs-lookup"><span data-stu-id="1cc19-108">DESCRIPTION</span></span>
<span data-ttu-id="1cc19-109">為 MySQL 彈性伺服器建立新的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="1cc19-109">Creates a new firewall rule for MySQL flexible server</span></span>

## <span data-ttu-id="1cc19-110">例子</span><span class="sxs-lookup"><span data-stu-id="1cc19-110">EXAMPLES</span></span>

### <span data-ttu-id="1cc19-111">範例 1：建立新的 MySql 伺服器防火牆規則</span><span class="sxs-lookup"><span data-stu-id="1cc19-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name              StartIPAddress EndIPAddress
----------------- -------------- ------------
firewallrule-test 0.0.0.0        0.0.0.1
```

<span data-ttu-id="1cc19-112">此 Cmdlet 會建立 MySql 伺服器防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="1cc19-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="1cc19-113">範例 2：使用 -ClientIPAddress 建立新 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="1cc19-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="1cc19-114">此 Cmdlet 會使用 -ClientIPAddress 建立 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="1cc19-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="1cc19-115">範例 3：建立新 MySql 防火牆規則以允許所有 IP</span><span class="sxs-lookup"><span data-stu-id="1cc19-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="1cc19-116">此 Cmdlet 會建立新的 MySql 防火牆規則，以允許所有 IP。</span><span class="sxs-lookup"><span data-stu-id="1cc19-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="1cc19-117">參數</span><span class="sxs-lookup"><span data-stu-id="1cc19-117">PARAMETERS</span></span>

### <span data-ttu-id="1cc19-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="1cc19-118">-AllowAll</span></span>
<span data-ttu-id="1cc19-119">展示以允許所有範圍 IP，範圍從 0.0.0.0 到 255.255.255.255。</span><span class="sxs-lookup"><span data-stu-id="1cc19-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="1cc19-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1cc19-120">-AsJob</span></span>
<span data-ttu-id="1cc19-121">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="1cc19-121">Run the command as a job</span></span>

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

### <span data-ttu-id="1cc19-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="1cc19-122">-ClientIPAddress</span></span>
<span data-ttu-id="1cc19-123">用戶端指定的伺服器防火牆規則之單一 IP。</span><span class="sxs-lookup"><span data-stu-id="1cc19-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="1cc19-124">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="1cc19-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="1cc19-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc19-125">-DefaultProfile</span></span>
<span data-ttu-id="1cc19-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1cc19-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cc19-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="1cc19-127">-EndIPAddress</span></span>
<span data-ttu-id="1cc19-128">伺服器防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1cc19-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="1cc19-129">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="1cc19-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="1cc19-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="1cc19-130">-Name</span></span>
<span data-ttu-id="1cc19-131">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="1cc19-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="1cc19-132">如果未指定，則預設為未定義。</span><span class="sxs-lookup"><span data-stu-id="1cc19-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="1cc19-133">如果 AllowAll 存在，預設名稱為 AllowAll_yyyy-MM-dd_HH-mm-ss。</span><span class="sxs-lookup"><span data-stu-id="1cc19-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="1cc19-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1cc19-134">-NoWait</span></span>
<span data-ttu-id="1cc19-135">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="1cc19-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1cc19-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cc19-136">-ResourceGroupName</span></span>
<span data-ttu-id="1cc19-137">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1cc19-137">The name of the resource group.</span></span>
<span data-ttu-id="1cc19-138">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="1cc19-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1cc19-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1cc19-139">-ServerName</span></span>
<span data-ttu-id="1cc19-140">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1cc19-140">The name of the server.</span></span>

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

### <span data-ttu-id="1cc19-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="1cc19-141">-StartIPAddress</span></span>
<span data-ttu-id="1cc19-142">伺服器防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1cc19-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="1cc19-143">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="1cc19-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="1cc19-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1cc19-144">-SubscriptionId</span></span>
<span data-ttu-id="1cc19-145">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1cc19-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1cc19-146">-確認</span><span class="sxs-lookup"><span data-stu-id="1cc19-146">-Confirm</span></span>
<span data-ttu-id="1cc19-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1cc19-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc19-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc19-148">-WhatIf</span></span>
<span data-ttu-id="1cc19-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1cc19-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cc19-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1cc19-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cc19-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc19-151">CommonParameters</span></span>
<span data-ttu-id="1cc19-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1cc19-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc19-153">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cc19-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc19-154">輸入</span><span class="sxs-lookup"><span data-stu-id="1cc19-154">INPUTS</span></span>

## <span data-ttu-id="1cc19-155">輸出</span><span class="sxs-lookup"><span data-stu-id="1cc19-155">OUTPUTS</span></span>

### <span data-ttu-id="1cc19-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1cc19-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="1cc19-157">筆記</span><span class="sxs-lookup"><span data-stu-id="1cc19-157">NOTES</span></span>

<span data-ttu-id="1cc19-158">別名</span><span class="sxs-lookup"><span data-stu-id="1cc19-158">ALIASES</span></span>

## <span data-ttu-id="1cc19-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="1cc19-159">RELATED LINKS</span></span>

