---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
ms.openlocfilehash: 6bb2a3891abe8453ee8460f6879dbc134f6ab29b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620464"
---
# <span data-ttu-id="1fef1-101">Get-AzSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="1fef1-101">Get-AzSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="1fef1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fef1-102">SYNOPSIS</span></span>
<span data-ttu-id="1fef1-103">取得 Azure SQL 資料庫與資源群組或 SQL Server 之間的異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="1fef1-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

## <span data-ttu-id="1fef1-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fef1-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fef1-105">說明</span><span class="sxs-lookup"><span data-stu-id="1fef1-105">DESCRIPTION</span></span>
<span data-ttu-id="1fef1-106">**AzSqlDatabaseReplicationLink** Cmdlet 會取代 **AzSqlDatabaseCopy** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1fef1-106">The **Get-AzSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="1fef1-107">它會取得指定 Azure SQL 資料庫與資源群組或 AzureSQL 伺服器之間的所有異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="1fef1-107">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="1fef1-108">示例</span><span class="sxs-lookup"><span data-stu-id="1fef1-108">EXAMPLES</span></span>

## <span data-ttu-id="1fef1-109">參數</span><span class="sxs-lookup"><span data-stu-id="1fef1-109">PARAMETERS</span></span>

### <span data-ttu-id="1fef1-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1fef1-110">-DatabaseName</span></span>
<span data-ttu-id="1fef1-111">指定要取得其連結之 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fef1-111">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="1fef1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fef1-112">-DefaultProfile</span></span>
<span data-ttu-id="1fef1-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1fef1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fef1-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fef1-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="1fef1-115">指定合作夥伴所分派的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fef1-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="1fef1-116">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="1fef1-116">-PartnerServerName</span></span>
<span data-ttu-id="1fef1-117">指定合作夥伴的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="1fef1-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="1fef1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fef1-118">-ResourceGroupName</span></span>
<span data-ttu-id="1fef1-119">指定要取得其連結之資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fef1-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="1fef1-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1fef1-120">-ServerName</span></span>
<span data-ttu-id="1fef1-121">指定要取得其連結之資料庫的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1fef1-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="1fef1-122">-確認</span><span class="sxs-lookup"><span data-stu-id="1fef1-122">-Confirm</span></span>
<span data-ttu-id="1fef1-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1fef1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fef1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fef1-124">-WhatIf</span></span>
<span data-ttu-id="1fef1-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1fef1-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fef1-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1fef1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fef1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fef1-127">CommonParameters</span></span>
<span data-ttu-id="1fef1-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fef1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fef1-129">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1fef1-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fef1-130">輸入</span><span class="sxs-lookup"><span data-stu-id="1fef1-130">INPUTS</span></span>

### <span data-ttu-id="1fef1-131">System.object</span><span class="sxs-lookup"><span data-stu-id="1fef1-131">System.String</span></span>

## <span data-ttu-id="1fef1-132">輸出</span><span class="sxs-lookup"><span data-stu-id="1fef1-132">OUTPUTS</span></span>

### <span data-ttu-id="1fef1-133">AzureReplicationLinkModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="1fef1-133">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="1fef1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="1fef1-134">NOTES</span></span>

## <span data-ttu-id="1fef1-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fef1-135">RELATED LINKS</span></span>

[<span data-ttu-id="1fef1-136">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="1fef1-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)