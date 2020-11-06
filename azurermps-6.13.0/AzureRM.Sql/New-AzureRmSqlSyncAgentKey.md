---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
ms.openlocfilehash: cb4ca947d9f87cd6a0d3b4cdf476cf0176db2c3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445395"
---
# <span data-ttu-id="4864c-101">New-AzureRmSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="4864c-101">New-AzureRmSqlSyncAgentKey</span></span>

## <span data-ttu-id="4864c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4864c-102">SYNOPSIS</span></span>
<span data-ttu-id="4864c-103">建立 Azure SQL 同步處理代理程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="4864c-103">Creates an Azure SQL Sync Agent Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4864c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4864c-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4864c-105">說明</span><span class="sxs-lookup"><span data-stu-id="4864c-105">DESCRIPTION</span></span>
<span data-ttu-id="4864c-106">**新的-AzureRmSqlSyncAgentKey** Cmdlet 會建立 Azure SQL 同步處理代理程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="4864c-106">The **New-AzureRmSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="4864c-107">示例</span><span class="sxs-lookup"><span data-stu-id="4864c-107">EXAMPLES</span></span>

### <span data-ttu-id="4864c-108">範例1：建立 Azure SQL 同步處理代理程式的同步處理常式金鑰。</span><span class="sxs-lookup"><span data-stu-id="4864c-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="4864c-109">這個命令會建立 Azure SQL 同步處理代理程式的同步處理常式金鑰。</span><span class="sxs-lookup"><span data-stu-id="4864c-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="4864c-110">參數</span><span class="sxs-lookup"><span data-stu-id="4864c-110">PARAMETERS</span></span>

### <span data-ttu-id="4864c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4864c-111">-DefaultProfile</span></span>
<span data-ttu-id="4864c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4864c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4864c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4864c-113">-ResourceGroupName</span></span>
<span data-ttu-id="4864c-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4864c-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="4864c-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4864c-115">-ServerName</span></span>
<span data-ttu-id="4864c-116">同步處理常式所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4864c-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="4864c-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="4864c-117">-SyncAgentName</span></span>
<span data-ttu-id="4864c-118">同步處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="4864c-118">The sync agent name.</span></span>

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

### <span data-ttu-id="4864c-119">-確認</span><span class="sxs-lookup"><span data-stu-id="4864c-119">-Confirm</span></span>
<span data-ttu-id="4864c-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4864c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4864c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4864c-121">-WhatIf</span></span>
<span data-ttu-id="4864c-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4864c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4864c-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4864c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4864c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4864c-124">CommonParameters</span></span>
<span data-ttu-id="4864c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4864c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4864c-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4864c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4864c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4864c-127">INPUTS</span></span>

### <span data-ttu-id="4864c-128">System.object</span><span class="sxs-lookup"><span data-stu-id="4864c-128">System.String</span></span>

## <span data-ttu-id="4864c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4864c-129">OUTPUTS</span></span>

### <span data-ttu-id="4864c-130">AzureSqlSyncAgentKeyModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="4864c-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="4864c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4864c-131">NOTES</span></span>

## <span data-ttu-id="4864c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="4864c-132">RELATED LINKS</span></span>
