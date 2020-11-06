---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ab2cca2fc0b517d8923d117978887c6dd0196ce5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453332"
---
# <span data-ttu-id="d7068-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d7068-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="d7068-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d7068-102">SYNOPSIS</span></span>
<span data-ttu-id="d7068-103">在兩個網路之間建立 ASR 網路對應。</span><span class="sxs-lookup"><span data-stu-id="d7068-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7068-104">句法</span><span class="sxs-lookup"><span data-stu-id="d7068-104">SYNTAX</span></span>

### <span data-ttu-id="d7068-105">EnterpriseToEnterprise (預設) </span><span class="sxs-lookup"><span data-stu-id="d7068-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7068-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="d7068-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7068-107">說明</span><span class="sxs-lookup"><span data-stu-id="d7068-107">DESCRIPTION</span></span>
<span data-ttu-id="d7068-108">**新的-AzureRmRecoveryServicesAsrNetworkMapping** Cmdlet 會啟動在兩個網路之間建立 ASR 網路對應的作業，並傳回用於追蹤作業之 asr 作業的 asr 工作物件。</span><span class="sxs-lookup"><span data-stu-id="d7068-108">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d7068-109">示例</span><span class="sxs-lookup"><span data-stu-id="d7068-109">EXAMPLES</span></span>

### <span data-ttu-id="d7068-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d7068-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="d7068-111">使用指定的名稱、主要和恢復網路來啟動網路對應建立作業，並傳回 ASR 作業來追蹤作業。</span><span class="sxs-lookup"><span data-stu-id="d7068-111">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

## <span data-ttu-id="d7068-112">參數</span><span class="sxs-lookup"><span data-stu-id="d7068-112">PARAMETERS</span></span>

### <span data-ttu-id="d7068-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7068-113">-Name</span></span>
<span data-ttu-id="d7068-114">要建立之 ASR 網路對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7068-114">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="d7068-115">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="d7068-115">-PrimaryNetwork</span></span>
<span data-ttu-id="d7068-116">指定網路對應的主要網路物件。</span><span class="sxs-lookup"><span data-stu-id="d7068-116">Specifies the primary network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7068-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="d7068-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="d7068-118">指定網路對應的 [恢復 azure 網路識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d7068-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7068-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="d7068-119">-RecoveryNetwork</span></span>
<span data-ttu-id="d7068-120">指定網路對應的恢復網路物件。</span><span class="sxs-lookup"><span data-stu-id="d7068-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7068-121">-確認</span><span class="sxs-lookup"><span data-stu-id="d7068-121">-Confirm</span></span>
<span data-ttu-id="d7068-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d7068-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7068-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7068-123">-WhatIf</span></span>
<span data-ttu-id="d7068-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d7068-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7068-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d7068-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7068-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7068-126">CommonParameters</span></span>
<span data-ttu-id="d7068-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d7068-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7068-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d7068-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7068-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d7068-129">INPUTS</span></span>

### <span data-ttu-id="d7068-130">RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="d7068-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="d7068-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d7068-131">OUTPUTS</span></span>

### <span data-ttu-id="d7068-132">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d7068-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d7068-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d7068-133">NOTES</span></span>

## <span data-ttu-id="d7068-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7068-134">RELATED LINKS</span></span>

[<span data-ttu-id="d7068-135">AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d7068-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="d7068-136">移除-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="d7068-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
