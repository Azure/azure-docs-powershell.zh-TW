---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 966d176d9941c35b717012944257bc58b9f7ebdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917394"
---
# <span data-ttu-id="79ba7-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="79ba7-101">Get-AzVM</span></span>

## <span data-ttu-id="79ba7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="79ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="79ba7-103">獲得虛擬機器的屬性。</span><span class="sxs-lookup"><span data-stu-id="79ba7-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="79ba7-104">語法</span><span class="sxs-lookup"><span data-stu-id="79ba7-104">SYNTAX</span></span>

### <span data-ttu-id="79ba7-105">DefaultParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="79ba7-105">DefaultParamSet (Default)</span></span>
```
Get-AzVM [[-ResourceGroupName] <String>] [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79ba7-106">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="79ba7-106">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79ba7-107">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="79ba7-107">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79ba7-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="79ba7-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79ba7-109">描述</span><span class="sxs-lookup"><span data-stu-id="79ba7-109">DESCRIPTION</span></span>
<span data-ttu-id="79ba7-110">**Get-AzCMdlet** 會取得 Azure 虛擬機器的模型視圖或實例視圖。</span><span class="sxs-lookup"><span data-stu-id="79ba7-110">The **Get-AzVM** cmdlet gets the model view or the instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="79ba7-111">模型視圖是使用者指定的虛擬機器屬性。</span><span class="sxs-lookup"><span data-stu-id="79ba7-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="79ba7-112">實例視圖是虛擬機器的實例層級狀態。</span><span class="sxs-lookup"><span data-stu-id="79ba7-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="79ba7-113">指定 *狀態* 參數以取得虛擬機器的實例視圖，而不是預設的模型視圖。</span><span class="sxs-lookup"><span data-stu-id="79ba7-113">Specify the *Status* parameter to get the instance view of a virtual machine instead of the model view which is the default.</span></span>

## <span data-ttu-id="79ba7-114">例子</span><span class="sxs-lookup"><span data-stu-id="79ba7-114">EXAMPLES</span></span>

### <span data-ttu-id="79ba7-115">範例 1：取得模型和實例視圖屬性</span><span class="sxs-lookup"><span data-stu-id="79ba7-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"

ResourceGroupName        : ResourceGroup11
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/M
icrosoft.Compute/virtualMachines/VirtualMachine07
VmId                     : 00000000-0000-0000-0000-000000000000
Name                     : VirtualMachine07
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {"creationSource":"acs-VirtualMachine07"}
AvailabilitySetReference : {Id}
DiagnosticsProfile       : {BootDiagnostics}
Extensions               : {linuxdiagnostic, waitforleader}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, LinuxConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
```

<span data-ttu-id="79ba7-116">此命令會獲得名為 VirtualMachine07 之虛擬機器的模型視圖和實例視圖屬性。</span><span class="sxs-lookup"><span data-stu-id="79ba7-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="79ba7-117">範例 2：取得實例視圖屬性</span><span class="sxs-lookup"><span data-stu-id="79ba7-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status

ResourceGroupName       : ResourceGroup11
Name                    : VirtualMachine07
Disks[0]                :
  Name                  : VirtualMachine07-osdisk
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Time                : 3/1/2019 12:59:30 AM
Extensions[0]           :
  Name                  : linuxdiagnostic
  Type                  : Microsoft.OSTCExtensions.LinuxDiagnostic
  TypeHandlerVersion    : 2.3.9029
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Invalid config settings given: Empty storageAccountName. Install will proceed, but enable
can't proceed, in which case it's still considered a success as it's an external error.
Extensions[1]           :
  Name                  : waitforleader
  Type                  : Microsoft.OSTCExtensions.CustomScriptForLinux
  TypeHandlerVersion    : 1.5.4
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Command is finished.
---stdout---
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
PING leader.mesos (xxx.xx.x.x) 56(84) bytes of data.
64 bytes from xxx.xx.x.x: icmp_seq=1 ttl=64 time=0.022 ms

--- leader.mesos ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 0.022/0.022/0.022/0.000 ms
leader.mesos up

---errout---
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos


PlatformFaultDomain     : 0
PlatformUpdateDomain    : 0
VMAgent                 :
  VmAgentVersion        : 2.2.37
  ExtensionHandlers[0]  :
    Type                : Microsoft.OSTCExtensions.LinuxDiagnostic
    TypeHandlerVersion  : 2.3.9029
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  ExtensionHandlers[1]  :
    Type                : Microsoft.OSTCExtensions.CustomScriptForLinux
    TypeHandlerVersion  : 1.5.4
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Ready
    Message             : Guest Agent is running
    Time                : 3/1/2019 2:04:12 AM
Statuses[0]             :
  Code                  : ProvisioningState/succeeded
  Level                 : Info
  DisplayStatus         : Provisioning succeeded
  Time                  : 3/1/2019 1:01:57 AM
Statuses[1]             :
  Code                  : PowerState/running
  Level                 : Info
  DisplayStatus         : VM running
```

<span data-ttu-id="79ba7-118">此命令會獲得名為 VirtualMachine07 的虛擬機器屬性。</span><span class="sxs-lookup"><span data-stu-id="79ba7-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="79ba7-119">此命令會指定 *狀態* 參數。</span><span class="sxs-lookup"><span data-stu-id="79ba7-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="79ba7-120">因此，命令只會獲得實例視圖屬性。</span><span class="sxs-lookup"><span data-stu-id="79ba7-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="79ba7-121">範例 3：取得資源群組中所有虛擬機器的屬性</span><span class="sxs-lookup"><span data-stu-id="79ba7-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
ResourceGroup11     test1         eastus Standard_DS1_v2 Windows          test1
ResourceGroup11     test2         westus Standard_DS1_v2 Windows          test2
ResourceGroup11     test3         eastus Standard_DS1_v2 Windows          test3
```

<span data-ttu-id="79ba7-122">此命令會針對資源群組中名為 ResourceGroup11 的所有虛擬機器，獲得屬性。</span><span class="sxs-lookup"><span data-stu-id="79ba7-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="79ba7-123">範例 4：取得訂閱中所有的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="79ba7-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="79ba7-124">此命令會獲得訂閱中所有的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="79ba7-124">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="79ba7-125">範例 5：在位置中取得所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="79ba7-125">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzVM -Location "westus"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST2               test4         westus Standard_DS1_v2 Windows          test4
```

<span data-ttu-id="79ba7-126">此命令會獲得美國西部地區的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="79ba7-126">This command gets all the virtual machines in West US region.</span></span>

### <span data-ttu-id="79ba7-127">範例 6：使用篩選取得所有虛擬機器</span><span class="sxs-lookup"><span data-stu-id="79ba7-127">Example 6: Get all virtual machines using filtering</span></span>
```
PS C:\> Get-AzVM -Name test*

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="79ba7-128">此命令會獲得訂閱中以「測試」開始的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="79ba7-128">This command gets all the virtual machines in your subscription that start with "test".</span></span>

## <span data-ttu-id="79ba7-129">參數</span><span class="sxs-lookup"><span data-stu-id="79ba7-129">PARAMETERS</span></span>

### <span data-ttu-id="79ba7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ba7-130">-DefaultProfile</span></span>
<span data-ttu-id="79ba7-131">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="79ba7-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79ba7-132">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="79ba7-132">-DisplayHint</span></span>
<span data-ttu-id="79ba7-133">決定虛擬機器物件的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="79ba7-133">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="79ba7-134">有效的值為： -- 精簡：僅顯示頂層屬性 -- 展開：顯示所有層級的所有屬性</span><span class="sxs-lookup"><span data-stu-id="79ba7-134">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79ba7-135">-位置</span><span class="sxs-lookup"><span data-stu-id="79ba7-135">-Location</span></span>
<span data-ttu-id="79ba7-136">指定要列出虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="79ba7-136">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79ba7-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="79ba7-137">-Name</span></span>
<span data-ttu-id="79ba7-138">指定要取得之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="79ba7-138">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases: ResourceName, VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="79ba7-139">-NextLink</span><span class="sxs-lookup"><span data-stu-id="79ba7-139">-NextLink</span></span>
<span data-ttu-id="79ba7-140">指定下一個連結。</span><span class="sxs-lookup"><span data-stu-id="79ba7-140">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79ba7-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79ba7-141">-ResourceGroupName</span></span>
<span data-ttu-id="79ba7-142">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="79ba7-142">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="79ba7-143">-狀態</span><span class="sxs-lookup"><span data-stu-id="79ba7-143">-Status</span></span>
<span data-ttu-id="79ba7-144">表示此 Cmdlet 僅會獲得虛擬機器的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="79ba7-144">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ba7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ba7-145">CommonParameters</span></span>
<span data-ttu-id="79ba7-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="79ba7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ba7-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79ba7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ba7-148">輸入</span><span class="sxs-lookup"><span data-stu-id="79ba7-148">INPUTS</span></span>

### <span data-ttu-id="79ba7-149">System.String</span><span class="sxs-lookup"><span data-stu-id="79ba7-149">System.String</span></span>

### <span data-ttu-id="79ba7-150">System.Uri</span><span class="sxs-lookup"><span data-stu-id="79ba7-150">System.Uri</span></span>

### <span data-ttu-id="79ba7-151">Microsoft.Azure.Commands.Compute.models.DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="79ba7-151">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="79ba7-152">輸出</span><span class="sxs-lookup"><span data-stu-id="79ba7-152">OUTPUTS</span></span>

### <span data-ttu-id="79ba7-153">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="79ba7-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="79ba7-154">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="79ba7-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="79ba7-155">筆記</span><span class="sxs-lookup"><span data-stu-id="79ba7-155">NOTES</span></span>

## <span data-ttu-id="79ba7-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="79ba7-156">RELATED LINKS</span></span>

[<span data-ttu-id="79ba7-157">New-AzMS</span><span class="sxs-lookup"><span data-stu-id="79ba7-157">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="79ba7-158">Remove-AzMS</span><span class="sxs-lookup"><span data-stu-id="79ba7-158">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="79ba7-159">Restart-AzMS</span><span class="sxs-lookup"><span data-stu-id="79ba7-159">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="79ba7-160">Start-AzMS</span><span class="sxs-lookup"><span data-stu-id="79ba7-160">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="79ba7-161">Stop-AzMS</span><span class="sxs-lookup"><span data-stu-id="79ba7-161">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="79ba7-162">Update-AzMS</span><span class="sxs-lookup"><span data-stu-id="79ba7-162">Update-AzVM</span></span>](./Update-AzVM.md)


