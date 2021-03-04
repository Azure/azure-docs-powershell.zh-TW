---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
ms.openlocfilehash: 07179b5fb139ba43b341114e2bf597fbbca05ed5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902722"
---
# <span data-ttu-id="097e5-101">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="097e5-101">New-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="097e5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="097e5-102">SYNOPSIS</span></span>
<span data-ttu-id="097e5-103">為 SQL Database 伺服器建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="097e5-103">Creates a firewall rule for a SQL Database server.</span></span>

## <span data-ttu-id="097e5-104">語法</span><span class="sxs-lookup"><span data-stu-id="097e5-104">SYNTAX</span></span>

### <span data-ttu-id="097e5-105">UserSifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="097e5-105">UserSpecifiedRuleSet</span></span>
```
New-AzSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="097e5-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="097e5-106">AzureIpRuleSet</span></span>
```
New-AzSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="097e5-107">描述</span><span class="sxs-lookup"><span data-stu-id="097e5-107">DESCRIPTION</span></span>
<span data-ttu-id="097e5-108">**New-AzSqlServerFirewallRule** Cmdlet 會為指定的 Azure SQL Database 伺服器建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="097e5-108">The **New-AzSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="097e5-109">例子</span><span class="sxs-lookup"><span data-stu-id="097e5-109">EXAMPLES</span></span>

### <span data-ttu-id="097e5-110">範例 1：建立防火牆規則</span><span class="sxs-lookup"><span data-stu-id="097e5-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="097e5-111">此命令會在伺服器上名為 Rule01 的伺服器上建立名為 Rule01 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="097e5-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="097e5-112">規則包含指定的開始與結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="097e5-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="097e5-113">範例 2：建立允許所有 Azure IP 位址存取伺服器的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="097e5-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="097e5-114">此命令會在伺服器上建立一個名為 Server01 的防火牆規則，該防火牆規則屬於名為 ResourceGroup01 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="097e5-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="097e5-115">由於 *使用 AllowAllAzureIPs* 參數，防火牆規則允許所有 Azure IP 位址存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="097e5-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="097e5-116">參數</span><span class="sxs-lookup"><span data-stu-id="097e5-116">PARAMETERS</span></span>

### <span data-ttu-id="097e5-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="097e5-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="097e5-118">表示此防火牆規則允許所有 Azure IP 位址存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="097e5-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="097e5-119">如果您想要使用 *FirewallRuleName、StartIpAddress* 和 *EndIpAddress* 參數，就無法使用此參數。</span><span class="sxs-lookup"><span data-stu-id="097e5-119">You cannot use this parameter if you intend to use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="097e5-120">如果您想要允許 Azure IP 存取伺服器，此參數應該用於不使用 *FirewallRuleName、StartIpAddress* 和 *EndIpAddress* 參數的個別 Cmdlet 呼叫中。</span><span class="sxs-lookup"><span data-stu-id="097e5-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="097e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="097e5-121">-DefaultProfile</span></span>
<span data-ttu-id="097e5-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="097e5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="097e5-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="097e5-123">-EndIpAddress</span></span>
<span data-ttu-id="097e5-124">指定此規則的 IP 位址範圍的結束值。</span><span class="sxs-lookup"><span data-stu-id="097e5-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="097e5-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="097e5-125">-FirewallRuleName</span></span>
<span data-ttu-id="097e5-126">指定新防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="097e5-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="097e5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="097e5-127">-ResourceGroupName</span></span>
<span data-ttu-id="097e5-128">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="097e5-128">Specifies the name of a resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="097e5-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="097e5-129">-ServerName</span></span>
<span data-ttu-id="097e5-130">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="097e5-130">Specifies the name of a server.</span></span>
<span data-ttu-id="097e5-131">指定伺服器名稱，而不是完整 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="097e5-131">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="097e5-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="097e5-132">-StartIpAddress</span></span>
<span data-ttu-id="097e5-133">指定防火牆規則的 IP 位址範圍的起始值。</span><span class="sxs-lookup"><span data-stu-id="097e5-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="097e5-134">-確認</span><span class="sxs-lookup"><span data-stu-id="097e5-134">-Confirm</span></span>
<span data-ttu-id="097e5-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="097e5-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="097e5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="097e5-136">-WhatIf</span></span>
<span data-ttu-id="097e5-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="097e5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="097e5-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="097e5-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="097e5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="097e5-139">CommonParameters</span></span>
<span data-ttu-id="097e5-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="097e5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="097e5-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="097e5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="097e5-142">輸入</span><span class="sxs-lookup"><span data-stu-id="097e5-142">INPUTS</span></span>

### <span data-ttu-id="097e5-143">System.String</span><span class="sxs-lookup"><span data-stu-id="097e5-143">System.String</span></span>

## <span data-ttu-id="097e5-144">輸出</span><span class="sxs-lookup"><span data-stu-id="097e5-144">OUTPUTS</span></span>

### <span data-ttu-id="097e5-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="097e5-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="097e5-146">筆記</span><span class="sxs-lookup"><span data-stu-id="097e5-146">NOTES</span></span>

## <span data-ttu-id="097e5-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="097e5-147">RELATED LINKS</span></span>

[<span data-ttu-id="097e5-148">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="097e5-148">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="097e5-149">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="097e5-149">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="097e5-150">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="097e5-150">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="097e5-151">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="097e5-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


