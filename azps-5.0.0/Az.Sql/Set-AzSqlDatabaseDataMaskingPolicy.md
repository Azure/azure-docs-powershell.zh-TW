---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d4a167871e452cb12533e38793fae463ba6f8dc8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140244"
---
# <span data-ttu-id="6194f-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="6194f-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="6194f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6194f-102">SYNOPSIS</span></span>
<span data-ttu-id="6194f-103">為資料庫設定資料遮罩。</span><span class="sxs-lookup"><span data-stu-id="6194f-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="6194f-104">句法</span><span class="sxs-lookup"><span data-stu-id="6194f-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6194f-105">說明</span><span class="sxs-lookup"><span data-stu-id="6194f-105">DESCRIPTION</span></span>
<span data-ttu-id="6194f-106">**AzSqlDatabaseDataMaskingPolicy** Cmdlet 會設定 Azure SQL 資料庫的資料遮罩原則。</span><span class="sxs-lookup"><span data-stu-id="6194f-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="6194f-107">若要使用這個 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="6194f-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="6194f-108">您可以設定 *DataMaskingState* 參數，以指定是否已啟用或停用資料遮罩作業。</span><span class="sxs-lookup"><span data-stu-id="6194f-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="6194f-109">如果 Cmdlet 成功且使用 *PassThru* 參數，則它會傳回描述目前資料遮罩原則的物件（除了資料庫識別碼之外）。</span><span class="sxs-lookup"><span data-stu-id="6194f-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="6194f-110">資料庫識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 和 **DatabaseName** 。</span><span class="sxs-lookup"><span data-stu-id="6194f-110">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="6194f-111">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6194f-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="6194f-112">示例</span><span class="sxs-lookup"><span data-stu-id="6194f-112">EXAMPLES</span></span>

### <span data-ttu-id="6194f-113">範例1：設定資料庫的資料遮罩原則</span><span class="sxs-lookup"><span data-stu-id="6194f-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="6194f-114">這個命令會在名為 server01 的伺服器上，為名為 database01 的資料庫設定資料遮罩原則。</span><span class="sxs-lookup"><span data-stu-id="6194f-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="6194f-115">參數</span><span class="sxs-lookup"><span data-stu-id="6194f-115">PARAMETERS</span></span>

### <span data-ttu-id="6194f-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6194f-116">-DatabaseName</span></span>
<span data-ttu-id="6194f-117">指定設定策略之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6194f-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="6194f-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="6194f-118">-DataMaskingState</span></span>
<span data-ttu-id="6194f-119">指定是否已啟用或停用資料遮罩操作。</span><span class="sxs-lookup"><span data-stu-id="6194f-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="6194f-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6194f-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6194f-121">後</span><span class="sxs-lookup"><span data-stu-id="6194f-121">Enabled</span></span>
- <span data-ttu-id="6194f-122">已停用預設值。</span><span class="sxs-lookup"><span data-stu-id="6194f-122">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6194f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6194f-123">-DefaultProfile</span></span>
<span data-ttu-id="6194f-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6194f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6194f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6194f-125">-PassThru</span></span>
<span data-ttu-id="6194f-126">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="6194f-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6194f-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="6194f-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6194f-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="6194f-128">-PrivilegedUsers</span></span>
<span data-ttu-id="6194f-129">指定以分號分隔的許可權使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="6194f-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="6194f-130">允許這些使用者查看遮罩資料。</span><span class="sxs-lookup"><span data-stu-id="6194f-130">These users are allowed to view the masking data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6194f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6194f-131">-ResourceGroupName</span></span>
<span data-ttu-id="6194f-132">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6194f-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="6194f-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6194f-133">-ServerName</span></span>
<span data-ttu-id="6194f-134">指定裝載資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="6194f-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="6194f-135">-確認</span><span class="sxs-lookup"><span data-stu-id="6194f-135">-Confirm</span></span>
<span data-ttu-id="6194f-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6194f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6194f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6194f-137">-WhatIf</span></span>
<span data-ttu-id="6194f-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6194f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6194f-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6194f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6194f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6194f-140">CommonParameters</span></span>
<span data-ttu-id="6194f-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6194f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6194f-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6194f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6194f-143">輸入</span><span class="sxs-lookup"><span data-stu-id="6194f-143">INPUTS</span></span>

### <span data-ttu-id="6194f-144">System.object</span><span class="sxs-lookup"><span data-stu-id="6194f-144">System.String</span></span>

## <span data-ttu-id="6194f-145">輸出</span><span class="sxs-lookup"><span data-stu-id="6194f-145">OUTPUTS</span></span>

### <span data-ttu-id="6194f-146">DatabaseDataMaskingPolicyModel 中的 [DataMasking]</span><span class="sxs-lookup"><span data-stu-id="6194f-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="6194f-147">筆記</span><span class="sxs-lookup"><span data-stu-id="6194f-147">NOTES</span></span>

## <span data-ttu-id="6194f-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="6194f-148">RELATED LINKS</span></span>

[<span data-ttu-id="6194f-149">AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="6194f-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="6194f-150">AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="6194f-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="6194f-151">新-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="6194f-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="6194f-152">移除-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="6194f-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="6194f-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="6194f-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="6194f-154">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="6194f-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


