---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: 07065c18b9e06f75863ddd41f8a6f0155a3699f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905769"
---
# <span data-ttu-id="633d9-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="633d9-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="633d9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="633d9-102">SYNOPSIS</span></span>
<span data-ttu-id="633d9-103">移除 Azure SQL Server DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="633d9-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="633d9-104">語法</span><span class="sxs-lookup"><span data-stu-id="633d9-104">SYNTAX</span></span>

### <span data-ttu-id="633d9-105">從 Cmdlet 輸入參數移除伺服器 Dns 別名</span><span class="sxs-lookup"><span data-stu-id="633d9-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="633d9-106">從 AzureSqlServerDnsAliasModel 實例定義移除伺服器 Dns 別名</span><span class="sxs-lookup"><span data-stu-id="633d9-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="633d9-107">從 Azure 資源識別碼移除伺服器 Dns 別名</span><span class="sxs-lookup"><span data-stu-id="633d9-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="633d9-108">描述</span><span class="sxs-lookup"><span data-stu-id="633d9-108">DESCRIPTION</span></span>
<span data-ttu-id="633d9-109">這個命令會從伺服器移除 Azure SQL Server DNS 別名，讓伺服器保持不變。</span><span class="sxs-lookup"><span data-stu-id="633d9-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="633d9-110">例子</span><span class="sxs-lookup"><span data-stu-id="633d9-110">EXAMPLES</span></span>

### <span data-ttu-id="633d9-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="633d9-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="633d9-112">使用名稱伺服器名稱從伺服器移除名稱 aliasName 的 Azure SQL Server DNS 別名</span><span class="sxs-lookup"><span data-stu-id="633d9-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="633d9-113">參數</span><span class="sxs-lookup"><span data-stu-id="633d9-113">PARAMETERS</span></span>

### <span data-ttu-id="633d9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="633d9-114">-AsJob</span></span>
<span data-ttu-id="633d9-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="633d9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="633d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="633d9-116">-DefaultProfile</span></span>
<span data-ttu-id="633d9-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="633d9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="633d9-118">-強制</span><span class="sxs-lookup"><span data-stu-id="633d9-118">-Force</span></span>
<span data-ttu-id="633d9-119">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="633d9-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="633d9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="633d9-120">-InputObject</span></span>
<span data-ttu-id="633d9-121">要移除的伺服器 Dns 別名物件</span><span class="sxs-lookup"><span data-stu-id="633d9-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="633d9-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="633d9-122">-Name</span></span>
<span data-ttu-id="633d9-123">Azure Sql Server Dns 別名名稱</span><span class="sxs-lookup"><span data-stu-id="633d9-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633d9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="633d9-124">-ResourceGroupName</span></span>
<span data-ttu-id="633d9-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="633d9-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633d9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="633d9-126">-ResourceId</span></span>
<span data-ttu-id="633d9-127">要移除的 Server Dns Alias 物件資源識別碼</span><span class="sxs-lookup"><span data-stu-id="633d9-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="633d9-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="633d9-128">-ServerName</span></span>
<span data-ttu-id="633d9-129">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="633d9-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="633d9-130">-確認</span><span class="sxs-lookup"><span data-stu-id="633d9-130">-Confirm</span></span>
<span data-ttu-id="633d9-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="633d9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="633d9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="633d9-132">-WhatIf</span></span>
<span data-ttu-id="633d9-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="633d9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="633d9-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="633d9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="633d9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="633d9-135">CommonParameters</span></span>
<span data-ttu-id="633d9-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="633d9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="633d9-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="633d9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="633d9-138">輸入</span><span class="sxs-lookup"><span data-stu-id="633d9-138">INPUTS</span></span>

### <span data-ttu-id="633d9-139">Microsoft.Azure.Commands.sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="633d9-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="633d9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="633d9-140">System.String</span></span>

## <span data-ttu-id="633d9-141">輸出</span><span class="sxs-lookup"><span data-stu-id="633d9-141">OUTPUTS</span></span>

### <span data-ttu-id="633d9-142">Microsoft.Azure.Commands.sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="633d9-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="633d9-143">筆記</span><span class="sxs-lookup"><span data-stu-id="633d9-143">NOTES</span></span>

## <span data-ttu-id="633d9-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="633d9-144">RELATED LINKS</span></span>
