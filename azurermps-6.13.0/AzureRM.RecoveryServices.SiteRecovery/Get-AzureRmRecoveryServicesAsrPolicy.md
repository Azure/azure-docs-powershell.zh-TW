---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: aeceb76fe2f1faf6e7e1f2ddf09ee9262370e8ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451083"
---
# <span data-ttu-id="c9459-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="c9459-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="c9459-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9459-102">SYNOPSIS</span></span>
<span data-ttu-id="c9459-103">取得 ASR 複製原則。</span><span class="sxs-lookup"><span data-stu-id="c9459-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9459-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9459-104">SYNTAX</span></span>

### <span data-ttu-id="c9459-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="c9459-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9459-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c9459-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9459-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c9459-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9459-108">說明</span><span class="sxs-lookup"><span data-stu-id="c9459-108">DESCRIPTION</span></span>
<span data-ttu-id="c9459-109">AzureRmRecoveryServicesAsrPolicy Cmdlet 會透過名稱 **取得** 已設定的 Azure 網站復原複製原則或特定複製原則的清單。</span><span class="sxs-lookup"><span data-stu-id="c9459-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="c9459-110">示例</span><span class="sxs-lookup"><span data-stu-id="c9459-110">EXAMPLES</span></span>

### <span data-ttu-id="c9459-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c9459-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy
```

<span data-ttu-id="c9459-112">Retuns 複製原則清單</span><span class="sxs-lookup"><span data-stu-id="c9459-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="c9459-113">範例2</span><span class="sxs-lookup"><span data-stu-id="c9459-113">Example 2</span></span>
```
PS C:\>  Get-AzureRmRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="c9459-114">Retuns 包含名稱的複製原則。</span><span class="sxs-lookup"><span data-stu-id="c9459-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="c9459-115">範例3</span><span class="sxs-lookup"><span data-stu-id="c9459-115">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="c9459-116">傳回具有指定易記名稱的複製原則。</span><span class="sxs-lookup"><span data-stu-id="c9459-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="c9459-117">參數</span><span class="sxs-lookup"><span data-stu-id="c9459-117">PARAMETERS</span></span>

### <span data-ttu-id="c9459-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9459-118">-DefaultProfile</span></span>
<span data-ttu-id="c9459-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9459-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c9459-120">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c9459-120">-FriendlyName</span></span>
<span data-ttu-id="c9459-121">指定 ASR 複製原則的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="c9459-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="c9459-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9459-122">-Name</span></span>
<span data-ttu-id="c9459-123">指定 ASR 複製原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9459-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="c9459-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9459-124">CommonParameters</span></span>
<span data-ttu-id="c9459-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9459-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9459-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c9459-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9459-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c9459-127">INPUTS</span></span>

### <span data-ttu-id="c9459-128">所有</span><span class="sxs-lookup"><span data-stu-id="c9459-128">None</span></span>

## <span data-ttu-id="c9459-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c9459-129">OUTPUTS</span></span>

### <span data-ttu-id="c9459-130">System.object. IEnumerable "1 [ASRPolicy，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="c9459-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c9459-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c9459-131">NOTES</span></span>

## <span data-ttu-id="c9459-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9459-132">RELATED LINKS</span></span>

[<span data-ttu-id="c9459-133">新-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="c9459-133">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="c9459-134">移除-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="c9459-134">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
