---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: 33be258858a6ace456b7aa3c5b25594a373ccfd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917381"
---
# <span data-ttu-id="a2c41-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a2c41-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="a2c41-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a2c41-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c41-103">在虛擬機器上安裝虛擬機器擴充功能的屬性。</span><span class="sxs-lookup"><span data-stu-id="a2c41-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="a2c41-104">語法</span><span class="sxs-lookup"><span data-stu-id="a2c41-104">SYNTAX</span></span>

### <span data-ttu-id="a2c41-105">GetExtensionParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a2c41-105">GetExtensionParameterSet (Default)</span></span>
```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2c41-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2c41-106">VMParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-VMObject <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2c41-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2c41-107">ResourceIdParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-ResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2c41-108">描述</span><span class="sxs-lookup"><span data-stu-id="a2c41-108">DESCRIPTION</span></span>
<span data-ttu-id="a2c41-109">**Get-Az VIRTUALExtension** Cmdlet 會取得安裝在虛擬機器上的虛擬機器擴充功能的屬性。</span><span class="sxs-lookup"><span data-stu-id="a2c41-109">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="a2c41-110">指定要取得屬性的副檔名。</span><span class="sxs-lookup"><span data-stu-id="a2c41-110">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="a2c41-111">如果只要取得擴充功能的實例視圖，請指定狀態參數。</span><span class="sxs-lookup"><span data-stu-id="a2c41-111">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="a2c41-112">例子</span><span class="sxs-lookup"><span data-stu-id="a2c41-112">EXAMPLES</span></span>

### <span data-ttu-id="a2c41-113">範例 1：取得擴充功能的屬性</span><span class="sxs-lookup"><span data-stu-id="a2c41-113">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="a2c41-114">此命令會針對資源群組 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器上名為 CustomScriptExtension 的副檔名，獲得屬性。</span><span class="sxs-lookup"><span data-stu-id="a2c41-114">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="a2c41-115">範例 2：取得擴充功能的實例視圖</span><span class="sxs-lookup"><span data-stu-id="a2c41-115">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                : {Microsoft.Azure.Management.Compute.Models.InstanceViewStatus}
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="a2c41-116">此命令會針對資源群組 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器上名為 CustomScriptExtension 的副檔名，獲得實例視圖。</span><span class="sxs-lookup"><span data-stu-id="a2c41-116">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="a2c41-117">範例 3：在 VM 上安裝所有擴充功能</span><span class="sxs-lookup"><span data-stu-id="a2c41-117">Example 3: Get all extensions installed on a VM</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

### <span data-ttu-id="a2c41-118">範例 4：使用 VM 參數取得擴充功能的屬性</span><span class="sxs-lookup"><span data-stu-id="a2c41-118">Example 4: Get properties of an extension using the VM parameter</span></span>
```
PS C:\> $vm = Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine22"
PS C:\> Get-AzVMExtension -VM $vm

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="a2c41-119">此命令會獲得在資源群組 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器上安裝的擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="a2c41-119">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="a2c41-120">參數</span><span class="sxs-lookup"><span data-stu-id="a2c41-120">PARAMETERS</span></span>

### <span data-ttu-id="a2c41-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c41-121">-DefaultProfile</span></span>
<span data-ttu-id="a2c41-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2c41-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2c41-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2c41-123">-Name</span></span>
<span data-ttu-id="a2c41-124">指定副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2c41-124">Specifies the name of an extension.</span></span>
<span data-ttu-id="a2c41-125">此 Cmdlet 會針對此參數指定的擴充功能，獲得屬性。</span><span class="sxs-lookup"><span data-stu-id="a2c41-125">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c41-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c41-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2c41-127">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2c41-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c41-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c41-128">-ResourceId</span></span>
<span data-ttu-id="a2c41-129">指定擴充功能所上之虛擬機器物件的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2c41-129">Resource Id specifying the virtual machine object the extension is on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c41-130">-狀態</span><span class="sxs-lookup"><span data-stu-id="a2c41-130">-Status</span></span>
<span data-ttu-id="a2c41-131">表示此 Cmdlet 僅會獲得擴充功能的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="a2c41-131">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c41-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="a2c41-132">-VMName</span></span>
<span data-ttu-id="a2c41-133">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2c41-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a2c41-134">此 Cmdlet 會從此參數指定的虛擬機器中，獲得擴充功能的屬性。</span><span class="sxs-lookup"><span data-stu-id="a2c41-134">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c41-135">-VMObject</span><span class="sxs-lookup"><span data-stu-id="a2c41-135">-VMObject</span></span>
<span data-ttu-id="a2c41-136">指定擴充功能所位於的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="a2c41-136">Specifies the virtual machine object the extension is on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c41-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c41-137">CommonParameters</span></span>
<span data-ttu-id="a2c41-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a2c41-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c41-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2c41-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c41-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a2c41-140">INPUTS</span></span>

### <span data-ttu-id="a2c41-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a2c41-141">System.String</span></span>

### <span data-ttu-id="a2c41-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a2c41-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a2c41-143">輸出</span><span class="sxs-lookup"><span data-stu-id="a2c41-143">OUTPUTS</span></span>

### <span data-ttu-id="a2c41-144">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="a2c41-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="a2c41-145">筆記</span><span class="sxs-lookup"><span data-stu-id="a2c41-145">NOTES</span></span>

## <span data-ttu-id="a2c41-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2c41-146">RELATED LINKS</span></span>

[<span data-ttu-id="a2c41-147">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a2c41-147">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="a2c41-148">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a2c41-148">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


