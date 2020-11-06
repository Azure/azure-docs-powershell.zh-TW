---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 33410022800111097610116732f6f137dfac41bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621017"
---
# <span data-ttu-id="2a45d-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2a45d-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="2a45d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a45d-102">SYNOPSIS</span></span>
<span data-ttu-id="2a45d-103">更新 Azure 網站復原方案的內容。</span><span class="sxs-lookup"><span data-stu-id="2a45d-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="2a45d-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a45d-104">SYNTAX</span></span>

### <span data-ttu-id="2a45d-105">ByRPObject (預設) </span><span class="sxs-lookup"><span data-stu-id="2a45d-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a45d-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="2a45d-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a45d-107">說明</span><span class="sxs-lookup"><span data-stu-id="2a45d-107">DESCRIPTION</span></span>
<span data-ttu-id="2a45d-108">**AzRecoveryServicesAsrRecoveryPlan** Cmdlet 會使用指定的 ASR 恢復方案物件或 ASR 復原方案定義 json 檔案的內容來更新復原方案的內容。</span><span class="sxs-lookup"><span data-stu-id="2a45d-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="2a45d-109">示例</span><span class="sxs-lookup"><span data-stu-id="2a45d-109">EXAMPLES</span></span>

### <span data-ttu-id="2a45d-110">範例1：更新復原方案</span><span class="sxs-lookup"><span data-stu-id="2a45d-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="2a45d-111">使用指定的 ASR 恢復方案物件的內容來開始更新復原方案，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="2a45d-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2a45d-112">參數</span><span class="sxs-lookup"><span data-stu-id="2a45d-112">PARAMETERS</span></span>

### <span data-ttu-id="2a45d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a45d-113">-DefaultProfile</span></span>
<span data-ttu-id="2a45d-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a45d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2a45d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a45d-115">-InputObject</span></span>
<span data-ttu-id="2a45d-116">Cmdlet 的輸入物件：指定 ASR 復原方案物件，這些物件的內容是用來更新物件所參照的復原方案。</span><span class="sxs-lookup"><span data-stu-id="2a45d-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

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

### <span data-ttu-id="2a45d-117">-Path</span><span class="sxs-lookup"><span data-stu-id="2a45d-117">-Path</span></span>
<span data-ttu-id="2a45d-118">指定用來更新復原方案之復原方案定義 json 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="2a45d-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

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

### <span data-ttu-id="2a45d-119">-確認</span><span class="sxs-lookup"><span data-stu-id="2a45d-119">-Confirm</span></span>
<span data-ttu-id="2a45d-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2a45d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a45d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a45d-121">-WhatIf</span></span>
<span data-ttu-id="2a45d-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a45d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a45d-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a45d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a45d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a45d-124">CommonParameters</span></span>
<span data-ttu-id="2a45d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a45d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a45d-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a45d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a45d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2a45d-127">INPUTS</span></span>

### <span data-ttu-id="2a45d-128">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2a45d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="2a45d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2a45d-129">OUTPUTS</span></span>

### <span data-ttu-id="2a45d-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2a45d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2a45d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2a45d-131">NOTES</span></span>

## <span data-ttu-id="2a45d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a45d-132">RELATED LINKS</span></span>

[<span data-ttu-id="2a45d-133">AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2a45d-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2a45d-134">新-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2a45d-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2a45d-135">移除-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2a45d-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)
