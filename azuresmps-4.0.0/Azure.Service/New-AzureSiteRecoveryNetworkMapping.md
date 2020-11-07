---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6802F2E9-5925-4E92-AEB8-827B5A303617
online version: ''
schema: 2.0.0
ms.openlocfilehash: 153e30c03de7a0a5c404526bd06b9acb2f0678f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967663"
---
# <span data-ttu-id="98a0a-101">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="98a0a-101">New-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="98a0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="98a0a-103">在虛擬網路之間建立對應。</span><span class="sxs-lookup"><span data-stu-id="98a0a-103">Creates a mapping between virtual networks.</span></span>

## <span data-ttu-id="98a0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="98a0a-104">SYNTAX</span></span>

### <span data-ttu-id="98a0a-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="98a0a-105">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -RecoveryNetwork <ASRNetwork>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="98a0a-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="98a0a-106">EnterpriseToAzure</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -AzureSubscriptionId <String>
 -AzureVMNetworkId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="98a0a-107">說明</span><span class="sxs-lookup"><span data-stu-id="98a0a-107">DESCRIPTION</span></span>
<span data-ttu-id="98a0a-108">**新的-AzureSiteRecoveryNetworkMapping** Cmdlet 會在兩個虛擬網路之間建立對應，並傳回 Azure Site Recovery 作業來進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="98a0a-108">The **New-AzureSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="98a0a-109">示例</span><span class="sxs-lookup"><span data-stu-id="98a0a-109">EXAMPLES</span></span>

### <span data-ttu-id="98a0a-110">範例1：建立網路與恢復網路之間的對應</span><span class="sxs-lookup"><span data-stu-id="98a0a-110">Example 1: Create a mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Networks = Get-AzureSiteRecoveryNetwork -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork $Networks[0] -RecoveryNetwork $Networks[1]
```

<span data-ttu-id="98a0a-111">第一個命令 Cmdlet 會使用 **AzureSiteRecoveryServer** Cmdlet，為目前的 Azure Site Recovery 保存庫取得伺服器。</span><span class="sxs-lookup"><span data-stu-id="98a0a-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="98a0a-112">該命令會將網站復原伺服器儲存在 $Servers 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="98a0a-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="98a0a-113">第二個命令會使用 **AzureSiteRecoveryNetwork** Cmdlet，透過 $Servers 陣列中的第一個伺服器來取得網站恢復網路。</span><span class="sxs-lookup"><span data-stu-id="98a0a-113">The second command gets the site recovery network for the first server in the $Servers array by using the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>
<span data-ttu-id="98a0a-114">該命令會將網路儲存在 $Networks 變數中。</span><span class="sxs-lookup"><span data-stu-id="98a0a-114">The command stores the networks in the $Networks variable.</span></span>

<span data-ttu-id="98a0a-115">最後一個命令會在主要網路和恢復網路之間建立對應。</span><span class="sxs-lookup"><span data-stu-id="98a0a-115">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="98a0a-116">該命令會將主要網路指定為 $Networks 的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="98a0a-116">The command specifies the primary network as the first element of $Networks.</span></span>
<span data-ttu-id="98a0a-117">該命令會將恢復網路指定為 $Networks 的第二個元素。</span><span class="sxs-lookup"><span data-stu-id="98a0a-117">The command specifies the recovery network as the second element of $Networks.</span></span>

## <span data-ttu-id="98a0a-118">參數</span><span class="sxs-lookup"><span data-stu-id="98a0a-118">PARAMETERS</span></span>

### <span data-ttu-id="98a0a-119">-AzureSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98a0a-119">-AzureSubscriptionId</span></span>
<span data-ttu-id="98a0a-120">指定您的 Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="98a0a-120">Specifies the ID of your Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a0a-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="98a0a-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="98a0a-122">指定 Azure 虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="98a0a-122">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a0a-123">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="98a0a-123">-PrimaryNetwork</span></span>
<span data-ttu-id="98a0a-124">指定主要網路物件。</span><span class="sxs-lookup"><span data-stu-id="98a0a-124">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a0a-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="98a0a-125">-Profile</span></span>
<span data-ttu-id="98a0a-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="98a0a-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="98a0a-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="98a0a-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a0a-128">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="98a0a-128">-RecoveryNetwork</span></span>
<span data-ttu-id="98a0a-129">指定復原網路物件。</span><span class="sxs-lookup"><span data-stu-id="98a0a-129">Specifies the recovery network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98a0a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a0a-130">CommonParameters</span></span>
<span data-ttu-id="98a0a-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98a0a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a0a-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="98a0a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a0a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="98a0a-133">INPUTS</span></span>

## <span data-ttu-id="98a0a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="98a0a-134">OUTPUTS</span></span>

## <span data-ttu-id="98a0a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="98a0a-135">NOTES</span></span>

## <span data-ttu-id="98a0a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="98a0a-136">RELATED LINKS</span></span>

[<span data-ttu-id="98a0a-137">AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="98a0a-137">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="98a0a-138">AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="98a0a-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="98a0a-139">移除-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="98a0a-139">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


