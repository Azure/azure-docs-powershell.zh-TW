---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383DD041-78DC-4170-9529-1FD6F13BC178
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29cbf01629ef772fc41436f3916a2077c1535329
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967552"
---
# <span data-ttu-id="fda28-101">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fda28-101">Remove-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="fda28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fda28-102">SYNOPSIS</span></span>
<span data-ttu-id="fda28-103">從 Azure SQL 資料庫伺服器移除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="fda28-103">Removes a firewall rule from an Azure SQL Database server.</span></span>

## <span data-ttu-id="fda28-104">句法</span><span class="sxs-lookup"><span data-stu-id="fda28-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fda28-105">說明</span><span class="sxs-lookup"><span data-stu-id="fda28-105">DESCRIPTION</span></span>
<span data-ttu-id="fda28-106">**AzureSqlDatabaseServerFirewallRule** Cmdlet 會從目前訂閱中的 Azure SQL Database Server 實例移除防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="fda28-106">The **Remove-AzureSqlDatabaseServerFirewallRule** cmdlet removes a firewall rule from an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="fda28-107">示例</span><span class="sxs-lookup"><span data-stu-id="fda28-107">EXAMPLES</span></span>

### <span data-ttu-id="fda28-108">範例1：移除規則</span><span class="sxs-lookup"><span data-stu-id="fda28-108">Example 1: Remove a rule</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="fda28-109">這個命令會從 Azure SQL Database server （名為 lpqd0zbr8y）中移除名為 FirewallRule24 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="fda28-109">This command removes the firewall rule named FirewallRule24 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="fda28-110">參數</span><span class="sxs-lookup"><span data-stu-id="fda28-110">PARAMETERS</span></span>

### <span data-ttu-id="fda28-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fda28-111">-Force</span></span>
<span data-ttu-id="fda28-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="fda28-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fda28-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="fda28-113">-Profile</span></span>
<span data-ttu-id="fda28-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="fda28-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fda28-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="fda28-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fda28-116">-RuleName</span><span class="sxs-lookup"><span data-stu-id="fda28-116">-RuleName</span></span>
<span data-ttu-id="fda28-117">指定此 Cmdlet 移除的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="fda28-117">Specifies the name of the firewall rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fda28-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fda28-118">-ServerName</span></span>
<span data-ttu-id="fda28-119">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="fda28-119">Specifies the name of a server.</span></span>
<span data-ttu-id="fda28-120">這個 Cmdlet 會從伺服器中移除此參數指定的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="fda28-120">This cmdlet removes a firewall rule from the server that this parameter specifies.</span></span>

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

### <span data-ttu-id="fda28-121">-確認</span><span class="sxs-lookup"><span data-stu-id="fda28-121">-Confirm</span></span>
<span data-ttu-id="fda28-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fda28-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fda28-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fda28-123">-WhatIf</span></span>
<span data-ttu-id="fda28-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fda28-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fda28-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fda28-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fda28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda28-126">CommonParameters</span></span>
<span data-ttu-id="fda28-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fda28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda28-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fda28-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda28-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fda28-129">INPUTS</span></span>

### <span data-ttu-id="fda28-130">WindowsAzure. SqlDatabase. SqlDatabaseServerFirewallRuleCoNtext</span><span class="sxs-lookup"><span data-stu-id="fda28-130">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="fda28-131">輸出</span><span class="sxs-lookup"><span data-stu-id="fda28-131">OUTPUTS</span></span>

## <span data-ttu-id="fda28-132">筆記</span><span class="sxs-lookup"><span data-stu-id="fda28-132">NOTES</span></span>

## <span data-ttu-id="fda28-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="fda28-133">RELATED LINKS</span></span>

[<span data-ttu-id="fda28-134">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="fda28-134">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="fda28-135">刪除防火牆規則</span><span class="sxs-lookup"><span data-stu-id="fda28-135">Delete Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505706.aspx)

[<span data-ttu-id="fda28-136">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="fda28-136">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="fda28-137">AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fda28-137">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="fda28-138">新-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fda28-138">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="fda28-139">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fda28-139">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


