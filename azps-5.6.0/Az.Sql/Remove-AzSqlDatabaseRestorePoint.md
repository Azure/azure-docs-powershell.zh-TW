---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 476340114ae2bc6e436301f37a0a9aeaf9fa5e92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903402"
---
# <span data-ttu-id="97785-101">Remove-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="97785-101">Remove-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="97785-102">簡介</span><span class="sxs-lookup"><span data-stu-id="97785-102">SYNOPSIS</span></span>
<span data-ttu-id="97785-103">從 SQL Database 移除提供還原點。</span><span class="sxs-lookup"><span data-stu-id="97785-103">Removes given restore point from a SQL Database.</span></span>

## <span data-ttu-id="97785-104">語法</span><span class="sxs-lookup"><span data-stu-id="97785-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97785-105">描述</span><span class="sxs-lookup"><span data-stu-id="97785-105">DESCRIPTION</span></span>
<span data-ttu-id="97785-106">**Remove-AzSqlDatabaseRestorePoint** Cmdlet 會從 Azure SQL Database 移除提供還原點。</span><span class="sxs-lookup"><span data-stu-id="97785-106">The **Remove-AzSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="97785-107">Azure SQL Database 上的 SQL Server Datawarehouse Service 目前支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97785-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="97785-108">例子</span><span class="sxs-lookup"><span data-stu-id="97785-108">EXAMPLES</span></span>

### <span data-ttu-id="97785-109">範例 1：移除還原點</span><span class="sxs-lookup"><span data-stu-id="97785-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="97785-110">此命令會移除 Azure SQL Database 建立日期的還原點。</span><span class="sxs-lookup"><span data-stu-id="97785-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="97785-111">參數</span><span class="sxs-lookup"><span data-stu-id="97785-111">PARAMETERS</span></span>

### <span data-ttu-id="97785-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="97785-112">-DatabaseName</span></span>
<span data-ttu-id="97785-113">指定 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="97785-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="97785-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97785-114">-DefaultProfile</span></span>
<span data-ttu-id="97785-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="97785-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97785-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97785-116">-PassThru</span></span>
<span data-ttu-id="97785-117">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="97785-117">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="97785-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97785-118">-ResourceGroupName</span></span>
<span data-ttu-id="97785-119">指定指派給 SQL Database 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="97785-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="97785-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="97785-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="97785-121">指定還原點建立日期。</span><span class="sxs-lookup"><span data-stu-id="97785-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97785-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="97785-122">-ServerName</span></span>
<span data-ttu-id="97785-123">指定主託管資料庫的 AzureSQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="97785-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="97785-124">-確認</span><span class="sxs-lookup"><span data-stu-id="97785-124">-Confirm</span></span>
<span data-ttu-id="97785-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="97785-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97785-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97785-126">-WhatIf</span></span>
<span data-ttu-id="97785-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="97785-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97785-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97785-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97785-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97785-129">CommonParameters</span></span>
<span data-ttu-id="97785-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="97785-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97785-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97785-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97785-132">輸入</span><span class="sxs-lookup"><span data-stu-id="97785-132">INPUTS</span></span>

### <span data-ttu-id="97785-133">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="97785-133">System.DateTime</span></span>

### <span data-ttu-id="97785-134">System.String</span><span class="sxs-lookup"><span data-stu-id="97785-134">System.String</span></span>

## <span data-ttu-id="97785-135">輸出</span><span class="sxs-lookup"><span data-stu-id="97785-135">OUTPUTS</span></span>

### <span data-ttu-id="97785-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="97785-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="97785-137">筆記</span><span class="sxs-lookup"><span data-stu-id="97785-137">NOTES</span></span>

## <span data-ttu-id="97785-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="97785-138">RELATED LINKS</span></span>
