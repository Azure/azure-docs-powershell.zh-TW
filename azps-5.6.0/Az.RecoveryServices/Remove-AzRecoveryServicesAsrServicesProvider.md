---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: f3c18813cd3c002270d655b88fbc9285338a4338
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902209"
---
# <span data-ttu-id="3142f-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3142f-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="3142f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3142f-102">SYNOPSIS</span></span>
<span data-ttu-id="3142f-103">從復原服務庫刪除/取消註冊指定的 Azure 網站復原服務提供者。</span><span class="sxs-lookup"><span data-stu-id="3142f-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="3142f-104">語法</span><span class="sxs-lookup"><span data-stu-id="3142f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3142f-105">描述</span><span class="sxs-lookup"><span data-stu-id="3142f-105">DESCRIPTION</span></span>
<span data-ttu-id="3142f-106">**Remove-AzRecoveryServicesAsrServicesProvider Cmdlet** 會從儲存庫移除指定的 Azure 網站復原服務提供者。</span><span class="sxs-lookup"><span data-stu-id="3142f-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="3142f-107">例子</span><span class="sxs-lookup"><span data-stu-id="3142f-107">EXAMPLES</span></span>

### <span data-ttu-id="3142f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="3142f-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="3142f-109">開始刪除/取消註冊指定的 Azure 網站修復服務提供者，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="3142f-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3142f-110">參數</span><span class="sxs-lookup"><span data-stu-id="3142f-110">PARAMETERS</span></span>

### <span data-ttu-id="3142f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3142f-111">-DefaultProfile</span></span>
<span data-ttu-id="3142f-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3142f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3142f-113">-強制</span><span class="sxs-lookup"><span data-stu-id="3142f-113">-Force</span></span>
<span data-ttu-id="3142f-114">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="3142f-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="3142f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3142f-115">-InputObject</span></span>
<span data-ttu-id="3142f-116">Cmdlet 的輸入物件：對應至要刪除之 ASR 復原服務提供者的 ASR 修復服務提供者物件。</span><span class="sxs-lookup"><span data-stu-id="3142f-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3142f-117">-確認</span><span class="sxs-lookup"><span data-stu-id="3142f-117">-Confirm</span></span>
<span data-ttu-id="3142f-118">指定如果需要確認。</span><span class="sxs-lookup"><span data-stu-id="3142f-118">Specify if confirmation is required.</span></span> <span data-ttu-id="3142f-119">將確認參數的值設定為$false跳過確認。</span><span class="sxs-lookup"><span data-stu-id="3142f-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="3142f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3142f-120">-WhatIf</span></span>
<span data-ttu-id="3142f-121">顯示執行 Cmdlet 而不實際執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3142f-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="3142f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3142f-122">CommonParameters</span></span>
<span data-ttu-id="3142f-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3142f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3142f-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3142f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3142f-125">輸入</span><span class="sxs-lookup"><span data-stu-id="3142f-125">INPUTS</span></span>

### <span data-ttu-id="3142f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3142f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="3142f-127">輸出</span><span class="sxs-lookup"><span data-stu-id="3142f-127">OUTPUTS</span></span>

### <span data-ttu-id="3142f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="3142f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3142f-129">筆記</span><span class="sxs-lookup"><span data-stu-id="3142f-129">NOTES</span></span>

## <span data-ttu-id="3142f-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="3142f-130">RELATED LINKS</span></span>

[<span data-ttu-id="3142f-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3142f-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="3142f-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3142f-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
