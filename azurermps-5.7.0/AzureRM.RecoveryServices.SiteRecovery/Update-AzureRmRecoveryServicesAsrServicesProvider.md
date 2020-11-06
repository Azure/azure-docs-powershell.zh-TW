---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 823ad4b0f7eff8f80fea012bdef4b3c2662d55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446051"
---
# <span data-ttu-id="67c8d-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="67c8d-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="67c8d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="67c8d-103">更新) 從 Azure Site Recovery 服務提供者收到的資訊， (重新整理伺服器。</span><span class="sxs-lookup"><span data-stu-id="67c8d-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67c8d-104">句法</span><span class="sxs-lookup"><span data-stu-id="67c8d-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67c8d-105">說明</span><span class="sxs-lookup"><span data-stu-id="67c8d-105">DESCRIPTION</span></span>
<span data-ttu-id="67c8d-106">**AzureRmRecoveryServicesAsrServicesProvider** Cmdlet 會更新從 Azure Site Recovery 服務提供者收到的資訊。</span><span class="sxs-lookup"><span data-stu-id="67c8d-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="67c8d-107">您可以使用這個 Cmdlet 觸發從復原服務提供者收到的資訊重新整理。</span><span class="sxs-lookup"><span data-stu-id="67c8d-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="67c8d-108">示例</span><span class="sxs-lookup"><span data-stu-id="67c8d-108">EXAMPLES</span></span>

### <span data-ttu-id="67c8d-109">範例1</span><span class="sxs-lookup"><span data-stu-id="67c8d-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="67c8d-110">開始從指定的 ASR 服務提供者中重新整理資訊的作業，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="67c8d-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="67c8d-111">參數</span><span class="sxs-lookup"><span data-stu-id="67c8d-111">PARAMETERS</span></span>

### <span data-ttu-id="67c8d-112">-確認</span><span class="sxs-lookup"><span data-stu-id="67c8d-112">-Confirm</span></span>
<span data-ttu-id="67c8d-113">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="67c8d-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67c8d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c8d-114">-DefaultProfile</span></span>
<span data-ttu-id="67c8d-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67c8d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="67c8d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67c8d-116">-InputObject</span></span>
<span data-ttu-id="67c8d-117">指定 ASR 服務提供者物件，該物件會識別要更新之資訊的伺服器 (進行刷新。 ) </span><span class="sxs-lookup"><span data-stu-id="67c8d-117">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="67c8d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67c8d-118">-WhatIf</span></span>
<span data-ttu-id="67c8d-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67c8d-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67c8d-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67c8d-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67c8d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c8d-121">CommonParameters</span></span>
<span data-ttu-id="67c8d-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67c8d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c8d-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67c8d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c8d-124">輸入</span><span class="sxs-lookup"><span data-stu-id="67c8d-124">INPUTS</span></span>

### <span data-ttu-id="67c8d-125">RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="67c8d-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="67c8d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="67c8d-126">OUTPUTS</span></span>

### <span data-ttu-id="67c8d-127">System.object</span><span class="sxs-lookup"><span data-stu-id="67c8d-127">System.Object</span></span>

## <span data-ttu-id="67c8d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="67c8d-128">NOTES</span></span>

## <span data-ttu-id="67c8d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="67c8d-129">RELATED LINKS</span></span>

[<span data-ttu-id="67c8d-130">AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="67c8d-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="67c8d-131">移除-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="67c8d-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
