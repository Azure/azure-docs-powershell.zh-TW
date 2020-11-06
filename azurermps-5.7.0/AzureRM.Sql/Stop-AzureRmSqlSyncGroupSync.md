---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 24e61d466ac691f0f6faaa0b87bf819671517809
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448528"
---
# <span data-ttu-id="bd9b3-101">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="bd9b3-101">Stop-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="bd9b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd9b3-102">SYNOPSIS</span></span>
<span data-ttu-id="bd9b3-103">停止同步處理群組同步處理。</span><span class="sxs-lookup"><span data-stu-id="bd9b3-103">Stops a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd9b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd9b3-104">SYNTAX</span></span>

```
Stop-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd9b3-105">說明</span><span class="sxs-lookup"><span data-stu-id="bd9b3-105">DESCRIPTION</span></span>
<span data-ttu-id="bd9b3-106">**AzureRmSqlSyncGroupSync** Cmdlet 會停止同步處理群組同步處理。</span><span class="sxs-lookup"><span data-stu-id="bd9b3-106">The **Stop-AzureRmSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="bd9b3-107">示例</span><span class="sxs-lookup"><span data-stu-id="bd9b3-107">EXAMPLES</span></span>

### <span data-ttu-id="bd9b3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bd9b3-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="bd9b3-109">這個命令會停止對同步處理群組 mysg 進行的同步處理。</span><span class="sxs-lookup"><span data-stu-id="bd9b3-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="bd9b3-110">參數</span><span class="sxs-lookup"><span data-stu-id="bd9b3-110">PARAMETERS</span></span>

### <span data-ttu-id="bd9b3-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd9b3-111">-DatabaseName</span></span>
<span data-ttu-id="bd9b3-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd9b3-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd9b3-113">-DefaultProfile</span></span>
<span data-ttu-id="bd9b3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bd9b3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd9b3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd9b3-115">-PassThru</span></span>
<span data-ttu-id="bd9b3-116">定義是否要傳回同步處理群組</span><span class="sxs-lookup"><span data-stu-id="bd9b3-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="bd9b3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd9b3-117">-ResourceGroupName</span></span>
<span data-ttu-id="bd9b3-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd9b3-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="bd9b3-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bd9b3-119">-ServerName</span></span>
<span data-ttu-id="bd9b3-120">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd9b3-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="bd9b3-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="bd9b3-121">-SyncGroupName</span></span>
<span data-ttu-id="bd9b3-122">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="bd9b3-122">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9b3-123">-確認</span><span class="sxs-lookup"><span data-stu-id="bd9b3-123">-Confirm</span></span>
<span data-ttu-id="bd9b3-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bd9b3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd9b3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd9b3-125">-WhatIf</span></span>
<span data-ttu-id="bd9b3-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd9b3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd9b3-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd9b3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd9b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd9b3-128">CommonParameters</span></span>
<span data-ttu-id="bd9b3-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd9b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd9b3-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd9b3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd9b3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="bd9b3-131">INPUTS</span></span>

### <span data-ttu-id="bd9b3-132">所有</span><span class="sxs-lookup"><span data-stu-id="bd9b3-132">None</span></span>
<span data-ttu-id="bd9b3-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="bd9b3-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd9b3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="bd9b3-134">OUTPUTS</span></span>

### <span data-ttu-id="bd9b3-135">AzureSqlSyncGroupModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="bd9b3-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="bd9b3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="bd9b3-136">NOTES</span></span>

## <span data-ttu-id="bd9b3-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd9b3-137">RELATED LINKS</span></span>

[<span data-ttu-id="bd9b3-138">開始-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="bd9b3-138">Start-AzureRmSqlSyncGroupSync</span></span>](./Start-AzureRmSqlSyncGroupSync.md)

