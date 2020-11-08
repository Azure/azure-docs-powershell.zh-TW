---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: cf7cf1dcd91bc1c9f703e4fc5ca613ad6407e575
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127234"
---
# <span data-ttu-id="dd20a-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dd20a-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="dd20a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd20a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd20a-103">**AzSqlInstanceDatabaseLongTermRetentionBackup** Cmdlet 會設定受管理資料庫的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="dd20a-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="dd20a-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd20a-104">SYNTAX</span></span>

### <span data-ttu-id="dd20a-105">WeeklyRetentionRequired (預設) </span><span class="sxs-lookup"><span data-stu-id="dd20a-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd20a-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="dd20a-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd20a-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="dd20a-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd20a-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="dd20a-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd20a-109">說明</span><span class="sxs-lookup"><span data-stu-id="dd20a-109">DESCRIPTION</span></span>
<span data-ttu-id="dd20a-110">**AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** Cmdlet 會為此受管理的資料庫設定長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="dd20a-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="dd20a-111">示例</span><span class="sxs-lookup"><span data-stu-id="dd20a-111">EXAMPLES</span></span>

### <span data-ttu-id="dd20a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="dd20a-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -WeeklyRetention "P1W"


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P1W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="dd20a-113">將資料庫的長期保留原則保持每週原則設定為一周。</span><span class="sxs-lookup"><span data-stu-id="dd20a-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="dd20a-114">範例2</span><span class="sxs-lookup"><span data-stu-id="dd20a-114">Example 2</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName target1 -RemovePolicy


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : target1
WeeklyRetention     : PT0S
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="dd20a-115">這個命令會從資料庫中移除長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="dd20a-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="dd20a-116">範例3</span><span class="sxs-lookup"><span data-stu-id="dd20a-116">Example 3</span></span>

<span data-ttu-id="dd20a-117">Set-AzSqlInstanceDatabaseLongTermRetentionBackup Cmdlet 會設定受管理資料庫的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="dd20a-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="dd20a-118"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="dd20a-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="dd20a-119">參數</span><span class="sxs-lookup"><span data-stu-id="dd20a-119">PARAMETERS</span></span>

### <span data-ttu-id="dd20a-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dd20a-120">-DatabaseName</span></span>
<span data-ttu-id="dd20a-121">要使用之 Azure Managed 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd20a-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="dd20a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd20a-122">-DefaultProfile</span></span>
<span data-ttu-id="dd20a-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd20a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd20a-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="dd20a-124">-InstanceName</span></span>
<span data-ttu-id="dd20a-125">資料庫所屬之 Azure 管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd20a-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="dd20a-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="dd20a-126">-MonthlyRetention</span></span>
<span data-ttu-id="dd20a-127">每月保留。</span><span class="sxs-lookup"><span data-stu-id="dd20a-127">The Monthly Retention.</span></span>
<span data-ttu-id="dd20a-128">如果只傳遞數位而不是 ISO 8601 字串，則會將天數視為單位。</span><span class="sxs-lookup"><span data-stu-id="dd20a-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="dd20a-129">最少7天，最多10年。</span><span class="sxs-lookup"><span data-stu-id="dd20a-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd20a-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="dd20a-130">-RemovePolicy</span></span>
<span data-ttu-id="dd20a-131">如果有提供，則會清除資料庫原則。</span><span class="sxs-lookup"><span data-stu-id="dd20a-131">If provided, the policy for the database will be cleared.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd20a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd20a-132">-ResourceGroupName</span></span>
<span data-ttu-id="dd20a-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd20a-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="dd20a-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="dd20a-134">-WeeklyRetention</span></span>
<span data-ttu-id="dd20a-135">每週保留。</span><span class="sxs-lookup"><span data-stu-id="dd20a-135">The Weekly Retention.</span></span>
<span data-ttu-id="dd20a-136">如果只傳遞數位而不是 ISO 8601 字串，則會將天數視為單位。</span><span class="sxs-lookup"><span data-stu-id="dd20a-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="dd20a-137">最少7天，最多10年。</span><span class="sxs-lookup"><span data-stu-id="dd20a-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd20a-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="dd20a-138">-WeekOfYear</span></span>
<span data-ttu-id="dd20a-139">要儲存每年保留的年（1到52）的周。</span><span class="sxs-lookup"><span data-stu-id="dd20a-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd20a-140">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="dd20a-140">-YearlyRetention</span></span>
<span data-ttu-id="dd20a-141">每年保留。</span><span class="sxs-lookup"><span data-stu-id="dd20a-141">The Yearly Retention.</span></span>
<span data-ttu-id="dd20a-142">如果只傳遞數位而不是 ISO 8601 字串，則會將天數視為單位。</span><span class="sxs-lookup"><span data-stu-id="dd20a-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="dd20a-143">最少7天，最多10年。</span><span class="sxs-lookup"><span data-stu-id="dd20a-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd20a-144">-確認</span><span class="sxs-lookup"><span data-stu-id="dd20a-144">-Confirm</span></span>
<span data-ttu-id="dd20a-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dd20a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd20a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd20a-146">-WhatIf</span></span>
<span data-ttu-id="dd20a-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd20a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd20a-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd20a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd20a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd20a-149">CommonParameters</span></span>
<span data-ttu-id="dd20a-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd20a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd20a-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dd20a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd20a-152">輸入</span><span class="sxs-lookup"><span data-stu-id="dd20a-152">INPUTS</span></span>

### <span data-ttu-id="dd20a-153">System.object</span><span class="sxs-lookup"><span data-stu-id="dd20a-153">System.String</span></span>

### <span data-ttu-id="dd20a-154">System.object</span><span class="sxs-lookup"><span data-stu-id="dd20a-154">System.Int32</span></span>

## <span data-ttu-id="dd20a-155">輸出</span><span class="sxs-lookup"><span data-stu-id="dd20a-155">OUTPUTS</span></span>

### <span data-ttu-id="dd20a-156">AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel 中的 [ManagedDatabaseBackup]</span><span class="sxs-lookup"><span data-stu-id="dd20a-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="dd20a-157">筆記</span><span class="sxs-lookup"><span data-stu-id="dd20a-157">NOTES</span></span>

## <span data-ttu-id="dd20a-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd20a-158">RELATED LINKS</span></span>

[<span data-ttu-id="dd20a-159">AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dd20a-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="dd20a-160">AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="dd20a-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="dd20a-161">移除-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="dd20a-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="dd20a-162">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="dd20a-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)