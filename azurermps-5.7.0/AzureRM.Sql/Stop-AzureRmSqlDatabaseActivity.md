---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: d0aa42b8b584ade698c3d03848a537350ac342d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624654"
---
# <span data-ttu-id="68f13-101">Stop-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="68f13-101">Stop-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="68f13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68f13-102">SYNOPSIS</span></span>
<span data-ttu-id="68f13-103">取消資料庫上的非同步更新操作。</span><span class="sxs-lookup"><span data-stu-id="68f13-103">Cancels the asynchronous updates operation on the database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68f13-104">句法</span><span class="sxs-lookup"><span data-stu-id="68f13-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68f13-105">說明</span><span class="sxs-lookup"><span data-stu-id="68f13-105">DESCRIPTION</span></span>
<span data-ttu-id="68f13-106">**AzureRmSqlDatabaseActivity** Cmdlet 會取消資料庫上的非同步更新作業。</span><span class="sxs-lookup"><span data-stu-id="68f13-106">The **Stop-AzureRmSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="68f13-107">示例</span><span class="sxs-lookup"><span data-stu-id="68f13-107">EXAMPLES</span></span>

### <span data-ttu-id="68f13-108">範例1：取消對資料庫的非同步更新操作</span><span class="sxs-lookup"><span data-stu-id="68f13-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
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

<span data-ttu-id="68f13-109">這個命令會取消資料庫上的非同步更新操作。</span><span class="sxs-lookup"><span data-stu-id="68f13-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="68f13-110">參數</span><span class="sxs-lookup"><span data-stu-id="68f13-110">PARAMETERS</span></span>

### <span data-ttu-id="68f13-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="68f13-111">-DatabaseName</span></span>
<span data-ttu-id="68f13-112">指定此 Cmdlet 取得狀態之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="68f13-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68f13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f13-113">-DefaultProfile</span></span>
<span data-ttu-id="68f13-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68f13-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68f13-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="68f13-115">-ElasticPoolName</span></span>
<span data-ttu-id="68f13-116">Azure SQL 彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="68f13-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="68f13-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="68f13-117">-OperationId</span></span>
<span data-ttu-id="68f13-118">指定此 Cmdlet 取得的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="68f13-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68f13-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68f13-119">-ResourceGroupName</span></span>
<span data-ttu-id="68f13-120">指定指派給資料庫之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68f13-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="68f13-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="68f13-121">-ServerName</span></span>
<span data-ttu-id="68f13-122">指定裝載資料庫之 Microsoft SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="68f13-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="68f13-123">-確認</span><span class="sxs-lookup"><span data-stu-id="68f13-123">-Confirm</span></span>
<span data-ttu-id="68f13-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="68f13-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68f13-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68f13-125">-WhatIf</span></span>
<span data-ttu-id="68f13-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68f13-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68f13-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68f13-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68f13-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f13-128">CommonParameters</span></span>
<span data-ttu-id="68f13-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68f13-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f13-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68f13-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f13-131">輸入</span><span class="sxs-lookup"><span data-stu-id="68f13-131">INPUTS</span></span>

### <span data-ttu-id="68f13-132">所有</span><span class="sxs-lookup"><span data-stu-id="68f13-132">None</span></span>
<span data-ttu-id="68f13-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="68f13-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="68f13-134">輸出</span><span class="sxs-lookup"><span data-stu-id="68f13-134">OUTPUTS</span></span>

### <span data-ttu-id="68f13-135">AzureSqlDatabaseActivityModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="68f13-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="68f13-136">筆記</span><span class="sxs-lookup"><span data-stu-id="68f13-136">NOTES</span></span>

## <span data-ttu-id="68f13-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="68f13-137">RELATED LINKS</span></span>
