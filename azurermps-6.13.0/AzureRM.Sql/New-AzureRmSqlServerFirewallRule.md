---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: e5d835d0dbe31728a0b524c95b4473a94bb42a20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445411"
---
# <span data-ttu-id="d306b-101">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d306b-101">New-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="d306b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d306b-102">SYNOPSIS</span></span>
<span data-ttu-id="d306b-103">建立 SQL 資料庫伺服器的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d306b-103">Creates a firewall rule for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d306b-104">句法</span><span class="sxs-lookup"><span data-stu-id="d306b-104">SYNTAX</span></span>

### <span data-ttu-id="d306b-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="d306b-105">UserSpecifiedRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d306b-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="d306b-106">AzureIpRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d306b-107">說明</span><span class="sxs-lookup"><span data-stu-id="d306b-107">DESCRIPTION</span></span>
<span data-ttu-id="d306b-108">**AzureRmSqlServerFirewallRule** Cmdlet 會為指定的 Azure SQL 資料庫伺服器建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d306b-108">The **New-AzureRmSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="d306b-109">示例</span><span class="sxs-lookup"><span data-stu-id="d306b-109">EXAMPLES</span></span>

### <span data-ttu-id="d306b-110">範例1：建立防火牆規則</span><span class="sxs-lookup"><span data-stu-id="d306b-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="d306b-111">這個命令會在名為 Server01 的伺服器上建立名為 Rule01 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d306b-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="d306b-112">規則包含指定的開始和結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d306b-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="d306b-113">範例2：建立可讓所有 Azure IP 位址存取伺服器的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="d306b-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="d306b-114">這個命令會在名為 [ResourceGroup01] 的資源群組所屬的伺服器上建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d306b-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="d306b-115">由於使用了 *AllowAllAzureIPs* 參數，因此防火牆規則可讓所有的 Azure IP 位址存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="d306b-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="d306b-116">參數</span><span class="sxs-lookup"><span data-stu-id="d306b-116">PARAMETERS</span></span>

### <span data-ttu-id="d306b-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="d306b-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="d306b-118">表示此防火牆規則允許所有 Azure IP 位址存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="d306b-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="d306b-119">如果您想要使用 *FirewallRuleName* 、 *StartIpAddress* 和 *EndIpAddress* 參數，則無法使用此參數。</span><span class="sxs-lookup"><span data-stu-id="d306b-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="d306b-120">如果您想要允許 Azure Ip 存取伺服器，應該在不使用 *FirewallRuleName* 、 *StartIpAddress* 和 *EndIpAddress* 參數的個別 Cmdlet 呼叫中使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="d306b-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

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

### <span data-ttu-id="d306b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d306b-121">-DefaultProfile</span></span>
<span data-ttu-id="d306b-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d306b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d306b-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="d306b-123">-EndIpAddress</span></span>
<span data-ttu-id="d306b-124">指定此規則 IP 位址範圍的結束值。</span><span class="sxs-lookup"><span data-stu-id="d306b-124">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="d306b-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="d306b-125">-FirewallRuleName</span></span>
<span data-ttu-id="d306b-126">指定新防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d306b-126">Specifies the name of the new firewall rule.</span></span>

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

### <span data-ttu-id="d306b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d306b-127">-ResourceGroupName</span></span>
<span data-ttu-id="d306b-128">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d306b-128">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d306b-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d306b-129">-ServerName</span></span>
<span data-ttu-id="d306b-130">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d306b-130">Specifies the name of a server.</span></span>
<span data-ttu-id="d306b-131">指定 [伺服器名稱]，而不是 [完全限定的 DNS 名稱]。</span><span class="sxs-lookup"><span data-stu-id="d306b-131">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="d306b-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="d306b-132">-StartIpAddress</span></span>
<span data-ttu-id="d306b-133">指定防火牆規則 IP 位址範圍的起始值。</span><span class="sxs-lookup"><span data-stu-id="d306b-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="d306b-134">-確認</span><span class="sxs-lookup"><span data-stu-id="d306b-134">-Confirm</span></span>
<span data-ttu-id="d306b-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d306b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d306b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d306b-136">-WhatIf</span></span>
<span data-ttu-id="d306b-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d306b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d306b-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d306b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d306b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d306b-139">CommonParameters</span></span>
<span data-ttu-id="d306b-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d306b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d306b-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d306b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d306b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="d306b-142">INPUTS</span></span>

### <span data-ttu-id="d306b-143">System.object</span><span class="sxs-lookup"><span data-stu-id="d306b-143">System.String</span></span>

## <span data-ttu-id="d306b-144">輸出</span><span class="sxs-lookup"><span data-stu-id="d306b-144">OUTPUTS</span></span>

### <span data-ttu-id="d306b-145">AzureSqlServerFirewallRuleModel 中的 [FirewallRule]</span><span class="sxs-lookup"><span data-stu-id="d306b-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="d306b-146">筆記</span><span class="sxs-lookup"><span data-stu-id="d306b-146">NOTES</span></span>

## <span data-ttu-id="d306b-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d306b-147">RELATED LINKS</span></span>

[<span data-ttu-id="d306b-148">AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d306b-148">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="d306b-149">移除-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d306b-149">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="d306b-150">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d306b-150">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="d306b-151">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="d306b-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


