---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: F6C01C25-655C-4798-9826-F7CB168181C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc8b7dc7e23a98111e75c2b2c9c079f010e3c5dc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967036"
---
# <span data-ttu-id="da4aa-101">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="da4aa-101">Get-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="da4aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da4aa-102">SYNOPSIS</span></span>
<span data-ttu-id="da4aa-103">取得網站復原電子倉庫的網路對應。</span><span class="sxs-lookup"><span data-stu-id="da4aa-103">Gets network mappings for a Site Recovery vault.</span></span>

## <span data-ttu-id="da4aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="da4aa-104">SYNTAX</span></span>

### <span data-ttu-id="da4aa-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="da4aa-105">EnterpriseToEnterprise</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="da4aa-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="da4aa-106">EnterpriseToAzure</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> [-Azure] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="da4aa-107">說明</span><span class="sxs-lookup"><span data-stu-id="da4aa-107">DESCRIPTION</span></span>
<span data-ttu-id="da4aa-108">**AzureSiteRecoveryNetworkMapping** Cmdlet 會取得目前網站復原電子倉庫的 Azure 網站復原網路對應的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="da4aa-108">The **Get-AzureSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="da4aa-109">示例</span><span class="sxs-lookup"><span data-stu-id="da4aa-109">EXAMPLES</span></span>

### <span data-ttu-id="da4aa-110">範例1：取得網路與恢復網路之間的對應</span><span class="sxs-lookup"><span data-stu-id="da4aa-110">Example 1: Get the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryNetworkId   : d903e2c6-3141-4cef-bfe1-04616cd43cbb
RecoveryNetworkName : phase2PrimaryVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="da4aa-111">第一個命令 Cmdlet 會使用 **AzureSiteRecoveryServer** Cmdlet，為目前的 Azure Site Recovery 保存庫取得伺服器。</span><span class="sxs-lookup"><span data-stu-id="da4aa-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="da4aa-112">該命令會將網站復原伺服器儲存在 $Servers 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="da4aa-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="da4aa-113">第二個命令會取得主要網路和恢復網路之間的對應。</span><span class="sxs-lookup"><span data-stu-id="da4aa-113">The second command gets the mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="da4aa-114">命令會將網路對應的主伺服器指定為 $Servers 的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="da4aa-114">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="da4aa-115">該命令會將恢復網路的伺服器指定為 $Servers 的第二個元素。</span><span class="sxs-lookup"><span data-stu-id="da4aa-115">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

### <span data-ttu-id="da4aa-116">範例2：取得網路與 Azure 虛擬機器網路之間的對應</span><span class="sxs-lookup"><span data-stu-id="da4aa-116">Example 2: Get the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -Azure -PrimaryServer $Servers[0] 
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 21a9403c-6ec1-44f2-b744-b4e50b792387
RecoveryNetworkId   : ecb3a462-664f-4f57-873e-d09b5925e1a1
RecoveryNetworkName : AzureVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="da4aa-117">第一個命令 Cmdlet 會針對目前的網站復原電子倉庫取得伺服器。</span><span class="sxs-lookup"><span data-stu-id="da4aa-117">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="da4aa-118">該命令會將伺服器儲存在 $Servers 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="da4aa-118">The command stores the servers in the $Servers array variable.</span></span>

<span data-ttu-id="da4aa-119">第二個命令會在主要網路和 Azure 虛擬機器網路之間取得對應。</span><span class="sxs-lookup"><span data-stu-id="da4aa-119">The second command gets a mapping between the primary network and an Azure virtual machine network.</span></span>
<span data-ttu-id="da4aa-120">該命令會將網路的主要伺服器指定為 $Servers 的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="da4aa-120">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="da4aa-121">命令會指定 *Azure* 參數。</span><span class="sxs-lookup"><span data-stu-id="da4aa-121">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="da4aa-122">因此，命令會取得 Azure 虛擬機器網路的對應。</span><span class="sxs-lookup"><span data-stu-id="da4aa-122">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

## <span data-ttu-id="da4aa-123">參數</span><span class="sxs-lookup"><span data-stu-id="da4aa-123">PARAMETERS</span></span>

### <span data-ttu-id="da4aa-124">-Azure</span><span class="sxs-lookup"><span data-stu-id="da4aa-124">-Azure</span></span>
<span data-ttu-id="da4aa-125">表示此 Cmdlet 會取得對應至 Azure 虛擬網路之主伺服器上網路的網路對應。</span><span class="sxs-lookup"><span data-stu-id="da4aa-125">Indicates that this cmdlet gets network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4aa-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="da4aa-126">-PrimaryServer</span></span>
<span data-ttu-id="da4aa-127">指定要取得對應的主伺服器。</span><span class="sxs-lookup"><span data-stu-id="da4aa-127">Specifies a primary server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4aa-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="da4aa-128">-Profile</span></span>
<span data-ttu-id="da4aa-129">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="da4aa-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="da4aa-130">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="da4aa-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da4aa-131">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="da4aa-131">-RecoveryServer</span></span>
<span data-ttu-id="da4aa-132">指定要取得其對應的復原伺服器。</span><span class="sxs-lookup"><span data-stu-id="da4aa-132">Specifies a recovery server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da4aa-133">CommonParameters</span></span>
<span data-ttu-id="da4aa-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da4aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da4aa-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="da4aa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da4aa-136">輸入</span><span class="sxs-lookup"><span data-stu-id="da4aa-136">INPUTS</span></span>

## <span data-ttu-id="da4aa-137">輸出</span><span class="sxs-lookup"><span data-stu-id="da4aa-137">OUTPUTS</span></span>

## <span data-ttu-id="da4aa-138">筆記</span><span class="sxs-lookup"><span data-stu-id="da4aa-138">NOTES</span></span>

## <span data-ttu-id="da4aa-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="da4aa-139">RELATED LINKS</span></span>

[<span data-ttu-id="da4aa-140">新-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="da4aa-140">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="da4aa-141">移除-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="da4aa-141">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


