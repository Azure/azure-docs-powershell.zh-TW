---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0b91e2892f087da6eb510d087980e6f31dd67ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622684"
---
# <span data-ttu-id="1fcaf-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1fcaf-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="1fcaf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fcaf-102">SYNOPSIS</span></span>
<span data-ttu-id="1fcaf-103">將 VMAccess 延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="1fcaf-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fcaf-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fcaf-105">說明</span><span class="sxs-lookup"><span data-stu-id="1fcaf-105">DESCRIPTION</span></span>
<span data-ttu-id="1fcaf-106">**AzVMAccessExtension** Cmdlet 會將虛擬機器存取 (VMAccess) 虛擬電腦 VMAccess 擴展新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="1fcaf-107">VMAccess 延伸可以用來設定暫時的密碼，而且應該在登入電腦後立即變更它。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="1fcaf-108">Windows 網網域控制站不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="1fcaf-109">示例</span><span class="sxs-lookup"><span data-stu-id="1fcaf-109">EXAMPLES</span></span>

### <span data-ttu-id="1fcaf-110">範例1：新增 VMAccess 延伸</span><span class="sxs-lookup"><span data-stu-id="1fcaf-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="1fcaf-111">這個命令會在 ResrouceGroup11 中為名為 VirtualMachine07 的虛擬機器新增 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="1fcaf-112">此命令會指定 VMAccess 的 name 和 type 處理常式版本。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="1fcaf-113">參數</span><span class="sxs-lookup"><span data-stu-id="1fcaf-113">PARAMETERS</span></span>

### <span data-ttu-id="1fcaf-114">-認證</span><span class="sxs-lookup"><span data-stu-id="1fcaf-114">-Credential</span></span>
<span data-ttu-id="1fcaf-115">指定虛擬機器的使用者名稱和密碼作為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="1fcaf-116">如果您輸入的名稱與您 VM 上目前的本機系統管理員帳戶不同，VMAccess 延伸將會新增該名稱的本機系統管理員帳戶，並將您指定的密碼指派給該帳戶。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="1fcaf-117">如果您 VM 上的本機系統管理員帳戶存在，將會重設密碼，如果該帳戶已停用，則 VMAccess 延伸啟用該帳戶。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="1fcaf-118">若要取得認證，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="1fcaf-119">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-119">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fcaf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fcaf-120">-DefaultProfile</span></span>
<span data-ttu-id="1fcaf-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fcaf-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1fcaf-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="1fcaf-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="1fcaf-123">-ForceRerun</span></span>
<span data-ttu-id="1fcaf-124">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="1fcaf-125">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="1fcaf-126">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="1fcaf-127">-位置</span><span class="sxs-lookup"><span data-stu-id="1fcaf-127">-Location</span></span>
<span data-ttu-id="1fcaf-128">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="1fcaf-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="1fcaf-129">-Name</span></span>
<span data-ttu-id="1fcaf-130">指定此 Cmdlet 所新增之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-130">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="1fcaf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fcaf-131">-ResourceGroupName</span></span>
<span data-ttu-id="1fcaf-132">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-132">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1fcaf-133">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1fcaf-133">-TypeHandlerVersion</span></span>
<span data-ttu-id="1fcaf-134">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-134">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="1fcaf-135">若要取得版本，請使用 Microsoft 的值來執行 Get-AzVMExtensionImage Cmdlet。針對 *PublisherName* 參數和 VMAccessAgent （針對 *Type* 參數）進行計算。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-135">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="1fcaf-136">TypeHandlerVersion 必須是2.0 或更高版本，因為版本1已過時。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-136">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="1fcaf-137">-VMName</span><span class="sxs-lookup"><span data-stu-id="1fcaf-137">-VMName</span></span>
<span data-ttu-id="1fcaf-138">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-138">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1fcaf-139">這個 Cmdlet 會為此參數指定的虛擬機器新增 VMAccess。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-139">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1fcaf-140">-確認</span><span class="sxs-lookup"><span data-stu-id="1fcaf-140">-Confirm</span></span>
<span data-ttu-id="1fcaf-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fcaf-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fcaf-142">-WhatIf</span></span>
<span data-ttu-id="1fcaf-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fcaf-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fcaf-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fcaf-145">CommonParameters</span></span>
<span data-ttu-id="1fcaf-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fcaf-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1fcaf-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fcaf-148">輸入</span><span class="sxs-lookup"><span data-stu-id="1fcaf-148">INPUTS</span></span>

### <span data-ttu-id="1fcaf-149">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="1fcaf-149">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="1fcaf-150">System.object</span><span class="sxs-lookup"><span data-stu-id="1fcaf-150">System.String</span></span>

### <span data-ttu-id="1fcaf-151">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="1fcaf-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1fcaf-152">輸出</span><span class="sxs-lookup"><span data-stu-id="1fcaf-152">OUTPUTS</span></span>

### <span data-ttu-id="1fcaf-153">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="1fcaf-153">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1fcaf-154">筆記</span><span class="sxs-lookup"><span data-stu-id="1fcaf-154">NOTES</span></span>

## <span data-ttu-id="1fcaf-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fcaf-155">RELATED LINKS</span></span>

[<span data-ttu-id="1fcaf-156">AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1fcaf-156">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="1fcaf-157">移除-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1fcaf-157">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="1fcaf-158">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1fcaf-158">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="1fcaf-159">AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="1fcaf-159">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


