---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0dd5f38f00e715141a967160cadc8ab075825ac6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138138"
---
# <span data-ttu-id="dd074-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dd074-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="dd074-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd074-102">SYNOPSIS</span></span>
<span data-ttu-id="dd074-103">取得資料庫長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="dd074-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="dd074-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd074-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd074-105">說明</span><span class="sxs-lookup"><span data-stu-id="dd074-105">DESCRIPTION</span></span>
<span data-ttu-id="dd074-106">**AzSqlDatabaseBackupLongTermRetentionPolicy** Cmdlet 會取得向這個資料庫註冊的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="dd074-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="dd074-107">原則是用來定義備份儲存原則的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="dd074-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="dd074-108">示例</span><span class="sxs-lookup"><span data-stu-id="dd074-108">EXAMPLES</span></span>

### <span data-ttu-id="dd074-109">範例1：取得目前版本的長期保留原則</span><span class="sxs-lookup"><span data-stu-id="dd074-109">Example 1: Get the current version of the long term retention policy</span></span>
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

<span data-ttu-id="dd074-110">這個命令會取得 database01 之長期保留原則的目前版本</span><span class="sxs-lookup"><span data-stu-id="dd074-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="dd074-111">參數</span><span class="sxs-lookup"><span data-stu-id="dd074-111">PARAMETERS</span></span>

### <span data-ttu-id="dd074-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dd074-112">-DatabaseName</span></span>
<span data-ttu-id="dd074-113">要使用之 Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd074-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="dd074-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd074-114">-DefaultProfile</span></span>
<span data-ttu-id="dd074-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd074-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd074-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd074-116">-ResourceGroupName</span></span>
<span data-ttu-id="dd074-117">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd074-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="dd074-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dd074-118">-ServerName</span></span>
<span data-ttu-id="dd074-119">資料庫所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd074-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="dd074-120">-確認</span><span class="sxs-lookup"><span data-stu-id="dd074-120">-Confirm</span></span>
<span data-ttu-id="dd074-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dd074-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd074-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd074-122">-WhatIf</span></span>
<span data-ttu-id="dd074-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd074-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd074-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd074-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd074-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd074-125">CommonParameters</span></span>
<span data-ttu-id="dd074-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd074-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd074-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dd074-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd074-128">輸入</span><span class="sxs-lookup"><span data-stu-id="dd074-128">INPUTS</span></span>

### <span data-ttu-id="dd074-129">System.object</span><span class="sxs-lookup"><span data-stu-id="dd074-129">System.String</span></span>

## <span data-ttu-id="dd074-130">輸出</span><span class="sxs-lookup"><span data-stu-id="dd074-130">OUTPUTS</span></span>

### <span data-ttu-id="dd074-131">AzureSqlDatabaseBackupLongTermRetentionPolicyModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="dd074-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="dd074-132">筆記</span><span class="sxs-lookup"><span data-stu-id="dd074-132">NOTES</span></span>

## <span data-ttu-id="dd074-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd074-133">RELATED LINKS</span></span>

[<span data-ttu-id="dd074-134">AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="dd074-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="dd074-135">移除-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="dd074-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="dd074-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dd074-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="dd074-137">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="dd074-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)