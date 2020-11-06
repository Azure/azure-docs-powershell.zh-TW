---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 32f3cfa8f9e27a9b54e0b103ec09195946ac3e55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622821"
---
# <span data-ttu-id="28efc-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="28efc-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="28efc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28efc-102">SYNOPSIS</span></span>
<span data-ttu-id="28efc-103">將診斷延伸新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="28efc-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="28efc-104">句法</span><span class="sxs-lookup"><span data-stu-id="28efc-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28efc-105">說明</span><span class="sxs-lookup"><span data-stu-id="28efc-105">DESCRIPTION</span></span>
<span data-ttu-id="28efc-106">**AzVmssDiagnosticsExtension** Cmdlet 會將診斷延伸新增至虛擬電腦比例集 (VMSS) 實例。</span><span class="sxs-lookup"><span data-stu-id="28efc-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="28efc-107">示例</span><span class="sxs-lookup"><span data-stu-id="28efc-107">EXAMPLES</span></span>

### <span data-ttu-id="28efc-108">範例1：在 VMSS 中新增診斷延伸</span><span class="sxs-lookup"><span data-stu-id="28efc-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="28efc-109">這個命令會將診斷延伸新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="28efc-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="28efc-110">參數</span><span class="sxs-lookup"><span data-stu-id="28efc-110">PARAMETERS</span></span>

### <span data-ttu-id="28efc-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="28efc-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="28efc-112">指示此 Cmdlet 是否允許 Azure 來賓代理程式自動將延伸更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="28efc-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28efc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28efc-113">-DefaultProfile</span></span>
<span data-ttu-id="28efc-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="28efc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28efc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="28efc-115">-Force</span></span>
<span data-ttu-id="28efc-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="28efc-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28efc-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="28efc-117">-Name</span></span>
<span data-ttu-id="28efc-118">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="28efc-118">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28efc-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="28efc-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="28efc-120">指定私人設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="28efc-120">Specifies the path of the private configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28efc-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="28efc-121">-SettingFilePath</span></span>
<span data-ttu-id="28efc-122">指定公用設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="28efc-122">Specifies the path of the public configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28efc-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="28efc-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="28efc-124">指定要用於此 VMSS 的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="28efc-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="28efc-125">若要取得版本，請執行 [AzVMExtensionImage](./Get-AzVMExtensionImage.md) Cmdlet 與 *PublisherName* 參數的值，以及針對 *Type* 參數 IaaSDiagnostics 的。</span><span class="sxs-lookup"><span data-stu-id="28efc-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28efc-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="28efc-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="28efc-127">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="28efc-127">Specify the VMSS object.</span></span>
<span data-ttu-id="28efc-128">您可以使用 [新的-AzVmssConfig](./New-AzVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="28efc-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="28efc-129">-確認</span><span class="sxs-lookup"><span data-stu-id="28efc-129">-Confirm</span></span>
<span data-ttu-id="28efc-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="28efc-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28efc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28efc-131">-WhatIf</span></span>
<span data-ttu-id="28efc-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28efc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28efc-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28efc-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28efc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28efc-134">CommonParameters</span></span>
<span data-ttu-id="28efc-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28efc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28efc-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="28efc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28efc-137">輸入</span><span class="sxs-lookup"><span data-stu-id="28efc-137">INPUTS</span></span>

### <span data-ttu-id="28efc-138">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="28efc-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="28efc-139">System.object</span><span class="sxs-lookup"><span data-stu-id="28efc-139">System.String</span></span>

### <span data-ttu-id="28efc-140">System.object</span><span class="sxs-lookup"><span data-stu-id="28efc-140">System.Boolean</span></span>

## <span data-ttu-id="28efc-141">輸出</span><span class="sxs-lookup"><span data-stu-id="28efc-141">OUTPUTS</span></span>

### <span data-ttu-id="28efc-142">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="28efc-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="28efc-143">筆記</span><span class="sxs-lookup"><span data-stu-id="28efc-143">NOTES</span></span>

## <span data-ttu-id="28efc-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="28efc-144">RELATED LINKS</span></span>

[<span data-ttu-id="28efc-145">附加 AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="28efc-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="28efc-146">移除-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="28efc-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="28efc-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="28efc-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)