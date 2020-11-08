---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 4353a61efd0141947879ad6795c321f5ed43e1d3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137267"
---
# <span data-ttu-id="f947a-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f947a-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="f947a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f947a-102">SYNOPSIS</span></span>
<span data-ttu-id="f947a-103">終止 SQL 資料庫與指定的次要資料庫之間的資料複製。</span><span class="sxs-lookup"><span data-stu-id="f947a-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="f947a-104">句法</span><span class="sxs-lookup"><span data-stu-id="f947a-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f947a-105">說明</span><span class="sxs-lookup"><span data-stu-id="f947a-105">DESCRIPTION</span></span>
<span data-ttu-id="f947a-106">**AzSqlDatabaseSecondary** Cmdlet 會強制終止異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="f947a-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="f947a-107">這個 Cmdlet 取代 Stop-AzSqlDatabaseCopy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f947a-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="f947a-108">終止前沒有複製同步處理。</span><span class="sxs-lookup"><span data-stu-id="f947a-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="f947a-109">示例</span><span class="sxs-lookup"><span data-stu-id="f947a-109">EXAMPLES</span></span>

## <span data-ttu-id="f947a-110">參數</span><span class="sxs-lookup"><span data-stu-id="f947a-110">PARAMETERS</span></span>

### <span data-ttu-id="f947a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f947a-111">-DatabaseName</span></span>
<span data-ttu-id="f947a-112">指定具有此 Cmdlet 移除之複製連結的主要 Azure SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="f947a-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f947a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f947a-113">-DefaultProfile</span></span>
<span data-ttu-id="f947a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f947a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f947a-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f947a-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="f947a-116">指定合作夥伴資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f947a-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="f947a-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="f947a-117">-PartnerServerName</span></span>
<span data-ttu-id="f947a-118">指定合作夥伴 SQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f947a-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="f947a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f947a-119">-ResourceGroupName</span></span>
<span data-ttu-id="f947a-120">指定與要移除之複製連結相關聯之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f947a-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="f947a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f947a-121">-ServerName</span></span>
<span data-ttu-id="f947a-122">指定具有要移除之複製連結的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f947a-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="f947a-123">-確認</span><span class="sxs-lookup"><span data-stu-id="f947a-123">-Confirm</span></span>
<span data-ttu-id="f947a-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f947a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f947a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f947a-125">-WhatIf</span></span>
<span data-ttu-id="f947a-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f947a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f947a-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f947a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f947a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f947a-128">CommonParameters</span></span>
<span data-ttu-id="f947a-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f947a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f947a-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f947a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f947a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f947a-131">INPUTS</span></span>

### <span data-ttu-id="f947a-132">System.object</span><span class="sxs-lookup"><span data-stu-id="f947a-132">System.String</span></span>

## <span data-ttu-id="f947a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f947a-133">OUTPUTS</span></span>

### <span data-ttu-id="f947a-134">AzureReplicationLinkModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="f947a-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="f947a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f947a-135">NOTES</span></span>

## <span data-ttu-id="f947a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f947a-136">RELATED LINKS</span></span>

[<span data-ttu-id="f947a-137">新-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f947a-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="f947a-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f947a-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="f947a-139">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="f947a-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
