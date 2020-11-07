---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: d78e4d8e84508e9a737bb15dc31b0dad1c9bdedc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800717"
---
# <span data-ttu-id="80bab-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="80bab-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="80bab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80bab-102">SYNOPSIS</span></span>
<span data-ttu-id="80bab-103">設定公用 IP 位址的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="80bab-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80bab-104">句法</span><span class="sxs-lookup"><span data-stu-id="80bab-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80bab-105">說明</span><span class="sxs-lookup"><span data-stu-id="80bab-105">DESCRIPTION</span></span>
<span data-ttu-id="80bab-106">**AzureRmPublicIpAddress** Cmdlet 設定公用 IP 位址的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="80bab-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="80bab-107">示例</span><span class="sxs-lookup"><span data-stu-id="80bab-107">EXAMPLES</span></span>

### <span data-ttu-id="80bab-108">1：變更公用 IP 位址的配置方法</span><span class="sxs-lookup"><span data-stu-id="80bab-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="80bab-109">第一個命令會在資源群組 $rgName 中取得名稱 $publicIPName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="80bab-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="80bab-110">[第二個] 命令會將公用 IP 位址物件的配置方法設定為「靜態」。</span><span class="sxs-lookup"><span data-stu-id="80bab-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="80bab-111">Set-AzureRmPublicIPAddress 命令會以更新的物件更新公用 IP 位址資源，並將分攤方法修改為 [Static "。</span><span class="sxs-lookup"><span data-stu-id="80bab-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="80bab-112">公用 IP 位址會立即得到分配。</span><span class="sxs-lookup"><span data-stu-id="80bab-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="80bab-113">2：變更公用 IP 位址的 DNS 網域標籤</span><span class="sxs-lookup"><span data-stu-id="80bab-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="80bab-114">第一個命令會在資源群組 $rgName 中取得名稱 $publicIPName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="80bab-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="80bab-115">[第二個] 命令會將 DomainNameLabel 屬性設為所需的 dns 前置詞。</span><span class="sxs-lookup"><span data-stu-id="80bab-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="80bab-116">Set-AzureRmPublicIPAddress 命令會以更新的物件更新公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="80bab-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="80bab-117">DomainNameLabel & Fqdn 會依預期修改。</span><span class="sxs-lookup"><span data-stu-id="80bab-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="80bab-118">參數</span><span class="sxs-lookup"><span data-stu-id="80bab-118">PARAMETERS</span></span>

### <span data-ttu-id="80bab-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80bab-119">-AsJob</span></span>
<span data-ttu-id="80bab-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80bab-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80bab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80bab-121">-DefaultProfile</span></span>
<span data-ttu-id="80bab-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80bab-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80bab-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="80bab-123">-PublicIpAddress</span></span>
<span data-ttu-id="80bab-124">指定代表應該設定公用 IP 位址之目標狀態的 **PublicIpAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="80bab-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80bab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80bab-125">CommonParameters</span></span>
<span data-ttu-id="80bab-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80bab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80bab-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80bab-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80bab-128">輸入</span><span class="sxs-lookup"><span data-stu-id="80bab-128">INPUTS</span></span>

### <span data-ttu-id="80bab-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="80bab-129">PSPublicIpAddress</span></span>
<span data-ttu-id="80bab-130">形參 "PublicIpAddress" 接受管線中 "PSPublicIpAddress" 類型的值</span><span class="sxs-lookup"><span data-stu-id="80bab-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="80bab-131">輸出</span><span class="sxs-lookup"><span data-stu-id="80bab-131">OUTPUTS</span></span>

### <span data-ttu-id="80bab-132">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="80bab-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="80bab-133">筆記</span><span class="sxs-lookup"><span data-stu-id="80bab-133">NOTES</span></span>

## <span data-ttu-id="80bab-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="80bab-134">RELATED LINKS</span></span>

[<span data-ttu-id="80bab-135">AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="80bab-135">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="80bab-136">新-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="80bab-136">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="80bab-137">移除-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="80bab-137">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


