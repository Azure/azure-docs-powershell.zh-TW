---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: d2dc1b6acf1978976ce29adea2e79146828accb1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138429"
---
# <span data-ttu-id="e7b03-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="e7b03-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="e7b03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7b03-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b03-103">建立可還原 SQL 資料庫的新還原點。</span><span class="sxs-lookup"><span data-stu-id="e7b03-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="e7b03-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7b03-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7b03-105">說明</span><span class="sxs-lookup"><span data-stu-id="e7b03-105">DESCRIPTION</span></span>
<span data-ttu-id="e7b03-106">**新的-AzSqlDatabaseRestorePoint** Cmdlet 會建立新的還原點，以便從 Azure SQL 資料倉儲還原。</span><span class="sxs-lookup"><span data-stu-id="e7b03-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="e7b03-107">Azure SQL 資料倉儲目前支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7b03-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="e7b03-108">示例</span><span class="sxs-lookup"><span data-stu-id="e7b03-108">EXAMPLES</span></span>

### <span data-ttu-id="e7b03-109">範例1：建立還原點</span><span class="sxs-lookup"><span data-stu-id="e7b03-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="e7b03-110">這個命令會建立 Azure SQL 資料倉儲的還原點，並傳回還原點的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e7b03-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="e7b03-111">參數</span><span class="sxs-lookup"><span data-stu-id="e7b03-111">PARAMETERS</span></span>

### <span data-ttu-id="e7b03-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7b03-112">-DatabaseName</span></span>
<span data-ttu-id="e7b03-113">指定 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7b03-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="e7b03-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b03-114">-DefaultProfile</span></span>
<span data-ttu-id="e7b03-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e7b03-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7b03-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7b03-116">-ResourceGroupName</span></span>
<span data-ttu-id="e7b03-117">指定指派 SQL 資料庫的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7b03-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="e7b03-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="e7b03-118">-RestorePointLabel</span></span>
<span data-ttu-id="e7b03-119">指定還原點的標籤，輕鬆識別。</span><span class="sxs-lookup"><span data-stu-id="e7b03-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="e7b03-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e7b03-120">-ServerName</span></span>
<span data-ttu-id="e7b03-121">指定裝載資料庫之 AzureSQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7b03-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="e7b03-122">-確認</span><span class="sxs-lookup"><span data-stu-id="e7b03-122">-Confirm</span></span>
<span data-ttu-id="e7b03-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e7b03-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7b03-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7b03-124">-WhatIf</span></span>
<span data-ttu-id="e7b03-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e7b03-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7b03-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e7b03-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7b03-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b03-127">CommonParameters</span></span>
<span data-ttu-id="e7b03-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7b03-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b03-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e7b03-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b03-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e7b03-130">INPUTS</span></span>

### <span data-ttu-id="e7b03-131">System.object</span><span class="sxs-lookup"><span data-stu-id="e7b03-131">System.String</span></span>

## <span data-ttu-id="e7b03-132">輸出</span><span class="sxs-lookup"><span data-stu-id="e7b03-132">OUTPUTS</span></span>

### <span data-ttu-id="e7b03-133">AzureSqlDatabaseRestorePointModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="e7b03-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="e7b03-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e7b03-134">NOTES</span></span>

## <span data-ttu-id="e7b03-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7b03-135">RELATED LINKS</span></span>
