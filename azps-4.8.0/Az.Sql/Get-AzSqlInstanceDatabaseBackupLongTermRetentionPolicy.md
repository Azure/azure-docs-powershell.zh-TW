---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0ece582a85216637454811621aae8a6262475d5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129193"
---
# <span data-ttu-id="d4dd9-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4dd9-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="d4dd9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="d4dd9-103">取得受管理資料庫的長期保留原則</span><span class="sxs-lookup"><span data-stu-id="d4dd9-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="d4dd9-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4dd9-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4dd9-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4dd9-105">DESCRIPTION</span></span>
<span data-ttu-id="d4dd9-106">**AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** Cmdlet 會取得向這個受管理的資料庫註冊的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="d4dd9-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="d4dd9-107">原則是用來定義備份儲存原則的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="d4dd9-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="d4dd9-108">示例</span><span class="sxs-lookup"><span data-stu-id="d4dd9-108">EXAMPLES</span></span>

### <span data-ttu-id="d4dd9-109">範例1</span><span class="sxs-lookup"><span data-stu-id="d4dd9-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P2W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="d4dd9-110">取得資料庫的長期保留原則目前版本</span><span class="sxs-lookup"><span data-stu-id="d4dd9-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="d4dd9-111">參數</span><span class="sxs-lookup"><span data-stu-id="d4dd9-111">PARAMETERS</span></span>

### <span data-ttu-id="d4dd9-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d4dd9-112">-DatabaseName</span></span>
<span data-ttu-id="d4dd9-113">要使用之 Azure Managed 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4dd9-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="d4dd9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4dd9-114">-DefaultProfile</span></span>
<span data-ttu-id="d4dd9-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4dd9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4dd9-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d4dd9-116">-InstanceName</span></span>
<span data-ttu-id="d4dd9-117">資料庫所屬之 Azure 管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4dd9-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="d4dd9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4dd9-118">-ResourceGroupName</span></span>
<span data-ttu-id="d4dd9-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4dd9-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="d4dd9-120">-確認</span><span class="sxs-lookup"><span data-stu-id="d4dd9-120">-Confirm</span></span>
<span data-ttu-id="d4dd9-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4dd9-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4dd9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4dd9-122">-WhatIf</span></span>
<span data-ttu-id="d4dd9-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4dd9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4dd9-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4dd9-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4dd9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4dd9-125">CommonParameters</span></span>
<span data-ttu-id="d4dd9-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4dd9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4dd9-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d4dd9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4dd9-128">輸入</span><span class="sxs-lookup"><span data-stu-id="d4dd9-128">INPUTS</span></span>

### <span data-ttu-id="d4dd9-129">System.object</span><span class="sxs-lookup"><span data-stu-id="d4dd9-129">System.String</span></span>

## <span data-ttu-id="d4dd9-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d4dd9-130">OUTPUTS</span></span>

### <span data-ttu-id="d4dd9-131">AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel 中的 [ManagedDatabaseBackup]</span><span class="sxs-lookup"><span data-stu-id="d4dd9-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="d4dd9-132">筆記</span><span class="sxs-lookup"><span data-stu-id="d4dd9-132">NOTES</span></span>

## <span data-ttu-id="d4dd9-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4dd9-133">RELATED LINKS</span></span>

[<span data-ttu-id="d4dd9-134">AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d4dd9-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d4dd9-135">移除-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d4dd9-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="d4dd9-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4dd9-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="d4dd9-137">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="d4dd9-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)