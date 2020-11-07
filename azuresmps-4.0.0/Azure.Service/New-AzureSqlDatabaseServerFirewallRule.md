---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967415"
---
# <span data-ttu-id="788d4-101">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="788d4-101">New-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="788d4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="788d4-102">SYNOPSIS</span></span>
<span data-ttu-id="788d4-103">在 Azure SQL Database Server 中建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="788d4-103">Creates a firewall rule in Azure SQL Database Server.</span></span>

## <span data-ttu-id="788d4-104">句法</span><span class="sxs-lookup"><span data-stu-id="788d4-104">SYNTAX</span></span>

### <span data-ttu-id="788d4-105">IpRange (預設) </span><span class="sxs-lookup"><span data-stu-id="788d4-105">IpRange (Default)</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="788d4-106">AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="788d4-106">AllowAllAzureServices</span></span>
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="788d4-107">說明</span><span class="sxs-lookup"><span data-stu-id="788d4-107">DESCRIPTION</span></span>
<span data-ttu-id="788d4-108">**AzureSqlDatabaseServerFirewallRule** Cmdlet 會在目前訂閱中指定的 Azure SQL Database Server 實例中建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="788d4-108">The **New-AzureSqlDatabaseServerFirewallRule** cmdlet creates a firewall rule in the specified instance of Azure SQL Database Server in the current subscription.</span></span>

<span data-ttu-id="788d4-109">使用 *StartIpAddress* 和 *EndIpAddress* 參數來指定此規則允許連線至 Azure SQL 資料庫伺服器的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="788d4-109">Use the *StartIpAddress* and *EndIpAddress* parameters to specify a range of IP addresses that this rule allows to connect to the Azure SQL Database server.</span></span>

<span data-ttu-id="788d4-110">指定 *AllowAllAzureServices* 參數，以建立允許 Azure 連線至伺服器的規則。</span><span class="sxs-lookup"><span data-stu-id="788d4-110">Specify the *AllowAllAzureServices* parameter to create a rule that allows Azure connections to the server.</span></span>
<span data-ttu-id="788d4-111">規則的開始和結束 IP 位址值0.0.0.0。</span><span class="sxs-lookup"><span data-stu-id="788d4-111">The rule has starting and ending IP address values of 0.0.0.0.</span></span>
<span data-ttu-id="788d4-112">如果您沒有指定防火牆規則名稱，此 Cmdlet 會指派預設名稱 AllowAllAzureServices。</span><span class="sxs-lookup"><span data-stu-id="788d4-112">If you do not specify a firewall rule name, this cmdlet assigns the default name AllowAllAzureServices.</span></span>

## <span data-ttu-id="788d4-113">示例</span><span class="sxs-lookup"><span data-stu-id="788d4-113">EXAMPLES</span></span>

### <span data-ttu-id="788d4-114">範例1：建立防火牆規則</span><span class="sxs-lookup"><span data-stu-id="788d4-114">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

<span data-ttu-id="788d4-115">這個命令會在名為 lpqd0zbr8y 的 Azure SQL 資料庫伺服器上建立防火牆規則 FirewallRule24。</span><span class="sxs-lookup"><span data-stu-id="788d4-115">This command creates a firewall rule FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="788d4-116">命令會指定 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="788d4-116">The command specifies an IP address range.</span></span>

### <span data-ttu-id="788d4-117">範例2：建立允許所有 Azure 服務的規則</span><span class="sxs-lookup"><span data-stu-id="788d4-117">Example 2: Create a rule that allows all Azure services</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

<span data-ttu-id="788d4-118">這個命令會在伺服器上建立名為 AzureConnections 的防火牆規則，該伺服器可允許 Azure 連線。</span><span class="sxs-lookup"><span data-stu-id="788d4-118">This command creates a firewall rule named AzureConnections on the server named lpqd0zbr8y that allows Azure connections.</span></span>

### <span data-ttu-id="788d4-119">範例3：建立允許所有使用預設名稱的 Azure 服務的規則建立規則，以允許所有使用預設名稱的 Azure 服務</span><span class="sxs-lookup"><span data-stu-id="788d4-119">Example 3: Create a rule that allows all Azure services that uses the default name Create a rule that allows all Azure services that uses the default name</span></span>
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

<span data-ttu-id="788d4-120">這個命令會在名為 lpqd0zbr8y 的指定伺服器上建立一個防火牆規則，以允許 Azure 連線。</span><span class="sxs-lookup"><span data-stu-id="788d4-120">This command creates a firewall rule on the specified server named lpqd0zbr8y that allows Azure connections.</span></span>
<span data-ttu-id="788d4-121">該命令會指派預設規則名稱 AllowAllAzureServices。</span><span class="sxs-lookup"><span data-stu-id="788d4-121">The command assigns the default rule name AllowAllAzureServices.</span></span>

## <span data-ttu-id="788d4-122">參數</span><span class="sxs-lookup"><span data-stu-id="788d4-122">PARAMETERS</span></span>

### <span data-ttu-id="788d4-123">-AllowAllAzureServices</span><span class="sxs-lookup"><span data-stu-id="788d4-123">-AllowAllAzureServices</span></span>
<span data-ttu-id="788d4-124">表示此防火牆規則可讓所有 Azure IP 位址存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="788d4-124">Indicates that this firewall rule enables all Azure IP addresses to access the server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788d4-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="788d4-125">-EndIpAddress</span></span>
<span data-ttu-id="788d4-126">指定此規則 IP 位址範圍的結束值。</span><span class="sxs-lookup"><span data-stu-id="788d4-126">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788d4-127">-Force</span><span class="sxs-lookup"><span data-stu-id="788d4-127">-Force</span></span>
<span data-ttu-id="788d4-128">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="788d4-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788d4-129">-設定檔</span><span class="sxs-lookup"><span data-stu-id="788d4-129">-Profile</span></span>
<span data-ttu-id="788d4-130">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="788d4-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="788d4-131">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="788d4-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788d4-132">-RuleName</span><span class="sxs-lookup"><span data-stu-id="788d4-132">-RuleName</span></span>
<span data-ttu-id="788d4-133">指定新防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="788d4-133">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788d4-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="788d4-134">-ServerName</span></span>
<span data-ttu-id="788d4-135">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="788d4-135">Specifies the name of a server.</span></span>
<span data-ttu-id="788d4-136">這個 Cmdlet 會在此 Cmdlet 指定的伺服器上建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="788d4-136">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="788d4-137">指定 [伺服器名稱]，而不是 [完全限定的 DNS 名稱]。</span><span class="sxs-lookup"><span data-stu-id="788d4-137">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="788d4-138">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="788d4-138">-StartIpAddress</span></span>
<span data-ttu-id="788d4-139">指定防火牆規則 IP 位址範圍的起始值。</span><span class="sxs-lookup"><span data-stu-id="788d4-139">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788d4-140">-確認</span><span class="sxs-lookup"><span data-stu-id="788d4-140">-Confirm</span></span>
<span data-ttu-id="788d4-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="788d4-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788d4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="788d4-142">-WhatIf</span></span>
<span data-ttu-id="788d4-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="788d4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="788d4-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="788d4-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788d4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="788d4-145">CommonParameters</span></span>
<span data-ttu-id="788d4-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="788d4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="788d4-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="788d4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="788d4-148">輸入</span><span class="sxs-lookup"><span data-stu-id="788d4-148">INPUTS</span></span>

## <span data-ttu-id="788d4-149">輸出</span><span class="sxs-lookup"><span data-stu-id="788d4-149">OUTPUTS</span></span>

### <span data-ttu-id="788d4-150">WindowsAzure. SqlDatabase. SqlDatabaseServerFirewallRuleCoNtext</span><span class="sxs-lookup"><span data-stu-id="788d4-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="788d4-151">筆記</span><span class="sxs-lookup"><span data-stu-id="788d4-151">NOTES</span></span>

## <span data-ttu-id="788d4-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="788d4-152">RELATED LINKS</span></span>

[<span data-ttu-id="788d4-153">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="788d4-153">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="788d4-154">建立防火牆規則</span><span class="sxs-lookup"><span data-stu-id="788d4-154">Create Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[<span data-ttu-id="788d4-155">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="788d4-155">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="788d4-156">AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="788d4-156">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="788d4-157">移除-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="788d4-157">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="788d4-158">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="788d4-158">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


