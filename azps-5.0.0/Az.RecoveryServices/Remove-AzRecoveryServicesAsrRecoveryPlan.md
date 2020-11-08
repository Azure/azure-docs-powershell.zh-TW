---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 138fd84684fda149d66be85a0fabfbe4a2df0e52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139484"
---
# <span data-ttu-id="bf9ec-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bf9ec-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="bf9ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="bf9ec-103">從 [恢復服務] 保存庫刪除指定的 ASR 恢復方案。</span><span class="sxs-lookup"><span data-stu-id="bf9ec-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="bf9ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf9ec-104">SYNTAX</span></span>

### <span data-ttu-id="bf9ec-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="bf9ec-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf9ec-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bf9ec-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf9ec-107">說明</span><span class="sxs-lookup"><span data-stu-id="bf9ec-107">DESCRIPTION</span></span>
<span data-ttu-id="bf9ec-108">**AzRecoveryServicesAsrRecoveryPlan** Cmdlet 會從 [恢復服務] 保存庫中刪除指定的復原方案。</span><span class="sxs-lookup"><span data-stu-id="bf9ec-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="bf9ec-109">示例</span><span class="sxs-lookup"><span data-stu-id="bf9ec-109">EXAMPLES</span></span>

### <span data-ttu-id="bf9ec-110">範例1</span><span class="sxs-lookup"><span data-stu-id="bf9ec-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="bf9ec-111">開始刪除指定的復原方案，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="bf9ec-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="bf9ec-112">參數</span><span class="sxs-lookup"><span data-stu-id="bf9ec-112">PARAMETERS</span></span>

### <span data-ttu-id="bf9ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf9ec-113">-DefaultProfile</span></span>
<span data-ttu-id="bf9ec-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf9ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bf9ec-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf9ec-115">-InputObject</span></span>
<span data-ttu-id="bf9ec-116">Cmdlet 的輸入物件：對應至要刪除之復原方案的 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="bf9ec-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="bf9ec-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf9ec-117">-Name</span></span>
<span data-ttu-id="bf9ec-118">指定要刪除的復原方案名稱。</span><span class="sxs-lookup"><span data-stu-id="bf9ec-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="bf9ec-119">-確認</span><span class="sxs-lookup"><span data-stu-id="bf9ec-119">-Confirm</span></span>
<span data-ttu-id="bf9ec-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bf9ec-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf9ec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf9ec-121">-WhatIf</span></span>
<span data-ttu-id="bf9ec-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bf9ec-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf9ec-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bf9ec-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf9ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf9ec-124">CommonParameters</span></span>
<span data-ttu-id="bf9ec-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf9ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf9ec-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bf9ec-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf9ec-127">輸入</span><span class="sxs-lookup"><span data-stu-id="bf9ec-127">INPUTS</span></span>

### <span data-ttu-id="bf9ec-128">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bf9ec-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="bf9ec-129">輸出</span><span class="sxs-lookup"><span data-stu-id="bf9ec-129">OUTPUTS</span></span>

### <span data-ttu-id="bf9ec-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bf9ec-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bf9ec-131">筆記</span><span class="sxs-lookup"><span data-stu-id="bf9ec-131">NOTES</span></span>

## <span data-ttu-id="bf9ec-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf9ec-132">RELATED LINKS</span></span>

[<span data-ttu-id="bf9ec-133">AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bf9ec-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="bf9ec-134">新-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bf9ec-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="bf9ec-135">更新-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bf9ec-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


