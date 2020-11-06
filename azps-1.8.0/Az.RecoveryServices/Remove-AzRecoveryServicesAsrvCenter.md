---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: c1ac3ae34e92feb2b356d5946a7b9f0a30a0a2aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621070"
---
# <span data-ttu-id="e16e5-101">Remove-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="e16e5-101">Remove-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="e16e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e16e5-102">SYNOPSIS</span></span>
<span data-ttu-id="e16e5-103">從 ASR 結構中移除 vCenter 伺服器，並停止從 vCenter 伺服器探索虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e16e5-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="e16e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="e16e5-104">SYNTAX</span></span>

### <span data-ttu-id="e16e5-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="e16e5-105">Default (Default)</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e16e5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e16e5-106">ByResourceId</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e16e5-107">ByName</span><span class="sxs-lookup"><span data-stu-id="e16e5-107">ByName</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e16e5-108">說明</span><span class="sxs-lookup"><span data-stu-id="e16e5-108">DESCRIPTION</span></span>
<span data-ttu-id="e16e5-109">**AzRecoveryServicesAsrvCenter** Cmdlet 會從 ASR 結構中移除 vCenter 伺服器，並停止從 vCenter 伺服器探索虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e16e5-109">The **Remove-AzRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="e16e5-110">示例</span><span class="sxs-lookup"><span data-stu-id="e16e5-110">EXAMPLES</span></span>

### <span data-ttu-id="e16e5-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e16e5-111">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="e16e5-112">從 ASR 結構中移除 vCenter 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e16e5-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="e16e5-113">參數</span><span class="sxs-lookup"><span data-stu-id="e16e5-113">PARAMETERS</span></span>

### <span data-ttu-id="e16e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e16e5-114">-DefaultProfile</span></span>
<span data-ttu-id="e16e5-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e16e5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e16e5-116">-結構</span><span class="sxs-lookup"><span data-stu-id="e16e5-116">-Fabric</span></span>
<span data-ttu-id="e16e5-117">代表佈建服務器的 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="e16e5-117">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e16e5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e16e5-118">-InputObject</span></span>
<span data-ttu-id="e16e5-119">要移除的 vCenter 伺服器所代表的 ASR vCenter 物件。</span><span class="sxs-lookup"><span data-stu-id="e16e5-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e16e5-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e16e5-120">-Name</span></span>
<span data-ttu-id="e16e5-121">VCenter 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e16e5-121">Name of the vCenter Server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16e5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e16e5-122">-ResourceId</span></span>
<span data-ttu-id="e16e5-123">指定要移除的 vCenter resourceId。</span><span class="sxs-lookup"><span data-stu-id="e16e5-123">Specifies the resourceId of vCenter to remove.</span></span>

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

### <span data-ttu-id="e16e5-124">-確認</span><span class="sxs-lookup"><span data-stu-id="e16e5-124">-Confirm</span></span>
<span data-ttu-id="e16e5-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e16e5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e16e5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e16e5-126">-WhatIf</span></span>
<span data-ttu-id="e16e5-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e16e5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e16e5-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e16e5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e16e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e16e5-129">CommonParameters</span></span>
<span data-ttu-id="e16e5-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e16e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e16e5-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e16e5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e16e5-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e16e5-132">INPUTS</span></span>

### <span data-ttu-id="e16e5-133">System.object</span><span class="sxs-lookup"><span data-stu-id="e16e5-133">System.String</span></span>

### <span data-ttu-id="e16e5-134">RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="e16e5-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

### <span data-ttu-id="e16e5-135">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e16e5-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e16e5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e16e5-136">OUTPUTS</span></span>

### <span data-ttu-id="e16e5-137">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e16e5-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e16e5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e16e5-138">NOTES</span></span>

## <span data-ttu-id="e16e5-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e16e5-139">RELATED LINKS</span></span>
