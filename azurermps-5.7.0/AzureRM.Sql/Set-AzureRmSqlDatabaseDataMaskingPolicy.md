---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 26d056b5ad9cdff22f0419f90fad17c3147e0e14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447584"
---
# <span data-ttu-id="02767-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="02767-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="02767-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02767-102">SYNOPSIS</span></span>
<span data-ttu-id="02767-103">為資料庫設定資料遮罩。</span><span class="sxs-lookup"><span data-stu-id="02767-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02767-104">句法</span><span class="sxs-lookup"><span data-stu-id="02767-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02767-105">說明</span><span class="sxs-lookup"><span data-stu-id="02767-105">DESCRIPTION</span></span>
<span data-ttu-id="02767-106">**AzureRmSqlDatabaseDataMaskingPolicy** Cmdlet 會設定 Azure SQL 資料庫的資料遮罩原則。</span><span class="sxs-lookup"><span data-stu-id="02767-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="02767-107">若要使用這個 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="02767-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="02767-108">您可以設定 *DataMaskingState* 參數，以指定是否已啟用或停用資料遮罩作業。</span><span class="sxs-lookup"><span data-stu-id="02767-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>

<span data-ttu-id="02767-109">您也可以設定 *PrivilegedLogins* 參數，以指定允許哪些使用者查看未遮罩的資料。</span><span class="sxs-lookup"><span data-stu-id="02767-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="02767-110">如果 Cmdlet 成功且使用 *PassThru* 參數，則它會傳回描述目前資料遮罩原則的物件（除了資料庫識別碼之外）。</span><span class="sxs-lookup"><span data-stu-id="02767-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="02767-111">資料庫識別碼包括但不限於、 **ResourceGroupName** 、 **ServerName** 和 **DatabaseName** 。</span><span class="sxs-lookup"><span data-stu-id="02767-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="02767-112">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02767-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="02767-113">示例</span><span class="sxs-lookup"><span data-stu-id="02767-113">EXAMPLES</span></span>

### <span data-ttu-id="02767-114">範例1：設定資料庫的資料遮罩原則</span><span class="sxs-lookup"><span data-stu-id="02767-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="02767-115">這個命令會在名為 server01 的伺服器上，為名為 database01 的資料庫設定資料遮罩原則。</span><span class="sxs-lookup"><span data-stu-id="02767-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="02767-116">參數</span><span class="sxs-lookup"><span data-stu-id="02767-116">PARAMETERS</span></span>

### <span data-ttu-id="02767-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="02767-117">-DatabaseName</span></span>
<span data-ttu-id="02767-118">指定設定策略之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="02767-118">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="02767-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="02767-119">-DataMaskingState</span></span>
<span data-ttu-id="02767-120">指定是否已啟用或停用資料遮罩操作。</span><span class="sxs-lookup"><span data-stu-id="02767-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="02767-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="02767-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="02767-122">後</span><span class="sxs-lookup"><span data-stu-id="02767-122">Enabled</span></span>
- <span data-ttu-id="02767-123">禁止</span><span class="sxs-lookup"><span data-stu-id="02767-123">Disabled</span></span>

<span data-ttu-id="02767-124">預設值為 [已啟用]。</span><span class="sxs-lookup"><span data-stu-id="02767-124">The default value is Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02767-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02767-125">-DefaultProfile</span></span>
<span data-ttu-id="02767-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="02767-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02767-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02767-127">-PassThru</span></span>
<span data-ttu-id="02767-128">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="02767-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02767-129">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="02767-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02767-130">-PrivilegedLogins</span><span class="sxs-lookup"><span data-stu-id="02767-130">-PrivilegedLogins</span></span>
<span data-ttu-id="02767-131">指定要從遮罩中排除哪些 SQL 使用者。</span><span class="sxs-lookup"><span data-stu-id="02767-131">Specifies which SQL users are excluded from masking.</span></span>

<span data-ttu-id="02767-132">此參數已棄用，將會從未來版本中移除。</span><span class="sxs-lookup"><span data-stu-id="02767-132">This parameter is deprecated and will be removed from future releases.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02767-133">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="02767-133">-PrivilegedUsers</span></span>
<span data-ttu-id="02767-134">指定以分號分隔的許可權使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="02767-134">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="02767-135">允許這些使用者查看遮罩資料。</span><span class="sxs-lookup"><span data-stu-id="02767-135">These users are allowed to view the masking data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02767-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02767-136">-ResourceGroupName</span></span>
<span data-ttu-id="02767-137">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="02767-137">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="02767-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="02767-138">-ServerName</span></span>
<span data-ttu-id="02767-139">指定裝載資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="02767-139">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="02767-140">-確認</span><span class="sxs-lookup"><span data-stu-id="02767-140">-Confirm</span></span>
<span data-ttu-id="02767-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="02767-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02767-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02767-142">-WhatIf</span></span>
<span data-ttu-id="02767-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02767-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02767-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02767-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02767-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02767-145">CommonParameters</span></span>
<span data-ttu-id="02767-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02767-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02767-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02767-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02767-148">輸入</span><span class="sxs-lookup"><span data-stu-id="02767-148">INPUTS</span></span>

### <span data-ttu-id="02767-149">所有</span><span class="sxs-lookup"><span data-stu-id="02767-149">None</span></span>
<span data-ttu-id="02767-150">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="02767-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02767-151">輸出</span><span class="sxs-lookup"><span data-stu-id="02767-151">OUTPUTS</span></span>

### <span data-ttu-id="02767-152">DatabaseDataMaskingPolicyModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="02767-152">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="02767-153">筆記</span><span class="sxs-lookup"><span data-stu-id="02767-153">NOTES</span></span>

## <span data-ttu-id="02767-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="02767-154">RELATED LINKS</span></span>

[<span data-ttu-id="02767-155">AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="02767-155">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="02767-156">AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="02767-156">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="02767-157">新-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="02767-157">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="02767-158">移除-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="02767-158">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="02767-159">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="02767-159">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="02767-160">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="02767-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


