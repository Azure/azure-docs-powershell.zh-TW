---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 3c9e19c30d89d73a52be4defd18166f88b700889
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910750"
---
# <span data-ttu-id="8c28a-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c28a-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="8c28a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8c28a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c28a-103">從 VMSS 移除網路介面組。</span><span class="sxs-lookup"><span data-stu-id="8c28a-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="8c28a-104">語法</span><span class="sxs-lookup"><span data-stu-id="8c28a-104">SYNTAX</span></span>

### <span data-ttu-id="8c28a-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c28a-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c28a-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c28a-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c28a-107">描述</span><span class="sxs-lookup"><span data-stu-id="8c28a-107">DESCRIPTION</span></span>
<span data-ttu-id="8c28a-108">**Remove-Az VmssNetworkInterfaceConfiguration Cmdlet** 會從虛擬機器縮放集 (VMSS) 移除網路介面設定。</span><span class="sxs-lookup"><span data-stu-id="8c28a-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8c28a-109">例子</span><span class="sxs-lookup"><span data-stu-id="8c28a-109">EXAMPLES</span></span>

### <span data-ttu-id="8c28a-110">範例 1：移除介面組</span><span class="sxs-lookup"><span data-stu-id="8c28a-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="8c28a-111">第一個命令會使用 Get-AzVmss Cmdlet 來獲得 VMSS，然後將它儲存在 $VMSS 變數中。</span><span class="sxs-lookup"><span data-stu-id="8c28a-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="8c28a-112">第二個命令會從 $VMSS 中的集合移除名為 ContosoEvssInterface02 的網路介面$VMSS。</span><span class="sxs-lookup"><span data-stu-id="8c28a-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="8c28a-113">參數</span><span class="sxs-lookup"><span data-stu-id="8c28a-113">PARAMETERS</span></span>

### <span data-ttu-id="8c28a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c28a-114">-DefaultProfile</span></span>
<span data-ttu-id="8c28a-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c28a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c28a-116">-Id</span><span class="sxs-lookup"><span data-stu-id="8c28a-116">-Id</span></span>
<span data-ttu-id="8c28a-117">指定此 Cmdlet 移除的網路介面群組原則識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c28a-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c28a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c28a-118">-Name</span></span>
<span data-ttu-id="8c28a-119">指定此 Cmdlet 移除的網路介面組配置名稱。</span><span class="sxs-lookup"><span data-stu-id="8c28a-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c28a-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8c28a-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8c28a-121">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="8c28a-121">Specifies the VMSS object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c28a-122">-確認</span><span class="sxs-lookup"><span data-stu-id="8c28a-122">-Confirm</span></span>
<span data-ttu-id="8c28a-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8c28a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c28a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c28a-124">-WhatIf</span></span>
<span data-ttu-id="8c28a-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c28a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c28a-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c28a-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c28a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c28a-127">CommonParameters</span></span>
<span data-ttu-id="8c28a-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8c28a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c28a-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c28a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c28a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8c28a-130">INPUTS</span></span>

### <span data-ttu-id="8c28a-131">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8c28a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8c28a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8c28a-132">System.String</span></span>

## <span data-ttu-id="8c28a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="8c28a-133">OUTPUTS</span></span>

### <span data-ttu-id="8c28a-134">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8c28a-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8c28a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="8c28a-135">NOTES</span></span>

## <span data-ttu-id="8c28a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c28a-136">RELATED LINKS</span></span>

[<span data-ttu-id="8c28a-137">Add-AzEvssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c28a-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="8c28a-138">Get-AzEvss</span><span class="sxs-lookup"><span data-stu-id="8c28a-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


