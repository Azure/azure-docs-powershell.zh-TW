---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 27f1f0f03da7a4ad912be28a2de85bf6e7cf58f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917657"
---
# <span data-ttu-id="6cc6d-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6cc6d-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="6cc6d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6cc6d-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc6d-103">為複本受保護的專案獲得可用的修復點。</span><span class="sxs-lookup"><span data-stu-id="6cc6d-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="6cc6d-104">語法</span><span class="sxs-lookup"><span data-stu-id="6cc6d-104">SYNTAX</span></span>

### <span data-ttu-id="6cc6d-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="6cc6d-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cc6d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="6cc6d-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cc6d-107">描述</span><span class="sxs-lookup"><span data-stu-id="6cc6d-107">DESCRIPTION</span></span>
<span data-ttu-id="6cc6d-108">**Get-AzRecoveryServicesrRecoveryPoint** Cmdlet 會取得複本受保護專案的可用修復點清單。</span><span class="sxs-lookup"><span data-stu-id="6cc6d-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="6cc6d-109">例子</span><span class="sxs-lookup"><span data-stu-id="6cc6d-109">EXAMPLES</span></span>

### <span data-ttu-id="6cc6d-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="6cc6d-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="6cc6d-111">為指定的 ASR 複本受保護專案獲得復原點。</span><span class="sxs-lookup"><span data-stu-id="6cc6d-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="6cc6d-112">參數</span><span class="sxs-lookup"><span data-stu-id="6cc6d-112">PARAMETERS</span></span>

### <span data-ttu-id="6cc6d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc6d-113">-DefaultProfile</span></span>
<span data-ttu-id="6cc6d-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6cc6d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6cc6d-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="6cc6d-115">-Name</span></span>
<span data-ttu-id="6cc6d-116">指定要取得復原點的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cc6d-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="6cc6d-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6cc6d-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6cc6d-118">指定要取得可用修復點清單的 Azure 網站復原複本受保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="6cc6d-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="6cc6d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc6d-119">CommonParameters</span></span>
<span data-ttu-id="6cc6d-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6cc6d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc6d-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cc6d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc6d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="6cc6d-122">INPUTS</span></span>

### <span data-ttu-id="6cc6d-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6cc6d-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="6cc6d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="6cc6d-124">OUTPUTS</span></span>

### <span data-ttu-id="6cc6d-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6cc6d-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="6cc6d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="6cc6d-126">NOTES</span></span>

## <span data-ttu-id="6cc6d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="6cc6d-127">RELATED LINKS</span></span>

[<span data-ttu-id="6cc6d-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6cc6d-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6cc6d-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6cc6d-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6cc6d-130">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6cc6d-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6cc6d-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6cc6d-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6cc6d-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6cc6d-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
