---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 67e38be81ddce808151824ee307f27dd758768ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956551"
---
# <span data-ttu-id="2b1a9-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2b1a9-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="2b1a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b1a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2b1a9-103">取得受複製受保護專案的可用復原點數。</span><span class="sxs-lookup"><span data-stu-id="2b1a9-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="2b1a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b1a9-104">SYNTAX</span></span>

### <span data-ttu-id="2b1a9-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="2b1a9-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b1a9-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="2b1a9-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b1a9-107">說明</span><span class="sxs-lookup"><span data-stu-id="2b1a9-107">DESCRIPTION</span></span>
<span data-ttu-id="2b1a9-108">**AzRecoveryServicesAsrRecoveryPoint** Cmdlet 會取得受複製受保護專案的可用復原點數清單。</span><span class="sxs-lookup"><span data-stu-id="2b1a9-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="2b1a9-109">示例</span><span class="sxs-lookup"><span data-stu-id="2b1a9-109">EXAMPLES</span></span>

### <span data-ttu-id="2b1a9-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2b1a9-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="2b1a9-111">取得指定的 ASR 複製受保護專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="2b1a9-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="2b1a9-112">參數</span><span class="sxs-lookup"><span data-stu-id="2b1a9-112">PARAMETERS</span></span>

### <span data-ttu-id="2b1a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b1a9-113">-DefaultProfile</span></span>
<span data-ttu-id="2b1a9-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b1a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2b1a9-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b1a9-115">-Name</span></span>
<span data-ttu-id="2b1a9-116">指定要取得的復原點名稱。</span><span class="sxs-lookup"><span data-stu-id="2b1a9-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="2b1a9-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2b1a9-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="2b1a9-118">指定要取得可用復原點數清單的 Azure Site Recovery 複製受保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="2b1a9-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="2b1a9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b1a9-119">CommonParameters</span></span>
<span data-ttu-id="2b1a9-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b1a9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b1a9-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2b1a9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b1a9-122">輸入</span><span class="sxs-lookup"><span data-stu-id="2b1a9-122">INPUTS</span></span>

### <span data-ttu-id="2b1a9-123">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2b1a9-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="2b1a9-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2b1a9-124">OUTPUTS</span></span>

### <span data-ttu-id="2b1a9-125">RecoveryServices. SiteRecovery. ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2b1a9-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="2b1a9-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2b1a9-126">NOTES</span></span>

## <span data-ttu-id="2b1a9-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b1a9-127">RELATED LINKS</span></span>

[<span data-ttu-id="2b1a9-128">編輯-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2b1a9-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2b1a9-129">AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2b1a9-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2b1a9-130">新-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2b1a9-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2b1a9-131">移除-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2b1a9-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2b1a9-132">更新-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2b1a9-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)