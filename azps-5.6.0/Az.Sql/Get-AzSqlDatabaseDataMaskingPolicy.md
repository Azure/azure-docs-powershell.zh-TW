---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d84a954fc6ca6531f1f485baf2cd8006c8a509bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902170"
---
# <span data-ttu-id="a2dfc-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="a2dfc-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="a2dfc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a2dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="a2dfc-103">獲得資料庫的資料遮罩策略。</span><span class="sxs-lookup"><span data-stu-id="a2dfc-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="a2dfc-104">語法</span><span class="sxs-lookup"><span data-stu-id="a2dfc-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2dfc-105">描述</span><span class="sxs-lookup"><span data-stu-id="a2dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="a2dfc-106">**Get-AzSqlDatabaseDataMaskingPolicy** Cmdlet 會取得 Azure SQL 資料庫的資料遮罩策略。</span><span class="sxs-lookup"><span data-stu-id="a2dfc-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="a2dfc-107">若要使用此 Cmdlet，請使用 *ResourceGroupName、ServerName* 和 *DatabaseName* 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="a2dfc-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="a2dfc-108">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2dfc-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a2dfc-109">例子</span><span class="sxs-lookup"><span data-stu-id="a2dfc-109">EXAMPLES</span></span>

### <span data-ttu-id="a2dfc-110">範例 1：取得 Azure SQL 資料庫的資料遮罩策略</span><span class="sxs-lookup"><span data-stu-id="a2dfc-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="a2dfc-111">此命令會從 Server01 資源群組 ResourceGroup01 中的資料庫 Database01 中，獲得資料遮罩策略。</span><span class="sxs-lookup"><span data-stu-id="a2dfc-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="a2dfc-112">參數</span><span class="sxs-lookup"><span data-stu-id="a2dfc-112">PARAMETERS</span></span>

### <span data-ttu-id="a2dfc-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2dfc-113">-DatabaseName</span></span>
<span data-ttu-id="a2dfc-114">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2dfc-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="a2dfc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2dfc-115">-DefaultProfile</span></span>
<span data-ttu-id="a2dfc-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a2dfc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2dfc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2dfc-117">-ResourceGroupName</span></span>
<span data-ttu-id="a2dfc-118">指定指派資料庫的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a2dfc-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a2dfc-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a2dfc-119">-ServerName</span></span>
<span data-ttu-id="a2dfc-120">指定資料庫所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a2dfc-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="a2dfc-121">-確認</span><span class="sxs-lookup"><span data-stu-id="a2dfc-121">-Confirm</span></span>
<span data-ttu-id="a2dfc-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a2dfc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2dfc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2dfc-123">-WhatIf</span></span>
<span data-ttu-id="a2dfc-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2dfc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2dfc-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2dfc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2dfc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2dfc-126">CommonParameters</span></span>
<span data-ttu-id="a2dfc-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a2dfc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2dfc-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2dfc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2dfc-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a2dfc-129">INPUTS</span></span>

### <span data-ttu-id="a2dfc-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a2dfc-130">System.String</span></span>

## <span data-ttu-id="a2dfc-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a2dfc-131">OUTPUTS</span></span>

### <span data-ttu-id="a2dfc-132">Microsoft.Azure.Commands.sql.DataMasking.model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a2dfc-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="a2dfc-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a2dfc-133">NOTES</span></span>

## <span data-ttu-id="a2dfc-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2dfc-134">RELATED LINKS</span></span>

[<span data-ttu-id="a2dfc-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a2dfc-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a2dfc-136">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a2dfc-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a2dfc-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a2dfc-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a2dfc-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="a2dfc-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="a2dfc-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a2dfc-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


