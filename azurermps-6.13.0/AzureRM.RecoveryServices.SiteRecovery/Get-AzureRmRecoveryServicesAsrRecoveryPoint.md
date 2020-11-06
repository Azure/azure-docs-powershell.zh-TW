---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 21a01ae07c383484a6ec8e17d9b09a93671bfbe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447282"
---
# <span data-ttu-id="b2ad8-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b2ad8-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="b2ad8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="b2ad8-103">取得受複製受保護專案的可用復原點數。</span><span class="sxs-lookup"><span data-stu-id="b2ad8-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2ad8-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2ad8-104">SYNTAX</span></span>

### <span data-ttu-id="b2ad8-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="b2ad8-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2ad8-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="b2ad8-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2ad8-107">說明</span><span class="sxs-lookup"><span data-stu-id="b2ad8-107">DESCRIPTION</span></span>
<span data-ttu-id="b2ad8-108">**AzureRmRecoveryServicesAsrRecoveryPoint** Cmdlet 會取得受複製受保護專案的可用復原點數清單。</span><span class="sxs-lookup"><span data-stu-id="b2ad8-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="b2ad8-109">示例</span><span class="sxs-lookup"><span data-stu-id="b2ad8-109">EXAMPLES</span></span>

### <span data-ttu-id="b2ad8-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b2ad8-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="b2ad8-111">取得指定的 ASR 複製受保護專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="b2ad8-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="b2ad8-112">參數</span><span class="sxs-lookup"><span data-stu-id="b2ad8-112">PARAMETERS</span></span>

### <span data-ttu-id="b2ad8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2ad8-113">-DefaultProfile</span></span>
<span data-ttu-id="b2ad8-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b2ad8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b2ad8-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2ad8-115">-Name</span></span>
<span data-ttu-id="b2ad8-116">指定要取得的復原點名稱。</span><span class="sxs-lookup"><span data-stu-id="b2ad8-116">Specifies the name of the recovery point to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2ad8-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b2ad8-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b2ad8-118">指定要取得可用復原點數清單的 Azure Site Recovery 複製受保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="b2ad8-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ad8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2ad8-119">CommonParameters</span></span>
<span data-ttu-id="b2ad8-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2ad8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2ad8-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b2ad8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2ad8-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b2ad8-122">INPUTS</span></span>

### <span data-ttu-id="b2ad8-123">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b2ad8-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="b2ad8-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b2ad8-124">OUTPUTS</span></span>

### <span data-ttu-id="b2ad8-125">System.object. IEnumerable "1 [ASRRecoveryPoint，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="b2ad8-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b2ad8-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b2ad8-126">NOTES</span></span>

## <span data-ttu-id="b2ad8-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2ad8-127">RELATED LINKS</span></span>

[<span data-ttu-id="b2ad8-128">編輯-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2ad8-128">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b2ad8-129">AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2ad8-129">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b2ad8-130">新-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2ad8-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b2ad8-131">移除-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2ad8-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b2ad8-132">更新-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2ad8-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
