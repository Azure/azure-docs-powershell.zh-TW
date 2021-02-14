---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: e6ccf84d2de6c64000a6663de5a5b696d9033eae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142966"
---
# <span data-ttu-id="e94e0-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="e94e0-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="e94e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e94e0-102">SYNOPSIS</span></span>
<span data-ttu-id="e94e0-103">建立 Azure SQL 同步處理代理程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="e94e0-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="e94e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="e94e0-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e94e0-105">說明</span><span class="sxs-lookup"><span data-stu-id="e94e0-105">DESCRIPTION</span></span>
<span data-ttu-id="e94e0-106">**新的-AzSqlSyncAgentKey** Cmdlet 會建立 Azure SQL 同步處理代理程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="e94e0-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="e94e0-107">示例</span><span class="sxs-lookup"><span data-stu-id="e94e0-107">EXAMPLES</span></span>

### <span data-ttu-id="e94e0-108">範例1：建立 Azure SQL 同步處理代理程式的同步處理常式金鑰。</span><span class="sxs-lookup"><span data-stu-id="e94e0-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="e94e0-109">這個命令會建立 Azure SQL 同步處理代理程式的同步處理常式金鑰。</span><span class="sxs-lookup"><span data-stu-id="e94e0-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="e94e0-110">參數</span><span class="sxs-lookup"><span data-stu-id="e94e0-110">PARAMETERS</span></span>

### <span data-ttu-id="e94e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e94e0-111">-DefaultProfile</span></span>
<span data-ttu-id="e94e0-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e94e0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e94e0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e94e0-113">-ResourceGroupName</span></span>
<span data-ttu-id="e94e0-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e94e0-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="e94e0-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e94e0-115">-ServerName</span></span>
<span data-ttu-id="e94e0-116">同步處理常式所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e94e0-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="e94e0-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="e94e0-117">-SyncAgentName</span></span>
<span data-ttu-id="e94e0-118">同步處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="e94e0-118">The sync agent name.</span></span>

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

### <span data-ttu-id="e94e0-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e94e0-119">-Confirm</span></span>
<span data-ttu-id="e94e0-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e94e0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e94e0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e94e0-121">-WhatIf</span></span>
<span data-ttu-id="e94e0-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e94e0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e94e0-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e94e0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e94e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94e0-124">CommonParameters</span></span>
<span data-ttu-id="e94e0-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e94e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94e0-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e94e0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94e0-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e94e0-127">INPUTS</span></span>

### <span data-ttu-id="e94e0-128">System.object</span><span class="sxs-lookup"><span data-stu-id="e94e0-128">System.String</span></span>

## <span data-ttu-id="e94e0-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e94e0-129">OUTPUTS</span></span>

### <span data-ttu-id="e94e0-130">AzureSqlSyncAgentKeyModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="e94e0-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="e94e0-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e94e0-131">NOTES</span></span>

## <span data-ttu-id="e94e0-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e94e0-132">RELATED LINKS</span></span>
