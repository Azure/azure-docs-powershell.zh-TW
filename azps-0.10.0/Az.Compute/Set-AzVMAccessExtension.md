---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0335a063e810a94e6d557986e682ec4c777e5c1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795902"
---
# <span data-ttu-id="957af-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="957af-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="957af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="957af-102">SYNOPSIS</span></span>
<span data-ttu-id="957af-103">將 VMAccess 延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="957af-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="957af-104">句法</span><span class="sxs-lookup"><span data-stu-id="957af-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="957af-105">說明</span><span class="sxs-lookup"><span data-stu-id="957af-105">DESCRIPTION</span></span>
<span data-ttu-id="957af-106">**AzVMAccessExtension** Cmdlet 會將虛擬機器存取 (VMAccess) 虛擬電腦 VMAccess 擴展新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="957af-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="957af-107">VMAccess 延伸可以用來設定暫時的密碼，而且應該在登入電腦後立即變更它。</span><span class="sxs-lookup"><span data-stu-id="957af-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="957af-108">示例</span><span class="sxs-lookup"><span data-stu-id="957af-108">EXAMPLES</span></span>

### <span data-ttu-id="957af-109">範例1：新增 VMAccess 延伸</span><span class="sxs-lookup"><span data-stu-id="957af-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="957af-110">這個命令會在 ResrouceGroup11 中為名為 VirtualMachine07 的虛擬機器新增 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="957af-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="957af-111">此命令會指定 VMAccess 的 name 和 type 處理常式版本。</span><span class="sxs-lookup"><span data-stu-id="957af-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="957af-112">參數</span><span class="sxs-lookup"><span data-stu-id="957af-112">PARAMETERS</span></span>

### <span data-ttu-id="957af-113">-認證</span><span class="sxs-lookup"><span data-stu-id="957af-113">-Credential</span></span>
<span data-ttu-id="957af-114">指定虛擬機器的使用者名稱和密碼作為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="957af-114">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="957af-115">若要取得認證，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="957af-115">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="957af-116">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="957af-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="957af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="957af-117">-DefaultProfile</span></span>
<span data-ttu-id="957af-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="957af-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="957af-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="957af-119">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="957af-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="957af-120">-ForceRerun</span></span>
<span data-ttu-id="957af-121">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="957af-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="957af-122">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="957af-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="957af-123">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="957af-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="957af-124">-位置</span><span class="sxs-lookup"><span data-stu-id="957af-124">-Location</span></span>
<span data-ttu-id="957af-125">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="957af-125">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="957af-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="957af-126">-Name</span></span>
<span data-ttu-id="957af-127">指定此 Cmdlet 所新增之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="957af-127">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="957af-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="957af-128">-ResourceGroupName</span></span>
<span data-ttu-id="957af-129">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="957af-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="957af-130">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="957af-130">-TypeHandlerVersion</span></span>
<span data-ttu-id="957af-131">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="957af-131">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="957af-132">若要取得版本，請使用 Microsoft 的值來執行 Get-AzVMExtensionImage Cmdlet。針對 *PublisherName* 參數和 VMAccessAgent （針對 *Type* 參數）進行計算。</span><span class="sxs-lookup"><span data-stu-id="957af-132">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="957af-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="957af-133">-VMName</span></span>
<span data-ttu-id="957af-134">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="957af-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="957af-135">這個 Cmdlet 會為此參數指定的虛擬機器新增 VMAccess。</span><span class="sxs-lookup"><span data-stu-id="957af-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="957af-136">-確認</span><span class="sxs-lookup"><span data-stu-id="957af-136">-Confirm</span></span>
<span data-ttu-id="957af-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="957af-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="957af-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="957af-138">-WhatIf</span></span>
<span data-ttu-id="957af-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="957af-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="957af-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="957af-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="957af-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="957af-141">CommonParameters</span></span>
<span data-ttu-id="957af-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="957af-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="957af-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="957af-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="957af-144">輸入</span><span class="sxs-lookup"><span data-stu-id="957af-144">INPUTS</span></span>

### <span data-ttu-id="957af-145">所有</span><span class="sxs-lookup"><span data-stu-id="957af-145">None</span></span>
<span data-ttu-id="957af-146">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="957af-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="957af-147">輸出</span><span class="sxs-lookup"><span data-stu-id="957af-147">OUTPUTS</span></span>

### <span data-ttu-id="957af-148">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="957af-148">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="957af-149">筆記</span><span class="sxs-lookup"><span data-stu-id="957af-149">NOTES</span></span>

## <span data-ttu-id="957af-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="957af-150">RELATED LINKS</span></span>

[<span data-ttu-id="957af-151">AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="957af-151">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="957af-152">移除-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="957af-152">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="957af-153">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="957af-153">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="957af-154">AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="957af-154">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


