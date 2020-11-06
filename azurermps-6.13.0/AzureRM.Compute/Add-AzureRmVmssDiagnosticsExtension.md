---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 4370a7b87ee87b223ddadd6f872b549c2537e1e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450250"
---
# <span data-ttu-id="24e71-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="24e71-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="24e71-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24e71-102">SYNOPSIS</span></span>
<span data-ttu-id="24e71-103">將診斷延伸新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="24e71-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24e71-104">句法</span><span class="sxs-lookup"><span data-stu-id="24e71-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24e71-105">說明</span><span class="sxs-lookup"><span data-stu-id="24e71-105">DESCRIPTION</span></span>
<span data-ttu-id="24e71-106">**AzureRmVmssDiagnosticsExtension** Cmdlet 會將診斷延伸新增至虛擬電腦比例集 (VMSS) 實例。</span><span class="sxs-lookup"><span data-stu-id="24e71-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="24e71-107">示例</span><span class="sxs-lookup"><span data-stu-id="24e71-107">EXAMPLES</span></span>

### <span data-ttu-id="24e71-108">範例1：在 VMSS 中新增診斷延伸</span><span class="sxs-lookup"><span data-stu-id="24e71-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="24e71-109">這個命令會將診斷延伸新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="24e71-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="24e71-110">參數</span><span class="sxs-lookup"><span data-stu-id="24e71-110">PARAMETERS</span></span>

### <span data-ttu-id="24e71-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="24e71-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="24e71-112">指示此 Cmdlet 是否允許 Azure 來賓代理程式自動將延伸更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="24e71-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="24e71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e71-113">-DefaultProfile</span></span>
<span data-ttu-id="24e71-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24e71-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e71-115">-Force</span><span class="sxs-lookup"><span data-stu-id="24e71-115">-Force</span></span>
<span data-ttu-id="24e71-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="24e71-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="24e71-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="24e71-117">-Name</span></span>
<span data-ttu-id="24e71-118">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="24e71-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="24e71-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="24e71-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="24e71-120">指定私人設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="24e71-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="24e71-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="24e71-121">-SettingFilePath</span></span>
<span data-ttu-id="24e71-122">指定公用設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="24e71-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="24e71-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="24e71-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="24e71-124">指定要用於此 VMSS 的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="24e71-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="24e71-125">若要取得版本，請執行 [AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) Cmdlet 與 *PublisherName* 參數的值，以及針對 *Type* 參數 IaaSDiagnostics 的。</span><span class="sxs-lookup"><span data-stu-id="24e71-125">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="24e71-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="24e71-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="24e71-127">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="24e71-127">Specify the VMSS object.</span></span>
<span data-ttu-id="24e71-128">您可以使用 [新的-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="24e71-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="24e71-129">-確認</span><span class="sxs-lookup"><span data-stu-id="24e71-129">-Confirm</span></span>
<span data-ttu-id="24e71-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24e71-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24e71-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24e71-131">-WhatIf</span></span>
<span data-ttu-id="24e71-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24e71-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24e71-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24e71-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24e71-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e71-134">CommonParameters</span></span>
<span data-ttu-id="24e71-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24e71-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e71-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24e71-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e71-137">輸入</span><span class="sxs-lookup"><span data-stu-id="24e71-137">INPUTS</span></span>

### <span data-ttu-id="24e71-138">VirtualMachineScaleSet 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="24e71-138">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

### <span data-ttu-id="24e71-139">System.object</span><span class="sxs-lookup"><span data-stu-id="24e71-139">System.String</span></span>

### <span data-ttu-id="24e71-140">System.object</span><span class="sxs-lookup"><span data-stu-id="24e71-140">System.Boolean</span></span>

## <span data-ttu-id="24e71-141">輸出</span><span class="sxs-lookup"><span data-stu-id="24e71-141">OUTPUTS</span></span>

### <span data-ttu-id="24e71-142">VirtualMachineScaleSet 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="24e71-142">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="24e71-143">筆記</span><span class="sxs-lookup"><span data-stu-id="24e71-143">NOTES</span></span>

## <span data-ttu-id="24e71-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="24e71-144">RELATED LINKS</span></span>

[<span data-ttu-id="24e71-145">附加 AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="24e71-145">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="24e71-146">移除-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="24e71-146">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="24e71-147">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="24e71-147">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
