---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: 5eaf09aec561ed1fff37d2687253634bd1efc921
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956857"
---
# <span data-ttu-id="c330b-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c330b-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="c330b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c330b-102">SYNOPSIS</span></span>
<span data-ttu-id="c330b-103">將 VMAccess 延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c330b-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="c330b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c330b-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c330b-105">說明</span><span class="sxs-lookup"><span data-stu-id="c330b-105">DESCRIPTION</span></span>
<span data-ttu-id="c330b-106">**AzVMAccessExtension** Cmdlet 會將虛擬機器存取 (VMAccess) 虛擬電腦 VMAccess 擴展新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c330b-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="c330b-107">VMAccess 延伸可以用來設定暫時的密碼，而且應該在登入電腦後立即變更它。</span><span class="sxs-lookup"><span data-stu-id="c330b-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="c330b-108">Windows 網網域控制站不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="c330b-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="c330b-109">示例</span><span class="sxs-lookup"><span data-stu-id="c330b-109">EXAMPLES</span></span>

### <span data-ttu-id="c330b-110">範例1：新增 VMAccess 延伸</span><span class="sxs-lookup"><span data-stu-id="c330b-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.4" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="c330b-111">這個命令會在 ResourceGroup11 中為名為 VirtualMachine07 的虛擬機器新增 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="c330b-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>
<span data-ttu-id="c330b-112">此命令會指定 VMAccess 的 name 和 type 處理常式版本。</span><span class="sxs-lookup"><span data-stu-id="c330b-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="c330b-113">參數</span><span class="sxs-lookup"><span data-stu-id="c330b-113">PARAMETERS</span></span>

### <span data-ttu-id="c330b-114">-認證</span><span class="sxs-lookup"><span data-stu-id="c330b-114">-Credential</span></span>
<span data-ttu-id="c330b-115">指定虛擬機器的使用者名稱和密碼作為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="c330b-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="c330b-116">如果您輸入的名稱與您 VM 上目前的本機系統管理員帳戶不同，VMAccess 延伸將會新增該名稱的本機系統管理員帳戶，並將您指定的密碼指派給該帳戶。</span><span class="sxs-lookup"><span data-stu-id="c330b-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="c330b-117">如果您 VM 上的本機系統管理員帳戶存在，將會重設密碼，如果該帳戶已停用，則 VMAccess 延伸啟用該帳戶。</span><span class="sxs-lookup"><span data-stu-id="c330b-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="c330b-118">若要取得認證，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c330b-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="c330b-119">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="c330b-119">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="c330b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c330b-120">-DefaultProfile</span></span>
<span data-ttu-id="c330b-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c330b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c330b-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c330b-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="c330b-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="c330b-123">-ForceRerun</span></span>
<span data-ttu-id="c330b-124">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="c330b-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="c330b-125">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="c330b-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="c330b-126">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="c330b-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="c330b-127">-位置</span><span class="sxs-lookup"><span data-stu-id="c330b-127">-Location</span></span>
<span data-ttu-id="c330b-128">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="c330b-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="c330b-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="c330b-129">-Name</span></span>
<span data-ttu-id="c330b-130">指定此 Cmdlet 所新增之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="c330b-130">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="c330b-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c330b-131">-NoWait</span></span>
<span data-ttu-id="c330b-132">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="c330b-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="c330b-133">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="c330b-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="c330b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c330b-134">-ResourceGroupName</span></span>
<span data-ttu-id="c330b-135">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c330b-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c330b-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c330b-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="c330b-137">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="c330b-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="c330b-138">若要取得版本，請使用 Microsoft 的值來執行 Get-AzVMExtensionImage Cmdlet。針對 *PublisherName* 參數和 VMAccessAgent （針對 *Type* 參數）進行計算。</span><span class="sxs-lookup"><span data-stu-id="c330b-138">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="c330b-139">TypeHandlerVersion 必須是2.0 或更高版本，因為版本1已過時。</span><span class="sxs-lookup"><span data-stu-id="c330b-139">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="c330b-140">-VMName</span><span class="sxs-lookup"><span data-stu-id="c330b-140">-VMName</span></span>
<span data-ttu-id="c330b-141">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c330b-141">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c330b-142">這個 Cmdlet 會為此參數指定的虛擬機器新增 VMAccess。</span><span class="sxs-lookup"><span data-stu-id="c330b-142">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="c330b-143">-確認</span><span class="sxs-lookup"><span data-stu-id="c330b-143">-Confirm</span></span>
<span data-ttu-id="c330b-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c330b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c330b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c330b-145">-WhatIf</span></span>
<span data-ttu-id="c330b-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c330b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c330b-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c330b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c330b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c330b-148">CommonParameters</span></span>
<span data-ttu-id="c330b-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c330b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c330b-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c330b-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c330b-151">輸入</span><span class="sxs-lookup"><span data-stu-id="c330b-151">INPUTS</span></span>

### <span data-ttu-id="c330b-152">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="c330b-152">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="c330b-153">System.object</span><span class="sxs-lookup"><span data-stu-id="c330b-153">System.String</span></span>

### <span data-ttu-id="c330b-154">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="c330b-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c330b-155">輸出</span><span class="sxs-lookup"><span data-stu-id="c330b-155">OUTPUTS</span></span>

### <span data-ttu-id="c330b-156">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="c330b-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c330b-157">筆記</span><span class="sxs-lookup"><span data-stu-id="c330b-157">NOTES</span></span>

## <span data-ttu-id="c330b-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="c330b-158">RELATED LINKS</span></span>

[<span data-ttu-id="c330b-159">AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c330b-159">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="c330b-160">移除-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c330b-160">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="c330b-161">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="c330b-161">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="c330b-162">AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="c330b-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


