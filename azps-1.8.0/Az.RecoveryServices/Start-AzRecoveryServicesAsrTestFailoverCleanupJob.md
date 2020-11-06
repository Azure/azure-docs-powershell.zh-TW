---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 4143bc481091889b293d206192e0c5eba386d68a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621042"
---
# <span data-ttu-id="72bbd-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="72bbd-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="72bbd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="72bbd-103">啟動測試容錯移轉清除操作。</span><span class="sxs-lookup"><span data-stu-id="72bbd-103">Starts the test failover cleanup operation.</span></span>

## <span data-ttu-id="72bbd-104">句法</span><span class="sxs-lookup"><span data-stu-id="72bbd-104">SYNTAX</span></span>

### <span data-ttu-id="72bbd-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="72bbd-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72bbd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="72bbd-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72bbd-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="72bbd-107">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72bbd-108">說明</span><span class="sxs-lookup"><span data-stu-id="72bbd-108">DESCRIPTION</span></span>
<span data-ttu-id="72bbd-109">**AzRecoveryServicesAsrTestFailoverCleanupJob** Cmdlet 會在已執行測試容錯移轉的複製受保護專案或復原方案上啟動測試容錯移轉清除作業。</span><span class="sxs-lookup"><span data-stu-id="72bbd-109">The **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="72bbd-110">示例</span><span class="sxs-lookup"><span data-stu-id="72bbd-110">EXAMPLES</span></span>

### <span data-ttu-id="72bbd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="72bbd-111">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="72bbd-112">針對 Azure Site Recovery 複製受保護的專案追蹤測試容錯移轉清除的工作。</span><span class="sxs-lookup"><span data-stu-id="72bbd-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="72bbd-113">範例2</span><span class="sxs-lookup"><span data-stu-id="72bbd-113">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

<span data-ttu-id="72bbd-114">追蹤 Azure 網站復原 recoveryPlan 的測試容錯移轉清除的工作。</span><span class="sxs-lookup"><span data-stu-id="72bbd-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="72bbd-115">參數</span><span class="sxs-lookup"><span data-stu-id="72bbd-115">PARAMETERS</span></span>

### <span data-ttu-id="72bbd-116">-批註</span><span class="sxs-lookup"><span data-stu-id="72bbd-116">-Comment</span></span>
<span data-ttu-id="72bbd-117">測試容錯移轉的使用者意見。</span><span class="sxs-lookup"><span data-stu-id="72bbd-117">User Comment for Test Failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bbd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72bbd-118">-DefaultProfile</span></span>
<span data-ttu-id="72bbd-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72bbd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72bbd-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="72bbd-120">-RecoveryPlan</span></span>
<span data-ttu-id="72bbd-121">執行測試容錯移轉清除的復原方案。</span><span class="sxs-lookup"><span data-stu-id="72bbd-121">Recovery Plan to perform the test failover cleanup on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72bbd-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="72bbd-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="72bbd-123">複製受保護的專案，以執行測試容錯移轉清除。</span><span class="sxs-lookup"><span data-stu-id="72bbd-123">Replication Protected Item to perform the test failover cleanup on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72bbd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72bbd-124">-ResourceId</span></span>
<span data-ttu-id="72bbd-125">Cleaningup 測試容錯移轉的複製受保護專案/復原方案的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="72bbd-125">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72bbd-126">-確認</span><span class="sxs-lookup"><span data-stu-id="72bbd-126">-Confirm</span></span>
<span data-ttu-id="72bbd-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="72bbd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72bbd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72bbd-128">-WhatIf</span></span>
<span data-ttu-id="72bbd-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="72bbd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72bbd-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72bbd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72bbd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72bbd-131">CommonParameters</span></span>
<span data-ttu-id="72bbd-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72bbd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72bbd-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="72bbd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72bbd-134">輸入</span><span class="sxs-lookup"><span data-stu-id="72bbd-134">INPUTS</span></span>

### <span data-ttu-id="72bbd-135">System.object</span><span class="sxs-lookup"><span data-stu-id="72bbd-135">System.String</span></span>

### <span data-ttu-id="72bbd-136">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="72bbd-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="72bbd-137">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="72bbd-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="72bbd-138">輸出</span><span class="sxs-lookup"><span data-stu-id="72bbd-138">OUTPUTS</span></span>

### <span data-ttu-id="72bbd-139">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="72bbd-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="72bbd-140">筆記</span><span class="sxs-lookup"><span data-stu-id="72bbd-140">NOTES</span></span>

## <span data-ttu-id="72bbd-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="72bbd-141">RELATED LINKS</span></span>
