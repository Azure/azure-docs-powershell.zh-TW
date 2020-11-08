---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 9df5cdd2a601977b453cb8242a9241cede3d4539
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126488"
---
# <span data-ttu-id="ff353-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ff353-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="ff353-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff353-102">SYNOPSIS</span></span>
<span data-ttu-id="ff353-103">取得公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ff353-103">Gets a public IP address.</span></span>

## <span data-ttu-id="ff353-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff353-104">SYNTAX</span></span>

### <span data-ttu-id="ff353-105">NoExpandStandAloneIp (預設) </span><span class="sxs-lookup"><span data-stu-id="ff353-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff353-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="ff353-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff353-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="ff353-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff353-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="ff353-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff353-109">說明</span><span class="sxs-lookup"><span data-stu-id="ff353-109">DESCRIPTION</span></span>
<span data-ttu-id="ff353-110">**AzPublicIPAddress** Cmdlet 會取得資源群組中的一個或多個公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ff353-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="ff353-111">示例</span><span class="sxs-lookup"><span data-stu-id="ff353-111">EXAMPLES</span></span>

### <span data-ttu-id="ff353-112">範例1：取得公用 IP 資源</span><span class="sxs-lookup"><span data-stu-id="ff353-112">Example 1: Get a public IP resource</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp1 -ResourceGroupName myRg

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="ff353-113">這個命令會在資源群組 myRg 中取得名稱為 myPublicIp 的公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="ff353-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="ff353-114">範例2：使用篩選來取得公用 IP 資源</span><span class="sxs-lookup"><span data-stu-id="ff353-114">Example 2: Get public IP resources using filtering</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp*

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="ff353-115">這個命令會取得名稱以 myPublicIp 開頭的所有公用 IP 位址資源。</span><span class="sxs-lookup"><span data-stu-id="ff353-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="ff353-116">參數</span><span class="sxs-lookup"><span data-stu-id="ff353-116">PARAMETERS</span></span>

### <span data-ttu-id="ff353-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff353-117">-DefaultProfile</span></span>
<span data-ttu-id="ff353-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff353-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff353-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ff353-119">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff353-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ff353-120">-IpConfigurationName</span></span>
<span data-ttu-id="ff353-121">網路介面 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="ff353-121">Network Interface IP Configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff353-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff353-122">-Name</span></span>
<span data-ttu-id="ff353-123">指定此 Cmdlet 所取得之公用 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff353-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ff353-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="ff353-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="ff353-125">虛擬機器網路介面名稱。</span><span class="sxs-lookup"><span data-stu-id="ff353-125">Virtual Machine Network Interface Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff353-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff353-126">-ResourceGroupName</span></span>
<span data-ttu-id="ff353-127">指定包含此 Cmdlet 所取得之公用 IP 位址之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff353-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ff353-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="ff353-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="ff353-129">虛擬機器索引。</span><span class="sxs-lookup"><span data-stu-id="ff353-129">Virtual Machine Index.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff353-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ff353-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="ff353-131">虛擬機器的規模集名稱。</span><span class="sxs-lookup"><span data-stu-id="ff353-131">Virtual Machine Scale Set Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff353-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff353-132">CommonParameters</span></span>
<span data-ttu-id="ff353-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff353-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff353-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ff353-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff353-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ff353-135">INPUTS</span></span>

### <span data-ttu-id="ff353-136">System.object</span><span class="sxs-lookup"><span data-stu-id="ff353-136">System.String</span></span>

## <span data-ttu-id="ff353-137">輸出</span><span class="sxs-lookup"><span data-stu-id="ff353-137">OUTPUTS</span></span>

### <span data-ttu-id="ff353-138">PSPublicIpAddress 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ff353-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="ff353-139">筆記</span><span class="sxs-lookup"><span data-stu-id="ff353-139">NOTES</span></span>

## <span data-ttu-id="ff353-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff353-140">RELATED LINKS</span></span>

[<span data-ttu-id="ff353-141">新-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ff353-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="ff353-142">移除-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ff353-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="ff353-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ff353-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


