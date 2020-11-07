---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
ms.openlocfilehash: 46058901188b99eb30d088e2ea784fdc0df8d782
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802102"
---
# <span data-ttu-id="02ab3-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="02ab3-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="02ab3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="02ab3-103">從 VMSS 中移除網路介面設定。</span><span class="sxs-lookup"><span data-stu-id="02ab3-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02ab3-104">句法</span><span class="sxs-lookup"><span data-stu-id="02ab3-104">SYNTAX</span></span>

### <span data-ttu-id="02ab3-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="02ab3-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02ab3-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02ab3-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02ab3-107">說明</span><span class="sxs-lookup"><span data-stu-id="02ab3-107">DESCRIPTION</span></span>
<span data-ttu-id="02ab3-108">**AzureRmVmssNetworkInterfaceConfiguration** Cmdlet 會從虛擬電腦規模集 (VMSS) 中移除網路介面配置。</span><span class="sxs-lookup"><span data-stu-id="02ab3-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="02ab3-109">示例</span><span class="sxs-lookup"><span data-stu-id="02ab3-109">EXAMPLES</span></span>

### <span data-ttu-id="02ab3-110">範例1：移除介面配置</span><span class="sxs-lookup"><span data-stu-id="02ab3-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="02ab3-111">第一個命令會使用 Get-AzureRmVmss Cmdlet 來取得 VMSS，然後將它儲存在 $VMSS 變數中。</span><span class="sxs-lookup"><span data-stu-id="02ab3-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="02ab3-112">第二個命令會從 $VMSS 的集合中移除名為 ContosoVmssInterface02 的網路介面設定。</span><span class="sxs-lookup"><span data-stu-id="02ab3-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="02ab3-113">參數</span><span class="sxs-lookup"><span data-stu-id="02ab3-113">PARAMETERS</span></span>

### <span data-ttu-id="02ab3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ab3-114">-DefaultProfile</span></span>
<span data-ttu-id="02ab3-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="02ab3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02ab3-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="02ab3-116">-Id</span></span>
<span data-ttu-id="02ab3-117">指定此 Cmdlet 移除之網路介面設定的 ID。</span><span class="sxs-lookup"><span data-stu-id="02ab3-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ab3-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="02ab3-118">-Name</span></span>
<span data-ttu-id="02ab3-119">指定此 Cmdlet 移除的網路介面配置名稱。</span><span class="sxs-lookup"><span data-stu-id="02ab3-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ab3-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="02ab3-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="02ab3-121">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="02ab3-121">Specifies the VMSS object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02ab3-122">-確認</span><span class="sxs-lookup"><span data-stu-id="02ab3-122">-Confirm</span></span>
<span data-ttu-id="02ab3-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="02ab3-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ab3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02ab3-124">-WhatIf</span></span>
<span data-ttu-id="02ab3-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02ab3-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02ab3-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02ab3-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ab3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ab3-127">CommonParameters</span></span>
<span data-ttu-id="02ab3-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02ab3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ab3-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02ab3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ab3-130">輸入</span><span class="sxs-lookup"><span data-stu-id="02ab3-130">INPUTS</span></span>

### <span data-ttu-id="02ab3-131">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="02ab3-131">VirtualMachineScaleSet</span></span>
<span data-ttu-id="02ab3-132">形參 "VirtualMachineScaleSet" 接受管線中 "VirtualMachineScaleSet" 類型的值</span><span class="sxs-lookup"><span data-stu-id="02ab3-132">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="02ab3-133">輸出</span><span class="sxs-lookup"><span data-stu-id="02ab3-133">OUTPUTS</span></span>

### <span data-ttu-id="02ab3-134">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="02ab3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="02ab3-135">筆記</span><span class="sxs-lookup"><span data-stu-id="02ab3-135">NOTES</span></span>

## <span data-ttu-id="02ab3-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="02ab3-136">RELATED LINKS</span></span>

[<span data-ttu-id="02ab3-137">附加 AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="02ab3-137">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="02ab3-138">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="02ab3-138">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


