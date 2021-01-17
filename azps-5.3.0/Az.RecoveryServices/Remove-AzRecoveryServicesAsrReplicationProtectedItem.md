---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 71731c0a6f4f0bb917cb7490c1647add71b9a893
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435924"
---
# <span data-ttu-id="c6e96-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c6e96-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="c6e96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6e96-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e96-103">停止/停用 Azure Site Recovery 複製受保護的專案的複製。</span><span class="sxs-lookup"><span data-stu-id="c6e96-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="c6e96-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6e96-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6e96-105">說明</span><span class="sxs-lookup"><span data-stu-id="c6e96-105">DESCRIPTION</span></span>
<span data-ttu-id="c6e96-106">**AzRecoveryServicesAsrReplicationProtectedItem** Cmdlet 會停用對指定的 Azure 網站復原複製受保護專案的複製。</span><span class="sxs-lookup"><span data-stu-id="c6e96-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="c6e96-107">這個操作會導致複製停止受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="c6e96-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="c6e96-108">示例</span><span class="sxs-lookup"><span data-stu-id="c6e96-108">EXAMPLES</span></span>

### <span data-ttu-id="c6e96-109">範例1</span><span class="sxs-lookup"><span data-stu-id="c6e96-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="c6e96-110">針對指定的複製受保護專案啟動 [停用複製] 作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="c6e96-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c6e96-111">參數</span><span class="sxs-lookup"><span data-stu-id="c6e96-111">PARAMETERS</span></span>

### <span data-ttu-id="c6e96-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e96-112">-DefaultProfile</span></span>
<span data-ttu-id="c6e96-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6e96-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c6e96-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c6e96-114">-Force</span></span>
<span data-ttu-id="c6e96-115">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="c6e96-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="c6e96-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6e96-116">-InputObject</span></span>
<span data-ttu-id="c6e96-117">Cmdlet 的輸入物件：對應到要停用複製之受複製受保護專案的 ASR 複製受保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="c6e96-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

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

### <span data-ttu-id="c6e96-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="c6e96-118">-WaitForCompletion</span></span>
<span data-ttu-id="c6e96-119">指示在傳回前，該指令必須等待操作完成。</span><span class="sxs-lookup"><span data-stu-id="c6e96-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="c6e96-120">-確認</span><span class="sxs-lookup"><span data-stu-id="c6e96-120">-Confirm</span></span>
<span data-ttu-id="c6e96-121">指定是否需要確認。</span><span class="sxs-lookup"><span data-stu-id="c6e96-121">Specify if confirmation is required.</span></span> <span data-ttu-id="c6e96-122">將確認參數的值設定為 [$false]，以略過確認。</span><span class="sxs-lookup"><span data-stu-id="c6e96-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="c6e96-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6e96-123">-WhatIf</span></span>
<span data-ttu-id="c6e96-124">顯示在未實際執行 Cmdlet 的情況下執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6e96-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="c6e96-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e96-125">CommonParameters</span></span>
<span data-ttu-id="c6e96-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6e96-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e96-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c6e96-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e96-128">輸入</span><span class="sxs-lookup"><span data-stu-id="c6e96-128">INPUTS</span></span>

### <span data-ttu-id="c6e96-129">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c6e96-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c6e96-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c6e96-130">OUTPUTS</span></span>

### <span data-ttu-id="c6e96-131">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c6e96-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c6e96-132">筆記</span><span class="sxs-lookup"><span data-stu-id="c6e96-132">NOTES</span></span>

## <span data-ttu-id="c6e96-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6e96-133">RELATED LINKS</span></span>

[<span data-ttu-id="c6e96-134">AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c6e96-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="c6e96-135">新-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c6e96-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="c6e96-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c6e96-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
