---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 7985a979f9bbb89d6594416575e3fa00640784b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129859"
---
# <span data-ttu-id="87826-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="87826-101">Get-AzVmss</span></span>

## <span data-ttu-id="87826-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87826-102">SYNOPSIS</span></span>
<span data-ttu-id="87826-103">取得 VMSS 的屬性。</span><span class="sxs-lookup"><span data-stu-id="87826-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="87826-104">句法</span><span class="sxs-lookup"><span data-stu-id="87826-104">SYNTAX</span></span>

### <span data-ttu-id="87826-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="87826-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87826-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="87826-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87826-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="87826-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87826-108">說明</span><span class="sxs-lookup"><span data-stu-id="87826-108">DESCRIPTION</span></span>
<span data-ttu-id="87826-109">**AzVmss** Cmdlet 會取得虛擬機器縮放集 (VMSS) 的模型和實例視圖。</span><span class="sxs-lookup"><span data-stu-id="87826-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="87826-110">模型視圖是使用者指定的虛擬機器規模設定屬性。</span><span class="sxs-lookup"><span data-stu-id="87826-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="87826-111">[實例] 視圖是虛擬機器規模集的實例層級狀態。</span><span class="sxs-lookup"><span data-stu-id="87826-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="87826-112">指定 *InstanceView* 參數，只取得虛擬機器縮放集的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="87826-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="87826-113">示例</span><span class="sxs-lookup"><span data-stu-id="87826-113">EXAMPLES</span></span>

### <span data-ttu-id="87826-114">範例1：取得 VMSS 的屬性</span><span class="sxs-lookup"><span data-stu-id="87826-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"

ResourceGroupName                           : Group001
Sku                                         :
  Name                                      : Standard_DS1_v2
  Tier                                      : Standard
  Capacity                                  : 2
UpgradePolicy                               :
  Mode                                      : Manual
VirtualMachineProfile                       :
  OsProfile                                 :
    ComputerNamePrefix                      : test
    AdminUsername                           : contoso
    WindowsConfiguration                    :
      ProvisionVMAgent                      : True
      EnableAutomaticUpdates                : True
  StorageProfile                            :
    ImageReference                          :
      Publisher                             : MicrosoftWindowsServer
      Offer                                 : WindowsServer
      Sku                                   : 2016-Datacenter
      Version                               : latest
    OsDisk                                  :
      Caching                               : None
      CreateOption                          : FromImage
      ManagedDisk                           :
        StorageAccountType                  : Premium_LRS
  NetworkProfile                            :
    NetworkInterfaceConfigurations[0]       :
      Name                                  : Group001
      Primary                               : True
      EnableAcceleratedNetworking           : False
      NetworkSecurityGroup                  :
        Id                                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001
/providers/Microsoft.Network/networkSecurityGroups/Group001
      DnsSettings                           :
      IpConfigurations[0]                   :
        Name                                : Group001
        Subnet                              :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/virtualNetworks/Group001/subnets/Group001
        PrivateIPAddressVersion             : IPv4
        LoadBalancerBackendAddressPools[0]  :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/backendAddressPools/Group001
        LoadBalancerInboundNatPools[0]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
        LoadBalancerInboundNatPools[1]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
      EnableIPForwarding                    : False
ProvisioningState                           : Succeeded
Overprovision                               : True
UniqueId                                    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SinglePlacementGroup                        : False
Id                                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001/
providers/Microsoft.Compute/virtualMachineScaleSets/VMSS001
Name                                        : VMSS001
Type                                        : Microsoft.Compute/virtualMachineScaleSets
Location                                    : eastus
Tags                                        : {}
```

<span data-ttu-id="87826-115">這個命令會取得屬於名為 Group001 之資源群組之名為 VMSS001 的 VMSS 屬性。</span><span class="sxs-lookup"><span data-stu-id="87826-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="87826-116">由於命令不會指定 *InstanceView* 切換參數，因此 Cmdlet 會取得虛擬機器縮放集的模型視圖。</span><span class="sxs-lookup"><span data-stu-id="87826-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="87826-117">範例2：取得資源群組中的所有 Vmss</span><span class="sxs-lookup"><span data-stu-id="87826-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="87826-118">取得資源群組 "Group001" 中的所有 Vmss</span><span class="sxs-lookup"><span data-stu-id="87826-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="87826-119">範例3：取得訂閱中的所有 Vmss</span><span class="sxs-lookup"><span data-stu-id="87826-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="87826-120">取得訂閱中的所有 Vmss。</span><span class="sxs-lookup"><span data-stu-id="87826-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="87826-121">範例4：使用篩選取得所有 Vmss</span><span class="sxs-lookup"><span data-stu-id="87826-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="87826-122">取得所有以 "VMSS00" 開頭的訂閱中的 Vmss。</span><span class="sxs-lookup"><span data-stu-id="87826-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="87826-123">參數</span><span class="sxs-lookup"><span data-stu-id="87826-123">PARAMETERS</span></span>

### <span data-ttu-id="87826-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87826-124">-DefaultProfile</span></span>
<span data-ttu-id="87826-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87826-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87826-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="87826-126">-InstanceView</span></span>
<span data-ttu-id="87826-127">表示此 Cmdlet 只會取得虛擬機器縮放集的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="87826-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87826-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="87826-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="87826-129">表示此 Cmdlet 列出虛擬機器規模集的 os 升級歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="87826-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87826-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87826-130">-ResourceGroupName</span></span>
<span data-ttu-id="87826-131">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="87826-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="87826-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="87826-132">-VMScaleSetName</span></span>
<span data-ttu-id="87826-133">Species VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="87826-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="87826-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87826-134">CommonParameters</span></span>
<span data-ttu-id="87826-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87826-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87826-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="87826-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87826-137">輸入</span><span class="sxs-lookup"><span data-stu-id="87826-137">INPUTS</span></span>

### <span data-ttu-id="87826-138">System.object</span><span class="sxs-lookup"><span data-stu-id="87826-138">System.String</span></span>

## <span data-ttu-id="87826-139">輸出</span><span class="sxs-lookup"><span data-stu-id="87826-139">OUTPUTS</span></span>

### <span data-ttu-id="87826-140">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="87826-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="87826-141">筆記</span><span class="sxs-lookup"><span data-stu-id="87826-141">NOTES</span></span>

## <span data-ttu-id="87826-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="87826-142">RELATED LINKS</span></span>

[<span data-ttu-id="87826-143">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="87826-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="87826-144">移除-AzVmss</span><span class="sxs-lookup"><span data-stu-id="87826-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="87826-145">重新開機-AzVmss</span><span class="sxs-lookup"><span data-stu-id="87826-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="87826-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="87826-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="87826-147">開始-AzVmss</span><span class="sxs-lookup"><span data-stu-id="87826-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="87826-148">停止 AzVmss</span><span class="sxs-lookup"><span data-stu-id="87826-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="87826-149">更新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="87826-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


