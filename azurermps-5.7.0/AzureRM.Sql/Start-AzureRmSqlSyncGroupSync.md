---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 040b08e328cb06629e706350fa14752fa6918954
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448529"
---
# <span data-ttu-id="eb59a-101">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="eb59a-101">Start-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="eb59a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb59a-102">SYNOPSIS</span></span>
<span data-ttu-id="eb59a-103">啟動同步處理群組同步處理。</span><span class="sxs-lookup"><span data-stu-id="eb59a-103">Starts a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb59a-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb59a-104">SYNTAX</span></span>

```
Start-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb59a-105">說明</span><span class="sxs-lookup"><span data-stu-id="eb59a-105">DESCRIPTION</span></span>
<span data-ttu-id="eb59a-106">**Start-AzureRmSqlSyncGroupSync** Cmdlet 會啟動同步處理群組同步處理。</span><span class="sxs-lookup"><span data-stu-id="eb59a-106">The **Start-AzureRmSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="eb59a-107">示例</span><span class="sxs-lookup"><span data-stu-id="eb59a-107">EXAMPLES</span></span>

### <span data-ttu-id="eb59a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="eb59a-108">Example 1</span></span>
```
PS C:\> Start-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="eb59a-109">這個命令會針對同步處理群組 mysg 啟動一輪同步處理。</span><span class="sxs-lookup"><span data-stu-id="eb59a-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="eb59a-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb59a-110">PARAMETERS</span></span>

### <span data-ttu-id="eb59a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb59a-111">-DatabaseName</span></span>
<span data-ttu-id="eb59a-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb59a-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="eb59a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb59a-113">-DefaultProfile</span></span>
<span data-ttu-id="eb59a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="eb59a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb59a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb59a-115">-PassThru</span></span>
<span data-ttu-id="eb59a-116">定義是否要傳回同步處理群組</span><span class="sxs-lookup"><span data-stu-id="eb59a-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="eb59a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb59a-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb59a-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb59a-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="eb59a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eb59a-119">-ServerName</span></span>
<span data-ttu-id="eb59a-120">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb59a-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="eb59a-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="eb59a-121">-SyncGroupName</span></span>
<span data-ttu-id="eb59a-122">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="eb59a-122">The sync group name.</span></span>

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

### <span data-ttu-id="eb59a-123">-確認</span><span class="sxs-lookup"><span data-stu-id="eb59a-123">-Confirm</span></span>
<span data-ttu-id="eb59a-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eb59a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb59a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb59a-125">-WhatIf</span></span>
<span data-ttu-id="eb59a-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb59a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb59a-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb59a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb59a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb59a-128">CommonParameters</span></span>
<span data-ttu-id="eb59a-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb59a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb59a-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb59a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb59a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="eb59a-131">INPUTS</span></span>

### <span data-ttu-id="eb59a-132">所有</span><span class="sxs-lookup"><span data-stu-id="eb59a-132">None</span></span>
<span data-ttu-id="eb59a-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="eb59a-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb59a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="eb59a-134">OUTPUTS</span></span>

### <span data-ttu-id="eb59a-135">AzureSqlSyncGroupModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="eb59a-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="eb59a-136">筆記</span><span class="sxs-lookup"><span data-stu-id="eb59a-136">NOTES</span></span>

## <span data-ttu-id="eb59a-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb59a-137">RELATED LINKS</span></span>

[<span data-ttu-id="eb59a-138">停止 AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="eb59a-138">Stop-AzureRmSqlSyncGroupSync</span></span>](./Stop-AzureRmSqlSyncGroupSync.md)

