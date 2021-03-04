---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: 30c0cca7fb1d8eab2c5d0abe4d6c0d556cc92d7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913093"
---
# <span data-ttu-id="f9c48-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f9c48-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="f9c48-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f9c48-102">SYNOPSIS</span></span>
<span data-ttu-id="f9c48-103">移除 Azure SQL 同步代理程式。</span><span class="sxs-lookup"><span data-stu-id="f9c48-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="f9c48-104">語法</span><span class="sxs-lookup"><span data-stu-id="f9c48-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9c48-105">描述</span><span class="sxs-lookup"><span data-stu-id="f9c48-105">DESCRIPTION</span></span>
<span data-ttu-id="f9c48-106">**Remove-AzSqlSyncAgent** Cmdlet 會移除 Azure SQL 同步代理程式。</span><span class="sxs-lookup"><span data-stu-id="f9c48-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="f9c48-107">例子</span><span class="sxs-lookup"><span data-stu-id="f9c48-107">EXAMPLES</span></span>

### <span data-ttu-id="f9c48-108">範例 1：移除同步代理程式</span><span class="sxs-lookup"><span data-stu-id="f9c48-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="f9c48-109">此命令會移除名為 syncAgent01 的 Azure SQL 同步管理代理程式。</span><span class="sxs-lookup"><span data-stu-id="f9c48-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="f9c48-110">參數</span><span class="sxs-lookup"><span data-stu-id="f9c48-110">PARAMETERS</span></span>

### <span data-ttu-id="f9c48-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9c48-111">-DefaultProfile</span></span>
<span data-ttu-id="f9c48-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f9c48-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9c48-113">-強制</span><span class="sxs-lookup"><span data-stu-id="f9c48-113">-Force</span></span>
<span data-ttu-id="f9c48-114">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="f9c48-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f9c48-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9c48-115">-Name</span></span>
<span data-ttu-id="f9c48-116">同步代理程式名稱。</span><span class="sxs-lookup"><span data-stu-id="f9c48-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9c48-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9c48-117">-PassThru</span></span>
<span data-ttu-id="f9c48-118">定義是否退回已移除的同步代理程式</span><span class="sxs-lookup"><span data-stu-id="f9c48-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="f9c48-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9c48-119">-ResourceGroupName</span></span>
<span data-ttu-id="f9c48-120">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9c48-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9c48-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f9c48-121">-ServerName</span></span>
<span data-ttu-id="f9c48-122">同步處理代理程式位於 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9c48-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="f9c48-123">-確認</span><span class="sxs-lookup"><span data-stu-id="f9c48-123">-Confirm</span></span>
<span data-ttu-id="f9c48-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f9c48-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9c48-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9c48-125">-WhatIf</span></span>
<span data-ttu-id="f9c48-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9c48-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9c48-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9c48-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9c48-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9c48-128">CommonParameters</span></span>
<span data-ttu-id="f9c48-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f9c48-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9c48-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9c48-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9c48-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f9c48-131">INPUTS</span></span>

### <span data-ttu-id="f9c48-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f9c48-132">System.String</span></span>

## <span data-ttu-id="f9c48-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f9c48-133">OUTPUTS</span></span>

### <span data-ttu-id="f9c48-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="f9c48-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="f9c48-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f9c48-135">NOTES</span></span>

## <span data-ttu-id="f9c48-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9c48-136">RELATED LINKS</span></span>

[<span data-ttu-id="f9c48-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f9c48-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="f9c48-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f9c48-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

