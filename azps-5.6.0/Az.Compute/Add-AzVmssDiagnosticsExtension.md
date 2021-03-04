---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 93e9f660b0667286e5ce8c799b5404caae0ba0c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906313"
---
# <span data-ttu-id="bc962-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bc962-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="bc962-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bc962-102">SYNOPSIS</span></span>
<span data-ttu-id="bc962-103">將診斷擴充功能新增到 VMSS。</span><span class="sxs-lookup"><span data-stu-id="bc962-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="bc962-104">語法</span><span class="sxs-lookup"><span data-stu-id="bc962-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc962-105">描述</span><span class="sxs-lookup"><span data-stu-id="bc962-105">DESCRIPTION</span></span>
<span data-ttu-id="bc962-106">**Add-Az VmssDiagnosticsExtension** Cmdlet 會將診斷擴充功能新增到虛擬機器縮放集 (VMSS) 實例。</span><span class="sxs-lookup"><span data-stu-id="bc962-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="bc962-107">例子</span><span class="sxs-lookup"><span data-stu-id="bc962-107">EXAMPLES</span></span>

### <span data-ttu-id="bc962-108">範例 1：新增診斷擴充功能至 VMSS</span><span class="sxs-lookup"><span data-stu-id="bc962-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="bc962-109">此命令會將診斷擴充功能新增到 VMSS。</span><span class="sxs-lookup"><span data-stu-id="bc962-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="bc962-110">參數</span><span class="sxs-lookup"><span data-stu-id="bc962-110">PARAMETERS</span></span>

### <span data-ttu-id="bc962-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bc962-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="bc962-112">指出此 Cmdlet 是否允許 Azure 來賓代理程式自動更新擴充功能至較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="bc962-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="bc962-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc962-113">-DefaultProfile</span></span>
<span data-ttu-id="bc962-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc962-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc962-115">-強制</span><span class="sxs-lookup"><span data-stu-id="bc962-115">-Force</span></span>
<span data-ttu-id="bc962-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="bc962-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bc962-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc962-117">-Name</span></span>
<span data-ttu-id="bc962-118">指定副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc962-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="bc962-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="bc962-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="bc962-120">指定私人組設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="bc962-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="bc962-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="bc962-121">-SettingFilePath</span></span>
<span data-ttu-id="bc962-122">指定公用組設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="bc962-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="bc962-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bc962-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="bc962-124">指定要用於此 VMSS 的擴充功能版本。</span><span class="sxs-lookup"><span data-stu-id="bc962-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="bc962-125">若要取得版本，請針對 [Type 參數執行 Get-Az解說ExtensionImdlet](./Get-AzVMExtensionImage.md)與 Microsoft.Azure.Diagnostics 值 *與 PublisherName* 參數和IaaSDiagnostics 值。 </span><span class="sxs-lookup"><span data-stu-id="bc962-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="bc962-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bc962-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bc962-127">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="bc962-127">Specify the VMSS object.</span></span>
<span data-ttu-id="bc962-128">您可以使用 [New-AzEvssConfig](./New-AzVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="bc962-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="bc962-129">-確認</span><span class="sxs-lookup"><span data-stu-id="bc962-129">-Confirm</span></span>
<span data-ttu-id="bc962-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bc962-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc962-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc962-131">-WhatIf</span></span>
<span data-ttu-id="bc962-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bc962-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc962-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc962-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc962-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc962-134">CommonParameters</span></span>
<span data-ttu-id="bc962-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bc962-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc962-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc962-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc962-137">輸入</span><span class="sxs-lookup"><span data-stu-id="bc962-137">INPUTS</span></span>

### <span data-ttu-id="bc962-138">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bc962-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="bc962-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bc962-139">System.String</span></span>

### <span data-ttu-id="bc962-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bc962-140">System.Boolean</span></span>

## <span data-ttu-id="bc962-141">輸出</span><span class="sxs-lookup"><span data-stu-id="bc962-141">OUTPUTS</span></span>

### <span data-ttu-id="bc962-142">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bc962-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bc962-143">筆記</span><span class="sxs-lookup"><span data-stu-id="bc962-143">NOTES</span></span>

## <span data-ttu-id="bc962-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc962-144">RELATED LINKS</span></span>

[<span data-ttu-id="bc962-145">Add-AzEvssExtension</span><span class="sxs-lookup"><span data-stu-id="bc962-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="bc962-146">Remove-AzEvssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bc962-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="bc962-147">Set-AzMSDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bc962-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
