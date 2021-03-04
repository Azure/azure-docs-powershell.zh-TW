---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: 269285b806149c191e8162b41faa80177f6ca4eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903978"
---
# <span data-ttu-id="8ae03-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="8ae03-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="8ae03-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8ae03-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae03-103">從一個程式伺服器切換到另一個程式伺服器以平衡負載。</span><span class="sxs-lookup"><span data-stu-id="8ae03-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="8ae03-104">語法</span><span class="sxs-lookup"><span data-stu-id="8ae03-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ae03-105">描述</span><span class="sxs-lookup"><span data-stu-id="8ae03-105">DESCRIPTION</span></span>
<span data-ttu-id="8ae03-106">**Start-AzRecoveryServicesAsrSwitchProcessServerJob** 會切換指定虛擬機器或指定程式伺服器的複製資料移動至指定的目標流程伺服器。</span><span class="sxs-lookup"><span data-stu-id="8ae03-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="8ae03-107">用於在程式伺服器之間負載平衡或切換複製。</span><span class="sxs-lookup"><span data-stu-id="8ae03-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="8ae03-108">例子</span><span class="sxs-lookup"><span data-stu-id="8ae03-108">EXAMPLES</span></span>

### <span data-ttu-id="8ae03-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="8ae03-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="8ae03-110">工作以追蹤從來源到目標流程伺服器之所有複製受保護專案的切換程式伺服器。</span><span class="sxs-lookup"><span data-stu-id="8ae03-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="8ae03-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="8ae03-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="8ae03-112">針對從來源到目標流程伺服器傳遞的複製受保護專案，執行追蹤切換程式伺服器的工作。</span><span class="sxs-lookup"><span data-stu-id="8ae03-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="8ae03-113">參數</span><span class="sxs-lookup"><span data-stu-id="8ae03-113">PARAMETERS</span></span>

### <span data-ttu-id="8ae03-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ae03-114">-DefaultProfile</span></span>
<span data-ttu-id="8ae03-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ae03-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ae03-116">-布料</span><span class="sxs-lookup"><span data-stu-id="8ae03-116">-Fabric</span></span>
<span data-ttu-id="8ae03-117">對應到 Configuration Server 的網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="8ae03-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

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

### <span data-ttu-id="8ae03-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8ae03-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8ae03-119">要切換其程式伺服器之複製受保護的專案清單。</span><span class="sxs-lookup"><span data-stu-id="8ae03-119">List of replication protected item whose process server to be switched.</span></span>

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

### <span data-ttu-id="8ae03-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="8ae03-120">-SourceProcessServer</span></span>
<span data-ttu-id="8ae03-121">從程式伺服器切換出複製。</span><span class="sxs-lookup"><span data-stu-id="8ae03-121">The Process server to switch replication out from.</span></span>

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

### <span data-ttu-id="8ae03-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="8ae03-122">-TargetProcessServer</span></span>
<span data-ttu-id="8ae03-123">要切換複製的 Process 伺服器。</span><span class="sxs-lookup"><span data-stu-id="8ae03-123">The Process server to switch replication to.</span></span>

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

### <span data-ttu-id="8ae03-124">-確認</span><span class="sxs-lookup"><span data-stu-id="8ae03-124">-Confirm</span></span>
<span data-ttu-id="8ae03-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8ae03-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ae03-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ae03-126">-WhatIf</span></span>
<span data-ttu-id="8ae03-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ae03-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ae03-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ae03-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ae03-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae03-129">CommonParameters</span></span>
<span data-ttu-id="8ae03-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8ae03-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae03-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ae03-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae03-132">輸入</span><span class="sxs-lookup"><span data-stu-id="8ae03-132">INPUTS</span></span>

### <span data-ttu-id="8ae03-133">沒有</span><span class="sxs-lookup"><span data-stu-id="8ae03-133">None</span></span>

## <span data-ttu-id="8ae03-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8ae03-134">OUTPUTS</span></span>

### <span data-ttu-id="8ae03-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="8ae03-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8ae03-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8ae03-136">NOTES</span></span>

## <span data-ttu-id="8ae03-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ae03-137">RELATED LINKS</span></span>
