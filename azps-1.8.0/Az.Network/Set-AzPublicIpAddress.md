---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: cc2ef6f016047bd20beba1671129a15c3dfa06f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621427"
---
# <span data-ttu-id="67b27-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="67b27-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="67b27-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67b27-102">SYNOPSIS</span></span>
<span data-ttu-id="67b27-103">更新公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="67b27-103">Updates a public IP address.</span></span>

## <span data-ttu-id="67b27-104">句法</span><span class="sxs-lookup"><span data-stu-id="67b27-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67b27-105">說明</span><span class="sxs-lookup"><span data-stu-id="67b27-105">DESCRIPTION</span></span>
<span data-ttu-id="67b27-106">**AzPublicIpAddress** Cmdlet 會更新公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="67b27-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="67b27-107">示例</span><span class="sxs-lookup"><span data-stu-id="67b27-107">EXAMPLES</span></span>

### <span data-ttu-id="67b27-108">1：變更公用 IP 位址的配置方法</span><span class="sxs-lookup"><span data-stu-id="67b27-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="67b27-109">第一個命令會在資源群組 $rgName 中取得名稱 $publicIPName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="67b27-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="67b27-110">[第二個] 命令會將公用 IP 位址物件的配置方法設定為「靜態」。</span><span class="sxs-lookup"><span data-stu-id="67b27-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="67b27-111">Set-AzPublicIPAddress 命令會以更新的物件更新公用 IP 位址資源，並將分攤方法修改為 [Static "。</span><span class="sxs-lookup"><span data-stu-id="67b27-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="67b27-112">公用 IP 位址會立即得到分配。</span><span class="sxs-lookup"><span data-stu-id="67b27-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="67b27-113">2：變更公用 IP 位址的 DNS 網域標籤</span><span class="sxs-lookup"><span data-stu-id="67b27-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="67b27-114">第一個命令會在資源群組 $rgName 中取得名稱 $publicIPName 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="67b27-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="67b27-115">[第二個] 命令會將 DomainNameLabel 屬性設為所需的 dns 前置詞。</span><span class="sxs-lookup"><span data-stu-id="67b27-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="67b27-116">Set-AzPublicIPAddress 命令會以更新的物件更新公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="67b27-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="67b27-117">DomainNameLabel & Fqdn 會依預期修改。</span><span class="sxs-lookup"><span data-stu-id="67b27-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="67b27-118">參數</span><span class="sxs-lookup"><span data-stu-id="67b27-118">PARAMETERS</span></span>

### <span data-ttu-id="67b27-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67b27-119">-AsJob</span></span>
<span data-ttu-id="67b27-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="67b27-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b27-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b27-121">-DefaultProfile</span></span>
<span data-ttu-id="67b27-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67b27-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67b27-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="67b27-123">-PublicIpAddress</span></span>
<span data-ttu-id="67b27-124">指定代表應該設定公用 IP 位址之狀態的公用 IP 位址物件。</span><span class="sxs-lookup"><span data-stu-id="67b27-124">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="67b27-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b27-125">CommonParameters</span></span>
<span data-ttu-id="67b27-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67b27-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b27-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67b27-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b27-128">輸入</span><span class="sxs-lookup"><span data-stu-id="67b27-128">INPUTS</span></span>

### <span data-ttu-id="67b27-129">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="67b27-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="67b27-130">輸出</span><span class="sxs-lookup"><span data-stu-id="67b27-130">OUTPUTS</span></span>

### <span data-ttu-id="67b27-131">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="67b27-131">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="67b27-132">筆記</span><span class="sxs-lookup"><span data-stu-id="67b27-132">NOTES</span></span>

## <span data-ttu-id="67b27-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="67b27-133">RELATED LINKS</span></span>

[<span data-ttu-id="67b27-134">AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="67b27-134">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="67b27-135">新-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="67b27-135">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="67b27-136">移除-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="67b27-136">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


