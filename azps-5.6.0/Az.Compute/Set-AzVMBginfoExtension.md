---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: 9b8eafaead04c2e2f727676c78bd717b1c6e97c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913254"
---
# <span data-ttu-id="336af-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="336af-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="336af-102">簡介</span><span class="sxs-lookup"><span data-stu-id="336af-102">SYNOPSIS</span></span>
<span data-ttu-id="336af-103">將 BGInfo 擴充功能新增到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="336af-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="336af-104">語法</span><span class="sxs-lookup"><span data-stu-id="336af-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="336af-105">描述</span><span class="sxs-lookup"><span data-stu-id="336af-105">DESCRIPTION</span></span>
<span data-ttu-id="336af-106">**Set-AzVMBGInfoExtension** Cmdlet 會將 BGInfo 擴充功能新增到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="336af-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="336af-107">例子</span><span class="sxs-lookup"><span data-stu-id="336af-107">EXAMPLES</span></span>

### <span data-ttu-id="336af-108">範例 1：新增虛擬機器的 BGInfo 擴充功能</span><span class="sxs-lookup"><span data-stu-id="336af-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="336af-109">此命令會將 BGInfo 擴充功能新增到名為 Contoso VIRTUAL 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="336af-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="336af-110">命令會指定虛擬機器的資源群組和位置。</span><span class="sxs-lookup"><span data-stu-id="336af-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="336af-111">命令會指定副檔名的名稱及版本。</span><span class="sxs-lookup"><span data-stu-id="336af-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="336af-112">參數</span><span class="sxs-lookup"><span data-stu-id="336af-112">PARAMETERS</span></span>

### <span data-ttu-id="336af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="336af-113">-DefaultProfile</span></span>
<span data-ttu-id="336af-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="336af-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="336af-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="336af-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="336af-116">表示此 Cmdlet 可防止 Azure 來賓代理程式自動更新擴充功能至較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="336af-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="336af-117">根據預設，此 Cmdlet 可讓來賓代理程式更新擴充功能。</span><span class="sxs-lookup"><span data-stu-id="336af-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336af-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="336af-118">-ForceRerun</span></span>
<span data-ttu-id="336af-119">指定應該使用相同的公用或受保護的設定再次執行擴充功能。</span><span class="sxs-lookup"><span data-stu-id="336af-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="336af-120">該值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="336af-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="336af-121">如果未變更 forceUpdateTag，處理常式仍然會使用公用或受保護的設定更新。</span><span class="sxs-lookup"><span data-stu-id="336af-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336af-122">-位置</span><span class="sxs-lookup"><span data-stu-id="336af-122">-Location</span></span>
<span data-ttu-id="336af-123">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="336af-123">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336af-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="336af-124">-Name</span></span>
<span data-ttu-id="336af-125">指定此 Cmdlet 新增到虛擬機器的 BGInfo 副檔名。</span><span class="sxs-lookup"><span data-stu-id="336af-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336af-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="336af-126">-NoWait</span></span>
<span data-ttu-id="336af-127">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="336af-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="336af-128">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="336af-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="336af-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="336af-129">-ResourceGroupName</span></span>
<span data-ttu-id="336af-130">指定此 Cmdlet 新增擴充功能之虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="336af-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="336af-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="336af-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="336af-132">指定此 Cmdlet 新增到虛擬機器的擴充功能版本。</span><span class="sxs-lookup"><span data-stu-id="336af-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336af-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="336af-133">-VMName</span></span>
<span data-ttu-id="336af-134">指定此 Cmdlet 新增 BGInfo 副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="336af-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="336af-135">-確認</span><span class="sxs-lookup"><span data-stu-id="336af-135">-Confirm</span></span>
<span data-ttu-id="336af-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="336af-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="336af-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="336af-137">-WhatIf</span></span>
<span data-ttu-id="336af-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="336af-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="336af-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="336af-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="336af-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336af-140">CommonParameters</span></span>
<span data-ttu-id="336af-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="336af-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336af-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="336af-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336af-143">輸入</span><span class="sxs-lookup"><span data-stu-id="336af-143">INPUTS</span></span>

### <span data-ttu-id="336af-144">System.String</span><span class="sxs-lookup"><span data-stu-id="336af-144">System.String</span></span>

### <span data-ttu-id="336af-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="336af-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="336af-146">輸出</span><span class="sxs-lookup"><span data-stu-id="336af-146">OUTPUTS</span></span>

### <span data-ttu-id="336af-147">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="336af-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="336af-148">筆記</span><span class="sxs-lookup"><span data-stu-id="336af-148">NOTES</span></span>

## <span data-ttu-id="336af-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="336af-149">RELATED LINKS</span></span>
