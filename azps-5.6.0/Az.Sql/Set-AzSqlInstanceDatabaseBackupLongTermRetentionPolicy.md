---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: b8284d4f2ac5b28baffed630e789fc002c2c7d9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917885"
---
# <span data-ttu-id="94c69-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="94c69-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="94c69-102">簡介</span><span class="sxs-lookup"><span data-stu-id="94c69-102">SYNOPSIS</span></span>
<span data-ttu-id="94c69-103">**Set-AzSqlInstanceDatabaseLongTermRetentionBackup** Cmdlet 會設定受管理資料庫的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="94c69-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="94c69-104">語法</span><span class="sxs-lookup"><span data-stu-id="94c69-104">SYNTAX</span></span>

### <span data-ttu-id="94c69-105">WeeklyRetentionRequired (預設) </span><span class="sxs-lookup"><span data-stu-id="94c69-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94c69-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="94c69-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94c69-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="94c69-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94c69-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="94c69-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94c69-109">描述</span><span class="sxs-lookup"><span data-stu-id="94c69-109">DESCRIPTION</span></span>
<span data-ttu-id="94c69-110">**Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolidlet** 會為此受管理資料庫設定長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="94c69-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="94c69-111">例子</span><span class="sxs-lookup"><span data-stu-id="94c69-111">EXAMPLES</span></span>

### <span data-ttu-id="94c69-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="94c69-112">Example 1</span></span>
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

<span data-ttu-id="94c69-113">將資料庫的長期保留每週政策設定為一周。</span><span class="sxs-lookup"><span data-stu-id="94c69-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="94c69-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="94c69-114">Example 2</span></span>
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

<span data-ttu-id="94c69-115">此命令會從資料庫移除長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="94c69-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="94c69-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="94c69-116">Example 3</span></span>

<span data-ttu-id="94c69-117">此Set-AzSqlInstanceDatabaseLongTermRetentionBackup Cmdlet 會設定受管理資料庫的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="94c69-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="94c69-118"> (自動) </span><span class="sxs-lookup"><span data-stu-id="94c69-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="94c69-119">參數</span><span class="sxs-lookup"><span data-stu-id="94c69-119">PARAMETERS</span></span>

### <span data-ttu-id="94c69-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="94c69-120">-DatabaseName</span></span>
<span data-ttu-id="94c69-121">要使用的 Azure Managed 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="94c69-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="94c69-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c69-122">-DefaultProfile</span></span>
<span data-ttu-id="94c69-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="94c69-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94c69-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="94c69-124">-InstanceName</span></span>
<span data-ttu-id="94c69-125">資料庫所屬的 Azure Managed 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="94c69-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="94c69-126">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="94c69-126">-MonthlyRetention</span></span>
<span data-ttu-id="94c69-127">每月保留。</span><span class="sxs-lookup"><span data-stu-id="94c69-127">The Monthly Retention.</span></span>
<span data-ttu-id="94c69-128">如果只傳遞數位而非 ISO 8601 字串，則天數會假設為單位。</span><span class="sxs-lookup"><span data-stu-id="94c69-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="94c69-129">最短為 7 天，最多 10 年。</span><span class="sxs-lookup"><span data-stu-id="94c69-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="94c69-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="94c69-130">-RemovePolicy</span></span>
<span data-ttu-id="94c69-131">如果提供，將會清除資料庫的這個策略。</span><span class="sxs-lookup"><span data-stu-id="94c69-131">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="94c69-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c69-132">-ResourceGroupName</span></span>
<span data-ttu-id="94c69-133">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="94c69-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="94c69-134">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="94c69-134">-WeeklyRetention</span></span>
<span data-ttu-id="94c69-135">每週保留。</span><span class="sxs-lookup"><span data-stu-id="94c69-135">The Weekly Retention.</span></span>
<span data-ttu-id="94c69-136">如果只傳遞數位而非 ISO 8601 字串，則天數會假設為單位。</span><span class="sxs-lookup"><span data-stu-id="94c69-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="94c69-137">最短為 7 天，最多 10 年。</span><span class="sxs-lookup"><span data-stu-id="94c69-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="94c69-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="94c69-138">-WeekOfYear</span></span>
<span data-ttu-id="94c69-139">一年中的 1 到 52 周，以儲存為每年保留。</span><span class="sxs-lookup"><span data-stu-id="94c69-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="94c69-140">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="94c69-140">-YearlyRetention</span></span>
<span data-ttu-id="94c69-141">每年保留。</span><span class="sxs-lookup"><span data-stu-id="94c69-141">The Yearly Retention.</span></span>
<span data-ttu-id="94c69-142">如果只傳遞數位而非 ISO 8601 字串，則天數會假設為單位。</span><span class="sxs-lookup"><span data-stu-id="94c69-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="94c69-143">最短為 7 天，最多 10 年。</span><span class="sxs-lookup"><span data-stu-id="94c69-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="94c69-144">-確認</span><span class="sxs-lookup"><span data-stu-id="94c69-144">-Confirm</span></span>
<span data-ttu-id="94c69-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="94c69-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94c69-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94c69-146">-WhatIf</span></span>
<span data-ttu-id="94c69-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94c69-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94c69-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94c69-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94c69-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c69-149">CommonParameters</span></span>
<span data-ttu-id="94c69-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="94c69-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c69-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94c69-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c69-152">輸入</span><span class="sxs-lookup"><span data-stu-id="94c69-152">INPUTS</span></span>

### <span data-ttu-id="94c69-153">System.String</span><span class="sxs-lookup"><span data-stu-id="94c69-153">System.String</span></span>

### <span data-ttu-id="94c69-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="94c69-154">System.Int32</span></span>

## <span data-ttu-id="94c69-155">輸出</span><span class="sxs-lookup"><span data-stu-id="94c69-155">OUTPUTS</span></span>

### <span data-ttu-id="94c69-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="94c69-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="94c69-157">筆記</span><span class="sxs-lookup"><span data-stu-id="94c69-157">NOTES</span></span>

## <span data-ttu-id="94c69-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="94c69-158">RELATED LINKS</span></span>

[<span data-ttu-id="94c69-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="94c69-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="94c69-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="94c69-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="94c69-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="94c69-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="94c69-162">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="94c69-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)