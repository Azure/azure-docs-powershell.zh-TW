---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 8fb1b8125a6fd0c42bedc00733f3a128846673e4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138137"
---
# <span data-ttu-id="1e492-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="1e492-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="1e492-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e492-102">SYNOPSIS</span></span>
<span data-ttu-id="1e492-103">取得資料庫的資料遮罩原則。</span><span class="sxs-lookup"><span data-stu-id="1e492-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="1e492-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e492-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e492-105">說明</span><span class="sxs-lookup"><span data-stu-id="1e492-105">DESCRIPTION</span></span>
<span data-ttu-id="1e492-106">**AzSqlDatabaseDataMaskingPolicy** Cmdlet 會取得 Azure SQL 資料庫的資料遮罩原則。</span><span class="sxs-lookup"><span data-stu-id="1e492-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="1e492-107">若要使用這個 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="1e492-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="1e492-108">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e492-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1e492-109">示例</span><span class="sxs-lookup"><span data-stu-id="1e492-109">EXAMPLES</span></span>

### <span data-ttu-id="1e492-110">範例1：取得 Azure SQL 資料庫的資料遮罩原則</span><span class="sxs-lookup"><span data-stu-id="1e492-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="1e492-111">這個命令會從伺服器 Server01 的資源群組 ResourceGroup01 中的資料庫 Database01 取得資料遮罩原則。</span><span class="sxs-lookup"><span data-stu-id="1e492-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="1e492-112">參數</span><span class="sxs-lookup"><span data-stu-id="1e492-112">PARAMETERS</span></span>

### <span data-ttu-id="1e492-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1e492-113">-DatabaseName</span></span>
<span data-ttu-id="1e492-114">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e492-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="1e492-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e492-115">-DefaultProfile</span></span>
<span data-ttu-id="1e492-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1e492-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e492-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e492-117">-ResourceGroupName</span></span>
<span data-ttu-id="1e492-118">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e492-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="1e492-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1e492-119">-ServerName</span></span>
<span data-ttu-id="1e492-120">指定資料庫所在之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e492-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="1e492-121">-確認</span><span class="sxs-lookup"><span data-stu-id="1e492-121">-Confirm</span></span>
<span data-ttu-id="1e492-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e492-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e492-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e492-123">-WhatIf</span></span>
<span data-ttu-id="1e492-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e492-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e492-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e492-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e492-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e492-126">CommonParameters</span></span>
<span data-ttu-id="1e492-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e492-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e492-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1e492-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e492-129">輸入</span><span class="sxs-lookup"><span data-stu-id="1e492-129">INPUTS</span></span>

### <span data-ttu-id="1e492-130">System.object</span><span class="sxs-lookup"><span data-stu-id="1e492-130">System.String</span></span>

## <span data-ttu-id="1e492-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1e492-131">OUTPUTS</span></span>

### <span data-ttu-id="1e492-132">DatabaseDataMaskingPolicyModel 中的 [DataMasking]</span><span class="sxs-lookup"><span data-stu-id="1e492-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="1e492-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1e492-133">NOTES</span></span>

## <span data-ttu-id="1e492-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e492-134">RELATED LINKS</span></span>

[<span data-ttu-id="1e492-135">AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1e492-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="1e492-136">新-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1e492-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="1e492-137">移除-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1e492-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="1e492-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="1e492-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="1e492-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1e492-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


