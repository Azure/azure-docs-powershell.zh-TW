---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 0a641c99af2c0dac668dce2de7c9751dc769de18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913030"
---
# <span data-ttu-id="49fbd-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="49fbd-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="49fbd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="49fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="49fbd-103">設定資料庫的資料遮罩。</span><span class="sxs-lookup"><span data-stu-id="49fbd-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="49fbd-104">語法</span><span class="sxs-lookup"><span data-stu-id="49fbd-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49fbd-105">描述</span><span class="sxs-lookup"><span data-stu-id="49fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="49fbd-106">**Set-AzSqlDatabaseDataMaskingPolicy** Cmdlet 會設定 Azure SQL 資料庫的資料遮罩策略。</span><span class="sxs-lookup"><span data-stu-id="49fbd-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="49fbd-107">若要使用此 Cmdlet，請使用 *ResourceGroupName、ServerName* 和 *DatabaseName* 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="49fbd-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="49fbd-108">您可以設定 *DataMaskingState* 參數來指定是否啟用或停用資料遮罩作業。</span><span class="sxs-lookup"><span data-stu-id="49fbd-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="49fbd-109">如果 Cmdlet 成功且 *使用 PassThru* 參數，除了資料庫識別碼之外，會傳回描述目前資料遮罩策略的物件。</span><span class="sxs-lookup"><span data-stu-id="49fbd-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="49fbd-110">資料庫識別碼包含但不限於 **ResourceGroupName、ServerName** 和 **DatabaseName。**</span><span class="sxs-lookup"><span data-stu-id="49fbd-110">Database identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, and **DatabaseName**.</span></span>
<span data-ttu-id="49fbd-111">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49fbd-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="49fbd-112">例子</span><span class="sxs-lookup"><span data-stu-id="49fbd-112">EXAMPLES</span></span>

### <span data-ttu-id="49fbd-113">範例 1：設定資料庫的資料遮罩策略</span><span class="sxs-lookup"><span data-stu-id="49fbd-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="49fbd-114">此命令會針對伺服器名為 database01 的資料庫設定資料遮罩策略。</span><span class="sxs-lookup"><span data-stu-id="49fbd-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="49fbd-115">參數</span><span class="sxs-lookup"><span data-stu-id="49fbd-115">PARAMETERS</span></span>

### <span data-ttu-id="49fbd-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="49fbd-116">-DatabaseName</span></span>
<span data-ttu-id="49fbd-117">指定設定該策略的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="49fbd-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="49fbd-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="49fbd-118">-DataMaskingState</span></span>
<span data-ttu-id="49fbd-119">指定是否啟用或停用資料遮罩作業。</span><span class="sxs-lookup"><span data-stu-id="49fbd-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="49fbd-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="49fbd-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49fbd-121">啟用</span><span class="sxs-lookup"><span data-stu-id="49fbd-121">Enabled</span></span>
- <span data-ttu-id="49fbd-122">已停用預設值為啟用。</span><span class="sxs-lookup"><span data-stu-id="49fbd-122">Disabled The default value is Enabled.</span></span>

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

### <span data-ttu-id="49fbd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49fbd-123">-DefaultProfile</span></span>
<span data-ttu-id="49fbd-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="49fbd-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49fbd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49fbd-125">-PassThru</span></span>
<span data-ttu-id="49fbd-126">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="49fbd-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="49fbd-127">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="49fbd-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="49fbd-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="49fbd-128">-PrivilegedUsers</span></span>
<span data-ttu-id="49fbd-129">指定具有許可權的使用者 ID 的分號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="49fbd-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="49fbd-130">這些使用者可以查看遮罩資料。</span><span class="sxs-lookup"><span data-stu-id="49fbd-130">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="49fbd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49fbd-131">-ResourceGroupName</span></span>
<span data-ttu-id="49fbd-132">指定指派資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="49fbd-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="49fbd-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="49fbd-133">-ServerName</span></span>
<span data-ttu-id="49fbd-134">指定主託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="49fbd-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="49fbd-135">-確認</span><span class="sxs-lookup"><span data-stu-id="49fbd-135">-Confirm</span></span>
<span data-ttu-id="49fbd-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="49fbd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49fbd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49fbd-137">-WhatIf</span></span>
<span data-ttu-id="49fbd-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49fbd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49fbd-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49fbd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49fbd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49fbd-140">CommonParameters</span></span>
<span data-ttu-id="49fbd-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="49fbd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49fbd-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49fbd-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49fbd-143">輸入</span><span class="sxs-lookup"><span data-stu-id="49fbd-143">INPUTS</span></span>

### <span data-ttu-id="49fbd-144">System.String</span><span class="sxs-lookup"><span data-stu-id="49fbd-144">System.String</span></span>

## <span data-ttu-id="49fbd-145">輸出</span><span class="sxs-lookup"><span data-stu-id="49fbd-145">OUTPUTS</span></span>

### <span data-ttu-id="49fbd-146">Microsoft.Azure.Commands.sql.DataMasking.model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="49fbd-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="49fbd-147">筆記</span><span class="sxs-lookup"><span data-stu-id="49fbd-147">NOTES</span></span>

## <span data-ttu-id="49fbd-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="49fbd-148">RELATED LINKS</span></span>

[<span data-ttu-id="49fbd-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="49fbd-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="49fbd-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="49fbd-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="49fbd-151">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="49fbd-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="49fbd-152">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="49fbd-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="49fbd-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="49fbd-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="49fbd-154">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="49fbd-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


