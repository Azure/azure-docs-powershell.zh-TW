---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 96c50c812dcb73c92dc3704e576bfc45fbf21bba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902233"
---
# <span data-ttu-id="cec09-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cec09-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="cec09-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cec09-102">SYNOPSIS</span></span>
<span data-ttu-id="cec09-103">從修復服務儲存庫刪除指定的 ASR 復原計畫。</span><span class="sxs-lookup"><span data-stu-id="cec09-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="cec09-104">語法</span><span class="sxs-lookup"><span data-stu-id="cec09-104">SYNTAX</span></span>

### <span data-ttu-id="cec09-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="cec09-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cec09-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cec09-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cec09-107">描述</span><span class="sxs-lookup"><span data-stu-id="cec09-107">DESCRIPTION</span></span>
<span data-ttu-id="cec09-108">**Remove-AzRecoveryServicesrRecoveryPlan** Cmdlet 會從修復服務儲存庫刪除指定的復原計畫。</span><span class="sxs-lookup"><span data-stu-id="cec09-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="cec09-109">例子</span><span class="sxs-lookup"><span data-stu-id="cec09-109">EXAMPLES</span></span>

### <span data-ttu-id="cec09-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="cec09-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="cec09-111">開始刪除指定的復原計畫，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="cec09-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="cec09-112">參數</span><span class="sxs-lookup"><span data-stu-id="cec09-112">PARAMETERS</span></span>

### <span data-ttu-id="cec09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cec09-113">-DefaultProfile</span></span>
<span data-ttu-id="cec09-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cec09-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cec09-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cec09-115">-InputObject</span></span>
<span data-ttu-id="cec09-116">Cmdlet 的輸入物件：對應到要刪除之復原計畫的 ASR 復原計畫物件。</span><span class="sxs-lookup"><span data-stu-id="cec09-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cec09-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="cec09-117">-Name</span></span>
<span data-ttu-id="cec09-118">指定要刪除的復原計畫名稱。</span><span class="sxs-lookup"><span data-stu-id="cec09-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="cec09-119">-確認</span><span class="sxs-lookup"><span data-stu-id="cec09-119">-Confirm</span></span>
<span data-ttu-id="cec09-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cec09-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cec09-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cec09-121">-WhatIf</span></span>
<span data-ttu-id="cec09-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cec09-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cec09-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cec09-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cec09-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cec09-124">CommonParameters</span></span>
<span data-ttu-id="cec09-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cec09-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cec09-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cec09-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cec09-127">輸入</span><span class="sxs-lookup"><span data-stu-id="cec09-127">INPUTS</span></span>

### <span data-ttu-id="cec09-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cec09-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="cec09-129">輸出</span><span class="sxs-lookup"><span data-stu-id="cec09-129">OUTPUTS</span></span>

### <span data-ttu-id="cec09-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="cec09-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cec09-131">筆記</span><span class="sxs-lookup"><span data-stu-id="cec09-131">NOTES</span></span>

## <span data-ttu-id="cec09-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="cec09-132">RELATED LINKS</span></span>

[<span data-ttu-id="cec09-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cec09-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="cec09-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cec09-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="cec09-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cec09-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


