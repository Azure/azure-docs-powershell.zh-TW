---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: e9559993e122e5b713228630b3b783b1f0e6a981
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915914"
---
# <span data-ttu-id="e8ba8-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="e8ba8-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="e8ba8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e8ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ba8-103">獲得 ASR 複寫原則。</span><span class="sxs-lookup"><span data-stu-id="e8ba8-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="e8ba8-104">語法</span><span class="sxs-lookup"><span data-stu-id="e8ba8-104">SYNTAX</span></span>

### <span data-ttu-id="e8ba8-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="e8ba8-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ba8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e8ba8-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ba8-107">By有LylyName</span><span class="sxs-lookup"><span data-stu-id="e8ba8-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8ba8-108">描述</span><span class="sxs-lookup"><span data-stu-id="e8ba8-108">DESCRIPTION</span></span>
<span data-ttu-id="e8ba8-109">**Get-AzRecoveryServicesAsrPolicy** Cmdlet 會取得已配置的 Azure 網站復原複寫策略清單，或按名稱的特定複寫策略。</span><span class="sxs-lookup"><span data-stu-id="e8ba8-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="e8ba8-110">例子</span><span class="sxs-lookup"><span data-stu-id="e8ba8-110">EXAMPLES</span></span>

### <span data-ttu-id="e8ba8-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="e8ba8-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="e8ba8-112">會返回複寫原則清單</span><span class="sxs-lookup"><span data-stu-id="e8ba8-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="e8ba8-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="e8ba8-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="e8ba8-114">會以名稱返回複寫原則。</span><span class="sxs-lookup"><span data-stu-id="e8ba8-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="e8ba8-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="e8ba8-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="e8ba8-116">會以指定的好用名稱來返回複寫原則。</span><span class="sxs-lookup"><span data-stu-id="e8ba8-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="e8ba8-117">參數</span><span class="sxs-lookup"><span data-stu-id="e8ba8-117">PARAMETERS</span></span>

### <span data-ttu-id="e8ba8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ba8-118">-DefaultProfile</span></span>
<span data-ttu-id="e8ba8-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8ba8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e8ba8-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e8ba8-120">-FriendlyName</span></span>
<span data-ttu-id="e8ba8-121">指定 ASR 複寫原則的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="e8ba8-121">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba8-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8ba8-122">-Name</span></span>
<span data-ttu-id="e8ba8-123">指定 ASR 複寫原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8ba8-123">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ba8-124">CommonParameters</span></span>
<span data-ttu-id="e8ba8-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e8ba8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ba8-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8ba8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ba8-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e8ba8-127">INPUTS</span></span>

### <span data-ttu-id="e8ba8-128">沒有</span><span class="sxs-lookup"><span data-stu-id="e8ba8-128">None</span></span>

## <span data-ttu-id="e8ba8-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e8ba8-129">OUTPUTS</span></span>

### <span data-ttu-id="e8ba8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="e8ba8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="e8ba8-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e8ba8-131">NOTES</span></span>

## <span data-ttu-id="e8ba8-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8ba8-132">RELATED LINKS</span></span>

[<span data-ttu-id="e8ba8-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="e8ba8-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="e8ba8-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="e8ba8-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
