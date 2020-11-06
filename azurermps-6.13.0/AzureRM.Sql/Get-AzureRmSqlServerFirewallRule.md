---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 5e32e136d293c7b5eb8017592cf1ac4e01c60b01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448883"
---
# <span data-ttu-id="4fe7e-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4fe7e-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="4fe7e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4fe7e-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe7e-103">取得 SQL 資料庫伺服器的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="4fe7e-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fe7e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4fe7e-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4fe7e-105">說明</span><span class="sxs-lookup"><span data-stu-id="4fe7e-105">DESCRIPTION</span></span>
<span data-ttu-id="4fe7e-106">**AzureRmSqlServerFirewallRule** Cmdlet 會取得 Azure SQL 資料庫伺服器的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="4fe7e-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="4fe7e-107">如果您指定防火牆規則的名稱，此 Cmdlet 會取得該特定防火牆規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4fe7e-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="4fe7e-108">示例</span><span class="sxs-lookup"><span data-stu-id="4fe7e-108">EXAMPLES</span></span>

### <span data-ttu-id="4fe7e-109">範例1：取得伺服器的所有規則</span><span class="sxs-lookup"><span data-stu-id="4fe7e-109">Example 1: Get all rules for a server</span></span>
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

<span data-ttu-id="4fe7e-110">這個命令會取得伺服器名為 Server01 的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="4fe7e-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="4fe7e-111">參數</span><span class="sxs-lookup"><span data-stu-id="4fe7e-111">PARAMETERS</span></span>

### <span data-ttu-id="4fe7e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe7e-112">-DefaultProfile</span></span>
<span data-ttu-id="4fe7e-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4fe7e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fe7e-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="4fe7e-114">-FirewallRuleName</span></span>
<span data-ttu-id="4fe7e-115">指定防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fe7e-115">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe7e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fe7e-116">-ResourceGroupName</span></span>
<span data-ttu-id="4fe7e-117">指定指派 SQL Server 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fe7e-117">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="4fe7e-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4fe7e-118">-ServerName</span></span>
<span data-ttu-id="4fe7e-119">指定 SQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fe7e-119">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="4fe7e-120">-確認</span><span class="sxs-lookup"><span data-stu-id="4fe7e-120">-Confirm</span></span>
<span data-ttu-id="4fe7e-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4fe7e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fe7e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fe7e-122">-WhatIf</span></span>
<span data-ttu-id="4fe7e-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4fe7e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fe7e-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4fe7e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fe7e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe7e-125">CommonParameters</span></span>
<span data-ttu-id="4fe7e-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4fe7e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe7e-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4fe7e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe7e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="4fe7e-128">INPUTS</span></span>

### <span data-ttu-id="4fe7e-129">System.object</span><span class="sxs-lookup"><span data-stu-id="4fe7e-129">System.String</span></span>

## <span data-ttu-id="4fe7e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="4fe7e-130">OUTPUTS</span></span>

### <span data-ttu-id="4fe7e-131">AzureSqlServerFirewallRuleModel 中的 [FirewallRule]</span><span class="sxs-lookup"><span data-stu-id="4fe7e-131">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="4fe7e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="4fe7e-132">NOTES</span></span>

## <span data-ttu-id="4fe7e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="4fe7e-133">RELATED LINKS</span></span>

[<span data-ttu-id="4fe7e-134">新-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4fe7e-134">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="4fe7e-135">移除-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4fe7e-135">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="4fe7e-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4fe7e-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="4fe7e-137">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="4fe7e-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

