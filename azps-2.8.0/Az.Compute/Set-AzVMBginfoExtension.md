---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: a008281b6406bce8917c2b3997d9f14e5daf18ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613163"
---
# <span data-ttu-id="02f41-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="02f41-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="02f41-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02f41-102">SYNOPSIS</span></span>
<span data-ttu-id="02f41-103">將 BGInfo 延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="02f41-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="02f41-104">句法</span><span class="sxs-lookup"><span data-stu-id="02f41-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02f41-105">說明</span><span class="sxs-lookup"><span data-stu-id="02f41-105">DESCRIPTION</span></span>
<span data-ttu-id="02f41-106">**AzVMBGInfoExtension** Cmdlet 會將 BGInfo 延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="02f41-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="02f41-107">示例</span><span class="sxs-lookup"><span data-stu-id="02f41-107">EXAMPLES</span></span>

### <span data-ttu-id="02f41-108">範例1：為虛擬機器新增 BGInfo 延伸</span><span class="sxs-lookup"><span data-stu-id="02f41-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="02f41-109">這個命令會將 BGInfo 延伸新增到名為 ContosoVM 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="02f41-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="02f41-110">命令會指定虛擬機器的資源群組和位置。</span><span class="sxs-lookup"><span data-stu-id="02f41-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="02f41-111">該命令會指定延伸的名稱和版本。</span><span class="sxs-lookup"><span data-stu-id="02f41-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="02f41-112">參數</span><span class="sxs-lookup"><span data-stu-id="02f41-112">PARAMETERS</span></span>

### <span data-ttu-id="02f41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f41-113">-DefaultProfile</span></span>
<span data-ttu-id="02f41-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="02f41-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02f41-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="02f41-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="02f41-116">表示此 Cmdlet 可防止 Azure 來賓代理程式自動將延伸更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="02f41-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="02f41-117">根據預設，這個 Cmdlet 可讓來賓代理程式更新延伸。</span><span class="sxs-lookup"><span data-stu-id="02f41-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="02f41-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="02f41-118">-ForceRerun</span></span>
<span data-ttu-id="02f41-119">指定應該使用相同的公用或受保護設定來再次執行延伸。</span><span class="sxs-lookup"><span data-stu-id="02f41-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="02f41-120">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="02f41-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="02f41-121">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="02f41-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="02f41-122">-位置</span><span class="sxs-lookup"><span data-stu-id="02f41-122">-Location</span></span>
<span data-ttu-id="02f41-123">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="02f41-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="02f41-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="02f41-124">-Name</span></span>
<span data-ttu-id="02f41-125">指定此 Cmdlet 新增至虛擬機器之 BGInfo 延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="02f41-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="02f41-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="02f41-126">-NoWait</span></span>
<span data-ttu-id="02f41-127">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="02f41-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="02f41-128">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="02f41-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="02f41-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02f41-129">-ResourceGroupName</span></span>
<span data-ttu-id="02f41-130">指定此 Cmdlet 新增副檔名的虛擬機器資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="02f41-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="02f41-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="02f41-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="02f41-132">指定此 Cmdlet 新增至虛擬機器的延伸版本。</span><span class="sxs-lookup"><span data-stu-id="02f41-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="02f41-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="02f41-133">-VMName</span></span>
<span data-ttu-id="02f41-134">指定此 Cmdlet 新增 BGInfo 延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="02f41-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="02f41-135">-確認</span><span class="sxs-lookup"><span data-stu-id="02f41-135">-Confirm</span></span>
<span data-ttu-id="02f41-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="02f41-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02f41-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02f41-137">-WhatIf</span></span>
<span data-ttu-id="02f41-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02f41-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02f41-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02f41-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02f41-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f41-140">CommonParameters</span></span>
<span data-ttu-id="02f41-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02f41-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f41-142">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="02f41-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f41-143">輸入</span><span class="sxs-lookup"><span data-stu-id="02f41-143">INPUTS</span></span>

### <span data-ttu-id="02f41-144">System.object</span><span class="sxs-lookup"><span data-stu-id="02f41-144">System.String</span></span>

### <span data-ttu-id="02f41-145">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="02f41-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="02f41-146">輸出</span><span class="sxs-lookup"><span data-stu-id="02f41-146">OUTPUTS</span></span>

### <span data-ttu-id="02f41-147">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="02f41-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="02f41-148">筆記</span><span class="sxs-lookup"><span data-stu-id="02f41-148">NOTES</span></span>

## <span data-ttu-id="02f41-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="02f41-149">RELATED LINKS</span></span>