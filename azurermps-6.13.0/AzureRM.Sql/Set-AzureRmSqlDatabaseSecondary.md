---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 56749c265980fc40ee19b60261641f0c98c25da9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449701"
---
# <span data-ttu-id="7eb76-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7eb76-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="7eb76-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7eb76-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb76-103">將次要資料庫切換為主要資料庫，以便啟動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="7eb76-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eb76-104">句法</span><span class="sxs-lookup"><span data-stu-id="7eb76-104">SYNTAX</span></span>

### <span data-ttu-id="7eb76-105">NoOptionsSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7eb76-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb76-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="7eb76-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eb76-107">說明</span><span class="sxs-lookup"><span data-stu-id="7eb76-107">DESCRIPTION</span></span>
<span data-ttu-id="7eb76-108">**AzureRmSqlDatabaseSecondary** Cmdlet 會將次要資料庫切換為主要資料庫，以便啟動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="7eb76-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="7eb76-109">這個 Cmdlet 是設計為一般配置命令，但目前僅限於啟動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="7eb76-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="7eb76-110">指定 *AllowDataLoss* 參數，以在中斷期間啟動強制容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="7eb76-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="7eb76-111">您不需要在執行計畫作業時（例如復原鑽孔）來指定此參數。</span><span class="sxs-lookup"><span data-stu-id="7eb76-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="7eb76-112">在後一種情況下，次要資料庫會在切換前與主要資料庫同步處理。</span><span class="sxs-lookup"><span data-stu-id="7eb76-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="7eb76-113">示例</span><span class="sxs-lookup"><span data-stu-id="7eb76-113">EXAMPLES</span></span>

## <span data-ttu-id="7eb76-114">參數</span><span class="sxs-lookup"><span data-stu-id="7eb76-114">PARAMETERS</span></span>

### <span data-ttu-id="7eb76-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="7eb76-115">-AllowDataLoss</span></span>
<span data-ttu-id="7eb76-116">表示此容錯移轉作業允許資料遺失。</span><span class="sxs-lookup"><span data-stu-id="7eb76-116">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb76-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7eb76-117">-AsJob</span></span>
<span data-ttu-id="7eb76-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7eb76-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7eb76-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7eb76-119">-DatabaseName</span></span>
<span data-ttu-id="7eb76-120">指定 Azure SQL 資料庫副的名稱。</span><span class="sxs-lookup"><span data-stu-id="7eb76-120">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="7eb76-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb76-121">-DefaultProfile</span></span>
<span data-ttu-id="7eb76-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7eb76-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7eb76-123">-容錯移轉</span><span class="sxs-lookup"><span data-stu-id="7eb76-123">-Failover</span></span>
<span data-ttu-id="7eb76-124">表示此操作為容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="7eb76-124">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb76-125">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb76-125">-PartnerResourceGroupName</span></span>
<span data-ttu-id="7eb76-126">指定合作夥伴 Azure SQL 資料庫所指派的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7eb76-126">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="7eb76-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb76-127">-ResourceGroupName</span></span>
<span data-ttu-id="7eb76-128">指定 Azure SQL 資料庫副指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7eb76-128">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="7eb76-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7eb76-129">-ServerName</span></span>
<span data-ttu-id="7eb76-130">指定託管 Azure SQL 資料庫副的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="7eb76-130">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="7eb76-131">-確認</span><span class="sxs-lookup"><span data-stu-id="7eb76-131">-Confirm</span></span>
<span data-ttu-id="7eb76-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7eb76-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eb76-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eb76-133">-WhatIf</span></span>
<span data-ttu-id="7eb76-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7eb76-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eb76-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7eb76-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eb76-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb76-136">CommonParameters</span></span>
<span data-ttu-id="7eb76-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7eb76-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb76-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7eb76-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb76-139">輸入</span><span class="sxs-lookup"><span data-stu-id="7eb76-139">INPUTS</span></span>

### <span data-ttu-id="7eb76-140">System.object</span><span class="sxs-lookup"><span data-stu-id="7eb76-140">System.String</span></span>

## <span data-ttu-id="7eb76-141">輸出</span><span class="sxs-lookup"><span data-stu-id="7eb76-141">OUTPUTS</span></span>

### <span data-ttu-id="7eb76-142">AzureReplicationLinkModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="7eb76-142">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="7eb76-143">筆記</span><span class="sxs-lookup"><span data-stu-id="7eb76-143">NOTES</span></span>

## <span data-ttu-id="7eb76-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="7eb76-144">RELATED LINKS</span></span>

[<span data-ttu-id="7eb76-145">新-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7eb76-145">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="7eb76-146">移除-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7eb76-146">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="7eb76-147">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="7eb76-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
