---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: BE00A25D-3ECE-4B27-9D79-78128CFEBDB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 100202df1871610aff3af1fe90bb7d603c141d62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967018"
---
# <span data-ttu-id="3ce85-101">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3ce85-101">Get-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="3ce85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ce85-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce85-103">取得 Azure SQL Database Server 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="3ce85-103">Gets firewall rules for Azure SQL Database Server.</span></span>

## <span data-ttu-id="3ce85-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ce85-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ce85-105">說明</span><span class="sxs-lookup"><span data-stu-id="3ce85-105">DESCRIPTION</span></span>
<span data-ttu-id="3ce85-106">**AzureSqlDatabaseServerFirewallRule** Cmdlet 會取得 Azure SQL Database Server 實例的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="3ce85-106">The **Get-AzureSqlDatabaseServerFirewallRule** cmdlet gets firewall rules for an instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="3ce85-107">如果您依名稱指定防火牆規則，此 Cmdlet 會傳回有關該防火牆規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="3ce85-107">If you specify a firewall rule by name, this cmdlet returns information about that firewall rule.</span></span>
<span data-ttu-id="3ce85-108">否則，Cmdlet 會傳回指定 Azure SQL 資料庫伺服器上所有防火牆規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3ce85-108">Otherwise, the cmdlet returns information about all the firewall rules on the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="3ce85-109">示例</span><span class="sxs-lookup"><span data-stu-id="3ce85-109">EXAMPLES</span></span>

### <span data-ttu-id="3ce85-110">範例1：取得伺服器上的所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="3ce85-110">Example 1: Get all firewall rules on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="3ce85-111">這個命令會取得名為 lpqd0zbr8y 的 Azure SQL Database server 上的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="3ce85-111">This command gets all the firewall rules on the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="3ce85-112">範例2：使用其名稱取得防火牆規則</span><span class="sxs-lookup"><span data-stu-id="3ce85-112">Example 2: Get a firewall rule by using its name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="3ce85-113">這個命令會在名為 lpqd0zbr8y 的伺服器上取得名為 FirewallRule24 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="3ce85-113">This command gets the firewall rule named FirewallRule24 on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="3ce85-114">參數</span><span class="sxs-lookup"><span data-stu-id="3ce85-114">PARAMETERS</span></span>

### <span data-ttu-id="3ce85-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3ce85-115">-Profile</span></span>
<span data-ttu-id="3ce85-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3ce85-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3ce85-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3ce85-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3ce85-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="3ce85-118">-RuleName</span></span>
<span data-ttu-id="3ce85-119">指定此 Cmdlet 所取得之防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ce85-119">Specifies the name of the firewall rule that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce85-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3ce85-120">-ServerName</span></span>
<span data-ttu-id="3ce85-121">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ce85-121">Specifies the name of a server.</span></span>
<span data-ttu-id="3ce85-122">這個 Cmdlet 會從伺服器取得此參數指定的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="3ce85-122">This cmdlet gets firewall rules from the server that this parameter specifies.</span></span>
<span data-ttu-id="3ce85-123">指定 [伺服器名稱]，而不是 [完全限定的 DNS 名稱]。</span><span class="sxs-lookup"><span data-stu-id="3ce85-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="3ce85-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce85-124">CommonParameters</span></span>
<span data-ttu-id="3ce85-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ce85-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce85-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3ce85-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce85-127">輸入</span><span class="sxs-lookup"><span data-stu-id="3ce85-127">INPUTS</span></span>

### <span data-ttu-id="3ce85-128">WindowsAzure. SqlDatabase. SqlDatabaseServerFirewallRuleCoNtext</span><span class="sxs-lookup"><span data-stu-id="3ce85-128">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="3ce85-129">輸出</span><span class="sxs-lookup"><span data-stu-id="3ce85-129">OUTPUTS</span></span>

### <span data-ttu-id="3ce85-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span><span class="sxs-lookup"><span data-stu-id="3ce85-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span></span>

## <span data-ttu-id="3ce85-131">筆記</span><span class="sxs-lookup"><span data-stu-id="3ce85-131">NOTES</span></span>

## <span data-ttu-id="3ce85-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ce85-132">RELATED LINKS</span></span>

[<span data-ttu-id="3ce85-133">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="3ce85-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="3ce85-134">清單防火牆規則</span><span class="sxs-lookup"><span data-stu-id="3ce85-134">List Firewall Rules</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505715.aspx)

[<span data-ttu-id="3ce85-135">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="3ce85-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="3ce85-136">新-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3ce85-136">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="3ce85-137">移除-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3ce85-137">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="3ce85-138">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3ce85-138">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


