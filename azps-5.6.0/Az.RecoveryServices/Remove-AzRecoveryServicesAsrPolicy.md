---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 5743d1d9288f0045755aab752274c24640b3c548
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902241"
---
# <span data-ttu-id="d9054-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d9054-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="d9054-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d9054-102">SYNOPSIS</span></span>
<span data-ttu-id="d9054-103">從修復服務儲存庫刪除指定的 ASR 複本策略。</span><span class="sxs-lookup"><span data-stu-id="d9054-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="d9054-104">語法</span><span class="sxs-lookup"><span data-stu-id="d9054-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9054-105">描述</span><span class="sxs-lookup"><span data-stu-id="d9054-105">DESCRIPTION</span></span>
<span data-ttu-id="d9054-106">**Remove-AzRecoveryServicesAsrPolicy** Cmdlet 已刪除復原服務庫中指定的複本策略。</span><span class="sxs-lookup"><span data-stu-id="d9054-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="d9054-107">例子</span><span class="sxs-lookup"><span data-stu-id="d9054-107">EXAMPLES</span></span>

### <span data-ttu-id="d9054-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="d9054-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="d9054-109">開始刪除指定的複寫原則，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="d9054-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d9054-110">參數</span><span class="sxs-lookup"><span data-stu-id="d9054-110">PARAMETERS</span></span>

### <span data-ttu-id="d9054-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9054-111">-DefaultProfile</span></span>
<span data-ttu-id="d9054-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9054-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d9054-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9054-113">-InputObject</span></span>
<span data-ttu-id="d9054-114">Cmdlet 的輸入物件：對應到要刪除之複寫原則的 ASR 複寫原則物件。</span><span class="sxs-lookup"><span data-stu-id="d9054-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9054-115">-確認</span><span class="sxs-lookup"><span data-stu-id="d9054-115">-Confirm</span></span>
<span data-ttu-id="d9054-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d9054-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9054-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9054-117">-WhatIf</span></span>
<span data-ttu-id="d9054-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9054-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9054-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9054-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9054-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9054-120">CommonParameters</span></span>
<span data-ttu-id="d9054-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d9054-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9054-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9054-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9054-123">輸入</span><span class="sxs-lookup"><span data-stu-id="d9054-123">INPUTS</span></span>

### <span data-ttu-id="d9054-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="d9054-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="d9054-125">輸出</span><span class="sxs-lookup"><span data-stu-id="d9054-125">OUTPUTS</span></span>

### <span data-ttu-id="d9054-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d9054-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d9054-127">筆記</span><span class="sxs-lookup"><span data-stu-id="d9054-127">NOTES</span></span>

## <span data-ttu-id="d9054-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9054-128">RELATED LINKS</span></span>

[<span data-ttu-id="d9054-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d9054-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="d9054-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d9054-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
