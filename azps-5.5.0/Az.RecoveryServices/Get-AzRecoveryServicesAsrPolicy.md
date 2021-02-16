---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a7cd359714be965c232019310ac2f2abfe0fe233
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140043"
---
# <span data-ttu-id="d9434-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d9434-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="d9434-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9434-102">SYNOPSIS</span></span>
<span data-ttu-id="d9434-103">取得 ASR 複製原則。</span><span class="sxs-lookup"><span data-stu-id="d9434-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="d9434-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9434-104">SYNTAX</span></span>

### <span data-ttu-id="d9434-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="d9434-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9434-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d9434-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9434-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d9434-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9434-108">說明</span><span class="sxs-lookup"><span data-stu-id="d9434-108">DESCRIPTION</span></span>
<span data-ttu-id="d9434-109">AzRecoveryServicesAsrPolicy Cmdlet 會透過名稱 **取得** 已設定的 Azure 網站復原複製原則或特定複製原則的清單。</span><span class="sxs-lookup"><span data-stu-id="d9434-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="d9434-110">示例</span><span class="sxs-lookup"><span data-stu-id="d9434-110">EXAMPLES</span></span>

### <span data-ttu-id="d9434-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d9434-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="d9434-112">傳回復制原則的清單</span><span class="sxs-lookup"><span data-stu-id="d9434-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="d9434-113">範例2</span><span class="sxs-lookup"><span data-stu-id="d9434-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="d9434-114">傳回名稱為的複製原則。</span><span class="sxs-lookup"><span data-stu-id="d9434-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="d9434-115">範例3</span><span class="sxs-lookup"><span data-stu-id="d9434-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="d9434-116">傳回具有指定易記名稱的複製原則。</span><span class="sxs-lookup"><span data-stu-id="d9434-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="d9434-117">參數</span><span class="sxs-lookup"><span data-stu-id="d9434-117">PARAMETERS</span></span>

### <span data-ttu-id="d9434-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9434-118">-DefaultProfile</span></span>
<span data-ttu-id="d9434-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9434-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d9434-120">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d9434-120">-FriendlyName</span></span>
<span data-ttu-id="d9434-121">指定 ASR 複製原則的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="d9434-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="d9434-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d9434-122">-Name</span></span>
<span data-ttu-id="d9434-123">指定 ASR 複製原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9434-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="d9434-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9434-124">CommonParameters</span></span>
<span data-ttu-id="d9434-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9434-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9434-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d9434-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9434-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d9434-127">INPUTS</span></span>

### <span data-ttu-id="d9434-128">所有</span><span class="sxs-lookup"><span data-stu-id="d9434-128">None</span></span>

## <span data-ttu-id="d9434-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d9434-129">OUTPUTS</span></span>

### <span data-ttu-id="d9434-130">RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="d9434-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="d9434-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d9434-131">NOTES</span></span>

## <span data-ttu-id="d9434-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9434-132">RELATED LINKS</span></span>

[<span data-ttu-id="d9434-133">新-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d9434-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="d9434-134">移除-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d9434-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
