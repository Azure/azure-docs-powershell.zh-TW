---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 46a3476d5ae4cead17eba0d03412ad2db57b01a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902725"
---
# <span data-ttu-id="252b4-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="252b4-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="252b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="252b4-102">SYNOPSIS</span></span>
<span data-ttu-id="252b4-103">此命令會建立一個新的 Azure SQL Server DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="252b4-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="252b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="252b4-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="252b4-105">描述</span><span class="sxs-lookup"><span data-stu-id="252b4-105">DESCRIPTION</span></span>
<span data-ttu-id="252b4-106">建立指向指定伺服器的新 Azure SQL Server DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="252b4-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="252b4-107">例子</span><span class="sxs-lookup"><span data-stu-id="252b4-107">EXAMPLES</span></span>

### <span data-ttu-id="252b4-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="252b4-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="252b4-109">此命令會使用指向伺服器伺服器名稱的名稱別名建立 Azure SQL Server DNS 別名</span><span class="sxs-lookup"><span data-stu-id="252b4-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="252b4-110">參數</span><span class="sxs-lookup"><span data-stu-id="252b4-110">PARAMETERS</span></span>

### <span data-ttu-id="252b4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="252b4-111">-AsJob</span></span>
<span data-ttu-id="252b4-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="252b4-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="252b4-113">-DefaultProfile</span></span>
<span data-ttu-id="252b4-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="252b4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="252b4-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="252b4-115">-Name</span></span>
<span data-ttu-id="252b4-116">Azure Sql Server Dns 別名。</span><span class="sxs-lookup"><span data-stu-id="252b4-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="252b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="252b4-118">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="252b4-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="252b4-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="252b4-119">-ServerName</span></span>
<span data-ttu-id="252b4-120">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="252b4-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="252b4-121">-確認</span><span class="sxs-lookup"><span data-stu-id="252b4-121">-Confirm</span></span>
<span data-ttu-id="252b4-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="252b4-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252b4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="252b4-123">-WhatIf</span></span>
<span data-ttu-id="252b4-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="252b4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="252b4-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="252b4-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="252b4-126">CommonParameters</span></span>
<span data-ttu-id="252b4-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="252b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="252b4-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="252b4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="252b4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="252b4-129">INPUTS</span></span>

### <span data-ttu-id="252b4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="252b4-130">System.String</span></span>

## <span data-ttu-id="252b4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="252b4-131">OUTPUTS</span></span>

### <span data-ttu-id="252b4-132">Microsoft.Azure.Commands.sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="252b4-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="252b4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="252b4-133">NOTES</span></span>

## <span data-ttu-id="252b4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="252b4-134">RELATED LINKS</span></span>
