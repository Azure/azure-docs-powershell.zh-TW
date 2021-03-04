---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 566081ea78137c3816ecee58e76a4811c7f54f62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904265"
---
# <span data-ttu-id="1dd28-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1dd28-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="1dd28-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1dd28-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd28-103">終止 SQL 資料庫與指定次要資料庫之間的資料複製。</span><span class="sxs-lookup"><span data-stu-id="1dd28-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="1dd28-104">語法</span><span class="sxs-lookup"><span data-stu-id="1dd28-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dd28-105">描述</span><span class="sxs-lookup"><span data-stu-id="1dd28-105">DESCRIPTION</span></span>
<span data-ttu-id="1dd28-106">**Remove-AzSqlDatabase二維 Cmdlet** 強制終止異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="1dd28-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="1dd28-107">此 Cmdlet 會取代 Stop-AzSqlDatabaseCopy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dd28-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="1dd28-108">終止之前沒有複製同步處理。</span><span class="sxs-lookup"><span data-stu-id="1dd28-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="1dd28-109">例子</span><span class="sxs-lookup"><span data-stu-id="1dd28-109">EXAMPLES</span></span>

## <span data-ttu-id="1dd28-110">參數</span><span class="sxs-lookup"><span data-stu-id="1dd28-110">PARAMETERS</span></span>

### <span data-ttu-id="1dd28-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1dd28-111">-DatabaseName</span></span>
<span data-ttu-id="1dd28-112">指定具有此 Cmdlet 移除之複製連結的主 Azure SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1dd28-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1dd28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd28-113">-DefaultProfile</span></span>
<span data-ttu-id="1dd28-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1dd28-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dd28-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dd28-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="1dd28-116">指定合作夥伴資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dd28-116">Specifies the name of the partner  resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd28-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="1dd28-117">-PartnerServerName</span></span>
<span data-ttu-id="1dd28-118">指定合作夥伴 SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dd28-118">Specifies the name of the partner SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd28-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dd28-119">-ResourceGroupName</span></span>
<span data-ttu-id="1dd28-120">指定與要移除的複製連結相關聯的資源組名。</span><span class="sxs-lookup"><span data-stu-id="1dd28-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="1dd28-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1dd28-121">-ServerName</span></span>
<span data-ttu-id="1dd28-122">指定要移除複製連結的 SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="1dd28-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="1dd28-123">-確認</span><span class="sxs-lookup"><span data-stu-id="1dd28-123">-Confirm</span></span>
<span data-ttu-id="1dd28-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1dd28-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dd28-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd28-125">-WhatIf</span></span>
<span data-ttu-id="1dd28-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1dd28-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dd28-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dd28-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dd28-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd28-128">CommonParameters</span></span>
<span data-ttu-id="1dd28-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1dd28-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd28-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1dd28-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd28-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1dd28-131">INPUTS</span></span>

### <span data-ttu-id="1dd28-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1dd28-132">System.String</span></span>

## <span data-ttu-id="1dd28-133">輸出</span><span class="sxs-lookup"><span data-stu-id="1dd28-133">OUTPUTS</span></span>

### <span data-ttu-id="1dd28-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="1dd28-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="1dd28-135">筆記</span><span class="sxs-lookup"><span data-stu-id="1dd28-135">NOTES</span></span>

## <span data-ttu-id="1dd28-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dd28-136">RELATED LINKS</span></span>

[<span data-ttu-id="1dd28-137">New-AzSqlDatabase2ary</span><span class="sxs-lookup"><span data-stu-id="1dd28-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="1dd28-138">Set-AzSqlDatabase二一</span><span class="sxs-lookup"><span data-stu-id="1dd28-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="1dd28-139">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="1dd28-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
