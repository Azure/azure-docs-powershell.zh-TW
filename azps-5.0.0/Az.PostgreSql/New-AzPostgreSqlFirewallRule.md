---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: bafd0e20530198da87c1fa3ece36905e73307a42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139016"
---
# <span data-ttu-id="96a5c-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="96a5c-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="96a5c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="96a5c-103">建立新的防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="96a5c-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="96a5c-104">句法</span><span class="sxs-lookup"><span data-stu-id="96a5c-104">SYNTAX</span></span>

### <span data-ttu-id="96a5c-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="96a5c-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="96a5c-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="96a5c-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="96a5c-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="96a5c-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="96a5c-108">說明</span><span class="sxs-lookup"><span data-stu-id="96a5c-108">DESCRIPTION</span></span>
<span data-ttu-id="96a5c-109">建立新的防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="96a5c-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="96a5c-110">示例</span><span class="sxs-lookup"><span data-stu-id="96a5c-110">EXAMPLES</span></span>

### <span data-ttu-id="96a5c-111">範例1：建立新的 PostgreSql 伺服器防火牆規則</span><span class="sxs-lookup"><span data-stu-id="96a5c-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="96a5c-112">這個 Cmdlet 會建立 PostgreSql 伺服器防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="96a5c-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="96a5c-113">範例2：使用-ClientIPAddress 建立新的 PostgreSql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="96a5c-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="96a5c-114">這個 Cmdlet 會使用-ClientIPAddress 建立 PostgreSql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="96a5c-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="96a5c-115">範例3：建立新的 PostgreSql 防火牆規則，以允許所有 Ip</span><span class="sxs-lookup"><span data-stu-id="96a5c-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="96a5c-116">這個 Cmdlet 會建立新的 PostgreSql 防火牆規則，以允許所有的 Ip。</span><span class="sxs-lookup"><span data-stu-id="96a5c-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="96a5c-117">參數</span><span class="sxs-lookup"><span data-stu-id="96a5c-117">PARAMETERS</span></span>

### <span data-ttu-id="96a5c-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="96a5c-118">-AllowAll</span></span>
<span data-ttu-id="96a5c-119">[提供] 可允許所有範圍的 Ip （從0.0.0.0 到255.255.255.255）。</span><span class="sxs-lookup"><span data-stu-id="96a5c-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="96a5c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96a5c-120">-AsJob</span></span>
<span data-ttu-id="96a5c-121">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="96a5c-121">Run the command as a job</span></span>

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

### <span data-ttu-id="96a5c-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="96a5c-122">-ClientIPAddress</span></span>
<span data-ttu-id="96a5c-123">用戶端指定的伺服器防火牆規則單一 IP。</span><span class="sxs-lookup"><span data-stu-id="96a5c-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="96a5c-124">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="96a5c-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="96a5c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a5c-125">-DefaultProfile</span></span>
<span data-ttu-id="96a5c-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96a5c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96a5c-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="96a5c-127">-EndIPAddress</span></span>
<span data-ttu-id="96a5c-128">伺服器防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="96a5c-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="96a5c-129">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="96a5c-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="96a5c-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="96a5c-130">-Name</span></span>
<span data-ttu-id="96a5c-131">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="96a5c-131">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="96a5c-132">-NoWait</span><span class="sxs-lookup"><span data-stu-id="96a5c-132">-NoWait</span></span>
<span data-ttu-id="96a5c-133">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="96a5c-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="96a5c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96a5c-134">-ResourceGroupName</span></span>
<span data-ttu-id="96a5c-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="96a5c-135">The name of the resource group.</span></span>
<span data-ttu-id="96a5c-136">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="96a5c-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="96a5c-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="96a5c-137">-ServerName</span></span>
<span data-ttu-id="96a5c-138">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="96a5c-138">The name of the server.</span></span>

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

### <span data-ttu-id="96a5c-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="96a5c-139">-StartIPAddress</span></span>
<span data-ttu-id="96a5c-140">伺服器防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="96a5c-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="96a5c-141">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="96a5c-141">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="96a5c-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96a5c-142">-SubscriptionId</span></span>
<span data-ttu-id="96a5c-143">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="96a5c-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="96a5c-144">-確認</span><span class="sxs-lookup"><span data-stu-id="96a5c-144">-Confirm</span></span>
<span data-ttu-id="96a5c-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="96a5c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96a5c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a5c-146">-WhatIf</span></span>
<span data-ttu-id="96a5c-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96a5c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96a5c-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96a5c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96a5c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a5c-149">CommonParameters</span></span>
<span data-ttu-id="96a5c-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96a5c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a5c-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="96a5c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a5c-152">輸入</span><span class="sxs-lookup"><span data-stu-id="96a5c-152">INPUTS</span></span>

## <span data-ttu-id="96a5c-153">輸出</span><span class="sxs-lookup"><span data-stu-id="96a5c-153">OUTPUTS</span></span>

### <span data-ttu-id="96a5c-154">IFirewallRule （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="96a5c-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="96a5c-155">筆記</span><span class="sxs-lookup"><span data-stu-id="96a5c-155">NOTES</span></span>

<span data-ttu-id="96a5c-156">別名</span><span class="sxs-lookup"><span data-stu-id="96a5c-156">ALIASES</span></span>

## <span data-ttu-id="96a5c-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="96a5c-157">RELATED LINKS</span></span>

