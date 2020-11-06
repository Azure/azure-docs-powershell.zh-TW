---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 5afd12ac027b19f888eb6a5110db2179dd6df24d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455932"
---
# <span data-ttu-id="0aadd-101">Remove-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="0aadd-101">Remove-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="0aadd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0aadd-102">SYNOPSIS</span></span>
<span data-ttu-id="0aadd-103">移除 Azure SQL Server DNS 別名。</span><span class="sxs-lookup"><span data-stu-id="0aadd-103">Removes Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aadd-104">句法</span><span class="sxs-lookup"><span data-stu-id="0aadd-104">SYNTAX</span></span>

### <span data-ttu-id="0aadd-105">從 Cmdlet 輸入參數移除伺服器 Dns 別名</span><span class="sxs-lookup"><span data-stu-id="0aadd-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzureRmSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aadd-106">從 AzureSqlServerDnsAliasModel 實例定義中移除伺服器 Dns 別名</span><span class="sxs-lookup"><span data-stu-id="0aadd-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzureRmSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aadd-107">從 Azure 資源識別碼中移除伺服器 Dns 別名</span><span class="sxs-lookup"><span data-stu-id="0aadd-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzureRmSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aadd-108">說明</span><span class="sxs-lookup"><span data-stu-id="0aadd-108">DESCRIPTION</span></span>
<span data-ttu-id="0aadd-109">這個命令會從伺服器移除 Azure SQL Server DNS 別名，讓伺服器保持不變。</span><span class="sxs-lookup"><span data-stu-id="0aadd-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="0aadd-110">示例</span><span class="sxs-lookup"><span data-stu-id="0aadd-110">EXAMPLES</span></span>

### <span data-ttu-id="0aadd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0aadd-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="0aadd-112">從伺服器名稱為 serverName 的名稱為 aliasName 的 Azure SQL Server DNS 別名移除。</span><span class="sxs-lookup"><span data-stu-id="0aadd-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="0aadd-113">參數</span><span class="sxs-lookup"><span data-stu-id="0aadd-113">PARAMETERS</span></span>

### <span data-ttu-id="0aadd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0aadd-114">-AsJob</span></span>
<span data-ttu-id="0aadd-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0aadd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0aadd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aadd-116">-DefaultProfile</span></span>
<span data-ttu-id="0aadd-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0aadd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aadd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0aadd-118">-Force</span></span>
<span data-ttu-id="0aadd-119">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="0aadd-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0aadd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0aadd-120">-InputObject</span></span>
<span data-ttu-id="0aadd-121">要移除的伺服器 Dns 別名物件</span><span class="sxs-lookup"><span data-stu-id="0aadd-121">The Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="0aadd-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0aadd-122">-Name</span></span>
<span data-ttu-id="0aadd-123">Azure Sql Server Dns 別名名稱</span><span class="sxs-lookup"><span data-stu-id="0aadd-123">Azure Sql Server Dns Alias name</span></span>

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

### <span data-ttu-id="0aadd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aadd-124">-ResourceGroupName</span></span>
<span data-ttu-id="0aadd-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0aadd-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="0aadd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0aadd-126">-ResourceId</span></span>
<span data-ttu-id="0aadd-127">要移除的伺服器 Dns 別名物件的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0aadd-127">The resource id of Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="0aadd-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0aadd-128">-ServerName</span></span>
<span data-ttu-id="0aadd-129">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="0aadd-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="0aadd-130">-確認</span><span class="sxs-lookup"><span data-stu-id="0aadd-130">-Confirm</span></span>
<span data-ttu-id="0aadd-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0aadd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aadd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aadd-132">-WhatIf</span></span>
<span data-ttu-id="0aadd-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0aadd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aadd-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0aadd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aadd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aadd-135">CommonParameters</span></span>
<span data-ttu-id="0aadd-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0aadd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aadd-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0aadd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aadd-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0aadd-138">INPUTS</span></span>

### <span data-ttu-id="0aadd-139">AzureSqlServerDnsAliasModel 中的 [ServerDnsAlias]</span><span class="sxs-lookup"><span data-stu-id="0aadd-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>
<span data-ttu-id="0aadd-140">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="0aadd-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0aadd-141">System.object</span><span class="sxs-lookup"><span data-stu-id="0aadd-141">System.String</span></span>

## <span data-ttu-id="0aadd-142">輸出</span><span class="sxs-lookup"><span data-stu-id="0aadd-142">OUTPUTS</span></span>

### <span data-ttu-id="0aadd-143">AzureSqlServerDnsAliasModel 中的 [ServerDnsAlias]</span><span class="sxs-lookup"><span data-stu-id="0aadd-143">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="0aadd-144">筆記</span><span class="sxs-lookup"><span data-stu-id="0aadd-144">NOTES</span></span>

## <span data-ttu-id="0aadd-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="0aadd-145">RELATED LINKS</span></span>
