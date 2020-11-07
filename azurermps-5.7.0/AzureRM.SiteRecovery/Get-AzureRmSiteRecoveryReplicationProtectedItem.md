---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 99196F44-F1DB-4219-91C0-3056624ADE5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 210b8ca6d8165049edc190e24e4a435046e1461e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625426"
---
# <span data-ttu-id="32f28-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="32f28-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="32f28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32f28-102">SYNOPSIS</span></span>
<span data-ttu-id="32f28-103">取得 Azure 網站復原受保護專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="32f28-103">Gets the properties of Azure Site Recovery Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32f28-104">句法</span><span class="sxs-lookup"><span data-stu-id="32f28-104">SYNTAX</span></span>

### <span data-ttu-id="32f28-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="32f28-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32f28-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="32f28-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32f28-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="32f28-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32f28-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="32f28-108">ByProtectableItemObject</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32f28-109">說明</span><span class="sxs-lookup"><span data-stu-id="32f28-109">DESCRIPTION</span></span>
<span data-ttu-id="32f28-110">**AzureRmSiteRecoveryReplicationProtectedItem** Cmdlet 會取得 Azure Site Recovery 受保護專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="32f28-110">The **Get-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet gets the properties of Azure Site Recovery Protected Items.</span></span>

## <span data-ttu-id="32f28-111">示例</span><span class="sxs-lookup"><span data-stu-id="32f28-111">EXAMPLES</span></span>

## <span data-ttu-id="32f28-112">參數</span><span class="sxs-lookup"><span data-stu-id="32f28-112">PARAMETERS</span></span>

### <span data-ttu-id="32f28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32f28-113">-DefaultProfile</span></span>
<span data-ttu-id="32f28-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="32f28-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32f28-115">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="32f28-115">-FriendlyName</span></span>
<span data-ttu-id="32f28-116">指定此 Cmdlet 所取得的複製受保護專案的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="32f28-116">Specifies the friendly name of the Replication Protected Item that this cmdlet gets.</span></span>

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

### <span data-ttu-id="32f28-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="32f28-117">-Name</span></span>
<span data-ttu-id="32f28-118">指定這個 Cmdlet 所取得之受保護的複製專案名稱。</span><span class="sxs-lookup"><span data-stu-id="32f28-118">Specifies the name of the Replication Protected Item that this cmdlet gets.</span></span>

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

### <span data-ttu-id="32f28-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="32f28-119">-ProtectableItem</span></span>
<span data-ttu-id="32f28-120">指定對應至複製受保護專案的可保護專案。</span><span class="sxs-lookup"><span data-stu-id="32f28-120">Specifies the Protectable Item corresponding to the Replication Protected Item.</span></span>

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

### <span data-ttu-id="32f28-121">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="32f28-121">-ProtectionContainer</span></span>
<span data-ttu-id="32f28-122">指定 Azure Site Recovery 保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="32f28-122">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="32f28-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f28-123">CommonParameters</span></span>
<span data-ttu-id="32f28-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32f28-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f28-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="32f28-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f28-126">輸入</span><span class="sxs-lookup"><span data-stu-id="32f28-126">INPUTS</span></span>

### <span data-ttu-id="32f28-127">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="32f28-127">ASRProtectableItem</span></span>
<span data-ttu-id="32f28-128">形參 "ProtectableItem" 接受管線中 "ASRProtectableItem" 類型的值</span><span class="sxs-lookup"><span data-stu-id="32f28-128">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

### <span data-ttu-id="32f28-129">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="32f28-129">ASRProtectionContainer</span></span>
<span data-ttu-id="32f28-130">形參 "ProtectionContainer" 接受管線中 "ASRProtectionContainer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="32f28-130">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="32f28-131">輸出</span><span class="sxs-lookup"><span data-stu-id="32f28-131">OUTPUTS</span></span>

### <span data-ttu-id="32f28-132">System.object. IEnumerable "1 [ASRReplicationProtectedItem，SiteRecovery，Version = 2.0.1.0，Culture = 中性，PublicKeyToken = null]] （SiteRecovery =，Culture = 中立）</span><span class="sxs-lookup"><span data-stu-id="32f28-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="32f28-133">筆記</span><span class="sxs-lookup"><span data-stu-id="32f28-133">NOTES</span></span>

## <span data-ttu-id="32f28-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="32f28-134">RELATED LINKS</span></span>

[<span data-ttu-id="32f28-135">新-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="32f28-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="32f28-136">移除-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="32f28-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="32f28-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="32f28-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
