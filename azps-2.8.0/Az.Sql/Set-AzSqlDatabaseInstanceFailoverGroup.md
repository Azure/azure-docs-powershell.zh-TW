---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 38e19e764e7a9d272db777a295f05016f0ef95af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792599"
---
# <span data-ttu-id="13454-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="13454-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="13454-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13454-102">SYNOPSIS</span></span>
<span data-ttu-id="13454-103">修改實例容錯移轉群組的配置。</span><span class="sxs-lookup"><span data-stu-id="13454-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="13454-104">句法</span><span class="sxs-lookup"><span data-stu-id="13454-104">SYNTAX</span></span>

### <span data-ttu-id="13454-105">SetIFGDefault (預設) </span><span class="sxs-lookup"><span data-stu-id="13454-105">SetIFGDefault (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13454-106">從資源識別碼設定實例容錯移轉群組</span><span class="sxs-lookup"><span data-stu-id="13454-106">Set a Instance Failover Group from Resource Id</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13454-107">從 AzureSqlInstanceFailoverGroupModel 實例定義設定實例容錯移轉群組</span><span class="sxs-lookup"><span data-stu-id="13454-107">Set a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13454-108">說明</span><span class="sxs-lookup"><span data-stu-id="13454-108">DESCRIPTION</span></span>
<span data-ttu-id="13454-109">這個命令會修改實例容錯移轉群組的配置。</span><span class="sxs-lookup"><span data-stu-id="13454-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="13454-110">應使用實例容錯移轉群組的主要區域來執行命令。</span><span class="sxs-lookup"><span data-stu-id="13454-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="13454-111">在實例容錯移轉群組功能的預覽期間，"-GracePeriodWithDataLossHours" 參數只支援大於或等於1小時的值。</span><span class="sxs-lookup"><span data-stu-id="13454-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="13454-112">示例</span><span class="sxs-lookup"><span data-stu-id="13454-112">EXAMPLES</span></span>

### <span data-ttu-id="13454-113">範例1</span><span class="sxs-lookup"><span data-stu-id="13454-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="13454-114">透過 [容錯移轉] 群組中的管道，將實例容錯移轉群組的容錯移轉原則設定為「手動」。</span><span class="sxs-lookup"><span data-stu-id="13454-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="13454-115">參數</span><span class="sxs-lookup"><span data-stu-id="13454-115">PARAMETERS</span></span>

### <span data-ttu-id="13454-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="13454-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="13454-117">在次要伺服器上的中斷是否應該觸發唯讀端點的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="13454-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="13454-118">尚不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="13454-118">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13454-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13454-119">-DefaultProfile</span></span>
<span data-ttu-id="13454-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="13454-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13454-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="13454-121">-FailoverPolicy</span></span>
<span data-ttu-id="13454-122">實例容錯移轉群組的容錯移轉原則。</span><span class="sxs-lookup"><span data-stu-id="13454-122">The failover policy of the Instance Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13454-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="13454-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="13454-124">啟動自動容錯移轉前的間隔如果主伺服器發生停機，而容錯移轉無法在不遺失資料的情況下完成。</span><span class="sxs-lookup"><span data-stu-id="13454-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13454-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13454-125">-InputObject</span></span>
<span data-ttu-id="13454-126">要設定的實例容錯移轉群組物件</span><span class="sxs-lookup"><span data-stu-id="13454-126">The Instance Failover Group object to set</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Set a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13454-127">-位置</span><span class="sxs-lookup"><span data-stu-id="13454-127">-Location</span></span>
<span data-ttu-id="13454-128">要從中取得實例容錯移轉群組的本機區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="13454-128">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault, Set a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13454-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="13454-129">-Name</span></span>
<span data-ttu-id="13454-130">實例容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="13454-130">The name of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13454-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13454-131">-ResourceGroupName</span></span>
<span data-ttu-id="13454-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="13454-132">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13454-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13454-133">-ResourceId</span></span>
<span data-ttu-id="13454-134">要設定之實例容錯移轉群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="13454-134">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: String
Parameter Sets: Set a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13454-135">-確認</span><span class="sxs-lookup"><span data-stu-id="13454-135">-Confirm</span></span>
<span data-ttu-id="13454-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13454-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13454-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13454-137">-WhatIf</span></span>
<span data-ttu-id="13454-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13454-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13454-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13454-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13454-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13454-140">CommonParameters</span></span>
<span data-ttu-id="13454-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13454-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13454-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13454-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13454-143">輸入</span><span class="sxs-lookup"><span data-stu-id="13454-143">INPUTS</span></span>

### <span data-ttu-id="13454-144">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="13454-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="13454-145">System.object</span><span class="sxs-lookup"><span data-stu-id="13454-145">System.String</span></span>

## <span data-ttu-id="13454-146">輸出</span><span class="sxs-lookup"><span data-stu-id="13454-146">OUTPUTS</span></span>

### <span data-ttu-id="13454-147">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="13454-147">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="13454-148">筆記</span><span class="sxs-lookup"><span data-stu-id="13454-148">NOTES</span></span>

## <span data-ttu-id="13454-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="13454-149">RELATED LINKS</span></span>
