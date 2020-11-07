---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 3cd241b84f7ac03dc268a8f04df0490f6a9f9665
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802038"
---
# <span data-ttu-id="5ebdb-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5ebdb-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="5ebdb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ebdb-102">SYNOPSIS</span></span>
<span data-ttu-id="5ebdb-103">建立負載平衡器的前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ebdb-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ebdb-104">SYNTAX</span></span>

### <span data-ttu-id="5ebdb-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="5ebdb-105">SetByResourceSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ebdb-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="5ebdb-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ebdb-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ebdb-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ebdb-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ebdb-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ebdb-109">說明</span><span class="sxs-lookup"><span data-stu-id="5ebdb-109">DESCRIPTION</span></span>
<span data-ttu-id="5ebdb-110">**新的-AzureRmLoadBalancerFrontendIpConfig** Cmdlet 會為 Azure 負載平衡器建立前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="5ebdb-111">示例</span><span class="sxs-lookup"><span data-stu-id="5ebdb-111">EXAMPLES</span></span>

### <span data-ttu-id="5ebdb-112">範例1：建立負載平衡器的前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="5ebdb-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="5ebdb-113">第一個命令會在名為 [MyResourceGroup] 的資源群組中建立名為 MyPublicIP 的動態公用 IP 位址，然後將它儲存在 $publicip 變數中。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="5ebdb-114">第二個命令會使用 $publicip 中的公用 IP 位址來建立名為 FrontendIpConfig01 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="5ebdb-115">參數</span><span class="sxs-lookup"><span data-stu-id="5ebdb-115">PARAMETERS</span></span>

### <span data-ttu-id="5ebdb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ebdb-116">-DefaultProfile</span></span>
<span data-ttu-id="5ebdb-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ebdb-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ebdb-118">-Name</span></span>
<span data-ttu-id="5ebdb-119">指定此 Cmdlet 所建立的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5ebdb-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ebdb-120">-PrivateIpAddress</span></span>
<span data-ttu-id="5ebdb-121">指定負載平衡器的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="5ebdb-122">如果您也指定了 *Subnet* 參數，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="5ebdb-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ebdb-123">-PublicIpAddress</span></span>
<span data-ttu-id="5ebdb-124">指定要與前端 IP 配置相關聯的 **PublicIpAddress** 物件。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="5ebdb-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="5ebdb-125">-PublicIpAddressId</span></span>
<span data-ttu-id="5ebdb-126">指定要與前端 IP 設定相關聯之 **PublicIpAddress** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="5ebdb-127">-子網</span><span class="sxs-lookup"><span data-stu-id="5ebdb-127">-Subnet</span></span>
<span data-ttu-id="5ebdb-128">指定要建立前端 IP 配置的 **子網** 物件。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="5ebdb-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5ebdb-129">-SubnetId</span></span>
<span data-ttu-id="5ebdb-130">指定要在其中建立前端 IP 配置的子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="5ebdb-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="5ebdb-131">-Zone</span></span>
<span data-ttu-id="5ebdb-132">代表資源所分派的 IP 必須來自的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="5ebdb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ebdb-133">CommonParameters</span></span>
<span data-ttu-id="5ebdb-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ebdb-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ebdb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ebdb-136">輸入</span><span class="sxs-lookup"><span data-stu-id="5ebdb-136">INPUTS</span></span>

## <span data-ttu-id="5ebdb-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5ebdb-137">OUTPUTS</span></span>

### <span data-ttu-id="5ebdb-138">PSFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5ebdb-138">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="5ebdb-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5ebdb-139">NOTES</span></span>

## <span data-ttu-id="5ebdb-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ebdb-140">RELATED LINKS</span></span>

[<span data-ttu-id="5ebdb-141">附加 AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5ebdb-141">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5ebdb-142">AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5ebdb-142">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5ebdb-143">新-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ebdb-143">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="5ebdb-144">移除-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5ebdb-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="5ebdb-145">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5ebdb-145">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


