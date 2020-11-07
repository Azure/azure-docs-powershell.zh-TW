---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: c893d256351473aa1d840cf1a7e62a960300bdf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623741"
---
# <span data-ttu-id="1b57d-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1b57d-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="1b57d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b57d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b57d-103">取得 Azure Site Recovery 保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="1b57d-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b57d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b57d-104">SYNTAX</span></span>

### <span data-ttu-id="1b57d-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="1b57d-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b57d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="1b57d-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b57d-107">說明</span><span class="sxs-lookup"><span data-stu-id="1b57d-107">DESCRIPTION</span></span>
<span data-ttu-id="1b57d-108">**AzureRmRecoveryServicesAsrProtectionContainerMapping** Cmdlet 會針對指定的 ASR 保護容器，取得保存庫中針對複製原則對應 (關聯性) 的保護容器資訊。</span><span class="sxs-lookup"><span data-stu-id="1b57d-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="1b57d-109">示例</span><span class="sxs-lookup"><span data-stu-id="1b57d-109">EXAMPLES</span></span>

### <span data-ttu-id="1b57d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1b57d-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="1b57d-111">容器的保護容器對應清單。</span><span class="sxs-lookup"><span data-stu-id="1b57d-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="1b57d-112">範例2</span><span class="sxs-lookup"><span data-stu-id="1b57d-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

Name                                  : pcmmapping
ID                                    : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replica
                                        tionProtectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectionContainerMappings/pcmmapping
Health                                : Normal
HealthErrorDetails                    : {}
PolicyFriendlyName                    : V2aTestPolicy
PolicyId                              : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationPolicies/V2aTestPolicy
SourceFabricFriendlyName              : V2A-W2K12-400
SourceProtectionContainerFriendlyName : V2A-W2K12-400
State                                 : Paired
TargetFabricFriendlyName              : Microsoft Azure
TargetProtectionContainerFriendlyName : Microsoft Azure
TargetProtectionContainerId           : Microsoft Azure
```

<span data-ttu-id="1b57d-113">取得指定保護容器的所有保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="1b57d-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="1b57d-114">參數</span><span class="sxs-lookup"><span data-stu-id="1b57d-114">PARAMETERS</span></span>

### <span data-ttu-id="1b57d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b57d-115">-DefaultProfile</span></span>
<span data-ttu-id="1b57d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b57d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1b57d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="1b57d-117">-Name</span></span>
<span data-ttu-id="1b57d-118">指定要取得之保護容器對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b57d-118">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="1b57d-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1b57d-119">-ProtectionContainer</span></span>
<span data-ttu-id="1b57d-120">取得與指定的 ASR 保護容器物件相對應的保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="1b57d-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b57d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b57d-121">CommonParameters</span></span>
<span data-ttu-id="1b57d-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b57d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b57d-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b57d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b57d-124">輸入</span><span class="sxs-lookup"><span data-stu-id="1b57d-124">INPUTS</span></span>

### <span data-ttu-id="1b57d-125">RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1b57d-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="1b57d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="1b57d-126">OUTPUTS</span></span>

### <span data-ttu-id="1b57d-127">System.object. IEnumerable "1 [ASRProtectionContainerMapping，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="1b57d-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1b57d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="1b57d-128">NOTES</span></span>

## <span data-ttu-id="1b57d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b57d-129">RELATED LINKS</span></span>

[<span data-ttu-id="1b57d-130">新-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1b57d-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="1b57d-131">移除-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1b57d-131">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
