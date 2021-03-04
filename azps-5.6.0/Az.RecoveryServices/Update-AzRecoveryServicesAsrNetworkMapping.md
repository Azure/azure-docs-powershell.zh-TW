---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 6041973d4bab91310ed213d461cf97db9cc5e720
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912622"
---
# <span data-ttu-id="ed742-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="ed742-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="ed742-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ed742-102">SYNOPSIS</span></span>
<span data-ttu-id="ed742-103">更新指定的 Azure 網站復原網路地圖。</span><span class="sxs-lookup"><span data-stu-id="ed742-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="ed742-104">語法</span><span class="sxs-lookup"><span data-stu-id="ed742-104">SYNTAX</span></span>

### <span data-ttu-id="ed742-105">ByNetworkObject (預設) </span><span class="sxs-lookup"><span data-stu-id="ed742-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed742-106">ById</span><span class="sxs-lookup"><span data-stu-id="ed742-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed742-107">描述</span><span class="sxs-lookup"><span data-stu-id="ed742-107">DESCRIPTION</span></span>
<span data-ttu-id="ed742-108">**Update-AzRecoveryServicesAsrNetworkMapping** Cmdlet 會更新指定的 Azure 網站復原網路地圖。</span><span class="sxs-lookup"><span data-stu-id="ed742-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="ed742-109">例子</span><span class="sxs-lookup"><span data-stu-id="ed742-109">EXAMPLES</span></span>

### <span data-ttu-id="ed742-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="ed742-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="ed742-111">使用指定的參數啟動更新網路地圖作業，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="ed742-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ed742-112">參數</span><span class="sxs-lookup"><span data-stu-id="ed742-112">PARAMETERS</span></span>

### <span data-ttu-id="ed742-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed742-113">-DefaultProfile</span></span>
<span data-ttu-id="ed742-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed742-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ed742-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed742-115">-InputObject</span></span>
<span data-ttu-id="ed742-116">輸入物件：指定對應至 ASR 網路對應以更新的 ASR 網路對應物件。</span><span class="sxs-lookup"><span data-stu-id="ed742-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed742-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="ed742-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="ed742-118">指定網路地圖的復原 Azure 網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed742-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed742-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="ed742-119">-RecoveryNetwork</span></span>
<span data-ttu-id="ed742-120">指定網路地圖的復原網路物件。</span><span class="sxs-lookup"><span data-stu-id="ed742-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed742-121">-確認</span><span class="sxs-lookup"><span data-stu-id="ed742-121">-Confirm</span></span>
<span data-ttu-id="ed742-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ed742-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed742-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed742-123">-WhatIf</span></span>
<span data-ttu-id="ed742-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed742-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed742-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed742-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed742-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed742-126">CommonParameters</span></span>
<span data-ttu-id="ed742-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ed742-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed742-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed742-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed742-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ed742-129">INPUTS</span></span>

### <span data-ttu-id="ed742-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="ed742-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="ed742-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ed742-131">OUTPUTS</span></span>

### <span data-ttu-id="ed742-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ed742-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ed742-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ed742-133">NOTES</span></span>

## <span data-ttu-id="ed742-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed742-134">RELATED LINKS</span></span>
