---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 7a2508669c0beba7fc9edd92ac645ce149633e05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624292"
---
# <span data-ttu-id="eb1cd-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="eb1cd-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="eb1cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb1cd-102">SYNOPSIS</span></span>
<span data-ttu-id="eb1cd-103">刪除指定的 Azure Site Recovery 防護容器對應。</span><span class="sxs-lookup"><span data-stu-id="eb1cd-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb1cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb1cd-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb1cd-105">說明</span><span class="sxs-lookup"><span data-stu-id="eb1cd-105">DESCRIPTION</span></span>
<span data-ttu-id="eb1cd-106">**AzureRmRecoveryServicesAsrProtectionContainerMapping** Cmdlet 會刪除指定的 Azure Site Recovery 防護容器對應。</span><span class="sxs-lookup"><span data-stu-id="eb1cd-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="eb1cd-107">示例</span><span class="sxs-lookup"><span data-stu-id="eb1cd-107">EXAMPLES</span></span>

### <span data-ttu-id="eb1cd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="eb1cd-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="eb1cd-109">開始刪除指定的保護容器對應，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="eb1cd-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="eb1cd-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb1cd-110">PARAMETERS</span></span>

### <span data-ttu-id="eb1cd-111">-確認</span><span class="sxs-lookup"><span data-stu-id="eb1cd-111">-Confirm</span></span>
<span data-ttu-id="eb1cd-112">指定是否需要確認。</span><span class="sxs-lookup"><span data-stu-id="eb1cd-112">Specify if confirmation is required.</span></span> <span data-ttu-id="eb1cd-113">將確認參數的值設定為 $false，以略過確認</span><span class="sxs-lookup"><span data-stu-id="eb1cd-113">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="eb1cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb1cd-114">-DefaultProfile</span></span>
<span data-ttu-id="eb1cd-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb1cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb1cd-116">-Force</span><span class="sxs-lookup"><span data-stu-id="eb1cd-116">-Force</span></span>
<span data-ttu-id="eb1cd-117">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="eb1cd-117">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="eb1cd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb1cd-118">-InputObject</span></span>
<span data-ttu-id="eb1cd-119">Cmdlet 的輸入物件：與要刪除之保護容器相對應的 ASR 保護容器對應物件。</span><span class="sxs-lookup"><span data-stu-id="eb1cd-119">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb1cd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb1cd-120">-WhatIf</span></span>
<span data-ttu-id="eb1cd-121">顯示在未實際執行 Cmdlet 的情況下執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb1cd-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="eb1cd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb1cd-122">CommonParameters</span></span>
<span data-ttu-id="eb1cd-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb1cd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb1cd-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb1cd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb1cd-125">輸入</span><span class="sxs-lookup"><span data-stu-id="eb1cd-125">INPUTS</span></span>

### <span data-ttu-id="eb1cd-126">RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="eb1cd-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="eb1cd-127">輸出</span><span class="sxs-lookup"><span data-stu-id="eb1cd-127">OUTPUTS</span></span>

### <span data-ttu-id="eb1cd-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="eb1cd-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="eb1cd-129">筆記</span><span class="sxs-lookup"><span data-stu-id="eb1cd-129">NOTES</span></span>

## <span data-ttu-id="eb1cd-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb1cd-130">RELATED LINKS</span></span>

[<span data-ttu-id="eb1cd-131">AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="eb1cd-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="eb1cd-132">新-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="eb1cd-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
