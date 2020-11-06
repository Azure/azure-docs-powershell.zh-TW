---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
ms.openlocfilehash: b96d125b2a4f608c54024619ca6259a136d2ed69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447598"
---
# <span data-ttu-id="d1c12-101">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d1c12-101">Remove-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="d1c12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1c12-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c12-103">移除 Azure SQL 資料庫同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="d1c12-103">Removes an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1c12-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1c12-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1c12-105">說明</span><span class="sxs-lookup"><span data-stu-id="d1c12-105">DESCRIPTION</span></span>
<span data-ttu-id="d1c12-106">**AzureRmSqlSyncMember** Cmdlet 會移除 Azure SQL 資料庫同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="d1c12-106">The **Remove-AzureRmSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="d1c12-107">示例</span><span class="sxs-lookup"><span data-stu-id="d1c12-107">EXAMPLES</span></span>

### <span data-ttu-id="d1c12-108">範例1：移除同步處理成員</span><span class="sxs-lookup"><span data-stu-id="d1c12-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="d1c12-109">這個命令會移除名為 syncMember01 的 Azure SQL 資料庫同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="d1c12-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="d1c12-110">參數</span><span class="sxs-lookup"><span data-stu-id="d1c12-110">PARAMETERS</span></span>

### <span data-ttu-id="d1c12-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d1c12-111">-DatabaseName</span></span>
<span data-ttu-id="d1c12-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1c12-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d1c12-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c12-113">-DefaultProfile</span></span>
<span data-ttu-id="d1c12-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d1c12-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1c12-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d1c12-115">-Force</span></span>
<span data-ttu-id="d1c12-116">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="d1c12-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d1c12-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d1c12-117">-Name</span></span>
<span data-ttu-id="d1c12-118">同步處理成員名稱。</span><span class="sxs-lookup"><span data-stu-id="d1c12-118">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1c12-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1c12-119">-PassThru</span></span>
<span data-ttu-id="d1c12-120">定義是否傳回已移除的同步處理成員</span><span class="sxs-lookup"><span data-stu-id="d1c12-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="d1c12-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c12-121">-ResourceGroupName</span></span>
<span data-ttu-id="d1c12-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1c12-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="d1c12-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d1c12-123">-ServerName</span></span>
<span data-ttu-id="d1c12-124">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1c12-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d1c12-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c12-125">-SyncGroupName</span></span>
<span data-ttu-id="d1c12-126">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="d1c12-126">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1c12-127">-確認</span><span class="sxs-lookup"><span data-stu-id="d1c12-127">-Confirm</span></span>
<span data-ttu-id="d1c12-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d1c12-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1c12-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1c12-129">-WhatIf</span></span>
<span data-ttu-id="d1c12-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1c12-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1c12-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1c12-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1c12-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c12-132">CommonParameters</span></span>
<span data-ttu-id="d1c12-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1c12-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c12-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d1c12-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c12-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d1c12-135">INPUTS</span></span>

### <span data-ttu-id="d1c12-136">所有</span><span class="sxs-lookup"><span data-stu-id="d1c12-136">None</span></span>
<span data-ttu-id="d1c12-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d1c12-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1c12-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d1c12-138">OUTPUTS</span></span>

### <span data-ttu-id="d1c12-139">AzureSqlSyncMemberModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="d1c12-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="d1c12-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d1c12-140">NOTES</span></span>

## <span data-ttu-id="d1c12-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1c12-141">RELATED LINKS</span></span>

[<span data-ttu-id="d1c12-142">新-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d1c12-142">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="d1c12-143">更新-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d1c12-143">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="d1c12-144">AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d1c12-144">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)
