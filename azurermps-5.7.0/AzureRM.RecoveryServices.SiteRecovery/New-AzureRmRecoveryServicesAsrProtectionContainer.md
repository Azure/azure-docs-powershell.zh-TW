---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 73d57e6e73b0e7e84dd3fb8bfff04ac8705bd108
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625008"
---
# <span data-ttu-id="c291a-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c291a-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="c291a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c291a-102">SYNOPSIS</span></span>
<span data-ttu-id="c291a-103">在指定的結構中建立 Azure Site Recovery 保護容器。</span><span class="sxs-lookup"><span data-stu-id="c291a-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c291a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c291a-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c291a-105">說明</span><span class="sxs-lookup"><span data-stu-id="c291a-105">DESCRIPTION</span></span>
<span data-ttu-id="c291a-106">New-AzureRmRecoveryServicesAsrProtectionContainer Cmdlet 會在指定的 Azure Site Recovery 結構下建立保護容器。</span><span class="sxs-lookup"><span data-stu-id="c291a-106">The New-AzureRmRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="c291a-107">示例</span><span class="sxs-lookup"><span data-stu-id="c291a-107">EXAMPLES</span></span>

### <span data-ttu-id="c291a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c291a-108">Example 1</span></span>
```
PS C:\> $job = New-AzureRmRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="c291a-109">使用指定的參數開始建立保護容器，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="c291a-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c291a-110">參數</span><span class="sxs-lookup"><span data-stu-id="c291a-110">PARAMETERS</span></span>

### <span data-ttu-id="c291a-111">-確認</span><span class="sxs-lookup"><span data-stu-id="c291a-111">-Confirm</span></span>
<span data-ttu-id="c291a-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c291a-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c291a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c291a-113">-DefaultProfile</span></span>
<span data-ttu-id="c291a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c291a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c291a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c291a-115">-InputObject</span></span>
<span data-ttu-id="c291a-116">在指定的輸入物件 (Azure Fabric) 中建立禁止複製容器。</span><span class="sxs-lookup"><span data-stu-id="c291a-116">Creates the replication protection container in specifed input Object (Azure Fabric).</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c291a-117">-Name</span></span>
<span data-ttu-id="c291a-118">保護容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c291a-118">Name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c291a-119">-WhatIf</span></span>
<span data-ttu-id="c291a-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c291a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c291a-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c291a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c291a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c291a-122">CommonParameters</span></span>
<span data-ttu-id="c291a-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c291a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c291a-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c291a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c291a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c291a-125">INPUTS</span></span>

### <span data-ttu-id="c291a-126">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c291a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c291a-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c291a-127">OUTPUTS</span></span>

### <span data-ttu-id="c291a-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c291a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c291a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c291a-129">NOTES</span></span>

## <span data-ttu-id="c291a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c291a-130">RELATED LINKS</span></span>
