---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 33712b9813d6c23ed72097597d94a22bf7644992
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911894"
---
# <span data-ttu-id="1b8c2-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1b8c2-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="1b8c2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1b8c2-102">SYNOPSIS</span></span>
<span data-ttu-id="1b8c2-103">更新公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-103">Updates a public IP address.</span></span>

## <span data-ttu-id="1b8c2-104">語法</span><span class="sxs-lookup"><span data-stu-id="1b8c2-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b8c2-105">描述</span><span class="sxs-lookup"><span data-stu-id="1b8c2-105">DESCRIPTION</span></span>
<span data-ttu-id="1b8c2-106">**Set-AzPublicIpAddress** Cmdlet 會更新公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="1b8c2-107">例子</span><span class="sxs-lookup"><span data-stu-id="1b8c2-107">EXAMPLES</span></span>

### <span data-ttu-id="1b8c2-108">1：變更公用 IP 位址的分配方法</span><span class="sxs-lookup"><span data-stu-id="1b8c2-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="1b8c2-109">第一個命令會獲得公用 IP 位址資源，其名稱$publicIPName資源群組中$rgName。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="1b8c2-110">第二個命令將公用 IP 位址物件的配置方法設定為「靜態」。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="1b8c2-111">Set-AzPublicIPAddress命令會以更新的物件更新公用 IP 位址資源，並且將配置方法修改為 '靜態'。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="1b8c2-112">公用 IP 位址會立即配置。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="1b8c2-113">2：新增公用 IP 位址的 DNS 網域標籤</span><span class="sxs-lookup"><span data-stu-id="1b8c2-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="1b8c2-114">第一個命令會獲得公用 IP 位址資源，其名稱$publicIPName資源群組中$rgName。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="1b8c2-115">第二個命令將 DomainNameLabel 屬性設定為必要的 dns 首碼。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="1b8c2-116">Set-AzPublicIPAddress命令會以更新的物件更新公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="1b8c2-117">DomainNameLabel & Fqdn 會如預期修改。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="1b8c2-118">3：變更公用 IP 位址的 DNS 網域標籤</span><span class="sxs-lookup"><span data-stu-id="1b8c2-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="1b8c2-119">第一個命令會獲得公用 IP 位址資源，其名稱$publicIPName資源群組中$rgName。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="1b8c2-120">第二個命令將 DomainNameLabel 屬性設定為必要的 dns 首碼。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="1b8c2-121">Set-AzPublicIPAddress命令會以更新的物件更新公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="1b8c2-122">DomainNameLabel & Fqdn 會如預期修改。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="1b8c2-123">參數</span><span class="sxs-lookup"><span data-stu-id="1b8c2-123">PARAMETERS</span></span>

### <span data-ttu-id="1b8c2-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b8c2-124">-AsJob</span></span>
<span data-ttu-id="1b8c2-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1b8c2-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b8c2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b8c2-126">-DefaultProfile</span></span>
<span data-ttu-id="1b8c2-127">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b8c2-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1b8c2-128">-PublicIpAddress</span></span>
<span data-ttu-id="1b8c2-129">指定代表應設定公用 IP 位址之狀態公用 IP 位址物件。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="1b8c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b8c2-130">CommonParameters</span></span>
<span data-ttu-id="1b8c2-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b8c2-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1b8c2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b8c2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="1b8c2-133">INPUTS</span></span>

### <span data-ttu-id="1b8c2-134">Microsoft.Azure.Commands.Network.models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1b8c2-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="1b8c2-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1b8c2-135">OUTPUTS</span></span>

### <span data-ttu-id="1b8c2-136">Microsoft.Azure.Commands.Network.models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1b8c2-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="1b8c2-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1b8c2-137">NOTES</span></span>

## <span data-ttu-id="1b8c2-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b8c2-138">RELATED LINKS</span></span>

[<span data-ttu-id="1b8c2-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1b8c2-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="1b8c2-140">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1b8c2-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="1b8c2-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1b8c2-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


