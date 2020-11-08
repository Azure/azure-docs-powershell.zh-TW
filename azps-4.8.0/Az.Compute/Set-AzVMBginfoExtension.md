---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: a98a2f5cbc8034e8cec4d324bb7ecaa28297e772
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128356"
---
# <span data-ttu-id="d81f4-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="d81f4-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="d81f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d81f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d81f4-103">將 BGInfo 延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d81f4-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="d81f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="d81f4-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d81f4-105">說明</span><span class="sxs-lookup"><span data-stu-id="d81f4-105">DESCRIPTION</span></span>
<span data-ttu-id="d81f4-106">**AzVMBGInfoExtension** Cmdlet 會將 BGInfo 延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d81f4-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="d81f4-107">示例</span><span class="sxs-lookup"><span data-stu-id="d81f4-107">EXAMPLES</span></span>

### <span data-ttu-id="d81f4-108">範例1：為虛擬機器新增 BGInfo 延伸</span><span class="sxs-lookup"><span data-stu-id="d81f4-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="d81f4-109">這個命令會將 BGInfo 延伸新增到名為 ContosoVM 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d81f4-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="d81f4-110">命令會指定虛擬機器的資源群組和位置。</span><span class="sxs-lookup"><span data-stu-id="d81f4-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="d81f4-111">該命令會指定延伸的名稱和版本。</span><span class="sxs-lookup"><span data-stu-id="d81f4-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="d81f4-112">參數</span><span class="sxs-lookup"><span data-stu-id="d81f4-112">PARAMETERS</span></span>

### <span data-ttu-id="d81f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d81f4-113">-DefaultProfile</span></span>
<span data-ttu-id="d81f4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d81f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d81f4-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d81f4-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d81f4-116">表示此 Cmdlet 可防止 Azure 來賓代理程式自動將延伸更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="d81f4-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="d81f4-117">根據預設，這個 Cmdlet 可讓來賓代理程式更新延伸。</span><span class="sxs-lookup"><span data-stu-id="d81f4-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="d81f4-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="d81f4-118">-ForceRerun</span></span>
<span data-ttu-id="d81f4-119">指定應該使用相同的公用或受保護設定來再次執行延伸。</span><span class="sxs-lookup"><span data-stu-id="d81f4-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="d81f4-120">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="d81f4-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="d81f4-121">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="d81f4-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="d81f4-122">-位置</span><span class="sxs-lookup"><span data-stu-id="d81f4-122">-Location</span></span>
<span data-ttu-id="d81f4-123">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="d81f4-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="d81f4-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d81f4-124">-Name</span></span>
<span data-ttu-id="d81f4-125">指定此 Cmdlet 新增至虛擬機器之 BGInfo 延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="d81f4-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="d81f4-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d81f4-126">-NoWait</span></span>
<span data-ttu-id="d81f4-127">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="d81f4-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d81f4-128">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="d81f4-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d81f4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d81f4-129">-ResourceGroupName</span></span>
<span data-ttu-id="d81f4-130">指定此 Cmdlet 新增副檔名的虛擬機器資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d81f4-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="d81f4-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d81f4-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="d81f4-132">指定此 Cmdlet 新增至虛擬機器的延伸版本。</span><span class="sxs-lookup"><span data-stu-id="d81f4-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="d81f4-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="d81f4-133">-VMName</span></span>
<span data-ttu-id="d81f4-134">指定此 Cmdlet 新增 BGInfo 延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="d81f4-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="d81f4-135">-確認</span><span class="sxs-lookup"><span data-stu-id="d81f4-135">-Confirm</span></span>
<span data-ttu-id="d81f4-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d81f4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d81f4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d81f4-137">-WhatIf</span></span>
<span data-ttu-id="d81f4-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d81f4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d81f4-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d81f4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d81f4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d81f4-140">CommonParameters</span></span>
<span data-ttu-id="d81f4-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d81f4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d81f4-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d81f4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d81f4-143">輸入</span><span class="sxs-lookup"><span data-stu-id="d81f4-143">INPUTS</span></span>

### <span data-ttu-id="d81f4-144">System.object</span><span class="sxs-lookup"><span data-stu-id="d81f4-144">System.String</span></span>

### <span data-ttu-id="d81f4-145">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="d81f4-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d81f4-146">輸出</span><span class="sxs-lookup"><span data-stu-id="d81f4-146">OUTPUTS</span></span>

### <span data-ttu-id="d81f4-147">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="d81f4-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d81f4-148">筆記</span><span class="sxs-lookup"><span data-stu-id="d81f4-148">NOTES</span></span>

## <span data-ttu-id="d81f4-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="d81f4-149">RELATED LINKS</span></span>
