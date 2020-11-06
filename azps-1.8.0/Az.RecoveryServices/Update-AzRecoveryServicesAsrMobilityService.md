---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 6dd1c87617d83754af430ae25aea1b47aaaa34e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621027"
---
# <span data-ttu-id="7969b-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="7969b-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="7969b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7969b-102">SYNOPSIS</span></span>
<span data-ttu-id="7969b-103">將行動服務代理程式更新推入受保護的電腦。</span><span class="sxs-lookup"><span data-stu-id="7969b-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="7969b-104">句法</span><span class="sxs-lookup"><span data-stu-id="7969b-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7969b-105">說明</span><span class="sxs-lookup"><span data-stu-id="7969b-105">DESCRIPTION</span></span>
<span data-ttu-id="7969b-106">如果有可用的更新，則 **AzRecoveryServicesAsrMobilityService** Cmdlet 會嘗試將行動服務代理更新推送到受保護的電腦 (。 ) </span><span class="sxs-lookup"><span data-stu-id="7969b-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="7969b-107">示例</span><span class="sxs-lookup"><span data-stu-id="7969b-107">EXAMPLES</span></span>

### <span data-ttu-id="7969b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7969b-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="7969b-109">追蹤更新受保護的專案 Moblility 服務代理程式的工作。</span><span class="sxs-lookup"><span data-stu-id="7969b-109">Job to track Update Replication Protected Item's Moblility Service Agent.</span></span>

## <span data-ttu-id="7969b-110">參數</span><span class="sxs-lookup"><span data-stu-id="7969b-110">PARAMETERS</span></span>

### <span data-ttu-id="7969b-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="7969b-111">-Account</span></span>
<span data-ttu-id="7969b-112">要用來推入更新的執行方式帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="7969b-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="7969b-113">必須是與要更新的電腦對應的 ASR 結構中的 [作為帳戶執行] 清單中的一個。</span><span class="sxs-lookup"><span data-stu-id="7969b-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7969b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7969b-114">-DefaultProfile</span></span>
<span data-ttu-id="7969b-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7969b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7969b-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7969b-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="7969b-117">要更新的 Azure Site Recovery 複製受保護專案。</span><span class="sxs-lookup"><span data-stu-id="7969b-117">Azure Site Recovery replication protected item to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7969b-118">-確認</span><span class="sxs-lookup"><span data-stu-id="7969b-118">-Confirm</span></span>
<span data-ttu-id="7969b-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7969b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7969b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7969b-120">-WhatIf</span></span>
<span data-ttu-id="7969b-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7969b-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7969b-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7969b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7969b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7969b-123">CommonParameters</span></span>
<span data-ttu-id="7969b-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7969b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7969b-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7969b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7969b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="7969b-126">INPUTS</span></span>

### <span data-ttu-id="7969b-127">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7969b-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="7969b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="7969b-128">OUTPUTS</span></span>

### <span data-ttu-id="7969b-129">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7969b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7969b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="7969b-130">NOTES</span></span>

## <span data-ttu-id="7969b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="7969b-131">RELATED LINKS</span></span>
