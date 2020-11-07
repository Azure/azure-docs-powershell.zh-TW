---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 1305e9e74b0f8a2ef1a8d866d4a2dd6d62e1cef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624983"
---
# <span data-ttu-id="74a2b-101">New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="74a2b-101">New-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="74a2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="74a2b-103">建立可還原 SQL 資料庫的新還原點。</span><span class="sxs-lookup"><span data-stu-id="74a2b-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74a2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="74a2b-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74a2b-105">說明</span><span class="sxs-lookup"><span data-stu-id="74a2b-105">DESCRIPTION</span></span>
<span data-ttu-id="74a2b-106">**新的-AzureRmSqlDatabaseRestorePoint** Cmdlet 會建立可從中還原 Azure SQL 資料庫的新還原點。</span><span class="sxs-lookup"><span data-stu-id="74a2b-106">The **New-AzureRmSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Database can be restored from.</span></span>

<span data-ttu-id="74a2b-107">Azure SQL Database 上的 SQL Server 資料倉儲服務目前支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74a2b-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="74a2b-108">示例</span><span class="sxs-lookup"><span data-stu-id="74a2b-108">EXAMPLES</span></span>

### <span data-ttu-id="74a2b-109">範例1：建立還原點</span><span class="sxs-lookup"><span data-stu-id="74a2b-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="74a2b-110">這個命令會建立 Azure SQL 資料庫的還原點，並傳回還原點的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="74a2b-110">This command creates a restore point for Azure SQL Database and returns the details of the restore point.</span></span>

## <span data-ttu-id="74a2b-111">參數</span><span class="sxs-lookup"><span data-stu-id="74a2b-111">PARAMETERS</span></span>

### <span data-ttu-id="74a2b-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="74a2b-112">-DatabaseName</span></span>
<span data-ttu-id="74a2b-113">指定 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="74a2b-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="74a2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a2b-114">-DefaultProfile</span></span>
<span data-ttu-id="74a2b-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="74a2b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74a2b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a2b-116">-ResourceGroupName</span></span>
<span data-ttu-id="74a2b-117">指定指派 SQL 資料庫的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="74a2b-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="74a2b-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="74a2b-118">-RestorePointLabel</span></span>
<span data-ttu-id="74a2b-119">指定還原點的標籤，輕鬆識別。</span><span class="sxs-lookup"><span data-stu-id="74a2b-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="74a2b-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="74a2b-120">-ServerName</span></span>
<span data-ttu-id="74a2b-121">指定裝載資料庫之 AzureSQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="74a2b-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="74a2b-122">-確認</span><span class="sxs-lookup"><span data-stu-id="74a2b-122">-Confirm</span></span>
<span data-ttu-id="74a2b-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74a2b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74a2b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74a2b-124">-WhatIf</span></span>
<span data-ttu-id="74a2b-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74a2b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74a2b-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74a2b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74a2b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a2b-127">CommonParameters</span></span>
<span data-ttu-id="74a2b-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74a2b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a2b-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74a2b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a2b-130">輸入</span><span class="sxs-lookup"><span data-stu-id="74a2b-130">INPUTS</span></span>

## <span data-ttu-id="74a2b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="74a2b-131">OUTPUTS</span></span>

## <span data-ttu-id="74a2b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="74a2b-132">NOTES</span></span>

## <span data-ttu-id="74a2b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="74a2b-133">RELATED LINKS</span></span>
