---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 036628943afc8b2c5f07b30f2db14f27229364c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127725"
---
# <span data-ttu-id="54509-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="54509-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="54509-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54509-102">SYNOPSIS</span></span>
<span data-ttu-id="54509-103">建立新的防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="54509-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="54509-104">句法</span><span class="sxs-lookup"><span data-stu-id="54509-104">SYNTAX</span></span>

### <span data-ttu-id="54509-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="54509-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="54509-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="54509-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="54509-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="54509-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="54509-108">說明</span><span class="sxs-lookup"><span data-stu-id="54509-108">DESCRIPTION</span></span>
<span data-ttu-id="54509-109">建立新的防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="54509-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="54509-110">示例</span><span class="sxs-lookup"><span data-stu-id="54509-110">EXAMPLES</span></span>

### <span data-ttu-id="54509-111">範例1：建立新的 MySql 伺服器防火牆規則</span><span class="sxs-lookup"><span data-stu-id="54509-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="54509-112">這個 Cmdlet 會建立 MySql 伺服器防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="54509-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="54509-113">範例2：使用-ClientIPAddress 建立新的 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="54509-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="54509-114">這個 Cmdlet 會使用-ClientIPAddress 建立 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="54509-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="54509-115">範例3：建立新的 MySql 防火牆規則，以允許所有 Ip</span><span class="sxs-lookup"><span data-stu-id="54509-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="54509-116">這個 Cmdlet 會建立新的 MySql 防火牆規則，以允許所有的 Ip。</span><span class="sxs-lookup"><span data-stu-id="54509-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="54509-117">參數</span><span class="sxs-lookup"><span data-stu-id="54509-117">PARAMETERS</span></span>

### <span data-ttu-id="54509-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="54509-118">-AllowAll</span></span>
<span data-ttu-id="54509-119">[提供] 可允許所有範圍的 Ip （從0.0.0.0 到255.255.255.255）。</span><span class="sxs-lookup"><span data-stu-id="54509-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="54509-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54509-120">-AsJob</span></span>
<span data-ttu-id="54509-121">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="54509-121">Run the command as a job</span></span>

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

### <span data-ttu-id="54509-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="54509-122">-ClientIPAddress</span></span>
<span data-ttu-id="54509-123">用戶端指定的伺服器防火牆規則單一 IP。</span><span class="sxs-lookup"><span data-stu-id="54509-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="54509-124">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="54509-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="54509-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54509-125">-DefaultProfile</span></span>
<span data-ttu-id="54509-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54509-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54509-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="54509-127">-EndIPAddress</span></span>
<span data-ttu-id="54509-128">伺服器防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="54509-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="54509-129">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="54509-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="54509-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="54509-130">-Name</span></span>
<span data-ttu-id="54509-131">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="54509-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="54509-132">如果未指定，則預設值為未定義。</span><span class="sxs-lookup"><span data-stu-id="54509-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="54509-133">如果 AllowAll 存在，預設名稱是 AllowAll_yyyy MM dd_HH-ss。</span><span class="sxs-lookup"><span data-stu-id="54509-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="54509-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="54509-134">-NoWait</span></span>
<span data-ttu-id="54509-135">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="54509-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="54509-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54509-136">-ResourceGroupName</span></span>
<span data-ttu-id="54509-137">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54509-137">The name of the resource group.</span></span>
<span data-ttu-id="54509-138">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="54509-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="54509-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="54509-139">-ServerName</span></span>
<span data-ttu-id="54509-140">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="54509-140">The name of the server.</span></span>

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

### <span data-ttu-id="54509-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="54509-141">-StartIPAddress</span></span>
<span data-ttu-id="54509-142">伺服器防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="54509-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="54509-143">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="54509-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="54509-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54509-144">-SubscriptionId</span></span>
<span data-ttu-id="54509-145">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="54509-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="54509-146">-確認</span><span class="sxs-lookup"><span data-stu-id="54509-146">-Confirm</span></span>
<span data-ttu-id="54509-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="54509-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54509-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54509-148">-WhatIf</span></span>
<span data-ttu-id="54509-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54509-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54509-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54509-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54509-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54509-151">CommonParameters</span></span>
<span data-ttu-id="54509-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54509-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54509-153">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="54509-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54509-154">輸入</span><span class="sxs-lookup"><span data-stu-id="54509-154">INPUTS</span></span>

## <span data-ttu-id="54509-155">輸出</span><span class="sxs-lookup"><span data-stu-id="54509-155">OUTPUTS</span></span>

### <span data-ttu-id="54509-156">IFirewallRule 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="54509-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="54509-157">筆記</span><span class="sxs-lookup"><span data-stu-id="54509-157">NOTES</span></span>

<span data-ttu-id="54509-158">別名</span><span class="sxs-lookup"><span data-stu-id="54509-158">ALIASES</span></span>

## <span data-ttu-id="54509-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="54509-159">RELATED LINKS</span></span>
