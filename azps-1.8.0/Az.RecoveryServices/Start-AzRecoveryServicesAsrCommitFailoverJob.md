---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 1e453f8b11929b96e6e0f2dbe96164c2bf351ae7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621048"
---
# <span data-ttu-id="bff9b-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="bff9b-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="bff9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bff9b-102">SYNOPSIS</span></span>
<span data-ttu-id="bff9b-103">啟動針對網站復原物件的 [確認容錯移轉] 動作。</span><span class="sxs-lookup"><span data-stu-id="bff9b-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="bff9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="bff9b-104">SYNTAX</span></span>

### <span data-ttu-id="bff9b-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="bff9b-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bff9b-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="bff9b-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bff9b-107">說明</span><span class="sxs-lookup"><span data-stu-id="bff9b-107">DESCRIPTION</span></span>
<span data-ttu-id="bff9b-108">在容錯移轉作業之後， **Start AzRecoveryServicesAsrCommitFailoverJob** Cmdlet 會啟動 Azure Site Recovery 物件的 commit 容錯移轉進程。</span><span class="sxs-lookup"><span data-stu-id="bff9b-108">The **Start-AzRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="bff9b-109">示例</span><span class="sxs-lookup"><span data-stu-id="bff9b-109">EXAMPLES</span></span>

### <span data-ttu-id="bff9b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="bff9b-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="bff9b-111">針對指定的損毀修復方案啟動「確認容錯移轉」，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="bff9b-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="bff9b-112">參數</span><span class="sxs-lookup"><span data-stu-id="bff9b-112">PARAMETERS</span></span>

### <span data-ttu-id="bff9b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff9b-113">-DefaultProfile</span></span>
<span data-ttu-id="bff9b-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bff9b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bff9b-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bff9b-115">-RecoveryPlan</span></span>
<span data-ttu-id="bff9b-116">指定與要 failovered 之復原方案對應的 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="bff9b-116">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

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

### <span data-ttu-id="bff9b-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bff9b-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="bff9b-118">指定與要 failovered 之複製受保護專案對應的 ASR 複製受保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="bff9b-118">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

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

### <span data-ttu-id="bff9b-119">-確認</span><span class="sxs-lookup"><span data-stu-id="bff9b-119">-Confirm</span></span>
<span data-ttu-id="bff9b-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bff9b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bff9b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bff9b-121">-WhatIf</span></span>
<span data-ttu-id="bff9b-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bff9b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bff9b-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bff9b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bff9b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff9b-124">CommonParameters</span></span>
<span data-ttu-id="bff9b-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bff9b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff9b-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bff9b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff9b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="bff9b-127">INPUTS</span></span>

### <span data-ttu-id="bff9b-128">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bff9b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="bff9b-129">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bff9b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="bff9b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="bff9b-130">OUTPUTS</span></span>

### <span data-ttu-id="bff9b-131">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bff9b-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bff9b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="bff9b-132">NOTES</span></span>

## <span data-ttu-id="bff9b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="bff9b-133">RELATED LINKS</span></span>
