---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/switch-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 708b010a8ff7b2a289d538a07e7b679fcec6efab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625546"
---
# <span data-ttu-id="c257f-101">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c257f-101">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="c257f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c257f-102">SYNOPSIS</span></span>
<span data-ttu-id="c257f-103">執行 Azure SQL Database 容錯移轉群組的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="c257f-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c257f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c257f-104">SYNTAX</span></span>

```
Switch-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c257f-105">說明</span><span class="sxs-lookup"><span data-stu-id="c257f-105">DESCRIPTION</span></span>
<span data-ttu-id="c257f-106">這個命令會交換容錯移轉群組中伺服器的角色，並將所有次要資料庫切換為主要角色。</span><span class="sxs-lookup"><span data-stu-id="c257f-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="c257f-107">在重新整理 DNS 用戶端快取之後，所有新的 TDS 會話都會自動重新路由到從屬伺服器。</span><span class="sxs-lookup"><span data-stu-id="c257f-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="c257f-108">當原始主要伺服器回到線上時，所有先前的主資料庫都會切換到副角色。</span><span class="sxs-lookup"><span data-stu-id="c257f-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="c257f-109">容錯移轉群組的次要伺服器必須用來執行這個命令。</span><span class="sxs-lookup"><span data-stu-id="c257f-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="c257f-110">示例</span><span class="sxs-lookup"><span data-stu-id="c257f-110">EXAMPLES</span></span>

### <span data-ttu-id="c257f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c257f-111">Example 1</span></span>
```
C:\> Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzureRmSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="c257f-112">在容錯移轉群組中，以管道方式發出容錯移轉作業，以使資料遺失。</span><span class="sxs-lookup"><span data-stu-id="c257f-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="c257f-113">範例2</span><span class="sxs-lookup"><span data-stu-id="c257f-113">Example 2</span></span>
```
C:\> Switch-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="c257f-114">在不遺失資料或失敗與回滾的情況下，發出最佳的成功容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="c257f-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="c257f-115">參數</span><span class="sxs-lookup"><span data-stu-id="c257f-115">PARAMETERS</span></span>

### <span data-ttu-id="c257f-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="c257f-116">-AllowDataLoss</span></span>
<span data-ttu-id="c257f-117">完成容錯移轉，即使這樣做可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="c257f-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="c257f-118">這可讓容錯移轉即使在主要資料庫無法使用時仍能繼續進行。</span><span class="sxs-lookup"><span data-stu-id="c257f-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c257f-119">-AsJob</span></span>
<span data-ttu-id="c257f-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c257f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c257f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c257f-121">-DefaultProfile</span></span>
<span data-ttu-id="c257f-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c257f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c257f-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="c257f-123">-FailoverGroupName</span></span>
<span data-ttu-id="c257f-124">Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c257f-124">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c257f-125">-ResourceGroupName</span></span>
<span data-ttu-id="c257f-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c257f-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="c257f-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c257f-127">-ServerName</span></span>
<span data-ttu-id="c257f-128">容錯移轉群組之副 Azure SQL Database 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c257f-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="c257f-129">-確認</span><span class="sxs-lookup"><span data-stu-id="c257f-129">-Confirm</span></span>
<span data-ttu-id="c257f-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c257f-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c257f-131">-WhatIf</span></span>
<span data-ttu-id="c257f-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c257f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c257f-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c257f-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c257f-134">CommonParameters</span></span>
<span data-ttu-id="c257f-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c257f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c257f-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c257f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c257f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="c257f-137">INPUTS</span></span>

### <span data-ttu-id="c257f-138">System.object</span><span class="sxs-lookup"><span data-stu-id="c257f-138">System.String</span></span>

## <span data-ttu-id="c257f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c257f-139">OUTPUTS</span></span>

### <span data-ttu-id="c257f-140">AzureSqlFailoverGroupModel 中的 [FailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="c257f-140">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="c257f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c257f-141">NOTES</span></span>

## <span data-ttu-id="c257f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c257f-142">RELATED LINKS</span></span>

[<span data-ttu-id="c257f-143">新-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c257f-143">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c257f-144">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c257f-144">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c257f-145">AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c257f-145">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c257f-146">附加 AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c257f-146">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="c257f-147">移除-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c257f-147">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="c257f-148">移除-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c257f-148">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c257f-149">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="c257f-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
