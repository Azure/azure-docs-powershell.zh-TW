---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276755"
---
# <span data-ttu-id="a3199-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a3199-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="a3199-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3199-102">SYNOPSIS</span></span>
<span data-ttu-id="a3199-103">更新指定的 azure site recovery 網路對應。</span><span class="sxs-lookup"><span data-stu-id="a3199-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="a3199-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3199-104">SYNTAX</span></span>

### <span data-ttu-id="a3199-105">ByNetworkObject (預設) </span><span class="sxs-lookup"><span data-stu-id="a3199-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3199-106">ById</span><span class="sxs-lookup"><span data-stu-id="a3199-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3199-107">說明</span><span class="sxs-lookup"><span data-stu-id="a3199-107">DESCRIPTION</span></span>
<span data-ttu-id="a3199-108">**AzRecoveryServicesAsrNetworkMapping** Cmdlet 會更新指定的 Azure Site Recovery 網路對應。</span><span class="sxs-lookup"><span data-stu-id="a3199-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="a3199-109">示例</span><span class="sxs-lookup"><span data-stu-id="a3199-109">EXAMPLES</span></span>

### <span data-ttu-id="a3199-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a3199-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="a3199-111">使用指定的參數啟動更新網路對應作業，並傳回用來追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="a3199-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a3199-112">參數</span><span class="sxs-lookup"><span data-stu-id="a3199-112">PARAMETERS</span></span>

### <span data-ttu-id="a3199-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3199-113">-DefaultProfile</span></span>
<span data-ttu-id="a3199-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3199-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a3199-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3199-115">-InputObject</span></span>
<span data-ttu-id="a3199-116">輸入物件：指定要更新之 ASR 網路對應的 ASR 網路對應物件。</span><span class="sxs-lookup"><span data-stu-id="a3199-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="a3199-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="a3199-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="a3199-118">指定網路對應的 [恢復 azure 網路識別碼]。</span><span class="sxs-lookup"><span data-stu-id="a3199-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="a3199-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="a3199-119">-RecoveryNetwork</span></span>
<span data-ttu-id="a3199-120">指定網路對應的恢復網路物件。</span><span class="sxs-lookup"><span data-stu-id="a3199-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="a3199-121">-確認</span><span class="sxs-lookup"><span data-stu-id="a3199-121">-Confirm</span></span>
<span data-ttu-id="a3199-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a3199-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3199-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3199-123">-WhatIf</span></span>
<span data-ttu-id="a3199-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3199-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3199-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3199-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3199-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3199-126">CommonParameters</span></span>
<span data-ttu-id="a3199-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3199-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3199-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a3199-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3199-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a3199-129">INPUTS</span></span>

### <span data-ttu-id="a3199-130">RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a3199-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="a3199-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a3199-131">OUTPUTS</span></span>

### <span data-ttu-id="a3199-132">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a3199-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a3199-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a3199-133">NOTES</span></span>

## <span data-ttu-id="a3199-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3199-134">RELATED LINKS</span></span>
