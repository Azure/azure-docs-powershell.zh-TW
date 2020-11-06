---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: bb6beb99171f376fb1ce6ba19b43a93b830457e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452032"
---
# <span data-ttu-id="22887-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="22887-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="22887-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22887-102">SYNOPSIS</span></span>
<span data-ttu-id="22887-103">取得資料庫的資料遮罩原則。</span><span class="sxs-lookup"><span data-stu-id="22887-103">Gets the data masking policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22887-104">句法</span><span class="sxs-lookup"><span data-stu-id="22887-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22887-105">說明</span><span class="sxs-lookup"><span data-stu-id="22887-105">DESCRIPTION</span></span>
<span data-ttu-id="22887-106">**AzureRmSqlDatabaseDataMaskingPolicy** Cmdlet 會取得 Azure SQL 資料庫的資料遮罩原則。</span><span class="sxs-lookup"><span data-stu-id="22887-106">The **Get-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="22887-107">若要使用這個 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="22887-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="22887-108">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22887-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="22887-109">示例</span><span class="sxs-lookup"><span data-stu-id="22887-109">EXAMPLES</span></span>

### <span data-ttu-id="22887-110">範例1：取得 Azure SQL 資料庫的資料遮罩原則</span><span class="sxs-lookup"><span data-stu-id="22887-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="22887-111">這個命令會從伺服器 Server01 的資源群組 ResourceGroup01 中的資料庫 Database01 取得資料遮罩原則。</span><span class="sxs-lookup"><span data-stu-id="22887-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="22887-112">參數</span><span class="sxs-lookup"><span data-stu-id="22887-112">PARAMETERS</span></span>

### <span data-ttu-id="22887-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="22887-113">-DatabaseName</span></span>
<span data-ttu-id="22887-114">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="22887-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="22887-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22887-115">-DefaultProfile</span></span>
<span data-ttu-id="22887-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="22887-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22887-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22887-117">-ResourceGroupName</span></span>
<span data-ttu-id="22887-118">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="22887-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="22887-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="22887-119">-ServerName</span></span>
<span data-ttu-id="22887-120">指定資料庫所在之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="22887-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="22887-121">-確認</span><span class="sxs-lookup"><span data-stu-id="22887-121">-Confirm</span></span>
<span data-ttu-id="22887-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="22887-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22887-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22887-123">-WhatIf</span></span>
<span data-ttu-id="22887-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22887-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22887-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22887-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22887-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22887-126">CommonParameters</span></span>
<span data-ttu-id="22887-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22887-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22887-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22887-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22887-129">輸入</span><span class="sxs-lookup"><span data-stu-id="22887-129">INPUTS</span></span>

### <span data-ttu-id="22887-130">所有</span><span class="sxs-lookup"><span data-stu-id="22887-130">None</span></span>
<span data-ttu-id="22887-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="22887-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22887-132">輸出</span><span class="sxs-lookup"><span data-stu-id="22887-132">OUTPUTS</span></span>

### <span data-ttu-id="22887-133">DatabaseDataMaskingPolicyModel 中的 [.Sql.]</span><span class="sxs-lookup"><span data-stu-id="22887-133">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="22887-134">筆記</span><span class="sxs-lookup"><span data-stu-id="22887-134">NOTES</span></span>

## <span data-ttu-id="22887-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="22887-135">RELATED LINKS</span></span>

[<span data-ttu-id="22887-136">AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="22887-136">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="22887-137">新-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="22887-137">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="22887-138">移除-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="22887-138">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="22887-139">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="22887-139">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="22887-140">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="22887-140">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


