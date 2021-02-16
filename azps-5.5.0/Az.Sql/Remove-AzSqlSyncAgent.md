---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: ca3ef83fab80e73d687fd11cde418c9ad43f499e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128195"
---
# <span data-ttu-id="cb9d5-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="cb9d5-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="cb9d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9d5-103">移除 Azure SQL 同步處理代理程式。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="cb9d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb9d5-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb9d5-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb9d5-105">DESCRIPTION</span></span>
<span data-ttu-id="cb9d5-106">**AzSqlSyncAgent** Cmdlet 會移除 Azure SQL 同步處理代理程式。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="cb9d5-107">示例</span><span class="sxs-lookup"><span data-stu-id="cb9d5-107">EXAMPLES</span></span>

### <span data-ttu-id="cb9d5-108">範例1：移除同步處理常式</span><span class="sxs-lookup"><span data-stu-id="cb9d5-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="cb9d5-109">這個命令會移除名為 syncAgent01 的 Azure SQL 同步處理代理程式。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="cb9d5-110">參數</span><span class="sxs-lookup"><span data-stu-id="cb9d5-110">PARAMETERS</span></span>

### <span data-ttu-id="cb9d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9d5-111">-DefaultProfile</span></span>
<span data-ttu-id="cb9d5-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cb9d5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb9d5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cb9d5-113">-Force</span></span>
<span data-ttu-id="cb9d5-114">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="cb9d5-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="cb9d5-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb9d5-115">-Name</span></span>
<span data-ttu-id="cb9d5-116">同步處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-116">The sync agent name.</span></span>

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

### <span data-ttu-id="cb9d5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb9d5-117">-PassThru</span></span>
<span data-ttu-id="cb9d5-118">定義是否傳回已移除的同步處理常式</span><span class="sxs-lookup"><span data-stu-id="cb9d5-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="cb9d5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb9d5-119">-ResourceGroupName</span></span>
<span data-ttu-id="cb9d5-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="cb9d5-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb9d5-121">-ServerName</span></span>
<span data-ttu-id="cb9d5-122">同步處理常式所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="cb9d5-123">-確認</span><span class="sxs-lookup"><span data-stu-id="cb9d5-123">-Confirm</span></span>
<span data-ttu-id="cb9d5-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb9d5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb9d5-125">-WhatIf</span></span>
<span data-ttu-id="cb9d5-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb9d5-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb9d5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9d5-128">CommonParameters</span></span>
<span data-ttu-id="cb9d5-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9d5-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cb9d5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9d5-131">輸入</span><span class="sxs-lookup"><span data-stu-id="cb9d5-131">INPUTS</span></span>

### <span data-ttu-id="cb9d5-132">System.object</span><span class="sxs-lookup"><span data-stu-id="cb9d5-132">System.String</span></span>

## <span data-ttu-id="cb9d5-133">輸出</span><span class="sxs-lookup"><span data-stu-id="cb9d5-133">OUTPUTS</span></span>

### <span data-ttu-id="cb9d5-134">AzureSqlSyncAgentModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="cb9d5-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="cb9d5-135">筆記</span><span class="sxs-lookup"><span data-stu-id="cb9d5-135">NOTES</span></span>

## <span data-ttu-id="cb9d5-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb9d5-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb9d5-137">新-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="cb9d5-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="cb9d5-138">AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="cb9d5-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

