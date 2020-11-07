---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
ms.openlocfilehash: b357c44afd52dd398631b9b7edfcedb0360cf377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623790"
---
# <span data-ttu-id="e4f88-101">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e4f88-101">Remove-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="e4f88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4f88-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f88-103">移除 Azure SQL 同步處理代理程式。</span><span class="sxs-lookup"><span data-stu-id="e4f88-103">Removes an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4f88-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4f88-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4f88-105">說明</span><span class="sxs-lookup"><span data-stu-id="e4f88-105">DESCRIPTION</span></span>
<span data-ttu-id="e4f88-106">**AzureRmSqlSyncAgent** Cmdlet 會移除 Azure SQL 同步處理代理程式。</span><span class="sxs-lookup"><span data-stu-id="e4f88-106">The **Remove-AzureRmSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="e4f88-107">示例</span><span class="sxs-lookup"><span data-stu-id="e4f88-107">EXAMPLES</span></span>

### <span data-ttu-id="e4f88-108">範例1：移除同步處理常式</span><span class="sxs-lookup"><span data-stu-id="e4f88-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="e4f88-109">這個命令會移除名為 syncAgent01 的 Azure SQL 同步處理代理程式。</span><span class="sxs-lookup"><span data-stu-id="e4f88-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="e4f88-110">參數</span><span class="sxs-lookup"><span data-stu-id="e4f88-110">PARAMETERS</span></span>

### <span data-ttu-id="e4f88-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f88-111">-DefaultProfile</span></span>
<span data-ttu-id="e4f88-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e4f88-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f88-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e4f88-113">-Force</span></span>
<span data-ttu-id="e4f88-114">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="e4f88-114">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f88-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4f88-115">-Name</span></span>
<span data-ttu-id="e4f88-116">同步處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="e4f88-116">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f88-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4f88-117">-PassThru</span></span>
<span data-ttu-id="e4f88-118">定義是否傳回已移除的同步處理常式</span><span class="sxs-lookup"><span data-stu-id="e4f88-118">Defines Whether return the removed sync agent</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f88-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4f88-119">-ResourceGroupName</span></span>
<span data-ttu-id="e4f88-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4f88-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f88-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e4f88-121">-ServerName</span></span>
<span data-ttu-id="e4f88-122">同步處理常式所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4f88-122">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f88-123">-確認</span><span class="sxs-lookup"><span data-stu-id="e4f88-123">-Confirm</span></span>
<span data-ttu-id="e4f88-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e4f88-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f88-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4f88-125">-WhatIf</span></span>
<span data-ttu-id="e4f88-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e4f88-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4f88-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e4f88-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f88-128">CommonParameters</span></span>
<span data-ttu-id="e4f88-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4f88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f88-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4f88-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f88-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e4f88-131">INPUTS</span></span>

### <span data-ttu-id="e4f88-132">所有</span><span class="sxs-lookup"><span data-stu-id="e4f88-132">None</span></span>
<span data-ttu-id="e4f88-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e4f88-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4f88-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e4f88-134">OUTPUTS</span></span>

### <span data-ttu-id="e4f88-135">AzureSqlSyncAgentModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="e4f88-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="e4f88-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e4f88-136">NOTES</span></span>

## <span data-ttu-id="e4f88-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4f88-137">RELATED LINKS</span></span>

[<span data-ttu-id="e4f88-138">新-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e4f88-138">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="e4f88-139">AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="e4f88-139">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

