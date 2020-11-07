---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967556"
---
# <span data-ttu-id="cee85-101">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cee85-101">Remove-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="cee85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cee85-102">SYNOPSIS</span></span>
<span data-ttu-id="cee85-103">從 Site Recovery 保存庫移除網路對應。</span><span class="sxs-lookup"><span data-stu-id="cee85-103">Removes a network mapping from a Site Recovery vault.</span></span>

## <span data-ttu-id="cee85-104">句法</span><span class="sxs-lookup"><span data-stu-id="cee85-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="cee85-105">說明</span><span class="sxs-lookup"><span data-stu-id="cee85-105">DESCRIPTION</span></span>
<span data-ttu-id="cee85-106">**AzureSiteRecoveryNetworkMapping** Cmdlet 會從目前的 Azure Site Recovery 保存庫中移除網路對應。</span><span class="sxs-lookup"><span data-stu-id="cee85-106">The **Remove-AzureSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="cee85-107">示例</span><span class="sxs-lookup"><span data-stu-id="cee85-107">EXAMPLES</span></span>

### <span data-ttu-id="cee85-108">範例1：移除網路與恢復網路之間的對應</span><span class="sxs-lookup"><span data-stu-id="cee85-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="cee85-109">第一個命令 Cmdlet 會使用 **AzureSiteRecoveryServer** Cmdlet，為目前的 Azure Site Recovery 保存庫取得伺服器。</span><span class="sxs-lookup"><span data-stu-id="cee85-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="cee85-110">該命令會將網站復原伺服器儲存在 $Servers 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="cee85-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="cee85-111">第二個命令會在主要網路和恢復網路之間取得對應，然後將它儲存在 $NetworkMapping 變數中。</span><span class="sxs-lookup"><span data-stu-id="cee85-111">The second command gets the mapping between the primary network and the recovery network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="cee85-112">命令會將網路對應的主伺服器指定為 $Servers 的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="cee85-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="cee85-113">該命令會將恢復網路的伺服器指定為 $Servers 的第二個元素。</span><span class="sxs-lookup"><span data-stu-id="cee85-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="cee85-114">最後一個命令會在 $NetworkMapping 中移除網路對應。</span><span class="sxs-lookup"><span data-stu-id="cee85-114">The final command removes the network mapping in $NetworkMapping.</span></span>

### <span data-ttu-id="cee85-115">範例2：移除網路與 Azure 虛擬機器網路之間的對應</span><span class="sxs-lookup"><span data-stu-id="cee85-115">Example 2: Remove the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="cee85-116">第一個命令 Cmdlet 會針對目前的網站復原電子倉庫取得伺服器。</span><span class="sxs-lookup"><span data-stu-id="cee85-116">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="cee85-117">該命令會將網站復原伺服器儲存在 $Servers 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="cee85-117">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="cee85-118">第二個命令會在主要網路和 Azure 虛擬機器網路之間取得對應，然後將它儲存在 $NetworkMapping 變數中。</span><span class="sxs-lookup"><span data-stu-id="cee85-118">The second command gets a mapping between the primary network and an Azure virtual machine network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="cee85-119">該命令會將網路的主要伺服器指定為 $Servers 的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="cee85-119">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="cee85-120">命令會指定 *Azure* 參數。</span><span class="sxs-lookup"><span data-stu-id="cee85-120">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="cee85-121">因此，命令會取得 Azure 虛擬機器網路的對應。</span><span class="sxs-lookup"><span data-stu-id="cee85-121">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

<span data-ttu-id="cee85-122">最後一個命令會在 $NetworkMapping 中移除網路對應。</span><span class="sxs-lookup"><span data-stu-id="cee85-122">The final command removes the network mapping in $NetworkMapping.</span></span>

## <span data-ttu-id="cee85-123">參數</span><span class="sxs-lookup"><span data-stu-id="cee85-123">PARAMETERS</span></span>

### <span data-ttu-id="cee85-124">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cee85-124">-NetworkMapping</span></span>
<span data-ttu-id="cee85-125">指定要移除的網路對應。</span><span class="sxs-lookup"><span data-stu-id="cee85-125">Specifies the network mapping to remove.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cee85-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="cee85-126">-Profile</span></span>
<span data-ttu-id="cee85-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="cee85-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cee85-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="cee85-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cee85-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee85-129">CommonParameters</span></span>
<span data-ttu-id="cee85-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cee85-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee85-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cee85-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee85-132">輸入</span><span class="sxs-lookup"><span data-stu-id="cee85-132">INPUTS</span></span>

## <span data-ttu-id="cee85-133">輸出</span><span class="sxs-lookup"><span data-stu-id="cee85-133">OUTPUTS</span></span>

## <span data-ttu-id="cee85-134">筆記</span><span class="sxs-lookup"><span data-stu-id="cee85-134">NOTES</span></span>

## <span data-ttu-id="cee85-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="cee85-135">RELATED LINKS</span></span>

[<span data-ttu-id="cee85-136">AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cee85-136">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="cee85-137">新-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cee85-137">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="cee85-138">AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="cee85-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


