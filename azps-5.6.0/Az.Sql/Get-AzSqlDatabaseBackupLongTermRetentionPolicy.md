---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: b0f3f657caea0da29ecf78baff15fe0afb7008ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905802"
---
# <span data-ttu-id="58f0b-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="58f0b-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="58f0b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="58f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="58f0b-103">獲得資料庫長期保留政策。</span><span class="sxs-lookup"><span data-stu-id="58f0b-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="58f0b-104">語法</span><span class="sxs-lookup"><span data-stu-id="58f0b-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58f0b-105">描述</span><span class="sxs-lookup"><span data-stu-id="58f0b-105">DESCRIPTION</span></span>
<span data-ttu-id="58f0b-106">**Get-AzSqlDatabaseBackupLongTermRetentionPolidlet** 會在此資料庫中註冊長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="58f0b-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="58f0b-107">此策略是 Azure 備份資源，用來定義備份儲存策略。</span><span class="sxs-lookup"><span data-stu-id="58f0b-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="58f0b-108">例子</span><span class="sxs-lookup"><span data-stu-id="58f0b-108">EXAMPLES</span></span>

### <span data-ttu-id="58f0b-109">範例 1：取得目前版本的長期保留政策</span><span class="sxs-lookup"><span data-stu-id="58f0b-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="58f0b-110">此命令會獲得目前版本的資料庫長期保留政策</span><span class="sxs-lookup"><span data-stu-id="58f0b-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="58f0b-111">參數</span><span class="sxs-lookup"><span data-stu-id="58f0b-111">PARAMETERS</span></span>

### <span data-ttu-id="58f0b-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="58f0b-112">-DatabaseName</span></span>
<span data-ttu-id="58f0b-113">要使用的 Azure SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="58f0b-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="58f0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f0b-114">-DefaultProfile</span></span>
<span data-ttu-id="58f0b-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="58f0b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58f0b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58f0b-116">-ResourceGroupName</span></span>
<span data-ttu-id="58f0b-117">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="58f0b-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="58f0b-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="58f0b-118">-ServerName</span></span>
<span data-ttu-id="58f0b-119">資料庫位於中的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="58f0b-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="58f0b-120">-確認</span><span class="sxs-lookup"><span data-stu-id="58f0b-120">-Confirm</span></span>
<span data-ttu-id="58f0b-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="58f0b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58f0b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58f0b-122">-WhatIf</span></span>
<span data-ttu-id="58f0b-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58f0b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58f0b-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58f0b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58f0b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f0b-125">CommonParameters</span></span>
<span data-ttu-id="58f0b-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="58f0b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f0b-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58f0b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f0b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="58f0b-128">INPUTS</span></span>

### <span data-ttu-id="58f0b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="58f0b-129">System.String</span></span>

## <span data-ttu-id="58f0b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="58f0b-130">OUTPUTS</span></span>

### <span data-ttu-id="58f0b-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="58f0b-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="58f0b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="58f0b-132">NOTES</span></span>

## <span data-ttu-id="58f0b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="58f0b-133">RELATED LINKS</span></span>

[<span data-ttu-id="58f0b-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="58f0b-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="58f0b-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="58f0b-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="58f0b-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="58f0b-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="58f0b-137">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="58f0b-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)