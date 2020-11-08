---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: d611f0bc14d657f47881cbdfbb1326111873114a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137971"
---
# <span data-ttu-id="ef577-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="ef577-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="ef577-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef577-102">SYNOPSIS</span></span>
<span data-ttu-id="ef577-103">移除 Azure SQL Server DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="ef577-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="ef577-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef577-104">SYNTAX</span></span>

### <span data-ttu-id="ef577-105">從 Cmdlet 輸入參數移除伺服器 Dns 別名</span><span class="sxs-lookup"><span data-stu-id="ef577-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef577-106">從 AzureSqlServerDnsAliasModel 實例定義中移除伺服器 Dns 別名</span><span class="sxs-lookup"><span data-stu-id="ef577-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef577-107">從 Azure 資源識別碼中移除伺服器 Dns 別名</span><span class="sxs-lookup"><span data-stu-id="ef577-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef577-108">說明</span><span class="sxs-lookup"><span data-stu-id="ef577-108">DESCRIPTION</span></span>
<span data-ttu-id="ef577-109">這個命令會從伺服器移除 Azure SQL Server DNS 別名，讓伺服器保持不變。</span><span class="sxs-lookup"><span data-stu-id="ef577-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="ef577-110">示例</span><span class="sxs-lookup"><span data-stu-id="ef577-110">EXAMPLES</span></span>

### <span data-ttu-id="ef577-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ef577-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="ef577-112">從伺服器名稱為 serverName 的名稱為 aliasName 的 Azure SQL Server DNS 別名移除。</span><span class="sxs-lookup"><span data-stu-id="ef577-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="ef577-113">參數</span><span class="sxs-lookup"><span data-stu-id="ef577-113">PARAMETERS</span></span>

### <span data-ttu-id="ef577-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef577-114">-AsJob</span></span>
<span data-ttu-id="ef577-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ef577-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef577-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef577-116">-DefaultProfile</span></span>
<span data-ttu-id="ef577-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef577-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef577-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ef577-118">-Force</span></span>
<span data-ttu-id="ef577-119">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="ef577-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ef577-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef577-120">-InputObject</span></span>
<span data-ttu-id="ef577-121">要移除的伺服器 Dns 別名物件</span><span class="sxs-lookup"><span data-stu-id="ef577-121">The Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="ef577-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef577-122">-Name</span></span>
<span data-ttu-id="ef577-123">Azure Sql Server Dns 別名名稱</span><span class="sxs-lookup"><span data-stu-id="ef577-123">Azure Sql Server Dns Alias name</span></span>

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

### <span data-ttu-id="ef577-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef577-124">-ResourceGroupName</span></span>
<span data-ttu-id="ef577-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef577-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ef577-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef577-126">-ResourceId</span></span>
<span data-ttu-id="ef577-127">要移除的伺服器 Dns 別名物件的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ef577-127">The resource id of Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="ef577-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ef577-128">-ServerName</span></span>
<span data-ttu-id="ef577-129">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="ef577-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="ef577-130">-確認</span><span class="sxs-lookup"><span data-stu-id="ef577-130">-Confirm</span></span>
<span data-ttu-id="ef577-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef577-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef577-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef577-132">-WhatIf</span></span>
<span data-ttu-id="ef577-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef577-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef577-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef577-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef577-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef577-135">CommonParameters</span></span>
<span data-ttu-id="ef577-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef577-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef577-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ef577-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef577-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ef577-138">INPUTS</span></span>

### <span data-ttu-id="ef577-139">AzureSqlServerDnsAliasModel 中的 [ServerDnsAlias]</span><span class="sxs-lookup"><span data-stu-id="ef577-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="ef577-140">System.object</span><span class="sxs-lookup"><span data-stu-id="ef577-140">System.String</span></span>

## <span data-ttu-id="ef577-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ef577-141">OUTPUTS</span></span>

### <span data-ttu-id="ef577-142">AzureSqlServerDnsAliasModel 中的 [ServerDnsAlias]</span><span class="sxs-lookup"><span data-stu-id="ef577-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="ef577-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ef577-143">NOTES</span></span>

## <span data-ttu-id="ef577-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef577-144">RELATED LINKS</span></span>
