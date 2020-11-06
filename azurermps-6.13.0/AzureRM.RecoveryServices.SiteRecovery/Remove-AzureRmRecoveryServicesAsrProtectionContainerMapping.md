---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: f034f91f026538bbae475466fbd9d3afa7067145
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455095"
---
# <span data-ttu-id="7811c-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7811c-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="7811c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7811c-102">SYNOPSIS</span></span>
<span data-ttu-id="7811c-103">刪除指定的 Azure Site Recovery 防護容器對應。</span><span class="sxs-lookup"><span data-stu-id="7811c-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7811c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7811c-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7811c-105">說明</span><span class="sxs-lookup"><span data-stu-id="7811c-105">DESCRIPTION</span></span>
<span data-ttu-id="7811c-106">**AzureRmRecoveryServicesAsrProtectionContainerMapping** Cmdlet 會刪除指定的 Azure Site Recovery 防護容器對應。</span><span class="sxs-lookup"><span data-stu-id="7811c-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="7811c-107">示例</span><span class="sxs-lookup"><span data-stu-id="7811c-107">EXAMPLES</span></span>

### <span data-ttu-id="7811c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7811c-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="7811c-109">開始刪除指定的保護容器對應，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="7811c-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7811c-110">參數</span><span class="sxs-lookup"><span data-stu-id="7811c-110">PARAMETERS</span></span>

### <span data-ttu-id="7811c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7811c-111">-DefaultProfile</span></span>
<span data-ttu-id="7811c-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7811c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7811c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7811c-113">-Force</span></span>
<span data-ttu-id="7811c-114">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="7811c-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="7811c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7811c-115">-InputObject</span></span>
<span data-ttu-id="7811c-116">Cmdlet 的輸入物件：與要刪除之保護容器相對應的 ASR 保護容器對應物件。</span><span class="sxs-lookup"><span data-stu-id="7811c-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7811c-117">-確認</span><span class="sxs-lookup"><span data-stu-id="7811c-117">-Confirm</span></span>
<span data-ttu-id="7811c-118">指定是否需要確認。</span><span class="sxs-lookup"><span data-stu-id="7811c-118">Specify if confirmation is required.</span></span> <span data-ttu-id="7811c-119">將確認參數的值設定為 $false，以略過確認</span><span class="sxs-lookup"><span data-stu-id="7811c-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="7811c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7811c-120">-WhatIf</span></span>
<span data-ttu-id="7811c-121">顯示在未實際執行 Cmdlet 的情況下執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7811c-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="7811c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7811c-122">CommonParameters</span></span>
<span data-ttu-id="7811c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7811c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7811c-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7811c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7811c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="7811c-125">INPUTS</span></span>

### <span data-ttu-id="7811c-126">RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7811c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="7811c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="7811c-127">OUTPUTS</span></span>

### <span data-ttu-id="7811c-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7811c-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7811c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="7811c-129">NOTES</span></span>

## <span data-ttu-id="7811c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="7811c-130">RELATED LINKS</span></span>

[<span data-ttu-id="7811c-131">AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7811c-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="7811c-132">新-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="7811c-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
