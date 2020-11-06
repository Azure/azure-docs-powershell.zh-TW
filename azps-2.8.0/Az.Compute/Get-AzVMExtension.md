---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: f861465fcc9f27f71142ffd4e49935039f3da9c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613381"
---
# <span data-ttu-id="84a9b-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="84a9b-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="84a9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="84a9b-103">取得在虛擬機器上安裝之虛擬機器延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="84a9b-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="84a9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="84a9b-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84a9b-105">說明</span><span class="sxs-lookup"><span data-stu-id="84a9b-105">DESCRIPTION</span></span>
<span data-ttu-id="84a9b-106">**AzVMExtension** Cmdlet 會取得在虛擬機器上安裝的虛擬機器延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="84a9b-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="84a9b-107">指定要取得屬性之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="84a9b-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="84a9b-108">若只要取得延伸的 [實例] 視圖，請指定 Status 參數。</span><span class="sxs-lookup"><span data-stu-id="84a9b-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="84a9b-109">示例</span><span class="sxs-lookup"><span data-stu-id="84a9b-109">EXAMPLES</span></span>

### <span data-ttu-id="84a9b-110">範例1：取得延伸的屬性</span><span class="sxs-lookup"><span data-stu-id="84a9b-110">Example 1: Get properties of an extension</span></span>
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

<span data-ttu-id="84a9b-111">這個命令會取得「資源群組」 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器上名為 CustomScriptExtension 的副檔名的屬性。</span><span class="sxs-lookup"><span data-stu-id="84a9b-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="84a9b-112">範例2：取得延伸的實例視圖</span><span class="sxs-lookup"><span data-stu-id="84a9b-112">Example 2: Get instance view of an extension</span></span>
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

<span data-ttu-id="84a9b-113">這個命令會針對資源群組 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器上名為 CustomScriptExtension 的副檔名取得實例視圖。</span><span class="sxs-lookup"><span data-stu-id="84a9b-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="84a9b-114">範例3：取得已安裝在 VM 上的所有擴充功能</span><span class="sxs-lookup"><span data-stu-id="84a9b-114">Example 3: Get all extensions installed on a VM</span></span>
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

<span data-ttu-id="84a9b-115">這個命令會在資源群組 ResourceGroup11 中取得名為 VirtualMachine22 的虛擬機器上所安裝的延伸清單。</span><span class="sxs-lookup"><span data-stu-id="84a9b-115">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="84a9b-116">參數</span><span class="sxs-lookup"><span data-stu-id="84a9b-116">PARAMETERS</span></span>

### <span data-ttu-id="84a9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a9b-117">-DefaultProfile</span></span>
<span data-ttu-id="84a9b-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84a9b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84a9b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="84a9b-119">-Name</span></span>
<span data-ttu-id="84a9b-120">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="84a9b-120">Specifies the name of an extension.</span></span>
<span data-ttu-id="84a9b-121">這個 Cmdlet 會取得此參數指定之副檔名的屬性。</span><span class="sxs-lookup"><span data-stu-id="84a9b-121">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84a9b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a9b-122">-ResourceGroupName</span></span>
<span data-ttu-id="84a9b-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="84a9b-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84a9b-124">-狀態</span><span class="sxs-lookup"><span data-stu-id="84a9b-124">-Status</span></span>
<span data-ttu-id="84a9b-125">表示此 Cmdlet 只會取得延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="84a9b-125">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="84a9b-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="84a9b-126">-VMName</span></span>
<span data-ttu-id="84a9b-127">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="84a9b-127">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="84a9b-128">這個 Cmdlet 會從虛擬機器中取得此參數指定之延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="84a9b-128">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84a9b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a9b-129">CommonParameters</span></span>
<span data-ttu-id="84a9b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84a9b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a9b-131">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="84a9b-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a9b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="84a9b-132">INPUTS</span></span>

### <span data-ttu-id="84a9b-133">System.object</span><span class="sxs-lookup"><span data-stu-id="84a9b-133">System.String</span></span>

### <span data-ttu-id="84a9b-134">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="84a9b-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="84a9b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="84a9b-135">OUTPUTS</span></span>

### <span data-ttu-id="84a9b-136">PSVirtualMachineExtension 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="84a9b-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="84a9b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="84a9b-137">NOTES</span></span>

## <span data-ttu-id="84a9b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="84a9b-138">RELATED LINKS</span></span>

[<span data-ttu-id="84a9b-139">移除-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="84a9b-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="84a9b-140">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="84a9b-140">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

