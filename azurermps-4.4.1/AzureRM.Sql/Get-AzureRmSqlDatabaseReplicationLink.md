---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
ms.openlocfilehash: 05b090de647f1c6e6abfb7f2c83e5bd0a4cf616b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453251"
---
# <span data-ttu-id="8aaa2-101">Get-AzureRmSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="8aaa2-101">Get-AzureRmSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="8aaa2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8aaa2-102">SYNOPSIS</span></span>
<span data-ttu-id="8aaa2-103">取得 Azure SQL 資料庫與資源群組或 SQL Server 之間的異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8aaa2-104">句法</span><span class="sxs-lookup"><span data-stu-id="8aaa2-104">SYNTAX</span></span>

### <span data-ttu-id="8aaa2-105">ByDatabaseName (預設) </span><span class="sxs-lookup"><span data-stu-id="8aaa2-105">ByDatabaseName (Default)</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aaa2-106">ByPartnerServerName</span><span class="sxs-lookup"><span data-stu-id="8aaa2-106">ByPartnerServerName</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8aaa2-107">說明</span><span class="sxs-lookup"><span data-stu-id="8aaa2-107">DESCRIPTION</span></span>
<span data-ttu-id="8aaa2-108">**AzureRMSqlDatabaseReplicationLink** Cmdlet 會取代 **AzureSqlDatabaseCopy** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-108">The **Get-AzureRMSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="8aaa2-109">它會取得指定 Azure SQL 資料庫與資源群組或 AzureSQL 伺服器之間的所有異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-109">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="8aaa2-110">示例</span><span class="sxs-lookup"><span data-stu-id="8aaa2-110">EXAMPLES</span></span>

## <span data-ttu-id="8aaa2-111">參數</span><span class="sxs-lookup"><span data-stu-id="8aaa2-111">PARAMETERS</span></span>

### <span data-ttu-id="8aaa2-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8aaa2-112">-DatabaseName</span></span>
<span data-ttu-id="8aaa2-113">指定要取得其連結之 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-113">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="8aaa2-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aaa2-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="8aaa2-115">指定合作夥伴所分派的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="8aaa2-116">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="8aaa2-116">-PartnerServerName</span></span>
<span data-ttu-id="8aaa2-117">指定合作夥伴的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

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

### <span data-ttu-id="8aaa2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aaa2-118">-ResourceGroupName</span></span>
<span data-ttu-id="8aaa2-119">指定要取得其連結之資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="8aaa2-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8aaa2-120">-ServerName</span></span>
<span data-ttu-id="8aaa2-121">指定要取得其連結之資料庫的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="8aaa2-122">-確認</span><span class="sxs-lookup"><span data-stu-id="8aaa2-122">-Confirm</span></span>
<span data-ttu-id="8aaa2-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aaa2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aaa2-124">-WhatIf</span></span>
<span data-ttu-id="8aaa2-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8aaa2-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aaa2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aaa2-127">-DefaultProfile</span></span>
<span data-ttu-id="8aaa2-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8aaa2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aaa2-129">CommonParameters</span></span>
<span data-ttu-id="8aaa2-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aaa2-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aaa2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="8aaa2-132">INPUTS</span></span>

###  
<span data-ttu-id="8aaa2-133">這個 Cmdlet 接受主要或次要資料庫的 **ReplicationLink** 或 **資料庫** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-133">This cmdlet accepts instances of the **ReplicationLink** or the **Database** object for the primary or secondary database.</span></span>

## <span data-ttu-id="8aaa2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8aaa2-134">OUTPUTS</span></span>

###  
<span data-ttu-id="8aaa2-135">這個 Cmdlet 會傳回 **ReplicationLink** 物件。</span><span class="sxs-lookup"><span data-stu-id="8aaa2-135">This cmdlet returns a **ReplicationLink** object.</span></span>

## <span data-ttu-id="8aaa2-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8aaa2-136">NOTES</span></span>

## <span data-ttu-id="8aaa2-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8aaa2-137">RELATED LINKS</span></span>

[<span data-ttu-id="8aaa2-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="8aaa2-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
