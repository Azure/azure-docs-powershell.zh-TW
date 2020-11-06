---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 96a30621bc545b635262fd7937e0e55739d0be7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456443"
---
# <span data-ttu-id="902a0-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="902a0-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="902a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="902a0-102">SYNOPSIS</span></span>
<span data-ttu-id="902a0-103">取得受複製受保護專案的可用復原點數。</span><span class="sxs-lookup"><span data-stu-id="902a0-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="902a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="902a0-104">SYNTAX</span></span>

### <span data-ttu-id="902a0-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="902a0-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [<CommonParameters>]
```

### <span data-ttu-id="902a0-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="902a0-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [<CommonParameters>]
```

## <span data-ttu-id="902a0-107">說明</span><span class="sxs-lookup"><span data-stu-id="902a0-107">DESCRIPTION</span></span>
<span data-ttu-id="902a0-108">**AzureRmRecoveryServicesAsrRecoveryPoint** Cmdlet 會取得受複製受保護專案的可用復原點數清單。</span><span class="sxs-lookup"><span data-stu-id="902a0-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="902a0-109">示例</span><span class="sxs-lookup"><span data-stu-id="902a0-109">EXAMPLES</span></span>

### <span data-ttu-id="902a0-110">範例1</span><span class="sxs-lookup"><span data-stu-id="902a0-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="902a0-111">取得指定的 ASR 複製受保護專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="902a0-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="902a0-112">參數</span><span class="sxs-lookup"><span data-stu-id="902a0-112">PARAMETERS</span></span>

### <span data-ttu-id="902a0-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="902a0-113">-Name</span></span>
<span data-ttu-id="902a0-114">指定要取得的復原點名稱。</span><span class="sxs-lookup"><span data-stu-id="902a0-114">Specifies the name of the recovery point to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="902a0-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="902a0-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="902a0-116">指定要取得可用復原點數清單的 Azure Site Recovery 複製受保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="902a0-116">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="902a0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="902a0-117">CommonParameters</span></span>
<span data-ttu-id="902a0-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="902a0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="902a0-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="902a0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="902a0-120">輸入</span><span class="sxs-lookup"><span data-stu-id="902a0-120">INPUTS</span></span>

### <span data-ttu-id="902a0-121">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="902a0-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="902a0-122">輸出</span><span class="sxs-lookup"><span data-stu-id="902a0-122">OUTPUTS</span></span>

### <span data-ttu-id="902a0-123">System.object. IEnumerable "1 [ASRRecoveryPoint，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="902a0-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="902a0-124">筆記</span><span class="sxs-lookup"><span data-stu-id="902a0-124">NOTES</span></span>

## <span data-ttu-id="902a0-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="902a0-125">RELATED LINKS</span></span>

[<span data-ttu-id="902a0-126">編輯-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="902a0-126">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="902a0-127">AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="902a0-127">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="902a0-128">新-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="902a0-128">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="902a0-129">移除-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="902a0-129">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="902a0-130">更新-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="902a0-130">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
