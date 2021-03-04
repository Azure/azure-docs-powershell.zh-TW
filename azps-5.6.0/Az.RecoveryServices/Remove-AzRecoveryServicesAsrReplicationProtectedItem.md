---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 533a5932aea282158bb1f53bf9464942ed9f17c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902221"
---
# <span data-ttu-id="0cf51-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0cf51-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="0cf51-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0cf51-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf51-103">停止/停用 Azure 網站復原複寫受保護專案的複寫。</span><span class="sxs-lookup"><span data-stu-id="0cf51-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="0cf51-104">語法</span><span class="sxs-lookup"><span data-stu-id="0cf51-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0cf51-105">描述</span><span class="sxs-lookup"><span data-stu-id="0cf51-105">DESCRIPTION</span></span>
<span data-ttu-id="0cf51-106">**Remove-AzRecoveryServicesAsrReplicationProtecedItem** Cmdlet 會停用指定的 Azure 網站復原複寫受保護專案的複寫。</span><span class="sxs-lookup"><span data-stu-id="0cf51-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="0cf51-107">此作業會使受保護專案的複製停止。</span><span class="sxs-lookup"><span data-stu-id="0cf51-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="0cf51-108">例子</span><span class="sxs-lookup"><span data-stu-id="0cf51-108">EXAMPLES</span></span>

### <span data-ttu-id="0cf51-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="0cf51-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="0cf51-110">針對指定的複製受保護的專案啟動停用複製作業，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="0cf51-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0cf51-111">參數</span><span class="sxs-lookup"><span data-stu-id="0cf51-111">PARAMETERS</span></span>

### <span data-ttu-id="0cf51-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf51-112">-DefaultProfile</span></span>
<span data-ttu-id="0cf51-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0cf51-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0cf51-114">-強制</span><span class="sxs-lookup"><span data-stu-id="0cf51-114">-Force</span></span>
<span data-ttu-id="0cf51-115">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="0cf51-115">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf51-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cf51-116">-InputObject</span></span>
<span data-ttu-id="0cf51-117">Cmdlet 的輸入物件：對應到要停用複製之複製受保護專案的 ASR 複製受保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="0cf51-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf51-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="0cf51-118">-WaitForCompletion</span></span>
<span data-ttu-id="0cf51-119">表示 Cmdlet 應等候作業完成再返回。</span><span class="sxs-lookup"><span data-stu-id="0cf51-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf51-120">-確認</span><span class="sxs-lookup"><span data-stu-id="0cf51-120">-Confirm</span></span>
<span data-ttu-id="0cf51-121">指定如果需要確認。</span><span class="sxs-lookup"><span data-stu-id="0cf51-121">Specify if confirmation is required.</span></span> <span data-ttu-id="0cf51-122">將確認參數的值設定為$false跳過確認。</span><span class="sxs-lookup"><span data-stu-id="0cf51-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="0cf51-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cf51-123">-WhatIf</span></span>
<span data-ttu-id="0cf51-124">顯示執行 Cmdlet 而不實際執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0cf51-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="0cf51-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf51-125">CommonParameters</span></span>
<span data-ttu-id="0cf51-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0cf51-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf51-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cf51-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf51-128">輸入</span><span class="sxs-lookup"><span data-stu-id="0cf51-128">INPUTS</span></span>

### <span data-ttu-id="0cf51-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0cf51-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="0cf51-130">輸出</span><span class="sxs-lookup"><span data-stu-id="0cf51-130">OUTPUTS</span></span>

### <span data-ttu-id="0cf51-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="0cf51-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0cf51-132">筆記</span><span class="sxs-lookup"><span data-stu-id="0cf51-132">NOTES</span></span>

## <span data-ttu-id="0cf51-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="0cf51-133">RELATED LINKS</span></span>

[<span data-ttu-id="0cf51-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0cf51-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="0cf51-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0cf51-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="0cf51-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0cf51-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
