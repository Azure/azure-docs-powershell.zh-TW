---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b0780e4fb82a3e58e70f3a0bd64b5211ad07fd42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911862"
---
# <span data-ttu-id="630ab-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="630ab-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="630ab-102">簡介</span><span class="sxs-lookup"><span data-stu-id="630ab-102">SYNOPSIS</span></span>
<span data-ttu-id="630ab-103">更新 Azure 網站復原計畫的內容。</span><span class="sxs-lookup"><span data-stu-id="630ab-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="630ab-104">語法</span><span class="sxs-lookup"><span data-stu-id="630ab-104">SYNTAX</span></span>

### <span data-ttu-id="630ab-105">ByRPObject (預設) </span><span class="sxs-lookup"><span data-stu-id="630ab-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="630ab-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="630ab-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="630ab-107">描述</span><span class="sxs-lookup"><span data-stu-id="630ab-107">DESCRIPTION</span></span>
<span data-ttu-id="630ab-108">**Update-AzRecoveryServicesAsrRecoveryPlan** Cmdlet 會使用指定的 ASR 復原計畫物件或 ASR 復原計畫定義 json 檔案的內容更新復原計畫的內容。</span><span class="sxs-lookup"><span data-stu-id="630ab-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="630ab-109">例子</span><span class="sxs-lookup"><span data-stu-id="630ab-109">EXAMPLES</span></span>

### <span data-ttu-id="630ab-110">範例 1：更新復原計畫</span><span class="sxs-lookup"><span data-stu-id="630ab-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="630ab-111">使用指定的 ASR 復原計畫物件的內容開始更新復原計畫，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="630ab-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="630ab-112">參數</span><span class="sxs-lookup"><span data-stu-id="630ab-112">PARAMETERS</span></span>

### <span data-ttu-id="630ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="630ab-113">-DefaultProfile</span></span>
<span data-ttu-id="630ab-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="630ab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="630ab-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="630ab-115">-InputObject</span></span>
<span data-ttu-id="630ab-116">Cmdlet 的輸入物件：指定 ASR 復原計畫物件，其內容會用來更新物件所參考的復原計畫。</span><span class="sxs-lookup"><span data-stu-id="630ab-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="630ab-117">-路徑</span><span class="sxs-lookup"><span data-stu-id="630ab-117">-Path</span></span>
<span data-ttu-id="630ab-118">指定用來更新復原計畫的復原計畫定義 json 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="630ab-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="630ab-119">-確認</span><span class="sxs-lookup"><span data-stu-id="630ab-119">-Confirm</span></span>
<span data-ttu-id="630ab-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="630ab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="630ab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="630ab-121">-WhatIf</span></span>
<span data-ttu-id="630ab-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="630ab-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="630ab-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="630ab-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="630ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="630ab-124">CommonParameters</span></span>
<span data-ttu-id="630ab-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="630ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="630ab-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="630ab-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="630ab-127">輸入</span><span class="sxs-lookup"><span data-stu-id="630ab-127">INPUTS</span></span>

### <span data-ttu-id="630ab-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="630ab-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="630ab-129">輸出</span><span class="sxs-lookup"><span data-stu-id="630ab-129">OUTPUTS</span></span>

### <span data-ttu-id="630ab-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="630ab-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="630ab-131">筆記</span><span class="sxs-lookup"><span data-stu-id="630ab-131">NOTES</span></span>

## <span data-ttu-id="630ab-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="630ab-132">RELATED LINKS</span></span>

[<span data-ttu-id="630ab-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="630ab-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="630ab-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="630ab-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="630ab-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="630ab-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)
