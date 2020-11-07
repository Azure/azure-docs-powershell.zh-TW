---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: c8a3e10fb2f78556112831f4310eca60e296cf48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626480"
---
# <span data-ttu-id="06089-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="06089-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="06089-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06089-102">SYNOPSIS</span></span>
<span data-ttu-id="06089-103">修改 Azure SQL 資料庫伺服器中的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="06089-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06089-104">句法</span><span class="sxs-lookup"><span data-stu-id="06089-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06089-105">說明</span><span class="sxs-lookup"><span data-stu-id="06089-105">DESCRIPTION</span></span>
<span data-ttu-id="06089-106">**AzureRmSqlServerFirewallRule** Cmdlet 會修改 Azure SQL 資料庫伺服器中的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="06089-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="06089-107">示例</span><span class="sxs-lookup"><span data-stu-id="06089-107">EXAMPLES</span></span>

### <span data-ttu-id="06089-108">範例1：修改防火牆規則</span><span class="sxs-lookup"><span data-stu-id="06089-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="06089-109">這個命令會修改名為 Server01 的伺服器上名為 Rule01 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="06089-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="06089-110">此命令會修改開始和結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="06089-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="06089-111">參數</span><span class="sxs-lookup"><span data-stu-id="06089-111">PARAMETERS</span></span>

### <span data-ttu-id="06089-112">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="06089-112">-EndIpAddress</span></span>
<span data-ttu-id="06089-113">指定此規則 IP 位址範圍的結束值。</span><span class="sxs-lookup"><span data-stu-id="06089-113">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="06089-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="06089-114">-FirewallRuleName</span></span>
<span data-ttu-id="06089-115">指定此 Cmdlet 修改的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="06089-115">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06089-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06089-116">-ResourceGroupName</span></span>
<span data-ttu-id="06089-117">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="06089-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="06089-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="06089-118">-ServerName</span></span>
<span data-ttu-id="06089-119">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="06089-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="06089-120">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="06089-120">-StartIpAddress</span></span>
<span data-ttu-id="06089-121">指定防火牆規則 IP 位址範圍的起始值。</span><span class="sxs-lookup"><span data-stu-id="06089-121">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="06089-122">-確認</span><span class="sxs-lookup"><span data-stu-id="06089-122">-Confirm</span></span>
<span data-ttu-id="06089-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="06089-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06089-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06089-124">-WhatIf</span></span>
<span data-ttu-id="06089-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06089-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06089-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06089-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06089-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06089-127">-DefaultProfile</span></span>
<span data-ttu-id="06089-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="06089-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06089-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06089-129">CommonParameters</span></span>
<span data-ttu-id="06089-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06089-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06089-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="06089-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06089-132">輸入</span><span class="sxs-lookup"><span data-stu-id="06089-132">INPUTS</span></span>

## <span data-ttu-id="06089-133">輸出</span><span class="sxs-lookup"><span data-stu-id="06089-133">OUTPUTS</span></span>

### <span data-ttu-id="06089-134">AzureSqlServerFirewallRuleModel 中的 [FirewallRule]</span><span class="sxs-lookup"><span data-stu-id="06089-134">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="06089-135">筆記</span><span class="sxs-lookup"><span data-stu-id="06089-135">NOTES</span></span>

## <span data-ttu-id="06089-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="06089-136">RELATED LINKS</span></span>

[<span data-ttu-id="06089-137">AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="06089-137">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="06089-138">新-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="06089-138">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="06089-139">移除-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="06089-139">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="06089-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="06089-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


