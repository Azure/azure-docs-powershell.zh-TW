---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: be4a4f418268d1e2523e13d5a779f911381c7309
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450983"
---
# <span data-ttu-id="25ca5-101">Remove-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="25ca5-101">Remove-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="25ca5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="25ca5-103">從 SQL 資料庫移除指定的還原點。</span><span class="sxs-lookup"><span data-stu-id="25ca5-103">Removes given restore point from a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25ca5-104">句法</span><span class="sxs-lookup"><span data-stu-id="25ca5-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25ca5-105">說明</span><span class="sxs-lookup"><span data-stu-id="25ca5-105">DESCRIPTION</span></span>
<span data-ttu-id="25ca5-106">**AzureRmSqlDatabaseRestorePoint** Cmdlet 會從 Azure SQL Database 中移除指定的還原點。</span><span class="sxs-lookup"><span data-stu-id="25ca5-106">The **Remove-AzureRmSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="25ca5-107">Azure SQL Database 上的 SQL Server 資料倉儲服務目前支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25ca5-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="25ca5-108">示例</span><span class="sxs-lookup"><span data-stu-id="25ca5-108">EXAMPLES</span></span>

### <span data-ttu-id="25ca5-109">範例1：移除還原點</span><span class="sxs-lookup"><span data-stu-id="25ca5-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="25ca5-110">這個命令會針對指定的建立日期，移除 Azure SQL Database 的還原點。</span><span class="sxs-lookup"><span data-stu-id="25ca5-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="25ca5-111">參數</span><span class="sxs-lookup"><span data-stu-id="25ca5-111">PARAMETERS</span></span>

### <span data-ttu-id="25ca5-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="25ca5-112">-DatabaseName</span></span>
<span data-ttu-id="25ca5-113">指定 SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="25ca5-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="25ca5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25ca5-114">-DefaultProfile</span></span>
<span data-ttu-id="25ca5-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="25ca5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25ca5-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25ca5-116">-PassThru</span></span>
<span data-ttu-id="25ca5-117">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="25ca5-117">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="25ca5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25ca5-118">-ResourceGroupName</span></span>
<span data-ttu-id="25ca5-119">指定指派 SQL 資料庫的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="25ca5-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="25ca5-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="25ca5-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="25ca5-121">指定還原點建立日期。</span><span class="sxs-lookup"><span data-stu-id="25ca5-121">Specifies the restore point creation date.</span></span>

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

### <span data-ttu-id="25ca5-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="25ca5-122">-ServerName</span></span>
<span data-ttu-id="25ca5-123">指定裝載資料庫之 AzureSQL 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="25ca5-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="25ca5-124">-確認</span><span class="sxs-lookup"><span data-stu-id="25ca5-124">-Confirm</span></span>
<span data-ttu-id="25ca5-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="25ca5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25ca5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25ca5-126">-WhatIf</span></span>
<span data-ttu-id="25ca5-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25ca5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25ca5-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25ca5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25ca5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ca5-129">CommonParameters</span></span>
<span data-ttu-id="25ca5-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25ca5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25ca5-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25ca5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ca5-132">輸入</span><span class="sxs-lookup"><span data-stu-id="25ca5-132">INPUTS</span></span>

### <span data-ttu-id="25ca5-133">System.object</span><span class="sxs-lookup"><span data-stu-id="25ca5-133">System.DateTime</span></span>

### <span data-ttu-id="25ca5-134">System.object</span><span class="sxs-lookup"><span data-stu-id="25ca5-134">System.String</span></span>

## <span data-ttu-id="25ca5-135">輸出</span><span class="sxs-lookup"><span data-stu-id="25ca5-135">OUTPUTS</span></span>

### <span data-ttu-id="25ca5-136">AzureSqlDatabaseRestorePointModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="25ca5-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="25ca5-137">筆記</span><span class="sxs-lookup"><span data-stu-id="25ca5-137">NOTES</span></span>

## <span data-ttu-id="25ca5-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="25ca5-138">RELATED LINKS</span></span>
