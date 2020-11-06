---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 90b615edefe860e084de0040a13c1ba5a1ff39ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447705"
---
# <span data-ttu-id="c4f0e-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c4f0e-101">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="c4f0e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="c4f0e-103">取得 Azure 網站復原複製受保護專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="c4f0e-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4f0e-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4f0e-104">SYNTAX</span></span>

### <span data-ttu-id="c4f0e-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="c4f0e-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4f0e-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c4f0e-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4f0e-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c4f0e-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4f0e-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="c4f0e-108">ByProtectableItemObject</span></span>
```
Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4f0e-109">說明</span><span class="sxs-lookup"><span data-stu-id="c4f0e-109">DESCRIPTION</span></span>
<span data-ttu-id="c4f0e-110">**AzureRmRecoveryServicesAsrReplicationProtectedItem** Cmdlet 會從指定的 asr 保護容器中取得全部或指定的 asr 複製受保護專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="c4f0e-110">The **Get-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="c4f0e-111">示例</span><span class="sxs-lookup"><span data-stu-id="c4f0e-111">EXAMPLES</span></span>

### <span data-ttu-id="c4f0e-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c4f0e-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="c4f0e-113">在指定的 [ASR 保護] 容器中列出所有受禁止複製的專案。</span><span class="sxs-lookup"><span data-stu-id="c4f0e-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="c4f0e-114">參數</span><span class="sxs-lookup"><span data-stu-id="c4f0e-114">PARAMETERS</span></span>

### <span data-ttu-id="c4f0e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4f0e-115">-DefaultProfile</span></span>
<span data-ttu-id="c4f0e-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4f0e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f0e-117">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c4f0e-117">-FriendlyName</span></span>
<span data-ttu-id="c4f0e-118">指定要取得的複製受保護專案的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="c4f0e-118">Specifies the friendly name of the replication protected item to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4f0e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c4f0e-119">-Name</span></span>
<span data-ttu-id="c4f0e-120">指定要取得的複製受保護專案名稱。</span><span class="sxs-lookup"><span data-stu-id="c4f0e-120">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="c4f0e-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c4f0e-121">-ProtectableItem</span></span>
<span data-ttu-id="c4f0e-122">指定 ASR 可保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="c4f0e-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="c4f0e-123">如果專案受到保護，則 Cmdlet 會取得與指定的 ASR 可保護專案相對應的 ASR 複製受保護專案。</span><span class="sxs-lookup"><span data-stu-id="c4f0e-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4f0e-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c4f0e-124">-ProtectionContainer</span></span>
<span data-ttu-id="c4f0e-125">指定對應至 [複製受保護專案] 的 ASR 保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="c4f0e-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4f0e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4f0e-126">CommonParameters</span></span>
<span data-ttu-id="c4f0e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4f0e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4f0e-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c4f0e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4f0e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c4f0e-129">INPUTS</span></span>

### <span data-ttu-id="c4f0e-130">RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c4f0e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>
<span data-ttu-id="c4f0e-131">RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c4f0e-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="c4f0e-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c4f0e-132">OUTPUTS</span></span>

### <span data-ttu-id="c4f0e-133">System.object. IEnumerable "1 [ASRReplicationProtectedItem，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="c4f0e-133">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c4f0e-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c4f0e-134">NOTES</span></span>

## <span data-ttu-id="c4f0e-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4f0e-135">RELATED LINKS</span></span>

[<span data-ttu-id="c4f0e-136">新-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c4f0e-136">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="c4f0e-137">移除-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c4f0e-137">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="c4f0e-138">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c4f0e-138">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
