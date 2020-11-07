---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
ms.openlocfilehash: 4fd7f894ea9a338addaae409df683b9bc003cd8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792438"
---
# <span data-ttu-id="47cce-101">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="47cce-101">New-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="47cce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47cce-102">SYNOPSIS</span></span>
<span data-ttu-id="47cce-103">建立 SQL 資料庫伺服器的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="47cce-103">Creates a firewall rule for a SQL Database server.</span></span>

## <span data-ttu-id="47cce-104">句法</span><span class="sxs-lookup"><span data-stu-id="47cce-104">SYNTAX</span></span>

### <span data-ttu-id="47cce-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="47cce-105">UserSpecifiedRuleSet</span></span>
```
New-AzSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47cce-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="47cce-106">AzureIpRuleSet</span></span>
```
New-AzSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47cce-107">說明</span><span class="sxs-lookup"><span data-stu-id="47cce-107">DESCRIPTION</span></span>
<span data-ttu-id="47cce-108">**AzSqlServerFirewallRule** Cmdlet 會為指定的 Azure SQL 資料庫伺服器建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="47cce-108">The **New-AzSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="47cce-109">示例</span><span class="sxs-lookup"><span data-stu-id="47cce-109">EXAMPLES</span></span>

### <span data-ttu-id="47cce-110">範例1：建立防火牆規則</span><span class="sxs-lookup"><span data-stu-id="47cce-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="47cce-111">這個命令會在名為 Server01 的伺服器上建立名為 Rule01 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="47cce-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="47cce-112">規則包含指定的開始和結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="47cce-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="47cce-113">範例2：建立可讓所有 Azure IP 位址存取伺服器的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="47cce-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="47cce-114">這個命令會在名為 [ResourceGroup01] 的資源群組所屬的伺服器上建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="47cce-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="47cce-115">由於使用了 *AllowAllAzureIPs* 參數，因此防火牆規則可讓所有的 Azure IP 位址存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="47cce-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="47cce-116">參數</span><span class="sxs-lookup"><span data-stu-id="47cce-116">PARAMETERS</span></span>

### <span data-ttu-id="47cce-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="47cce-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="47cce-118">表示此防火牆規則允許所有 Azure IP 位址存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="47cce-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="47cce-119">如果您想要使用 *FirewallRuleName* 、 *StartIpAddress* 和 *EndIpAddress* 參數，則無法使用此參數。</span><span class="sxs-lookup"><span data-stu-id="47cce-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="47cce-120">如果您想要允許 Azure Ip 存取伺服器，應該在不使用 *FirewallRuleName* 、 *StartIpAddress* 和 *EndIpAddress* 參數的個別 Cmdlet 呼叫中使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="47cce-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

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

### <span data-ttu-id="47cce-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47cce-121">-DefaultProfile</span></span>
<span data-ttu-id="47cce-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="47cce-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47cce-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="47cce-123">-EndIpAddress</span></span>
<span data-ttu-id="47cce-124">指定此規則 IP 位址範圍的結束值。</span><span class="sxs-lookup"><span data-stu-id="47cce-124">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="47cce-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="47cce-125">-FirewallRuleName</span></span>
<span data-ttu-id="47cce-126">指定新防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="47cce-126">Specifies the name of the new firewall rule.</span></span>

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

### <span data-ttu-id="47cce-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47cce-127">-ResourceGroupName</span></span>
<span data-ttu-id="47cce-128">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="47cce-128">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="47cce-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="47cce-129">-ServerName</span></span>
<span data-ttu-id="47cce-130">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="47cce-130">Specifies the name of a server.</span></span>
<span data-ttu-id="47cce-131">指定 [伺服器名稱]，而不是 [完全限定的 DNS 名稱]。</span><span class="sxs-lookup"><span data-stu-id="47cce-131">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="47cce-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="47cce-132">-StartIpAddress</span></span>
<span data-ttu-id="47cce-133">指定防火牆規則 IP 位址範圍的起始值。</span><span class="sxs-lookup"><span data-stu-id="47cce-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="47cce-134">-確認</span><span class="sxs-lookup"><span data-stu-id="47cce-134">-Confirm</span></span>
<span data-ttu-id="47cce-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="47cce-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47cce-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47cce-136">-WhatIf</span></span>
<span data-ttu-id="47cce-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47cce-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47cce-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47cce-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47cce-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47cce-139">CommonParameters</span></span>
<span data-ttu-id="47cce-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47cce-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47cce-141">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="47cce-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47cce-142">輸入</span><span class="sxs-lookup"><span data-stu-id="47cce-142">INPUTS</span></span>

### <span data-ttu-id="47cce-143">System.object</span><span class="sxs-lookup"><span data-stu-id="47cce-143">System.String</span></span>

## <span data-ttu-id="47cce-144">輸出</span><span class="sxs-lookup"><span data-stu-id="47cce-144">OUTPUTS</span></span>

### <span data-ttu-id="47cce-145">AzureSqlServerFirewallRuleModel 中的 [FirewallRule]</span><span class="sxs-lookup"><span data-stu-id="47cce-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="47cce-146">筆記</span><span class="sxs-lookup"><span data-stu-id="47cce-146">NOTES</span></span>

## <span data-ttu-id="47cce-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="47cce-147">RELATED LINKS</span></span>

[<span data-ttu-id="47cce-148">AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="47cce-148">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="47cce-149">移除-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="47cce-149">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="47cce-150">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="47cce-150">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="47cce-151">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="47cce-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


