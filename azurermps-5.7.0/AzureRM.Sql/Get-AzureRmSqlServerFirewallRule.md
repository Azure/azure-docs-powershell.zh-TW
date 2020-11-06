---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: eb514075bd366a0360f29c65455805be5f85569f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444264"
---
# <span data-ttu-id="01c0f-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="01c0f-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="01c0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="01c0f-103">取得 SQL 資料庫伺服器的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="01c0f-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01c0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="01c0f-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01c0f-105">說明</span><span class="sxs-lookup"><span data-stu-id="01c0f-105">DESCRIPTION</span></span>
<span data-ttu-id="01c0f-106">**AzureRmSqlServerFirewallRule** Cmdlet 會取得 Azure SQL 資料庫伺服器的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="01c0f-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="01c0f-107">如果您指定防火牆規則的名稱，此 Cmdlet 會取得該特定防火牆規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="01c0f-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="01c0f-108">示例</span><span class="sxs-lookup"><span data-stu-id="01c0f-108">EXAMPLES</span></span>

### <span data-ttu-id="01c0f-109">範例1：取得伺服器的所有規則</span><span class="sxs-lookup"><span data-stu-id="01c0f-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="01c0f-110">這個命令會取得伺服器名為 Server01 的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="01c0f-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="01c0f-111">參數</span><span class="sxs-lookup"><span data-stu-id="01c0f-111">PARAMETERS</span></span>

### <span data-ttu-id="01c0f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c0f-112">-DefaultProfile</span></span>
<span data-ttu-id="01c0f-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="01c0f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c0f-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="01c0f-114">-FirewallRuleName</span></span>
<span data-ttu-id="01c0f-115">指定防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="01c0f-115">Specifies the name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c0f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c0f-116">-ResourceGroupName</span></span>
<span data-ttu-id="01c0f-117">指定指派 SQL Server 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="01c0f-117">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c0f-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="01c0f-118">-ServerName</span></span>
<span data-ttu-id="01c0f-119">指定 SQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="01c0f-119">Specifies the name of the SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01c0f-120">-確認</span><span class="sxs-lookup"><span data-stu-id="01c0f-120">-Confirm</span></span>
<span data-ttu-id="01c0f-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="01c0f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01c0f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c0f-122">-WhatIf</span></span>
<span data-ttu-id="01c0f-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="01c0f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01c0f-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01c0f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01c0f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c0f-125">CommonParameters</span></span>
<span data-ttu-id="01c0f-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="01c0f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c0f-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="01c0f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c0f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="01c0f-128">INPUTS</span></span>

### <span data-ttu-id="01c0f-129">所有</span><span class="sxs-lookup"><span data-stu-id="01c0f-129">None</span></span>
<span data-ttu-id="01c0f-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="01c0f-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01c0f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="01c0f-131">OUTPUTS</span></span>

### <span data-ttu-id="01c0f-132">AzureSqlServerFirewallRuleModel 中的 [FirewallRule]</span><span class="sxs-lookup"><span data-stu-id="01c0f-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="01c0f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="01c0f-133">NOTES</span></span>

## <span data-ttu-id="01c0f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="01c0f-134">RELATED LINKS</span></span>

[<span data-ttu-id="01c0f-135">新-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="01c0f-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="01c0f-136">移除-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="01c0f-136">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="01c0f-137">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="01c0f-137">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="01c0f-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="01c0f-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


