---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F311A7A9-5FE9-4E81-8FF1-8E3A02F2BF4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce9d384a5dd7f57fb4444fb173864ec5859b3a81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967309"
---
# <span data-ttu-id="b6bfc-101">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b6bfc-101">Set-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="b6bfc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="b6bfc-103">修改 Azure SQL 資料庫伺服器中的現有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-103">Modifies an existing firewall rule in an Azure SQL Database Server.</span></span>

## <span data-ttu-id="b6bfc-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6bfc-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6bfc-105">說明</span><span class="sxs-lookup"><span data-stu-id="b6bfc-105">DESCRIPTION</span></span>
<span data-ttu-id="b6bfc-106">**AzureSqlDatabaseServerFirewallRule** Cmdlet 會修改 Azure SQL Database Server 指定實例中現有防火牆規則的起始 ip 位址和結束 ip 位址值。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-106">The **Set-AzureSqlDatabaseServerFirewallRule** cmdlet modifies the start IP address and end IP address values of an existing firewall rule in the specified instance of Azure SQL Database Server.</span></span>

## <span data-ttu-id="b6bfc-107">示例</span><span class="sxs-lookup"><span data-stu-id="b6bfc-107">EXAMPLES</span></span>

### <span data-ttu-id="b6bfc-108">範例1：修改防火牆規則</span><span class="sxs-lookup"><span data-stu-id="b6bfc-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\> Set-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.2 -EndIpAddress 10.1.1.4
```

<span data-ttu-id="b6bfc-109">這個命令會修改名為 lpqd0zbr8y 之 Azure SQL Database server 上名為 FirewallRule24 的防火牆規則的開始 IP 位址和結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-109">This command modifies the start IP address and end IP address of the firewall rule named FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="b6bfc-110">參數</span><span class="sxs-lookup"><span data-stu-id="b6bfc-110">PARAMETERS</span></span>

### <span data-ttu-id="b6bfc-111">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="b6bfc-111">-EndIpAddress</span></span>
<span data-ttu-id="b6bfc-112">指定此規則 IP 位址範圍的結束值。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-112">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bfc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b6bfc-113">-Force</span></span>
<span data-ttu-id="b6bfc-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6bfc-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b6bfc-115">-Profile</span></span>
<span data-ttu-id="b6bfc-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6bfc-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6bfc-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="b6bfc-118">-RuleName</span></span>
<span data-ttu-id="b6bfc-119">指定此 Cmdlet 修改的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-119">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b6bfc-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b6bfc-120">-ServerName</span></span>
<span data-ttu-id="b6bfc-121">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-121">Specifies the name of a server.</span></span>
<span data-ttu-id="b6bfc-122">這個 Cmdlet 會在此 Cmdlet 指定的伺服器上建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-122">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="b6bfc-123">指定 [伺服器名稱]，而不是 [完全限定的 DNS 名稱]。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="b6bfc-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="b6bfc-124">-StartIpAddress</span></span>
<span data-ttu-id="b6bfc-125">指定防火牆規則 IP 位址範圍的起始值。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-125">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bfc-126">-確認</span><span class="sxs-lookup"><span data-stu-id="b6bfc-126">-Confirm</span></span>
<span data-ttu-id="b6bfc-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6bfc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6bfc-128">-WhatIf</span></span>
<span data-ttu-id="b6bfc-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6bfc-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6bfc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6bfc-131">CommonParameters</span></span>
<span data-ttu-id="b6bfc-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6bfc-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b6bfc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6bfc-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b6bfc-134">INPUTS</span></span>

### <span data-ttu-id="b6bfc-135">WindowsAzure. SqlDatabase. SqlDatabaseServerFirewallRuleCoNtext</span><span class="sxs-lookup"><span data-stu-id="b6bfc-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="b6bfc-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b6bfc-136">OUTPUTS</span></span>

### <span data-ttu-id="b6bfc-137">WindowsAzure. SqlDatabase. SqlDatabaseServerFirewallRuleCoNtext</span><span class="sxs-lookup"><span data-stu-id="b6bfc-137">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="b6bfc-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b6bfc-138">NOTES</span></span>

## <span data-ttu-id="b6bfc-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6bfc-139">RELATED LINKS</span></span>

[<span data-ttu-id="b6bfc-140">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="b6bfc-140">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="b6bfc-141">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="b6bfc-141">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="b6bfc-142">設定防火牆規則</span><span class="sxs-lookup"><span data-stu-id="b6bfc-142">Set Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505707.aspx)

[<span data-ttu-id="b6bfc-143">AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b6bfc-143">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="b6bfc-144">新-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b6bfc-144">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="b6bfc-145">移除-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b6bfc-145">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)


