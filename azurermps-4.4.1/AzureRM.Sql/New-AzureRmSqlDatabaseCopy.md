---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: a962ca86c3d65cd11da4169626ed932bb78653b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626203"
---
# <span data-ttu-id="8931c-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8931c-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="8931c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8931c-102">SYNOPSIS</span></span>
<span data-ttu-id="8931c-103">建立在目前時間使用快照的 SQL 資料庫複本。</span><span class="sxs-lookup"><span data-stu-id="8931c-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8931c-104">句法</span><span class="sxs-lookup"><span data-stu-id="8931c-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8931c-105">說明</span><span class="sxs-lookup"><span data-stu-id="8931c-105">DESCRIPTION</span></span>
<span data-ttu-id="8931c-106">**新的-AzureRmSqlDatabaseCopy** Cmdlet 會建立 Azure SQL Database 的複本，此資料庫會在目前時間使用資料的快照。</span><span class="sxs-lookup"><span data-stu-id="8931c-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="8931c-107">使用這個 Cmdlet （而不是 Start-AzureSqlDatabaseCopy Cmdlet）來建立一次性的資料庫複本。</span><span class="sxs-lookup"><span data-stu-id="8931c-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="8931c-108">這個 Cmdlet 會傳回復本的 **資料庫** 物件。</span><span class="sxs-lookup"><span data-stu-id="8931c-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="8931c-109">注意：請使用 New-AzureRmSqlDatabaseSecondary Cmdlet 來設定資料庫的異地複製。</span><span class="sxs-lookup"><span data-stu-id="8931c-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="8931c-110">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8931c-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8931c-111">示例</span><span class="sxs-lookup"><span data-stu-id="8931c-111">EXAMPLES</span></span>

## <span data-ttu-id="8931c-112">參數</span><span class="sxs-lookup"><span data-stu-id="8931c-112">PARAMETERS</span></span>

### <span data-ttu-id="8931c-113">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8931c-113">-CopyDatabaseName</span></span>
<span data-ttu-id="8931c-114">指定 SQL 資料庫複本的名稱。</span><span class="sxs-lookup"><span data-stu-id="8931c-114">Specifies the name of the SQL Database copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8931c-115">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8931c-115">-CopyResourceGroupName</span></span>
<span data-ttu-id="8931c-116">指定要在其中指派複本的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8931c-116">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8931c-117">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="8931c-117">-CopyServerName</span></span>
<span data-ttu-id="8931c-118">指定主持複本的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="8931c-118">Specifies the name of the SQL Server which hosts the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8931c-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8931c-119">-DatabaseName</span></span>
<span data-ttu-id="8931c-120">指定要複製的 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8931c-120">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="8931c-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8931c-121">-ElasticPoolName</span></span>
<span data-ttu-id="8931c-122">指定要在其中指派複本的彈性池名稱。</span><span class="sxs-lookup"><span data-stu-id="8931c-122">Specifies the name of the elastic pool in which to assign the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8931c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8931c-123">-ResourceGroupName</span></span>
<span data-ttu-id="8931c-124">指定此 Cmdlet 指派複製之資料庫的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8931c-124">Specifies the name of the  Resource Group to which this cmdlet assigns the copied database.</span></span>

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

### <span data-ttu-id="8931c-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8931c-125">-ServerName</span></span>
<span data-ttu-id="8931c-126">指定包含要複製之資料庫的 SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="8931c-126">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="8931c-127">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="8931c-127">-ServiceObjectiveName</span></span>
<span data-ttu-id="8931c-128">指定要指派給複本之服務目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="8931c-128">Specifies the name of the service objective to assign to the copy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8931c-129">-標記</span><span class="sxs-lookup"><span data-stu-id="8931c-129">-Tags</span></span>
<span data-ttu-id="8931c-130">指定雜湊資料表形式的鍵值對，以與 Azure SQL 資料庫複本建立關聯。</span><span class="sxs-lookup"><span data-stu-id="8931c-130">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="8931c-131">例如：</span><span class="sxs-lookup"><span data-stu-id="8931c-131">For example:</span></span>

<span data-ttu-id="8931c-132">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8931c-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8931c-133">-確認</span><span class="sxs-lookup"><span data-stu-id="8931c-133">-Confirm</span></span>
<span data-ttu-id="8931c-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8931c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8931c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8931c-135">-WhatIf</span></span>
<span data-ttu-id="8931c-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8931c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8931c-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8931c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8931c-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8931c-138">-DefaultProfile</span></span>
<span data-ttu-id="8931c-139">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8931c-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8931c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8931c-140">CommonParameters</span></span>
<span data-ttu-id="8931c-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8931c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8931c-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8931c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8931c-143">輸入</span><span class="sxs-lookup"><span data-stu-id="8931c-143">INPUTS</span></span>

## <span data-ttu-id="8931c-144">輸出</span><span class="sxs-lookup"><span data-stu-id="8931c-144">OUTPUTS</span></span>

### <span data-ttu-id="8931c-145">AzureSqlDatabaseCopyModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="8931c-145">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="8931c-146">這個 Cmdlet 會傳回代表複製資料庫的 **資料庫** 物件。</span><span class="sxs-lookup"><span data-stu-id="8931c-146">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="8931c-147">筆記</span><span class="sxs-lookup"><span data-stu-id="8931c-147">NOTES</span></span>

## <span data-ttu-id="8931c-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="8931c-148">RELATED LINKS</span></span>

[<span data-ttu-id="8931c-149">新-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8931c-149">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="8931c-150">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="8931c-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
