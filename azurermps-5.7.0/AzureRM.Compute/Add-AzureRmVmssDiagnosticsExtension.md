---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 0e28b5df77734645380316af6396f745469637df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450687"
---
# <span data-ttu-id="d6945-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d6945-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="d6945-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d6945-102">SYNOPSIS</span></span>
<span data-ttu-id="d6945-103">將診斷延伸新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="d6945-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6945-104">句法</span><span class="sxs-lookup"><span data-stu-id="d6945-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6945-105">說明</span><span class="sxs-lookup"><span data-stu-id="d6945-105">DESCRIPTION</span></span>
<span data-ttu-id="d6945-106">**AzureRmVmssDiagnosticsExtension** Cmdlet 會將診斷延伸新增至虛擬電腦比例集 (VMSS) 實例。</span><span class="sxs-lookup"><span data-stu-id="d6945-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="d6945-107">示例</span><span class="sxs-lookup"><span data-stu-id="d6945-107">EXAMPLES</span></span>

### <span data-ttu-id="d6945-108">範例1：在 VMSS 中新增診斷延伸</span><span class="sxs-lookup"><span data-stu-id="d6945-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="d6945-109">這個命令會將診斷延伸新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="d6945-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="d6945-110">參數</span><span class="sxs-lookup"><span data-stu-id="d6945-110">PARAMETERS</span></span>

### <span data-ttu-id="d6945-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d6945-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d6945-112">指示此 Cmdlet 是否允許 Azure 來賓代理程式自動將延伸更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="d6945-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6945-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d6945-113">-Force</span></span>
<span data-ttu-id="d6945-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d6945-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6945-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6945-115">-Name</span></span>
<span data-ttu-id="d6945-116">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6945-116">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6945-117">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="d6945-117">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="d6945-118">指定私人設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="d6945-118">Specifies the path of the private configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6945-119">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="d6945-119">-SettingFilePath</span></span>
<span data-ttu-id="d6945-120">指定公用設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="d6945-120">Specifies the path of the public configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6945-121">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d6945-121">-TypeHandlerVersion</span></span>
<span data-ttu-id="d6945-122">指定要用於此 VMSS 的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="d6945-122">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="d6945-123">若要取得版本，請執行 [AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) Cmdlet 與 *PublisherName* 參數的值，以及針對 *Type* 參數 IaaSDiagnostics 的。</span><span class="sxs-lookup"><span data-stu-id="d6945-123">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6945-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d6945-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d6945-125">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="d6945-125">Specify the VMSS object.</span></span>
<span data-ttu-id="d6945-126">您可以使用 [新的-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="d6945-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6945-127">-確認</span><span class="sxs-lookup"><span data-stu-id="d6945-127">-Confirm</span></span>
<span data-ttu-id="d6945-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d6945-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6945-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6945-129">-WhatIf</span></span>
<span data-ttu-id="d6945-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6945-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6945-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6945-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6945-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6945-132">CommonParameters</span></span>
<span data-ttu-id="d6945-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d6945-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6945-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d6945-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6945-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d6945-135">INPUTS</span></span>

### <span data-ttu-id="d6945-136">所有</span><span class="sxs-lookup"><span data-stu-id="d6945-136">None</span></span>
<span data-ttu-id="d6945-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d6945-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d6945-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d6945-138">OUTPUTS</span></span>

###  
<span data-ttu-id="d6945-139">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d6945-139">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d6945-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d6945-140">NOTES</span></span>

## <span data-ttu-id="d6945-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6945-141">RELATED LINKS</span></span>

[<span data-ttu-id="d6945-142">附加 AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d6945-142">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="d6945-143">移除-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d6945-143">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="d6945-144">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d6945-144">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
