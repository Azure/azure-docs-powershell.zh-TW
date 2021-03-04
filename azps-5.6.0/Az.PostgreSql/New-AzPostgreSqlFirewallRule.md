---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 7ba5a72d161f07ae55669ddfa9d0e399d7cf81ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915270"
---
# <span data-ttu-id="0f517-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0f517-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="0f517-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0f517-102">SYNOPSIS</span></span>
<span data-ttu-id="0f517-103">建立新防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="0f517-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="0f517-104">語法</span><span class="sxs-lookup"><span data-stu-id="0f517-104">SYNTAX</span></span>

### <span data-ttu-id="0f517-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="0f517-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0f517-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="0f517-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0f517-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="0f517-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0f517-108">描述</span><span class="sxs-lookup"><span data-stu-id="0f517-108">DESCRIPTION</span></span>
<span data-ttu-id="0f517-109">建立新防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="0f517-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="0f517-110">例子</span><span class="sxs-lookup"><span data-stu-id="0f517-110">EXAMPLES</span></span>

### <span data-ttu-id="0f517-111">範例 1：建立新的 PostgreSql 伺服器防火牆規則</span><span class="sxs-lookup"><span data-stu-id="0f517-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="0f517-112">此 Cmdlet 會建立 PostgreSql 伺服器防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="0f517-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="0f517-113">範例 2：使用 -ClientIPAddress 建立一個新的 PostgreSql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="0f517-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="0f517-114">此 Cmdlet 會使用 -ClientIPAddress 建立 PostgreSql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="0f517-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="0f517-115">範例 3：建立新 PostgreSql 防火牆規則以允許所有 IP</span><span class="sxs-lookup"><span data-stu-id="0f517-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="0f517-116">此 Cmdlet 會建立一個新的 PostgreSql 防火牆規則，以允許所有 IP。</span><span class="sxs-lookup"><span data-stu-id="0f517-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="0f517-117">參數</span><span class="sxs-lookup"><span data-stu-id="0f517-117">PARAMETERS</span></span>

### <span data-ttu-id="0f517-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="0f517-118">-AllowAll</span></span>
<span data-ttu-id="0f517-119">展示以允許所有範圍 IP，範圍從 0.0.0.0 到 255.255.255.255。</span><span class="sxs-lookup"><span data-stu-id="0f517-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="0f517-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f517-120">-AsJob</span></span>
<span data-ttu-id="0f517-121">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="0f517-121">Run the command as a job</span></span>

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

### <span data-ttu-id="0f517-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="0f517-122">-ClientIPAddress</span></span>
<span data-ttu-id="0f517-123">用戶端指定的伺服器防火牆規則之單一 IP。</span><span class="sxs-lookup"><span data-stu-id="0f517-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="0f517-124">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="0f517-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0f517-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f517-125">-DefaultProfile</span></span>
<span data-ttu-id="0f517-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f517-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f517-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="0f517-127">-EndIPAddress</span></span>
<span data-ttu-id="0f517-128">伺服器防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="0f517-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="0f517-129">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="0f517-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0f517-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="0f517-130">-Name</span></span>
<span data-ttu-id="0f517-131">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f517-131">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="0f517-132">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0f517-132">-NoWait</span></span>
<span data-ttu-id="0f517-133">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="0f517-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0f517-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f517-134">-ResourceGroupName</span></span>
<span data-ttu-id="0f517-135">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f517-135">The name of the resource group.</span></span>
<span data-ttu-id="0f517-136">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="0f517-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0f517-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0f517-137">-ServerName</span></span>
<span data-ttu-id="0f517-138">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="0f517-138">The name of the server.</span></span>

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

### <span data-ttu-id="0f517-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="0f517-139">-StartIPAddress</span></span>
<span data-ttu-id="0f517-140">伺服器防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="0f517-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="0f517-141">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="0f517-141">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0f517-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f517-142">-SubscriptionId</span></span>
<span data-ttu-id="0f517-143">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0f517-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0f517-144">-確認</span><span class="sxs-lookup"><span data-stu-id="0f517-144">-Confirm</span></span>
<span data-ttu-id="0f517-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0f517-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f517-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f517-146">-WhatIf</span></span>
<span data-ttu-id="0f517-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f517-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f517-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f517-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f517-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f517-149">CommonParameters</span></span>
<span data-ttu-id="0f517-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0f517-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f517-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f517-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f517-152">輸入</span><span class="sxs-lookup"><span data-stu-id="0f517-152">INPUTS</span></span>

## <span data-ttu-id="0f517-153">輸出</span><span class="sxs-lookup"><span data-stu-id="0f517-153">OUTPUTS</span></span>

### <span data-ttu-id="0f517-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0f517-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="0f517-155">筆記</span><span class="sxs-lookup"><span data-stu-id="0f517-155">NOTES</span></span>

<span data-ttu-id="0f517-156">別名</span><span class="sxs-lookup"><span data-stu-id="0f517-156">ALIASES</span></span>

## <span data-ttu-id="0f517-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f517-157">RELATED LINKS</span></span>

