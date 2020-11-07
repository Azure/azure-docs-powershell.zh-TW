---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 85967c0627a2b2d1eb249a67114297a6aacf3c1e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966513"
---
# <span data-ttu-id="32d06-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="32d06-101">Get-AzVM</span></span>

## <span data-ttu-id="32d06-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32d06-102">SYNOPSIS</span></span>
<span data-ttu-id="32d06-103">取得虛擬機器的屬性。</span><span class="sxs-lookup"><span data-stu-id="32d06-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="32d06-104">句法</span><span class="sxs-lookup"><span data-stu-id="32d06-104">SYNTAX</span></span>

### <span data-ttu-id="32d06-105">DefaultParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="32d06-105">DefaultParamSet (Default)</span></span>
```
Get-AzVM [[-ResourceGroupName] <String>] [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32d06-106">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="32d06-106">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32d06-107">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="32d06-107">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32d06-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="32d06-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32d06-109">說明</span><span class="sxs-lookup"><span data-stu-id="32d06-109">DESCRIPTION</span></span>
<span data-ttu-id="32d06-110">**AzVM** Cmdlet 會取得 Azure 虛擬機器的 [模型] 視圖和 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="32d06-110">The **Get-AzVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="32d06-111">模型視圖是使用者指定的虛擬機器屬性。</span><span class="sxs-lookup"><span data-stu-id="32d06-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="32d06-112">[實例] 視圖是虛擬機器的實例層級狀態。</span><span class="sxs-lookup"><span data-stu-id="32d06-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="32d06-113">指定 *Status* 參數，只取得虛擬機器的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="32d06-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="32d06-114">示例</span><span class="sxs-lookup"><span data-stu-id="32d06-114">EXAMPLES</span></span>

### <span data-ttu-id="32d06-115">範例1：取得模型和實例視圖屬性</span><span class="sxs-lookup"><span data-stu-id="32d06-115">Example 1: Get model and instance view properties</span></span>
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

<span data-ttu-id="32d06-116">這個命令會取得名為 VirtualMachine07 的虛擬機器的模型視圖和實例視圖屬性。</span><span class="sxs-lookup"><span data-stu-id="32d06-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="32d06-117">範例2：取得實例視圖屬性</span><span class="sxs-lookup"><span data-stu-id="32d06-117">Example 2: Get instance view properties</span></span>
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

<span data-ttu-id="32d06-118">這個命令會取得名為 VirtualMachine07 的虛擬機器的屬性。</span><span class="sxs-lookup"><span data-stu-id="32d06-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="32d06-119">這個命令會指定 *Status* 參數。</span><span class="sxs-lookup"><span data-stu-id="32d06-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="32d06-120">因此，命令只會取得實例視圖屬性。</span><span class="sxs-lookup"><span data-stu-id="32d06-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="32d06-121">範例3：取得資源群組中所有虛擬機器的屬性</span><span class="sxs-lookup"><span data-stu-id="32d06-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
ResourceGroup11     test1         eastus Standard_DS1_v2 Windows          test1
ResourceGroup11     test2         westus Standard_DS1_v2 Windows          test2
ResourceGroup11     test3         eastus Standard_DS1_v2 Windows          test3
```

<span data-ttu-id="32d06-122">這個命令會取得名為 ResourceGroup11 之資源群組中所有虛擬機器的屬性。</span><span class="sxs-lookup"><span data-stu-id="32d06-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="32d06-123">範例4：取得您訂閱中的所有虛擬機器</span><span class="sxs-lookup"><span data-stu-id="32d06-123">Example 4: Get all virtual machines in your subscription</span></span>
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

<span data-ttu-id="32d06-124">這個命令會取得您訂閱中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="32d06-124">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="32d06-125">範例5：取得位置中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="32d06-125">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzVM -Location "westus"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST2               test4         westus Standard_DS1_v2 Windows          test4
```

<span data-ttu-id="32d06-126">這個命令會取得西部美區域中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="32d06-126">This command gets all the virtual machines in West US region.</span></span>

### <span data-ttu-id="32d06-127">範例6：使用篩選取得所有虛擬機器</span><span class="sxs-lookup"><span data-stu-id="32d06-127">Example 6: Get all virtual machines using filtering</span></span>
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

<span data-ttu-id="32d06-128">這個命令會取得訂閱中以「test」開頭的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="32d06-128">This command gets all the virtual machines in your subscription that start with "test".</span></span>

## <span data-ttu-id="32d06-129">參數</span><span class="sxs-lookup"><span data-stu-id="32d06-129">PARAMETERS</span></span>

### <span data-ttu-id="32d06-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32d06-130">-DefaultProfile</span></span>
<span data-ttu-id="32d06-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="32d06-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32d06-132">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="32d06-132">-DisplayHint</span></span>
<span data-ttu-id="32d06-133">決定虛擬機器物件的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="32d06-133">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="32d06-134">有效值為：-精簡：只顯示最上層屬性--展開：顯示所有層級中的所有屬性</span><span class="sxs-lookup"><span data-stu-id="32d06-134">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

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

### <span data-ttu-id="32d06-135">-位置</span><span class="sxs-lookup"><span data-stu-id="32d06-135">-Location</span></span>
<span data-ttu-id="32d06-136">指定虛擬機器的清單位置。</span><span class="sxs-lookup"><span data-stu-id="32d06-136">Specifies a location for the virtual machines to list.</span></span>

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

### <span data-ttu-id="32d06-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="32d06-137">-Name</span></span>
<span data-ttu-id="32d06-138">指定要取得的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="32d06-138">Specifies the name of the virtual machine to get.</span></span>

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

### <span data-ttu-id="32d06-139">-NextLink</span><span class="sxs-lookup"><span data-stu-id="32d06-139">-NextLink</span></span>
<span data-ttu-id="32d06-140">指定 [下一步] 連結。</span><span class="sxs-lookup"><span data-stu-id="32d06-140">Specifies the next link.</span></span>

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

### <span data-ttu-id="32d06-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32d06-141">-ResourceGroupName</span></span>
<span data-ttu-id="32d06-142">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="32d06-142">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="32d06-143">-狀態</span><span class="sxs-lookup"><span data-stu-id="32d06-143">-Status</span></span>
<span data-ttu-id="32d06-144">表示此 Cmdlet 只會取得虛擬機器的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="32d06-144">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="32d06-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d06-145">CommonParameters</span></span>
<span data-ttu-id="32d06-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32d06-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d06-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="32d06-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d06-148">輸入</span><span class="sxs-lookup"><span data-stu-id="32d06-148">INPUTS</span></span>

### <span data-ttu-id="32d06-149">System.object</span><span class="sxs-lookup"><span data-stu-id="32d06-149">System.String</span></span>

### <span data-ttu-id="32d06-150">系統 Uri</span><span class="sxs-lookup"><span data-stu-id="32d06-150">System.Uri</span></span>

### <span data-ttu-id="32d06-151">DisplayHintType 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="32d06-151">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="32d06-152">輸出</span><span class="sxs-lookup"><span data-stu-id="32d06-152">OUTPUTS</span></span>

### <span data-ttu-id="32d06-153">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="32d06-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="32d06-154">PSVirtualMachineInstanceView 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="32d06-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="32d06-155">筆記</span><span class="sxs-lookup"><span data-stu-id="32d06-155">NOTES</span></span>

## <span data-ttu-id="32d06-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="32d06-156">RELATED LINKS</span></span>

[<span data-ttu-id="32d06-157">新-AzVM</span><span class="sxs-lookup"><span data-stu-id="32d06-157">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="32d06-158">移除-AzVM</span><span class="sxs-lookup"><span data-stu-id="32d06-158">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="32d06-159">重新開機-AzVM</span><span class="sxs-lookup"><span data-stu-id="32d06-159">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="32d06-160">開始-AzVM</span><span class="sxs-lookup"><span data-stu-id="32d06-160">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="32d06-161">停止 AzVM</span><span class="sxs-lookup"><span data-stu-id="32d06-161">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="32d06-162">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="32d06-162">Update-AzVM</span></span>](./Update-AzVM.md)


