---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: 35942c51aa383dbc7dcbe071083eee575228372a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903421"
---
# <span data-ttu-id="b2c84-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="b2c84-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="b2c84-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b2c84-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c84-103">建立 Azure SQL 同步管理代理程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="b2c84-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="b2c84-104">語法</span><span class="sxs-lookup"><span data-stu-id="b2c84-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2c84-105">描述</span><span class="sxs-lookup"><span data-stu-id="b2c84-105">DESCRIPTION</span></span>
<span data-ttu-id="b2c84-106">**New-AzSqlSyncAgentKey** Cmdlet 會建立 Azure SQL 同步管理代理程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="b2c84-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="b2c84-107">例子</span><span class="sxs-lookup"><span data-stu-id="b2c84-107">EXAMPLES</span></span>

### <span data-ttu-id="b2c84-108">範例 1：為 Azure SQL 同步代理程式建立同步代理程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="b2c84-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="b2c84-109">此命令會為 Azure SQL 同步代理程式建立同步代理程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="b2c84-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="b2c84-110">參數</span><span class="sxs-lookup"><span data-stu-id="b2c84-110">PARAMETERS</span></span>

### <span data-ttu-id="b2c84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c84-111">-DefaultProfile</span></span>
<span data-ttu-id="b2c84-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b2c84-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2c84-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2c84-113">-ResourceGroupName</span></span>
<span data-ttu-id="b2c84-114">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2c84-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="b2c84-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b2c84-115">-ServerName</span></span>
<span data-ttu-id="b2c84-116">同步處理代理程式位於 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2c84-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="b2c84-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="b2c84-117">-SyncAgentName</span></span>
<span data-ttu-id="b2c84-118">同步代理程式名稱。</span><span class="sxs-lookup"><span data-stu-id="b2c84-118">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c84-119">-確認</span><span class="sxs-lookup"><span data-stu-id="b2c84-119">-Confirm</span></span>
<span data-ttu-id="b2c84-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b2c84-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2c84-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c84-121">-WhatIf</span></span>
<span data-ttu-id="b2c84-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b2c84-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2c84-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2c84-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2c84-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c84-124">CommonParameters</span></span>
<span data-ttu-id="b2c84-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b2c84-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c84-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2c84-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c84-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b2c84-127">INPUTS</span></span>

### <span data-ttu-id="b2c84-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b2c84-128">System.String</span></span>

## <span data-ttu-id="b2c84-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b2c84-129">OUTPUTS</span></span>

### <span data-ttu-id="b2c84-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="b2c84-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="b2c84-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b2c84-131">NOTES</span></span>

## <span data-ttu-id="b2c84-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2c84-132">RELATED LINKS</span></span>
