---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 5c5c9509c7ae242f98c8474a2ab87635f94dd62d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906514"
---
# <span data-ttu-id="0d84d-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="0d84d-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="0d84d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0d84d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d84d-103">將行動服務代理程式更新推送到受保護的電腦。</span><span class="sxs-lookup"><span data-stu-id="0d84d-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="0d84d-104">語法</span><span class="sxs-lookup"><span data-stu-id="0d84d-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d84d-105">描述</span><span class="sxs-lookup"><span data-stu-id="0d84d-105">DESCRIPTION</span></span>
<span data-ttu-id="0d84d-106">**Update-AzRecoveryServicesrMobilityService** Cmdlet 會嘗試將行動服務代理程式更新推送到受保護的電腦 (如果有可用的更新) </span><span class="sxs-lookup"><span data-stu-id="0d84d-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="0d84d-107">例子</span><span class="sxs-lookup"><span data-stu-id="0d84d-107">EXAMPLES</span></span>

### <span data-ttu-id="0d84d-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0d84d-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="0d84d-109">追蹤更新複製受保護專案的行動性服務代理程式的工作。</span><span class="sxs-lookup"><span data-stu-id="0d84d-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="0d84d-110">參數</span><span class="sxs-lookup"><span data-stu-id="0d84d-110">PARAMETERS</span></span>

### <span data-ttu-id="0d84d-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="0d84d-111">-Account</span></span>
<span data-ttu-id="0d84d-112">以帳戶識別碼執行以推入更新。</span><span class="sxs-lookup"><span data-stu-id="0d84d-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="0d84d-113">必須是 ASR 結構中對應到電腦更新之執行帳戶清單中的一個帳戶。</span><span class="sxs-lookup"><span data-stu-id="0d84d-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

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

### <span data-ttu-id="0d84d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d84d-114">-DefaultProfile</span></span>
<span data-ttu-id="0d84d-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d84d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d84d-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0d84d-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="0d84d-117">要更新的 Azure 網站復原複本受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="0d84d-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="0d84d-118">-確認</span><span class="sxs-lookup"><span data-stu-id="0d84d-118">-Confirm</span></span>
<span data-ttu-id="0d84d-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0d84d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d84d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d84d-120">-WhatIf</span></span>
<span data-ttu-id="0d84d-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d84d-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d84d-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d84d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d84d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d84d-123">CommonParameters</span></span>
<span data-ttu-id="0d84d-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0d84d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d84d-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d84d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d84d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0d84d-126">INPUTS</span></span>

### <span data-ttu-id="0d84d-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0d84d-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="0d84d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0d84d-128">OUTPUTS</span></span>

### <span data-ttu-id="0d84d-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="0d84d-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0d84d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0d84d-130">NOTES</span></span>

## <span data-ttu-id="0d84d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d84d-131">RELATED LINKS</span></span>
