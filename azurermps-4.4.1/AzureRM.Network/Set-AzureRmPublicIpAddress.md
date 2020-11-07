---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: 1460b4497909d56e2d10d03e33df71518c52b796
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623876"
---
# <span data-ttu-id="a96ea-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a96ea-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="a96ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a96ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a96ea-103">設定公用 IP 位址的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="a96ea-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a96ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="a96ea-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a96ea-105">說明</span><span class="sxs-lookup"><span data-stu-id="a96ea-105">DESCRIPTION</span></span>
<span data-ttu-id="a96ea-106">**AzureRmPublicIpAddress** Cmdlet 設定公用 IP 位址的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="a96ea-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="a96ea-107">示例</span><span class="sxs-lookup"><span data-stu-id="a96ea-107">EXAMPLES</span></span>

### <span data-ttu-id="a96ea-108">1：變更公用 IP 位址的配置方法</span><span class="sxs-lookup"><span data-stu-id="a96ea-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="a96ea-109">第一個命令會在資源群組 $rgName 中取得名稱 $publicIPName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="a96ea-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="a96ea-110">[第二個] 命令會將公用 IP 位址物件的配置方法設定為「靜態」。</span><span class="sxs-lookup"><span data-stu-id="a96ea-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="a96ea-111">Set-AzureRmPublicIPAddress 命令會以更新的物件更新公用 IP 位址資源，並將分攤方法修改為 [Static "。</span><span class="sxs-lookup"><span data-stu-id="a96ea-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="a96ea-112">公用 IP 位址會立即得到分配。</span><span class="sxs-lookup"><span data-stu-id="a96ea-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="a96ea-113">2：變更公用 IP 位址的 DNS 網域標籤</span><span class="sxs-lookup"><span data-stu-id="a96ea-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="a96ea-114">第一個命令會在資源群組 $rgName 中取得名稱 $publicIPName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="a96ea-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="a96ea-115">[第二個] 命令會將 DomainNameLabel 屬性設為所需的 dns 前置詞。</span><span class="sxs-lookup"><span data-stu-id="a96ea-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="a96ea-116">Set-AzureRmPublicIPAddress 命令會以更新的物件更新公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="a96ea-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="a96ea-117">DomainNameLabel & Fqdn 會依預期修改。</span><span class="sxs-lookup"><span data-stu-id="a96ea-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="a96ea-118">參數</span><span class="sxs-lookup"><span data-stu-id="a96ea-118">PARAMETERS</span></span>

### <span data-ttu-id="a96ea-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a96ea-119">-PublicIpAddress</span></span>
<span data-ttu-id="a96ea-120">指定代表應該設定公用 IP 位址之目標狀態的 **PublicIpAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="a96ea-120">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a96ea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a96ea-121">-DefaultProfile</span></span>
<span data-ttu-id="a96ea-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a96ea-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a96ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a96ea-123">CommonParameters</span></span>
<span data-ttu-id="a96ea-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a96ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a96ea-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a96ea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a96ea-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a96ea-126">INPUTS</span></span>

### <span data-ttu-id="a96ea-127">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a96ea-127">PSPublicIpAddress</span></span>
<span data-ttu-id="a96ea-128">形參 "PublicIpAddress" 接受管線中 "PSPublicIpAddress" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a96ea-128">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="a96ea-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a96ea-129">OUTPUTS</span></span>

### <span data-ttu-id="a96ea-130">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a96ea-130">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="a96ea-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a96ea-131">NOTES</span></span>

## <span data-ttu-id="a96ea-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a96ea-132">RELATED LINKS</span></span>

[<span data-ttu-id="a96ea-133">AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a96ea-133">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="a96ea-134">AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a96ea-134">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="a96ea-135">新-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a96ea-135">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="a96ea-136">移除-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a96ea-136">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


