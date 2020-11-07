---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: df1c03551d520a833e8b974ae2a2b71fe442c4c4
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "93626658"
---
# <span data-ttu-id="0300d-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0300d-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="0300d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0300d-102">SYNOPSIS</span></span>
<span data-ttu-id="0300d-103">設定公用 IP 位址的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="0300d-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0300d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0300d-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0300d-105">說明</span><span class="sxs-lookup"><span data-stu-id="0300d-105">DESCRIPTION</span></span>
<span data-ttu-id="0300d-106">**AzureRmPublicIpAddress** Cmdlet 設定公用 IP 位址的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="0300d-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="0300d-107">示例</span><span class="sxs-lookup"><span data-stu-id="0300d-107">EXAMPLES</span></span>

### <span data-ttu-id="0300d-108">1：變更公用 IP 位址的配置方法</span><span class="sxs-lookup"><span data-stu-id="0300d-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="0300d-109">第一個命令會在資源群組 $rgName 中取得名稱 $publicIPName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="0300d-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="0300d-110">[第二個] 命令會將公用 IP 位址物件的配置方法設定為「靜態」。</span><span class="sxs-lookup"><span data-stu-id="0300d-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="0300d-111">Set-AzureRmPublicIPAddress 命令會以更新的物件更新公用 IP 位址資源，並將分攤方法修改為 [Static "。</span><span class="sxs-lookup"><span data-stu-id="0300d-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="0300d-112">公用 IP 位址會立即得到分配。</span><span class="sxs-lookup"><span data-stu-id="0300d-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="0300d-113">2：變更公用 IP 位址的 DNS 網域標籤</span><span class="sxs-lookup"><span data-stu-id="0300d-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="0300d-114">第一個命令會在資源群組 $rgName 中取得名稱 $publicIPName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="0300d-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="0300d-115">[第二個] 命令會將 DomainNameLabel 屬性設為所需的 dns 前置詞。</span><span class="sxs-lookup"><span data-stu-id="0300d-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="0300d-116">Set-AzureRmPublicIPAddress 命令會以更新的物件更新公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="0300d-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="0300d-117">DomainNameLabel & Fqdn 會依預期修改。</span><span class="sxs-lookup"><span data-stu-id="0300d-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="0300d-118">參數</span><span class="sxs-lookup"><span data-stu-id="0300d-118">PARAMETERS</span></span>

### <span data-ttu-id="0300d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0300d-119">-AsJob</span></span>
<span data-ttu-id="0300d-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0300d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0300d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0300d-121">-DefaultProfile</span></span>
<span data-ttu-id="0300d-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0300d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0300d-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0300d-123">-PublicIpAddress</span></span>
<span data-ttu-id="0300d-124">指定代表應該設定公用 IP 位址之目標狀態的 **PublicIpAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="0300d-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="0300d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0300d-125">CommonParameters</span></span>
<span data-ttu-id="0300d-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0300d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0300d-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0300d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0300d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="0300d-128">INPUTS</span></span>

### <span data-ttu-id="0300d-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0300d-129">PSPublicIpAddress</span></span>
<span data-ttu-id="0300d-130">形參 "PublicIpAddress" 接受管線中 "PSPublicIpAddress" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0300d-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="0300d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0300d-131">OUTPUTS</span></span>

### <span data-ttu-id="0300d-132">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0300d-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="0300d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="0300d-133">NOTES</span></span>

## <span data-ttu-id="0300d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="0300d-134">RELATED LINKS</span></span>

[<span data-ttu-id="0300d-135">AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0300d-135">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="0300d-136">新-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0300d-136">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="0300d-137">移除-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0300d-137">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


