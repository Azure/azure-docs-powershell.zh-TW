---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 496eeed8b4ed4b41ce2c67d47fc636711cd5cb84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448618"
---
# <span data-ttu-id="c1c4f-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c1c4f-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="c1c4f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c4f-103">從其結構中刪除指定的保護容器。</span><span class="sxs-lookup"><span data-stu-id="c1c4f-103">Deletes the specified Protection Container from its Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1c4f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1c4f-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1c4f-105">說明</span><span class="sxs-lookup"><span data-stu-id="c1c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="c1c4f-106">Remove-AzureRmRecoveryServicesAsrProtectionContainer Cmdlet 會刪除指定的 Azure Site Recovery 防護容器。</span><span class="sxs-lookup"><span data-stu-id="c1c4f-106">The Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="c1c4f-107">示例</span><span class="sxs-lookup"><span data-stu-id="c1c4f-107">EXAMPLES</span></span>

### <span data-ttu-id="c1c4f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c1c4f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="c1c4f-109">開始刪除指定的保護容器，並傳回用於追蹤移除操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="c1c4f-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="c1c4f-110">參數</span><span class="sxs-lookup"><span data-stu-id="c1c4f-110">PARAMETERS</span></span>

### <span data-ttu-id="c1c4f-111">-確認</span><span class="sxs-lookup"><span data-stu-id="c1c4f-111">-Confirm</span></span>
<span data-ttu-id="c1c4f-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c1c4f-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1c4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c4f-113">-DefaultProfile</span></span>
<span data-ttu-id="c1c4f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1c4f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1c4f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1c4f-115">-InputObject</span></span>
<span data-ttu-id="c1c4f-116">指定要移除的保護容器。</span><span class="sxs-lookup"><span data-stu-id="c1c4f-116">Specifies the protection container to be removed .</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c4f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1c4f-117">-WhatIf</span></span>
<span data-ttu-id="c1c4f-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1c4f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1c4f-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1c4f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1c4f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c4f-120">CommonParameters</span></span>
<span data-ttu-id="c1c4f-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1c4f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c4f-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1c4f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c4f-123">輸入</span><span class="sxs-lookup"><span data-stu-id="c1c4f-123">INPUTS</span></span>

### <span data-ttu-id="c1c4f-124">RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c1c4f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="c1c4f-125">輸出</span><span class="sxs-lookup"><span data-stu-id="c1c4f-125">OUTPUTS</span></span>

### <span data-ttu-id="c1c4f-126">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c1c4f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c1c4f-127">筆記</span><span class="sxs-lookup"><span data-stu-id="c1c4f-127">NOTES</span></span>

## <span data-ttu-id="c1c4f-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1c4f-128">RELATED LINKS</span></span>
