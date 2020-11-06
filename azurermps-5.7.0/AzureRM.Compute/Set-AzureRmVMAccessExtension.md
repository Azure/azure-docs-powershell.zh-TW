---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: 6c24c01ebff1d0a74835b968640caea6b5d2b308
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444695"
---
# <span data-ttu-id="5ebfb-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5ebfb-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="5ebfb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ebfb-102">SYNOPSIS</span></span>
<span data-ttu-id="5ebfb-103">將 VMAccess 延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ebfb-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ebfb-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-UserName <String>] [-Password <String>] [-ResourceGroupName] <String>
 [-VMName] <String> [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ebfb-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ebfb-105">DESCRIPTION</span></span>
<span data-ttu-id="5ebfb-106">**AzureRmVMAccessExtension** Cmdlet 會將虛擬機器存取 (VMAccess) 虛擬電腦 VMAccess 擴展新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="5ebfb-107">VMAccess 延伸可以用來設定暫時的密碼，而且應該在登入電腦後立即變更它。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="5ebfb-108">示例</span><span class="sxs-lookup"><span data-stu-id="5ebfb-108">EXAMPLES</span></span>

### <span data-ttu-id="5ebfb-109">範例1：新增 VMAccess 延伸</span><span class="sxs-lookup"><span data-stu-id="5ebfb-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="5ebfb-110">這個命令會在 ResrouceGroup11 中為名為 VirtualMachine07 的虛擬機器新增 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="5ebfb-111">此命令會指定 VMAccess 的 name 和 type 處理常式版本。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="5ebfb-112">參數</span><span class="sxs-lookup"><span data-stu-id="5ebfb-112">PARAMETERS</span></span>

### <span data-ttu-id="5ebfb-113">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5ebfb-113">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebfb-114">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="5ebfb-114">-ForceRerun</span></span>
<span data-ttu-id="5ebfb-115">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-115">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="5ebfb-116">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-116">The value can be any string different from the current value.</span></span>

<span data-ttu-id="5ebfb-117">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-117">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebfb-118">-位置</span><span class="sxs-lookup"><span data-stu-id="5ebfb-118">-Location</span></span>
<span data-ttu-id="5ebfb-119">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-119">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebfb-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ebfb-120">-Name</span></span>
<span data-ttu-id="5ebfb-121">指定此 Cmdlet 所新增之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-121">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebfb-122">-Password</span><span class="sxs-lookup"><span data-stu-id="5ebfb-122">-Password</span></span>
<span data-ttu-id="5ebfb-123">指定虛擬機器的新密碼。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-123">Specifies the new password of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebfb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ebfb-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ebfb-125">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebfb-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5ebfb-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="5ebfb-127">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-127">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="5ebfb-128">若要取得版本，請使用 Microsoft 的值來執行 Get-AzureRmVMExtensionImage Cmdlet。針對 *PublisherName* 參數和 VMAccessAgent （針對 *Type* 參數）進行計算。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-128">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebfb-129">-UserName</span><span class="sxs-lookup"><span data-stu-id="5ebfb-129">-UserName</span></span>
<span data-ttu-id="5ebfb-130">指定虛擬機器的新使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-130">Specifies the new user name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebfb-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="5ebfb-131">-VMName</span></span>
<span data-ttu-id="5ebfb-132">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-132">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5ebfb-133">這個 Cmdlet 會為此參數指定的虛擬機器新增 VMAccess。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-133">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebfb-134">-確認</span><span class="sxs-lookup"><span data-stu-id="5ebfb-134">-Confirm</span></span>
<span data-ttu-id="5ebfb-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ebfb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ebfb-136">-WhatIf</span></span>
<span data-ttu-id="5ebfb-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-137">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5ebfb-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ebfb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ebfb-139">CommonParameters</span></span>
<span data-ttu-id="5ebfb-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ebfb-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ebfb-142">輸入</span><span class="sxs-lookup"><span data-stu-id="5ebfb-142">INPUTS</span></span>

### <span data-ttu-id="5ebfb-143">所有</span><span class="sxs-lookup"><span data-stu-id="5ebfb-143">None</span></span>
<span data-ttu-id="5ebfb-144">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5ebfb-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5ebfb-145">輸出</span><span class="sxs-lookup"><span data-stu-id="5ebfb-145">OUTPUTS</span></span>

## <span data-ttu-id="5ebfb-146">筆記</span><span class="sxs-lookup"><span data-stu-id="5ebfb-146">NOTES</span></span>

## <span data-ttu-id="5ebfb-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ebfb-147">RELATED LINKS</span></span>

[<span data-ttu-id="5ebfb-148">AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5ebfb-148">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="5ebfb-149">移除-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5ebfb-149">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="5ebfb-150">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="5ebfb-150">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="5ebfb-151">AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="5ebfb-151">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


