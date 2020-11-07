---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: ba29cef7afe862f8aeb33f66488e0970b5ac6e9c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794270"
---
# <span data-ttu-id="49121-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="49121-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="49121-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49121-102">SYNOPSIS</span></span>
<span data-ttu-id="49121-103">建立負載平衡器的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="49121-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="49121-104">句法</span><span class="sxs-lookup"><span data-stu-id="49121-104">SYNTAX</span></span>

### <span data-ttu-id="49121-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="49121-105">SetByResourceSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49121-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="49121-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49121-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="49121-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49121-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="49121-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49121-109">說明</span><span class="sxs-lookup"><span data-stu-id="49121-109">DESCRIPTION</span></span>
<span data-ttu-id="49121-110">**新的-AzLoadBalancerFrontendIpConfig** Cmdlet 會為 Azure 負載平衡器建立前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="49121-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="49121-111">示例</span><span class="sxs-lookup"><span data-stu-id="49121-111">EXAMPLES</span></span>

### <span data-ttu-id="49121-112">範例1：建立負載平衡器的前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="49121-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="49121-113">第一個命令會在名為 [MyResourceGroup] 的資源群組中建立名為 MyPublicIP 的動態公用 IP 位址，然後將它儲存在 $publicip 變數中。</span><span class="sxs-lookup"><span data-stu-id="49121-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="49121-114">第二個命令會使用 $publicip 中的公用 IP 位址來建立名為 FrontendIpConfig01 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="49121-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="49121-115">參數</span><span class="sxs-lookup"><span data-stu-id="49121-115">PARAMETERS</span></span>

### <span data-ttu-id="49121-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49121-116">-DefaultProfile</span></span>
<span data-ttu-id="49121-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49121-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49121-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="49121-118">-Name</span></span>
<span data-ttu-id="49121-119">指定此 Cmdlet 所建立的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="49121-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49121-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="49121-120">-PrivateIpAddress</span></span>
<span data-ttu-id="49121-121">指定負載平衡器的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="49121-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="49121-122">如果您也指定了 *Subnet* 參數，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="49121-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49121-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="49121-123">-PublicIpAddress</span></span>
<span data-ttu-id="49121-124">指定要與前端 IP 配置相關聯的 **PublicIpAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="49121-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49121-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="49121-125">-PublicIpAddressId</span></span>
<span data-ttu-id="49121-126">指定要與前端 IP 設定相關聯之 **PublicIpAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="49121-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49121-127">-子網</span><span class="sxs-lookup"><span data-stu-id="49121-127">-Subnet</span></span>
<span data-ttu-id="49121-128">指定要建立前端 IP 配置的 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="49121-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49121-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="49121-129">-SubnetId</span></span>
<span data-ttu-id="49121-130">指定要在其中建立前端 IP 配置的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="49121-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49121-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="49121-131">-Zone</span></span>
<span data-ttu-id="49121-132">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="49121-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49121-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49121-133">CommonParameters</span></span>
<span data-ttu-id="49121-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49121-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49121-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49121-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49121-136">輸入</span><span class="sxs-lookup"><span data-stu-id="49121-136">INPUTS</span></span>

## <span data-ttu-id="49121-137">輸出</span><span class="sxs-lookup"><span data-stu-id="49121-137">OUTPUTS</span></span>

### <span data-ttu-id="49121-138">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="49121-138">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="49121-139">筆記</span><span class="sxs-lookup"><span data-stu-id="49121-139">NOTES</span></span>

## <span data-ttu-id="49121-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="49121-140">RELATED LINKS</span></span>

[<span data-ttu-id="49121-141">附加 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="49121-141">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="49121-142">AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="49121-142">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="49121-143">新-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="49121-143">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="49121-144">移除-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="49121-144">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="49121-145">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="49121-145">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


