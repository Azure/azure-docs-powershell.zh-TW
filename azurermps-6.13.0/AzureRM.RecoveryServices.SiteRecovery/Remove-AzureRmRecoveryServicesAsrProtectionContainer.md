---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 0cc4a1c58349157024f38bce6e5ee2d8bcaa3cd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455099"
---
# <span data-ttu-id="cb6c2-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cb6c2-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="cb6c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb6c2-102">SYNOPSIS</span></span>
<span data-ttu-id="cb6c2-103">從其結構中刪除指定的保護容器。</span><span class="sxs-lookup"><span data-stu-id="cb6c2-103">Deletes the specified Protection Container from its Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb6c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb6c2-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb6c2-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb6c2-105">DESCRIPTION</span></span>
<span data-ttu-id="cb6c2-106">Remove-AzureRmRecoveryServicesAsrProtectionContainer Cmdlet 會刪除指定的 Azure Site Recovery 防護容器。</span><span class="sxs-lookup"><span data-stu-id="cb6c2-106">The Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="cb6c2-107">示例</span><span class="sxs-lookup"><span data-stu-id="cb6c2-107">EXAMPLES</span></span>

### <span data-ttu-id="cb6c2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="cb6c2-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="cb6c2-109">開始刪除指定的保護容器，並傳回用於追蹤移除操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="cb6c2-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="cb6c2-110">參數</span><span class="sxs-lookup"><span data-stu-id="cb6c2-110">PARAMETERS</span></span>

### <span data-ttu-id="cb6c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb6c2-111">-DefaultProfile</span></span>
<span data-ttu-id="cb6c2-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb6c2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb6c2-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb6c2-113">-InputObject</span></span>
<span data-ttu-id="cb6c2-114">指定要移除的保護容器。</span><span class="sxs-lookup"><span data-stu-id="cb6c2-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb6c2-115">-確認</span><span class="sxs-lookup"><span data-stu-id="cb6c2-115">-Confirm</span></span>
<span data-ttu-id="cb6c2-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb6c2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb6c2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb6c2-117">-WhatIf</span></span>
<span data-ttu-id="cb6c2-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb6c2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb6c2-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb6c2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb6c2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb6c2-120">CommonParameters</span></span>
<span data-ttu-id="cb6c2-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb6c2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb6c2-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb6c2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb6c2-123">輸入</span><span class="sxs-lookup"><span data-stu-id="cb6c2-123">INPUTS</span></span>

### <span data-ttu-id="cb6c2-124">RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cb6c2-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="cb6c2-125">輸出</span><span class="sxs-lookup"><span data-stu-id="cb6c2-125">OUTPUTS</span></span>

### <span data-ttu-id="cb6c2-126">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cb6c2-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cb6c2-127">筆記</span><span class="sxs-lookup"><span data-stu-id="cb6c2-127">NOTES</span></span>

## <span data-ttu-id="cb6c2-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb6c2-128">RELATED LINKS</span></span>
