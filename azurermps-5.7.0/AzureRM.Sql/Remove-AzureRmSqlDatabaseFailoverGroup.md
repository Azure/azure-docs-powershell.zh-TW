---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a6fd65ed16797d3d497160f7f7d9d52f17bd2f1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453011"
---
# <span data-ttu-id="8d26f-101">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d26f-101">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="8d26f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d26f-102">SYNOPSIS</span></span>
<span data-ttu-id="8d26f-103">移除 [Azure SQL 資料庫容錯移轉] 群組。</span><span class="sxs-lookup"><span data-stu-id="8d26f-103">Removes an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d26f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d26f-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d26f-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d26f-105">DESCRIPTION</span></span>
<span data-ttu-id="8d26f-106">這個命令會移除具有指定名稱的容錯移轉群組，並將所有資料庫與複製關聯保持不變。</span><span class="sxs-lookup"><span data-stu-id="8d26f-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="8d26f-107">將會從 DNS 登出偵聽程式端點。</span><span class="sxs-lookup"><span data-stu-id="8d26f-107">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="8d26f-108">應使用容錯移轉群組的主要伺服器來執行命令。</span><span class="sxs-lookup"><span data-stu-id="8d26f-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="8d26f-109">示例</span><span class="sxs-lookup"><span data-stu-id="8d26f-109">EXAMPLES</span></span>

### <span data-ttu-id="8d26f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8d26f-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="8d26f-111">移除容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="8d26f-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="8d26f-112">參數</span><span class="sxs-lookup"><span data-stu-id="8d26f-112">PARAMETERS</span></span>

### <span data-ttu-id="8d26f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d26f-113">-DefaultProfile</span></span>
<span data-ttu-id="8d26f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8d26f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d26f-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="8d26f-115">-FailoverGroupName</span></span>
<span data-ttu-id="8d26f-116">要移除之 Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d26f-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="8d26f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8d26f-117">-Force</span></span>
<span data-ttu-id="8d26f-118">跳過確認訊息以執行動作。</span><span class="sxs-lookup"><span data-stu-id="8d26f-118">Skip confirmation message for performing the action.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d26f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d26f-119">-ResourceGroupName</span></span>
<span data-ttu-id="8d26f-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d26f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="8d26f-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8d26f-121">-ServerName</span></span>
<span data-ttu-id="8d26f-122">容錯移轉群組之主要 Azure SQL Database 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d26f-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="8d26f-123">-確認</span><span class="sxs-lookup"><span data-stu-id="8d26f-123">-Confirm</span></span>
<span data-ttu-id="8d26f-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d26f-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d26f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d26f-125">-WhatIf</span></span>
<span data-ttu-id="8d26f-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d26f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d26f-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d26f-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d26f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d26f-128">CommonParameters</span></span>
<span data-ttu-id="8d26f-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d26f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d26f-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8d26f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d26f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8d26f-131">INPUTS</span></span>

### <span data-ttu-id="8d26f-132">System.object</span><span class="sxs-lookup"><span data-stu-id="8d26f-132">System.String</span></span>

## <span data-ttu-id="8d26f-133">輸出</span><span class="sxs-lookup"><span data-stu-id="8d26f-133">OUTPUTS</span></span>

### <span data-ttu-id="8d26f-134">System.object</span><span class="sxs-lookup"><span data-stu-id="8d26f-134">System.Object</span></span>

## <span data-ttu-id="8d26f-135">筆記</span><span class="sxs-lookup"><span data-stu-id="8d26f-135">NOTES</span></span>

## <span data-ttu-id="8d26f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d26f-136">RELATED LINKS</span></span>

[<span data-ttu-id="8d26f-137">新-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d26f-137">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8d26f-138">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d26f-138">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8d26f-139">AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d26f-139">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8d26f-140">附加 AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d26f-140">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="8d26f-141">移除-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d26f-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="8d26f-142">切換 AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d26f-142">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="8d26f-143">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="8d26f-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
