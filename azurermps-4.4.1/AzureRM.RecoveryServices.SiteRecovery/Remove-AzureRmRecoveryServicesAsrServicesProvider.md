---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 5220271538903206876dd8d5c476824e1ac10874
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456427"
---
# <span data-ttu-id="576b3-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="576b3-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="576b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="576b3-102">SYNOPSIS</span></span>
<span data-ttu-id="576b3-103">從 [恢復服務] 保存庫刪除/取消註冊指定的 Azure Site Recovery 復原服務提供者。</span><span class="sxs-lookup"><span data-stu-id="576b3-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="576b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="576b3-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="576b3-105">說明</span><span class="sxs-lookup"><span data-stu-id="576b3-105">DESCRIPTION</span></span>
<span data-ttu-id="576b3-106">**AzureRmRecoveryServicesAsrServicesProvider** Cmdlet 會從保存庫中移除指定的 Azure Site recovery 復原服務提供者。</span><span class="sxs-lookup"><span data-stu-id="576b3-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="576b3-107">示例</span><span class="sxs-lookup"><span data-stu-id="576b3-107">EXAMPLES</span></span>

### <span data-ttu-id="576b3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="576b3-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="576b3-109">啟動指定 Azure 網站復原服務提供者的刪除/登出，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="576b3-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="576b3-110">參數</span><span class="sxs-lookup"><span data-stu-id="576b3-110">PARAMETERS</span></span>

### <span data-ttu-id="576b3-111">-Force</span><span class="sxs-lookup"><span data-stu-id="576b3-111">-Force</span></span>
<span data-ttu-id="576b3-112">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="576b3-112">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576b3-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="576b3-113">-InputObject</span></span>
<span data-ttu-id="576b3-114">Cmdlet 的輸入物件：對應至要刪除之 ASR 恢復服務提供者的 ASR 恢復服務提供者物件。</span><span class="sxs-lookup"><span data-stu-id="576b3-114">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="576b3-115">-確認</span><span class="sxs-lookup"><span data-stu-id="576b3-115">-Confirm</span></span>
<span data-ttu-id="576b3-116">指定是否需要確認。</span><span class="sxs-lookup"><span data-stu-id="576b3-116">Specify if confirmation is required.</span></span> <span data-ttu-id="576b3-117">將確認參數的值設定為 [$false]，以略過確認。</span><span class="sxs-lookup"><span data-stu-id="576b3-117">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576b3-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="576b3-118">-WhatIf</span></span>
<span data-ttu-id="576b3-119">顯示在未實際執行 Cmdlet 的情況下執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="576b3-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576b3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576b3-120">CommonParameters</span></span>
<span data-ttu-id="576b3-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="576b3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576b3-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="576b3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576b3-123">輸入</span><span class="sxs-lookup"><span data-stu-id="576b3-123">INPUTS</span></span>

### <span data-ttu-id="576b3-124">RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="576b3-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="576b3-125">輸出</span><span class="sxs-lookup"><span data-stu-id="576b3-125">OUTPUTS</span></span>

### <span data-ttu-id="576b3-126">System.object. IEnumerable "1 [ASRJob，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="576b3-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="576b3-127">筆記</span><span class="sxs-lookup"><span data-stu-id="576b3-127">NOTES</span></span>

## <span data-ttu-id="576b3-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="576b3-128">RELATED LINKS</span></span>

[<span data-ttu-id="576b3-129">AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="576b3-129">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="576b3-130">更新-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="576b3-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
