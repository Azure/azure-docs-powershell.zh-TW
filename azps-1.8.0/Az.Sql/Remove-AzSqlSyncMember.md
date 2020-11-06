---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: 34db2f2307d60f1653b0a806350d96fa9e3380af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614760"
---
# <span data-ttu-id="f4c0b-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f4c0b-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="f4c0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c0b-103">移除 Azure SQL 資料庫同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="f4c0b-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="f4c0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4c0b-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4c0b-105">說明</span><span class="sxs-lookup"><span data-stu-id="f4c0b-105">DESCRIPTION</span></span>
<span data-ttu-id="f4c0b-106">**AzSqlSyncMember** Cmdlet 會移除 Azure SQL 資料庫同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="f4c0b-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="f4c0b-107">示例</span><span class="sxs-lookup"><span data-stu-id="f4c0b-107">EXAMPLES</span></span>

### <span data-ttu-id="f4c0b-108">範例1：移除同步處理成員</span><span class="sxs-lookup"><span data-stu-id="f4c0b-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="f4c0b-109">這個命令會移除名為 syncMember01 的 Azure SQL 資料庫同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="f4c0b-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="f4c0b-110">參數</span><span class="sxs-lookup"><span data-stu-id="f4c0b-110">PARAMETERS</span></span>

### <span data-ttu-id="f4c0b-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4c0b-111">-DatabaseName</span></span>
<span data-ttu-id="f4c0b-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4c0b-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f4c0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4c0b-113">-DefaultProfile</span></span>
<span data-ttu-id="f4c0b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f4c0b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4c0b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f4c0b-115">-Force</span></span>
<span data-ttu-id="f4c0b-116">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="f4c0b-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f4c0b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4c0b-117">-Name</span></span>
<span data-ttu-id="f4c0b-118">同步處理成員名稱。</span><span class="sxs-lookup"><span data-stu-id="f4c0b-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c0b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4c0b-119">-PassThru</span></span>
<span data-ttu-id="f4c0b-120">定義是否傳回已移除的同步處理成員</span><span class="sxs-lookup"><span data-stu-id="f4c0b-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="f4c0b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4c0b-121">-ResourceGroupName</span></span>
<span data-ttu-id="f4c0b-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4c0b-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f4c0b-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f4c0b-123">-ServerName</span></span>
<span data-ttu-id="f4c0b-124">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4c0b-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f4c0b-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f4c0b-125">-SyncGroupName</span></span>
<span data-ttu-id="f4c0b-126">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="f4c0b-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c0b-127">-確認</span><span class="sxs-lookup"><span data-stu-id="f4c0b-127">-Confirm</span></span>
<span data-ttu-id="f4c0b-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4c0b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4c0b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4c0b-129">-WhatIf</span></span>
<span data-ttu-id="f4c0b-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4c0b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4c0b-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4c0b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4c0b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c0b-132">CommonParameters</span></span>
<span data-ttu-id="f4c0b-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4c0b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c0b-134">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f4c0b-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c0b-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f4c0b-135">INPUTS</span></span>

### <span data-ttu-id="f4c0b-136">System.object</span><span class="sxs-lookup"><span data-stu-id="f4c0b-136">System.String</span></span>

## <span data-ttu-id="f4c0b-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f4c0b-137">OUTPUTS</span></span>

### <span data-ttu-id="f4c0b-138">AzureSqlSyncMemberModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="f4c0b-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="f4c0b-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f4c0b-139">NOTES</span></span>

## <span data-ttu-id="f4c0b-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4c0b-140">RELATED LINKS</span></span>

[<span data-ttu-id="f4c0b-141">新-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f4c0b-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="f4c0b-142">更新-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f4c0b-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="f4c0b-143">AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f4c0b-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

