---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0f43956dfa29dac2d7c6ca1869716400b8adad35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453024"
---
# <span data-ttu-id="1b20a-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1b20a-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="1b20a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b20a-102">SYNOPSIS</span></span>
<span data-ttu-id="1b20a-103">取得資料庫長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="1b20a-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b20a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b20a-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-Current] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b20a-105">說明</span><span class="sxs-lookup"><span data-stu-id="1b20a-105">DESCRIPTION</span></span>
<span data-ttu-id="1b20a-106">**AzureRmSqlDatabaseBackupLongTermRetentionPolicy** Cmdlet 會取得向這個資料庫註冊的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="1b20a-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="1b20a-107">原則是用來定義備份儲存原則的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="1b20a-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="1b20a-108">示例</span><span class="sxs-lookup"><span data-stu-id="1b20a-108">EXAMPLES</span></span>

### <span data-ttu-id="1b20a-109">範例1：取得目前版本的長期保留原則</span><span class="sxs-lookup"><span data-stu-id="1b20a-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -Current


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

<span data-ttu-id="1b20a-110">這個命令會取得 database01 之長期保留原則的目前版本</span><span class="sxs-lookup"><span data-stu-id="1b20a-110">This command gets the current version of the long term retention policy for database01</span></span>

### <span data-ttu-id="1b20a-111">範例2：取得舊版本的長期保留原則</span><span class="sxs-lookup"><span data-stu-id="1b20a-111">Example 2: Get the legacy version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        :
MonthlyRetention                       :
YearlyRetention                        :
WeekOfYear                             :
State                                  : Enabled
RecoveryServicesBackupPolicyResourceId : /subscriptions/4f2b42fc-4fc3-fd41-8ab8-5a382d8b30df/resourceGroups/resourcegroup01/providers/MicrosoftRecoveryServices/vaults/vault01/backupPolicies/policy01
Location                               : Southeast Asia
```

<span data-ttu-id="1b20a-112">這個命令會取得 database01 的舊版保留原則舊版本</span><span class="sxs-lookup"><span data-stu-id="1b20a-112">This command gets the legacy version of the long term retention policy for database01</span></span>

## <span data-ttu-id="1b20a-113">參數</span><span class="sxs-lookup"><span data-stu-id="1b20a-113">PARAMETERS</span></span>

### <span data-ttu-id="1b20a-114">-目前</span><span class="sxs-lookup"><span data-stu-id="1b20a-114">-Current</span></span>
<span data-ttu-id="1b20a-115">如果未提供，命令會傳回舊版的長期保留原則資訊。</span><span class="sxs-lookup"><span data-stu-id="1b20a-115">If not provided, the command returns the legacy Long Term Retention policy information.</span></span>
<span data-ttu-id="1b20a-116">否則，命令會傳回長期保留原則的目前版本。</span><span class="sxs-lookup"><span data-stu-id="1b20a-116">Otherwise, the command returns the current version of the Long Term Retention policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b20a-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1b20a-117">-DatabaseName</span></span>
<span data-ttu-id="1b20a-118">要使用之 Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b20a-118">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="1b20a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b20a-119">-DefaultProfile</span></span>
<span data-ttu-id="1b20a-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b20a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b20a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b20a-121">-ResourceGroupName</span></span>
<span data-ttu-id="1b20a-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b20a-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="1b20a-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1b20a-123">-ServerName</span></span>
<span data-ttu-id="1b20a-124">資料庫所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b20a-124">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="1b20a-125">-確認</span><span class="sxs-lookup"><span data-stu-id="1b20a-125">-Confirm</span></span>
<span data-ttu-id="1b20a-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1b20a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b20a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b20a-127">-WhatIf</span></span>
<span data-ttu-id="1b20a-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1b20a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b20a-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1b20a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b20a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b20a-130">CommonParameters</span></span>
<span data-ttu-id="1b20a-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b20a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1b20a-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b20a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b20a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1b20a-133">INPUTS</span></span>

### <span data-ttu-id="1b20a-134">所有</span><span class="sxs-lookup"><span data-stu-id="1b20a-134">None</span></span>
<span data-ttu-id="1b20a-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1b20a-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1b20a-136">輸出</span><span class="sxs-lookup"><span data-stu-id="1b20a-136">OUTPUTS</span></span>

### <span data-ttu-id="1b20a-137">AzureSqlDatabaseBackupLongTermRetentionPolicyModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="1b20a-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="1b20a-138">筆記</span><span class="sxs-lookup"><span data-stu-id="1b20a-138">NOTES</span></span>

## <span data-ttu-id="1b20a-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b20a-139">RELATED LINKS</span></span>

[<span data-ttu-id="1b20a-140">AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="1b20a-140">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="1b20a-141">移除-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="1b20a-141">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="1b20a-142">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1b20a-142">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="1b20a-143">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="1b20a-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)