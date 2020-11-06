---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: af4dbdbb2741850cdb01eb88e321f80a4844919a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621168"
---
# <span data-ttu-id="cb1f6-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cb1f6-101">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="cb1f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb1f6-102">SYNOPSIS</span></span>
<span data-ttu-id="cb1f6-103">取得 Azure 網站復原複製受保護專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb1f6-103">Gets the properties of an Azure Site Recovery Replication Protected Items.</span></span>

## <span data-ttu-id="cb1f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb1f6-104">SYNTAX</span></span>

### <span data-ttu-id="cb1f6-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="cb1f6-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb1f6-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="cb1f6-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb1f6-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="cb1f6-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb1f6-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="cb1f6-108">ByProtectableItemObject</span></span>
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb1f6-109">說明</span><span class="sxs-lookup"><span data-stu-id="cb1f6-109">DESCRIPTION</span></span>
<span data-ttu-id="cb1f6-110">**AzRecoveryServicesAsrReplicationProtectedItem** Cmdlet 會從指定的 asr 保護容器中取得全部或指定的 asr 複製受保護專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="cb1f6-110">The **Get-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet gets the properties of all or the specified ASR replication protected item from the specified ASR protection container.</span></span>

## <span data-ttu-id="cb1f6-111">示例</span><span class="sxs-lookup"><span data-stu-id="cb1f6-111">EXAMPLES</span></span>

### <span data-ttu-id="cb1f6-112">範例1</span><span class="sxs-lookup"><span data-stu-id="cb1f6-112">Example 1</span></span>
```
PS C:\> $ReplicationProtectedItems = Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

<span data-ttu-id="cb1f6-113">在指定的 [ASR 保護] 容器中列出所有受禁止複製的專案。</span><span class="sxs-lookup"><span data-stu-id="cb1f6-113">Lists all replication protected items in the specified ASR protection container.</span></span>

## <span data-ttu-id="cb1f6-114">參數</span><span class="sxs-lookup"><span data-stu-id="cb1f6-114">PARAMETERS</span></span>

### <span data-ttu-id="cb1f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb1f6-115">-DefaultProfile</span></span>
<span data-ttu-id="cb1f6-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb1f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cb1f6-117">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cb1f6-117">-FriendlyName</span></span>
<span data-ttu-id="cb1f6-118">指定要取得的複製受保護專案的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="cb1f6-118">Specifies the friendly name of the replication protected item to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb1f6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb1f6-119">-Name</span></span>
<span data-ttu-id="cb1f6-120">指定要取得的複製受保護專案名稱。</span><span class="sxs-lookup"><span data-stu-id="cb1f6-120">Specifies the name of the replication protected item to get.</span></span>

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

### <span data-ttu-id="cb1f6-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="cb1f6-121">-ProtectableItem</span></span>
<span data-ttu-id="cb1f6-122">指定 ASR 可保護的專案物件。</span><span class="sxs-lookup"><span data-stu-id="cb1f6-122">Specifies an ASR protectable item object.</span></span> <span data-ttu-id="cb1f6-123">如果專案受到保護，則 Cmdlet 會取得與指定的 ASR 可保護專案相對應的 ASR 複製受保護專案。</span><span class="sxs-lookup"><span data-stu-id="cb1f6-123">The cmdlet gets the ASR replication protected item corresponding to the specified ASR protectable item if the item is protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb1f6-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cb1f6-124">-ProtectionContainer</span></span>
<span data-ttu-id="cb1f6-125">指定對應至 [複製受保護專案] 的 ASR 保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="cb1f6-125">Specifies the ASR protection container object of the ASR protection container corresponding to the replication protected item.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb1f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb1f6-126">CommonParameters</span></span>
<span data-ttu-id="cb1f6-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb1f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb1f6-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb1f6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb1f6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="cb1f6-129">INPUTS</span></span>

### <span data-ttu-id="cb1f6-130">RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cb1f6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

### <span data-ttu-id="cb1f6-131">RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="cb1f6-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="cb1f6-132">輸出</span><span class="sxs-lookup"><span data-stu-id="cb1f6-132">OUTPUTS</span></span>

### <span data-ttu-id="cb1f6-133">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cb1f6-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="cb1f6-134">筆記</span><span class="sxs-lookup"><span data-stu-id="cb1f6-134">NOTES</span></span>

## <span data-ttu-id="cb1f6-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb1f6-135">RELATED LINKS</span></span>

[<span data-ttu-id="cb1f6-136">新-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cb1f6-136">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="cb1f6-137">移除-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cb1f6-137">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="cb1f6-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cb1f6-138">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
