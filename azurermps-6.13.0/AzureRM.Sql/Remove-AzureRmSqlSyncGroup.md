---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 62f3c74f94ac0e775adc70f4eef9c4250e041145
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455920"
---
# <span data-ttu-id="8d11f-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="8d11f-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="8d11f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d11f-102">SYNOPSIS</span></span>
<span data-ttu-id="8d11f-103">移除 Azure SQL 資料庫同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="8d11f-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d11f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d11f-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d11f-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d11f-105">DESCRIPTION</span></span>
<span data-ttu-id="8d11f-106">**AzureRmSqlSyncGroup** Cmdlet 會移除 Azure SQL 資料庫同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="8d11f-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="8d11f-107">示例</span><span class="sxs-lookup"><span data-stu-id="8d11f-107">EXAMPLES</span></span>

### <span data-ttu-id="8d11f-108">範例1：移除同步處理群組</span><span class="sxs-lookup"><span data-stu-id="8d11f-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="8d11f-109">這個命令會移除名為 syncGroup01 的 Azure SQL 資料庫同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="8d11f-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="8d11f-110">參數</span><span class="sxs-lookup"><span data-stu-id="8d11f-110">PARAMETERS</span></span>

### <span data-ttu-id="8d11f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8d11f-111">-DatabaseName</span></span>
<span data-ttu-id="8d11f-112">Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d11f-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="8d11f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d11f-113">-DefaultProfile</span></span>
<span data-ttu-id="8d11f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8d11f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d11f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8d11f-115">-Force</span></span>
<span data-ttu-id="8d11f-116">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="8d11f-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="8d11f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d11f-117">-Name</span></span>
<span data-ttu-id="8d11f-118">同步處理組名。</span><span class="sxs-lookup"><span data-stu-id="8d11f-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d11f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d11f-119">-PassThru</span></span>
<span data-ttu-id="8d11f-120">定義是否傳回已移除的同步處理群組</span><span class="sxs-lookup"><span data-stu-id="8d11f-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="8d11f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d11f-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d11f-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d11f-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="8d11f-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8d11f-123">-ServerName</span></span>
<span data-ttu-id="8d11f-124">Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d11f-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="8d11f-125">-確認</span><span class="sxs-lookup"><span data-stu-id="8d11f-125">-Confirm</span></span>
<span data-ttu-id="8d11f-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d11f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d11f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d11f-127">-WhatIf</span></span>
<span data-ttu-id="8d11f-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d11f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d11f-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d11f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d11f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d11f-130">CommonParameters</span></span>
<span data-ttu-id="8d11f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d11f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d11f-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8d11f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d11f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="8d11f-133">INPUTS</span></span>

### <span data-ttu-id="8d11f-134">System.object</span><span class="sxs-lookup"><span data-stu-id="8d11f-134">System.String</span></span>

## <span data-ttu-id="8d11f-135">輸出</span><span class="sxs-lookup"><span data-stu-id="8d11f-135">OUTPUTS</span></span>

### <span data-ttu-id="8d11f-136">AzureSqlSyncGroupModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="8d11f-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="8d11f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="8d11f-137">NOTES</span></span>

## <span data-ttu-id="8d11f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d11f-138">RELATED LINKS</span></span>

[<span data-ttu-id="8d11f-139">新-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="8d11f-139">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="8d11f-140">更新-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="8d11f-140">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="8d11f-141">AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="8d11f-141">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

