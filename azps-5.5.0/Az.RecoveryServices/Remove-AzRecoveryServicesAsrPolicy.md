---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133651"
---
# <span data-ttu-id="a5fc5-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="a5fc5-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="a5fc5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="a5fc5-103">從 [恢復服務] 保存庫刪除指定的 ASR 複製原則。</span><span class="sxs-lookup"><span data-stu-id="a5fc5-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="a5fc5-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5fc5-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5fc5-105">說明</span><span class="sxs-lookup"><span data-stu-id="a5fc5-105">DESCRIPTION</span></span>
<span data-ttu-id="a5fc5-106">**AzRecoveryServicesAsrPolicy** Cmdlet 已從復原服務保存庫中刪除指定的複製原則。</span><span class="sxs-lookup"><span data-stu-id="a5fc5-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="a5fc5-107">示例</span><span class="sxs-lookup"><span data-stu-id="a5fc5-107">EXAMPLES</span></span>

### <span data-ttu-id="a5fc5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a5fc5-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="a5fc5-109">開始刪除指定的複製原則，並傳回用於追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="a5fc5-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a5fc5-110">參數</span><span class="sxs-lookup"><span data-stu-id="a5fc5-110">PARAMETERS</span></span>

### <span data-ttu-id="a5fc5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5fc5-111">-DefaultProfile</span></span>
<span data-ttu-id="a5fc5-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5fc5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a5fc5-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5fc5-113">-InputObject</span></span>
<span data-ttu-id="a5fc5-114">Cmdlet 的輸入物件：與要刪除之複製原則相對應的 ASR 複製原則物件。</span><span class="sxs-lookup"><span data-stu-id="a5fc5-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="a5fc5-115">-確認</span><span class="sxs-lookup"><span data-stu-id="a5fc5-115">-Confirm</span></span>
<span data-ttu-id="a5fc5-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a5fc5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5fc5-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5fc5-117">-WhatIf</span></span>
<span data-ttu-id="a5fc5-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5fc5-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5fc5-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5fc5-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5fc5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5fc5-120">CommonParameters</span></span>
<span data-ttu-id="a5fc5-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5fc5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5fc5-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a5fc5-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5fc5-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a5fc5-123">INPUTS</span></span>

### <span data-ttu-id="a5fc5-124">RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="a5fc5-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="a5fc5-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a5fc5-125">OUTPUTS</span></span>

### <span data-ttu-id="a5fc5-126">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a5fc5-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a5fc5-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a5fc5-127">NOTES</span></span>

## <span data-ttu-id="a5fc5-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5fc5-128">RELATED LINKS</span></span>

[<span data-ttu-id="a5fc5-129">AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="a5fc5-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="a5fc5-130">新-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="a5fc5-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
