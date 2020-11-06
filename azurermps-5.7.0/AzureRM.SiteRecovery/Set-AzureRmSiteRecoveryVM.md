---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 483D4C1A-D34E-40ED-B92B-82187FF321F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: b330cb59281a3f140ba30f10f31ecb5bf3b49f97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454003"
---
# <span data-ttu-id="e8bd2-101">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="e8bd2-101">Set-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="e8bd2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="e8bd2-103">設定網站恢復保護實體的復原端選項。</span><span class="sxs-lookup"><span data-stu-id="e8bd2-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8bd2-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8bd2-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryNicSubnetName <String>]
 [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8bd2-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="e8bd2-106">**AzureRmSiteRecoveryVM** Cmdlet 會針對 Azure Site recovery 保護實體設定復原端保護選項，例如，恢復虛擬機器大小與復原虛擬機器網路。</span><span class="sxs-lookup"><span data-stu-id="e8bd2-106">The **Set-AzureRmSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="e8bd2-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8bd2-107">EXAMPLES</span></span>

## <span data-ttu-id="e8bd2-108">參數</span><span class="sxs-lookup"><span data-stu-id="e8bd2-108">PARAMETERS</span></span>

### <span data-ttu-id="e8bd2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8bd2-109">-DefaultProfile</span></span>
<span data-ttu-id="e8bd2-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8bd2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8bd2-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8bd2-111">-Name</span></span>
<span data-ttu-id="e8bd2-112">指定目標虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8bd2-112">Specifies the name of the target virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bd2-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="e8bd2-113">-NicSelectionType</span></span>
<span data-ttu-id="e8bd2-114">指定網路介面卡選取專案屬性。</span><span class="sxs-lookup"><span data-stu-id="e8bd2-114">Specifies the network adapter selection properties.</span></span>
<span data-ttu-id="e8bd2-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e8bd2-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e8bd2-116">NotSelected</span><span class="sxs-lookup"><span data-stu-id="e8bd2-116">NotSelected</span></span>
- <span data-ttu-id="e8bd2-117">SelectedByUser</span><span class="sxs-lookup"><span data-stu-id="e8bd2-117">SelectedByUser</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bd2-118">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="e8bd2-118">-PrimaryNic</span></span>
<span data-ttu-id="e8bd2-119">指定主要網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="e8bd2-119">Specifies the primary network adapter card.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bd2-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="e8bd2-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="e8bd2-121">指定恢復網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8bd2-121">Specifies the recovery network ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bd2-122">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="e8bd2-122">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="e8bd2-123">指定在恢復時指派給主要網路介面卡控制器的靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e8bd2-123">Specifies the static IP address that is assigned to primary network adapter controller on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bd2-124">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="e8bd2-124">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="e8bd2-125">指定要在恢復時附加主要網路介面卡控制器的 Azure 虛擬網路子網名稱。</span><span class="sxs-lookup"><span data-stu-id="e8bd2-125">Specifies the Azure virtual network subnet name with which to attach the primary network adapter controller on recovery.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bd2-126">-大小</span><span class="sxs-lookup"><span data-stu-id="e8bd2-126">-Size</span></span>
<span data-ttu-id="e8bd2-127">指定目標虛擬機器大小。</span><span class="sxs-lookup"><span data-stu-id="e8bd2-127">Specifies the target virtual machine size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bd2-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e8bd2-128">-VirtualMachine</span></span>
<span data-ttu-id="e8bd2-129">指定網站復原虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="e8bd2-129">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bd2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8bd2-130">CommonParameters</span></span>
<span data-ttu-id="e8bd2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8bd2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8bd2-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8bd2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8bd2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e8bd2-133">INPUTS</span></span>

### <span data-ttu-id="e8bd2-134">ASRVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e8bd2-134">ASRVirtualMachine</span></span>
<span data-ttu-id="e8bd2-135">形參 "VirtualMachine" 接受管線中 "ASRVirtualMachine" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e8bd2-135">Parameter 'VirtualMachine' accepts value of type 'ASRVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="e8bd2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e8bd2-136">OUTPUTS</span></span>

### <span data-ttu-id="e8bd2-137">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e8bd2-137">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e8bd2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e8bd2-138">NOTES</span></span>

## <span data-ttu-id="e8bd2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8bd2-139">RELATED LINKS</span></span>

[<span data-ttu-id="e8bd2-140">AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="e8bd2-140">Get-AzureRmSiteRecoveryVM</span></span>](./Get-AzureRmSiteRecoveryVM.md)
