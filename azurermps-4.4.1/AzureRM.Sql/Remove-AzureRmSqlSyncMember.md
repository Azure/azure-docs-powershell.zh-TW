---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncMember.md
ms.openlocfilehash: d57e73c71e95fe673f9b54d9129714ca22670d31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457228"
---
# <span data-ttu-id="84d44-101">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="84d44-101">Remove-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="84d44-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84d44-102">SYNOPSIS</span></span>
<span data-ttu-id="84d44-103">移除 Azure SQL 資料庫同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="84d44-103">Removes an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84d44-104">句法</span><span class="sxs-lookup"><span data-stu-id="84d44-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84d44-105">說明</span><span class="sxs-lookup"><span data-stu-id="84d44-105">DESCRIPTION</span></span>
<span data-ttu-id="84d44-106">**AzureRmSqlSyncMember** Cmdlet 會移除 Azure SQL 資料庫同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="84d44-106">The **Remove-AzureRmSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="84d44-107">示例</span><span class="sxs-lookup"><span data-stu-id="84d44-107">EXAMPLES</span></span>

### <span data-ttu-id="84d44-108">範例1：移除同步處理成員</span><span class="sxs-lookup"><span data-stu-id="84d44-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="84d44-109">這個命令會移除名為 syncMember01 的 Azure SQL 資料庫同步處理成員。</span><span class="sxs-lookup"><span data-stu-id="84d44-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="84d44-110">參數</span><span class="sxs-lookup"><span data-stu-id="84d44-110">PARAMETERS</span></span>

### <span data-ttu-id="84d44-111">-確認</span><span class="sxs-lookup"><span data-stu-id="84d44-111">-Confirm</span></span>
<span data-ttu-id="84d44-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="84d44-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84d44-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="84d44-113">-DatabaseName</span></span>
<span data-ttu-id="84d44-114">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="84d44-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="84d44-115">-Force</span><span class="sxs-lookup"><span data-stu-id="84d44-115">-Force</span></span>
<span data-ttu-id="84d44-116">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="84d44-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="84d44-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="84d44-117">-Name</span></span>
<span data-ttu-id="84d44-118">同步處理成員名稱。</span><span class="sxs-lookup"><span data-stu-id="84d44-118">The sync member name.</span></span>

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

### <span data-ttu-id="84d44-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84d44-119">-PassThru</span></span>
<span data-ttu-id="84d44-120">定義是否傳回已移除的同步處理成員</span><span class="sxs-lookup"><span data-stu-id="84d44-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="84d44-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84d44-121">-ResourceGroupName</span></span>
<span data-ttu-id="84d44-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="84d44-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="84d44-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="84d44-123">-ServerName</span></span>
<span data-ttu-id="84d44-124">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="84d44-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="84d44-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="84d44-125">-SyncGroupName</span></span>
<span data-ttu-id="84d44-126">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="84d44-126">The sync group name.</span></span>

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

### <span data-ttu-id="84d44-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84d44-127">-WhatIf</span></span>
<span data-ttu-id="84d44-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84d44-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84d44-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84d44-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84d44-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d44-130">-DefaultProfile</span></span>
<span data-ttu-id="84d44-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84d44-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84d44-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d44-132">CommonParameters</span></span>
<span data-ttu-id="84d44-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84d44-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d44-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="84d44-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d44-135">輸入</span><span class="sxs-lookup"><span data-stu-id="84d44-135">INPUTS</span></span>

## <span data-ttu-id="84d44-136">輸出</span><span class="sxs-lookup"><span data-stu-id="84d44-136">OUTPUTS</span></span>

### <span data-ttu-id="84d44-137">AzureSqlSyncMemberModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="84d44-137">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="84d44-138">筆記</span><span class="sxs-lookup"><span data-stu-id="84d44-138">NOTES</span></span>

## <span data-ttu-id="84d44-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="84d44-139">RELATED LINKS</span></span>

[<span data-ttu-id="84d44-140">新-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="84d44-140">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="84d44-141">更新-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="84d44-141">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="84d44-142">AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="84d44-142">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

