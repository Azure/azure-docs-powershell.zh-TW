---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: ca9693f715d72366a6cc78030d0a8328bf0abc50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141302"
---
# <span data-ttu-id="d90d8-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d90d8-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="d90d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d90d8-102">SYNOPSIS</span></span>
<span data-ttu-id="d90d8-103">取得在虛擬機器上安裝之虛擬機器延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="d90d8-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="d90d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="d90d8-104">SYNTAX</span></span>

### <span data-ttu-id="d90d8-105">GetExtensionParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d90d8-105">GetExtensionParameterSet (Default)</span></span>
```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d90d8-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="d90d8-106">VMParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-VMObject <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d90d8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d90d8-107">ResourceIdParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-ResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d90d8-108">說明</span><span class="sxs-lookup"><span data-stu-id="d90d8-108">DESCRIPTION</span></span>
<span data-ttu-id="d90d8-109">**AzVMExtension** Cmdlet 會取得在虛擬機器上安裝的虛擬機器延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="d90d8-109">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="d90d8-110">指定要取得屬性之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="d90d8-110">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="d90d8-111">若只要取得延伸的 [實例] 視圖，請指定 Status 參數。</span><span class="sxs-lookup"><span data-stu-id="d90d8-111">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="d90d8-112">示例</span><span class="sxs-lookup"><span data-stu-id="d90d8-112">EXAMPLES</span></span>

### <span data-ttu-id="d90d8-113">範例1：取得延伸的屬性</span><span class="sxs-lookup"><span data-stu-id="d90d8-113">Example 1: Get properties of an extension</span></span>
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

<span data-ttu-id="d90d8-114">這個命令會取得「資源群組」 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器上名為 CustomScriptExtension 的副檔名的屬性。</span><span class="sxs-lookup"><span data-stu-id="d90d8-114">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="d90d8-115">範例2：取得延伸的實例視圖</span><span class="sxs-lookup"><span data-stu-id="d90d8-115">Example 2: Get instance view of an extension</span></span>
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

<span data-ttu-id="d90d8-116">這個命令會針對資源群組 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器上名為 CustomScriptExtension 的副檔名取得實例視圖。</span><span class="sxs-lookup"><span data-stu-id="d90d8-116">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="d90d8-117">範例3：取得已安裝在 VM 上的所有擴充功能</span><span class="sxs-lookup"><span data-stu-id="d90d8-117">Example 3: Get all extensions installed on a VM</span></span>
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

### <span data-ttu-id="d90d8-118">範例4：使用 VM 參數取得延伸的屬性</span><span class="sxs-lookup"><span data-stu-id="d90d8-118">Example 4: Get properties of an extension using the VM parameter</span></span>
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

<span data-ttu-id="d90d8-119">這個命令會在資源群組 ResourceGroup11 中取得名為 VirtualMachine22 的虛擬機器上所安裝的延伸清單。</span><span class="sxs-lookup"><span data-stu-id="d90d8-119">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="d90d8-120">參數</span><span class="sxs-lookup"><span data-stu-id="d90d8-120">PARAMETERS</span></span>

### <span data-ttu-id="d90d8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d90d8-121">-DefaultProfile</span></span>
<span data-ttu-id="d90d8-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d90d8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d90d8-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="d90d8-123">-Name</span></span>
<span data-ttu-id="d90d8-124">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="d90d8-124">Specifies the name of an extension.</span></span>
<span data-ttu-id="d90d8-125">這個 Cmdlet 會取得此參數指定之副檔名的屬性。</span><span class="sxs-lookup"><span data-stu-id="d90d8-125">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="d90d8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d90d8-126">-ResourceGroupName</span></span>
<span data-ttu-id="d90d8-127">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d90d8-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d90d8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d90d8-128">-ResourceId</span></span>
<span data-ttu-id="d90d8-129">資源識別碼，指定延伸所在的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="d90d8-129">Resource Id specifying the virtual machine object the extension is on.</span></span>

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

### <span data-ttu-id="d90d8-130">-狀態</span><span class="sxs-lookup"><span data-stu-id="d90d8-130">-Status</span></span>
<span data-ttu-id="d90d8-131">表示此 Cmdlet 只會取得延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="d90d8-131">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="d90d8-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="d90d8-132">-VMName</span></span>
<span data-ttu-id="d90d8-133">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d90d8-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d90d8-134">這個 Cmdlet 會從虛擬機器中取得此參數指定之延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="d90d8-134">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d90d8-135">-VMObject</span><span class="sxs-lookup"><span data-stu-id="d90d8-135">-VMObject</span></span>
<span data-ttu-id="d90d8-136">指定副檔名所在的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="d90d8-136">Specifies the virtual machine object the extension is on.</span></span>

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

### <span data-ttu-id="d90d8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d90d8-137">CommonParameters</span></span>
<span data-ttu-id="d90d8-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d90d8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d90d8-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d90d8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d90d8-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d90d8-140">INPUTS</span></span>

### <span data-ttu-id="d90d8-141">System.object</span><span class="sxs-lookup"><span data-stu-id="d90d8-141">System.String</span></span>

### <span data-ttu-id="d90d8-142">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="d90d8-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d90d8-143">輸出</span><span class="sxs-lookup"><span data-stu-id="d90d8-143">OUTPUTS</span></span>

### <span data-ttu-id="d90d8-144">PSVirtualMachineExtension 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="d90d8-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="d90d8-145">筆記</span><span class="sxs-lookup"><span data-stu-id="d90d8-145">NOTES</span></span>

## <span data-ttu-id="d90d8-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="d90d8-146">RELATED LINKS</span></span>

[<span data-ttu-id="d90d8-147">移除-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d90d8-147">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="d90d8-148">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d90d8-148">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


