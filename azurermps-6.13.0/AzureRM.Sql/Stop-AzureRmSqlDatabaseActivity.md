---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: af2f10b371eb21558a4b675331ec97f797611d26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448166"
---
# <span data-ttu-id="7c269-101">Stop-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="7c269-101">Stop-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="7c269-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c269-102">SYNOPSIS</span></span>
<span data-ttu-id="7c269-103">取消資料庫上的非同步更新操作。</span><span class="sxs-lookup"><span data-stu-id="7c269-103">Cancels the asynchronous updates operation on the database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c269-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c269-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c269-105">說明</span><span class="sxs-lookup"><span data-stu-id="7c269-105">DESCRIPTION</span></span>
<span data-ttu-id="7c269-106">**AzureRmSqlDatabaseActivity** Cmdlet 會取消資料庫上的非同步更新作業。</span><span class="sxs-lookup"><span data-stu-id="7c269-106">The **Stop-AzureRmSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="7c269-107">示例</span><span class="sxs-lookup"><span data-stu-id="7c269-107">EXAMPLES</span></span>

### <span data-ttu-id="7c269-108">範例1：取消對資料庫的非同步更新操作</span><span class="sxs-lookup"><span data-stu-id="7c269-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : Database01
State           : CANCELLED
Operation       : UpdateLogicalDatabase
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
Properties      : Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel+DatabaseState
```

<span data-ttu-id="7c269-109">這個命令會取消資料庫上的非同步更新操作。</span><span class="sxs-lookup"><span data-stu-id="7c269-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="7c269-110">參數</span><span class="sxs-lookup"><span data-stu-id="7c269-110">PARAMETERS</span></span>

### <span data-ttu-id="7c269-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7c269-111">-DatabaseName</span></span>
<span data-ttu-id="7c269-112">指定此 Cmdlet 取得狀態之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c269-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="7c269-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c269-113">-DefaultProfile</span></span>
<span data-ttu-id="7c269-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c269-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c269-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7c269-115">-ElasticPoolName</span></span>
<span data-ttu-id="7c269-116">Azure SQL 彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c269-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="7c269-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7c269-117">-OperationId</span></span>
<span data-ttu-id="7c269-118">指定此 Cmdlet 取得的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="7c269-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c269-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c269-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c269-120">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c269-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="7c269-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7c269-121">-ServerName</span></span>
<span data-ttu-id="7c269-122">指定裝載資料庫之 Microsoft SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c269-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="7c269-123">-確認</span><span class="sxs-lookup"><span data-stu-id="7c269-123">-Confirm</span></span>
<span data-ttu-id="7c269-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7c269-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c269-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c269-125">-WhatIf</span></span>
<span data-ttu-id="7c269-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c269-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c269-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c269-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c269-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c269-128">CommonParameters</span></span>
<span data-ttu-id="7c269-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c269-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c269-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c269-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c269-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7c269-131">INPUTS</span></span>

### <span data-ttu-id="7c269-132">System.object</span><span class="sxs-lookup"><span data-stu-id="7c269-132">System.String</span></span>

### <span data-ttu-id="7c269-133">系統. Nullable "1 [[System. Guid，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7c269-133">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7c269-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7c269-134">OUTPUTS</span></span>

### <span data-ttu-id="7c269-135">AzureSqlDatabaseActivityModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="7c269-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="7c269-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7c269-136">NOTES</span></span>

## <span data-ttu-id="7c269-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c269-137">RELATED LINKS</span></span>
