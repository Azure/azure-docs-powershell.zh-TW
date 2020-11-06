---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
ms.openlocfilehash: 993d7ef8958e96cebcd104d25550e860cdfd1853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452708"
---
# <span data-ttu-id="1e044-101">Get-AzureRmSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="1e044-101">Get-AzureRmSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="1e044-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e044-102">SYNOPSIS</span></span>
<span data-ttu-id="1e044-103">取得 Azure SQL 資料庫與資源群組或 SQL Server 之間的異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="1e044-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e044-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e044-104">SYNTAX</span></span>

### <span data-ttu-id="1e044-105">ByDatabaseName (預設) </span><span class="sxs-lookup"><span data-stu-id="1e044-105">ByDatabaseName (Default)</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e044-106">ByPartnerServerName</span><span class="sxs-lookup"><span data-stu-id="1e044-106">ByPartnerServerName</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e044-107">說明</span><span class="sxs-lookup"><span data-stu-id="1e044-107">DESCRIPTION</span></span>
<span data-ttu-id="1e044-108">**AzureRMSqlDatabaseReplicationLink** Cmdlet 會取代 **AzureSqlDatabaseCopy** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e044-108">The **Get-AzureRMSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="1e044-109">它會取得指定 Azure SQL 資料庫與資源群組或 AzureSQL 伺服器之間的所有異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="1e044-109">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="1e044-110">示例</span><span class="sxs-lookup"><span data-stu-id="1e044-110">EXAMPLES</span></span>

## <span data-ttu-id="1e044-111">參數</span><span class="sxs-lookup"><span data-stu-id="1e044-111">PARAMETERS</span></span>

### <span data-ttu-id="1e044-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1e044-112">-DatabaseName</span></span>
<span data-ttu-id="1e044-113">指定要取得其連結之 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e044-113">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="1e044-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e044-114">-DefaultProfile</span></span>
<span data-ttu-id="1e044-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1e044-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e044-116">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e044-116">-PartnerResourceGroupName</span></span>
<span data-ttu-id="1e044-117">指定合作夥伴所分派的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e044-117">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="1e044-118">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="1e044-118">-PartnerServerName</span></span>
<span data-ttu-id="1e044-119">指定合作夥伴的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="1e044-119">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPartnerServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e044-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e044-120">-ResourceGroupName</span></span>
<span data-ttu-id="1e044-121">指定要取得其連結之資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e044-121">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="1e044-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1e044-122">-ServerName</span></span>
<span data-ttu-id="1e044-123">指定要取得其連結之資料庫的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1e044-123">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="1e044-124">-確認</span><span class="sxs-lookup"><span data-stu-id="1e044-124">-Confirm</span></span>
<span data-ttu-id="1e044-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e044-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e044-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e044-126">-WhatIf</span></span>
<span data-ttu-id="1e044-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e044-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e044-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e044-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e044-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e044-129">CommonParameters</span></span>
<span data-ttu-id="1e044-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e044-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e044-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e044-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e044-132">輸入</span><span class="sxs-lookup"><span data-stu-id="1e044-132">INPUTS</span></span>

### <span data-ttu-id="1e044-133">System.object</span><span class="sxs-lookup"><span data-stu-id="1e044-133">System.String</span></span>

## <span data-ttu-id="1e044-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1e044-134">OUTPUTS</span></span>

### <span data-ttu-id="1e044-135">AzureReplicationLinkModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="1e044-135">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="1e044-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1e044-136">NOTES</span></span>

## <span data-ttu-id="1e044-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e044-137">RELATED LINKS</span></span>

[<span data-ttu-id="1e044-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="1e044-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
