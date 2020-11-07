---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: 4f926b88214a60cc05b6eb9666e10fa8ed7bf3ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792321"
---
# <span data-ttu-id="d4129-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="d4129-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="d4129-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4129-102">SYNOPSIS</span></span>
<span data-ttu-id="d4129-103">將複製從一個進程伺服器切換到另一個處理，以進行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="d4129-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="d4129-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4129-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4129-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4129-105">DESCRIPTION</span></span>
<span data-ttu-id="d4129-106">**Start-AzRecoveryServicesAsrSwitchProcessServerJob** 會將指定虛擬機器或指定的進程伺服器的複製資料移動切換至指定的目標處理伺服器。</span><span class="sxs-lookup"><span data-stu-id="d4129-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="d4129-107">用於負載平衡或切換進程伺服器之間的複製。</span><span class="sxs-lookup"><span data-stu-id="d4129-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="d4129-108">示例</span><span class="sxs-lookup"><span data-stu-id="d4129-108">EXAMPLES</span></span>

### <span data-ttu-id="d4129-109">範例1</span><span class="sxs-lookup"><span data-stu-id="d4129-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="d4129-110">[作業]，以追蹤從來源到目標處理常式伺服器的所有受複製受保護專案的切換程式伺服器。</span><span class="sxs-lookup"><span data-stu-id="d4129-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="d4129-111">範例2</span><span class="sxs-lookup"><span data-stu-id="d4129-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="d4129-112">[作業] 可用於追蹤將受複製受保護的專案從來源移至目標進程伺服器的切換程式伺服器。</span><span class="sxs-lookup"><span data-stu-id="d4129-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="d4129-113">參數</span><span class="sxs-lookup"><span data-stu-id="d4129-113">PARAMETERS</span></span>

### <span data-ttu-id="d4129-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4129-114">-DefaultProfile</span></span>
<span data-ttu-id="d4129-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4129-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4129-116">-結構</span><span class="sxs-lookup"><span data-stu-id="d4129-116">-Fabric</span></span>
<span data-ttu-id="d4129-117">與佈建服務器相對應的網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="d4129-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4129-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d4129-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d4129-119">要切換其進程伺服器的複製受保護專案清單。</span><span class="sxs-lookup"><span data-stu-id="d4129-119">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4129-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="d4129-120">-SourceProcessServer</span></span>
<span data-ttu-id="d4129-121">要從中切換複製的進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="d4129-121">The Process server to switch replication out from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4129-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="d4129-122">-TargetProcessServer</span></span>
<span data-ttu-id="d4129-123">要將複製切換到其中的進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="d4129-123">The Process server to switch replication to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4129-124">-確認</span><span class="sxs-lookup"><span data-stu-id="d4129-124">-Confirm</span></span>
<span data-ttu-id="d4129-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4129-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4129-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4129-126">-WhatIf</span></span>
<span data-ttu-id="d4129-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4129-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4129-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4129-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4129-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4129-129">CommonParameters</span></span>
<span data-ttu-id="d4129-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4129-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4129-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4129-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4129-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d4129-132">INPUTS</span></span>

### <span data-ttu-id="d4129-133">所有</span><span class="sxs-lookup"><span data-stu-id="d4129-133">None</span></span>

## <span data-ttu-id="d4129-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d4129-134">OUTPUTS</span></span>

### <span data-ttu-id="d4129-135">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d4129-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d4129-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d4129-136">NOTES</span></span>

## <span data-ttu-id="d4129-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4129-137">RELATED LINKS</span></span>
