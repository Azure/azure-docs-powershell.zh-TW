---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: be521545111667493c5b0e268013ffa4464ed3a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444412"
---
# <span data-ttu-id="10d53-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="10d53-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="10d53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10d53-102">SYNOPSIS</span></span>
<span data-ttu-id="10d53-103">更新指定的 azure site recovery 網路對應。</span><span class="sxs-lookup"><span data-stu-id="10d53-103">Updates the specified azure site recovery network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10d53-104">句法</span><span class="sxs-lookup"><span data-stu-id="10d53-104">SYNTAX</span></span>

### <span data-ttu-id="10d53-105">ByNetworkObject (預設) </span><span class="sxs-lookup"><span data-stu-id="10d53-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10d53-106">ById</span><span class="sxs-lookup"><span data-stu-id="10d53-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10d53-107">說明</span><span class="sxs-lookup"><span data-stu-id="10d53-107">DESCRIPTION</span></span>
<span data-ttu-id="10d53-108">**AzureRmRecoveryServicesAsrNetworkMapping** Cmdlet 會更新指定的 Azure Site Recovery 網路對應。</span><span class="sxs-lookup"><span data-stu-id="10d53-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="10d53-109">示例</span><span class="sxs-lookup"><span data-stu-id="10d53-109">EXAMPLES</span></span>

### <span data-ttu-id="10d53-110">範例1</span><span class="sxs-lookup"><span data-stu-id="10d53-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="10d53-111">使用指定的參數啟動更新網路對應作業，並傳回用來追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="10d53-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="10d53-112">參數</span><span class="sxs-lookup"><span data-stu-id="10d53-112">PARAMETERS</span></span>

### <span data-ttu-id="10d53-113">-確認</span><span class="sxs-lookup"><span data-stu-id="10d53-113">-Confirm</span></span>
<span data-ttu-id="10d53-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10d53-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10d53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d53-115">-DefaultProfile</span></span>
<span data-ttu-id="10d53-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10d53-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="10d53-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10d53-117">-InputObject</span></span>
<span data-ttu-id="10d53-118">輸入物件：指定要更新之 ASR 網路對應的 ASR 網路對應物件。</span><span class="sxs-lookup"><span data-stu-id="10d53-118">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10d53-119">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="10d53-119">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="10d53-120">指定網路對應的 [恢復 azure 網路識別碼]。</span><span class="sxs-lookup"><span data-stu-id="10d53-120">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d53-121">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="10d53-121">-RecoveryNetwork</span></span>
<span data-ttu-id="10d53-122">指定網路對應的恢復網路物件。</span><span class="sxs-lookup"><span data-stu-id="10d53-122">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d53-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10d53-123">-WhatIf</span></span>
<span data-ttu-id="10d53-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10d53-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10d53-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10d53-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10d53-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d53-126">CommonParameters</span></span>
<span data-ttu-id="10d53-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10d53-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d53-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10d53-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d53-129">輸入</span><span class="sxs-lookup"><span data-stu-id="10d53-129">INPUTS</span></span>

### <span data-ttu-id="10d53-130">所有</span><span class="sxs-lookup"><span data-stu-id="10d53-130">None</span></span>

## <span data-ttu-id="10d53-131">輸出</span><span class="sxs-lookup"><span data-stu-id="10d53-131">OUTPUTS</span></span>

### <span data-ttu-id="10d53-132">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="10d53-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="10d53-133">筆記</span><span class="sxs-lookup"><span data-stu-id="10d53-133">NOTES</span></span>

## <span data-ttu-id="10d53-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="10d53-134">RELATED LINKS</span></span>
