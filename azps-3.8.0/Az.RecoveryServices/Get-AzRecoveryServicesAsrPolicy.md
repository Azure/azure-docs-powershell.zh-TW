---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a7cd359714be965c232019310ac2f2abfe0fe233
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956558"
---
# <span data-ttu-id="9ac6a-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="9ac6a-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="9ac6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ac6a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac6a-103">取得 ASR 複製原則。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="9ac6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ac6a-104">SYNTAX</span></span>

### <span data-ttu-id="9ac6a-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="9ac6a-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ac6a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9ac6a-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ac6a-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9ac6a-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ac6a-108">說明</span><span class="sxs-lookup"><span data-stu-id="9ac6a-108">DESCRIPTION</span></span>
<span data-ttu-id="9ac6a-109">AzRecoveryServicesAsrPolicy Cmdlet 會透過名稱 **取得** 已設定的 Azure 網站復原複製原則或特定複製原則的清單。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="9ac6a-110">示例</span><span class="sxs-lookup"><span data-stu-id="9ac6a-110">EXAMPLES</span></span>

### <span data-ttu-id="9ac6a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9ac6a-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="9ac6a-112">傳回復制原則的清單</span><span class="sxs-lookup"><span data-stu-id="9ac6a-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="9ac6a-113">範例2</span><span class="sxs-lookup"><span data-stu-id="9ac6a-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="9ac6a-114">傳回名稱為的複製原則。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="9ac6a-115">範例3</span><span class="sxs-lookup"><span data-stu-id="9ac6a-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="9ac6a-116">傳回具有指定易記名稱的複製原則。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="9ac6a-117">參數</span><span class="sxs-lookup"><span data-stu-id="9ac6a-117">PARAMETERS</span></span>

### <span data-ttu-id="9ac6a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac6a-118">-DefaultProfile</span></span>
<span data-ttu-id="9ac6a-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9ac6a-120">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9ac6a-120">-FriendlyName</span></span>
<span data-ttu-id="9ac6a-121">指定 ASR 複製原則的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="9ac6a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9ac6a-122">-Name</span></span>
<span data-ttu-id="9ac6a-123">指定 ASR 複製原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="9ac6a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac6a-124">CommonParameters</span></span>
<span data-ttu-id="9ac6a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac6a-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9ac6a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac6a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9ac6a-127">INPUTS</span></span>

### <span data-ttu-id="9ac6a-128">所有</span><span class="sxs-lookup"><span data-stu-id="9ac6a-128">None</span></span>

## <span data-ttu-id="9ac6a-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9ac6a-129">OUTPUTS</span></span>

### <span data-ttu-id="9ac6a-130">RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="9ac6a-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="9ac6a-131">筆記</span><span class="sxs-lookup"><span data-stu-id="9ac6a-131">NOTES</span></span>

## <span data-ttu-id="9ac6a-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ac6a-132">RELATED LINKS</span></span>

[<span data-ttu-id="9ac6a-133">新-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="9ac6a-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="9ac6a-134">移除-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="9ac6a-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
