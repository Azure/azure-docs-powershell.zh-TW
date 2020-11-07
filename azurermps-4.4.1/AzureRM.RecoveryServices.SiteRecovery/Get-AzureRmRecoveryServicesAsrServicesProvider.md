---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 1d6199042cec106d81ba91ccb7ccb854741d319d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625106"
---
# <span data-ttu-id="673dd-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="673dd-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="673dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="673dd-102">SYNOPSIS</span></span>
<span data-ttu-id="673dd-103">取得已登錄至 [恢復服務] 保存庫的 ASR 恢復服務提供者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="673dd-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="673dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="673dd-104">SYNTAX</span></span>

### <span data-ttu-id="673dd-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="673dd-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="673dd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="673dd-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="673dd-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="673dd-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric> [<CommonParameters>]
```

## <span data-ttu-id="673dd-108">說明</span><span class="sxs-lookup"><span data-stu-id="673dd-108">DESCRIPTION</span></span>
<span data-ttu-id="673dd-109">**AzureRmRecoveryServicesAsrServicesProvider** Cmdlet 會取得保存庫中 Azure 網站恢復提供者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="673dd-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="673dd-110">示例</span><span class="sxs-lookup"><span data-stu-id="673dd-110">EXAMPLES</span></span>

### <span data-ttu-id="673dd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="673dd-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="673dd-112">列出已登錄至 [恢復服務] 保存庫（對應至指定結構）的所有 ASR 複製服務提供者。</span><span class="sxs-lookup"><span data-stu-id="673dd-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="673dd-113">參數</span><span class="sxs-lookup"><span data-stu-id="673dd-113">PARAMETERS</span></span>

### <span data-ttu-id="673dd-114">-結構</span><span class="sxs-lookup"><span data-stu-id="673dd-114">-Fabric</span></span>
<span data-ttu-id="673dd-115">指定 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="673dd-115">Specifies the ASR fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="673dd-116">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="673dd-116">-FriendlyName</span></span>
<span data-ttu-id="673dd-117">指定 ASR 恢復服務提供者的易記名稱，以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="673dd-117">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="673dd-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="673dd-118">-Name</span></span>
<span data-ttu-id="673dd-119">指定要取得詳細資料之 ASR 恢復服務提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="673dd-119">Specifies the name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="673dd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="673dd-120">CommonParameters</span></span>
<span data-ttu-id="673dd-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="673dd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="673dd-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="673dd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="673dd-123">輸入</span><span class="sxs-lookup"><span data-stu-id="673dd-123">INPUTS</span></span>

### <span data-ttu-id="673dd-124">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="673dd-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="673dd-125">輸出</span><span class="sxs-lookup"><span data-stu-id="673dd-125">OUTPUTS</span></span>

### <span data-ttu-id="673dd-126">System.object. IEnumerable "1 [ASRRecoveryServicesProvider，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="673dd-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="673dd-127">筆記</span><span class="sxs-lookup"><span data-stu-id="673dd-127">NOTES</span></span>

## <span data-ttu-id="673dd-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="673dd-128">RELATED LINKS</span></span>

[<span data-ttu-id="673dd-129">移除-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="673dd-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="673dd-130">更新-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="673dd-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
